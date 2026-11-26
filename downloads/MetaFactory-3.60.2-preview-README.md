# MetaFactory 3.60.2 preview — language-switch shutdown correction

The supplied Windows screenshot shows “Safe handle has been closed” while the old window is removing temporary login files after changing language. The same exception message was reproduced in3.60.1 by disposing an already-stopped ImportCoordinator: its second Dispose called Set on an already-disposed AutoResetEvent.

Changes:
- ImportCoordinator shutdown is idempotent, including concurrent Dispose calls. Closing detaches the old window's queue reference and performs shutdown once.
- Reentrant WM_CLOSE during normal credential-cleanup message pumping cannot repeat resource disposal. Windows shutdown retains immediate startup-file cleanup behavior.
- A language rebuild does not enter the blocking protected-start-file waiting loop. The already-shared pending list transfers to the next window in the same process; the new window resumes its cleanup timer. It uses the original acknowledgement/expiry policy and original timestamps, rather than deleting a fresh startup file early or extending its lifetime.
- If a close request is cancelled before shutdown starts, the rebuild flag is cleared. Saved language still applies on the next normal launch.

No terminal is terminated merely to switch language. Plain names, note pencil, verified-only text/Excel import, financial/native reporting and bot behavior remain in place. No financial formula, native collector, startup pacing or update policy is changed.

Validation includes the exact old double-dispose reproducer, concurrent disposal, three real settings-to-window language transitions, pending-file handoff/resumption/expiry, repeated-close handling during a real cleanup loop, and a harmless running helper process to check no-kill behavior. Tests use synthetic .NET/Mono UI and files. They reproduce the managed lifecycle bug and check the fix; they do not reproduce the user's exact Windows process stack or perform real broker execution.

Install by closing MetaFactory and running this installer. Existing MetaTrader windows can stay open. After opening the updated app, change language in Settings as usual. Existing accounts and settings use the same storage.

Verification outcome:29 lifecycle checks,37 import model checks,2393 application checks,55 normal+55 at125% account UI/model checks passed,0 failures. One existing Python/Unix chart check skipped. Microsoft.NET Framework4.5 reference build and app/installer resource/version/embedded payload verified.
