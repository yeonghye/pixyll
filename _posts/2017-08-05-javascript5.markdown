---
layout:     post
title:      Javascript 글 편집기
date:       2017-08-05 
summary:    Javascript #4
categories: Javascript
---

## Javascript #4

[결과보러가기](https://jsfiddle.net/lea2015/q69krneg/1/)


### HTML
```html
<div id="wrap">
	<h1>editor</h1>
	<table>
		<tbody>
			<tr>
				<th>
					<select name="fontFamily" id="fontFamily">
						<option value="돋움">돋움</option>
						<option value="바탕" >바탕</option>
						<option value="arial">arial</option>
						<option value="verdana">verdana</option>
					</select>
				</th>
				<th>
					<select name="fontSize" id="fontSize">
						<option value="9pt">9pt</option>
						<option value="12pt">12pt</option>
						<option value="14pt">14pt</option>
						<option value="16pt">16pt</option>
						<option value="20pt">20pt</option>
					</select>
				</th>
				<th><button type="button" id="fontWeight"><span>가</span></button></th>
				<th><button type="button" id="fontDeco"><span>가</span></button></th>
				<th><button type="button" id="fontStyle"><span>가</span></button></th>
			</tr>
			<tr>
				<td colspan="5" class="textpad">
					<textarea name="textpad" id="textpad" cols="30" rows="10"></textarea>
				</td>
			</tr>
		</tbody>
	</table>
</div>
```



### CSS
```css
*{margin:0;padding:0;}
#wrap{width:660px;margin:50px auto;}
h1{text-align: center;}
table{border-collapse: collapse;width:100%;}
table th{border:1px solid #ddd;height:40px;}
table td{border:1px solid #ddd;width:20%;}

#fontFamily{height:30px;}
#fontFamily option{height:30px;}

#fontSize{height:30px;}
#fontSize option{height:30px;}

#fontWeight{width:30px;height:30px;}
#fontWeight span{font-weight: 700;}

#fontDeco{width:30px;height:30px;}
#fontDeco span{text-decoration: underline;}

#fontStyle{width:30px;height:30px;}
#fontStyle span{font-style: italic;}

.textpad{height:500px;background:#eaeaea;}
.textpad textarea{height:500px;width: 100%;border:none;background:#fafafa;}
```



### JAVASCRIPT
```javascript
var textpad = document.getElementById("textpad");

document.getElementById("fontFamily").addEventListener("click",function(){
	var fontFamily = document.getElementById("fontFamily");
	var fontFamilyVal = fontFamily.options[fontFamily.selectedIndex].text;
	textpad.style.fontFamily = fontFamilyVal;
});



document.getElementById("fontSize").addEventListener("click",function(){
	var fontSize = document.getElementById("fontSize");
	var fontSizeVal = fontSize.options[fontSize.selectedIndex].text;
	textpad.style.fontSize = fontSizeVal;
});



document.getElementById("fontWeight").addEventListener("click",function(){
	if(textpad.style.fontWeight != 700){
		textpad.style.fontWeight = 700;
	}else{
		textpad.style.fontWeight = 500;
	}
});



document.getElementById("fontDeco").addEventListener("click",function(){
	if(textpad.style.textDecoration != "underline"){
		textpad.style.textDecoration = "underline";

	}else{
		textpad.style.textDecoration = "none";
	}
});



document.getElementById("fontStyle").addEventListener("click",function(){
	if(textpad.style.fontStyle != "italic"){
		textpad.style.fontStyle = "italic";
	}else{
		textpad.style.fontStyle = "normal";
	}
});
```