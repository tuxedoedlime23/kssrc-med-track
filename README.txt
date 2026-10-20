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

New in this version
- Rounded PRN display times no longer show the “exact time retained” note in the regular history. The Pharmacist panel now has an Exact PRN recording times section showing each rounded PRN entry’s original recorded timestamp and its rounded display time.

New in this version
- Pharmacist can create/remove employees with unique 4–8 digit employee PINs. Every scheduled or PRN dose record requires a valid employee PIN and stores the employee name in the history.
- Pharmacy Technician and Pharmacist can choose a previous date on the Today page and record missed historical scheduled doses. The app asks for the actual time taken for a previous date rather than pretending it was logged today. Future dates are blocked.
- A persistent Lock admin button appears while an admin session is unlocked, including when navigating to Medications or Dose history.
- Rounded PRN entries store the rounding mode used at the time of recording, so the Pharmacist's Exact PRN Recording Times panel can continue to show exact and displayed times even if the medication's rounding setting later changes.
- Employee PINs and all dose/medication data are stored in local browser storage only. They are not secure authentication and do not sync to other devices.


Latest update: Employee sign-in/sign-off now persists for a session, and each employee has a Pharmacist or Pharmacy Technician position. Pharmacists receive full admin access; Pharmacy Technicians receive basic admin access. Previous-day dose review and entry are now located on the Dose history page in the right-side panel.
