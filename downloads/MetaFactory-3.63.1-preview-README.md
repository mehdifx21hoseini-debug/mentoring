# MetaFactory 3.63.1 preview

Only the two requested UI behaviors change relative to3.63.0:

- Individual and bulk issue-copy actions in text/Excel import copy only the displayed student name and account number, one student per line. No reason, platform, server, password, original-name alias or correction request is included. Missing account numbers remain missing. Visible diagnostic details, import parsing, verification, registration and Excel exports are unchanged.
- Opening the main-list row menu on a checked student captures the full checked group. Copy, folder membership, role-specific Close and confirmed Delete use that exact group; menu labels show its count. Edit visits each student's existing individual editor separately; Cancel stops the remaining editors. Clicking an unchecked row keeps that row as the only target. Student report-page Manage remains individual. The existing launch/close implementations, deletion confirmations and running-copy guards are retained.

Scope verification: only src/Ui.cs, src/StudentActions.cs and src/TextStudentImport.cs change behavior; Core/Program/setup/resource changes are version markers only.72 other source/resource files are byte-identical to3.63.0, including native reporters, live/report calculations, launch/close pipelines, startup pacing, clipboard resource handling, bot integrations and storage retention.

Validation: synthetic real-UI group copy, folder update, per-student editing and cancellation, exact deletion confirmation and deletion persistence, import clipboard/diagnostic/export behavior; English/Persian and normal/125% layouts; prior application/status/storage/report/resource regressions; installer embedded payload/resources and downloadable artifact hashes.

No new native broker/Windows execution is claimed. Existing3.63.0 native resource-capacity validation limits remain.

Installer: MetaFactory-Setup-3.63.1-preview.exe
Full source and blank Excel template: MetaFactory-3.63.1-preview-Full-Package.zip
