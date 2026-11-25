# MetaFactory 3.53.0 preview

یادداشت دانشجو، بازخورد نام و انتخاب‌های عملیات

- از منوی سه‌نقطهٔ هر دانشجو، «یادداشت…» را باز کنید؛ متن چندخطی ذخیره، ویرایش یا حذف می‌شود و زمان آخرین ویرایش نمایش داده می‌شود.
- دانشجوی دارای یادداشت، کنار نام نشانهٔ کوچکی دارد؛ کلیک روی نشانه یادداشت را باز می‌کند. کلیک روی خود نام همان صفحهٔ اصلی اطلاعات و گزارش را باز می‌کند و با رفتن موس روی نام، رنگ آن آبی می‌شود.
- پس از پذیرش اجرای متاتریدر، گزارش دستی یا بستن، تیک حساب‌های پذیرفته‌شده برداشته می‌شود. صف، حساب‌های اولیه را حفظ می‌کند. عملیات لغوشده یا ردشده و گزارش‌های خودکار، انتخاب کاربر را پاک نمی‌کنند.
- یادداشت‌ها محلی هستند و در پشتیبان استاندارد برنامه هم ذخیره و بازگردانی می‌شوند. پشتیبان قدیمی بدون یادداشت، یادداشت موجود را پاک نمی‌کند. یادداشت به گزارش‌ها یا کانال‌های ارسال اضافه نمی‌شود.
- قالب جدول، شماره‌گذاری هر فهرست، ردیف‌های سفید و طوسی، خروجی اکسل در ابزارها و فاصلهٔ لوگو و عنوان از نسخهٔ 3.52.4 حفظ شده‌اند.

نصب: متافکتوری را ببندید و نصب‌کننده را اجرا کنید؛ سپس برنامه را دوباره باز کنید. حساب‌ها و تنظیمات موجود حفظ می‌شوند. همیشه نگه‌داشتن یک پشتیبان پیش از نصب توصیه می‌شود.

## Validation

Built against Microsoft .NET Framework 4.5 reference assemblies. Existing logic suite: 2376 passed, 0 failed (one pre-existing Python-on-Unix chart test skipped in the Mono container). Notes model tests cover multiline Unicode, atomic persistence, encrypted backup roundtrip, restore mapping, legacy backups, deletion and corrupt-file preservation. UI tests use synthetic accounts under Linux Mono/Xvfb in English and Persian at normal and simulated 125% scale; no real terminals or delivery transports are launched. Native Windows font/DPI rendering and broker operation are not validated here.

Native MT4/MT5 reporter sources, report math, history/freshness rules, scheduling engine and update policy are unchanged. UI queue admission adds selection consumption after accepted work; reporting targets are snapshotted beforehand. Local note files are encoded for reliable storage, not encrypted; the existing encrypted backup container also includes notes.
