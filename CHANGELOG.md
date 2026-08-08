# Privacy Advisor Tool — Changelog

## v1.8.3.2 (2026-08-08)

### UI Clarity Improvements - Results Page Redesign
- **Issue:** Results page was cluttered with verbose explanations, making key findings unclear
- **Changes:**
  1. **First Page:** "מזהה ספק" → "שם הספק" (clearer label)
  2. **Tree Navigation:** Updated to "שם הספק" for consistency
  3. **Groups Section Redesign:**
     - Removed verbose "🔍 מה בדקנו?" explanation
     - Added concise "🔄 ההשוואה:" with real example
     - Simplified result summary: clear pass/fail/risk status
     - Changed table headers from "דרישה חוזית / מתקיים? / דרישות פרטיות" to "דורש / מצב / פעולה נדרשת" (more actionable)
     - Shortened action text from "📋 בדוק: יש DPA - אולי צריך עדכון" to "📋 יש DPA - בדוק" (cleaner)
     - Better visual hierarchy with status-first summary

- **Impact:** 
  - Clearer first impression
  - Easier to understand group analysis at a glance
  - More action-oriented language
  - Better mobile/desktop presentation

---

## v1.8.3.1 (2026-08-08)

### Smart HIPAA Filtering - Only Shows for Medical Data
- Added conditional logic to only show HIPAA question if medical/PHI data selected
- Added `hasPhysicalData()` function
- Updated `totalSteps()`, `nextRegStep()`, `nextReg()` logic
- Cleaner flow for non-medical workflows

---

## v1.8.3.0 (2026-08-08)

### Major Release - Simplified Groups & Smart DPA Analysis
- Customer Groups Simplified: EU/EEA → EU
- Vendor Regions: Removed UK
- Smart DPA Analysis with conditional recommendations

---

## v1.8.2.9 (2026-08-08)

### Update 5/5 - Enhanced Groups Analysis Section
- Clear testing explanation and outcomes
- Summary statistics with pass/fail/risk counts

---

## v1.8.2.8 (2026-08-08)

### Update 4/5 - Vendor Region Simplification
- Simplified question to "אזורי אחסון הספק? 🏪"
- Moved logic to detailed explanation box

---

## v1.8.2.7 (2026-08-08)

### Updates 3, 2, 1/5
- Fixed progress bar (119% → 100%)
- Enhanced IL Taqana 15 documentation
- Simplified GDPR legal basis question

---

