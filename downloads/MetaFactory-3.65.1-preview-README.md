# MetaFactory 3.65.1 preview

Main-list Today column presentation only, following the approved two-line mockup.

- First line starts with the money amount, then Open or Close, then trade count. Example: `-$5.13 · Open · 2 trades · No SL: 1`; flat example: `+$20.40 · Close · 3 trades`. There is no Net, Day, O or C prefix. Open retains the existing floating-only amount/current open count; Close retains the verified closed trading result/count for the displayed broker day. Missing/unknown stop evidence and No SL counting remain unchanged.
- Fresh live data says `Live · Just now` instead of a changing seconds counter. Actual UTC heartbeat and age remain in the tooltip. Existing freshness, account identity and history checks remain unchanged; stale reports are not relabeled fresh. Restart reporter / History pending notices are preserved.
- Two lines, original row height, fonts, neutral labels, colored signed amounts and No SL warning remain. Separator spacing adapts only for the new money/status/count format so the amount fits at125% scaling without changing other columns. Historical Report ages remain unchanged.

No changes to financial arithmetic, native observers, polling cadence, feed acceptance, terminal launch/close, import/replacement, bots, scheduling or storage behavior. This is not a fix for resource pressure or stale/identity-mismatched terminal feeds.

Validation: existing two-line live/open/closed/unknown-stop/main-grid checks updated to the approved labels; fresh, near-expiry and stale footer checks; both platforms/languages and normal/125% UI scaling. Protected source files compared with3.65.0, Framework4.5 build and installer/resource identity verified. Tests run on Mono/Linux with synthetic data; actual Windows/native broker execution remains untested here.

Installer: MetaFactory-Setup-3.65.1-preview.exe
Full source and blank template: MetaFactory-3.65.1-preview-Full-Package.zip
