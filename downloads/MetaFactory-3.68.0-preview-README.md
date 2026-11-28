# MetaFactory 3.68.0 preview

Pasted-message recognition rules and optional comprehensive prompt.

- Recognize A.N / B.N account/broker labels, Arabic final ya in Persian labels/names, WM Markets Ltd aliases and a full WM endpoint supplied in the Broker field without globally remapping complete Server values.
- Keep standalone headings as pending fields, including Server demo: followed by the actual complete server on the next line. Preserve WingoGroupLtd-server and other exact supplied endpoints. Conflicting explicit server/type or broker declarations require correction.
- Treat an explicit new Name after a complete nameless account as a record boundary. Attach a trailing unlabelled owner name to that same account when the next message header or end of input establishes the boundary. Keep previously supported nameless and adjacent named-account boundaries intact.
- Ignore recognized greetings, account-opening introductions, broker clarification prose, and contact URLs/emails after a credential is already available. These do not become extra students or overwrite passwords.
- Strip only a recognized, whitespace-separated trailing credential annotation such as (read only password). Keep attached parentheses and unknown annotation text literally. An explicit Master conflicting with a read-only annotation requires correction; no credential role is silently changed.
- Keep missing MT4/MT5 unresolved when no explicit platform or unambiguous complete-server token supplies it. Do not infer from account-number prefixes, generic Demo/Real, or text inside the password. Normal missing-field validation identifies the issue.
- Add Copy prompt to the text-entry footer. It copies a detailed Persian Excel-conversion instruction set, not student input. Parsing remains local and automatic; this optional button neither connects an AI service nor sends credentials. The footer's minimum width accommodates all three buttons at100%/125%, Persian/English. Standalone prompt is also included under docs.

Eight submitted message layouts were reproduced with synthetic names, identifiers and passwords. Baseline3.67.3 produced9 rows (2ready,7invalid); this version produces8 independent accounts (7ready,1missing the genuinely absent platform). Ready means structurally complete, not authenticated. The original messages and credentials are excluded from the package.

Scope: text parsing, broker-label normalization, name-script normalization, prompt copying, necessary text-entry footer sizing and version/test/docs only. Native verification, normal terminal launch/close, live feed, financial calculations, transactions/replacement, bots, storage and legacy runtime unchanged.

Validation:2908 automated engine/Python/main checks passed (24new mixed-message checks plus the2884-check regression suite);24 targeted prompt UI checks passed at100% and125% in Persian and English. After the footer sizing correction, the targeted UI checks and final installer/PE/resource identity were rerun; parsing and native source bodies were unchanged. One existing chart retry check skipped for its Python environment requirement. Real Windows broker authentication not tested.

Installer: MetaFactory-Setup-3.68.0-preview.exe
Full source, blank template and prompt: MetaFactory-3.68.0-preview-Full-Package.zip
