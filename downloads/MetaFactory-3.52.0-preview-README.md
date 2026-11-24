# MetaFactory 3.52.0 preview — Silver Workspace

Implements the approved light MacBook-inspired redesign with small graphite navigation accents. Main accounts, settings, report text, folders and support share a single application shell. Standard Windows window controls are retained. Confirmations and account-entry dialogs remain small, consistently light app dialogs; Windows file pickers retain native styling.

Accounts use rich compact rows with initials, student name, account login and broker together, platform badge, report summary, status, checkboxes, icon launch/show and overflow menu. Hidden underlying account/server/folder cells remain populated; search, filtering, sorting, selection and exports keep using the existing models. A responsive inspector shows the selected account and its real report freshness, with original open/show, report and edit actions. At smaller widths the inspector collapses and the account report remains reachable from its name.

Settings use category tabs inside the shared frame. Draft edits survive navigation to accounts; Save and Cancel use the existing persistence and validation. Switching away from report text closes its view and polling, so reopening uses the current account roster. Settings are not saved or messages sent merely by navigating. Report text still uses the original selection confirmation and reporting source. Footer launch/report progress and Stop retain their original behavior.

Native MT4/MT5 collectors, financial calculations, strict freshness/history validation, live source, launch queue and pacing, update policy, Sandboxie and sending/scheduling backend are byte-identical to 3.51.1. No automatic trading permissions or UAC behavior changed. The redesign adds no blur, animation engine or new polling timer.

Install: close MetaFactory, run the installer, reopen MetaFactory. Existing account settings are retained by the original installer. Already-running MetaTrader terminals may remain open. Prior 3.51.1 installer remains available for rollback.

Verification uses synthetic accounts on Linux Mono/Xvfb and Microsoft's .NET Framework 4.5 references. Native Windows Persian shaping, system caption/DPI rendering and live-broker execution require user-side verification. Generated design images are conceptual and are not runtime screenshots. The release UI was also inspected using actual program captures.
