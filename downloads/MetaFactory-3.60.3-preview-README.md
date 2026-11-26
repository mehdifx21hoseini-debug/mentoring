# MetaFactory 3.60.3 preview — توضیحات فارسی در ورود دانشجو

در پنجرهٔ افزودن دانشجو از متن یا اکسل، توضیحات نتیجه و متن کپیِ درخواست اصلاح، حتی با زبان انگلیسی برنامه، فارسی هستند. دکمه‌ها، ستون‌های مشخصات و وضعیت‌ها از زبان فعلی رابط پیروی می‌کنند؛ نام، شماره حساب، سرور و شناسهٔ MT4/MT5 دست‌کاری نمی‌شوند.

- توضیحات شناخته‌شدهٔ رد ورود، پایان زمان بررسی، تکراری، اطلاعات ناقص، بررسی سرور و ثبت موفق به فارسی نمایش داده می‌شوند.
- کپی وضعیت همان نفر یا «کپی موارد نیازمند اصلاح»، توضیح و درخواست فارسی می‌دهد. رمزها مانند قبل حذف می‌شوند.
- توضیحات در خروجی نتیجهٔ Excel هم فارسی است. خروجی اطلاعات قابل ورود مجدد، قالب و داده‌های حساب همان ساختار قبلی را دارند.
- جهت متنِ ستون توضیحات راست‌به‌چپ است و ارتفاع ردیف با متن متناسب می‌شود. توضیح بلند در راهنمای موس و متن کپی کامل در دسترس است.
- پیام فنی ناشناخته با مقدمهٔ فارسی و جزئیات اصلی/کد خطا حفظ می‌شود؛ علت حدسی یا حکم اشتباه دربارهٔ رمز ساخته نمی‌شود.

This is import presentation/localization only. Raw verification reasons and status flags are retained. The application language is never temporarily switched to translate a message, including parallel workers. Verified-only registration, server probing, credential handling, main/report UI, native/financial logic and the3.60.2 language-close fix are unchanged.

Validation:13 focused Persian-description/copy/Excel/thread-safety checks;37 import-model checks;2394 application checks;28 import UI checks at normal scale and28 at125% in English/Persian, all passed. App/installer PE versions, resources and embedded payload verified. Tests used synthetic accounts/private-login verifiers on Mono; native Windows font shaping and real broker execution were not newly tested. Public artifacts contain no supplied bot tokens or real student passwords.
