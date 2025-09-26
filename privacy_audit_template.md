# Privacy & Compliance Audit Template

_This template is a checklist for independent auditors and civil society organisations to assess the compliance and privacy-preservation of any Project SHIELD pilot. It should be used as a baseline for continuous oversight._

---

### Audit Area: Data Minimisation

- [ ] **Verification Endpoint:** Confirm that the `/verify-right-to-work` endpoint only accepts a cryptographic proof and does not receive any personally identifiable information (PII).
- [ ] **Response Data:** Confirm that the API response is limited to a boolean `eligible` status and a non-personally-identifiable `audit_id`.
- [ ] **Issuer Data:** Confirm that the government issuer only stores the minimum data required to issue and (if necessary) revoke a credential, and that this data is not accessible to the verification service.
- [ ] **Holder Wallet:** Confirm that the reference wallet application does not collect or transmit any telemetry or user data.

### Audit Area: No Secondary Use (Purpose Limitation)

- [ ] **API Logs:** Verify that the verification service does not store logs containing IP addresses, user agents, or other request metadata.
- [ ] **Legal Agreements:** Review all pilot partner agreements to ensure they contain a strict “Use Lock” clause, legally prohibiting the use of the system for any purpose other than right-to-work verification.
- [ ] **Technical Architecture:** Confirm that the system architecture does not allow for data matching, linking, or sharing with other government or private sector databases.

### Audit Area: Transparency & Accountability

- [ ] **Immutable Audit Log:** Verify that all verification events are recorded to a publicly accessible, immutable audit log, using only the `audit_id`.
- [ ] **Source Code:** Confirm that the source code for all core components (verifier, reference wallet) is publicly available for inspection.
- [ ] **Public Reporting:** Ensure that the pilot operators are publishing regular transparency reports detailing the volume of verifications and any security incidents.

### Audit Area: Inclusion & Accessibility

- [ ] **Non-Digital Alternative:** Confirm that a clear, accessible, and equally efficient non-digital verification path is available and actively signposted for individuals without smartphone access or who opt out.
- [ ] **Usability Testing:** Review the results of usability testing with a diverse range of users, including those with low digital literacy or disabilities.
- [ ] **No Coercion:** Verify that employers are not coercing or pressuring individuals to use the digital system over the non-digital alternative.

### Audit Area: Legal Safeguards

- [ ] **Sunset Clause:** Confirm that all pilot agreements contain a sunset clause that mandates the secure decommissioning of the system and deletion of all operational data within 30 days of the pilot’s conclusion.
- [ ] **Data Protection Impact Assessment (DPIA):** Review the pilot’s DPIA to ensure it adequately addresses and mitigates all identified privacy risks.
- [ ] **Legal Basis:** Confirm that the data processing activities have a clear and lawful basis under GDPR and the Data Protection Act 2018.
