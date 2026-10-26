# Ajaia AI-Native Assessment — Submission

**Candidate Repository:** https://github.com/nn2006/Ajaia-AI-Native-Assessment  

**Deliverables:** Five structured Word documents covering the complete five-module security & compliance assessment for Ajaia.

---

## Approach

I treated the five modules as a single end-to-end security transformation program for Ajaia rather than isolated exercises. Each module builds on the previous:

1. **Architecture & exposure** (Module 1) established the current risk posture and a 90-day hardening roadmap.
2. **Live incident response** (Module 2) tested decision-making under concurrent P1 events involving PHI.
3. **Multi-framework compliance** (Module 3) designed one unified Trust, Security & Privacy Program with HIPAA, FERPA, and SOC 2 overlays.
4. **Vendor & access governance** (Module 4) applied those controls to a prospective medical LLM vendor and redesigned identity from universal admin access to least-privilege RBAC.
5. **AI-native operations** (Module 5) defined how the security team itself uses AI safely while governing shadow AI across the company.

All recommendations are grounded in the concrete environment details provided (Cloud SQL with PHI, public service-account key, AKS default namespace, no Conditional Access, shared VPN PSK, etc.). No generic advice was added.

---

## Deliverables

| Module | Document | Focus |
|--------|----------|-------|
| 1 | [Module1_Security_Architecture_Summary.docx](Module1_Security_Architecture_Summary.docx) | Multi-cloud security design, infrastructure assessment, 90-day remediation plan |
| 2 | [Module2_Incident_Response_Summary.docx](Module2_Incident_Response_Summary.docx) | First-hour incident response, concurrent P1 handling, HIPAA breach determination, CEO communication |
| 3 | [Module3_Compliance_Governance_Summary.docx](Module3_Compliance_Governance_Summary.docx) | Unified compliance program (HIPAA + FERPA + SOC 2), PHI determination for AI APIs, policy gap analysis |
| 4 | [Module4_Vendor_Risk_IAM_Summary.docx](Module4_Vendor_Risk_IAM_Summary.docx) | Vendor security assessment (medical LLM), handling of already-built integration, full RBAC redesign |
| 5 | [Module5_AI_Native_Security_Summary.docx](Module5_AI_Native_Security_Summary.docx) | Three AI-native security workflows, AI risk register, AI tool governance framework |

---

## Key Decisions by Module

### Module 1 — Security Architecture
- Eliminate standing Owner roles and long-lived service-account keys.
- Move Cloud SQL to private IP only; implement hub-and-spoke Shared VPC + HA VPN with unique PSKs.
- Shift images to Artifact Registry + Binary Authorization; harden AKS with private API, namespaces, and Pod Security Standards.
- 90-day execution order: credentials & public exposure first, then network & identity, then supply chain & recovery.

### Module 2 — Incident Response
- Service-account compromise prioritized for containment (confirmed 14 unauthorized SELECTs against PHI tables).
- Stolen laptop treated as concurrent P1 stream.
- Both incidents treated as presumptive HIPAA breaches under the BAA with Harmoni pending formal risk assessment and counsel determination.
- Recommended stance to CEO: proactive transparency; do not default to silence.

### Module 3 — Compliance Governance
- One “Ajaia Trust, Security & Privacy Program” with three framework overlays rather than three separate programs.
- Legal interpretation that “stripped PII means HIPAA does not apply to Anthropic API calls” is incorrect; symptoms + medication names can still constitute PHI.
- Student performance data sent to OpenAI requires FERPA school-official controls and contractual restrictions.
- Draft Incident Response and Data Classification policies contain multiple material gaps (notification timelines, evidence preservation, incorrect classification of education records).

### Module 4 — Vendor Risk & IAM
- Prospective medical LLM vendor is **not approved**. Marketing claims (SOC 2 Type II, encryption, “we will sign a BAA”) are insufficient.
- Already-built integration must be frozen for PHI; synthetic data only until full evidence package and executed BAA are received.
- Current universal admin access replaced by T0–T4 least-privilege model with SSO, MFA, group-based assignment, and automated joiner/mover/leaver lifecycle.

### Module 5 — AI-Native Security
- AI is a productivity layer inside existing controls, never an autonomous decision-maker.
- Three concrete workflows defined (alert triage, secure code review, compliance evidence) with explicit trust boundaries and time-savings estimates.
- Risk register covers eight AI-amplified risks, including the real scenario of pasting client source code into consumer ChatGPT.
- Governance framework centers on an AI Review Board, single tool inventory, data-owner approval for any vendor boundary crossing, and clear consequences without a blame culture.

---

## How AI Was Used

- Structured the five modules into consistent professional documents.
- Mapped concrete environment facts (public Cloud SQL, 14 SELECT queries, 4-digit PIN laptop, etc.) to specific control recommendations.
- Cross-checked HIPAA/HITECH, FERPA school-official exception, SOC 2 Trust Services Criteria, and GCP/Azure best practices against the given scenario.
- Produced decision-ready language suitable for CEO, legal, and engineering audiences.

All final recommendations, risk rankings, timelines, and policy gaps remain my own.

---

## Next Steps (if selected)

I am prepared to:
- Expand any module into full policy language, playbooks, or runbooks.
- Lead the 90-day execution plan outlined in Module 1.
- Stand up the AI Review Board and tool inventory described in Module 5.
- Support the Harmoni BAA notification and formal risk assessment process.

Thank you for the opportunity to demonstrate how I approach security, compliance, and AI-native operations under real constraints.
