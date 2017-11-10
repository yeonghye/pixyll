---
layout:     post
title:      Javascript 예제 - 시계
date:       2017-07-25 
summary:    Javascript #2
categories: Javascript
---

## Javascript 시계

[결과보러가기](https://jsfiddle.net/leayhkim/r8oa4qtu/)


### HTML
```html
<div id="clock">
	<div class="hand" id="hours"></div>
	<div class="hand" id="minutes"></div>
	<div class="hand" id="seconds"></div>



	<div class="line00"></div>
	<div class="line00 line02"></div>
	<div class="line00 line04"></div>
	<div class="line01 "></div>
	<div class="line01 line03"></div>
	<div class="line01 line05"></div>
	<div class="circle01"></div>
</div>
```



### CSS
```css
*{background: #ccc;}
#clock{position: relative;width:400px;height:400px;background: #fff;border-radius:50%;margin:50px auto;}
.hand{position: absolute;width:50%;height:5px;background: #000;transform-origin:100%;top:50%;}
#hours{background: #004488;width: 30%;left:80px;z-index:90;}
#minutes{background: #008888;width: 40%;left:40px;z-index:90;}
#seconds{z-index: 90;}

.line00{width:100%;height:5px;background: #000;position:absolute;top:50%;}
.line02{transform:rotate(30deg);}
.line04{transform:rotate(60deg);}

.line01{width:5px;height: 100%;background: #000;position: absolute;left:50%;}
.line03{transform:rotate(30deg);}
.line05{transform:rotate(60deg);}
.circle01{width:360px;height: 360px;border-radius:50%;background: #fff;position: absolute;left:5%;top:5%;}
```



### JAVASCRIPT
```javascript
var hourH = document.getElementById("hours");
var minuH = document.getElementById("minutes");
var secoH = document.getElementById("seconds");


function setTime(){
    var now = new Date();

    var hour = now.getHours();
    var minu = now.getMinutes();
    var seco = now.getSeconds();

    var hourD = (hour/12)*360 +90;
    var minuD = (minu/60)*360 +90;
    var secoD = (seco/60)*360 +90;

    hourH.style.transform = "rotate("+ hourD +"deg)";
    minuH.style.transform = "rotate("+ minuD +"deg)";
    secoH.style.transform = "rotate("+ secoD +"deg)";

};
setInterval(setTime, 1000);
```