---
layout: post
header-img: "img/chrome-theme.png"
title: "使用Chrome Console的调试技巧"
subtitle: "除了console.log，console不能干别的了么？"
author: "Nanya"
date: 2016-11-04
catalog: true
tags:
    - Chrome
    - Console
    - 阿肆
    - 1 克拉
---

<audio autoplay="ture" controls src="https://rawgithub.com/mushroommie/loved-songs/master/Tanya-1-Carat.mp3"></audio>

文章翻译自[treamtreehouse](http://blog.teamtreehouse.com/mastering-developer-tools-console)，些许地方有改动，转载请标明出处。

开发者工具控制台（console）是对你来说在调试前端web应用的时候可用的工具中最有力的一个。console有一整套API，提供多种方法让调试更加容易。看见开发者用
<span style="color:red">console.log()</span>或者<span style="color:red">console.dir()</span>来定位问题不是什么特别的事情；但是console可以提供更多的东西。

在这篇博文中你将会学习如何用[Chrome console API](https://developers.google.com/web/tools/chrome-devtools/console/console-reference)提供的方法调试你的web应用程序。一些浏览器可能比另一些支持更多的功能，因此我会在继续博文的同事指出一些兼容性问题。

*Let's get the dance started,now!(稍稍改动了一些，引用wuli Jolin的名言~)*

## 使用Console

如果你以前没有使用过console，不要担心。在这一部分，我将向你展示怎么获取并且使用console。如果你已经熟悉的话，随意跳到下一个部分即可。

有几种打开浏览器开发者工具的不同方法。最简单的方法是点击页面上的某个地方，然后在出现的菜单栏中选择“检查”。

你也可以用快捷键打开开发者工具。Mac上的大多数浏览器的快捷键是<span style=
"color:red">Alt+Command+I</span>，Windows可以使用<span style="color:red">Ctrl+Shift+I</span>。

<img src="https://rawgithub.com/mushroommie/images/master/console/open-console.png">

<span style="font-size:12px">在Chrome中打开开发者工具。</span>

打开开发者工具之后，你可以点击下图中箭头所指的标签页切换到console。

<img src="https://rawgithub.com/mushroommie/images/master/console/change-to-console.png">

<span style="font-size:12px">切换到console</span>

**注意：**在这篇文章中我们将会使用浏览器默认的开发工具。有很多特别棒的浏览器插件可以提供相似的工具。使用Firefox的用户可以安装Firebug，因为firebug console支持很多默认的Firefox console不支持的方法。

现在你已经打开了console，让我们来执行一个简单的语句。

在console中输入下面的内容，然后点击**Enter**。

	console.log("Hello World!");

你会看到测试的*Hello World!*在console中被打印了出来（如下图所示）。

<img src="">

<span style="font-size:12px">在console中使用console.log</span>

现在你已经学会了怎么使用console，让我们来看下你可以用来调试你的应用的<span style="color:red">方法</span>。

## console.log(object[,object,...])

让我们从最长被使用的<span style="color:red">console</span>方法
<span style="color:red">console.log</span>开始。这个方法只是在console中简单的输出一个对象。

	console.log("Hello Trehouse");

<img src="https://rawgithub.com/mushroommie/images/master/console/hello-world.png">

如果你列举出了几个对象，它们会被空格连接成一个单独的字符串输出到console。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-log.png">

<span style="font-size:12px">使用console.log输出多个对象</span>

第一个参数可以包括*格式化指定符(format specifiers)*，允许你定义后续对象的格式和位置。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-log-1">

<span style="font-size:12px">使用带有格式化指定符的console.log</span>。


chrome支持下面的格式化字符：

<table>
<thead>
<tr>
<th>Specifier</th>
<th align="left">Output</th>
</tr>
</thead>
<tbody>
<tr>
<td>%s</td>
<td align="left">Formats the value as a string</td>
</tr>
<tr>
<td>%i or %d</td>
<td align="left">Formats the value as an integer</td>
</tr>
<tr>
<td>%f</td>
<td align="left">Formats the value as a floating point value</td>
</tr>
<tr>
<td>%o</td>
<td align="left">Formats the value as an expandable DOM element. As seen in the Elements panel</td>
</tr>
<tr>
<td>%O</td>
<td align="left">Formats the value as an expandable JavaScript object</td>
</tr>
<tr>
<td>%c</td>
<td align="left">Applies CSS style rules to the output string as specified by the second parameter</td>
</tr>
</tbody>
</table>

使用%c格式化指定符允许你设置console输出的样式。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-log-2.png">

<span style="font-size:12px>使用console.log得到带有样式的输出</span>

## console.assert(expression,object)

    <span style="color:red">console.assert()</span>方法需要两个参数，一个bool的表达式，还有一个对象。如果表达式是<span style="color:red">false</span>，那么对象就会被打印到console。

通常情况下，你会使用一个字符串对象作为第二个参数，但是任意有效的javascript对象也同样可以。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-assert.png">

<span style="font-size:12px">使用console.assert()</span>

这个表达式检查1是不是大于2。如果不是，消息'1 is not bigger than 2'被打印到控制台。

## console.clear()

<span style="color:red">console.clear()</span>方法清楚在console中的所有输出。

**注意：**这个方法不被Firefox默认的开发工具支持，但是在Firebug console中收到支持。

## console.count(label)

输出带有同样标记的count()方法在同一行被激活的次数。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-count.png">

<span style="font-size:12px">在console中使用console.count()</span>

**小窍门：**你可以使用那个<span style="color:red">Shift+Enter</span>来换行，写多行表达式。

**注意：**这种方法原生Firefox不支持，替代使用Firebug console。

## console.dir(object)

<span style="color:red">console.dir()</span>方法将会把输入的对象打印成Javascript形式。这个方法在检测HTML元素时十分有用，因为它展示元素的DOM格式而不是像<span style="color:red">console.log()</span>一样输出XML格式。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-dir.png">

<span style="font-size:12px">使用console.dir()来检查HTML元素</span>

## console.info()

<span style="color:red">console.info()</span>方法和<span style="color:red">console.log()</span>功能相同，除了info的log信息带有*info*标志。你可以使用这个特性当作来方便的过滤你的log信息。

注意下图中log信息左侧的蓝色的info图标。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-info.png'>

<span style="font-size:12px">使用console.info打印log信息</span>

## console.table(data)

<span style="color:red">console.table()</span>方法允许你在控制台中以机构化数据的格式输出可交互的表格。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-table.png">

<span style="font-size:12px">用console.table()创建交互性表格</span>

这种方法在检查AJAX返回的数据时十分方便。

**注意：**这种方法原生Firefox不支持，可以使用firebug。

## console.warn(object[,object,...])

最后，<span style="color:red">console.warn()</span>方法将在控制台输出带有<span style="color:red">warning</span>标志的消息。

<img src="https://rawgithub.com/mushroommie/images/master/console/console-warn.png">

<span style="font-size:12px">使用console.warn()输入告警信息</span>

## Summary

在这篇博文中，你学到了几种<span style="color:red">console</span>方法来调试你的web应用。你会发现相比其他的，其中的几种你会更经常用到。但那时了解可以从console中拿到什么东西绝对是有用的。

我建议你读一下下面*Further Reading*的部分，尤其是Google Developers website的[dev tools tips and tricks](https://developers.google.com/chrome-developer-tools/docs/tips-and-tricks)。

## Further Reading

- [MDN:Console Documentation](https://developer.mozilla.org/en-US/docs/Web/API/console)
- [Google Developers:Console API Reference](https://developers.google.com/chrome-developer-tools/docs/console-api)
- [Google Developers:Dev Tools Tips and Tricks](https://developers.google.com/chrome-developer-tools/docs/tips-and-tricks)










































