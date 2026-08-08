# Privacy Advisor Tool — Changelog

## v1.8.3.1 (2026-08-08)

### Smart Regulation Filtering - HIPAA Only Shows for Medical Data
- **Issue:** HIPAA BAA question appeared even when no medical/PHI data was selected
- **Fix:** Added conditional logic to only show HIPAA question if:
  - HIPAA is in selected regulations AND
  - User selected "רפואי" (medical) in dataTypes
- **Changes:**
  - Added `hasPhysicalData()` function to check if medical data was selected
  - Updated `totalSteps()` to only count HIPAA step when medical data present
  - Updated `nextRegStep()` to skip HIPAA question if no medical data
  - Updated `nextReg()` navigation to respect medical data check
- **Impact:** Cleaner flow for non-medical data handling - users won't see HIPAA questions if they don't have PHI

---

## v1.8.3.0 (2026-08-08)

### Major Release - Simplified Groups & Smart DPA Analysis
- **Customer Groups Simplified:** Removed "EU / EEA" separate option → Now just "EU"
- **Vendor Regions Simplified:** Removed "UK" → Consolidated to EU, US, IL, Global
- **Smart DPA Analysis:** Groups table shows intelligent DPA recommendations based on answers
- **New Logic:**
  - ✅ **Region Match:** "✅ Region תואם" - No action needed
  - ❌ **Region Mismatch with DPA:** "📋 בדוק: יש DPA - אולי צריך עדכון"
  - ❌ **Region Mismatch, DPA Planned:** "📋 בדוק: DPA מתוכנן - הוסף לתקופת ההטמעה"
  - ❌ **Region Mismatch, No DPA:** "❌ חיוני: יש מרווח משפטי - דרוש DPA"
  - 🟠 **Partial Match:** "🟠 בדוק Sub-processors + DPA"

---

## v1.8.2.9 (2026-08-08)

### Update 5/5 - Enhanced Groups Analysis Section
- Clear explanation of what was tested
- Three possible outcomes with color-coded indicators
- Summary statistics: Pass count, Fail count, Risk count
- Vendor region reference in explanation

---

## v1.8.2.8 (2026-08-08)

### Update 4/5 - Vendor Region Storage Simplification
- From: "איפה הספק שומר את המידע בפועל? 🏪"
- To: "אזורי אחסון הספק? 🏪"
- Moved comprehensive region logic to detailed box below

---

## v1.8.2.7 (2026-08-08)

### Updates 3, 2, 1/5
- Fixed progress bar (was showing 119%)
- Enhanced IL Taqana 15 documentation
- Simplified GDPR legal basis question

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

