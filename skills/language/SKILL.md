---
name: language
description: >-
  RTL Persian writing style for all agent responses, progress reports, and
  result summaries. Enforces right-to-left formatting with English words placed
  on separate lines when embedded in Persian text. Always active when
  communicating with this user in Persian/Farsi.
---

# اسکیل زبان — Language Skill

## قانون اصلی — اجباری

هر پاسخ فارسی **باید** داخل تگ HTML زیر نوشته شود تا متن از سمت راست شروع شود:

```html
<div dir="rtl">

متن فارسی اینجا

</div>
```

## قوانین نوشتاری

### ۱. کلمات انگلیسی در جمله فارسی

هر کلمه یا عبارت انگلیسی که بخواهی در یک جمله فارسی استفاده کنی، باید در **خط جداگانه** بنویسی:

**درست:**
```
من الان سایتت رو روی
Cloudflare
آپلود کردم و زمان
run
کردن سایته!
```

**غلط:**
```
من الان سایتت رو روی Cloudflare آپلود کردم و زمان run کردن سایته!
```

### ۲. مسیرها، دستورات، پکیج‌ها

همه این موارد در خط جداگانه:
- مسیر فایل‌ها: `src/App.tsx`
- دستورات ترمینال: `npm run dev`
- نام پکیج‌ها: `react-query`
- URL ها: `https://example.com`

### ۳. ساختار پاسخ کامل

```html
<div dir="rtl">

توضیح فارسی اینجا...

فایل
`src/index.ts`
رو ویرایش کردم و دستور
`npm install`
رو اجرا کردم.

</div>
```

### ۴. گزارش پیشرفت (در حین کار)

```html
<div dir="rtl">

دارم فایل‌های پروژه رو بررسی می‌کنم...

فایل
`package.json`
رو خوندم تا وابستگی‌ها رو بفهمم.

در حال اجرای
`npm install`
هستم...

</div>
```

### ۵. گزارش نتیجه (بعد از اتمام کار)

```html
<div dir="rtl">

کارهایی که انجام دادم:

۱. فایل
`index.html`
رو ساختم

۲. پروژه رو روی
`Vercel`
دیپلوی کردم

۳. لینک سایت:
`https://your-project.vercel.app`

</div>
```

### ۶. گزارش خطا

```html
<div dir="rtl">

یه خطا پیدا کردم:

`TypeError: Cannot read property 'map' of undefined`

این خطا توی فایل
`src/components/List.tsx`
خط ۴۵ هست.

</div>
```

## نکات مهم

- **همیشه** از `<div dir="rtl">` استفاده کن — بدون استثنا
- اعداد فارسی (۱، ۲، ۳) برای لیست‌های فارسی
- از علائم نگارشی فارسی استفاده کن: «»، ،، ؛
- کدبلاک‌های چندخطی هنوز می‌توانند داخل div باشند
