---
title: Hover کردن عناصر غیر لینک در مرورگر Internet Explorer ۶ در کمتر از یک دقیقه
author: فرهاد عیدی
excerpt: |
  |
    همیشه طراحان وبسایتها از سر و کله زدن با Internet Explorer وحشت دارند مخصوصا اگر نسخه ۶ باشد. IE۶ همیشه یکی از مرورگرهایی است که با وجود استاندارد نبودن، کاربران زیادی در سرتاسر جهان دارد و عمده مشکل آن، عدم نمایش صحیح کدهای CSS و برخی از عناصر می باشد. از مشکلات آن میتوان عدم پشتیبانی از Hover در عناصر غیر لینک، دو برابر کردن برخی فاصله ها و در موارد html هم عدم پشتیبانی از PNG را نام برد.
    در این مطلب خواهید آموخت چگونه با صرف کمتر از یک دقیقه وقت، مشکل Hover نشدن عناصر غیر لینک در Internet Explorer ۶ را برطرف سازید.
layout: post
redirect_from: /19/
categories:
  - وب و طراحی
tags:
  - IE6
  - ترفند
---
همیشه طراحان وبسایتها از سر و کله زدن با Internet Explorer وحشت دارند مخصوصا اگر نسخه ۶ باشد. IE۶ همیشه یکی از مرورگرهایی است که با وجود استاندارد نبودن، کاربران زیادی در سرتاسر جهان دارد و عمده مشکل آن، عدم نمایش صحیح کدهای CSS و برخی از عناصر می باشد. از مشکلات آن میتوان عدم پشتیبانی از Hover در عناصر غیر لینک، دو برابر کردن برخی فاصله ها و در موارد html هم عدم پشتیبانی از PNG را نام برد.  
در این مطلب خواهید آموخت چگونه با صرف کمتر از یک دقیقه وقت، مشکل Hover نشدن عناصر غیر لینک در Internet Explorer ۶ را برطرف سازید.

<!-- more -->

  
**مرحله اول : **ابتدا یک فایل با نام iehover.htc بسازید(برای این کار میتوانید از Notepad کمک بگیرید) سپس کدهای زیر را در آن کپی کنید:

