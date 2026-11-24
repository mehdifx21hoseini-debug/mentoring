# MetaFactory 3.51.0 preview

Approved compact visual redesign: graphite header; consolidated Output, Send, Tools and Support menus; one fixed-size Settings frame with General, Running, Delivery and Advanced tabs. Telegram, Bale and Email keep independent enable switches; token fields remain masked with Paste controls.

MT4/MT5 collectors, financial calculations, freshness validation, launch queue/pacing, update policy, Sandboxie integration and reporting backend remain unchanged from 3.50.9. Sending and scheduling backend is unchanged; its editor is embedded in Settings. Tab navigation does not save or send. Unchanged delivery settings are not revalidated during unrelated general saves.

Install: close MetaFactory, run the installer, reopen MetaFactory. Existing terminal windows can remain open. Existing installer retains accounts and settings. 3.50.9 remains available for rollback.

Validation: .NET Framework 4.5 reference build; 2375 logic checks, 194 unified-settings UI checks each at 100% and 125% scale, 144 main-header bounds/overlap checks, 66 delivery UI checks, 15 English + 15 Persian launch-progress/Stop checks passed. Installer payload/report resources verified. UI tests used Linux Mono/Xvfb with synthetic data. Native Windows rendering, DPI and live broker execution remain untested. One pre-existing Python chart check skipped. No new UAC approval claim.

General settings and delivery retain separate stores. Delivery validation runs first. Storage failure after general save is explicitly displayed.
