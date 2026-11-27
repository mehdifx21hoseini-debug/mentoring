# MetaFactory 3.62.1 preview

- A newer bound, fully validated report takes precedence over an older inconclusive login check when its broker clock establishes chronology. Pending/new checks, changed-credential invalidation and explicit credential rejection are preserved.
- A fresh, noncached successful report can persist login verification only for the exact current credential revision; superseded background verification tokens cannot overwrite that success.
- Accepted newer live data can clear an earlier structured transient connection/history failure only when it matches the account/credential revision and covers the failed range. The cleared error does not return when live stops. Unknown, IO/credential, newer or missing-range errors remain visible. Status hover shows a redacted reason.
- Cleanup displays small sizes in B / KB / MB / GB rather than rounding them to0MB. The preview explicitly identifies eligible cleanup files, not total disk usage, and explains an empty result. Empty previews disable deletion.
- Storage retention and all launch/close/native reporter behavior from3.62.0 are retained. The39-concurrent-terminal issue still needs same-machine diagnostics. Bot redesign remains paused.

Validation: timestamp/identity/proof/scope and credential-change regressions, real MainForm stale-check/live-stop/new-error flows, persistence and password redaction, cleanup empty/small-size UI, EN/FA at normal/125%, filesystem storage and application regressions. Synthetic Mono/Linux data; native Windows broker execution not newly tested.

Installer: MetaFactory-Setup-3.62.1-preview.exe
Full package includes source and blank student Excel template, without private connection files or real student credentials.
