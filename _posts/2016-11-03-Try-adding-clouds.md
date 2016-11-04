---
layout: post
header-img: "img/arch.jpg"
title: "Try a cloud who can rain and light"
subtitle: "Patience"
date: 2016-11-03
author: "Nanya"
catalog: true
tags:
    - 前端资源
    - 特效
    - 建筑
---

<div class="container-fluid">
    <div class="row">
        <div class="col-md-10 col-md-offset-2">
            <svg class="icon" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:sketch="http://www.bohemiancoding.com/sketch/ns" width="178px" height="178px" viewBox="0 0 178 178" version="1.1">
                    <defs/>
                    <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" sketch:type="MSPage">
                        <g id="Cloud" sketch:type="MSLayerGroup">
                            <circle id="Oval-4" fill="#D8D8D8" sketch:type="MSShapeGroup" cx="89" cy="89" r="89" />
                            <path d="M62.591343 44.5037112C44.8577507 44.6968468 30.59375 52.4037829 30.59375 61.8828125 30.59375 71.4830748 45.2249445 79.265625 63.2734375 79.265625L85.5234375 79.265625 92.2427582 79.265625 107.773438 79.265625C125.821931 79.265625 140.453125 71.4830748 140.453125 61.8828125 140.453125 56.5903424 136.006501 51.8503004 128.992061 48.6620524 129.21354 47.5297254 129.328125 46.3722762 129.328125 45.1953125 129.328125 31.7549453 114.385629 20.859375 95.953125 20.859375 77.8378389 20.859375 63.0934697 31.3831538 62.5913433 44.5037031L62.591343 44.5037112Z" id="Oval-1" fill="#000000" sketch:type="MSShapeGroup" />
                            <path class="lightning" d="M104.118299 81.17867L114.679489 81.1922433 108.93231 92.6730268 117.525366 92.4705578 106.132809 123.121422 112.042867 96.9203512 103.625134 96.9203512 109.25807 85.4655832 102.931763 85.4655832 104.118299 81.17867Z" id="lightning" fill="#D8D8D8" sketch:type="MSShapeGroup" />
                            <path class="rain1" d="M57.7109375 95.5785693C59.63099 95.5785693 61.1875 93.8563015 61.1875 90.64904 61.1875 87.4417785 57.7109375 81.17867 57.7109375 81.17867 57.7109375 81.17867 54.234375 87.4417785 54.234375 90.64904 54.234375 93.8563015 55.790885 95.5785693 57.7109375 95.5785693Z" id="rain1" fill="#4990E2" sketch:type="MSShapeGroup" />
                            <path class="rain2" d="M85.5234375 95.5785693C87.44349 95.5785693 89 93.8563015 89 90.64904 89 87.4417785 85.5234375 81.17867 85.5234375 81.17867 85.5234375 81.17867 82.046875 87.4417785 82.046875 90.64904 82.046875 93.8563015 83.603385 95.5785693 85.5234375 95.5785693Z" id="rain2" fill="#4990E2" sketch:type="MSShapeGroup" />
                            <path class="rain3" d="M71.6171875 102.778519C73.53724 102.778519 75.09375 101.056251 75.09375 97.8489897 75.09375 94.6417281 71.6171875 88.3786197 71.6171875 88.3786197 71.6171875 88.3786197 68.140625 94.6417281 68.140625 97.8489897 68.140625 101.056251 69.697135 102.778519 71.6171875 102.778519Z" id="rain3" fill="#4990E2" sketch:type="MSShapeGroup" />
                        </g>
                    </g>
                </svg>
         </div>
     </div>
</div>

