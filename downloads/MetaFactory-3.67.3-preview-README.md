# MetaFactory 3.67.3 preview

Pasted student-message field recognition and unnamed-account placeholders.

- Infer a missing platform only from a bounded, unambiguous MT4/MT5 token in a complete supplied server name, such as Alpari-mt5-demo. Preserve the exact server string. An explicit platform conflicting with that server becomes a correction item; it is never silently changed. Generic Demo names and account-number prefixes do not imply a platform.
- Recognize a standalone Alpari / آلپاری / الپاری as the broker before positional name/password assignment. Strong password-shaped unlabelled strings go to the credential field rather than the visible name. Account-first and password-first nameless message forms are supported. Adjacent complete nameless accounts and the next named person's account remain separate.
- Assign No Name1, No Name2 and so on (displayed with spaces: No Name 1) when no name was supplied. OriginalName stays empty rather than exposing a password there. Generated names avoid explicit names already present in that batch.
- A transient generated-name marker prevents these placeholders from replacing an existing account owner's real stored name. A manual explicit name edit remains effective. This marker is not exported or stored as account data.
- Explicit names, investor/master roles and exact password content/case remain unchanged. Ambiguous or contradictory records still require correction before authentication. Spreadsheet recognition and native connection/report/live/bot/storage behavior remain3.67.2 behavior.

The user's five-line message layout (account, password, Persian Alpari, Persian Demo, complete Alpari MT5 server) was reproduced with synthetic credentials and identifiers. Public tests contain no user credentials or original student data.

These tests verify parsing and regressions, not real Windows broker authentication. For the prior unconfirmed accounts, System check taken immediately after a failed attempt plus Save results can help identify routing/runtime/network errors. System check alone does not certify a password or determine every broker refusal.

Installer: MetaFactory-Setup-3.67.3-preview.exe
Full source and blank template: MetaFactory-3.67.3-preview-Full-Package.zip

Validation:2884 automated checks passed, including16 new field-role/placeholder tests,11 endpoint source tests,14 private MT4 checks,46 Python checks, parser/import/replacement/live regressions and2425 main checks. One existing chart retry check skipped for its Python environment requirement. Framework4.5 build, assembly/PE versions, embedded probes and exact installer payload verified.
