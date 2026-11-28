# MetaFactory 3.68.1 preview

Foreground student-import queue responsiveness.

- In a multi-account import, give each credential check a cooperative20-second first-sweep scheduling slice. A pending check yields its place to the remaining accounts instead of consuming the entire native multi-server search first. The account remains unsaved and queued; the scheduling deadline is neither a wrong-password result nor a user cancellation.
- Append each yielded account once to the end of the queue for a complete verification with the existing native budgets and safeguards. The later check creates a new request token and repeats all required credential-role checks before committing. Successful and explicitly rejected responses finish normally. This changes when peers are checked, not broker/network response speed; total batch completion can still take time and an extra initial attempt may add work for slow accounts.
- Dispose the expired operation-owned checker before starting peers, without raising concurrent terminal counts. Normal helper ownership checks govern cleanup. A cleanup exception blocks further credential launches with an explicit reason rather than launching over uncertain cleanup.
- Preserve real user cancellation, single-account full-check behavior, unchanged/metadata-only handling, duplicate protection, replacement approval and atomic commits. Failed full replacement retains previous credentials/name. User cancellation does not schedule hidden retries. Existing queued status/counters represent the deferred row; no new persistent account state or UI control is introduced.
- Native cancellation/shutdown and unavoidable OS/storage calls can add time after the scheduling slice. This is not a guaranteed20-second wall-clock handoff on every Windows computer. Native full verification and its MT4/MT5 phase/candidate limits are unchanged.

Scope: foreground import scheduling and a compatible constructor overload for bounded test budgets, plus version metadata/tests/docs. Parser/prompt/Excel, normal terminal launch/close, live reporting, calculations, background import worker loop, native helpers/runtime, bots and storage retain3.68.0 source behavior.

Validation:16 new queue tests cover a slow first account yielding to two peers, full later success with fresh tokens, cleanup ordering, rejected replacement preserving the previous account, immediate rejection without deferral, actual user cancellation, single-account behavior and cleanup failure blocking unsafe launches. Native Windows/broker timing is not tested; fake cooperative verifiers exercise the actual coordinator/registration path.

Installer: MetaFactory-Setup-3.68.1-preview.exe
Full source, blank template and existing prompt: MetaFactory-3.68.1-preview-Full-Package.zip

Validation:2924 automated checks passed:16new queue checks plus the prior2908 engine/Python/main checks, including2425main and46Python. The headless UI server was restarted on a fresh display after a test-environment display-lock failure; remaining UI/live/replacement/main and exact installer/resource verification passed. One existing chart retry check skipped for its Python environment requirement.
