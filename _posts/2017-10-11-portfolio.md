---
layout:     post
title:      Portfolio - admin login page
date:       2017-10-11 
summary:    portfolio -
categories: git
---


## portfolio - admin login page

[결과보러가기](https://ddnayo.com/bms/login.aspx?ReturnUrl=%2fAms%2fDefault.aspx&id_hotel=)


### HTML
```html
<form method="post" action="./login.aspx?ReturnUrl=%2fAms%2fDefault.aspx&amp;id_hotel=" id="form1">
	<div class="container">
		<div class="login_box">
			<div class="lb_inner">
				<h1 id="ctt_divLogo"><a href="../"><img src="http://www.yeonghyekim.com/img/logo3.gif" alt="떠나요닷컴로고"></a></h1>
			</div>

			<div class="lb_inner">
				<h2>관리자 로그인</h2>
				<div class="input_outer">
					<div class="input_box">
						<input name="ctl00$ctt$id_login" value="kyh" size="15" id="ctt_id_login" tabindex="1" placeholder="아이디" type="text">
						<label for="ctt_id_login">아이디</label>
					</div>
					<div class="input_box">
						<input name="ctl00$ctt$pwd_login" size="15" id="ctt_pwd_login" tabindex="2" placeholder="비밀번호" type="password">
						<label for="ctt_pwd_login">비밀번호</label>
					</div>
					<input name="ctl00$ctt$btn_login" value="확인" onclick="return ValidateCheck('');" id="ctt_btn_login" tabindex="3" class="button" type="submit">
					<div class="save_id">
						<span class="save_input"><input id="ctt_idSave" name="ctl00$ctt$idSave" checked="checked" tabindex="4" type="checkbox"></span>
						<label for="ctt_idSave" class="save_label">ID저장</label>
					</div>						
				</div>
			</div>
			<div class="text_box">
				<p>업체로그인 아이디와 패스워드를 모르시면 <strong>고객센터 02-813-0960</strong> 로 전화주세요.</p>
			</div>
		</div>
		<div id="ctt_divPartner" class="partnership">
			<h2>연동사 안내</h2>
			<ul>
				<li><img src="http://www.yeonghyekim.com/img/part_naver.gif" alt="naver"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_auction.gif" alt="action"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_gmarket.gif" alt="gmarget"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_11.gif" alt="11st"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_dailyhotel.png" alt="데일리호텔"></li>
				<li class="img_height"><img src="http://www.yeonghyekim.com/img/part_dailyhotel2.png" alt="데일리호텔"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_interpark.png" alt="인터파크"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_hoteltime.png" alt="호텔타임"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_isitgood.png" alt="여기어때"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_saleTonight.png" alt="saletonight"></li>
				<li><img src="http://www.yeonghyekim.com/img/part_gajago.png" alt="gajago"></li>
			</ul>
		</div>
	</div>
</form>	
```


### CSS
```css
*{box-sizing:border-box;}
html, body{font-size:12px;color:#666;font-family:"돋움","굴림","arial";}

.login_box{width:500px;margin:20px auto 0;}
.login_box p{padding-top:5px;line-height:16px;}
.login_box p strong{color:#ff106a;font-weight: 700;}



.lb_inner h1{text-align:center;}
.lb_inner h2{margin-bottom:20px;margin-top:20px;font-size: 14px;font-weight: 700;color:#666;}
.lb_inner .input_box{margin-bottom:15px;position: relative;}
.lb_inner .input_box label{position:absolute;top:-99999px;}
.lb_inner .input_box input{width:100%;padding:12px 10px;-moz-appearance:none;-webkit-appearance:none;border:1px solid #d7d7d7;border-radius:3px;}
.lb_inner .input_box input:focus{outline:none;border-color: #ff106a;background:#fff;}
.lb_inner .button{width:100%;padding:12px; border:none;color:#fff;letter-spacing: 2px;border-radius: 3px;background: #ff106a;-webkit-appearance: none;-moz-appearance: none;appearance: none;}
.lb_inner .save_id {margin-top:20px;}
.lb_inner .save_id input{vertical-align:middle;margin-top:-1px;}
/* 제휴업체 로고 들어갈때 */
.lb_inner .align_logo a{display:inline-block;}
.lb_inner .align_logo img{width:100%;}


.text_box{border-top:1px dotted #d7d7d7; border-bottom:1px solid #d7d7d7;padding-top:20px;padding-bottom:20px;margin-top:20px;}



.partnership{width:500px;margin:20px auto 0;}
.partnership h2{margin-bottom: 20px;text-align: center;font-size: 14px;font-weight: 700;color:#666;}
.partnership ul:after{content: '';display: block; clear: both;}
.partnership li{float:left;width:33.33333%;height:70px;line-height:70px;margin-bottom:30px;text-align:center;}
.partnership li img{width:80%;margin:0 auto;vertical-align:middle;}
.partnership li.img_height img{height:100%;width:auto}



/*ie7 hack*/
.lb_inner .input_box input{*width:95.5%;}
.lb_inner .save_id input{*margin-top:-2px;}
.lb_inner .align_logo img{*width:90%;}
.partnership li{*width:32.33333%;}



@media screen and (max-width:525px){
	.login_box{ width:90%;}
	.lb_inner .input_box input{padding:15px 10px;}
	.lb_inner .button{padding:15px 12px;}



	.partnership{width:90%;}
	.partnership li{width:50%;float:left;height:82px;line-height:82px;}

}
```



```css
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video,input,label {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}

article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```
