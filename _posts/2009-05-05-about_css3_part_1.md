---
title: 'شناخت CSS۳ و قابلیت های آن &#8211; بخش اول'
author: فرهاد عیدی
layout: post
redirect_from: /5/
categories:
  - وب و طراحی
tags:
  - CSS3
---
کسانی که به نوعی با طراحی سایت و قالب سروکار دارند به خوبی میدانند CSS در ساختار یک قالب ارزش بسیاری دارد به خصوص از زمانی که پدیده ای به نام Web۲ پا به عرصه طراحی گذاشت. CSS هم مانند سایر زبان های برنامهنویسی، ورژن های مختلفی دارد. جدیدترین ورژن این زبان، ورژن سوم آن است که اخیرا ذهن طراحان را مشغول کرده است. در نسخه ی جدید CSS یعنی CSS۳ قابلیت هایی گنجانده شده است که شاید حیرت همگان را برانگیزد.در اینجا به معرفی برخی از این ویژگی ها میپردازیم که بسیار جالب و پرکاربرد هستند:

<!-- more -->

  
**۱. استفاده از Gradient در حاشیه ها:**  
شما میتوانید از خاصیت Gradient در حاشیه‌‌ی کادر خود استفاده کنید. برای مثال تصویر زیر را ببینید:

<div align="center">
  <a href="/asset/legacy/css3-border-1.gif"><img alt="Border in CSS3" src="/asset/legacy/css3-border-1.gif" width="445" height="43" /></a>
</div>

برای اینکه بتوانید کادری مثل کادر تصویر بالا را ایجاد نمایید باید از کدهای زیر استفاده کنید:  

{% highlight css %}
border: 8px solid #000;
-moz-border-bottom-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
-moz-border-top-colors:    #555 #666 #777 #888 #999 #aaa #bbb #ccc;
-moz-border-left-colors:   #555 #666 #777 #888 #999 #aaa #bbb #ccc;
-moz-border-right-colors:  #555 #666 #777 #888 #999 #aaa #bbb #ccc;
padding: 5px 5px 5px 15px;
{% endhighlight %}


**۲. استفاده از تصاویر به جای کد در کادر حاشیه :**  
در نسخه های قبلی CSS شما فقط میتوانستید از کدهای مخصوص رنگ در حاشیه ( Border ) استفاده کنید ولی در CSS۳ میتوانید از تصاویر نیز استفاده نمایید.

<div align="center">
  <a href="/asset/legacy/css3-border-2.gif"><img alt="Border in CSS3" src="/asset/legacy/css3-border-2.gif" /></a>
</div>

<div align="center">
  <a href="/asset/legacy/css3-border-3.gif"><img alt="Border in CSS3" src="/asset/legacy/css3-border-3.gif" /></a>
</div>

برای اینکه بتوان کادری با استفاده از تصاویر ایجاد کرد، از کدهای زیر استفاده میشود :  

{% highlight css %}
border-image:
border-top-image
border-right-image
border-bottom-image
border-left-image
border-corner-image:
border-top-left-image
border-top-right-image
border-bottom-left-image
border-bottom-right-image
{% endhighlight %}

یا  

{% highlight css %}
border-image: url(border.png) 27 27 27 27 round round;
{% endhighlight %}

یا

{% highlight css %}
border-image: url(border.png) 27 27 27 27 round round;
{% endhighlight %}

**۳. ایجاد گوشه های گرد در CSS۳ :**  
در نسخه‌ی جدید CSS یعنی CSS۳ شما میتوانید بدون استفاده از هیچگونه تصویری، حاشیه های سایت خود را به صورت منحنی درآورید. البته این قابلیت قبلا هم وجود داشت اما در CSS۳ کاملتر شده و تمام نیازهای شما را برطرف میکند. شما میتوانید به تک تک حاشیه های خود، خاصیت های متفاوت اضافه کنید. به عنوان مثال شما دوست دارید فقط یک گوشه ی سایت شما انحنا داشته باشد. به تصاویر زیر توجه کنید:

<div align="center">
  <a href="/asset/legacy/css3-border-4.gif"><img alt="Border in CSS3" src="/asset/legacy/css3-border-4.gif" width="445" height="140" /></a>
</div>

{% highlight css %}
-moz-border-radius-topleft / -webkit-border-top-left-radius
-moz-border-radius-topright / -webkit-border-top-right-radius
-moz-border-radius-bottomleft / -webkit-border-bottom-left-radius
-moz-border-radius-bottomright / -webkit-border-bottom-right-radius
{% endhighlight %}

اگر دوست دارید تمام گوشه ها گرد شوند میتوانید از کد زیر استفاده کنید:  

{% highlight css %}
-moz-border-radius: 5px;
-webkit-border-radius: 5px;
border: 1px solid #000;
{% endhighlight %}

**۴.  تصاویر در CSS۳ :**  
یکی از نقص های نسخه قبلی CSS محدودیت کاربر در انتخاب تصاویر پس‌زمینه بود به طوری که شما نمیتوانستید بیش از یک تصویر را به یک div اختصاص دهید ولی در CSS۳ شما میتوانید به تعداد دلخواه تصویر به یک div اضافه کنید. به کدهای زیر دقت کنید:

{% highlight css %}
background: url(body-top.gif) top left no-repeat,
url(banner_fresco.jpg) top 11px no-repeat,
url(body-bottom.gif) bottom left no-repeat,
url(body-middle.gif) left repeat-y;
{% endhighlight %}

همانطور که می‌بینید، ما چهار تصویر به یک div نسبت داده ایم.

**۵.  اضافه کردن سایه به متن ها:**  
۱. شما میتوانید با استفاده از خصوصیت های CSS۳ به متن های خود، سایه نیز اضافه کنید. شاید این یکی از بهترین امکاناتی باشد به در CSS۳ گنجانده شده است.

<div align="center">
  <a href="/asset/legacy/css3-text-shadow.gif"><img alt="Text Shadow in CSS3" src="/asset/legacy/css3-text-shadow.gif" width="445" height="33" /></a>
</div>

برای اعمال خاصیت بالا، میتوانید از کد زیر استفاده کنید:

{% highlight css %}
text-shadow: 2px 2px 2px #000;
{% endhighlight %}

اینها فقط بخشی از خواص جدید CSS۳ هستند. در پست های بعدی، به طور کاملتر به معرفی CSS۳ خواهیم پرداخت. توجه داشته باشید که اکثر مرورگرهای فعلی قادر به اجرای کدهای CSS۳ نیستند و ممکن است هم اکنون نتوانید این کدها را در وبسایت خود به کار ببرید.  
اگر سوالی دارید در قسمت نظرات مطرح نمایید  
موفق و پیروز باشید.