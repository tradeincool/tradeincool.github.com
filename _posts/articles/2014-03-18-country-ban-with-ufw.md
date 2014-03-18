---
published: 
  - true
  - "false"
layout: article
title: Country ban with UFW
abstract: Ban countries with UFW
author_twitter: jasonruyle
author: Jason Ruyle
categories: articles
---

Grab your different country ip addresses and save as Linux IPTables

http://www.ip2location.com/free/visitor-blocker


##Add country##
Run the following command

```
while read line; do sudo ufw deny from $line; done < all.txt
```

Where the filename is the country.


##Remove country##
To remove or revert these rules, keep that list of IPs! Then run a command like so to remove the rules:

```
while read line; do sudo ufw delete deny from $line; done < all.txt
```

##Suggestion##
What I did was exported each individual country as their own country.txt file.
But then realized that I wanted to run this thing one time, so I ran the following command:

```
cat *.txt >> all.txt
```

Then you can run your rule against all of the files.