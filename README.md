# Bazı Önemli SEO Uygulamaları

Bugüne kadar geliştirdiğim web sitelerden öğrendiğim bazı SEO uygulamalarını bu dökümanda bulabilirsiniz.

    Bu uygulamalar zamanla eskimiş veya değiştirilmiş olabilir. Bu uygulamaları yapmadan önce güncelliğini kontrol ediniz ve buna uygun olarak uygulamaları gerçekleştiriniz.

## Meta Etiketleri

Meta etiketler, arama motorlarına web siteleri hakkında bilgi sağlamaları için kullanılır. Kısaca web sitenizin bilgilerini gösterirler. SEO uygulamalarının en önemli konularından biridir ve uygulanması son derece önemlidir.

Meta etiketler, HTML sayfanızın ```<head>``` bölümüne eklenir.

Bazı meta etiketleri;
- ```<meta name="description" content="İçeriğinizi buraya yazabilirsiniz">```: Web sitenizin içeriğini açıkladığınız etikettir.
- ```<meta name="keywords" content="Anahtar kelimelerinizi buraya yazabilirsiniz">```: Web sitenizin anahtar kelimelerini açıkladığınız etikettir.
- ```<meta name="robots" content="index, follow">```: Web sitenizin arama motorları tarafından izlenip izlenmeyeceğini belirten etikettir. Bu etiketin değeri ```index, follow``` olabilir. ```index``` etiketi web sitenizin arama motorları tarafından görüntülenebilir olmasını sağlar. ```follow``` etiketi web sitenizin arama motorları tarafından izlenmesini sağlar. Bu etiketlerin değeri ```noindex, nofollow``` olabilir. ```noindex``` etiketi web sitenizin arama motorları tarafından görüntülenemez olmasını sağlar. ```nofollow``` etiketi web sitenizin arama motorları tarafından izlenmesini sağlamaz.

