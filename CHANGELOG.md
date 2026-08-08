# Privacy Advisor Tool — Changelog

## v1.8.3.0 (2026-08-08)

### Major Release - Simplified Groups & Smart DPA Analysis
- **What Changed:**
  - **Customer Groups Simplified:** Removed "EU / EEA" separate option → Now just "EU" (cleaner)
  - **Vendor Regions Simplified:** Removed "UK" → Consolidated to EU, US, IL, Global
  - **Smart DPA Analysis:** Groups table now shows intelligent DPA recommendations based on actual answers
  
- **New Logic:**
  - ✅ **Region Match:** "✅ Region תואם" - No action needed
  - ❌ **Region Mismatch with DPA:** "📋 בדוק: יש DPA - אולי צריך עדכון" - Review existing DPA
  - ❌ **Region Mismatch, DPA Planned:** "📋 בדוק: DPA מתוכנן - הוסף לתקופת ההטמעה" - Add to implementation plan
  - ❌ **Region Mismatch, No DPA:** "❌ חיוני: יש מרווח משפטי - דרוש DPA" - Critical legal gap
  - 🟠 **Partial Match:** "🟠 בדוק Sub-processors + DPA" - Review both elements

- **Impact:** Users now get actionable DPA guidance based on their specific responses

---

## v1.8.2.9 (2026-08-08)

### Update 5/5 - Enhanced Groups Analysis Section
- **Change:** Completely redesigned "קבוצות לקוחות" (Customer Groups) result display
- **Added:**
  - Clear explanation of what was tested (which vendor regions vs. which customer groups)
  - Three possible outcomes with color-coded indicators
  - Summary statistics: Pass count, Fail count, Risk count
  - Vendor region reference in explanation
- **Details:**
  - ✅ **התאמה** = Vendor region matches customer requirement
  - ❌ **אין התאמה** = Legal risk! Customer requirement not met
  - 🟠 **חלקי/אין דרישה** = Partial match or no clear requirement defined
- **Impact:** Users now see exactly what was tested and what the risks are for each customer group

---

## v1.8.2.8 (2026-08-08)

### Update 4/5 - Vendor Region Storage Simplification
- **From:** "איפה הספק שומר את המידע בפועל? 🏪"
- **To:** "אזורי אחסון הספק? 🏪"
- **Explanation:** Moved comprehensive region logic to detailed box below
- **Details:** Now includes:
  - Why we ask per region (different requirements per area)
  - Region examples (Israel, EU, US)
  - Clear distinction between Region ספק (fact) and Region דרישה (law)
  - Compliance warning (red 🔴 if mismatch)

---

## v1.8.2.7 (2026-08-08)

### Update 3/5 - Fixed Progress Bar
- **Issue:** Progress bar showed 119% instead of max 100%
- **Root Cause:** `totalSteps()` didn't count dynamic `grpContract_[group]` steps
- **Fix:** Added `n += S.groups.length` to calculation
- **Impact:** Progress now accurately reflects total steps including all groups

### Update 2/5 - IL Taqana 15 Documentation
- **Change:** Enhanced explanation for IL Privacy Regulation 15
- **Details:** Added comprehensive documentation requirements

### Update 1/5 - GDPR Legal Basis Simplification
- **From:** "איזה סיבה חוקית הספק יכול לעבד את המידע? (Art.6)"
- **To:** "בסיס חוקי (Art.6)?"
- **Impact:** Cleaner UI, better readability

---

## v1.8.2.4 (2026-08-08)

### Five Consolidated Updates
1. Button text simplification
2. DPA question clarity
3. Sub-processors documentation
4. Regulatory steps code consolidation
5. Group contract simplification

---

## v1.8.2.3

- Initial version with 4-column groups table
- Regulations auto-completion by Region
- GDPR Art.6 legal basis multi-select with SaaS context

