---
title: ساخت پادکست و پخش کننده فایلهای صوتی در مووبل تایپ
author: فرهاد عیدی
layout: post
redirect_from: /12/
categories:
  - وب و طراحی
tags:
  - مووبل‌تایپ
---
امروزه با گسترش وب۲ و ارتباطات، وبلاگنویسان اقدام به تولید و انتشار پادکست میکنند. اخیرا پلاگینی در رابطه با همین موضوع در وبسایت رسمی [مووبل تایپ][1] منتشر شده است که قرار دادن فایل های صوتی را در وبلاگ، فوق العاده راحت میکند.

<img class="mt-image-center" style="text-align: center; display: block; margin: 0pt auto 20px;" alt="ساخت پادکست با مووبل تایپ" src="/asset/legacy/create-podcast-with-movable-type.jpg" width="560" height="150" />طریقه نصب:  
۱. ابتدا فایل مورد نظر را از [این آدرس][2] دریافت کنید.  
۲. سپس با نرم افزارهایی مانند Winrar و Winzip آن را از حالت فشرده خارج نمایید.  
۳. در داخل پوشه اکسترکت شده، سه پوشه مشاهده میشود که طبق دستورالعمل زیر آنها را در جای مناسب خود آپلود نمایید:  
**پوشه mt-static **: محتویات این پوشه را باید در روت وبلاگ و در پوشه mt-static آپلود نمایید. به عنوان مثال در پوشه Public_html/mt-static  
**پوشه PHP : **محتویات این پوشه را باید در پوشه php واقع در مسیر نصب مووبل تایپ آپلود کنید. به عنوام مثال:  

{% highlight perl %}
/home/user/public_html/cgi-bin/mt/php/
{% endhighlight %}

**پوشه Plugins :** محتویات این پوشه را نیز باید در پوشه Plugins واقع در مسیر نصب مووبل تایپ آپلود نمایید. به عنوان مثال:  

{% highlight perl %}
/home/user/public_html/cgi-bin/mt/plugins/
{% endhighlight %}

۴. حالا وارد محیط مدیریت مووبل تایپ شوید. اگر مراحل بالا را به درستی انجام داده باشید، صفحه ای نمایان خواهد شد که از شما میخواهد مووبل‌تایپ خود را ارتقا دهید. شما تایید کرده و پس از اتمام کار وارد محیط مدیریت خواهید شد.  
خب مراحل نصب به پایان رسید. حالا مانند تصویر زیر، در منوی Creat یک گزینه به اسم Podcast Asset نمایان خواهد شد.

<div align="center">
  <img alt="Creat podcast with MovableType" src="/asset/legacy/podcast_01.jpg" />
</div>

حالا با کلیک بر روی گزینه Podcast Asset یک صفحه جدید برای شما باز میشود که از شما لینک فایل صوتی را میخواهد. شما لینک را وارد کرده و گزینه Continue را میزنید. یک سری مشخصات دیگر را که دلبخواهی میباشد را پر میکنید و حالا پادکست شما آماده است.

<div align="center">
  <img alt="Creat podcast with MovableType" src="/asset/legacy/podcast_02.jpg" />
</div>

موفق و پیروز باشید.

 [1]: http://www.movabletype.org/
 [2]: http://www.majordojo.com/projects/movable-type/podcasting/