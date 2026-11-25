# MetaFactory 3.54.0 preview

## تغییرات

- افراد را مانند قبل از فهرست انتخاب کنید (یک نفر، چند نفر یا انتخاب همه) و «اجرا» را بزنید. پنجرهٔ تأیید فقط تعداد نسخه برای هر نفر را می‌پرسد و هر بار از **۱** شروع می‌شود. انتخاب تعداد ذخیره نمی‌شود و اجرای اضافه خودکار فعال نمی‌شود.
- پیش‌فرض یک نسخهٔ اصلی با گزارش زنده است. تعداد ۲ یعنی یک نسخهٔ اصلی و یک نسخهٔ بررسی بدون اکسپرت گزارش‌خوان؛ تعداد بیشتر، نسخه‌های بررسی بیشتری اضافه می‌کند. نسخه‌های باز دوباره اجرا نمی‌شوند؛ کم‌کردن عدد، پنجره‌های اضافهٔ موجود را نمی‌بندد. حالت عادی بدون اکسپرتِ قدیمی از منوی اجرای عادی همچنان قابل انتخاب است.
- برای فعال‌شدن گزارش زنده روی نسخهٔ اصلی که قبلاً به صورت عادی باز شده، آن را ببندید و دوباره اجرا کنید؛ برنامه حالت متاتریدر باز را بی‌اجازه تغییر نمی‌دهد. نسخهٔ بررسی در اولین اجرا محیط ساده دارد؛ چارت دلخواه را از خود متاتریدر باز کنید. چارت‌های آن هنگام اجرای دوباره حفظ می‌شوند.
- نسخه‌های بررسی در `_MTManager/review/<copy>/<number>` کنار پوشه‌های اصلی نگهداری می‌شوند. نسخهٔ اصلی، چارت‌ها و داده‌های گزارش زنده دست‌نخورده می‌مانند. نسخه‌های اضافه دانشجوی جدید یا هدف گزارش‌گیری نیستند. حساب اصلی برای هر نسخه به‌صورت جدا استفاده می‌شود؛ حساب یا رمز تازه‌ای از شما لازم نیست.
- صف اجرا، توقف صف، بستن انتخاب‌شده‌ها و بستن همه، نسخه‌های بررسی مربوط را هم در نظر می‌گیرند. بیشترشدن تعداد نسخه‌ها حافظه و فضای دیسک بیشتری مصرف می‌کند. بسته‌شدن متافکتوری، اجرای نسخه‌های باز را به‌طور خودکار متوقف نمی‌کند، مانند رفتار قبلی برنامه.
- ابزارها آیکون هماهنگ دارند: اکسل، پوشه، پشتیبان، بازگردانی، حافظهٔ ویندوز و جارو برای پاکسازی.
- خلاصهٔ پایان گزارش، تعداد موفق/ناموفق/گزارش قبلی و دلیل کوتاه را در همان نوار پایین نشان می‌دهد؛ کلیک پنجرهٔ نتیجهٔ جدا باز نمی‌کند. متن بلند در راهنمای زیر موس دیده می‌شود.
- خط قرمز تکراریِ آخرین خطا، روی نمای گزارش قبلی حذف شده و زمان آخرین خواندن حفظ شده است. وضعیت تازه/قبلی/ناموفق در منطق برنامه و نتایج گزارش حفظ می‌شود؛ دادهٔ قدیمی تازه تلقی نمی‌شود.
- صفحهٔ گزارش هفت شاخص فشرده، عنوان روشن «تعداد معاملات» با تفکیک باز/بسته و پروفیت فاکتور دارد. جدول ردیف‌های سفید و طوسی و عنوان‌های فارسی دارد. افت بازه، در صورت موجودبودن، زیر شاخص دراودان کلی نمایش داده می‌شود.
- پروفیت فاکتور فقط از نتایج خالص معاملات **بسته‌شده در بازهٔ انتخابی**، مطابق روش مالی موجود برنامه، محاسبه می‌شود؛ سود شناور و معاملات خارج از بازه وارد آن نمی‌شوند. بدون معامله مقدار «—» و سود بدون زیان «∞» نمایش داده می‌شود. مقدار حد ضرر همان آمار معتبر موجود برنامه است؛ پیپ فرضی یا نمونه جایگزین محاسبات نشده است.

## نصب

متافکتوری را ببندید، نصب‌کننده را اجرا و برنامه را دوباره باز کنید. داده‌ها، یادداشت‌ها و تنظیمات قبلی حفظ می‌شوند. برای آزمایش قابلیت جدید، ابتدا یک دانشجو را انتخاب و تعداد ۲ را اجرا کنید.

## Verification and limits

Strict Microsoft .NET Framework4.5 build. Synthetic Linux Mono/Xvfb model and UI checks cover PF boundaries/rounding, default/cancel/count preview, two confirmed targets yielding two live-primary requests plus two isolated plain review requests, queue cancellation/parent closing scope, visible menu icons, no duplicate cached warning, inline completion and narrow report rendering. Native report scripts, report engines, history and identity/freshness validation, existing Coach calculations, update policy, native launch pacing and scheduling engine are unchanged. Launcher changes add an explicit opt-in review branch; original callers keep review=false. The existing logic suite passed2376 checks (one pre-existing Python/Unix chart check skipped in Mono). UI rendering is tested at normal and simulated125% scale with synthetic accounts and stub launch delegates; no actual Windows terminals, broker login, concurrent broker sessions, Sandboxie execution or live performance benchmark is claimed. Real operation of the new review instances needs validation on the user's Windows system. Review chart folders persist separately and are not personal account backup exports.
