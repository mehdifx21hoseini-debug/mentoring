# MetaFactory 3.67.1 preview

Import-only MT4 verification responsiveness update.

- Restore the legacy early journal-flush principle in the reserved private MT4 verifier. At12seconds, buffered login acknowledgement is read after closing only the operation-owned verifier process. A fresh successful login or explicit rejection can finish then rather than waiting for the full60-second window. Earlier visible acknowledgements still finish immediately.
- If the early result remains pending or network-only, continue once with the remainder of the same monotonic60-second budget. A fresh journal baseline and exact token/account/server marker guards exclude cached proof. The restart receives its own start-INI reading window. A matching final marker produced during close is read before journal fallback.
- After the complete private MT4 window is exhausted, suppress the coordinator's automatic repeat of that same full window. Unconfirmed remains unconfirmed, never a wrong-password verdict. Manual Retry and ambiguous-server alternatives remain available.
- Ambiguous candidate servers still require independent proof. A rejection on one ambiguous endpoint does not assert that the credentials are invalid on every possible endpoint. No fabricated connection result or blanket server-family match is accepted.

Only src/ConnectionProbes.cs import-private MT4 behavior changed, plus version metadata and focused tests/documentation. Normal launch/close, live feed, report calculations, text/Excel parsing, replacement rules, MT5 verification, bots and storage remain3.67.0 behavior.

A12-second journal checkpoint is not a guaranteed total check duration: provisioning, compilation, process shutdown and additional ambiguous endpoints also take time. Real Windows/broker testing remains necessary. Manual WMMarkets-REAL6 success for the affected MT4 account is known, but its failure inside the private verifier is not reproduced here. This update addresses buffered confirmation and duplicated waiting; it does not certify that real account's connection.

Installer: MetaFactory-Setup-3.67.1-preview.exe
Full source and blank template: MetaFactory-3.67.1-preview-Full-Package.zip

Validation:2857 automated checks passed (14 new private MT4 speed/flush checks,46 Python checks, existing import/server/replacement/live regressions and2425 main checks). One existing chart retry check skipped for its Python environment requirement. Framework4.5 build, assembly/PE versions, embedded probes and installer payload verified. Native Windows broker authentication not tested.
