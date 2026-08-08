# Privacy Advisor Tool — Changelog

## v1.8.2.8 (2026-08-08)

### Update 4/5 - Vendor Region Storage Simplification
- **From:** "איפה הספק שומר את המידע בפועל? 🏪"
- **To:** "אזורי אחסון הספק? 🏪"
- **Explanation:** Moved comprehensive region logic to detailed box below
- **Details:** Now includes:
  - Why we ask per region (different requirements per area)
  - Region examples (Israel, EU, US)
  - Clear distinction between:
    - **Region ספק** = fact (actual storage location)
    - **Region דרישה** = law (contract requirement)
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
- **Details:** Added comprehensive documentation requirements:
  - Processing purpose
  - Data types
  - Storage duration
  - Security processes
  - Access & transfers
- **Target:** Data processors (מחזיק מידע)

### Update 1/5 - GDPR Legal Basis Simplification
- **From:** "איזה סיבה חוקית הספק יכול לעבד את המידע? (Art.6)"
- **To:** "בסיס חוקי (Art.6)?"
- **Explanation:** Moved detailed SaaS context to clarification box
- **Impact:** Cleaner UI, better readability

---

## v1.8.2.4 (2026-08-08)

### Five Consolidated Updates

1. **Button Text:** "✨ בדוק ספק" → "✨ בדיקת ספק נוסף"
2. **DPA Question:** Clearer wording - "האם יש כבר DPA חתום ? או האם מתוכנן להיות חתום ?"
3. **Sub-processors:** "האם יש כבר Sub-processors מתועדים ? או האם מתוכנן להעביר רשימה ?"
4. **Code Consolidation:** Regulatory steps navigation
   - Replaced 4 functions: `nextRegStep()`, `nextAfterGdpr()`, `nextAfterCcpa()`, `nextAfterIl()`
   - New consolidated: `nextRegStep()` + `nextReg(after)`
   - Removed duplication, easier maintenance
5. **grpContract Simplification:** 
   - Question: "[Region] דרישת Region בחוזה?"
   - Detailed explanation moved to bottom

---

## v1.8.2.3

- Initial version with 4-column groups table
- "לא יודע" regulations option with auto-completion by Region
- Shortened privacy banner
- Auto-Match for Region compatibility (removed grpMatch step)
- GDPR Art.6 legal basis multi-select with SaaS context

