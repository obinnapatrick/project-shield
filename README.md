# Project SHIELD

**A privacy-first, employer-facing verification system for right-to-work checks in the UK.**

This repository contains a public proposal for Project SHIELD, an open-source and decentralized alternative to a centralized national digital ID scheme. It is designed to meet the UK’s legitimate need for illegal work enforcement while protecting citizen privacy and civil liberties.

---

## What is Project SHIELD?

Project SHIELD is a technical and policy framework that allows employers to verify an individual’s right to work instantly and securely, without needing to see or store any of their personal data. It is not a digital ID card, a government database, or a citizen tracking system. It is a verification-only mechanism.

## Why does it exist?

The current system of physical document checks is burdensome for employers and susceptible to fraud. Proposed alternatives, such as a national digital ID card (“BritCard”), introduce significant risks of mass surveillance, data breaches, and function creep, which are unacceptable in a free society. 

Project SHIELD provides a “third way” that achieves the government’s policy goal (preventing illegal work) without resorting to disproportionate surveillance infrastructure.

## How it works

The system uses a simple, three-step process built on open, verifiable standards:

1.  **Issuance:** The Home Office, after performing its usual checks, issues a cryptographically signed **Verifiable Credential (VC)** to an individual. This VC is a digital certificate that simply states “Eligible to Work.” It is stored in a secure digital wallet on the individual’s smartphone.

2.  **Presentation:** When applying for a job, the individual presents a **Zero-Knowledge Proof (ZKP)** derived from their VC. This is like showing you have a key without showing the key itself. The employer’s system scans a QR code to receive this proof.

3.  **Verification:** The employer’s system makes an API call to a verification service, submitting only the ZKP. The service checks the cryptographic proof and returns a simple boolean response: `{ "eligible": true }` or `{ "eligible": false }`. No personal data (name, date of birth, nationality) is ever exchanged.

## Key Benefits vs. BritCard

| Feature | Project SHIELD | Centralized Digital ID (BritCard) |
| :--- | :--- | :--- |
| **Data Model** | Decentralized (citizen-controlled) | Centralized (government-controlled) |
| **Data Revealed** | Nothing (Zero-Knowledge Proof) | Name, photo, status, linked data |
| **Surveillance** | Not possible by design | Enables mass surveillance |
| **Function Creep** | Difficult (single-purpose architecture) | High risk (designed for data linking) |
| **Trust Model** | Trust in verifiable cryptography | Trust in government administration |
| **Citizen Control** | Individual holds their own credential | Government holds citizen data |

## Documents

This repository contains the core components of the proposal:

- **[Executive Brief](./executive_brief.md):** A one-page summary for policymakers.
- **[Pilot Blueprint](./pilot_plan.md):** A detailed 90-day implementation plan.
- **[API Specification](./api_spec.md):** Technical details for the verification endpoint.
- **[Privacy Audit Template](./privacy_audit_template.md):** A checklist for ensuring compliance and safety.

## How to Contribute

This is an open proposal. We welcome contributions from all sectors to improve its robustness and feasibility.

- **Developers:** Review the [API specification](./api_spec.md) and propose improvements. Fork this repository to build proof-of-concept applications or alternative components.

- **Auditors & Security Researchers:** Scrutinize the proposed architecture for vulnerabilities. Review the [Privacy Audit Template](./privacy_audit_template.md) and suggest additional safeguards.

- **Civil Society & Policy Experts:** Review the core proposal and its safeguards. Propose policy improvements, identify potential harms, and help strengthen the legal and ethical framework.

To contribute, please open an issue to start a discussion or submit a pull request with your proposed changes.
