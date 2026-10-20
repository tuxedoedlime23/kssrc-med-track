# KS Senior Rehab Center - Medtrack PWA starter

This package turns the current Medtrack prototype into an installable Progressive Web App (PWA) shell.

## What's included
- `index.html`: KS Senior Rehab Center - Medtrack interface and current local-browser tracking logic
- `manifest.webmanifest`: app name, appearance, and install icons
- `sw.js`: service worker for caching the app shell
- `icons/`: app icons

## Important limitations
- This version still saves data in the browser on the current device. It does **not** sync between iPhone and computer yet.
- The service worker and installation require the app to be served from HTTPS (or localhost during development); opening `index.html` directly as a file will not enable PWA installation/offline caching.
- This is a prototype, not a clinically validated medication system. Keep following medication labels and clinician/pharmacist instructions. It does not make missed-dose decisions or provide dependable medication reminders.

## How to try it on your computer
1. Upload the contents of this folder to an HTTPS static host (not just the ZIP file).
2. Open the hosted site in Chrome.
3. Use the browser's install option if it appears.

## How to add it on iPhone
1. Host the app over HTTPS.
2. Open the hosted URL in Safari on the iPhone.
3. Tap Share, then **Add to Home Screen**.

## Next step for shared iPhone/computer data
To keep a single medication list and dose history across both devices, the app needs a secure backend with authentication, database access rules, and backups. This package does not yet contain that backend; do not put real sensitive medication data into a public or untrusted deployment.
