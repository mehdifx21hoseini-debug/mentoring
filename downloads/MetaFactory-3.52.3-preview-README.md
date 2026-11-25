# MetaFactory 3.52.3 preview — Table polish

Moves Excel export from the main command toolbar to Tools > Export students to Excel. It calls the original export flow and stays disabled while the application is busy, as the toolbar action did.

Fixes the view-count selector (All/Open/Active/Inactive): its previous first box extended beyond the control edge. New bounds have explicit outside and inside padding, aligned text/count and a focus rectangle fully inside the box. Applies to every view and English/Persian layout.

Alternating rows now use white and clearer light grey (#F1F3F6), with slightly clearer separators. Selected, ticked, hover and report-status colors retain priority. Existing numbering per current folder/search/sort, row actions and account reporting behavior are preserved.

Native collectors, financial models, launch queue/pacing/Stop, update policy, scheduling/delivery and export models remain byte-identical to 3.52.2. No new data schema or backend behavior.

Validation: actual program captures inspected; 52 numbering checks at 100% and 125%, 64 table/menu/chip/row-color checks at each scale, 194 settings checks at each scale, 66 delivery checks, 15+15 launch/Stop checks and 19+19 report-text checks passed. Checks use synthetic data on Linux Mono/Xvfb and Microsoft .NET Framework 4.5 reference assemblies. Native Windows Persian shaping/DPI and broker execution remain untested. Installer payload/resources and actual download hashes are verified before delivery.

Install: close MetaFactory, install this version, reopen. Existing accounts/settings are preserved. Existing MetaTrader terminal windows may stay open. Earlier installers remain available for rollback.
