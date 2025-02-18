---
title : "قوانین امنیتی"
---

# قوانین امنیتی 

### جدول محتوا

## بررسی اجمالی

پچیم این امکان را به شما می‌دهد که وبسایت خود را با پسورد بر پایه [اصالت‌سنجی برای دسترسی‌های اولیه](https://fa.wikipedia.org/wiki/%D8%A7%D8%B5%D8%A7%D9%84%D8%AA%E2%80%8C%D8%B3%D9%86%D8%AC%DB%8C_%D8%A8%D8%B1%D8%A7%DB%8C_%D8%AF%D8%B3%D8%AA%D8%B1%D8%B3%DB%8C%E2%80%8C%D9%87%D8%A7%DB%8C_%D8%A7%D9%88%D9%84%DB%8C%D9%87) محافظت کنید، البته این امکان را هم به شما می‌دهد که مشخص کنید این پسورد برای کل وبسایت قرار بگیرد یا روت‌های بخصوصی که شما مشخص می‌کنید.

## مدیریت قوانین امنیتی

### ایجاد قانون امنیتی 

ایجاد کردن یک قانون امنیتی اصلا کاری ندارد، تنها کافیست وارد پنل مدیریتی سایت مورد نظر و بخش امنیتی شوید و بر روی دکمه اضافه کردن قانون امنیتی جدید کلیک کنید. با وارد کردن اطلاعات مورد نیاز شما می‌توانید قانون امنیتی مورد نیاز خود را به سایت‌تان اضافه کنید.

این قابلیت در پچیم وجود دارد که به شما اجازه می‌دهد چندین نام کاربری و پسورد را برای قانون مورد نظر خود قرار دهید.

### ویرایش و حذف قانون

اگر قانونی برای شما بلا استفاده شد و نیازی به آن ندارید به سادگی با کلیک بر روی دکمه حذف می‌توانید آن قانون را به کلی از سایت خود حذف کنید.

شما مستقیما نمی‌توانید نام کاربری و پسورد قانون مورد نظر خود را ویرایش کنید اما می‌توانید نام کاربری و پسورد جدیدی را به قانون قبلی خود اضافه کنید، برای انجام این کار هم تنها کافیست بر روی دکمه قانون جدید کلیک کنید و نام و مسیر قانون قبلی راه اعمال کنید و نام کاربری و پسورد جدید را ثبت کنید با اینکار نام‌های کاربری مشخص شده و پسورد آن در کنار اطلاعات قبلی در سایت شما ثبت می‌شود.


## اعتبارنامه‌ها

 پچیم برای ایجاد یک قانون جدید در اصل یک فایل یکتا `.htpasswd` به ازای هر قانون امنیتی در سرور شما ایجاد می‌کند و هر کدام از این فایل‌ها اعتبارنامه‌های (نام‌های کاربری و پسورد‌های‌) خود را دارند. اگر شما قصد دارید برای دو مسیر از سایت خود قانون امنیتی با یک نام کاربری و پسورد یکسان قرار دهید نیاز است به شکل جداگانه‌ای از طریق پنل کاربری اینکار را برای هر کدام به انجام برسانید.
 
شما می‌توانید فایل‌های `.htpasswd` را در مسیر `/etc/nginx/pachim-conf/.../server/.htpasswd-{ruleId}` سرور خود پیدا کنید.

:::note{.warning}
::title[نکته امنیتی]

هیچ کدام از پسورد‌های که شما در بخش قوانین امنیتی وارد می‌کنید `به هیچ عنوان در پچیم ذخیره سازی‌ نمی‌شوند`.

:::

## شخصی سازی 

بر اساس [**مستندات Nginx**](https://docs.nginx.com/nginx/admin-guide/security-controls/configuring-http-basic-authentication/#) شما می‌توانید موارد دیگری را نیز به فایل `.htpasswd` اضافه کنید، مانند اینکه چه IP اجازه درخواست دارد یا چه IP اجازه درخواست ندارد، در حال حاضر پچیم این مورد را پشتیبانی نمی‌کند اما شما آزاد هستید که از طریق ترمینال و SSH به فایل `.htpasswd` مربوط به قانون مورد نظر خود مراجعه کنید و این موارد را به آن اضافه کنید.

اگر این موضوع ضروریست و کار شما را راحت‌تر می‌کند به پشتیبانی ما پیام دهید در صورت اینکه تعداد درخواست کنندگان این ویژگی بالا رود این ویژگی به سایت اضافه می‌شود.
