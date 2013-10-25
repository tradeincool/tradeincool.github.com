---
published: 
  - true
  - "false"
layout: article
title: Image Optimization
abstract: Test study on jpeg image optimization
author_twitter: jasonruyle
author: Jason Ruyle
categories: articles
---

## Image Optimization

original image
http://mishkanyc.trafficincool.com/sites/default/files/tmp/1.jpg

jpegoptim --max=25 2.jpg
2.jpg 1000x1366 24bit Exif IPTC Adobe  [OK] 634112 --> 49059 bytes (92.26%), optimized.
http://mishkanyc.trafficincool.com/sites/default/files/tmp/25.jpg

jpegoptim --max=50 2.jpg
2.jpg 1000x1366 24bit Exif IPTC Adobe  [OK] 634112 --> 77496 bytes (87.78%), optimized.
http://mishkanyc.trafficincool.com/sites/default/files/tmp/50.jpg

jpegoptim --max=75 2.jpg
2.jpg 1000x1366 24bit Exif IPTC JFIF  [OK] 633103 --> 118633 bytes (81.26%), optimized.
http://mishkanyc.trafficincool.com/sites/default/files/tmp/75.jpg

jpegoptim --max=100 2.jpg
2.jpg 1000x1366 24bit Exif IPTC Adobe  [OK] 634112 --> 509479 bytes (19.65%), optimized.
http://mishkanyc.trafficincool.com/sites/default/files/tmp/100.jpg