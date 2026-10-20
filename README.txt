KS Senior Rehab Center - MedTrack PWA

Included files
- index.html: medication tracker prototype
- manifest.webmanifest: installable app metadata
- sw.js: service worker and app-shell cache
- icons/: app icons

Current role permissions
- Pharmacy Technician passcode: 1707. Can view medication and dose history, print history, and adjust scheduled times for fixed-time or interval medications. Cannot add/delete medications, change medication name/dose/type/limits, or clear dose history.
- Pharmacist passcode: 8522. Can add/edit/delete medications, clear dose history, import/export backups, and reset local app data.
- When a PRN medication reaches a configured maximum in a rolling 24 hours or its minimum interval has not elapsed, the app requires the Pharmacist passcode before it will record a dose despite that configured limit.

Important limitations
- This app stores data in the browser on the current device. It does not sync between devices and does not provide dependable reminders.
- These passcodes and role checks are implemented in client-side code on a static site. They are a basic workflow deterrent, not secure authentication. Anyone with access to the website source can inspect or bypass them.
- Do not use this prototype as a real resident medication administration record or to protect confidential resident health information. Follow the prescription label and clinician/pharmacist instructions. The app's configured limit warnings are not medical advice.
- To use PWA install/offline features, host the files over HTTPS (GitHub Pages supports HTTPS). Upload the contents of this folder, not the ZIP itself, with index.html at the repository root.
