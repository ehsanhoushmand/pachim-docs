---
title : "توزیع بار"
---

# توزیع بار

### جدول محتوا

## بررسی اجمالی

ویژگی توزیع بار برای به اشتراک گذاشتن ترافیک سایت شما بین چند سرور مورد استفاده قرار میگیرد و به جای اینکه یک سرور به درخواست‌های کاربران پاسخگو باشد چندین سرور اینکار را انجام می‌دهند و به این موضوع توزیع بار سرور می‌گویند. این موضوع به وبسایت‌های پربازدید کمک می‌کند تا بتوانند حجم زیادی از ورودی وبسایت خود را بین چند سرور توزیع کنند تا تجربه بدونه مشکلی را برای کاربران خود ایجاد کنند.

برای ایجاد کردن یک سیستم توزیع بار شما نیاز دارید یک سرور توزیع بار ایجاد کنید، برای اینکار کافیست زمانی که قصد ساخت سرور دارید نوع توزیع بار را انتخاب کنید، با انتخاب سرور توزیع بار تنها بر روی سرور شما Nginx نصب خواهد شد و شما هیچ اپلیکیشنی را مستقیما بر روی سرور بار نمی‌توانید بالا بی‌آورید.

## ایجاد توزیع بار

بعد از راه اندازی سرور توزیع بار شما باید وبسایت توزیع بار خود را در این سرور راه اندازی کنید، دامنه‌ای اصلی وبسایت خود را وارد کنید و وبسایت مورد نظر را ایجاد کنید.

:::note{.tip}
شما از یک سرور توزیع بار می‌توانید برای توزیع بار چندین سایت استفاده کنید و این نوع از سرورها یکبار مصرف و فقط برای یک سایت نیستند.
:::

حالا بعد از آنکه وبسایت مورد نظر را به سرور توزیع بار اضافه کردید وقتی وارد وبسایت مورد نظر در پنل پَچیم شوید، صفحه‌ای با عنوان توزیع بار مشاهده خواهید کرد. 
### روش‌های توزیع بار 

ما در پَچیم از دو مدل توزیع بار استفاده می‌کنیم که به شما اجازه می‌دهد آزادی عمل بیشتری داشته باشید. 

- توزیع بار در شبکه خصوصی
- توزیع بار در شبکه عمومی

درک کردن هر کدام از این روش‌ها در پیاده سازی توزیع بار بسیار بسیار مهم است که در زیر به تفضیل این دو را به شما توضیح خواهیم داد.

#### توزیع بار با شبکه خصوصی

توزیع بار با شبکه خصوصی روشی است که **سرورهای شما باید حتما دارای آدرس IP خصوصی باشند و از طریق آدرس‌های خصوصی توانایی ارتباط برقرار کردن با هم را داشته باشند** در غیر این صورت امکان استفاده کردن از این روش وجود ندارد. متاسفانه در ایران به دلیل وجود نداشتن سرورهای ابری متفاوت کمتر سرویس ‌دهنده‌ای را پیدا می‌کنید که این سرورهای به شما ارائه دهد که با استفاده از Ip خصوصی با هم در ارتباط باشند.

البته بعضی از سرویس‌دهنده ها هم چنین کاری انجام می‌دهند مانند ابرآروان و پارس پک (استفاده کردن یا نکردن از هر کدام به عهده خود شماست البته ممکن است موارد دیگری وجود داشته باشید که میتوانید از طریق لینک تغییر این صفحه در گیت‌هاب در انتهای این صفحه آنها را به ما معرفی کنید. ) 

#### توزیع بار در شبکه عمومی 

بدلیل محدود بودن ارائه دهندگانی که قابلیت شبکه خصوصی را داشته باشند ما سعی کردیم ویژگی دیگری را آماده کنیم تا با استفاده از آن بتوانید سرورهای با منطقه مکانی متفاوت تر را در قالب توزیع بار مورد استفاده قرار دهد. این روش با استفاده از Ip عمومی سرورها پیاده سازی ‌می‌شود و از طریق همین Ip هم سرورها با هم ارتباط برقرار می‌کنند.

با این حالت فرقی ندارد، شما سرورتان را از کدام ارائه دهنده و یا از کجای دنیا تهیه می‌کنید، شما می‌توانید برای مثال دو سرور در ایران و یک سرور در خارج از ایران تهیه کنید و بار سرورتان را بین آن‌ها تقسیم کنید.


### تفاوت روش شبکه خصوصی و شبکه عمومی

طبیعی است که بین روش شبکه خصوصی و شبک عمومی تفاوت‌های وجود داشته باشد که باعث برتری هر کدام نسبت به دیگری می‌شود. در زیر دو مورد از این تفاوت‌ها را برایتان توضیح خواهیم داد تا کاملا متوجه موضوع شوید.

#### سرعت دسترسی سرورها در شبکه خصوصی و عمومی 

زمانی که شما یک شبکه شخصوصی از سرورها را ایجاد کنید و سرورها با ip خصوصی با هم در ارتباط باشند طبیعتا سرعت این ارتباط در این شبکه خصوصی بالاتر از شبکه عمومی است، **بنابراین از نظر سرعت شبکه‌های خصوصی بهروری بهتری نسبت به شبکه‌های با Ip عمومی دارند**.

#### گواهی SSL در توزیع بار

در **شبکه خصوصی** الزامی برای داشتن SSL نیست اما معمولا سایت‌ها برای امنیت بیشتر نیاز به SSL دارند، برای این موضوع شما تنها کافیست برای سایتی که در سرور توزیع بار تعریف کرده‌اید وارد قسمت SSL شوید و SSL وبسایت را فعال کنید و تمام.

