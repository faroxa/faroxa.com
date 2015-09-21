---
title: ساخت نسخه قابل چاپ از مطالب سایت
author: فرهاد عیدی
layout: post
redirect_from: /7/
categories:
  - وب و طراحی
tags:
  - مووبل‌تایپ
---
سایت هایی که قصد پیشرفت دارند حتما باید یک نسخه قابل چاپ از مطالب خود داشته باشند تا بیننده مشکلی برای چاپ مطالب نداشته باشد. برای این کار شما باید یک صفحه آرشیو مخصوص برای نسخه قابل پرینت مطالب داشته باشید. کدهایی که در این مبحث قرار خواهم داد، برای سیستم مووبل تایپ است ولی شما با کمی تغییر میتوانید آن را برای سیستم های دیگر نیز آماده کنید.

<!-- more -->

  
خب شروع میکنیم:

۱. وارد قسمت مدیریت مووبل تایپ (داشبورد) شوید.  
۲. از منوی &#8220;طراحی (Design)&#8221; وارد قسمت &#8220;قالب ها (Templates)&#8221; شوید.

<div align="center">
  <img alt="How To Creat Print Archive" src="/asset/legacy/print_archive_01.jpg" />
</div>

۳. در منوی کناری، وارد قسمت &#8220;قالب های بایگانی (Archive Templates)&#8221; شوید.

<div align="center">
  <img alt="How To Creat Print Archive" src="/asset/legacy/print_archive_02.jpg" />
</div>

۴. حالا روی ساخت یک قالب آرشیو تکی(Entry) کلیک کنید.

<div align="center">
  <img alt="How To Creat Print Archive" src="/asset/legacy/print_archive_03.jpg" />
</div>

۵. در صفحه جدید، نام قالب را Print Archive گذاشته و کد زیر را در قسمت بدنه قالب وارد کنید:  
{% highlight html %}
<!DOCTYPE html PUBLIC &#8220;-//W۳C//DTD XHTML ۱.۰ Transitional//EN&#8221; &#8220;http://www.w۳.org/TR/xhtml۱/DTD/xhtml۱-transitional.dtd&#8221;>  
<html xmlns=&#8221;http://www.w۳.org/۱۹۹۹/xhtml&#8221;>  
<head>  
<meta content=&#8221;text/html; charset=utf-۸&#8221; http-equiv=&#8221;Content-Type&#8221; />  
<title>پرینت <$MTEntryTitle$> &#8211; <$MTBlogName$></title>  
<meta name=&#8221;Robots&#8221; content=&#8221;noindex, nofollow&#8221;>  
<style type=&#8221;text/css&#8221;>  
body {  
background: #fff;  
}  
.wrapper {  
direction: rtl;  
text-align: right;  
font: normal ۱۳px tahoma;  
line-height: ۱.۶;  
border: ۱px solid #۰۰۰;  
width: ۸۰%;  
padding: ۱۵px;  
}  
h۲{  
font: bold ۱۲px tahoma;  
border-bottom: ۱px dotted black;  
padding: ۵px;  
}  
.footer {  
font-size: ۱۱px;  
line-height: ۱.۲;  
}  
</style>  
</head>  
<body>  
<div align=&#8221;center&#8221;>  
<p style=&#8221;font:bold ۱۸px arial;&#8221;><$MTBlogName$> &#8211; <$MTBlogDescription$></p>  
<div class=&#8221;wrapper&#8221;>  
<h۲><$MTEntryTitle$></h۲>  
<$MTEntryBody$><br /><$MTEntryMore$>  
<div style=&#8221;clear:both; border-bottom:۱px solid #۰۰۰; padding: ۵px;&#8221;></div>  
<div class=&#8221;footer&#8221;>  
<p>ارسال شده در تاریخ <$MTEntryDate format=&#8221;%d %b %Y&#8221;$> در وبسایت <$MTBlogURL$></p>  
<p>لینک کامل منبع: <span style=&#8221;direction:ltr;&#8221;><$MTEntryPermaLink$></span></p>  
<p><a href=&#8221;#Print&#8221; onclick=&#8221;window.print(); return false;&#8221;>چاپ این صفحه</a></p>  
</div>  
</div>  
</div>  
</body>  
</html>
{% endhighlight %}

<div align="center">
  <img alt="How To Creat Print Archive" src="/asset/legacy/print_archive_04.jpg" />
</div>

۶. حالا صفحه را Save کرده و منتظر بمانید تا دوباره صفحه فراخوانی شود. در فراخوانی مجدد، گزینه های دیگری به صفحه اضافه میشوند که به شما اجازه ساختن فرمت آرشیو را میدهند. وقتی صفحه به طور کامل Save شده و فراخوانی مجدد گردید، در زیر بدنه کدها، روی گزینه &#8220;گزینه های قالب  
(Template Option)&#8221; کلیک کنید تا فیلدها نمایان شوند.  
۷. روی &#8220;ساخت نقشه کشی بایگانی (Create Archive Mapping)&#8221; کلیک کنید و پس از آن در قسمت جدید گزینه &#8220;اضافه کردن (add)&#8221; کلیک کنید.

<div align="center">
  <img alt="How To Creat Print Archive" src="/asset/legacy/print_archive_05.jpg" />
</div>

۸. حالا در قسمت &#8220;مسیر (Path)&#8221; عبارت زیر را وارد کرده و صفحه را Save کنید:  

{% highlight perl %}
print/<$MTEntryID$>/index.html
{% endhighlight %}

<div align="center">
  <img alt="How To Creat Print Archive" src="/asset/legacy/print_archive_06.jpg" />
</div>

۹. کار ساخت آرشیو تمام شد. حالا کد زیر را در هرجایی که میخواهید به صفحه پرینت لینک دهید قرار میدهید:  

{% highlight perl %}
<a href="<$MTBlogArchiveURL$>print/<$MTEntryID$>/" title="نسخه<br />
{% endhighlight %}

قابل چاپ این مطلب" target="_blank">نسخه قابل چاپ</a>` توجه داشته باشید که کد بالا را باید بین دو کد زیر کپی کنید: 

{% highlight perl %} 
<MTEntries>


</MTEntries>
{% endhighlight %}

موفق و پیروز باشید