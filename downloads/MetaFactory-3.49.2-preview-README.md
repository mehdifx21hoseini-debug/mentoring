# MetaFactory 3.49.2 preview

Appearance update based on 3.49.1. Settings, delivery, support, help and diagnostics use the main application workspace. Page/channel navigation never resizes the main window. Longer content scrolls internally. Accounts remain accessible through the Accounts tab. Save persists changes; Cancel or navigation discards the draft. Telegram, Bale and email keep independent enable switches. Reports groups the existing text and Excel commands; delivery actions retain send-now and latest delivery status. Technical options are grouped under Advanced. Existing reporting/native scripts, credentials, launch logic and financial calculations are unchanged.

Close MetaFactory before installing. Existing MetaTrader/account folders are not deleted. This release does not change terminal capacity or performance. Synthetic Mono UI checks are not a Windows/broker execution test.

Build: source/build.sh with Mono mcs, Microsoft .NET Framework 4.5 reference assemblies and llvm-rc. source/src/WorkspaceUi.cs contains the shared internal-page host.
