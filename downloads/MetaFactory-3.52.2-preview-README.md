# MetaFactory 3.52.2 preview — View numbering and visual corrections

Adds a read-only row number beside the selection checkbox. The number always follows the currently displayed list: All 1..N, each folder 1..its visible count, and a fresh 1..N after filtering, search or sorting. Account login numbers, identifiers, folder membership and saved ordering are unchanged. Clicking a number only selects its row; it does not tick its checkbox or open account details. Existing explicit report and Open/Show commands are preserved.

Compared with the approved proposal and the 3.52.1 Windows capture, fonts and student-name space are increased, the report-summary column is less dominant, table header/alternating rows have clearer contrast, selected filters/folders use graphite, and toolbar commands spread across the available row when they fit. Commands still wrap at smaller widths. Close open remains visible while idle and is disabled when no terminals are open. Actual report/error/freshness text is retained rather than replaced with mockup sample success states.

Native MT4/MT5 reporters, financial calculations, live source and history/freshness validation, launch queue/pacing/Stop, update policy, Sandboxie, delivery backend and Excel export models are unchanged from 3.52.1. Numbering is a view decoration, not a new stored account ID or an export-schema change.

Install: close MetaFactory, run the installer, reopen. Existing accounts/settings are preserved. Existing MetaTrader windows may stay open. Earlier installers remain available for rollback.

Verification uses synthetic data on Linux Mono/Xvfb and .NET Framework 4.5 reference assemblies. Numbering was checked with 107 accounts, 4- and 3-account folders, overlapping membership, sorting, search and return to All in English/Persian at 100%/125%. Native Windows Persian shaping, caption/DPI rendering and live-broker behavior require user-side verification. Concept art and runtime screens are distinct; actual UI captures were inspected before packaging.
