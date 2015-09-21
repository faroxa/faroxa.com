---
title: ویرایشگر متن کاملا فارسی CKEditor برای مووبل تایپ ۵
author: فرهاد عیدی
layout: post
redirect_from: /39/
categories:
  - وب و طراحی
tags:
  - مووبل‌تایپ
  - ویرایشگر
---
همانطور که می‌دانید هنوز فارسی‌ساز مووبل تایپ نسخه پنجم ارائه نشده است و بسیاری از کاربران مووبل تایپ نیز با توجه به قابلیت‌های نسخه جدید، مووبل‌تایپ خود را به این نسخه ارتقا داده‌اند و اگرچه مووبل‌تایپ جدید نیاز چندانی به فارسی‌ساز ندارد اما یک ویرایشگر متن فارسی خیلی می‌تواند برای وبلاگ‌نویس‌ها و مدیران وبسایت‌ها مفید باشد. در این مطلب قصد دارم یک ویرایشگر متن کامل به نام CKeditor را به شما معرفی کنم که به طور کامل از زبان شیرین فارسی پشتیبانی می‌کند و میتواند جایگزین مناسبی برای ویرایشگر متن پیشفرض مووبل‌تایپ شما باشد.

<img alt="CKEditor Screenshot" src="/asset/legacy/CKEditor-screenshot.jpg" class="mt-image-center" style="text-align: center; display: block; margin: 0pt auto 20px;" height="369" width="550" />

<!-- more -->

  
آخرین نسخه این پلاگین را می‌توانید از [اینجا ][1]دریافت کرده و با توجه به [این آموزش][2]، روی وبسایت خود نصب کنید. برای فارسی کردن نرم‌افزار هم کافی‌است در داخل فایل mt-config.cgi خود از طریق دو خط زیر، زبان پیشفرض خود را فارسی انتخاب کنید:

{% highlight perl %}
DefaultLanguage fa
DefaultUserLanguage fa 
{% endhighlight %}


توضیحات بیشتر را می‌توانید در [اینجا ][3]مشاهده کرده و اسکرین‌شات‌های ویرایشگر را نیز در [اینجا ][4]ببینید.  
[لینک این پلاگین در وبسایت رسمی مووبل تایپ][5]  
موفق و پیروز باشید.

 [1]: https://github.com/usualoma/ckeditor-for-mt/downloads
 [2]: http://faroxa.com/post/the-ultimate-guide-to-installing-movable-type-plugins/
 [3]: http://tec.toi-planning.net/en/mt/ckeditor
 [4]: http://tec.toi-planning.net/en/mt/ckeditor/screenshot
 [5]: http://plugins.movabletype.org/ckeditor-for-movable-type/