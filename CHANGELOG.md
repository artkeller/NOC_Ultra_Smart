# Version History / Changelog

[![Language](https://img.shields.io/badge/language-🇬🇧%20English-informational)](./LANGUAGE.md)

This document describes the **versioning** of the project following Semantic Versioning (SemVer).


CHANGELOG.md      
      ├── [v4.6.2 - Current](#v4.6.2---current)    
      ├── [v4.6.1](#v4-6-1)    
      ├── [v4.6.0](#v4-6-0)   
      ├── [v4.5.0](#v4-5-0)   
      ├── [v4.4.11](#v4-4-11)   
      ├── [vv4.4.2](#v4-4-2)   
      ├── [v4.0.0](#v4-0-0)   
      ├── [v2.0.0](#v2.0.0)   
      ├── [v1.0.0 - Initial](#v1-0-0---initial)   


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

## v4.6.0
**Date:** 2026-02-15  
**Changes:**
- **Feature:** Full Internationalization (i18n) support for 12 major EU languages.
- **Feature:** Automatic browser language detection with English fallback.
- **Refactoring:** Replaced all hardcoded UI strings with dynamic translation variables.
- **UI:** Translated all system messages (Network Error, Timeout, Offline, etc.).
- **Stability:** Combined i18n with the responsive layout from v4.5.0.

---

## v4.5.0
**Date:** 2026-02-15  
**Changes:**
- **Feature:** Full responsive design implementation for mobile and tablet support.
- **UI/UX:** Replaced fixed-width containers with flexible flexbox layouts.
- **UI/UX:** Added viewport meta-tags and media queries for small screens.
- **Optimization:** Dynamic graph scaling via CSS `max-width`.
- **Docs:** Updated README.md and README_DE.md with rate-limiting warnings and new badges.
- **New File:** Created `SECURITY.md` (CRA-Exempt compliant).

---

## v4.4.11
**Date:** 2026-02-10 
**Changes:**
- Improved sorting logic for IP segments and protocols.
- Refined blink animation for red status LED.
- Usage of favivons in favorite list.

---

## v4.0.0
**Date:** 2025-02-02
**Changes:**
- Extension of multi-domain monitoring.
- LoaclStorage of favorite lis.
  
---

## v2.0.0
**Date:** 2026-01-19  
**Changes:**
- Implementieng singele domainn monitoring.
- Handling of CORS/SOP.

---

## v1.0.0 – Initial
**Date:** 2026-01-10  
**Changes:**
- Initial project creation.
- Basic serverless monitoring functionality.

---

## Versioning Notes
- **Major** → incompatible changes, major restructuring  
- **Minor** → new features, documentation updates, improvements  
- **Patch** → small bug fixes, cosmetic changes
