# MetaFactory 3.54.2 preview

- پس از پایان صف اجرا (از جمله اجرای زنده)، نوار بزرگ مانند پایان گزارش‌گیری به یک ردیف جمع‌وجور تبدیل می‌شود. شروع‌های موفق تیک سبز، خطاها ضربدر قرمز و موارد لغوشده/اجرانشده نشانهٔ خنثی دارند. فضای جدول برمی‌گردد و متن آماده‌سازیِ قدیمی در خلاصه نمی‌ماند.
- هنگام اجرا، نوار پیشرفت و توقف باقی است؛ توقفِ آماده‌سازی جاری پس از پایان همان کار جمع می‌شود. مواردی که هنوز شروع نشده‌اند موفق حساب نمی‌شوند. تیک سبز این نوار تأیید **شروع اجرا** است؛ اتصال حساب و گزارش زنده همچنان از وضعیت خود حساب مشخص می‌شود.
- دکمهٔ «باز کردن» زیر موس آبی میانه و خوانا (#2463B5) با نوشته/آیکون سفید است. حالت انتخاب‌شدهٔ آن نیز آبی است. دکمهٔ «نمایش» مشکی زغالی باقی می‌ماند تا دو حالت اشتباه نشوند.
- منطق اجرا، گزارش، تعداد نسخه‌ها، تنظیمات، ورود اکسل و توکن‌ها تغییر نکرده‌اند.

نصب: متافکتوری را ببندید، نصب‌کننده را اجرا و دوباره برنامه را باز کنید؛ داده‌ها و تنظیمات حفظ می‌شوند.

Validation: synthetic English/Persian Linux Mono/Xvfb UI checks at normal/simulated125%, exact Open/Show pixel colors, finished/failed/skipped/stopping launch count distinctions, compact completion and unchanged window bounds, stop/next-batch behavior, report completion regression, strict .NET Framework4.5 build, installer version/payload/native resource and actual downloaded artifact integrity checks. Existing launch/report models and all native logic are byte-identical; no broker authentication or Windows live execution benchmark is claimed. Native Windows rendering remains untested.
