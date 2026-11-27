# MetaFactory 3.63.0 preview

- Temporary Send/Support/output menus, rebuilt folder items and their owned icon bitmaps are disposed. Main-window menus/timers/tooltips and borrowed process snapshots are released without closing their terminals.
- Progress animation/tooltip allocation failures degrade the optional display instead of interrupting the launch queue. Optional timers stop retrying after an allocation failure. Normal StartPace and existing startup-memory policy are retained. Only an actual native allocation/resource exception adds a five-second recovery gap before the next queued request. The failed request remains explicitly failed; it is not silently relaunched.
- The dedicated automatic MT5 report profile disables chart drawing with documented CHART_SHOW, keeps one-second live polling and uses the supported 5000-bar chart setting with news off. Manual observer deployments default to normal drawing; chart-review/personal profiles are unchanged. Chart drawing is restored when the EA detaches. Account history and financial calculations are unchanged. MT5 compiles the updated observer using its MetaEditor on first launch.
- Clipboard writes retry brief contention three times and do not claim success if all fail. Password expiry uses the existing watch timer, avoiding a new native timer window. Diagnostic-copy success is shown on the existing button.
- System checks are saved before opening the text dialog. Ctrl+Shift+D saves the same diagnostic text directly without creating another Form or starting a terminal. The bounded emergency-system-check.txt file is overwritten rather than accumulated. Resource failures record actual Win32 codes, stack and MetaFactory USER/GDI/process handles; own-process trends are logged every30seconds. Error reporting avoids repeated custom-dialog construction under resource pressure.
- Existing storage retention, report/status safeguards, folders, calculations and visual layouts are preserved. Bot redesign and pending bulk row-menu behavior are not part of this release.

Validation: Framework4.5 reference-assembly build; synthetic allocation-failure injection, bounded clipboard contention, repeated menu action/disposal, direct diagnostics, profile contracts and previous application/status/storage/report UI regressions. Normal and125% layouts tested under Mono/Linux. Installer embedded payload/resources and downloadable files checked.

Limits: Native Windows resource exhaustion, actual MetaEditor compilation/live broker execution and MT5 resource savings require same-machine validation. No claim that the39-terminal threshold is eliminated or that a particular terminal count is supported. No registry/antivirus changes or forced closing of unrelated terminals.

Installer: MetaFactory-Setup-3.63.0-preview.exe
Source: MetaFactory-3.63.0-preview-Full-Package.zip (includes blank Excel template; excludes private bot connections and student credentials).
