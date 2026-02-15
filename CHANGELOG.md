# CHANGELOG


---

## v4.6.2 – Current
**Date:** 2026-02-15  
**Changes:**
- **Bugfix:** Added input validation for the URL field. The "Add Monitor" button is now disabled if the input is empty.
- **Logic:** Implemented dynamic interval scheduling (minStepMs: 200ms) to prevent browser congestion with large monitor counts.
- **Logic:** Replaced static `setInterval` with recursive `scheduleCycle` for precise timing control.
- **Safety:** Added `minStepMs` (200ms) to ensure a minimum gap between individual monitor checks, regardless of the total number of monitors.

---

## v4.6.1
**Date:** 2026-02-15  
**Changes:**
- **Patch:** Extended i18n support to all 24 official languages of the European Union.
- **Documentation:** Verified ISO language codes and fallback logic for all added regions.

---

## v4.6.0 – Current
**Date:** 2026-02-15  
**Changes:**
- **Feature:** Full Internationalization (i18n) support for 12 major EU languages.
- **Feature:** Automatic browser language detection with English fallback.
- **Refactoring:** Replaced all hardcoded UI strings with dynamic translation variables.
- **UI:** Translated all system messages (Network Error, Timeout, Offline, etc.).
- **Stability:** Combined i18n with the responsive layout from v4.5.0.
