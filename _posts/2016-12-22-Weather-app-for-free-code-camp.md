---
layout: post
header-img: "img/MerryCmas-desktop_1440x900.jpg"
title: ""
subtitle: "天气APP"
author: "Nanya"
date: 2016-12-22
catalog: true
tags:
    - free code camp
    - weather
    - api
---

今天完成了第二个任务：一个根据用户所在位置显示天气的app

调用的第三方接口有:

 - [ipinfo](http://ipinfo.io) 获取用户所在的城市名字和国家名字
 - [openweathermap](https://openweathermap.org/city) 根据用户所在地获取当前天气

以上两个api都是免费使用的，第二个api需要注册得到免费api key。我的code pen地址：[Weather app from mushroommie](http://codepen.io/mushroommie/full/WomPMr/)。获取数据的方式采用jsonp格式，解决跨域问题。可以切换到editor view看看具体是如何实现的。
