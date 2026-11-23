# MetaFactory 3.50.1 preview

Based on 3.50.0 / original 3.48.2 appearance. Ordinary/live launch choice and A/B history remain available.

Changes:
- No private MT5 terminal or symbol-verification probe runs on the manual live-start critical path. Local, explicitly unverified account/chart/cache hints seed the display chart. Financial readiness still requires the existing validated fresh native feed.
- The MT5 EA checks its own display symbol after matching-account connection. If unreadable, it inspects a bounded set of selected symbols and up to four additional subscriptions every five seconds, then changes only its own chart when a quote is available. Reporting remains timer/account driven; it never waits for a chart tick.
- If snapshot replacement fails, the native EA can atomically publish the same closed complete frame to snapshot.txt.fallback. The reader chooses the newest completed slot, then applies the original identity, run/sequence, freshness and history-proof checks. New stopped/error/mismatched/invalid data is not replaced with older ready data. If both writes fail, no fresh feed is invented.
- Manual MT5 startup uses one or two observed initializer slots based on free RAM. A fresh verified dashboard or a window with three seconds of quiet CPU frees a slot. Native-update handoff retains the slot and rebinds to the managed replacement process. After a 90-second observation deadline the queue can continue; the slow process is never killed or assumed ready. This is not a total terminal cap. MT4 launch pacing is unchanged.
- Diagnostics record staging waits/deadlines and software version in the comparison conditions so different releases are not labelled as identical conditions.

Close MetaFactory and the managed terminals before installation. Select the same 20 test accounts, choose Run with live report EA, wait at least two minutes after the final launch and copy the full system-check text. First launch can include automatic one-time compilation of the new EA; later copies sharing the same compiler/source cache reuse it. No need to enable algorithmic trading for reporting.

Validation: 2296 logic checks passed, zero failures, one pre-existing Python chart-retry skip in the Mono image. Synthetic queue tests check low-memory staging, update-exit grace, deadline progress and leaving processes running. Transport tests exercise a locked primary, alternate publication selection, stopped/disconnected/mismatched/invalid/stale frames and unchanged financial proof. Native financial serialization/history/lease functions and manual-report scripts/bridge are audited against 3.50.0. Appearance components and financial math are unchanged.

Limit: no Windows/MetaEditor/broker runtime or speed benchmark is available in this workspace. MQL sources are embedded and MetaEditor compiles them automatically on the user's Windows machine; native API changes require that runtime validation. Transport fallback improves resilience to a blocked primary file; it is not proof of the cause of the earlier error5004.

راهنما: همهٔ متاتریدرها و متافکتوری را ببندید و نصب کنید. همان۲۰حساب قبلی را انتخاب کنید و از فلش کنار اجرا، حالت «با اکسپرت گزارش زنده» را بزنید. بعد از آخرین اجرا حداقل دو دقیقه صبر کنید و متن کامل عیب‌یابی را بفرستید. اجرای اول ممکن است برای کامپایل خودکار اکسپرت جدید مکث کند. ظاهر قبلی و گزینهٔ اجرای بدون اکسپرت حفظ شده‌اند.
