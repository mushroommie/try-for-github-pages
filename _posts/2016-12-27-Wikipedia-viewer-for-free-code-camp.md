---
layout: post
header-img: "img/animals.png"
title: "Wikipedia viewer"
subtitle: "维基百科浏览工具"
author: "Nanya"
date: 2016-12-27
catalog: true
tags:
    - free code camp
    - Wikipedia viewer
    - api
---

最近几天做了一个Wikipedia viewer，不知道中文翻译过来应该怎么说。主要用到Vue和ajax，最关键的查询url来自下面这个[stackoverflow 上的回答](http://stackoverflow.com/questions/25891076/wikipedia-api-fulltext-search-to-return-articles-with-title-snippet-and-image)，把第一个答案的gsrlimit参数从10改成20，可以获得20个结果，但是如果改成100的话就会出现有的结果没有extract字段的问题，也就是没有说明性段落，只有一个标题，这样就很尴尬，所以还是取20应该就够了。

因为涉及到根据获取到的数据动态渲染DOM，为了避免先取值，再取DOM，再写回DOM的繁杂流程，引入框架Vue，上手容易，参考文档能看懂，更多参考[Vue.js 官方文档](https://cn.vuejs.org/v2/guide/)。

完成后的项目放在我的Codepen上：[mushroommie's codePen](http://codepen.io/mushroommie/full/xRNeGe/)。