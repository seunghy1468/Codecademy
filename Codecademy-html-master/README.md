# HTML

🍈 HTML (Hypertext Markup Language)   
	- 웹 브라우저 상에서 보여지도록 디자인된 문서   
	- 표준화된 Markup Language를 이용

🍋 Markup Language
	- 일반적인 text 문서에 Annotating된 것

	<recipe>
		<title> Peanut-butter On A Spoon </title> 
	</recipe>
	
이처럼 tag를 이용하여 구조적으로 작성한 것을 의미한다.

------------------------------------------------------
🍌 JS Bin   
	- 개발 tool을 pc에 설치하지 않아도 간단하게 동작하는 것을 볼 수 있다.
```
<!DOCTYPE html>      	// 관습적으로 tag를 표기
<html>                  // 가장 최상위 tag
	<head>          // icon, 검색, css 정의. Metadata만 있다.
		  <meta charset="utf-8">
		  <meta name="viewport" content="width=device-width">
	
		  <title>JS Bin</title>
	</head>
	<body>  // 요소부분
	
	</body>
</html>
```
	- W3C 에서 정의된 규정에 따라 이런 규칙으로 모든 브라우저에서 동작한다. (간혹 그렇지 않은 브라우저가 존재한다.)
	Meta charset="utf-8" 현존하는 모든 언어에 대한 정의
	meta name="viewport" content="width=device-width" 스크린의 모든 너비를 이용

🍍 MDN    
	- 지원가능한, 정의된 tag들을 모두 확인할 수 있다!   
	- 정보도 가장 빠르게 업데이트 되고 있기 때문에 꼭!! 이용해보자   

🌶️ short-cut key      
	ol>li*3 를 입력하고 tab 키를 누르면 다음과 같이 된다.
	
   	
	<ol>   		// ol안에 list 3개를 만들어 넣는다.
		<li></li>   
		<li></li>   
		<li></li>   
	
	
	div.container>div.item.item${$}*10를 입력하고 tab을 누르면 다음과 같이 된다.
	
	
	<div class="container">
	      <div class="item item1">1</div>
	      <div class="item item2">2</div>
	      <div class="item item3">3</div>
	      <div class="item item4">4</div>
	      <div class="item item5">5</div>
	      <div class="item item6">6</div>
	      <div class="item item7">7</div>
	      <div class="item item8">8</div>
	      <div class="item item9">9</div>
	      <div class="item item10">10</div>
    	</div>
	
-------------------------------------------------------------
더미용 text   
	p>lorem 입력후 tab키
		
	p>lorem    
	p>lorem4 // 이런식으로 단어 개수 조절 가능   

* 2021.03.22 html course in Codecademy (chapter1) 
  * body, head, h, p, img, video, title, span, strong, em, vh    
  * vh : 부모의 크기와 상관없이 100% 사용하겠다.   

* 2021.03.23 html course in Codecademy (chapter2)
  * !DOCTYPE html, html, table, thead, tbody

* 2021.03.23 html course in Codecademy (chapter3)
  * form, label, input, text, password

* 2021.03.26 html course in Codecademy (chapter4)
  * hr, section, option, number, range(min, max (number)), checkbox, radio 

* 2021.03.27 html course in Codecademy (chapter4)
  * select, datalist, textarea, submit   
  * purpose of a form : users can input information and sent it.   
  * action : form's information이 어디로 이동하는지 결정한다.   
  * method : information을 어떻게 처리하고 보낼지 결정한다.   

* 2021.03.27 html course in Codecademy (chapter5)
  * validation, required : you must fill out here. , minlength, maxlength (text), pattern   
  * server-side verification // client-side verification : 정보를 서버로 전송하기 전에 브라우저에서 수행

* 2021.03.27 html course in Codecademy (chapter6)
  * semantic vs non-semantic 비교!!

* div --> header, nav, main, footer, section, article, aside, figure, figcaption, audio, source, video, embed
