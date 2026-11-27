# MetaFactory 3.64.2 preview

Changes are limited to the approved main-list Today/Open readability, row menu glyph and current open-stop indication.

- Today gets more minimum/fill width, with a small reduction in Status and Action allocation. Account-information minimums and its complete Balance/Maximum DD label renderer remain unchanged. The row-only menu glyph is vertical; its hit box is20x26logical pixels, separate from the Open/Show button. Existing row actions and selection scope are unchanged.
- First-line text uses measured device-context bounds and reserves the full Open count. It uses the existing9pt font when needed; unusually long other segments may ellipsize rather than consuming Open's reserved space. No amount/count calculation changes. The full text remains in the tooltip.
- A pale-red No SL badge is shown on the second line beside the existing freshness text only for known current-zero stops on open positions in the bound report or fresh identity-matched pending live frame. Multiple known unprotected positions include their count. Existing Live green and report-age/previous-report styling are retained.
- Current SL is distinct from entry SL and from closed-trade stop history. Entry-stop absence alone creates no badge. Unknown/malformed/nonfinite/negative current stops, stale live feeds and wrong-account/server data cannot be inferred as absent stops. Removing/adding a current stop updates the row rendering key and badge.
- The previous main-row path explicitly forced TodayNoSl=false and did not render it. It now maps actual open-position stop evidence. Nullable presentation provenance is retained when reading current-stop values; normal numeric report records remain unchanged. Invalid-stop cache records may append an optional MF_SL_UNKNOWN metadata token, which older readers ignore. Every legacy numeric value and the financial math are retained.
- No native reporter, startup/close pipeline, profile, bot, import/replacement, scoped Excel-export or storage-policy changes. No new per-row controls, fonts or timers. Native observer deployment is unchanged.

Validation: current-versus-entry stop cases for MT4/MT5; empty/invalid/unknown/stale/wrong-identity data; cache round trips preserving unknown status and numeric fallbacks; measured Open geometry including10000positions; badge bounds; actual MainForm manual/live projection and stop-addition updates; menu hit testing and Open/Show bounds; English/Persian at normal/125%. Existing application, financial/status, storage and scoped-export regressions pass. Framework4.5 reference build; installer embedded payload/resources and downloadable file hashes verified.

Limits: synthetic Mono/Linux positions and GUI, no new native broker/Windows session execution. Warning is as of the displayed snapshot/freshness time, not an assertion about a disconnected account's current state. Prior native resource-capacity limits remain.

Installer: MetaFactory-Setup-3.64.2-preview.exe
Full source and blank Excel template: MetaFactory-3.64.2-preview-Full-Package.zip
