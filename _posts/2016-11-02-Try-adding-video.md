---
layout: post
title: "Try adding video"
header-img: "img/Tanya.jpg"
subtitle: "Tanya"
date: 2016-11-02
author: "Nanya"
catalog: true
tags:
    - video
    - Tanya
    - Nanya
---
<div class="container-fluid">
    <div class="row">
        <video autoplay="true" class="col-md-10 col-md-offset-2" controls src="https://rawgithub.com/mushroommie/videos/master/Tanya-Speechlesser.mp4"></video>
    </div>
    <div class="row">
        <canvas id="c" class="col-md-2"></canvas>
        <div class="col-md-10">
            <p>并不是每天都有什么事情可以记录，要干的事情太多了，Udacity的课眼看着就要到期，毕设还没有做完。值得注意的是投在拉勾网上的简历全军覆没了。不知道什么时候可以找到工作。</p>
            <p>在知乎上看到一个非常不错的前端资源整理回答:<a href="https://zhuanlan.zhihu.com/p/23344447">前端Web开发资源整理:</a></p>
            左侧的特效来自:<a href="http://cssdeck.com/labs/a8ed194d">CssDeck</a>
        </div>
    </div>
</div>

<style>
    canvas {background: #CFF09E;}
</style>

<script>
(function() {

    var c = document.getElementById("c"),
        ctx = c.getContext("2d");
    c.width = innerWidth;
    c.height = innerHeight;

    var lines = [],
        maxSpeed = 5,
        spacing = 5,
        xSpacing = 0,
        n = innerWidth / spacing,
        colors = ["#3B8686", "#79BD9A", "#A8DBA8", "#0B486B"],
        i;

    for (i = 0; i < n; i++) {
        xSpacing += spacing;
        lines.push({
            x: xSpacing,
            y: Math.round(Math.random() * c.height),
            width: 2,
            height: Math.round(Math.random() * (innerHeight / 10)),
            speed: Math.random() * maxSpeed + 1,
            color: colors[Math.floor(Math.random() * colors.length)]
        });
    }


    function draw() {
        var i;
        ctx.clearRect(0, 0, c.width, c.height);

        for (i = 0; i < n; i++) {
            ctx.fillStyle = lines[i].color;
            ctx.fillRect(lines[i].x, lines[i].y, lines[i].width, lines[i].height);
            lines[i].y += lines[i].speed;

            if (lines[i].y > c.height)
                lines[i].y = 0 - lines[i].height;
        }

        requestAnimationFrame(draw);

    }

    draw();

}());
</script>