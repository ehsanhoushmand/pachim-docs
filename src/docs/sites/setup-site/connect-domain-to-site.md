---
title : "اتصال دامنه به سایت"
---

# اتصال دامنه به سایت

### جدول محتوا

## بررسی اجمالی

زمانی که شما یک سایت را از طریق پنل پَچیم به سرورتان اضافه می‌کنید برای آنکه آن سایت از طریق دامنه مورد نظرتان از طریق مرورگرها قابل دسترس باشد نیاز است دامنه را به سرورتان متصل کنید که در این صفحه قصد داریم دقیقا اینکار را به شما توضیح دهیم.

## سایت پیش فرض

قبل از هر چیزی ابتدا باید بدانید، زمانی که سرور شما راه اندازی می‌شود سایتی با عنوان default بروی سرور شما به شکل پیش فرض ساخته می‌شود. اگر IP سرورتان را در مرورگر وارد کنید می‌بینید که ظاهری را به شما نمایش می‌دهد که آن دقیقا همین سایت default ساخته شده است. دلیل ایجاد سایت default بعد از راه اندازی سرور شما این است که ممکن است شما بعد از راه اندازی سرور دامنه‌ای آماده ای برای استفاده نداشته باشید و یا اصلا بخواهید راه اندازی سرور خود را چک کنید که آیا همه چیز به درستی راه اندازی شده یا خیر.

در اکثر مواقع شما نیاز به این ندارید که سایتی از طریق IP اصلی سرور در دسترس باشد برای همین ممکن است سایت پیش فرض را حذف یا وارد تنظیمات سایت شوید و دامنه‌ای مورد نظرتان را به جای عنوان default برای آن قرار دهید.

اگر دامنه‌ای را خریداری کرده‌اید و تصمیم دارید آن را به سرور و سایت خود متصل کنید مستندات زیر را با دقت مطالعه کنید.

## آشنایی با DNS 

برای آنکه بتوانیم دامنه خود را سرور متصل کنیم در ابتدا باید کمی با مفهوم DNS آشنا شویم .

DNS مانند یک دفترچه تلفن برای اینترنت است. همانطور که شما برای تماس با دیگران به جای بخاطر سپردن شماره‌ی آن‌ها، از دفترچه تلفن استفاده می‌کنید، DNS نیز مانند یک دفترچه تلفن عمل می‌کند و نیازی به حفظ کردن آدرس IP ها نیست. همانطور که می‌دانید، کامپیوترها برای اتصال به یکدیگر از اعداد یا همان IP آدرس‌ها استفاده می‌کنند.

DNS مخفف Domain Name System فهرست توزیع شده‌ای است که نام دامنه قابل خواندن توسط انسان مانند www.site.com را به اعداد خوانا برای کامپیوترها یعنی IP آدرس تبدیل می‌کند. برعکس این نیز در مورد DNS صدق می‌کند، یعنی DNS سیستمی است که نام دامنه وب را سازماندهی می‌کند و آن‌ها را برای همه کسانی که می‌خواهند به شبکه وصل شوند، قابل‌فهم‌تر می‌کند.


## آشنایی با CDN

قبل از اینکه توضیح دهیم چطوری از CDN استفاده کنیم در ابتدا اجازه دهید توضیح دهیم که CDN و DNS یک چیز نیستند. CDN ها به شبکه‌های توزیع محتوا گفته می‌شوند که در داخل خود مدیریت کننده DNS را نیز ارائه می‌دهند، زمانی که دامنه خود را بر روی یک CDN قرار می‌دهید درخواست‌های که به دامنه‌های شما ارسال می‌شود با توجه به موقعیت مکانی درخواست کننده از طریق کش کردن اطلاعات سرور اصلی شما سریع‌تر به کاربر مورد نظر نمایش داده می‌شود.

CDN ها جدا از ارائه کردن مدیریت کننده CDN امکانات بیشتری را در اختیارتان قرار میدهند، مانند جلوگیری از حملات DDOS, امنیت ابری و لو نرفتن IP های اصلی سرور و کلی موارد دیگر تا وبسایت سریع‌تر و امن‌تری داشته باشید که این روزها مورد استفاده خیلی از افراد قرار میگیرند، که معمولا اکثر این CDN ها امکان مدیریت DNS را به شکل **رایگان** در اختیار کاربرانشان قرار میدهند.

معرفی بضی از CDN های داخلی و خارجی :

- cloudflare
- dns made easy
- ابردراک
- آروان

شما می‌توانی بر اساس نیاز خود از یکی از این گزینه‌ها استفاده کنید یا موارد دیگر را در گوگل سرچ کنید.

## معرفی دامنه به DNS

زمانی که دامنه خود را تهیه کردید، ابتدا در یکی از سرویس‌های CDN ثبت نام کنید و دامنه خود را در آنجا ثبت کنید زمانی که دامنه را ثبت کنید از شما درخواست ‌می‌کند مقادیری را در قسمت nameserver دامنه خود وارد کنید بعد از انجام اینکار بین ۲۴ تا ۷۲ ساعت زمان می‌برد که دامنه شما در سیستم ثبت شود. بعد از انجام این کار حالا نوبت به معرفی IP سرور به دامنه‌تان است.


## اتصال دامنه به سرور

حالا بعد از آن‌ که دامنه خود را به یک ارائه کننده DNS معرفی کردید باید وارد پنل مدیریت DNS آن شوید و یک رکورد از نوع A ایجاد کنید. نام این رکورد را عنوان دامنه خود قرار دهید و مقدار آن را IP سروری که با پَچیم راه اندازی کردید، قرار دهید. بعد از انجام اینکار با وارد کردن دامنه در مروگر وبسایتی که بر اساس دامنه بر روی سرور خود ایجاد کردید را می‌توانید مشاهده کنید.