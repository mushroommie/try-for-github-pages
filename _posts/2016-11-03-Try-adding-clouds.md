---
layout: post
header-img: "img/arch.jpg"
title: "Try adding some clouds"
subtitle: "Patience"
date: 2016-11-03
author: "Nanya"
catalog: true
tags:
    - 前端资源
    - 特效
    - 犬夜叉
---

<div class="container-fluid container">
    <div id="clouds">
        <div class="cloud1"></div>
        <div class="cloud2"></div>
        <div class="cloud3"></div>
    </div>
    <div id="clouds2">
        <div class="cloud1"></div>
        <div class="cloud2"></div>
        <div class="cloud3"></div>
    </div>
</div>

<style>
.container {
    background: #fff;
}

/* Clouds */
#clouds {
  top: 100px;
  position: relative;
  -webkit-animation: move 20s infinite linear;
  -moz-animation: move 20s infinite linear;
  -ms-animation: move 20s infinite linear;
  z-index: 1;
}

#clouds2 {
  position: relative;
  -webkit-animation: backup 14s infinite linear;
  -moz-animation: backup 14s infinite linear;
  -ms-animation: backup 14s infinite linear;
  z-index: 2;
}

.cloud1, .cloud2, .cloud3 {
  opacity: 1;
}

.cloud1 {
  width: 200px;
  height: 60px;
  background: #00c9ee;
  position: absolute;
  top: 80px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;

}

.cloud1:after {
  content: '';
  position: absolute;
  background: #00c9ee;
  width: 80px;
  height: 80px;
  top: -40px;
  left: 20px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;

}

.cloud1:before {
  content: '';
  position: absolute;
  background: #00c9ee;
  width: 100px;
  height: 100px;
  top: -60px;
  right: 30px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;
}

.cloud2 {
  width: 100px;
  height: 30px;
  background: #00c9ee;
  position: absolute;
  top: 180px;
  left: 400px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;
}

.cloud2:after {
  content: '';
  position: absolute;
  background: #00c9ee;
  width: 40px;
  height: 40px;
  top: -20px;
  left: 10px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;
}

.cloud2:before {
  content: '';
  position: absolute;
  background: #00c9ee;
  width: 50px;
  height: 50px;
  top: -30px;
  right: 15px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;

}

.cloud3 {
  width: 200px;
  height: 60px;
  background: #00c9ee;
  position: absolute;
  top: 100px;
  left: 740px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;
}

.cloud3:after {
  content: '';
  position: absolute;
  background: #00c9ee;
  width: 80px;
  height: 80px;
  top: -40px;
  left: 20px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;
}

.cloud3:before {
  content: '';
  position: absolute;
  background: #00c9ee;
  width: 100px;
  height: 100px;
  top: -60px;
  right: 30px;

  -webkit-border-radius: 200px;
  -moz-border-radius: 200px;
  border-radius: 200px;
}

@-webkit-keyframes move {
  0% {left: 0px;}
  49% {left: 940px; opacity: 1;}
  50% {left: 940px; opacity: 0;}
  51% {left: -940px; opacity: 0;}
  52% {left: -940px; opacity: 1;}
  100% {left: 0px;}
}

@-webkit-keyframes backup {
  0% {left: -940px;}
  100% {left: 940px;}

}

@-moz-keyframes move {
  0% {left: 0px;}
  49% {left: 940px; opacity: 1;}
  50% {left: 940px; opacity: 0;}
  51% {left: -940px; opacity: 0;}
  52% {left: -940px; opacity: 1;}
  100% {left: 0px;}
}

@-moz-keyframes backup {
  0% {left: -940px;}
  100% {left: 940px;}

}

@-ms-keyframes move {
  0% {left: 0px;}
  49% {left: 940px; opacity: 1;}
  50% {left: 940px; opacity: 0;}
  51% {left: -940px; opacity: 0;}
  52% {left: -940px; opacity: 1;}
  100% {left: 0px;}
}

@-ms-keyframes backup {
  0% {left: -940px;}
  100% {left: 940px;}

}

#clouds .cloud1, #clouds .cloud2, #clouds .cloud2:after, #clouds .cloud2:before, #clouds .cloud3, #clouds .cloud1:after, #clouds .cloud1:before, #clouds .cloud3:before, #clouds .cloud3:after {
    background: #00f1ee;
    box-shadow: 0px 0px 20px 5px #00f1ee;
    -moz-box-shadow: 0px 0px 20px 5px #00f1ee;
    -webkit-box-shadow: 0px 0px 20px 5px #00f1ee;
}

</style>

