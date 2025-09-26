_This document is submitted for consideration by the House of Commons Library and its researchers._

---

# **Written Evidence Submission**

**Submitted by Obinna Patrick, under the Sovereign Architect Framework**

**Date:** September 2025

---

## **Abstract**

This evidence submission presents Project SHIELD, a viable, privacy-preserving alternative to the proposed national digital identity scheme (“BritCard”) for the purpose of right-to-work verification. In the context of significant public concern over civil liberties, evidenced by petitions attracting over 500,000 signatures, there is a clear need for policy solutions that address illegal work without creating a centralised surveillance infrastructure. Project SHIELD is a technical and policy framework that enables employers to verify a potential employee’s right to work instantly and securely, using citizen-controlled Verifiable Credentials and optional Zero-Knowledge Proofs. This system is designed to be employer-facing, not a citizen-tracking mechanism. It strengthens enforcement, reduces the administrative burden on businesses, and upholds the privacy of UK residents. This submission provides an overview of the problem, details the proposed alternative, outlines a 90-day pilot plan, describes the robust governance and legal safeguards, and invites parliamentary scrutiny of the open-source proposal. It offers a practical pathway for achieving the government’s stated policy goals while respecting the fundamental rights and freedoms of individuals.

---

### **1. Introduction**

1.1. The UK faces a dual challenge in its right-to-work verification process. The current paper-based system is administratively burdensome for employers and vulnerable to increasingly sophisticated document fraud. This creates compliance risks for legitimate businesses and fails to adequately prevent illegal working.

1.2. The government’s proposed solution, a compulsory national digital identity card (“BritCard”), has generated significant public opposition due to well-founded concerns regarding civil liberties. Such a centralised system risks creating a permanent infrastructure for mass surveillance, is susceptible to large-scale data breaches, and carries a high probability of “function creep,” where it is expanded for purposes beyond its original intent.

1.3. Furthermore, a mandatory digital ID scheme raises critical issues of cost, estimated to be in the billions, and social inclusion. It risks marginalising individuals who lack digital literacy, do not have access to smartphones, or have legitimate reasons for not wanting a state-managed digital identity.

### **2. Proposed Alternative: Project SHIELD**

2.1. Project SHIELD is a decentralized, privacy-by-design framework that directly addresses the challenge of right-to-work verification without requiring a national ID card. In this model, the Home Office issues a single-purpose, cryptographically signed Verifiable Credential (VC) to an individual, which is stored in a secure digital wallet on their personal device. To prove their eligibility, the individual presents a Zero-Knowledge Proof (ZKP) to a prospective employer. The employer’s system verifies this proof via a secure API call, which returns a simple “yes” or “no” response. No personal data is transferred or stored by the employer or the verification service.

2.2. This architecture ensures that the government’s legitimate interest in enforcing work eligibility is met, while fundamentally protecting citizen rights. It prevents the creation of a central database linking citizens to their work activities, makes surveillance impossible by design, and keeps the individual in control of their own data. It is a verification system, not an identification system.

### **3. Pilot Proposal**

3.1. We have developed a comprehensive 90-day pilot blueprint to test the feasibility and effectiveness of Project SHIELD in a real-world environment. The pilot is designed to be conducted in three distinct sectors: NHS administrative hiring, university student enrolment, and local authority housing applications, to ensure the system is robust across different use cases.

3.2. The 12-week plan includes phases for technical setup, component development, integration testing, live operation, and final analysis. The pilot would be subject to continuous oversight by independent security and privacy auditors, with input from civil society organisations.

3.3. Key metrics for success have been defined, including:
    - **Verification Speed:** Target of < 3 seconds per check.
    - **Employer Adoption:** Target of > 90% usage among pilot partners.
    - **Audit Frequency:** Continuous monitoring of the immutable transaction log.
    - **Worker Satisfaction:** Target of > 90% satisfaction from user feedback.

### **4. Governance & Safeguards**

4.1. Project SHIELD is designed to be fully compliant with GDPR and the Data Protection Act 2018, adhering strictly to the principles of data minimisation and purpose limitation.

4.2. Participation in the system is entirely voluntary for individuals. A non-digital, paper-based verification route will be maintained as an equal and accessible alternative, ensuring no one is excluded.

4.3. The pilot and any subsequent implementation would be governed by strict legal safeguards, including:
    - A **Sunset Clause** to ensure the system is decommissioned after the pilot unless a new legal framework is publicly established.
    - A **Use-Lock Provision** that legally and architecturally prevents the system from being used for any purpose other than right-to-work verification.
    - **Statutory Oversight** from an independent body, which would have full access to the immutable audit log to monitor for misuse.

### **5. Conclusion**

5.1. Project SHIELD provides a credible and technologically sound solution to the challenge of modernising right-to-work checks. It demonstrates that it is possible to strengthen enforcement and support businesses without compromising the civil liberties that are fundamental to British society.

5.2. This approach directly addresses the public’s concerns about state surveillance while providing a more efficient, secure, and cost-effective model than a centralised national ID scheme. We encourage Members of Parliament, researchers, and clerks to review the detailed proposal and consider this evidence as a constructive contribution to the ongoing policy debate.

### **6. Appendix**

6.1. **Open-Source Repository:** The complete technical and policy framework for Project SHIELD, including all documents and specifications, is available for public review and contribution on GitHub.
    - [https://github.com/obinnapatrick/project-shield](https://github.com/obinnapatrick/project-shield)

6.2. **Supporting Documents:**
    - [Executive Brief (PDF)](https://github.com/obinnapatrick/project-shield/blob/main/executive_brief.pdf)
    - [Pilot Blueprint (PDF)](https://github.com/obinnapatrick/project-shield/blob/main/pilot_blueprint.pdf)
    - [Written Evidence Submission (PDF)](https://github.com/obinnapatrick/project-shield/blob/main/written_evidence_submission.pdf)

---

**Authored by Obinna Patrick**  
**Under the Sovereign Architect Framework**  
**© 2025 — Released for public implementation**
