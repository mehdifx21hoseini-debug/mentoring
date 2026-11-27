# MetaFactory 3.67.0 preview

Student import: resolve WMMarkets/Windsor ambiguity without assuming they are interchangeable endpoints.

- Keep complete supplied server names. Ambiguous broker labels can use known servers from both families, preserving Demo/Real type and platform. WindsorBrokers1-Demo is included from the confirmed native endpoint; numbered Real servers are discovered from installed catalogues rather than invented.
- A fresh MT5 login acknowledgement that reports a different related server is discovery only. Recheck the actual server with the same account and credentials before accepting it. Wrong account, disconnected terminal, stale token, unrelated broker or different account type cannot redirect or pass verification.
- Remember a verified endpoint per account only after a successful committed import. Failed replacement preserves the previous account and encrypted credentials.
- Read bounded installed server metadata, including ASCII/Unicode servers.dat. Private MT4 verification now allows its probe the existing sixty-second window instead of ending earlier. Successful and rejected responses still finish immediately.
- Normal terminal launch/close, live reporting, calculations, main UI, bots, storage and legacy runtime remain unchanged.

Validation: 46 Python tests, 25 server-resolution tests, 34 MT5 phase tests, 16 private workspace tests, 57 recognition tests, 37 text import tests, 29 import flow tests, 26 import UI tests, 49 replacement tests, 99 live-row tests and 2425 main checks passed. One existing chart check requires a different Python environment and was skipped. Framework4.5 build, PE versions, installer payload and embedded probes verified.

Tests use Linux/Mono and synthetic broker responses. Real Windows authentication remains to be tested. Account1218172 is manually connected to WMMarkets-REAL6, matching the original input; this establishes the exact endpoint but does not establish the cause of the private verifier failure. The longer private verification window addresses a confirmed timing mismatch, not proof that this particular account now connects.

Installer: MetaFactory-Setup-3.67.0-preview.exe
Full source and blank template: MetaFactory-3.67.0-preview-Full-Package.zip
