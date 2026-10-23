<div dir="rtl">

# اسکیل و قانون فارسی RTL برای Google Antigravity

این مخزن شامل یک **Skill** و یک **Rule** اختصاصی برای دستیار هوش مصنوعی **Google Antigravity** است که نوشتار فارسی را به صورت استاندارد راست‌به‌چپ (RTL) اجباری می‌کند.

---

## مشکلی که این پکیج حل می‌کند

وقتی با دستیار Antigravity به فارسی کار می‌کنید، متن‌ها به‌صورت پیش‌فرض از **چپ** شروع می‌شوند و کلمات انگلیسی وسط جمله فارسی قرار می‌گیرند — که خوانایی را خراب می‌کند.

با نصب این پکیج:

✅ تمام پاسخ‌های فارسی از سمت **راست** شروع می‌شوند  
✅ کلمات انگلیسی در **خط جداگانه** نوشته می‌شوند  
✅ قالب‌بندی در **تمام پروژه‌ها** به‌صورت خودکار اعمال می‌شود

---

## ساختار مخزن

</div>

```
antigravity-persian-rtl/
├── skills/
│   └── language/
│       └── SKILL.md       ← اسکیل زبان (جزئیات کامل)
├── rules/
│   └── language.md        ← قانون ایجنت زبان (always-on)
└── README.md
```

<div dir="rtl">

---

## نصب

### مرحله ۱ — کپی فایل‌ها به مسیر گلوبال Antigravity

**فایل Skill:**

فایل
`skills/language/SKILL.md`
را به این مسیر کپی کنید:

</div>

```
C:\Users\<YourUsername>\.gemini\config\skills\language\SKILL.md
```

<div dir="rtl">

**فایل Rule:**

فایل
`rules/language.md`
را به این مسیر کپی کنید:

</div>

```
C:\Users\<YourUsername>\.gemini\config\rules\language.md
```

<div dir="rtl">

### مرحله ۲ — ساخت پوشه‌ها (اگر وجود ندارند)

در
`PowerShell`
این دستورات را اجرا کنید:

</div>

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.gemini\config\skills\language"
New-Item -ItemType Directory -Force "$env:USERPROFILE\.gemini\config\rules"
```

<div dir="rtl">

### مرحله ۳ — کپی خودکار با PowerShell

می‌توانید این دستورات را یکجا اجرا کنید:

</div>

```powershell
# کلون کردن مخزن
git clone https://github.com/MMDALIROX/antigravity-persian-rtl.git
cd antigravity-persian-rtl

# ساخت پوشه‌های مقصد
New-Item -ItemType Directory -Force "$env:USERPROFILE\.gemini\config\skills\language"
New-Item -ItemType Directory -Force "$env:USERPROFILE\.gemini\config\rules"

# کپی فایل‌ها
Copy-Item "skills\language\SKILL.md" "$env:USERPROFILE\.gemini\config\skills\language\SKILL.md" -Force
Copy-Item "rules\language.md" "$env:USERPROFILE\.gemini\config\rules\language.md" -Force

Write-Host "نصب با موفقیت انجام شد!"
```

<div dir="rtl">

---

## نتیجه بعد از نصب

پاسخ‌های دستیار به این شکل خواهند بود:

</div>

```html
<div dir="rtl">

پروژه‌ات رو روی
Cloudflare
دیپلوی کردم و دستور
npm run build
رو اجرا کردم.

</div>
```

<div dir="rtl">

به جای این شکل غلط:

</div>

```
پروژه‌ات رو روی Cloudflare دیپلوی کردم و دستور npm run build رو اجرا کردم.
```

<div dir="rtl">

---

## سازگاری

| سیستم‌عامل | مسیر گلوبال |
|------------|-------------|
| ویندوز | `C:\Users\<Username>\.gemini\config\` |
| مک / لینوکس | `~/.gemini/config/` |

---

## مجوز

این پروژه تحت مجوز
`MIT`
منتشر شده است. آزادانه استفاده و توسعه دهید.

---

ساخته‌شده برای بهبود تجربه کار با **Google Antigravity** به زبان فارسی 🇮🇷

</div>
