# MetaFactory 3.50.0 preview — launch A/B comparison

Based on the original 3.48.2 appearance. None of the rejected 3.49.x visual changes are included.

Tick the same closed accounts and use the arrow beside Run:
- Run without report EA: isolated empty profile, no reporter preparation/compiler/symbol probe. Original profiles and charts stay intact; any files saved in the private profile are backed up on its next use.
- Run with live report EA: existing 3.48.2 live preparation and collectors, unchanged.

The Run button shows the selected mode. It persists and applies to subsequent manual opens, including row Open. Changing mode does not restart a running terminal. Manual/scheduled report reading is a separate operation, not this launch-mode switch.

Controlled comparison:
1. Disable folder auto-refresh and scheduled delivery for the test. Close the terminals. Select the same 5–6 accounts initially.
2. Choose ordinary mode; wait two minutes after the last terminal starts.
3. Close those terminals completely, select the same accounts and choose live mode. Again wait at least two minutes after the last start; allow more time if live readiness is pending.
4. Use Run arrow > Launch comparison diagnostics, or Tools > System check. Both runs are retained in one report (last eight batches, up to128 copies per batch).
5. Repeat in reverse order if a large difference appears; warm caches, updates, network and other applications can confound a single pair.

Diagnostics separate preparation, launcher/spawn return, observed window and first fresh verified live dashboard. Window presence is not broker-connection proof. Resource observations use the existing observer: samples every5s for first120s per process; readiness observations up to10min. CPU is cumulative terminal CPU time, not whole-system utilization. Missing values stay unknown. Plain mode has N/A live readiness and never presents an old snapshot as live. Account identity is hashed for cohort matching; no passwords or account login values are written to the A/B file. Sampled per-process memory peaks are not simultaneous total RAM.

No claim of Windows/broker performance validation: included checks are logic/unit tests and synthetic Mono UI checks. Native MQL collectors, bridge, reporting math and original appearance components remain byte identical to3.48.2.

راهنمای کوتاه:
حساب‌ها را انتخاب کنید و فلش کنار «اجرا» را بزنید. ابتدا «اجرای عادی بدون اکسپرت گزارش‌خوان» را امتحان کنید. دو دقیقه بعد از باز شدن آخرین نسخه صبر کنید، همه را ببندید و همان حساب‌ها را با «اکسپرت گزارش زنده» باز کنید. سپس «مقایسهٔ اجراها در عیب‌یابی» را بزنید و متن کامل گزارش را بفرستید. در زمان مقایسه، به‌روزرسانی خودکار پوشه‌ها و زمان‌بندی ارسال خاموش باشد و دستی گزارش نگیرید. نام حالت روی دکمهٔ اجرا مشخص است؛ تغییر حالت روی متاتریدرهایی که از قبل باز هستند اعمال نمی‌شود.
