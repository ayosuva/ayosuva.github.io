---
layout: post
title:  "Useful Test Automation Regex"
author: Yosuva
categories: [ Ranorex, tutorial ]
image: assets/images/16.jpg
---
This post contains few example regex that i used in test automation.

To get only number from the string
```js
\d+
```
To get just amount value
```js
([0-9]+[\\.,0-9]*)
```
To get first 5 characters from a string 
```js
^.{5}
```
To get the text of btw two strings
```js
(?<=Reference is )(.*)(?= and)
```
