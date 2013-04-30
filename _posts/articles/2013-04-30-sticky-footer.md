---
published: true
layout: article
title: Build sticky footers
abstract: Short coding example of sticky footers.
author_twitter: jasonruyle
author: Jason Ruyle
categories: HTML, CSS, Development
- articles

---

# Build sticky footers

It has become the norm for our agency to use _sticky_ _footers_ for nearly all of our sites.  We generally follow the css only principle and below is the code we use.

## HTML

	<html>
	<body>
		<div id="wrapper">
			<div id="footer-push"></div>
		</div>
		<div id="footer"></div>
	</body>
	<html>

## CSS

Make sure you run some type of reset for you stylesheets.

	html, body {
    	height: 100%; }

	#wrapper {
		min-height: 100%;
		height: auto !important;
		height: 100%;
		margin: 0;
		margin-bottom: -200px; }

	#footer-push {
		height: 200px;
		clear: both; }

	#footer {
		height: 200px; }