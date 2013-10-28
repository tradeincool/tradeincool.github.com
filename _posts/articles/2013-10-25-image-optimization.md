---
published: 
  - true
  - "true"
layout: article
title: Image Optimization
abstract: Test study on jpeg image optimization
author_twitter: jasonruyle
author: Jason Ruyle
categories: articles
---

## Image Optimization
We are running an ecommerce site that really needs good quality images.  It is running a zoom feature and we want to make sure the images are high quality.  But the original uploaded images are running around 619KB.  That is just way to big for a website.

We've had a lot of success running jpegoptim and so I decided to take a shot at a few settings.

Based off the results below, I think we are probably going with --max-75 (75.jpg).

original image

[http://mishkanyc.trafficincool.com/sites/default/files/tmp/1.jpg](http://mishkanyc.trafficincool.com/sites/default/files/tmp/1.jpg "Image Optimization")

jpegoptim --max=25 2.jpg

> 1000x1366 24bit Exif IPTC Adobe  [OK] 634112 --> 49059 bytes (92.26%), optimized.
[http://mishkanyc.trafficincool.com/sites/default/files/tmp/25.jpg](http://mishkanyc.trafficincool.com/sites/default/files/tmp/25.jpg "Image Optimization")

Size: 49KB


jpegoptim --max=50 2.jpg

> 1000x1366 24bit Exif IPTC Adobe  [OK] 634112 --> 77496 bytes (87.78%), optimized.
[http://mishkanyc.trafficincool.com/sites/default/files/tmp/50.jpg](http://mishkanyc.trafficincool.com/sites/default/files/tmp/50.jpg "Image Optimization")

Size: 77KB


jpegoptim --max=75 2.jpg

> 1000x1366 24bit Exif IPTC JFIF  [OK] 633103 --> 118633 bytes (81.26%), optimized.
[http://mishkanyc.trafficincool.com/sites/default/files/tmp/75.jpg](http://mishkanyc.trafficincool.com/sites/default/files/tmp/75.jpg "Image Optimization")

Size: 118KB


jpegoptim --max=100 2.jpg

> 1000x1366 24bit Exif IPTC Adobe  [OK] 634112 --> 509479 bytes (19.65%), optimized.
[http://mishkanyc.trafficincool.com/sites/default/files/tmp/100.jpg](http://mishkanyc.trafficincool.com/sites/default/files/tmp/100.jpg "Image Optimization")

Size: 509KB


### Original Image
![](http://mishkanyc.trafficincool.com/sites/default/files/tmp/1.jpg)

### Max 75 Image
![](http://mishkanyc.trafficincool.com/sites/default/files/tmp/75.jpg)