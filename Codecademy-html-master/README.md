# HTML

๐ HTML (Hypertext Markup Language)   
	- ์น ๋ธ๋ผ์ฐ์  ์์์ ๋ณด์ฌ์ง๋๋ก ๋์์ธ๋ ๋ฌธ์   
	- ํ์คํ๋ Markup Language๋ฅผ ์ด์ฉ

๐ Markup Language
	- ์ผ๋ฐ์ ์ธ text ๋ฌธ์์ Annotating๋ ๊ฒ

	<recipe>
		<title> Peanut-butter On A Spoon </title> 
	</recipe>
	
์ด์ฒ๋ผ tag๋ฅผ ์ด์ฉํ์ฌ ๊ตฌ์กฐ์ ์ผ๋ก ์์ฑํ ๊ฒ์ ์๋ฏธํ๋ค.

------------------------------------------------------
๐ JS Bin   
	- ๊ฐ๋ฐ tool์ pc์ ์ค์นํ์ง ์์๋ ๊ฐ๋จํ๊ฒ ๋์ํ๋ ๊ฒ์ ๋ณผ ์ ์๋ค.
```
<!DOCTYPE html>      	// ๊ด์ต์ ์ผ๋ก tag๋ฅผ ํ๊ธฐ
<html>                  // ๊ฐ์ฅ ์ต์์ tag
	<head>          // icon, ๊ฒ์, css ์ ์. Metadata๋ง ์๋ค.
		  <meta charset="utf-8">
		  <meta name="viewport" content="width=device-width">
	
		  <title>JS Bin</title>
	</head>
	<body>  // ์์๋ถ๋ถ
	
	</body>
</html>
```
	- W3C ์์ ์ ์๋ ๊ท์ ์ ๋ฐ๋ผ ์ด๋ฐ ๊ท์น์ผ๋ก ๋ชจ๋  ๋ธ๋ผ์ฐ์ ์์ ๋์ํ๋ค. (๊ฐํน ๊ทธ๋ ์ง ์์ ๋ธ๋ผ์ฐ์ ๊ฐ ์กด์ฌํ๋ค.)
	Meta charset="utf-8" ํ์กดํ๋ ๋ชจ๋  ์ธ์ด์ ๋ํ ์ ์
	meta name="viewport" content="width=device-width" ์คํฌ๋ฆฐ์ ๋ชจ๋  ๋๋น๋ฅผ ์ด์ฉ

๐ MDN    
	- ์ง์๊ฐ๋ฅํ, ์ ์๋ tag๋ค์ ๋ชจ๋ ํ์ธํ  ์ ์๋ค!   
	- ์ ๋ณด๋ ๊ฐ์ฅ ๋น ๋ฅด๊ฒ ์๋ฐ์ดํธ ๋๊ณ  ์๊ธฐ ๋๋ฌธ์ ๊ผญ!! ์ด์ฉํด๋ณด์   

๐ถ๏ธ short-cut key      
	ol>li*3 ๋ฅผ ์๋ ฅํ๊ณ  tab ํค๋ฅผ ๋๋ฅด๋ฉด ๋ค์๊ณผ ๊ฐ์ด ๋๋ค.
	
   	
	<ol>   		// ol์์ list 3๊ฐ๋ฅผ ๋ง๋ค์ด ๋ฃ๋๋ค.
		<li></li>   
		<li></li>   
		<li></li>   
	
	
	div.container>div.item.item${$}*10๋ฅผ ์๋ ฅํ๊ณ  tab์ ๋๋ฅด๋ฉด ๋ค์๊ณผ ๊ฐ์ด ๋๋ค.
	
	
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
๋๋ฏธ์ฉ text   
	p>lorem ์๋ ฅํ tabํค
		
	p>lorem    
	p>lorem4 // ์ด๋ฐ์์ผ๋ก ๋จ์ด ๊ฐ์ ์กฐ์  ๊ฐ๋ฅ   

* 2021.03.22 html course in Codecademy (chapter1) 
  * body, head, h, p, img, video, title, span, strong, em, vh    
  * vh : ๋ถ๋ชจ์ ํฌ๊ธฐ์ ์๊ด์์ด 100% ์ฌ์ฉํ๊ฒ ๋ค.   

* 2021.03.23 html course in Codecademy (chapter2)
  * !DOCTYPE html, html, table, thead, tbody

* 2021.03.23 html course in Codecademy (chapter3)
  * form, label, input, text, password

* 2021.03.26 html course in Codecademy (chapter4)
  * hr, section, option, number, range(min, max (number)), checkbox, radio 

* 2021.03.27 html course in Codecademy (chapter4)
  * select, datalist, textarea, submit   
  * purpose of a form : users can input information and sent it.   
  * action : form's information์ด ์ด๋๋ก ์ด๋ํ๋์ง ๊ฒฐ์ ํ๋ค.   
  * method : information์ ์ด๋ป๊ฒ ์ฒ๋ฆฌํ๊ณ  ๋ณด๋ผ์ง ๊ฒฐ์ ํ๋ค.   

* 2021.03.27 html course in Codecademy (chapter5)
  * validation, required : you must fill out here. , minlength, maxlength (text), pattern   
  * server-side verification // client-side verification : ์ ๋ณด๋ฅผ ์๋ฒ๋ก ์ ์กํ๊ธฐ ์ ์ ๋ธ๋ผ์ฐ์ ์์ ์ํ

* 2021.03.27 html course in Codecademy (chapter6)
  * semantic vs non-semantic ๋น๊ต!!

* div --> header, nav, main, footer, section, article, aside, figure, figcaption, audio, source, video, embed
