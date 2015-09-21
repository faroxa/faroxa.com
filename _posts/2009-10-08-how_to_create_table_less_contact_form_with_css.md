---
title: ساخت فرم تماس کاملا فارسی با استفاده از CSS و بدون به کار بردن Table
author: فرهاد عیدی
layout: post
redirect_from: /16/
categories:
  - وب و طراحی
---
کسانی که با استفاده از جدول (Table) به طراحی سایت میپردازند، هنوز باور ندارند که همه امکانات جدول در طراحی با CSS نیز میتوانند اجرا شوند. در انجمن های مختلفی که در رابطه با طراحی در آنها بحث میشوند یکی از دلایل استفاده نکردن از CSS را نحوه جایگیری عناصر می‌نامند و در اکثر مواقع نیز طراحی یک فرم تماس را مثال میزنند. آنها میگویند وقتی یک فرم تماس را با استفاده از CSS طراحی میکنند، نظم عناصر به هم ریخته و فرم ها درست بعد از نوشته قرار میگیرند که ظاهر خوبی به فرم طراحی شده نمیدهد.  
اما در این مطلب قصد دارم روشی را آموزش دهم که تمامی عناصر به یک اندازه و به طور کاملا منظم در کنار یکدیگر قرار خواهند گرفت. برای مشاهده نمونه کار روی [این لینک ][1]کلیک کنید.

<!-- more -->


<img class="mt-image-center" style="text-align: center; display: block; margin: 0pt auto 20px;" alt="ساخت فرم تماس با استفاده از CSS" src="/asset/legacy/create-table-less-contact-form-with-css.jpg" width="560" height="150" />

شروع آموزش:  
۱. ابتدا باید یک فایل html بسازید. برای این کار میتوانید یک پرونده با Notpad ایجاد کنید.  
۲. کدهای زیر را داخل آن کپی کنید:  

{% highlight html %}
<!DOCTYPE html PUBLIC "-//W۳C//DTD XHTML ۱.۰ Transitional//EN" "http://www.w۳.org/TR/xhtml۱/DTD/xhtml۱-transitional.dtd">
<html xmlns="http://www.w۳.org/۱۹۹۹/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-۸" />
<title>نمونه فرم تماس</title>
<style type="text/css">
body {
background: #fff;
margin: ۰ auto;
padding: ۰;
}
.contact {
width: ۴۰۰px;
direction: rtl;
text-align: right;
font: normal ۱۱px Tahoma, Geneva, sans-serif;
}
.contact h۲ {
font: bold ۱۱px tahoma;
padding: ۸px ۲px;
border-bottom: ۱px solid #CCC;
}
.contact label {
width: ۱۲۰px;
float: right;
margin: ۵px ۰ ۰ ۰;
}
.contact .form, .contact .form-ltr {
width: ۲۰۰px;
float: right;
padding: ۲px;
font: normal ۱۱px Tahoma, Geneva, sans-serif;
margin: ۵px ۰;
}
.contact .form-ltr {
direction: ltr;
text-align: left;
}
.contact .text {
width: ۲۵۰px;
height: ۱۰۰px;
overflow: auto;
font: normal ۱۱px/۱.۴ Tahoma, Geneva, sans-serif;
}
.contact .btn {
font: normal ۱۱px Tahoma, Geneva, sans-serif;
margin: ۵px ۰;
}
</style>
</head>
<body>
<div align="center"></p>
<p><div style="background:#۱۱۱; padding: ۶px;"><a style="color:
#fff; text-decoration: none;" href="#">Powered by
faroxa</a></div>
<div class="contact">
<h۲>پیام خود را ارسال نمایید</h۲>
<form method="post" action="">
<label for="name"> نام شما : </label>
<input type="text" value="" class="form" />
<br  />
<label for="Email"> پست الکترونیکی : </label>
<input type="text" class="form-ltr" value="" />

<label for="subject"> موضوع : </label>
<input type="text" value="" class="form" />

<label for="text"> متن پیام : </label>
<textarea class="text"></textarea>

<label>&nbsp;</label>
<input type="submit" value="ارسال" name="submit" class="btn" />
<input type="reset" value="دوباره" name="reset" class="btn" />
</form>
</div><!--Contact-->
</div><!--Center-->
</body>
</html>
{% endhighlight %}


