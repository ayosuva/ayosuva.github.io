---
layout: post
title:  "Useful Test Automation c# functions or code snippets"
author: Yosuva
categories: [Ranorex]
featured: true
image: https://upload.wikimedia.org/wikipedia/commons/thumb/7/7a/C_Sharp_logo.svg/1200px-C_Sharp_logo.svg.png
---
This post contains few useful c# code snippets that i used in test automation.

To convert today's date to specific format

```js

DateTime.Now.ToString("dd/MM/yyyy")	25/06/2020
DateTime.Now.ToString("dddd, dd MMMM yyyy")	Friday, 29 May 2015
DateTime.Now.ToString("dddd, dd MMMM yyyy")	Friday, 29 May 2015 05:50
DateTime.Now.ToString("dddd, dd MMMM yyyy")	Friday, 29 May 2015 05:50 AM
DateTime.Now.ToString("dddd, dd MMMM yyyy")	Friday, 29 May 2015 5:50
DateTime.Now.ToString("dddd, dd MMMM yyyy")	Friday, 29 May 2015 5:50 AM
DateTime.Now.ToString("dddd, dd MMMM yyyy HH:mm:ss")	Friday, 29 May 2015 05:50:06
DateTime.Now.ToString("MM/dd/yyyy HH:mm")	05/29/2015 05:50
DateTime.Now.ToString("MM/dd/yyyy hh:mm tt")	05/29/2015 05:50 AM
DateTime.Now.ToString("MM/dd/yyyy H:mm")	05/29/2015 5:50
DateTime.Now.ToString("MM/dd/yyyy h:mm tt")	05/29/2015 5:50 AM
DateTime.Now.ToString("MM/dd/yyyy HH:mm:ss")	05/29/2015 05:50:06
DateTime.Now.ToString("dd MMMM yyyy")	29 May 2020
```

To convert string date to DateTime
```js
DateTime dt=DateTime.ParseExact("24/01/2013", "dd/MM/yyyy", null);
```
To remove leading zero from string
```js
string s="0000001234567"
s.TrimStart(new Char[] { '0' } );
Console.WriteLine(s);
```
Output
>1234567

