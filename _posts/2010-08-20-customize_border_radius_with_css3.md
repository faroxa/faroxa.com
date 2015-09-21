---
title: شخصی سازی انحنای عناصر در CSS۳ به وسیله قابلیت جدید آن
author: فرهاد عیدی
excerpt: |
  |
    قبلا در اینجا توضیح دادیم که چگونه میتوان گوشه های عناصر را انحنا داد. اما اخیرا قابلیت جدیدی به CSS۳ اضافه شده است که با استفاده از آن میتوانید انحنای هر گوشه را به طور جداگانه و با امکاناتی جدید تعیین کنید.
    از امکانات جدید میتوان به انحنای افقی و عمودی اشاره کرد که با استفاده از آن میتوانید یک بیضی را با استفاده از CSS۳ طراحی کنید. کاری که قبل از این امکان پذیر نبود.
layout: post
redirect_from: /26/
categories:
  - وب و طراحی
tags:
  - CSS3
---
قبلا در [اینجا ][1]توضیح دادیم که چگونه میتوان گوشه های عناصر را انحنا داد. اما اخیرا قابلیت جدیدی به CSS۳ اضافه شده است که با استفاده از آن میتوانید انحنای هر گوشه را به طور جداگانه و با امکاناتی جدید تعیین کنید.  
از امکانات جدید میتوان به انحنای افقی و عمودی اشاره کرد که با استفاده از آن میتوانید یک بیضی را با استفاده از CSS۳ طراحی کنید. کاری که قبل از این امکان پذیر نبود.

<img alt="borders-redius.jpg" src="/asset/legacy/borders-redius.jpg" class="mt-image-center" style="text-align: center; display: block; margin: 0pt auto 20px;" width="560" height="150" />

<!-- more -->

  
در قابلیت جدید CSS۳ برای ایجاد و شخصی سازی میزان انحنای گوشه عناصر کدهای زیر اضافه شده اند:  
`border-bottom-left-radius, border-bottom-right-radius, border-top-left-radius, border-top-right-radius`  
که با شخصی سازی کدهای بالا میتوانید به نتیجه دلخواه خود برسید. برای درک بیشتر به مثال های زیر توجه کنید:  
[<img src="/asset/legacy/border-radius-diagram.png" alt="faroxa - Web2" width="530" height="167" />][2]  
البته اگر مقادیری برای میزان انحنا وارد نکنید، هیچگونه انحنایی نخواهید داشت.  
نیازی به توضیح اضافی نیست و فقط با توجه به کدهای زیر میتوانید به راحتی از کدها استفاده کنید:  
[![faroxa - Web2][3]][3]  
برای ایجاد منحنی های بالا از کدهای زیر استفاده شده است:  
`<br />
#Example_A {<br />
height: ۶۵px;<br />
width:۱۶۰px;<br />
-moz-border-radius-bottomright: ۵۰px;<br />
border-bottom-right-radius: ۵۰px;<br />
}<br />
#Example_B {<br />
height: ۶۵px;<br />
width:۱۶۰px;<br />
-moz-border-radius-bottomright: ۵۰px ۲۵px;<br />
border-bottom-right-radius: ۵۰px ۲۵px;<br />
}<br />
#Example_C {<br />
height: ۶۵px;<br />
width:۱۶۰px;<br />
-moz-border-radius-bottomright: ۲۵px ۵۰px;<br />
border-bottom-right-radius: ۲۵px ۵۰px;<br />
}<br />
#Example_D {<br />
height: ۵em;<br />
width: ۱۲em;<br />
-moz-border-radius: ۱em ۴em ۱em ۴em;<br />
border-radius: ۱em ۴em ۱em ۴em;<br />
}<br />
#Example_E {<br />
height: ۶۵px;<br />
width:۱۶۰px;<br />
-moz-border-radius: ۲۵px ۱۰px / ۱۰px ۲۵px;<br />
border-radius: ۲۵px ۱۰px / ۱۰px ۲۵px;<br />
}<br />
#Example_F {<br />
height: ۷۰px;<br />
width: ۷۰px;<br />
-moz-border-radius: ۳۵px;<br />
border-radius: ۳۵px;<br />
}`  
البته فعلا فقط مرورگرهای Safari و Google Chrome از نسخه ۵ به بعد و Opera ۱۰ از این قابلیت پشتیبانی میکنند و مرورگر فایرفاکس فقط از دستورهایی که با -moz شروع میشوند پشتیبانی میکند. اگر متوجه شده باشید دستورهای مرورگر فایرفاکس کمی با دستورهای استاندارد متفاوت است پس در هنگام پیاده سازی دقت داشته باشید.  
موفق و پیروز باشید.

 [1]: http://www.faroxa.com/archives/css/about_css3_part_1/
 [2]: /asset/legacy/border-radius-diagram.png
 [3]: /asset/legacy/border-radius-diagram-2.png