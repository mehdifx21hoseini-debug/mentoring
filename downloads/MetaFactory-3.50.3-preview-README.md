# MetaFactory 3.50.3 preview — updater observer lifetime correction

The3.50.2 report confirms20 processes dispatched in177s and zero added memory-pacing waits, but MT5 windows/readiness still lagged. The tested MT5 cohort changed to37/38/39/40/41/42/43/45/46/48, so it is not a controlled speed percentage comparison with the earlier01–18 cohort.

A concrete3.50.2 diagnostic bug remained: RefreshGrid disposes its temporary process-enumeration objects. Updater rebinding saved that borrowed object, so retained native capacity handles continued reporting a live process while A/B window/CPU/first-ready observations froze.3.50.3 retains an independent Process wrapper, validates kernel creation time plus exact path/account/cohort, and disposes only its owned wrappers on exit, eviction or shutdown. It never closes a terminal. A regression test reproduces caller disposal and confirms the observer still works.

New read-only Systemcheck sections separate current validated dashboard readiness from historical A/B first-ready counts, and report native feed state/reason, history availability and broker-time-offset proof. Primary/fallback transport metadata is bounded and explicitly not financial proof. No validation is relaxed. Native MQL scripts, bridge, financial calculations, startup pacing and original appearance remain byte identical to3.50.2. Historical counts are not retroactively repaired. This is an observer/diagnostic correction, not a claim that remaining native MT5 startup delays are solved.

If the20 terminals from the last test are still running, leave them open. Close only MetaFactory, install3.50.3, reopen it, wait10–20seconds and copy full Systemcheck text. The installer leaves MetaTrader terminals open. This avoids another full cold-start test and lets the current-readiness section reveal why remaining reports are unavailable.

UAC automation remains pending. Cached metadata showed a MetaQuotes updater with no per-path compatibility flags; it does not identify the exact protected-dialog caller or authorize a generic auto-Yes implementation. No UAC policy, elevation helper, scheduled task or registry change is introduced.

Validation:2322logic checks passed0failed, one existing Python chart-retry skip in the Mono image. Independent retained-wrapper/caller-disposal and no-kill cleanup regression, plus all prior PID/identity/transport tests. Microsoft.NET4.5 reference build, PE versions/resources/installer payload verified. No actual Windows/broker speed benchmark in this workspace.

راهنما: اگر متاتریدرهای آزمون قبلی هنوز باز هستند، آن‌ها را باز نگه دارید. فقط متافکتوری را ببندید و نسخهٔ جدید را نصب کنید. بعد از بازکردن برنامه۱۰تا۲۰ثانیه صبر کنید و متن کامل عیب‌یابی را بفرستید. این نسخه ثبت آمار پس از آپدیت را اصلاح می‌کند و دلیل آماده‌نبودن گزارش هر حساب را جدا نشان می‌دهد؛ تأیید خودکار پیام امنیتی ویندوز هنوز اضافه نشده است.