۳. پرونده را با نام contact.html ذخیره کنید.  
کار ساخت فرم تماس تمام شد و میماند مختصر توضیحی درباره کدهای بالا:  

{% highlight html %}


<div class="contact">
<h۲>پیام خود را ارسال نمایید</h۲>
<form method="post" action="">
<label for="name"> نام شما : </label>
<input type="text" value="" class="form" />
<br  />
<label for="Email"> پست الکترونیکی : </label>
<input type="text" class="form-ltr" value="" />

<label for="subject"> موضوع : </label>
<input type="text" value="" class="form" />

<label for="text"> متن پیام : </label>
<textarea class="text"></textarea>

<label>&nbsp;</label>
<input type="submit" value="ارسال" name="submit" class="btn" />
<input type="reset" value="دوباره" name="reset" class="btn" />
</form>
</div><!--Contact-->
{% endhighlight %}

توسط کد بالا ما یک فرم ساده html تولید کردیم که با استفاده از CSS سبک دهی  
شده اند. همانطور که میبینید در هیچ جای کد از واژه Table استفاده نشده  
است.  
اما میرویم سراغ قسمت اصلی یعنی همان کدهای CSS . این کدها برای  
سبک دهی فرم ما هستند که هم میتوانند در فایل html جاسازی شوند هم  
میتوانند در یک فایل جداگانه قرار گرفته و آدرس آنها را در فایل html وارد  
کنیم.  
از قسمت اول کدها شروع میکنیم: 

{% highlight css %}
body {
	background: #fff;
	margin: ۰ auto;
	padding: ۰;
}
{% endhighlight %} 

در این قسمت، خصوصیات کلی صفحه را ایجاد کردیم که شامل رنگ صفحه و فاصله صفحه از کناره هاست.  

{% highlight css %}
.contact {
	width: ۴۰۰px;
	direction: rtl;
	text-align: right;
	font: normal ۱۱px Tahoma, Geneva, sans-serif;
}
{% endhighlight %} 
در  
این قسمت، خواص کلی فرم از جمله اندازه، نوع قلم و نوع چینش فرم را تعیین  
کردیم یعنی فرم ما قرار است در یک div با خصوصیات بالا ایجاد شود.  

{% highlight css %}
.contact h۲ {
font: bold ۱۱px tahoma;
padding: ۸px ۲px;
border-bottom: ۱px solid #CCC;
}کد بالا، عنوان فرم را سبک دهی میکند.  
.contact label {
width: ۱۲۰px;
float: right;
margin: ۵px ۰ ۰ ۰;
}
{% endhighlight %} 

کد بالا، اندازه برچسب ها را مشخص میکند. به عنوان مثال عبارت &#8220;نام شما&#8221; که  
در فرم به کار رفته است، برچسبی برای فرم &#8220;نام شما&#8221; است. اگر خصوصیات بالا  
را اعمال نکنیم، فرم ما از این نظم بیرون آمده و فرم ها به برچسب ها  
میچسبند که ظاهر خوبی به طراحی ما نخواهد داد.  

{% highlight css %}
.contact .form, .contact .form-ltr {
width: ۲۰۰px;
float: right;
padding: ۲px;
font: normal ۱۱px Tahoma, Geneva, sans-serif;
margin: ۵px ۰;
}
.contact .form-ltr {
direction: ltr;
text-align: left;
}
.contact .text {
width: ۲۵۰px;
height: ۱۰۰px;
overflow: auto;
font: normal ۱۱px/۱.۴ Tahoma, Geneva, sans-serif;
}
.contact .btn {
font: normal ۱۱px Tahoma, Geneva, sans-serif;
margin: ۵px ۰;
}
{% endhighlight %} 

کدهای بالا هم برای سبکدهی و قالب بندی فرم های موجود به کار میروند. اگر کدهای  
بالا را حذف کنید، مرورگرها تنظیمات دلخواهشان را روی فرم شما پیاده  
خواهند کرد که کمی با زبان فارسی مشکل دارند.

شما میتوانید فرمهای دلخواهتان را با استفاده از نمونه بالا ایجاد کرده و سبک دهی کنید.  
شما میتوانید نمونه این فرم را در [این صفحه ][1]ببینید.  
موفق و پیروز باشید.

 [1]: http://www.faroxa.com/samples/contact.html