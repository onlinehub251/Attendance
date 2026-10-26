Attendance Mobile — Version 2

This folder is a separate V2 build for you to review and publish. It has not been deployed or uploaded to GitHub.

Publish the contents of this folder to a new V2 directory in the Attendance GitHub repository. Include index.html, manifest.webmanifest, sw.js, apple-touch-icon.png, icon-192.png, icon-512.png, and V2_messages.sql. Keep the existing root page in place.

Backend connection: attendance, employees, projects, leaves, approvals, and reports continue to use the existing Supabase project, auth, and row-level security. No attendance or employee schema changes are made. V2_messages.sql adds only the private app_messages table, participant-only row policies, a read-only contact directory, and a private profile-sync trigger for the Messages option. Before enabling Messages, an admin must run that SQL once in the Supabase SQL Editor. Message history is stored in Supabase and is visible only to the sender and recipient.

Mobile numbers: the app reads and saves numbers in the existing employees.mobile field. Records without a saved mobile number remain blank; add or update numbers in More → Employees or import an employee CSV/XLSX with Staff ID, Name, and Mobile columns. No real employee phone numbers are embedded in this GitHub-bound folder.

V2 changes:
- Removed Team status from the first dashboard screen and added “Time Attendance · Version V2 · Created by Engg Khalid” attribution.
- Added an aligned leave table, an absence entry form, and edit/save controls.
- Added private dashboard-to-dashboard messages for engineers and other active users (requires V2_messages.sql).
- Added team, person, project, project-code, and date filters to Insights and exports. Team exports include a Team Summary worksheet.
- Added colorful charts for hours by day, team, project, project code, and employee.
- Improved phone layout with stacked leave cards, wrapped dashboard controls, and safe-area spacing.
- Added per-account dashboard card visibility and a personal extra insight card (saved in that browser).
- Kept employee mobile editing/import and excluded passwords/authentication secrets from downloads.

Passwords are not included in app backups or the repository. Continue using the app's secure sign-in and password reset flow.

The page has not been tested against live Supabase data, and Codex has not run the SQL or deployed this version. Applying V2_messages.sql is required before the Messages screen can send or receive messages.