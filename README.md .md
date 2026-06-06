# AI.GOVERNANCE — Foundations of AI Governance and Cyber Risk Management

**EduQual Level 3 — Topic 37** | **Student:** Muhammad Ali Subhaniee

A structured risk assessment and governance project exploring how AI systems introduce cybersecurity and ethical risks, and how frameworks like the NIST AI Risk Management Framework can be used to identify, assess, and mitigate those risks.

---

## Project Structure

```
ai_governance/
├── AI_Governance.pptx                          ← Full oral presentation (15–20 min)
├── AI_Chatbot_Risk_Assessment_Muhammad_Ali.xlsx ← Live risk assessment (NIST AI RMF)
└── README.md                                   ← This file
```

---

## What This Project Covers

This project is based on a **Customer Support AI Chatbot** as the AI use case. It covers:

- What AI governance means and why it matters for cybersecurity
- 10 identified cyber and ethical risks in the chatbot system
- Risk scoring using **Likelihood × Severity** method
- Mapping each risk to the correct **NIST AI RMF function** (Govern, Map, Measure, Manage)
- System Architecture, Data Flow Diagram, and Security Architecture
- A written AI Acceptable Use Policy (AUP)
- A 7-step Incident Response Procedure for prompt injection attacks
- A failure and recovery scenario

---

## Risk Assessment Summary

| Risk No. | Risk Description | Risk Level | NIST Function |
|----------|-----------------|------------|---------------|
| R01 | Chatbot leaks personal user data (PII) in responses | High | GOVERN |
| R02 | Prompt injection attack manipulates chatbot behaviour | High | MANAGE |
| R03 | Biased training data causes unfair responses | Medium | MAP |
| R04 | Chatbot makes up answers (hallucination) | High | MEASURE |
| R05 | Users don't know they are talking to an AI | Medium | GOVERN |
| R06 | Unauthorized access to chatbot admin panel | High | MANAGE |
| R07 | Chat history stored without user consent | High | GOVERN |
| R08 | Training data poisoned by attacker | Medium | MAP |
| R09 | Staff over-rely on chatbot without human review | Medium | GOVERN |
| R10 | Chatbot goes offline — denial of service | Low | MANAGE |

> Risk Score = Likelihood (1–5) × Severity (1–5)
> Low: 1–5 | Medium: 6–11 | High: 12–19 | Critical: 20–25

---

## NIST AI Risk Management Framework — Applied

```
GOVERN ──► Set policies, rules, and accountability for safe AI use
    │         Used for: R01, R05, R07, R09
    │
MAP ────► Identify where risks exist before deployment
    │         Used for: R03, R08
    │
MEASURE ► Test and measure how big the risk actually is
    │         Used for: R04
    │
MANAGE ──► Take action to reduce or eliminate the risk
              Used for: R02, R06, R10
```

---

## Security Architecture Summary

```
User (Browser / Mobile App)
        │
        │ HTTPS / TLS 1.2+
        ▼
  API Gateway (Input Validation + Rate Limiting)
        │
        ├──► PII Filter (blocks personal data in outputs)
        │
        ▼
  AI Chatbot Model (LLM)
        │
        ├──► Confidence Threshold Check
        │         │ LOW CONFIDENCE?
        │         ▼
        │    Human Escalation Path
        │
        ▼
  Response Delivery to User
        │
        ▼
  Logging & Monitoring (Anomaly Detection)
        │
        ▼
  Admin Dashboard (MFA Protected — Least Privilege)
```

---

## Incident Response — Prompt Injection Attack (7 Steps)

1. **Detect** — Anomaly detection flags unusual input pattern
2. **Contain** — Automatically block the suspicious session
3. **Assess** — Security team reviews the flagged input
4. **Notify** — Inform relevant stakeholders and data protection officer
5. **Investigate** — Trace how the injection was crafted and what it accessed
6. **Remediate** — Patch the input validation rules; retrain if model was affected
7. **Review** — Update the risk register and improve controls to prevent recurrence

---

## Governance Controls Applied

| Control | Purpose |
|--------|---------|
| AI Acceptable Use Policy (AUP) | Defines how the chatbot can and cannot be used |
| PII Output Filter | Prevents personal data appearing in chatbot responses |
| MFA on Admin Access | Stops unauthorized access to the admin dashboard |
| User Consent for Data Storage | Ensures GDPR compliance before saving chat logs |
| Transparency Notice | Tells users they are talking to an AI, not a human |
| Human Review Escalation | Ensures a human checks high-risk chatbot decisions |

---

## Compliance References

- **NIST AI Risk Management Framework (AI RMF)** — Govern, Map, Measure, Manage
- **ISO/IEC 42001** — AI Management System standard
- **GDPR** — User consent, data minimisation, right to erasure
- **CIA Triad** — Confidentiality (TLS/PII filter), Integrity (input validation), Availability (backup systems)
