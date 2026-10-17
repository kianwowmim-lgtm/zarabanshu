# ضربان‌شو – ساخت APK با GitHub Actions

## مراحل
1. این پوشه را در یک ریپازیتوری جدید در GitHub قرار دهید (شاخه‌ی `main`).
   ```bash
   git init && git add . && git commit -m "init"
   git branch -M main
   git remote add origin https://github.com/<you>/zarbanshu.git
   git push -u origin main
   ```
2. به تب **Actions** بروید و workflow با نام **Build APK** را اجرا کنید (با push خودکار هم اجرا می‌شود).
3. پس از پایان، در صفحه‌ی همان اجرا بخش **Artifacts** را باز کنید و فایل `zarbanshu-debug-apk` را دانلود کنید. داخل آن `app-debug.apk` است.
4. فایل APK را روی گوشی اندروید منتقل کنید، «نصب از منابع ناشناس» را در تنظیمات مجاز کنید و نصب کنید.

## نکته‌ها
- این نسخه APK دیباگ است و برای استفاده‌ی شخصی و تست مناسب است. برای انتشار در گوگل‌پلی به نسخه‌ی امضاشده (release + keystore) نیاز است.
- نام پکیج: `com.zarbanshu.app` (در `capacitor.config.json` قابل تغییر است).
- محتوای بازی در `www/index.html` است؛ هر تغییری در آن را commit کنید تا APK جدید ساخته شود.
