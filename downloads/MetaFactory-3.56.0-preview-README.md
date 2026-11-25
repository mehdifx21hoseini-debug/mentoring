# MetaFactory 3.56.0 preview — shared bot settings and launch cancellation fix

## Changes
- Bot configuration is in Settings > Bots and delivery. The Tools bot entry is removed. Each provider has one masked token field shared by incoming requests and outbound delivery, an enable checkbox and its own connection status.
- Telegram retains the previously working connection until settings are saved. Existing legacy settings migrate when saved. Only a changed bot connection restarts; unrelated edits do not restart the other bot.
- Bale supports private /start inline menus, students/folders/ranges, current or explicitly cached reports and manual report sending through the Send menu. Its API, credentials, callbacks and private-chat reply routing are separate from Telegram. Telegram-specific global command/menu methods are not sent to Bale; existing webhooks are never removed.
- No user IDs are required for public incoming report requests. A fixed destination is only needed for optional scheduled delivery. Enabling a bot does not enable daily/fixed-destination sends. Existing native financial/account/freshness validation is retained.
- Selected folder chips use the same blue and white text as New student. Other filters and alternating table rows retain their existing styling.
- Fixed a stale shutdown flag that could cancel every later manual live launch after changing language in the same app process. Shutdown of the obsolete symbol probe no longer blocks the independent manual preparation path. MT4 and MT5 regression checks cover shutdown followed by new preparation. This does not establish a fix for unrelated native terminal exits.

## Connect on Windows
1. Open Settings > Bots and delivery.
2. Select Telegram or Bale and paste the complete token from that provider. Alternatively import the separately supplied private .mfbot connection file. This optional file contains credentials and is not part of this public package.
3. Tick the checkbox beside the desired bot logo and Save changes. Leave daily delivery and fixed-destination sends off unless wanted.
4. With MetaFactory and this PC online, send /start privately to the corresponding bot. Reports return to the requesting chat. For manual Send, message the running bot first so your chat appears in its recipient list.

Use only one running MetaFactory poller for each bot. A Telegram token belongs in Telegram, a Bale token in Bale. Use a whole-system connection/VPN if the PC cannot reach Telegram; the user confirmed Telegram worked after enabling that connection. A browser-only connection is not sufficient for this Windows app.

Tokens are encrypted for the current Windows user after Save. No real token is embedded in the public installer/source/package. Public report mode is expressly user-requested: private bot visitors can request this installation's configured account reports, but do not automatically become terminal administrators.

## Verification and limits
.NET Framework 4.5 reference build, model/mock-provider checks, settings and launch/table UI regression checks, plus application tests are recorded in the release verification. Native reporters and financial calculations are unchanged from 3.55.1. Actual Telegram access was confirmed by the user on Windows; the build environment cannot reach the provider APIs, so actual Bale activation, real messages and broker terminal launches require validation on that Windows PC. Mock/UI checks do not establish native broker or live network success.
