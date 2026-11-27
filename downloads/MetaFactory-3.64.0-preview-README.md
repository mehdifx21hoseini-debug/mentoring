# MetaFactory 3.64.0 preview

Changes are limited to duplicate replacement and concise details on the text/Excel student-import page.

- Existing accounts are matched by normalized account number only, including Persian/Arabic digits and leading-zero aliases. A duplicate does not establish whether an old account is connected.
- At import start, choose Replace or Skip; Apply to all affects this import attempt. File repeats are skipped once per account, and conflicting input credentials retain the existing validation guard. Multiple old entries for one number require explicit selection of the target copy rather than silently picking one.
- Replacement verifies the incoming login first using the existing private verifier/server-candidate pipeline. Only positive verification allows a durable metadata update of that exact old instance. Failed, timed-out, cancelled, changed/deleted-target, edited-input or failed-save cases preserve the prior account. No extra student is created for a successful replacement. Stale background verification tokens are invalidated after success.
- Folder memberships, notes, saved report/history files, instance identity and copy path are retained. New name/server/login-mode/password details apply on the copy's next launch; running terminals are not switched or closed. Unprovided original-name metadata is retained. A different MT4/MT5 platform is detected as the same account but replacement is refused with an explicit reason, preserving the incompatible old terminal files.
- Visible Details, tooltips and active-stage text are concise Persian phrases. Rejected login is not presented as definite proof of a wrong password; an unconfirmed connection remains unconfirmed. Full redacted diagnostic reasons remain in result exports. Individual/bulk issue copy remains name/account only.
- The Excel template guide describes the replacement policy. Existing spreadsheet headers and input data formats are retained.

Scope: native launch/close/reporting, financial calculations, main-list selection menus, bot integrations, storage retention, fonts and other screens are unchanged. Existing new-account registration and background verification workers are unchanged; only the pre-registration verification method gets an approved replacement branch.

Validation: synthetic account/private-verifier tests for replacement, failed authentication, timeout, cancellation, concurrent credential changes/deletion, failed atomic save/rollback, candidate-server selection, exact ambiguous target, apply-all/skip/file-repeat and stale approval guards. Real UI tests in English/Persian and normal/125%, import-copy and existing application/report/status/storage/selection regressions. Framework4.5 reference build, installer payload and remote artifact integrity checked.

Limits: no new native Windows/broker execution is claimed; verifier integration is exercised with synthetic responses. Existing resource-capacity validation limits remain. This release does not migrate a terminal between MT4 and MT5 or automatically delete other pre-existing duplicate copies.

Installer: MetaFactory-Setup-3.64.0-preview.exe
Full source and blank updated Excel template: MetaFactory-3.64.0-preview-Full-Package.zip
