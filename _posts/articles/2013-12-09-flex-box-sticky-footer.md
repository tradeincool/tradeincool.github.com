---
published: 
  - true
  - "true"
layout: article
title: Sticky by Flexbox
abstract: Sticky footer using flexbox css
author_twitter: jasonruyle
author: Jason Ruyle
categories: articles
---

## Sticky Footer

We are Trade in Cool are always looking for easier ways to put in common website features.  We have updated our sticky footer implementation to use [solved-by-flexbox](http://philipwalton.github.io/solved-by-flexbox/demos/sticky-footer/). It is an incrediably simple technique and very little code.

Here is the basic layout we usually use:

    <html>
    <head></head>
	<body>
	  <div id="page">
        <header id="branding-container"></header>
        <div id="content-container"></div>
        <footer id="footer-container"></footer>
      </div>
    </body>
    </html>

Here is the css you need to add:

	body {
      display: flex;
      min-height: 100vh;
      flex-direction: column;
    }
    #content-container {
      flex: 1;
    }

And that is it!  You don't have to do weird negative margins or calculate the height of the footer with empty div tags to push the page down.