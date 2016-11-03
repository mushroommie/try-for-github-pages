---
layout: post
header-img: "img/arch.jpg"
title: "Try adding automatically typing"
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
            <div class="type-js headline">
                <h1 class="text-js">Look mum, I'm typing!</h1>
            </div>
                <!-- Personal Twitter Link -->
            <a href="http://twitter.com/Connor_Gaunt" target="_blank" class="twitterLink">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 410.155 410.155">
                    <path d="M403.632 74.18c-9.113 4.04-18.573 7.23-28.28 9.537 10.696-10.164 18.738-22.877 23.275-37.067 1.295-4.05-3.105-7.554-6.763-5.385-13.504 8.01-28.05 14.02-43.235 17.862-.882.223-1.79.336-2.703.336-2.766 0-5.455-1.027-7.57-2.89C322.2 42.332 301.422 34.49 279.85 34.49c-9.336 0-18.76 1.456-28.015 4.326C223.163 47.71 201.04 71.36 194.1 100.54c-2.605 10.945-3.31 21.9-2.098 32.56.14 1.225-.44 2.08-.797 2.48-.627.704-1.516 1.107-2.44 1.107-.102 0-.208-.005-.313-.015-62.762-5.83-119.358-36.068-159.363-85.14-2.04-2.503-5.953-2.196-7.58.593C13.678 65.565 9.538 80.937 9.538 96.58c0 23.97 9.63 46.562 26.36 63.03-7.035-1.667-13.844-4.294-20.17-7.807-3.06-1.7-6.824.485-6.867 3.985-.438 35.612 20.412 67.3 51.646 81.57-.63.014-1.258.02-1.888.02-4.95 0-9.964-.477-14.898-1.42-3.446-.658-6.34 2.61-5.27 5.952 10.137 31.65 37.39 54.98 70 60.278-27.065 18.17-58.584 27.753-91.39 27.753l-10.226-.005c-3.15 0-5.816 2.054-6.62 5.106-.79 3.007.667 6.178 3.354 7.74 36.966 21.514 79.13 32.884 121.955 32.884 37.485 0 72.55-7.44 104.22-22.11 29.032-13.448 54.688-32.673 76.254-57.14 20.09-22.792 35.8-49.103 46.692-78.2 10.382-27.738 15.87-57.334 15.87-85.59v-1.346c0-4.537 2.05-8.806 5.63-11.712 13.586-11.03 25.416-24.014 35.16-38.59 2.574-3.85-1.484-8.674-5.718-6.796z" fill="#76A9EA" />
                </svg>
            </a>
         </div>
     </div>
</div>


<style>
// CSS Needed to make it work (Wrote not using SCSS at all copy and paste away)
// copy and paste into your CSS and the cursor should appear when typing begins
.text-js{
  opacity: 0;
}
.cursor{
  display: block;
  position: absolute;
  height: 100%;
  top: 0;
  right: -5px;
  width: 2px;
  /* Change colour of Cursor Here */
  background-color: white;
  z-index: 1;
  animation: flash 0.5s none infinite alternate;
}
@keyframes flash{
  0%{
    opacity: 1;
  }
  100%{
    opacity: 0;
  }
}





// Rest of CSS (Purely for this pen)
@import url('https://fonts.googleapis.com/css?family=Open+Sans:300,400');

*{
  margin: 0;
  padding: 0;
  boz-sizing: border-box;
  font-family: "Open Sans", sans-serif
}
.col-md-10{
  background: linear-gradient(135deg,#00C4FF,#9D1BB2);
  display: flex;
  align-items: center;
  justify-content: center;
}
// Text Can be styled just like normal
.headline{
  margin: 20px;
  color: white;
  font-size: 32px;
  text-align: center;
  h1{
    letter-spacing: 1.6px;
    font-weight: 300;
  }
}

.twitterLink{
  position: absolute;
  bottom: 0;
  right: 0;
  margin: 10px 15px;
  z-index: 3;
  svg{
    width: 25px;
  }
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

