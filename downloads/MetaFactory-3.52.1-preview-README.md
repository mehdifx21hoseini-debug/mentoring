# MetaFactory 3.52.1 preview — Refined classic table

Implements the latest approved design: full-width compact table, light search/brand/utility header and narrow graphite command toolbar. The 3.52.0 workspace sidebar, rich avatar rows and account inspector are removed. Student, copy, account and server are independent visible columns again. Rows are compact; each has a single Open or Show action according to the actual terminal state, plus overflow. Row actions use neutral graphite focus and blue is reserved for primary actions.

Clicking a student name selects the row and does not open a profile, inspector or separate window. Use the row's overflow menu > View account report (or the keyboard context menu) for the existing account report inside the original window. Report text and Excel export have direct toolbar commands. Existing checkbox-based group actions, selection, search, filtering, sorting and report/back navigation are retained.

At wider widths, report freshness has its own column using the existing TodayAgo value. At smaller widths it remains under the report summary, preserving information while keeping columns usable. Folder memberships remain stored and available through folder filters and menus. Settings return to a compact light preferences dialog; delivery, channel logos, masked tokens, paste, validation and persistence remain intact.

Native MT4/MT5 collectors, live source, financial calculations and strict history/freshness proofs, launch queue and pacing, update policy, Sandboxie and sending/scheduling backend are byte-identical to 3.52.0. Progress Stop behavior is unchanged. Progress-bar paint uses graphite; no new engine timer or blur dependency.

Install: close MetaFactory, run the installer, reopen. Existing accounts and settings are preserved by the original installer. Existing MetaTrader windows may remain open. Older installers remain available for rollback.

Validation: 2375 logic checks passed, 0 failed; one pre-existing Python chart check skipped. Refined table checks 48 at 100% and 48 at 125%, settings 194 at each scale, delivery 66, launch/Stop 15 English + 15 Persian, report text 19 English + 19 Persian passed. Tests used synthetic data on Linux Mono/Xvfb with Microsoft .NET Framework 4.5 references. Native Windows Persian font shaping, caption/DPI rendering and live broker execution require user-side verification. Installer payload/resources and real download integrity are checked before delivery.
