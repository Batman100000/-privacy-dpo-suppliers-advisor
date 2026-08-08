# Privacy Advisor Tool — Changelog

## v1.8.3.4 (2026-08-08)

### Deepened Concept Explanations & Sub-Processor Examples
- **Results Summary Expanded:**
  - Legal gap definition with real example (Israel contract vs EU storage)
  - Sub-Processor example: "Vendor in Israel (✅) but uses AWS US backup (❌)"
  - Detailed fixes: DPA, SCCs, Sub-processor approvals
  - Partial risk explanation with Sub-Processor checks

- **Groups Table Enhanced with Deep Explanations:**
  - ✅ Green: Added Sub-Processor verification reminder
  - ❌ Red (with DPA): "Check DPA Sub-Processor coverage"
  - ❌ Red (planned DPA): "DPA must cover Sub-Processors"
  - ❌ Red (no DPA): "Israel contract vs US storage = GDPR issue"
  - 🟠 Orange: "Check Sub-Processor list + DPA coverage"

- **GDPR Legal Basis Deepened:**
  - Comprehensive "why it matters" explanation
  - Real SaaS examples for each basis type:
    - Contract: "Gmail needs email to work"
    - Legitimate Interest: "Analytics, security, updates"
    - Consent: "Marketing only"
    - Legal Obligation: "Tax records, AML"
  - Sub-Processor example: "Google Analytics vs Stripe - both need same legal basis"

- **Impact:** Users understand not just what to do, but WHY and the consequences

---

## v1.8.3.3 (2026-08-08)

### Enhanced Explanations - Results Clarity
- Results summary with detailed risk level explanations
- Groups table with explanation column
- GDPR legal basis education box

---

## v1.8.3.2 (2026-08-08)

### UI Clarity - Renamed Fields
- "מזהה ספק" → "שם הספק"
- Redesigned groups results section

---

## v1.8.3.1 (2026-08-08)

### Smart HIPAA Filtering
- Only show HIPAA question for medical data

---

## v1.8.3.0 (2026-08-08)

### Major Release
- Simplified groups (EU/EEA → EU)
- Smart DPA analysis

---