Daha bir çok meta etiketi bulunmaktadır. Bu etiketlerin bazılarına [buradan](https://gist.github.com/whitingx/3840905) ulaşabilirsiniz.

## Başlık Etiketleri

- Başlık etiketlerinde en az 3 kelime ve en fazla 5 kelime kullanılmalıdır.
- Başlık etiketleri kullanılmazsa hem kullanıcıların hem de arama motorlarının sayfa içeriğinizle ilgili pek bir bilgisi olamayacaktır. Bu yüzden başlık etiketleri kullanmanız önerilir.

Başlık etiketlerinde temelde 2 tane önemli nokta bulunmaktadır.

1. Ana Başlık Etiketinin Önemi

    ```html
    <h1>Ana başlığınız burada olmalı</h1>
    ```

    1. Her bir sayfa için bir ana başlık etiketi zorunludur.
    2. Sayfanın en üstünde yer almalıdır.
    3. Hedeflenen içeriğe uygun başlık metni kullanmalıdır.
    4. **Bir sayfada birden fazla ana başlık etiketi olamaz!**

2. Başlık Etiketlerinin Sıralamaları

    ```html
    <!-- Ana Başlık Etiketi -->
    <h1>Ana başlığınız burada olmalı</h1>

    <!-- Alt Başlık Etiketleri -->
    <h2>Alt başlığınız burada olmalı</h2>
    <h3>Alt başlığınız burada olmalı</h3>
    <h4>Alt başlığınız burada olmalı</h4>
    <h5>Alt başlığınız burada olmalı</h5>
    <h6>Alt başlığınız burada olmalı</h6>
    ```

    1. Ana başlık etiketi öncelikli olmalıdır ve sırayla sıralanmalıdır.
    2. Alt başlık etiketileri, ana başlık etiketinin altında olmalıdır.

## Yinelenen Sayfalar

Her sayfada içeriklerin, meta verilerinin ve en önemlisi her sayfada ```<h1>``` etiketinin farklı metne sahip olması gerek. Eğer bu veriler aynısı ise sayfaları birbirine referans vermelisiniz ya da sayfalarınızın içeriğini değiştirmelisiniz. Bir başka çözüm olarak da sayfalarınızı bir sayfada birleştirebilirsiniz.

## Şemalar

Bir arama yaptıktan sonra ilgili sonuçların altında, yanında ya da üstünde bazı kutular, resimler veya ilişkili linkler görüntülenir. Bunların görüntülenmesindeki en büyük etken, web sitenize eklediğiniz şemalardır.

Bu şemalar sayesinde web sitenizin içeriğini daha fazla görüntüleyebilir ve daha iyi bir görünüm sağlar.

Bu şemaları oluşturmak için 2 yönteminiz vardır. Bunlar;
1. **Microdata**: HTML etiketlerine özellikler eklenerek yapılır. Bu yöntem yerini JSON-LD'ye bırakmaya başlamıştır.

```html
<html>
    <head>
        <title>Microdata Schema Example</title>
    </head>
    <body>
        <div itemscope itemtype="https://schema.org/Question">
            <h1 itemprop="name">What is attr_accessor in Ruby?</h1>
            <div itemprop="upvoteCount">196</div>
            <div itemprop="text">I am having difficulty understanding Ruby attr_accessors, can someone explain them?</div>
            <div>asked <time itemprop="dateCreated" datetime="2010-11-04T20:07Z">Nov 11 '10 at 20:07</time></div>
            <div itemprop="author" itemscope itemtype="https://schema.org/Person"><span itemprop="name">someuser</span></div>
            <div><span itemprop="answerCount">4</span> answers</div>
            <div itemprop="suggestedAnswer acceptedAnswer" itemscope itemtype="https://schema.org/Answer">
                <div itemprop="upvoteCount">1337</div>
                <div itemprop="text">
                (The text of the accepted answer goes here...).
                </div>
                <div>answered <time itemprop="dateCreated" datetime="2010-12-01T22:01Z">Dec 1 '10 at 22:01</time></div>
                <div itemprop="author" itemscope itemtype="https://schema.org/Person"><span itemprop="name">anotheruser</span></div>
            </div>
            <div itemprop="suggestedAnswer" itemscope itemtype="https://schema.org/Answer">
                <div itemprop="upvoteCount">39</div>
                <div itemprop="text">
                (Another explanation would go here).
                </div>
                <div>answered <time itemprop="dateCreated" datetime="2010-12-06T21:11Z">Dec 6 '10 at 21:11</time></div>
                <div itemprop="author" itemscope itemtype="https://schema.org/Person"><span itemprop="name">lonelyuser1234</span></div>
            </div>
        </div>
    </body>
</html>
```

2. **JSON-LD**: JSON formatında verilerinizi oluşturarak yapılır. Oluşturduğunuz JSON verinizi ```<script type="application/ld+json"></script>``` etiketinin içerisine yazarak web sitenizdeki ```<head></head>``` etiketleri arasına ekleyebilirsiniz.

    ```html
    <html>
        <head>
            <title>JSON-LD Schema Example</title>
            <script type='application/ld+json'>
                {
                    "@context": "http://www.schema.org",
                    "@type": "Organization",
                    "name": "NAME OF YOUR WEBSITE",
                    "legalName" : "LEGAL NAME OF YOUR WEBSITE",
                    "url": "DOMAIN",
                    "description":  "DESCRIPTION OF YOUR WEBSITE",
                    "logo": "LOGO URL",
                }
            </script>
        </head>
        <body>
            ...
        </body>
    </html>
    ```

Bu şemaları [schema.org](https://schema.org) adresini kullanarak geliştirebilirsiniz.

Bazı şema örnekleri;
- [Organization](https://schema.org/Organization)
- [Product](https://schema.org/Product)
- [Article](https://schema.org/Article)
- [Question](https://schema.org/Question)
- [BreadcrumbList](https://schema.org/BreadcrumbList)
- [SearchAction](https://schema.org/SearchAction)

## Google Pagespeed Insights

Web sitemizin hızlı açılması hem kullanıcı deneyimi hem de arama motorları tarafından daha iyi bir izlenim vermek için çok önemlidir. Kimse 10 saniyede açılan bir web sitesine girmek istemez. Bunun için web site hızlandırma çalışması yapılması gerekir. Bu çalışmayı yapmak için rapora ihtiyacımız vardır ve Google Pagespeed Insights bu raporu sizin için oluşturacaktır. Bu raporda en önemlisi skorlardır. Skorunuzu mobil ve masaüstü olarak 100 değerine yaklaştırmaya çalışın. 100 değerine ne kadar yakın olursa o kadar iyi olacaktır.

Verilen bu raporda hatalarınızı görebilir ve hatalarınızı önerilere göre çözebilirsiniz.

Bunun için [Google Pagespeed Insights](https://pagespeed.web.dev/) sayfasını kullanabilirsiniz.

## Resimlerin Alt Özelliği

Her resim etiketinin alt özelliği vardır ve bu özellik içerisine, resmin açıklamasını yazmanız gerekir. Bu açıklamalar resmin içeriğini açıklar şekilde olmalıdır.

Bu alt özelliğindeki yazıyı web site üzerinde göremezsiniz. Buraya yazılan metinler erişilebilirlik için çok önemlidir. Bu alt özellikler arama motorları için de önemlidir ancak en önemlisi görme engelli kişiler içindir. Buraya yazdığınız metinler, görme engelli kişilerin orada ne olduğunu anlamalarına olanak sağlar. Bunu da kullandıkları cihazlar tarafından metinleri sese dönüştürerek yaparlar.

Bu özelliği kullanmak için, resimlerin alt özelliğini girmeniz gerekir.

```html
<img src="https://www.yourdomain.com/assets/img/home/persons.jpg" alt="Biri kadın biri erkek olmak üzere iki insan, deniz kenarındaki restoranda, kahverengi ve üstünde beyaz bir örtü olan masada karşılıklı oturmaktadır.">
```

## AJAX Sayfalamasının Kullanım Sonucu Ortaya Çıkan Sorun

Eğer sayfasınızda, sayfalama varsa ve siz sayfalamanızı AJAX ile yapıyorsanız, muhtemelen sonradan yüklenen içerikler arama motorları tarafından görülemeyecektir.

Bu durumda sayfalamanızı AJAX ile değil bir link yapısı ile yapmanız önerilir.

    https://www.yourdomain.com/list/page/1
    https://www.yourdomain.com/list/page/2
    https://www.yourdomain.com/list/page/3

veya

    https://www.yourdomain.com/list?page=1
    https://www.yourdomain.com/list?page=2
    https://www.yourdomain.com/list?page=3

Bu link güncellemesini yaptıktan sonra sayfalarınza meta etiketler eklemeniz gerekmektedir. Bu etiketler sayesinde önceki sayfa veya sonraki sayfanızı arama motoruna tanıtmış olursunuz.

Sayfa 2'de olduğunuzu düşünürsek meta etiketlerinizi şu şekilde oluşturmalısınız.
```html
<link rel="prev" href="https://www.yourdomain.com/list/page/1" />
<link rel="next" href="https://www.yourdomain.com/list/page/3" />

<!-- VEYA -->
<link rel="prev" href="https://www.yourdomain.com/list?page=1" />
<link rel="next" href="https://www.yourdomain.com/list?page=3" />
```

Detaylı bilgiye ulaşmak için [bu](https://developers.google.com/search/blog/2011/09/pagination-with-relnext-and-relprev) sayfayı kullanabilirsiniz.

## Sitemap.xml Dosyası

Sitemap arama motoru botları ve tarayıcılar özelinde web sitelerinin daha iyi anlaşılması ve sayfaların dizine eklenmesi için oluşturulmuş sayfalardır.

Sitemap ile içeriğinizi arama motorlarına daha hızlı tanıtabilirsiniz ve daha hızlı indexlenmesine yardımcı olabilirsiniz. Yani hem sizin hem arama motorlarının işini kolaylaştırmış olursunuz.

Bu sayfalarınızı oluşturmak için ```https://www.yourdomain.com/sitemap.xml``` dosyasını oluşturmanız gerekir. Bu dosya XML formatında olmalıdır. Oluşturduğunuz bu dosyayı ```https://www.yourdomain.com/robots.txt``` dosyasında tanımlamanız gerekir.

Örnek sitemap.xml dosyanız şu şekilde olmalıdır.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9" xmlns:xhtml="http://www.w3.org/1999/xhtml">
	<url>
		<loc>https://www.yourdomain.com</loc>
        <lastmod>2022-07-16</lastmod>
        <changefreq>Daily</changefreq>
        <priority>1</priority>
	</url>
	<url>
        <loc>https://www.yourdomain.com/about</loc>
        <lastmod>2022-07-16</lastmod>
        <changefreq>Daily</changefreq>
        <priority>0.95</priority>
    </url>
</urlset>
```

Detaylı bilgiye ulaşmak için [bu](https://developers.google.com/search/docs/advanced/sitemaps/build-sitemap) sayfayı kullanabilirsiniz.

## Robots.txt Dosyası

Robots.txt dosyası, arama motoru tarayıcılarına sitenizdeki hangi URL'lere erişebileceklerini bildirir. Bu yöntem çoğunlukla isteklerin sitenizde yoğunluğa yol açmasını engellemek için kullanılır. Her arama motoru için farklı tanımlamalar vardır.

Örnek sitemap.xml dosyanız şu şekilde olmalıdır.

```txt
User-agent: Googlebot
Disallow: /

User-agent: Googlebot
User-agent: AdsBot-Google
Disallow: /

User-agent: *
Disallow: /

Allow: /

Sitemap: https://www.yourdomain.com/sitemap.xml
Sitemap: https://www.yourdomain.com/en/sitemap.xml
Sitemap: https://www.yourdomain.com/fr/sitemap.xml
```


Detaylı bilgiye ulaşmak için [bu](https://developers.google.com/search/docs/advanced/robots/intro) sayfayı kullanabilirsiniz.

## SSL

Genellikle web sitemizin güvenli olup olmadığı SSL sayesinde kontrol edilir. Eğer bir web sitesinde SSL varsa arama motorları bu web siteyi güvenli olarak işaretler ve arama sonuçlarından üst sıralara çıkmasını sağlar. Bu yüzden hem kullancıların hem de arama motorlarının güvenini kazanmak için SSL kullanmanız önerilir.

Bir websitesinde SSL olup olmadığını genellikle tarayıcı üzerindeki linkin yazıldığı barın sol tarafındaki kilit simgesinden anlarız. Eğer o kilit simgesi yeşil ise SSL kullanılmış demektir. SSL detayına erişmek için o kilit simgesine tıklayabilirsiniz.

## Kırık Linklerin Yönetilmesi

Bu kırık linkler genellikle içerik başlığının değişmesi sonucu linkin değişmesiyle ortaya çıkar. Eğer bir sayfa linki güncellendiyse, eski linki linke yönlendirmelisiniz. Bu sayede kullanıcıların kaybolmasının önüne geçilir.

Bu yönlendirme yapılırken temelde 2 yöntem vardır;

1. **301 Kalıcı Yönlendirme (Moved Permanently)**: Bu yöntem, eski linkin tamamen kaldırıldığı ve artık kullanılmadığı durumlarda kullanılır.
2. **302 Geçici Yönlendirme (Temporary Redirect)**: Bu yöntem ise eski linkin geçici bir süre için kaldırıldığında ve tekrar yeniden açılacağı durumlarda kullanılır.