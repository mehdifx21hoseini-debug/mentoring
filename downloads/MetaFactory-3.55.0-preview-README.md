# MetaFactory 3.55.0 preview — Telegram control

This release preserves 3.54.9 presentation, native reporters, financial calculations, local accounts and existing scheduled-delivery credentials. The Telegram control connection is separate and disabled by default.

Setup on the Windows PC holding the accounts:
1. Tools > Telegram bot > Import connection. Import the private .mfbot file supplied separately in the originating chat, or paste your own token.
2. Intended users send /start privately to the bot. With control still disabled, Find user IDs reads pending private messages without acknowledging/draining them. Only explicitly selected users are added. Alternatively enter numeric IDs, one per line: ID:report or ID:admin.
3. report users can request reports for all configured accounts. admin users additionally get terminal-open/close controls with a separate, expiring, one-use confirmation. Nobody is selected or made administrator automatically.
4. Enable requests and Save and connect, then send /start again. The app registers command menus for allowed private chats and renders inline buttons when requested. Windows, MetaFactory and system Internet/VPN must remain available.

Bot menus: students, folders, all-account scope, Today/Yesterday/Week/Month fresh reports, explicitly cached reports, validated live status,12 original content choices, help. Full PF/equity/account identity and read timestamps accompany the report. Long outputs are delivered as a text document.
Admin actions: one primary live copy per selected account; close review copies while keeping live; close live copies; close both, always through existing ownership-aware application methods. Dispatch acknowledgement is not a claim of successful broker connection.
Manual sends: Send > Send fresh report to Telegram bot lets the operator choose an allowed recipient and range for the existing selection/current list. Existing daily delivery settings remain separate; they are not overwritten or automatically enabled by importing a control token.

Freshness: live requests wait for a validated matching heartbeat at or after the request and matching account/full-history/server-time evidence. Missing range coverage uses the existing report reader. Native fresh results reject cached/cancelled/error rows, wrong identity, unverified history, unknown clock basis and pre-request/future timestamps. Unavailable fresh accounts have no financial figures; cached output is offered as a separate explicit choice. Cached reports with an unknown broker clock omit financial figures instead of inventing a requested day. Existing financial helpers are reused, including MT5 realization-day handling for live exports.

Credentials: the token is encrypted with Windows CurrentUser DPAPI after saving; no token is embedded in this public installer/source package. Changing it later needs no new build. The separately delivered private connection file is not in Git or the public ZIP. Passwords, local notes and raw bot updates are not exported in bot reports or control diagnostics.

Existing webhooks are detected and never removed/replaced. A conflicting long-poll client can cause HTTP409 and the new control worker stops; run only one controller for a bot. Scoped command menus may update the authorized chats as requested. Telegram sends with uncertain outcomes are not automatically resent.

Validation uses model/fake API and .NET/Mono UI tests, including normal/125% geometry and previous launch/close/table behavior. This environment denies api.telegram.org with a proxy403, so the supplied real token, real bot menu registration, real message delivery and real broker data have NOT been verified from here. Actual connection/registration happens after enabling the Windows app. Native Windows/MetaEditor verification limitations from3.54.9 remain; the old MT4-03 exit/access investigation is not claimed fixed.