اما در **شبکه عمومی** وضع متفاوت است، چون سرورها از طریق Ip عمومی با هم ارتباط برقرار می‌کنند برای آنکه امنیت توزیع بار بین سرورها را حفظ کنید، حتما باید برای تک تک وبسایت‌های داخل شبکه توزیع بار، از SSL استفاده کنید.

:::note{.tip}
::title[استفاده از SSL شخصی]

برای SSL شبکه عمومی حتما پیشنهاد می‌کنیم. یک SSL شخصی برای دامنه خود تهیه کنید و به شکل دستی برای تک تک وبسایت های داخل شبکه توزیع فعال کنید و برای بوجود نیامدن `مشکلات عجیب از SSL رایگان برای توزیع بار` استفاده نکنید.

:::

در کل روش شبکه عمومی در استفاده از SSL رایگان چالش‌های متفاوتی دارد که ما آن را پیشنهاد نمی‌کنیم.

:::note{.warning}
::title[یادگیری پیاده سازی سرور توزیع بار به شکل عملی]

اگر با خواندن توضیحات بالا فکر می‌کنید که راه اندازی یک سرور توزیع بار کار بسیار سختی است، پیشنهاد می‌کنیم حتما دوره آموزش ویدیوی [`راه اندازی سرور و سایت با Pachim`](https://roocket.ir/series/server-managment-with-pachim) را مشاهده کنید در آن دوره به شکل عملی این موضوع را آموزش داده‌ایم.

:::
### متدهای مختلف توزیع بار

بعد از آنکه روش توزیع بار خود را انتخاب کردید، نوبت به متد توزیع بار میرسد، هر کدام از این متدها روش توزیع بار در سرور شما را مشخص می‌کند : 

- **Round Robin** : متد پیشفرض، با توجه به وزن سرورها بار روی سرور شما را بین سرورهای مشخص شده تقسیم می‌کند.
- **Least Connections** : درخواست‌ها را به سروری که کمترین تعداد درخواست کننده داشته باشد ارسال می‌کند.
- **IP Hash** :  آدرس IP کاربر تعیین می‌کند که درخواست به کدام سرور ارسال شود.

شما هر زمان که بخواهید می‌توانید متد توزیع بار را تغییر دهید.

### لیست سرورهای توزیع بار

حالا نوبت به مشخص کردن استخر سرورها رسیده، استخر در اینجا به این معنی است که درخواست کاربر، زمانی که به توزیع کننده بار برسد در این استخر  بر اساس متدی که مشخص کردید، تعین تکلیف می‌شود و به سرور مقصد برای پاسخگویی ارسال می‌شود.

#### اضافه کردن سرور به استخر سرورها 

شما می‌توانید با کلیک بر روی دکمه **سرور جدید**، یکی از سرورهای که از قبل آماده سازی کرده‌اید را با توجه به نوع شبکه توزیع بار به لیست سرورهای داخل استخر خود اضافه کنید.

توجه کنید اگر نوع شبکه شما خصوصی باشد حتما سرور مورد نظر شما باید دارای IP خصوصی باشد تا بتوانید به لیست سرورهای توزیع کننده بار خود آن را اضافه کنید.

#### وزن سرورها

در زمان ایجاد کردن سرور یا حتی ویرایش کردن سرور شما می‌توانید وزن هر سرور را مشخص کنید و بر اساس وزن مشخص شده و متد توزیع بار درخواست‌ها بین سرورهای داخل استخر سرورها تقسیم می‌شوند. 

برای مثال شما دو سرور دارید وزن یک سرور را ۱۰ و وزن سرور دیگر را ۲ قرار می‌دهید.  اگر ۱۲ درخواست به سرور شما ارسال شود ۱۰ تای آن به سروری با وزن ۱۰ ارسال می ‌شود و ۲ تای آن به سروری با وزن ۲.

#### سرورهای پشتیبان

شما می‌توانید به استخر سرورها، سرور پشتیبان هم اضافه کنید، این نوع از سرور تا زمانی که سرورهای معمول داخل استخر از دسترس خارج نشوند وارد پروسه کار نمی‌شوند و همیشه به عنوان پشتیبان در زمان‌های اضطراری مورد استفاده قرار میگیرند

#### متوقف کردن موقت سرور

اگر زمانی نیاز دارید سروری را موقتاً از استخر سرورها خارج کنید، نیازی نیست که آن را از لیست سرورهای داخل استخر حذف کنید، برای این کار کافیست که گزینه متوقف کردن سرور را در قسمت ویرایش سرور فعال کنید و بعد از اینکار تا زمانی که شما بخواید سرور مورد نظر از لیست سرور‌های استخر شما بدون حذف کردن، خارج می‌شود.

#### تنظیمات بیشتر در توزیع بار 

در کنار مواردی که در بالا توضیح دادیم، شما در پَچیم تنظیمات دیگری هم برای سرورهای داخل استخر خود می‌توانید تعیین کنید. در زیر چند مورد از این تنظیمات را به شما توضیح می‌دهیم : 

- **حداکثر اتصال** : شما می‌توانید مشخص کنید که هر سرور حداکثر تا چه تعداد اتصال می‌تواند داشته باشد.
- **حداکثر تعداد شکست** : شما می‌توانید برای یک سرور مشخص کنید که حداکثر می‌تواند چند شکست در پردازش درخواست کاربر را قبول کند تا سرور دیگری جایگزینش شود.
- **حداکثر زمان شکست** : این گزینه به nginx می گوید حداکثر چه مقدار باید منتظر بماند تا پاسخی از سرور دریافت کند در غیر این صورت یک شکست ثبت کند.