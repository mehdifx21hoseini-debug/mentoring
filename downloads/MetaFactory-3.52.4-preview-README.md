# MetaFactory 3.52.4 preview — Combined requested refinements

Restores the original name-click behavior: clicking a student's name or pressing Enter opens the existing account information/report page within the same main window. The row's report menu command remains available. No sidebar or separate profile window is added. Number clicks and checkboxes keep their own selection behavior.

Brand logo and MetaFactory wordmark now have separate measured rectangles with an explicit 12 logical pixel gap. Search reserves space based on measured title width instead of assuming a fixed brand width. English and Persian layouts are checked.

Includes the pending 3.52.3 refinements: Excel export moves from the main toolbar to Tools > Export students to Excel, retaining busy-state gating; All/Open/Active/Inactive chip bounds have proper outside/inside padding; alternating rows are white and clearer light grey (#F1F3F6), with clearer separators. Selected/ticked/hover/status colors retain priority. Current-view numbering and report/launch logic remain unchanged.

Verification uses synthetic data on Linux Mono/Xvfb and .NET Framework 4.5 references. Name-click/report/back, logo/text gap, search exclusion, Tools export, chip containment, row stripes, numbering and existing Save/Cancel/Stop paths are checked at 100%/125% in English/Persian. Native Windows Persian font shaping/DPI and live broker execution remain untested. Actual UI captures are inspected and installer payload/download hashes verified before delivery.

Install: close MetaFactory, install this version, reopen. Existing accounts and settings are preserved. Running MetaTrader windows may remain open. Reporting, financial calculations, collectors, update policy, launch backend and Excel/delivery models are unchanged.
