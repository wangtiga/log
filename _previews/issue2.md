---
layout: page
title: issue2
---

## 关于 html 的页面标题

html 中生成了重复的 title 标签,
因为  seo  插件也会生成 title 标签 。

是否可以直接去掉 `_includes/head.html` 文件中定义的 title 标签呢？



- before

```html
<!doctype html>

<html>
	
  <head>
  <title>Home</title>
  
  <meta charset="utf-8" />
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no"/>
  
  <link type="application/atom+xml" rel="alternate" href="http://0.0.0.0:4000/log/feed.xml" title="Log" />
  <!-- Begin Jekyll SEO tag v2.7.1 -->
<title>Home | Log</title>
<meta name="generator" content="Jekyll v4.2.0" />
<meta property="og:title" content="Home" />
<meta property="og:locale" content="en_US" />
<meta name="description" content="Log your life" />
<meta property="og:description" content="Log your life" />
<link rel="canonical" href="http://0.0.0.0:4000/log/" />
<meta property="og:url" content="http://0.0.0.0:4000/log/" />
<meta property="og:site_name" content="Log" />
<meta name="twitter:card" content="summary" />
<meta property="twitter:title" content="Home" />
<script type="application/ld+json">
{"@type":"WebSite","headline":"Home","url":"http://0.0.0.0:4000/log/","description":"Log your life","name":"Log","@context":"https://schema.org"}</script>
<!-- End Jekyll SEO tag -->


  <link rel="shortcut icon" href="/log/favicon.ico" />
  
  <link rel="stylesheet" href="/log/assets/css/log.css" />
  
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.13/css/all.min.css" />
  
  
  
    
  
</head>

  <body>
  </body>
  
</html>
```

- diff

```diff
--- a/_includes/head.html
+++ b/_includes/head.html
@@ -1,12 +1,12 @@
 <head>
-  <title>{{ page.title }}</title>
+
+  {% seo %}
   
   <meta charset="utf-8" />
   
   <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no"/>
   
   {% feed_meta %}
-  {% seo %}
 
   <link rel="shortcut icon" href="{{ site.baseurl }}/favicon.ico" />
   
```

- after

```html
<!doctype html>

<html>
	
  <head>

  <!-- Begin Jekyll SEO tag v2.7.1 -->
<title>Home | Log</title>
<meta name="generator" content="Jekyll v4.2.0" />
<meta property="og:title" content="Home" />
<meta property="og:locale" content="en_US" />
<meta name="description" content="Log your life" />
<meta property="og:description" content="Log your life" />
<link rel="canonical" href="http://0.0.0.0:4000/log/" />
<meta property="og:url" content="http://0.0.0.0:4000/log/" />
<meta property="og:site_name" content="Log" />
<meta name="twitter:card" content="summary" />
<meta property="twitter:title" content="Home" />
<script type="application/ld+json">
{"@type":"WebSite","headline":"Home","url":"http://0.0.0.0:4000/log/","description":"Log your life","name":"Log","@context":"https://schema.org"}</script>
<!-- End Jekyll SEO tag -->

  
  <meta charset="utf-8" />
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no"/>
  
  <link type="application/atom+xml" rel="alternate" href="http://0.0.0.0:4000/log/feed.xml" title="Log" />

  <link rel="shortcut icon" href="/log/favicon.ico" />
  
  <link rel="stylesheet" href="/log/assets/css/log.css" />
  
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.13/css/all.min.css" />
  
  
</head>

  <body>
  </body>
  
</html>
```
