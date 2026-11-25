# MetaFactory 3.55.1 preview — public Telegram reports

The bot connection screen now has only token input, enable and save/connect (plus optional token-file import). No user IDs, enrollment, role selection or sender lookup is required for reports.

On the Windows PC holding MetaFactory accounts:
1. Open Tools > Telegram bot.
2. Paste the full BotFather token (or import the existing private .mfbot file), enable the bot and Save and connect.
3. Send /start privately to the bot. Menus are returned to every visitor, and report results go to that visitor's own chat automatically. Keep MetaFactory and this PC online.

Public mode deliberately makes the configured account reports accessible to anyone who contacts the bot privately. Menus include students, folders, all-account scope, date ranges, fresh vs explicitly cached reports, live status and content selection. Request-time freshness, account binding and existing financial calculations are unchanged. Public report users are not automatically terminal administrators; previously configured administrators retain their existing terminal controls.

Command menus are registered for all private chats. The main-panel manual-send recipient list is discovered automatically from people who have contacted the running bot, so there is no ID-entry step there either. Recent recipient routing is in memory; users can send /start again after app restart. Messages to groups are not used for report routing.

The connection window explicitly saves public report mode. Existing private profiles are preserved on deserialization/startup until the operator opens this window and saves; upgrading alone does not silently publish another installation's private reports. New unconfigured profiles default to public report mode with the bot still disabled until a token is saved/enabled. Existing scheduled delivery credentials remain separate and unchanged.

The real supplied token is not embedded in the public installer, source or package. It is encrypted for the current Windows user after saving. Native reporter sources and financial/freshness helpers are unchanged from3.55.0. Webhooks are never deleted or replaced.

Verification: model/mock API tests and normal/125% .NET/Mono UI checks. Direct access to api.telegram.org from this build environment still fails with proxy CONNECT403, so the actual token, bot menu registration, delivery and live broker outputs have NOT been confirmed from here. They are activated and verified by the running Windows app after Save and connect.
