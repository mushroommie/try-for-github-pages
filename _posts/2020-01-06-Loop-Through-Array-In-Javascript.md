---
layout: post
title: "loop-through-an-array-in-javascript"
subtitle: "js中数组循环的几种方法"
date: 2020-01-06
author: "Journee"
catalog: true
tags:
    - JS
    - array
---

循环数组，有好几种方法可以选择：

1、for循环

    var myStringArray = ["Hello","World"];
    var arrayLength = myStringArray.length;
    for (var i = 0; i < arrayLength; i++) {
        console.log(myStringArray[i]);
        //Do something
    }
    
优点：
* 任何环境都适用
* 可以使用break和continue这两种流控制语句

缺点：
* 太啰嗦
* 是个祈使句
* 容易引发[off-by-one-errors 差一错误](https://zh.wikipedia.org/zh-hans/%E5%B7%AE%E4%B8%80%E9%94%99%E8%AF%AF)

2.Array.prototype.forEach
ES5规范引入了很多有利的数组处理方法，Array.prototype.forEach是其中之一，它提供了一种简洁的遍历数组的方法。


    const array = ["one", "two", "three"]
    array.forEach(function (item, index) {
      console.log(item, index);
    });
    
ES5规范发布时（截至2009年12月）已经有将近10年的时间，它已经由台式机、服务器和移动环境中的几乎所有现代引擎实现，
因此可以安全地使用他们。
有了ES6的箭头函数，它更加简洁。

    array.forEach(item => console.log(item));
    
箭头函数也得到了广泛的实现，除非您计划支持古老的平台（例如，IE11）；你也可以安全地离开。

优点：
* 短小、简洁。
* 声明式的。

缺点：
* 不能使用break/continue
通常，你可以通过在迭代之前过滤数组元素来打破命令式循环的需要,例如：
    array.filter(item => item.condition < 10)
         .forEach(item => console.log(item))

记住，如果你是想通过循环一个数组来创建另一个数组，应该使用map，我已经见过好多次这种反模式。

反模式：

    const numbers = [1,2,3,4,5], doubled = [];
    numbers.forEach((n, i) => { doubled[i] = n * 2 });

map的正确使用方法：
    
    const numbers = [1,2,3,4,5];
    const doubled = numbers.map(n => n * 2);
    console.log(doubled);   
并且，如果你想使用reduce数组来获取一个值，例如，你想获取一个数字数组的和，你应该使用reduce方法。
反模式：
    
    const numbers = [1,2,3,4,5];
    const sum = 0;
    numbers.forEach(num => { sum += num });                 
    Uncaught SyntaxError: Identifier 'numbers' has already been declared at <anonymous>:1:1
reduce的正确使用方法：

    const numbers = [1,2,3,4,5];
    const sum = numbers.reduce((total, n) => total + n, 0);
    console.log(sum);     
    
3.ES6中的for-of语句

ES6标准介绍了可遍历对象的概念，并且定义一种新的结构体来遍历数据，for...of语句。
这个语句对任意一种可遍历对象都适用，也可用于generators（有[Symbol.iterator]属性的任何一个对象）。

根据定义，数组对象是ES6中内置的迭代器，因此你可以在数组中使用这个语句:

    let colors = ['red', 'green', 'blue'];
    for (const color of colors){
      console.log(color);
    }
优点：
* 它可以遍历各种对象。
* 可以使用常用的流控制语句（break/continue）。
* 可以用来迭代串行异步值。

缺点：
* 如果你的目标是更老的浏览器，转义的输出可能会[震惊到你](https://babeljs.io/repl#?babili=false&browsers=&build=&builtIns=false&spec=false&loose=false&code_lz=GYewTgBAFAxiB2BnALhOAbcETDSTYiAlAN4BQEeS-ApgHSYDms-4RA3GQL5A&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=true&fileSize=false&timeTravel=false&sourceType=module&lineWrap=false&presets=es2015&prettier=false&targets=&version=7.4.4&externalPlugins=)。

不要使用for...in
@zipcodeman推荐使用for...in语句，但是如果是遍历数组的话，应该避免for-in语句，该语句是为了列举对象属性。

不应该用它来遍历数组这类对象是因为：
1、迭代的顺序不能保证；数组索引不能按数字顺序访问。
2、继承的属性也会被遍历。

第二点是，它会带来很多问题，例如，如果你扩展了Array.prototype对象让它有了一个方法，这个方法属性也会被列举出来。
例如：

    Array.prototype.foo = "foo!";
        var array = ['a', 'b', 'c'];
        
        for (var i in array) {
          console.log(array[i]);
        }
上面的代码会输出，"a", "b", "c", 和 "foo!"。

如果你使用一些严重依赖于原生原型扩展的库（例如MooTools），那么这将是一个特别的问题。

如前所述，for in是用来循环对象属性的，例如：

    var obj = {
          "a": 1,
          "b": 2,
          "c": 3
        };
    
        for (var prop in obj) {
          if (obj.hasOwnProperty(prop)) { 
          // or if (Object.prototype.hasOwnProperty.call(obj,prop)) for safety...
            console.log("prop: " + prop + " value: " + obj[prop])
          }
        }
        
在上面的例子中，hasOwnProperty方法只允许列举独有属性，也就是说，只列举对象物理上具有的属性，而不允许列举继承的属性。

我建议你读一下下面的文章：[Enumeration VS Iteration](http://web.archive.org/web/20101213150231/http://dhtmlkitchen.com/?category=/JavaScript/&date=2007/10/21/&entry=Iteration-Enumeration-Primitives-and-Objects) 




    
    






    

    
    



    