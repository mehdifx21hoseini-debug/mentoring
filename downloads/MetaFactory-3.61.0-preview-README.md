# MetaFactory 3.61.0 preview

- Student report: whole-account profit factor remains the main value; selected-window closed-position profit factor appears beneath it.
- Whole-account maximum relative trading-balance drawdown remains the main value; the selected-window value appears beneath it, using the actual balance at the window start, resetting the peak there and excluding external cash movements inside the window. All retains the established full-account funding-neutral curve. These are balance drawdowns, not floating-equity estimates.
- Added All before Range. An explicit All click reads missing full trade detail; incomplete detail is not displayed as a complete account report. Existing full-history request boundary (2000-01-01) is retained.
- All can retain verified historical detail alongside a newer live window, subject to account identity and continuity checks.
- Undefined PF (no realized wins/losses), missing/unverified history, and unknown DD remain a dash. Winning-only PF is infinity; losing-only PF is zero. MT5 PF excludes still-open partial positions and includes costs of fully closed positions.

- Main page: folder membership column restored, full membership available on hover. Explicit Add to folder command in selection toolbar and row menu; bulk additions retain other memberships.

Installer: MetaFactory-Setup-3.61.0-preview.exe
Full package contains installer, source and blank student Excel template. User credentials and bot tokens are not included.

Validation: Microsoft .NET Framework 4.5 reference-assembly build, application regressions, focused period-metric and live-history checks, English/Persian layouts at normal/125% scale, installer payload/version checks. Native Windows broker execution and MetaTrader statement parity were not newly tested in this Linux environment.
