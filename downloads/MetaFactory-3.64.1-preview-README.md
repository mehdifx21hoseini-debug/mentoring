# MetaFactory 3.64.1 preview

Only the student-directory Excel export path changes relative to3.64.0.

- Choose All students, Selected students or Specific folder in the existing Tools > Export students to Excel dialog. Folder selection includes No folder. Checked students are the default when present; otherwise the currently viewed folder is the default, or All when viewing the full directory. Explicit All is independent of platform/search/folder filters. Folder scope includes the complete folder; checked scope includes exact checked instance IDs, including checked students outside the current view.
- Preview shows the count. Empty/unknown selections, empty/deleted folders and invalid scope states never fall back to exporting everyone. The save action is disabled for empty scope. Scope names are captured before the file chooser and passed into the existing row exporter. Matching occurs by instance identity, so one selected duplicate account does not pull in its unselected peer.
- Each run writes a separate Excel workbook with a scope-specific suggested filename and folder name where applicable. Choose the save location as before. The completion count reflects rows actually written.
- Spreadsheet columns, record values, text account IDs with leading zeros, folder-membership fields, missing-copy handling, import compatibility and the existing include-passwords default/option are retained. Account-only entries remain available in All and relevant folder scopes. Workbook guide describes the chosen scope and current duplicate-replacement policy. Password arrays are cleared after writing as before.
- Main UI outside the export helper/method is unchanged. Import replacement/short details, row-selection actions, native launch/close/reporting, financial calculations, bot integrations, fonts and storage retention are byte-identical to3.64.0; Core/Program/setup/resource changes are version markers only.

Validation: real XLSX round trips, subset isolation including excluded identities/secrets, same-login peers, overlap/unfiled/empty/deleted folders, account-only records, unchanged all-export rows and schema, password opt-out, leading zeros, import compatibility and no account/folder mutations. Real export-options UI in English/Persian at normal/125%, save-count/default-scope/empty guards and MainForm checked/current-folder integration. Existing application regressions and installer embedded payload verified. Synthetic Mono/Linux; native Windows file-picker interaction not newly exercised.

Installer: MetaFactory-Setup-3.64.1-preview.exe
Full source and blank Excel template: MetaFactory-3.64.1-preview-Full-Package.zip
