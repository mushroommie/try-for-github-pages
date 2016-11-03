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
        <div class="col-md-10">What is going on.</div>
    </div>
</div>

<style>
    canvas {background: #CFF09E;}
</style>

<script>
(function() {

    var c = document.getElementById("c"),
        ctx = c.getContext("2d");
    ctx.font="20px Georgia";
    ctx.fillText("Test",10,50);
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