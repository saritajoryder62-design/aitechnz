# Evidence Testing Log - aitechnz

This file documents manual and automated test evidence for the aitechnz project.

---

## Automated Tests (GitHub Actions)

Automated tests run on every push to `main` via `.github/workflows/test.yml`.

| Test Job | What It Checks | Status |
|---|---|---|
| check-pages | All required HTML files exist (index.html, booking.html, thank-you.html) | ✅ Active |
| security-check | No .env files committed, no hardcoded secrets | ✅ Active |
| link-check | CSS files referenced in HTML actually exist | ✅ Active |

View live results: [Actions tab](https://github.com/saritajoryder62-design/aitechnz/actions)

---

## Manual Test Evidence

### Test 1: Homepage Loads Correctly
- **Date:** 2026-05-31
- **Tester:** saritajoryder62-design
- **URL Tested:** https://aitechnz.vercel.app
- **Result:** PASS
- **Notes:** Page loads, navigation works, images display correctly

### Test 2: Booking Form Submission
- **Date:** 2026-05-31
- **Tester:** saritajoryder62-design
- **URL Tested:** https://aitechnz.vercel.app/booking.html
- **Steps:**
  1. Fill in name field
  2. Fill in email field
  3. Select service type
  4. Click Submit
- **Expected:** Redirect to thank-you.html
- **Result:** PASS / FAIL (update after testing)
- **Notes:**

### Test 3: Thank You Page Loads After Booking
- **Date:** 2026-05-31
- **Tester:** saritajoryder62-design
- **URL Tested:** https://aitechnz.vercel.app/thank-you.html
- **Result:** PASS / FAIL (update after testing)

### Test 4: Mobile Responsiveness
- **Date:** 2026-05-31
- **Tester:** saritajoryder62-design
- **Devices Tested:** iPhone 12, Samsung Galaxy
- **Result:** PASS / FAIL (update after testing)
- **Notes:**

---

## Security Evidence

| Check | Status | Date | Notes |
|---|---|---|---|
| .env files NOT in repo | ✅ PASS | 2026-05-31 | Verified via GitHub search - 0 results |
| .env in .gitignore | ✅ PASS | 2026-05-31 | Added to .gitignore |
| Dependabot alerts enabled | ✅ PASS | 2026-05-31 | Enabled in Security settings |
| Secret scanning enabled | ✅ PASS | 2026-05-31 | Secret Protection enabled |
| No hardcoded API keys | ✅ PASS | 2026-05-31 | No secrets found in code |

---

## How to Add New Test Evidence

1. Copy one of the test templates above
2. Fill in the date, result, and notes
3. Commit to this file
4. Link any screenshots or recordings in the Notes column
