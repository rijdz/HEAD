# HEAD

> Sebuah daftar dari semua yang \*dapat\* masuk di dalam `<head>` dari dokumenmu

[![CC0](https://img.shields.io/badge/license-CC0-green.svg?style=flat-square)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Contributors](https://img.shields.io/github/contributors/joshbuchea/head.svg?style=flat-square)](https://github.com/joshbuchea/HEAD/graphs/contributors)

## Table of Contents

- [HEAD](#head)
  - [Table of Contents](#table-of-contents)
  - [Recommended Minimum](#recommended-minimum)
  - [Elements](#elements)
  - [Meta](#meta)
  - [Link](#link)
  - [Icons](#icons)
  - [Social](#social)
    - [Facebook Open Graph](#facebook-open-graph)
    - [Twitter Card](#twitter-card)
    - [Twitter Privacy](#twitter-privacy)
    - [Schema.org](#schemaorg)
    - [Pinterest](#pinterest)
    - [Facebook Instant Articles](#facebook-instant-articles)
    - [OEmbed](#oembed)
  - [Browsers / Platforms](#browsers--platforms)
    - [Apple iOS](#apple-ios)
    - [Google Android](#google-android)
    - [Google Chrome](#google-chrome)
    - [Microsoft Internet Explorer](#microsoft-internet-explorer)
  - [Browsers (Chinese)](#browsers-chinese)
    - [360 Browser](#360-browser)
    - [QQ Mobile Browser](#qq-mobile-browser)
    - [UC Mobile Browser](#uc-mobile-browser)
  - [App Links](#app-links)
  - [Other Resources](#other-resources)
  - [Related Projects](#related-projects)
  - [Other Formats](#other-formats)
  - [Translations](#translations)
  - [Contributing](#contributing)
    - [Guide](#guide)
      - [1. `master`](#1-master)
      - [2. `gh-pages`](#2-gh-pages)
    - [Contributors](#contributors)
  - [Author](#author)
  - [License](#license)

## Recommended Minimum

Di bawah ini adalah elemen-elemen penting dari tiap dokumen web (website/aplikasi):

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  2 meta tags di atas *harus* ada di awal-awal pada <head>
  untuk memastikan konsistensi rendering dokumen yang layak.
  Elemen "head" yang lain harus hadir *setelah* tag-tag tersebut.
 -->
<title>Halaman Judul</title>
```

**[⬆ back to top](#table-of-contents)**

## Elements

Valid `<head>` elemen termasuk `meta`, `link`, `title`, `style`, `script`, `noscript`, and `base`.

Elemen-elemen berikut menyajikan informasi bagaimana sebuah dokumen seharusnya dirasakan (perceived), dan di-render, dengan teknologi web. misalnya. browsers, search engines, bots, dll.

```html
<!--
  Meneteapkan character encoding untuk dokumen ini, sehingga
  semua karakter berada pada format UTF-8 (contohnya emoji)
  di-render secara benar.
-->
<meta charset="utf-8">

<!-- Menentukan Judul Dokumen -->
<title>Halaman Judul</title>

<!-- Menentukan dasar alamat URL untuk semua URL terkait didalam dokumen -->
<base href="https://example.com/page.html">

<!-- Tautan ke file CSS eksternal  -->
<link rel="stylesheet" href="styles.css">

<!-- Digunakan untuk menambahkan in-dokumen CSS -->
<style>
  /* ... */
</style>

<!-- JavaScript & Bukan-JavaScript tags -->
<script src="script.js"></script>
<script>
  // function(s) go here
</script>
<noscript>
  <!-- No JS alternative -->
</noscript>
```

**[⬆ back to top](#table-of-contents)**

## Meta

```html
<!--
  2 meta tags di atas *harus* ada di awal-awal pada <head>
  untuk memastikan konsistensi rendering dokumen yang layak.
  Elemen "head" yang lain harus hadir *setelah* tag-tag tersebut.
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
  Mengizinkan kontrol resources dapat diambil dari sumber yang mana.
  Tempatkan seawal mungkin di <head>, mengingat tag  
  hanya berlaku terhadap resources yang dideklarasikan setelah itu.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Nama dari Aplikasi Web (hanya digunakan jika website digunakan sebagai sebuah app) -->
<meta name="application-name" content="Nama Aplikasi">

<!-- Warna tema untuk Chrome, Firefox OS dan Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Deskripsi singkat dari sebua dokumen (terbatas sampai 150 karakter) -->
<!-- Isian ini *mungkin* dapat digunakan sebagai sebuah bagian hasil mesin pencari (search engine). -->
<meta name="description" content="Sebuah deskripsi dari halaman">

<!-- Mengendalikan tingkah laku dari mesin pencari (search engine) crawling dan indexing -->
<meta name="robots" content="index,follow"><!-- Semua Mesing Pencari(Search Engines) -->
<meta name="googlebot" content="index,follow"><!-- Spesifik Google -->

<!-- Memberitahu Google untuk tidak menunjukan sitelinks kotak pencari -->
<meta name="google" content="nositelinkssearchbox">

<!-- Memberitahu Google untuk tidak memberikan penterjemahan untuk dokumen ini -->
<meta name="google" content="notranslate">

<!-- Memvalidasi kepemilakan website -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Mengidentifikasi software digunakan untuk membangun dokumen (misalnya - WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Deskripsi singkat subyek dari dokumen anda -->
<meta name="subject" content="Subyek dokumen anda">

<!-- Memberikan rating usia umum berdasarkan isi dari dokumen -->
<meta name="rating" content="General">

<!-- Mengizinkan pengendalian melalui bagaimana "referrer information" berlalu -->
<meta name="referrer" content="no-referrer">

<!-- Menonaktifkan deteksi dan pemformatan dari nomor telpon yang mungkin -->
<meta name="format-detection" content="telephone=no">

<!-- Sepenuhnya memilih keluar dari "DNS prefetching" melakukan penyetelan ke- "off" -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Menspesifikan dokumen untuk tampil pada sebuah frame yang spesifik -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Kode negara (ISO 3166-1): wajib, kode negara bagian (ISO 3166-2): optional; conth. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- contoh. content="New York City" -->
```

- 📖 [Meta tag yang dikenali Google](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM pada Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [Geotagging pada Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

**[⬆ back to top](#table-of-contents)**

## Link

```html
<!-- Mengarahkan ke sebuah stylesheet eksternal -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Membantu pencegahan duplikasi isian isu -->
<link rel="canonical" href="https://example.com/article/?page=2">

<!-- Tautan ke sebuah versi AMP HTML dari dokumen terkini -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Tautan ke sebuah JSON file yang menspesifikan "installation" credentials untuk aplikasi web -->
<link rel="manifest" href="manifest.json">

<!-- Tautan ke informasi mengenai penulis dari dokumen -->
<link rel="author" href="humans.txt">

<!-- Mengacu ke sebuah pernyataan hak cipta yang berlaku terhadap konteks tautan -->
<link rel="license" href="copyright.html">

<!-- Memberikan referensi ke sebuah lokasi di dalam dokumen yang mungkin terdapat di bahasa yang lain -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Memberikan informasi tentang seorang penulis atau orang lain -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Tautan ke dokumen yang mendeskripsikan sebuah koleksi catatan, dokumen, atau bahan material lain yang menarik sejarah -->
<link rel="archives" href="https://example.com/archives/">

<!-- Tautan ke top level resource pada sebuah struktur hierarki -->
<link rel="index" href="https://example.com/article/">

<!-- Menyajikan referensi diri - berguna saat dokumen memiliki beberapa referensi yang mungkin -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- Yang pertama, akhir, sebelumnya, and setelahnya dokumen pada sebuah rangkaian dari dokumen, secara berurutan -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Digunakan saat service pihak ketiga digunakan untuk memelihara sebuah blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Formulir sebuah komentar otomatis dimana tautan blog WordPress yang lain ke blog WordPress anda atau post -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Memberi tahu sebuah URL saat anda melakukan link kepadanya pada dokumen anda -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Memungkinkan posting ke domain anda sendiri menggunakan sebuah Micropub client -->
<link rel="micropub" href="https://example.com/micropub">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<!-- Info lebih lanjut: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Link Relations](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ back to top](#table-of-contents)**

## Icons

```html
<!-- Untuk IE 10 dan kebawah -->
<!-- Tempatkan favicon.ico pada direktori root - tidak ada tag yang diperlukan -->

<!-- Icon untuk resolusi tertinggi yang dibutuhkan -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Apple Touch Icon (reuse 192px icon.png) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Safari Pinned Tab Icon -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [Semua tentang Favicons (dan Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Membuat Pinned Tab Icons](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Icons & Browser Colors](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ back to top](#table-of-contents)**

## Social

### Facebook Open Graph

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:image:alt" content="A description of what is in the image (not a caption)">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- 📖 [Open Graph protocol](http://ogp.me/)
- 🛠 Test halaman anda dengan [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<meta name="twitter:image:alt" content="A text description of the image conveying the essential nature of an image to users who are visually impaired. Maximum 420 characters.">
```

- 📖 [Memulai dengan kartu — Twitter Developers](https://dev.twitter.com/cards/getting-started)
- 🛠 Test halaman anda dengan [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Twitter Privacy
Jika anda melakukan embed tweets pada website anda, Twitter dapat menggunkan informasi dari situs anda untuk mengkurasi isi dan rekomendasi untuk pengguna Twitter. [Lebih lanjut tentang Twitter privacy options](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- tidak mengijinkan Twitter dari menggunakan situs anda untuk tujuan personalisasi -->
<meta name="twitter:dnt" content="on">
```

### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Content Title">
      <meta itemprop="description" content="Content description less than 200 characters">
      <meta itemprop="image" content="https://example.com/image.jpg">
```

**Note:** Meta tags berikut diperlukan `itemscope` dan `itemtype` atribut untuk ditambahkan ke `<html>` tag.

- 🛠 Test halaman anda dengan [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)

### Pinterest

Pinterest mengizinkan anda untuk mencegah orang dari menyimpan hal-hal dari website anda, menurut [pusat bantuan mereka](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site). `description` adalah optional.

```html
<meta name="pinterest" content="nopin" description="Maaf, anda tidak dapat menyimpan dari website saya!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- URL versi web dari artikel anda -->
<link rel="canonical" href="https://example.com/article.html">

<!-- Style yang digunakan untuk artikel ini -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Membuat Artikel - Artikel Instan](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Contoh Kode - Artikel Instan](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- 📖 [oEmbed format](https://oembed.com/)

**[⬆ back to top](#table-of-contents)**

## Browsers / Platforms

### Apple iOS

```html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Nonaktifkan deteksi otomatis dan pemformatan nomor telpon yang mungkin -->
<meta name="format-detection" content="telephone=no">

<!-- Launch Icon (180x180px or larger) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Launch Screen Image -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Launch Icon Title -->
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Mengaktifkan standalone (full-screen) mode -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Tampilan Status bar (tidak ada efek kecuali kalo standalone mode diaktifkan) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Mengkonfigurasi Aplikasi Web](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Menambahkan ke home screen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Menonaktifkan prompt penerjamah -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- Memaksa IE 8/9/10 untuk menggunakan rendering engine terakhirnya -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Nonaktifkan deteksi otomatis dan pemformatan nomor telpon yang mungkin dari Skype Toolbar browser extension -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Judul Window -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Kebutuhan minimal xml markup untuk `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

- 📖 [Referensi skema konfigurasi browser](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

**[⬆ back to top](#table-of-contents)**

## Browsers (Chinese)

### 360 Browser

```html
<!-- Memilih urutan rendering engine -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

```html
<!-- Mengunci layar kunci ke orientasi yang spesifik -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Menampilkan dokumen ini ke tampilan fullscreen -->
<meta name="x5-fullscreen" content="true">

<!-- Dokumen akan ditampilkan dalam "application mode" (fullscreen, etc.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

```html
<!-- Mengunci layar kunci ke orientasi yang spesifik -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Menampilkan dokumen ini ke tampilan fullscreen -->
<meta name="full-screen" content="yes">

<!-- UC browser akan menampilkan gambar walaupun pada "text mode" -->
<meta name="imagemode" content="force">

<!-- Dokumen akan ditampilkan pada "application mode"(fullscreen, forbidding gesture, etc.) -->
<meta name="browsermode" content="application">

<!-- Menonaktifkan UC browser's "night mode" untuk dokumen ini -->
<meta name="nightmode" content="disable">

<!-- Menyederhanakan dokumen untuk mengurangi transfer data -->
<meta name="layoutmode" content="fitscreen">

<!-- Menonaktifkan fitur UC browser  "Membesarkan font saat banyak kata pada dokumen ini" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ back to top](#table-of-contents)**

## App Links

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [App Links](https://applinks.org/documentation/)

**[⬆ back to top](#table-of-contents)**

## Other Resources

- 📖 [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ back to top](#table-of-contents)**

## Related Projects

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package untuk `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package untuk `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface untuk `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Memanipulasi informasi meta pada sebuah `HEAD` tag untuk Vue.js

**[⬆ back to top](#table-of-contents)**

## Other Formats

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ back to top](#table-of-contents)**

## Translations

- 🇧🇷 [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [German](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Italian](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japanese](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Korean](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russian/Русский](https://github.com/Konfuze/HEAD)
- 🇪🇸 [Spanish](https://github.com/alvaroadlf/HEAD)
- 🇹🇷 [Turkish/Türkçe](https://github.com/mkg0/HEAD)
- 🇮🇩 [Bahasa](https://github.com/rijdz/HEAD)

**[⬆ back to top](#table-of-contents)**

## Contributing

**Open an issue or a pull request to suggest changes or additions.**

### Guide

The **HEAD** repository terdiri dari 2 cabang:

#### 1. `master`

Cabang ini terdiri dari `README.md` yang terefleksi otomatis ke [htmlhead.dev](https://htmlhead.dev/) website. Semua perubahan pada isian "cheat sheet" dengan demikian seharusnya sudah diarahkan ke file ini.

Mohon mengikuti langkah-langkah berikut untuk pull requests:

- Modifikasi hanya untuk satu tag, atau satu yang berelasi rangkaian dari tag disaat yang bersamaan
- Gunakan double quotes pada atribut
- Jangan memasukan sebuah trailing slash pada self-closing elements — spesifikasi HTML5  mengatakan itu optional
- Pertimbangkan memasukan sebuah tautan ke dokumentasi yang mendukung perubahan anda

#### 2. `gh-pages`

Cabang ini bertanggung jawab [htmlhead.dev](https://htmlhead.dev/) website. Kita menggunakan [Jekyll](https://jekyllrb.com/) untuk deploy `README.md` Markdown melalui [GitHub Pages](https://pages.github.com/). Semua modifikasi terkait website harus diarahkan kesini.

Anda mungkin ingin melalui [Jekyll Docs](https://jekyllrb.com/docs/home/) dan memahami bagaimana kinerja Jekyll sebelum bekerja untuk cabang ini.

### Contributors

Periksa semua super awesome berikut [contributors](https://github.com/joshbuchea/HEAD/graphs/contributors).

## Author

**[Josh](https://twitter.com/joshbuchea)**

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ back to top](#table-of-contents)**
