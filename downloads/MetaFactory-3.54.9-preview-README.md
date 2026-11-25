# MetaFactory 3.54.9 preview

Approved visual changes:
- Main action bar groups commands from the left; unused right area stays empty charcoal.
- Report-text dialog follows selected design4: student roster at the side, date/content settings above the preview, compact copy/save/close footer. All twelve original content flags, student selection/search/sort, custom dates, freshness warnings and copy/save behavior retained. Persian mirrors the report-dialog content naturally.
- Table keeps alternating white/gray row backgrounds when selected/hovered/open; checkbox, name hover, accent edge and black Show button still indicate state.
- Compact confirmation/message dialogs keep the standard MetaFactory title bar and omit the repeated inner brand heading. Important backup and account text is retained.

Overall Profit Factor:
- Independent of selected day/week/month/range; uses validated full account history, not the visible range.
- MT4: positive closed-order net totals / absolute negative closed-order net totals, excluding cash/credit and floating trades.
- MT5: full-history closed-position net totals including entry/exit commission, fee and swap. Open/partly open positions are excluded until fully closed. Existing full-history position aggregation is reused.
- New optional PF1 metadata is validated against the same complete history and its buy/sell net reconciliation; caches preserve the validated metadata. Missing/invalid proof shows unavailable rather than a range or invented value. MT5 requires a fresh report from the updated reporter before the number is available.
- No losing trades with gains shows infinity; no classified gains/losses shows unavailable. This is not an average profit or return percentage.

No Telegram token is bundled. Bot connection/control remains the next task after the user creates the bot; existing delivery settings are retained.

Validation details are recorded with this release. Automated .NET/Mono model and UI checks do not replace MetaEditor compilation or live broker validation on Windows. Native MT5 PF export compilation/statement parity still requires actual Windows verification. The pre-existing MT4-03 exit and folder-access investigation remains unresolved pending the user's native diagnostics; this release does not claim to cure it.
