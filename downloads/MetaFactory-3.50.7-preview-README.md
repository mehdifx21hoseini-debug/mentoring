# MetaFactory 3.50.7 recovery preview

Fixes the 3.50.6 zero-start regression reported on Windows. The report shows authentication/quote preflight could fail before launch and file ACL protection could refuse startup, despite3.5GB free RAM.

Restores the proven3.50.5 credential-file lifecycle and local symbol startup path: no mandatory private terminal quote check, no file ACL requirement to start, no session-long credential retention. A current own-chart hint can replace the old launch-plan hint only with a recent verified same-account feed and own catalogue membership. This is a hint, not proof of current quote availability. Automatic recovery of every invalid-symbol startup and login prompt is NOT solved by this release.

The scoped3.50.6 per-user trusted-MetaQuotes RunAsInvoker helper remains. It does not grant elevation or click UAC Yes; explicit vendor elevation/first undiscovered updater prompts may remain. Its Windows behavior is still unverified. No global UAC change. Financial collector/math/validation, MT4, original appearance and pacing remain unchanged from3.50.5.

Close MetaFactory, install, reopen and test one MT5 first in Live mode. If successful, try five, not thirty-eight at once. Healthy terminals may stay open. No account/settings reset is required. Send System Check if a launch fails. Native source1.05unchanged; no newEAcompile expected unless compiler identity changed.

See source/VERIFICATION-3.50.7.json for automated checks; these do not replace actual Windows/broker testing.