在知乎上看到一个喜欢收集各种前端资源的[林梓](https://www.zhihu.com/people/lin-zi-41-9)的回答:[前端开发资源整理](https://zhuanlan.zhihu.com/p/23344447)。

我找了两天终于找到一个可以适合博客排版的小[SVG图标](http://cssdeck.com/labs/auvy8wts)，还有几个其他的小图标，比如台灯什么的，感兴趣的可以过去看看。

<style>
* {
    padding: 0;
    margin: 0;
}


/*Eco Light icon animation*/

.icon {
    display: block;
    /*  background:red;*/
    margin: 0 auto;
    margin-top: 100px;
}

.icon .glow {
    -webkit-transition: fill 1s ease-in;
    transition: fill 1s ease-in;
}

.icon:hover .glow {
    fill: rgba(121, 175, 58, 0.8);
}


/*Table lamp animation*/

.icon .tableGlow {
    -webkit-transition: fill 1s ease-in;
    transition: fill 1s ease-in;
}

.icon:hover .tableGlow {
    fill: rgba(247, 237, 109, 0.8);
}


/*Cloud animation*/

.icon .lightning {
    -webkit-transition: fill 1s ease-in;
    transition: fill 1s ease-in;
}

.icon:hover .lightning {
    fill: rgb(247, 237, 109);
}

.icon .rain1 {
    fill: #D8D8D8;
    -webkit-transition: 1s ease-in;
    transition: 1s ease-in;
}

.icon:hover .rain1 {
    -webkit-transform: translate(0, 30px);
    transform: translate(0, 30px);
    fill: #666;
}

.icon .rain2 {
    fill: #D8D8D8;
    -webkit-transition: all 0.7s ease-in;
    transition: all 0.7s ease-in;
}

.icon:hover .rain2 {
    -webkit-transform: translate(0, 40px);
    transform: translate(0, 40px);
    fill: #555;
}

.icon .rain3 {
    fill: #D8D8D8;
    -webkit-transition: all 0.5s ease-in;
    transition: all 0.5s ease-in;
}

.icon:hover .rain3 {
    -webkit-transform: translate(0, 50px);
    transform: translate(0, 50px);
    fill: #666;
}


/*wheel animation*/

.icon .wheel {
    -webkit-transition: all 1s ease-in;
    transition: all 1s ease-in;
    -webkit-transform-origin: 50% 50%;
}

.icon:hover .wheel {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
}


/*Bike animation*/

.icon .wheel1 {
    -webkit-transition: all 3s ease-in;
    transition: all 3s ease-in;
    -webkit-transform-origin: 50% 50%;
}

.icon:hover .wheel1 {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
}

.icon .wheel2 {
    -webkit-transition: all 3s ease-in;
    transition: all 3s ease-in;
    -webkit-transform-origin: 50% 50%;
}

.icon:hover .wheel2 {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
}

.icon .grass {
    -webkit-transition: stroke 2s ease-in;
    transition: stroke 2s ease-in;
}

.icon:hover .grass {
    stroke: green;
}


/*Rainfall animation*/

.icon .drop1 {
    fill: #D8D8D8;
    -webkit-transition: 0.7s ease-in;
    transition: 0.7s ease-in;
}

.icon:hover .drop1 {
    -webkit-transform: translate(0, 80px);
    transform: translate(0, 80px);
    fill: #666;
}

.icon .drop2 {
    fill: #D8D8D8;
    -webkit-transition: 1s ease-in;
    transition: 1s ease-in;
}

.icon:hover .drop2 {
    -webkit-transform: translate(0, 60px);
    transform: translate(0, 60px);
    fill: #666;
}

.icon .drop3 {
    fill: #D8D8D8;
    -webkit-transition: 0.5s ease-in;
    transition: 0.5s ease-in;
}

.icon:hover .drop3 {
    -webkit-transform: translate(0, 50px);
    transform: translate(0, 50px);
    fill: #666;
}

.icon .drop4 {
    fill: #D8D8D8;
    -webkit-transition: 1s ease-in;
    transition: 1s ease-in;
}

.icon:hover .drop4 {
    -webkit-transform: translate(0, 50px);
    transform: translate(0, 50px);
    fill: #666;
}

.icon .drop5 {
    fill: #D8D8D8;
    -webkit-transition: 0.6s ease-in;
    transition: 0.6s ease-in;
}

.icon:hover .drop5 {
    -webkit-transform: translate(0, 50px);
    transform: translate(0, 50px);
    fill: #666;
}

.icon .drop6 {
    fill: #D8D8D8;
    -webkit-transition: 0.5s ease-in;
    transition: 0.5s ease-in;
}

.icon:hover .drop6 {
    -webkit-transform: translate(0, 60px);
    transform: translate(0, 60px);
    fill: #666;
}

.icon .drop7 {
    fill: #D8D8D8;
    -webkit-transition: 1s ease-in;
    transition: 1s ease-in;
}

.icon:hover .drop7 {
    -webkit-transform: translate(0, 50px);
    transform: translate(0, 50px);
    fill: #666;
}

.icon .drop8 {
    fill: #D8D8D8;
    -webkit-transition: 1s ease-in;
    transition: 1s ease-in;
}

.icon:hover .drop8 {
    -webkit-transform: translate(0, 30px);
    transform: translate(0, 30px);
    fill: #666;
}

</style>

<script>
    // DISCLAIMER: This function does require jQuery. I've used it here because the project I'm building this for already uses jQuery, so I thought why not. It can be modified quite simply to be done in raw JavaScript.  Just thought I'd let you know.




// This is the funtion you need to copy
// Copy from line 9 to 34

function autoType(elementClass, typingSpeed) {
    var thhis = $(elementClass);
    thhis.css({
        "position": "relative",
        "display": "inline-block"
    });
    thhis.prepend('<div class="cursor" style="right: initial; left:0;"></div>');
    thhis = thhis.find(".text-js");
    var text = thhis.text().trim().split('');
    var amntOfChars = text.length;
    var newString = "";
    thhis.text("|");
    setTimeout(function() {
        thhis.css("opacity", 1);
        thhis.prev().removeAttr("style");
        thhis.text("");
        for (var i = 0; i < amntOfChars; i++) {
            (function(i, char) {
                setTimeout(function() {
                    newString += char;
                    thhis.text(newString);
                }, i * typingSpeed);
            })(i + 1, text[i]);
        }
    }, 1500);
}

$(document).ready(function() {
    // Now to start autoTyping just call the autoType function with the
    // class of outer div
    // The second paramter is the speed between each letter is typed.
    autoType(".type-js", 200);


});
</script>

