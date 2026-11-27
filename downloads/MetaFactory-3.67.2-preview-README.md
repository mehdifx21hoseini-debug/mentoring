# MetaFactory 3.67.2 preview

Private MT4 import endpoint selection and candidate-flow correction.

- Select the private verifier's source using exact local endpoint metadata (.srv or bounded installed binary catalogue), including the native installation's AppData folder. If multiple sources know that endpoint, prefer a currently running native installation, then newer metadata. A running unrelated broker cannot win. This is routing metadata only; cached account credentials and cached login status never authenticate the imported account.
- Do not launch an arbitrary broker's terminal for an MT4 endpoint absent from every discovered local catalogue. Return an immediate server-setup diagnostic and continue to the next candidate, avoiding a full native timeout for each unsupported online server name. This does not assert that an unsupported server is nonexistent or that credentials are wrong. Register the endpoint in the native terminal if necessary.
- Fix3.67.1's candidate-loop regression: exhausting one endpoint's full budget suppresses a repeated check of that same endpoint, but no longer prevents independent verification of later candidates. Other non-retryable failures still stop the loop. A single explicit endpoint still does not receive a duplicate automatic full-minute retry.
- Retain3.67.1's12-second buffered-journal checkpoint and the remaining original60-second native verification window. This checkpoint is not a guaranteed total duration. Provisioning, compilation, closure and multiple supported endpoints can take additional time.
- Add per-candidate elapsed seconds to result details for multi-server checks. Missing catalogue, explicit credential rejection and network-only failure remain distinct. No network-only result becomes wrong-password proof, and failed replacement preserves the previous account.

Normal terminal launch/close, live reporting, financial calculations, MT5 authentication, text/Excel recognition, replacement transactions, bots and storage remain unchanged. Only private import routing, candidate continuation, timing diagnostics and version/test/documentation files changed.

The supplied result workbook showed explicit rejection on a Demo endpoint for one account, and NoConnection on a Real6 endpoint for another, with the candidate loop stopping after2/5 and1/16 respectively. It contained no per-attempt elapsed time, selected source path or fresh native journal, so the exact real-world connectivity cause and duration cannot be established from that workbook. User data and credentials are excluded from this package.

Validation runs on Linux/Mono with synthetic broker and local-catalogue fixtures. Native Windows/broker connection success is not certified; affected account retry remains necessary.

Installer: MetaFactory-Setup-3.67.2-preview.exe
Full source and blank template: MetaFactory-3.67.2-preview-Full-Package.zip

Validation:2868 automated checks passed, including11 new source-selection/candidate-continuation checks,14 prior MT4 early-flush checks,46 Python checks, import/server/replacement/live regressions and2425 main checks. One existing chart retry check skipped for its Python environment requirement. Framework4.5 assembly/PE versions, embedded probes and installer payload verified.
