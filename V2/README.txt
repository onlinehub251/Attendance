Time Attendance · Version V2 · Created by Engg: Khalid

Mobile-ready V2 attendance dashboard published at https://onlinehub251.github.io/Attendance/V2/. The existing root page remains in place; V2 shares the same Supabase attendance database and sign-in.

The V2 folder contains the complete deployable site: index.html, manifest.webmanifest, sw.js, icons, and V2_messages.sql (migration reference). The messaging schema has already been applied to the connected Supabase project. Message history is visible only to each message sender and recipient under the configured row-level policies.

Mobile numbers: the app reads and saves numbers in the existing employees.mobile field. Records without a saved mobile number remain blank; add or update numbers in More → Employees or import an employee CSV/XLSX with Staff ID, Name, and Mobile columns. No real employee phone numbers are embedded in this repository folder.

V2 features:
- Colorful Time Attendance · Version V2 branding with a highlighted “Created by Engg: Khalid” credit.
- Team status removed from the first dashboard screen; aligned leave table with absence edit/save controls.
- Dashboard messaging for engineers and other active users.
- Team, person, project, project-code, and date filters in Insights and attendance exports. Team exports include a Team Summary worksheet.
- Colorful charts for hours by day, team, project, project code, and employee.
- Export attribution in Excel workbooks, PDF reports, and JSON/Excel backups.
- Mobile layout with stacked leave cards, wrapped dashboard controls, and safe-area spacing.
- Per-account dashboard card visibility and a personal extra insight card (saved in that browser).
- Employee mobile editing/import; passwords and authentication secrets are excluded from downloads.

Use the existing secure sign-in and password reset flow. The V2 website shares attendance records with the original app.