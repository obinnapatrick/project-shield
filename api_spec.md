_This is a draft specification for the Project SHIELD verification endpoint. It is intended for public review and is subject to change._

# API Specification: Verification Service

## Endpoint

The core verification service consists of a single, stateless POST endpoint.

`POST /verify-right-to-work`

## Request Body

The request body must contain a JSON object with a single field: `verifiablePresentation`. This field holds the Zero-Knowledge Proof (ZKP) or other cryptographic proof derived from the individual's Verifiable Credential.

**Sample Request:**

```json
{
  "verifiablePresentation": {
    "@context": ["https://www.w3.org/2018/credentials/v1"],
    "type": ["VerifiablePresentation"],
    "proof": {
      "type": "ZkProof",
      "challenge": "a1b2c3d4-e5f6-7890-1234-567890abcdef",
      "proofValue": "0xabcdef1234567890..."
    }
  }
}
```

**Note:** The exact structure of the `verifiablePresentation` will depend on the final W3C standards and the specific ZKP library used. The above is illustrative.

## Response Body

The service returns a JSON object containing two fields:

- `eligible`: A boolean value (`true` or `false`) indicating whether the presented credential is valid and confers the right to work.
- `audit_id`: A unique, cryptographic hash of the transaction (e.g., a SHA-256 hash of the request and timestamp). This ID is recorded in the public, immutable audit log but contains no personal data.

**Sample Success Response:**

```json
{
  "eligible": true,
  "audit_id": "a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2"
}
```

**Sample Failure Response:**

```json
{
  "eligible": false,
  "audit_id": "b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3"
}
```

## Privacy & Security Notes

- **Stateless & Anonymous:** The endpoint is stateless. It does not log IP addresses, user agent strings, or any other metadata that could identify the verifier or the individual.
- **No Personal Data:** The service **never** receives, processes, or stores any personally identifiable information (PII). The `verifiablePresentation` contains only a cryptographic proof, not the credential itself.
- **Immutable Audit:** The `audit_id` is the only record of the transaction. It proves that a verification event occurred at a specific time but does not link to the individual being checked. This log is essential for public transparency and accountability.
- **Rate Limiting:** The endpoint should be protected by rate limiting to prevent denial-of-service attacks or attempts to probe the system.

