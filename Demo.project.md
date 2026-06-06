# DEMO — Live AI Chatbot Risk Assessment

**EduQual Level 3 — Topic 37** | **Student:** Muhammad Ali Subhaniee

This file explains how to open and run the live risk assessment demo for the oral presentation.

---

## What the Demo Is

A live risk assessment performed on a **Customer Support AI Chatbot** using the **NIST AI Risk Management Framework (AI RMF)**. Each risk is scored using **Likelihood × Severity** and linked to a NIST function with a governance control.

---

## How to Open It

**Option 1 — Google Sheets (Recommended for presentation)**
```
1. Download: AI_Chatbot_Risk_Assessment_Muhammad_Ali.xlsx
2. Go to: sheets.google.com
3. Click: File → Import → Upload the .xlsx file
4. Open Sheet 1: "Risk Assessment"
```

**Option 2 — Microsoft Excel**
```
1. Download: AI_Chatbot_Risk_Assessment_Muhammad_Ali.xlsx
2. Open directly in Excel
3. All formulas and colours load automatically
```

---

## What's Inside

### Sheet 1 — Risk Assessment
```
Column A → Risk No.        (R01 to R10)
Column B → Risk Description (what the risk is, in plain English)
Column C → Risk Type        (Privacy / Cyber Security / Ethics / Reliability)
Column D → Likelihood       (1–5 score — how likely is it to happen?)
Column E → Severity         (1–5 score — how bad would it be?)
Column F → Risk Score       (auto-calculated: Likelihood × Severity)
Column G → Risk Level       (colour-coded: High / Medium / Low)
Column H → NIST AI RMF Function (GOVERN / MAP / MEASURE / MANAGE)
Column I → What Should Be Done  (the governance control)
Column J → Status           (Completed / In Progress / Not Started)
```

### Sheet 2 — NIST AI RMF Notes
```
Simple explanation of all 4 NIST functions
and how each one was applied in this assessment
```

---

## Risk Level Colour Guide

| Colour | Level | Score | Meaning |
|--------|-------|-------|---------|
| 🔴 Dark Red | High | 12–19 | Needs urgent action |
| 🟡 Yellow | Medium | 6–11 | Needs scheduled action |
| 🟢 Green | Low | 1–5 | Monitor and review |

---

## Demo Walkthrough — What to Say

| Step | What to Click | What to Say |
|------|--------------|-------------|
| 1 | Point to R01 | "This is a privacy risk — the chatbot could leak personal user data. Likelihood is 3, Severity is 4, so the score is 12 — that makes it High risk. The control is a PII filter on all outputs." |
| 2 | Point to R02 | "R02 is prompt injection — a hacker tricks the chatbot into saying harmful things. Score is 16, High risk. We control it with input validation and anomaly alerts." |
| 3 | Point to R03 | "R03 is bias — if the training data is biased, the chatbot gives unfair answers. Score is 9, Medium. We fix this by auditing the training data before use." |
| 4 | Point to R05 | "R05 is an ethics risk — users don't know they are talking to AI. It is Medium risk but very important for transparency and trust." |
| 5 | Point to R06 | "R06 is unauthorized admin access — score 15, High. We require MFA and least privilege access to prevent this." |
| 6 | Switch to Sheet 2 | "I linked every risk to the NIST AI RMF. GOVERN is for policy risks, MAP is for identifying risks early, MEASURE is for testing accuracy, and MANAGE is for active security controls." |

---

## Scoring Method

```
Risk Score = Likelihood × Severity

Likelihood Scale:
  1 = Rare         (very unlikely)
  2 = Unlikely     (could happen)
  3 = Possible     (seen in similar systems)
  4 = Likely       (will probably happen)
  5 = Almost Certain (expected to happen)

Severity Scale:
  1 = Negligible   (no real harm)
  2 = Minor        (small impact)
  3 = Moderate     (noticeable disruption)
  4 = Major        (serious harm or data loss)
  5 = Catastrophic (breach, legal action, system failure)
```

---

## NIST AI RMF — Quick Reference

```
GOVERN ──► Create rules and policies for safe AI use
MAP ────► Identify where risks exist before deployment  
MEASURE ► Test and measure how big the risk actually is
MANAGE ──► Take action to reduce or eliminate the risk
```
