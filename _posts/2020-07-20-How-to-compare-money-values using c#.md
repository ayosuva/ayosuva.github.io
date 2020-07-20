---
layout: post
title:  "How to compare Money values using c#?"
author: Yosuva
categories: [Ranorex]
featured: true
image: https://upload.wikimedia.org/wikipedia/commons/thumb/7/7a/C_Sharp_logo.svg/1200px-C_Sharp_logo.svg.png
---

In this post, you will learn money comparison using c#

To get only number from the string
```c#
string amount="5000";
decimal converted_amount = decimal.Parse(amount);
if(converted_amount==5000)
{
Console.WriteLine("PASS");
}
else
{
Console.WriteLine("FAIL");
}
```