{% highlight html %}
<public:attach event="ondocumentready" onevent="CSSHover()" />
<script>
eval(function(p,a,c,k,e,r){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>۳۵?String.fromCharCode(c+۲۹):c.toString(۳۶))};if(!''.replace(/^/,String)){while(c--)r[e(c)]=k[c]||e(c);k=[function(e){return r[e]}];e=function(){return'\\w+'};c=۱};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('r.R=(۸(){۴ f=/(^|\\s)((([^a]([^ ]+)?)|(a([^#.][^ ]+)+)):(C|D|E))/i,S=/(.*?)\\:(C|D|E)/i,T=/[^:]+:([a-z-]+).*/i,U=/(\\.([a-V-W-]+):[a-z]+)|(:[a-z]+)/۱c,X=/\\.([a-V-W-]*Y(C|D|E))/i,Z=/۱d (۵|۶|۷)/i,۱۰=/۱e/i;۴ g=\'۱f-\';۴ h={p:[],t:{},۱۱:۸(){n(!Z.F(۱g.۱h)&&!۱۰.F(r.۱۲.۱i))u;۴ a=r.۱۲.۱j,l=a.v;w(۴ i=۰;i<l;i++){۳.G(a[i])}},G:۸(a){n(a.H){I{۴ b=a.H,l=b.v;w(۴ i=۰;i<l;i++){۳.G(a.H[i])}}J(۱۳){}}I{۴ c=a.۱k,l=c.v;w(۴ j=۰;j<l;j++){۳.۱۴(c[j],a)}}J(۱۳){}},۱۴:۸(a,b){۴ c=a.۱l;n(f.F(c)){۴ d=a.K.۱m,L=S.۱۵(c)[۱],M=c.N(T,\'Y$۱\'),O=c.N(U,\'.$۲\'+M),o=X.۱۵(O)[۱];۴ e=L+o;n(!۳.t[e]){b.۱۶(L,g+o+\':۱n(R(۳, "\'+M+\'", "\'+o+\'"))\');۳.t[e]=۱۷}b.۱۶(O,d)}},۱۸:۸(a,b,c){۴ d=g+c;n(a.K[d]){a.K[d]=q}n(!a.x)a.x=[];n(!a.x[c]){a.x[c]=۱۷;۴ e=۱۹ P(a,b,c);۳.p.۱o(e)}u b},y:۸(){I{۴ l=۳.p.v;w(۴ i=۰;i<l;i++){۳.p[i].y()}۳.p=[];۳.t={}}J(e){}}};r.Q(\'۱p\',۸(){h.y()});۴ k={۱q:{۹:\'۱r\',m:\'۱s\'},۱t:{۹:\'۱u\',m:\'۱v\'},۱a:{۹:\'۱a\',m:\'۱w\'}};۸ P(a,b,c){۳.A=a;۳.B=b;۴ d=۱۹ ۱x(\'(^|\\\\s)\'+c+\'(\\\\s|$)\',\'g\');۳.۹=۸(){a.o+=\' \'+c};۳.m=۸(){a.o=a.o.N(d,\' \')};a.Q(k[b].۹,۳.۹);a.Q(k[b].m,۳.m)}P.۱y={y:۸(){۳.A.۱b(k[۳.B].۹,۳.۹);۳.A.۱b(k[۳.B].m,۳.m);۳.۹=q;۳.m=q;۳.A=q;۳.B=q}};u ۸(a,b,c){n(a){u h.۱۸(a,b,c)}۱z{h.۱۱()}}})();',۶۲,۹۸,'|||this|var||||function|activator|||||||||||||deactivator|if|className|elements|null|window||callbacks|return|length|for|csshover|unload||node|type|hover|active|focus|test|parseStylesheet|imports|try|catch|style|affected|pseudo|replace|newSelect|CSSHoverElement|attachEvent|CSSHover|REG_AFFECTED|REG_PSEUDO|REG_SELECT|z۰|۹_|REG_CLASS|on|REG_MSIE|REG_COMPAT|init|document|securityException|parseCSSRule|exec|addRule|true|patch|new|onfocus|detachEvent|gi|msie|backcompat|csh|navigator|userAgent|compatMode|styleSheets|rules|selectorText|cssText|expression|push|onbeforeunload|onhover|onmouseenter|onmouseleave|onactive|onmousedown|onmouseup|onblur|RegExp|prototype|else'.split('|'),۰,{}));
</script>
{% endhighlight %}

**مرحله دوم : **
یک فایل با نام iehover.css ساخته و کد زیر را داخل آن قرار دهید:  

{% highlight css %}
body {
	behavior:url("iehover.htc");
}  
{% endhighlight %}

**مرحله سوم:** دو فایل بالا را در سایت خود آپلود کنید.

**مرحله آخر: **کد زیر را بین دو تگ head در قالبتان کپی کنید:  

{% highlight html %}
<head>

<!&#8211;[if lt IE ۷.]>  
<link rel=&#8221;stylesheet&#8221; type=&#8221;text/css&#8221; href=&#8221;iehover.css&#8221; />  
<![endif]&#8211;>

</head>  

{% endhighlight %}

حالا سایت شما آماده است تا به درستی عناصر غیر لینک را به کاربران Internet Explorer ۶ نشان دهد.  
شما میتوانید یک نمونه از کار این کد را در [اینجا ][1]ببینید. همچنین میتوانید سورس این آموزش را از [اینجا ][2]دریافت کنید.  
[لینک توسعه دهنده][3]

یک توصیه: اگر شما یکی از کاربران Internet Explorer ۶ هستید توصیه میکنم همین الان از این مرورگر دست بکشید و سراغ مرورگرهای دیگری همچون firefox , Opera یا &#8230; بروید.

 [1]: http://www.faroxa.com/samples/iehover/
 [2]: http://www.faroxa.com/download/samples/iehover.zip
 [3]: http://www.xs4all.nl/%7Epeterned/csshover.html