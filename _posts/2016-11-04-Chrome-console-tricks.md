---
layout: post
header-img: "img/chrome-theme.png"
title: "Google Chrome Console的调试技巧"
subtitle: "如何更高效的使用Google Chrome"
date: 2016-11-04
author: "Nanya"
catalog: true
tags:
    - Chrome
    - Google
    - Console
    - Tanya
    - 蔡健雅
---

文章翻译自[treamtreehouse](http://blog.teamtreehouse.com/mastering-developer-tools-console).

    开发者工具控制台（console）是对你来说在调试前端web应用的时候可用的工具中最有力的一个。console有一整套API，提供多种方法让调试更加容易。看见开发者用
<span style="color">console.log()</span>或者console.dir()来定位问题不是什么特别的事情；但是console可以提供更多的东西。

在这篇博文中你将会学习如何用[Chrome console API](https://developers.google.com/web/tools/chrome-devtools/console/console-reference)提供的方法调试你的web应用程序。一些浏览器可能比另一些支持更多的功能，因此我会在继续博文的同事指出一些兼容性问题。

