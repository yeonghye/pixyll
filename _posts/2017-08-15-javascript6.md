---
layout:     post
title:      Javascript D-day 날짜구하기
date:       2017-08-15 
summary:    Javascript #5
categories: Javascript
---

### Javascript D-day 구현하기

#### HTML
```html
<div class="wrap">
	<div class="inputBtn">
		<input type="text" id="inputtxt" placeholder="예)2016-01-01">
		<button onclick="inputSave()">save</button>
	</div>
	<div class="dateBox">
		<div>디데이<div id="dDay"></div></div>
		<div>오늘(기준) <div id="toDay"></div></div>
		<div>남은날<div id="dayLeft"></div></div>
	</div>
</div>
```




#### CSS
```css
*{margin:0;padding: 0;}
.wrap{width:300px;margin:0 auto;}
.inputBtn{margin-top:15px;}
.inputBtn input[type="text"]{height: 30px;color:#ccc;padding:0 20px;}
.dateBox div{min-height: 30px;line-height:30px;margin-top:5px;}

#dDay{background: #eee;padding:0 20px;}
#toDay{background: #ddd;padding:0 20px;}
#dayLeft{background: #bbb;padding:0 20px;}
```





#### Javascript
```javascript
function inputSave(){
  /*디데이*/
  var inputDate = document.getElementById("inputtxt").value;
  document.getElementById("dDay").innerHTML = inputDate;

  var dday = new Date(inputDate);
  var d_year = dday.getFullYear();
  var d_month = dday.getMonth()+1;
  var d_day = dday.getDate();
  var d_ymd = d_year+"-"+d_month+"-"+d_day;


  /*오늘(기준)*/
  var toDay = new Date();
  var year = toDay.getFullYear();
  var month = toDay.getMonth()+1;
  var day = toDay.getDate();
  var ymd = year+"-" + month+"-" +day;
  document.getElementById("toDay").innerHTML = ymd;


  /*남은날구하기*/
  var time = 24*60*60*1000;
  var day_left = Math.ceil((dday.getTime() - toDay.getTime())/time);
  document.getElementById("dayLeft").innerHTML = -day_left;
}
```
