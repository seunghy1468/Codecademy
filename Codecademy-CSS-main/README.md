# ๐ฅ CSS

	1. ์ ํ์ (selectors)
		- Universal : *
		- Type : Tag
		- ID : #id
		- Class : .class
		- State : :
		- Attribute : []   
Tag ์์ state๋ attribute๋ฅผ ์ฌ์ฉํ  ์ ์๋ค.  

CSS์ ๊ธฐ๋ณธํํ
--------------
```
/* selector {
  property : value;
} */
```
-----------------------------------------------------
```
/* state slector */
button:hover { 
  color: red;
  background: beige;
}

/* element value */
/* ^๋ฅผ ์ฌ์ฉํ๋ฉด href ์ค์์ naver๋ก ์์ํ๋ ๋ถ๋ถ๋ง ์ ์ฉ */
a[href^="naver"] {
  color : purple;
}

/* $๋ฅผ ์ฌ์ฉํ๋ฉด href ์ค์์ .co.kr๋ก ๋๋๋ ๋ถ๋ถ๋ง ์ ์ฉ */
a[href$=".co.kr"] {
  color : blue;
```

๊ตฌ์ฒด์ ์ผ๋ก ์ค์ ํ๋ฉด ์ฐ์ ์์ ๋๋ค!
```
#special {
  color : pink;
}
/* id๊ฐ special์ธ ๋์ ์ค li๋ง! */
li#special {
  color : purple;
}
```
๐ฅ Display์ Position ์๋ฒฝ ์ดํด ์ค์!!
-----------------------------------
```
/* span์ ๋ด์ฉ์ด ์์ด์ผ ๋์ ๋ณด์ธ๋ค. */
/* display */
div {
  background: red;
  display: inline-block;  
}

span {
  background: blue;
  display: block;
}
/*inline, inline-block, block ๊ตฌ๋ณ ์ค์!*/
```


๋จ, !important ์ฐ์ง ์๋๋ก ํ๋ค.
-------------------------------------------------------
2021.03.30 ~ 2021.04.01 Learn CSS (chapter 1) : Intro to CSS

inline Style : ์์ฑ์ ๋ฐ๊พธ๋ ๊ฐ์ฅ ๋น ๋ฅธ๋ฐฉ๋ฒ. (html code์ ์ถ๊ฐํ๋ ๋ฐฉ๋ฒ)   
-> ์ฌ๋ฌ ์์๋ฅผ ์คํ์ผ๋งํ๋ ค๋ฉด ์ผ์ผํ ์ถ๊ฐํด์ผํ๋ค.

๋ฐ๋์ link ํ์(head์ ์์น, href, type, rel=stylesheet 3์์ ํฌํจ)

multiple classes : class="name1 name2" (HTML)

.name1 {...}, .name2 {...} (CSS)

์ฐ์ ์์ : id > class > ์ผ๋ฐ elements tag, id์ class๋ ์ ์ด ์ฉ๋๊ฐ ๋ค๋ฅด๋ค.

Chaining selectors -> h1.special {} : h1 tag ์ค, special์ด๋ class๊ฐ ์ง์  ๋ ๋์๋ค๋ง ์ ์ฉ

Nested Elements -> .special h5 {} : special class๊ฐ ์ง์ ๋ tag ์์ h5 ์์๋ง 

Multiple selectors -> h5, p {} : h5์ p tag ๋ชจ๋

------------------------------------------------------------

2021.04.02 learn CSS (chapter 2) : elements of CSS

opacity : ํฌ๋ช๋ ์กฐ์ (๋ถํฌ๋ช0~1ํฌ๋ช)

!important : ๋ฌด์ํ  ์ ์๋ค. (๊ฐ์ tag๊ฐ ๊ฐ๊ฐ class, !important๋ก ์ ์ ๋์์ ๊ฒฝ์ฐ, class๋ก ์ ์๋์์ ๊ฒฝ์ฐ์๋ !important๊ฐ ์ ์ธ๋ ์์ฑ์ ๊ฐ์ง๋ค.)

padding: 6px 11px 4px 9px; (top๋ถํฐ ์๊ณ๋ฐฉํฅ์ผ๋ก), padding: 5px 10px; (top, bottom / left, light)

margin : padding๊ณผ ๊ฐ์ rule

resetting defaults : margin์ด๋ padding 0์ผ๋ก ์ค์ (์ด๊ธฐ ๊ฐ ์ฌ์ค์ )

visibility : (hidden, visible ์์ฑ ์ค ์ ํ)

-------------------------------------------------------------
2021.04.03 learn CSS (chapter 3) : box model of CSS

box model์ ์ค์ ํจ์ ์์ด border์ ๋๊ป, margin ๋ฑ์ ๋ฐ๋ผ box model์ ํฌ๊ธฐ๊ฐ ๋ฌ๋ผ์ง๋ค   
(์ ํํ ๊ฐ ์ธก์  ์ด๋ ค์)

width + padding + border = actual rendered width   

box-sizing: border-box; -> ์์ ์น์ ๋ฌธ์  ๋ฐฉ์งํ๋ค   
(tag๋ฅผ * ๋ก ํ๋ฉด ๋ชจ๋  box model์ ์ ์ฉ)

-------------------------------------------------------------
2021.04.03 learn CSS (chapter 4) : display and positioning of CSS

HTML ์์์ ์์น ์ค์  : position, display, z-index, float, clear

position : static(default), relative(default์์ ์ผ๋ง๋ ๋จ์ด์ ธ ์๋์ง   
top, bottom, left, right๋ก ์กฐ์ ), fixed (์คํฌ๋กค์ ๋ด๋ ค๋ ๊ณ ์ ๋ ์ฑ๋ก ์ ์ง)   

z-index : ๋ณด์ด๋ ์์๋ฅผ ์ ํจ (์ ์๋ก ํํ, ์๊ฐ ํด์๋ก ์์ ์์)

inline : ์์๋ง ๋ค์ด๊ฐ ์ ์๋ ๊ณต๊ฐ๋ง์ ์ฐจ์ง.    
block : ์ ๋งํ tag๋ ๋๋ถ๋ถ block์ด๋ค.    
inline-block : widtg์ height์ผ๋ก ์ง์ ๋ ๊ณต๊ฐ์ inline์ผ๋ก ์์๊ฐ ์กด์ฌ.   

float : left or right (์ฌ๋ฌ ์์๋ค์ ๋์ด๊ฐ ๋ค๋ฅด๋ฉด ์์๋ค์ด ๋ถ๋ชํ ์ ์๋ค.)

--------------------------------------------------------------
2021.04.03 learn CSS (chapter5) : color of CSS

foreground(color) vs background(background-color)

color : ๋ช์นญ, hex, rgb

HSL : Hue(์์กฐ), Saturation(์ฑ๋) and lightness(๋ฐ๊ธฐ) + opacity = hsla or rgba ๋ก ์ ์ฉ ๊ฐ๋ฅ(a,b,c,d)

---------------------------------------------------------------
2021.04.05 learn CSS (chapter6) : typography of CSS

typography : ํ์ด์ง์ ํ์คํธ๋ฅผ ๋ฐฐ์ดํ๋ ๊ธฐ์ , ์ธ๋ถ ๋งํฌ๋ฅผ ์ฐ๊ฒฐํ๋ ๋ฒ๋ ๋ค๋ฃฌ๋ค.

font-weight : ๋ช์นญ(normal, bold)๋ ๊ฐ๋ฅํ์ง๋ง 100์ ๋ฐฐ์๋ก ๊ฐ์ค์น๋ฅผ ๋ถ์ฌํ  ์ ์๋ค.   
(100 to 900)

word-spacing : em ๊ฐ๊ฒฉ์ผ๋ก ์ ์ํ๋ ๊ฒ ์ข๋ค. default : 0.25em    
(๊ธ์ ํฌ๊ธฐ์ ๋ฐ๋ผ ์๋์ผ๋ก ๋ฐ๋๊ธฐ ๋๋ฌธ์)

letter-spacing : ์์  ํ๋ํ๋์ ๊ฐ๊ฒฉ์ ์ค์ 

line heghit = font-size(๊ธ์ํฌ๊ธฐ) + leading(์๊ธ์์์ ์ฌ์ด ๊ฐ๊ฒฉ), 1.x ํน์ pixel๋ก ํํ๊ฐ๋ฅ

serif (๊ตด๊ณก์ง ex) times new roman) vs sans-serif (๊ณง๊ณ  ํํ ex) arial)

fallback font : ์ฌ์ฉ์์ ์ปดํจํฐ์ ๊ธ๊ผด์ด ์๋ ๊ฒฝ์ฐ ์ฌ์ฉ

-> h1 {
// h1์ Garamond ์ฌ์ฉ, ๋ง์ฝ ์๋ ๊ฒฝ์ฐ times ์ฌ์ฉ, ๋ ์์ผ๋ฉด ์ฌ์ฉ์ ์ปดํจํฐ์ ์๋ serif ์ฌ์ฉ
  ```
  font-family: "Garamond", "Times", serif;
  ```
}

linking font : ์ํ๋ ๊ธ๊ผด์ href๋ฅผ link tag๋ฅผ ํตํด head tag์ ์ถ๊ฐํ๋ฉด ์ฌ์ฉํ  ์ ์๋ค.   
-> google fonts ์ด์ฉ

font-face : link๋ฅผ ์ฌ์ฉํ์ง ์๊ณ  ์ธ๋ถ ๊ธ๊ผด ์ฌ์ฉ ๊ฐ๋ฅ

--> ์ ์ฌ์ฉ ์ํ๋๊ฒ ์ข๋ค.. ๊ทธ๋ฌ๋ font-face๋ฅผ ์์ ํ์ฌ ๋ก์ปฌ์ฒ๋ผ ์ฌ์ฉํ  ์ ์๋ค.

```
@font-face {
  src: url("relative-path") format('format');
}
```

-----------------------------------------------------------
2021.04.05 ~ 2021.04.08 learn of CSS (chapter 7) : flexbox of CSS

flexbox : ๊ฐ๋ณ ๋๋ ๊ทธ๋ฃน์ผ๋ก element๋ฅผ ๋ฐฐ์นํ๋ ๋ฐ ์ฉ์ด.   
์ฆ ์์์ ์์น๋ฅผ ์กฐ์ ํ๋๋ฐ ์์ฃผ ์ฌ์ด ๋ฐฉ๋ฒ! (1์ฐจ์์์ ์์๋ฅผ ์ ๋ ฌํ  ๋ ์ ์ฉํจ)    
flexbox -> flex containers (item์ด ํฌํจ๋ page์ element) , flex items

display: flex; -> ์์๋ฅผ block level container ์์ flex items๊ฐ ์๋ ์ํ๋ก ๋ฃ๋๋ค.

inilne-flex : ํ๋์ ์ค์ ์ฌ๋ฌ๊ฐ์ ์์๋ฅผ ๋ฐฐ์ดํ๋ค.    
(container width๊ฐ ์ ํด์ ธ ์๋ ๊ฒฝ์ฐ, ๊ทธ ์์ child๋ container width๋ฅผ ๋์ ์ ์๋ค.)

justify-content : ์ฃผ ์ถ์ ๋ฐ๋ผ ๋์์ ๋ฐฐ์ด  
(flex-start : ์์ container์ ์ผ์ชฝ๋ถํฐ ์ค๋ฅธ์ชฝ์ผ๋ก ์ฐจ๋ก๋๋ก ๋ฐฐ์ด.   
flex-end, center, space-around (์์์ฌ์ด์ ๋์ผํ ๊ณต๊ฐ๋งํผ ๋์์ ธ ๋ฐฐ์ด)    
space-between (space-around์ ๊ฐ์ผ๋, ์ฒซ ์์ ์์ด๋ ๋ง์ง๋ง ์์ ๋ค์๋ ๊ณต๊ฐ ์กด์ฌ x)

align-items : ์์ง์ผ๋ก ๋ฐฐ์ดํ๋๋ก ํ๋ค.  
(baseline: ์์๋์ ์ผ์ ํ ๊ฐ๊ฒฉ์ผ๋ก ๋ฐฐ์ด๋จ    
flex-start : ๋งจ ์์ ๋ฐฐ์ด๋จ    
flex-end : ๋งจ ๋์ ๋ฐฐ์ด๋จ   
center : ๊ฐ์ด๋ฐ์ ๋ฐฐ์ด๋จ       
stretch : ์์๋๋ก ๋ชจ๋ ๊ณต๊ฐ ์ฐจ์งํ๋ฉฐ )

flex-grow : ์์์ ํฌ๊ธฐ๋ฅผ container์ ๋ง๊ฒ ์กฐ์  ๊ฐ๋ฅํ๋ค.     
(์ ์๋ก ํํ ex)    
```
flex-grow: 1; 
```
container๊ฐ ๋งค์ฐ ํด ๋, ์์์ ํฌ๊ธฐ๋ฅผ ํค์ธ ๋ ์ฌ์ฉ)   
-> ๊ธฐ๋ณธ ๊ฐ : 0

flex-shrink : ์์์ ํฌ๊ธฐ๋ฅผ flex-grow์ ๋ง์ฐฌ๊ฐ์ง๋ก ์กฐ์  ๊ฐ๋ฅํ๋ค.     
container๊ฐ ๋งค์ฐ ์์ ๋, ์์์ ํฌ๊ธฐ๋ฅผ ์ค์ผ ๋ ์ฌ์ฉํ๋ค.    
-> ๊ธฐ๋ณธ ๊ฐ : 1

flex-basis : flex ํญ๋ชฉ์ ๋๋น๋ฅผ ์กฐ์ ํ๋ ๋ฐฉ๋ฒ. pixel ๋จ์๋ก ์กฐ์ 

flex : (flex-grow, flex-shrink, flex-basis) ์ธ ๊ฐ์ง๋ฅผ ํ๊บผ๋ฒ์ ์ ์ ๊ฐ๋ฅ.    
-> flex: 2 1 150px; ์ด๋ฐ์์ผ๋ก ์ฌ์ฉํ  ์ ์๋ค.

flex: 2 150px; -> ์ด๋ฐ์์ผ๋ก ์ ์ํ๋ฉด, flex-shrink ์์ฑ์ x

flex-wrap : ์์๊ฐ container์ ๋ง๊ฒ ์ถ์๋์ง ์๊ณ  ๋ค์ ํ์ผ๋ก ์ด๋์ํฌ ๋ ์ฌ์ฉ  
(wrap : ๋ค์ ์ค๋ก ์ด๋, wrap-reverse : wrap๊ณผ ๊ฐ์ง๋ง ํ์ ์์๊ฐ ๋ค๋ฐ๋, nowrap)

align-content : ์ฌ๋ฌ ํ์ด ์๋ ๊ฒฝ์ฐ, ํ์ ์์ชฝ๊ณผ ์๋์ชฝ์ ๋์ธ ์ ์๋ค.    
(flex-start, flex-end, center, space-between, space-around, stretch)

flex-direction : ์์๋ฅผ ํ ๋๋ ์ด๋ก ๋ฐฐ์ด ๊ฐ๋ฅํ๋๋ก ํ๋ค.  
(row, row-reverse, column, column-reverse)

flex-flow : flex-wrap, flex-direction ์์ฑ์ ํ์ค๋ก ์ ์ธํ  ๋ ์ฌ์ฉ    
-> flex-flow: column wrap; ์ด๋ฐ์์ผ๋ก ์ฌ์ฉ๋๋ค. (์๋ ฅ ์์ ์๊ด x)

flex container๋ค์ display: flex or display: inline-flex์ ์ค์ฒฉ์ด ์ ์ธํ  ์ ์๋ค.

```
align-content๋ ์ฌ๋ฌ ์ค๋ค ์ฌ์ด์ ๊ฐ๊ฒฉ์ ์ง์ ํ๋ฉฐ, 
align-items๋ ์ปจํ์ด๋ ์์์ ์ด๋ป๊ฒ ๋ชจ๋  ์์๋ค์ด ์ ๋ ฌํ๋์ง๋ฅผ ์ง์ ํ๋ค.
ํ ์ค๋ง ์๋ ๊ฒฝ์ฐ, align-content๋ ํจ๊ณผ x
๋ฐ๋์ ๋น๊ตํ  ์ ์์ด์ผ ํ๋ค.

-------------------------------------------------------------------------
2021.04.09~2021.04.12 learn of CSS (chapter 8) : CSS Grid

CSS Grid : 2์ฐจ์ ๋ ์ด์์์ ๊ฐ์ฅ ์ ์ฉํ๋ค.    
(ํ๊ณผ ์ด์ ๊ฑธ์ณ ์์๋ฅผ ์ ๋ ฌํ๊ณ  ์ด๋ํ  ๋ ๋ง์ ๋๊ตฌ ์ ๊ณต)

grid๋ฅผ ๋ง๋ค๋ ค๋ฉด, grid container์ grid items๊ฐ ํ์ํ๋ค.   
display๋ฅผ grid or inline-grid๋ก ์ค์ .

grid-template-columns : grid์ ์ด ์ ์.    
-> grid-template-columns: 100px 50% 200px; ์ด๋ฐ์์ผ๋ก ๋ฐฑ๋ถ์จ๋ก๋ ์ธ ์ ์๋ค. 

grid-template-rows : grid์ ํ ์ ์. ์์ ๊ฐ์ด columns ์ฒ๋ผ ์ธ ์ ์๋ค.

grid-template : columns์ rows ๋ฅผ ๋์ฒดํ  ์ ์๋ค.    
-> grid-template: 200px 300px (ํ) / 20% 10% 70% (์ด); (grid ๊ฒฝ๊ณ ๋์ด๊ฐ ์ ์๋ค.)

gird-template๋ฅผ fr ์ด๋ ๋จ์๋ก๋ ์ธ ์ ์๋ค!    
(๋ถ์์ ๊ฐ๋. grid ๊ฒฝ๊ณ์ ๋ง๊ฒ ๋๋์ด์ง๋ค.)
```
grid-template: 1fr 1fr 1fr / 3fr 50% 1fr;
```

repeat : ๋ฐ๋ณตํด์ ์์๋ฅผ ๋ฐฐ์ดํ  ์ ์๋ค.    
```
grid-template-columns: repeat(3, 100px); 
// 100px ์ง๋ฆฌ 3๊ฐ ์ด๋ก ๋ฐฐ์ด.     
```
(repeat(2, 100px 20px); 2๊ฐ์ value ์ค์  ๊ฐ๋ฅ-> 100 20 100 20px)

minmax : ์ ์ฒด grid ํฌ๊ธฐ์ ๋ฐ๋ผ ํฌ๊ธฐ๊ฐ ๋ฌ๋ผ์ง๋ค.    
```
minmax(100px, 300px); 
// 100px์์ 300px 
```
grid-gap : grid ์์ '์ฌ์ด'์ margin์ ์ค๋ค.   
(์์๊ณผ ๋์ margin์ ์ฃผ์ง ์๋๋ค.)         
-> grid-column-gap: 10px; : '์ด' ์ margin์ 10px ๋งํผ ์ฝ์

-> grid-gap: 20px 10px; : ์ด๋ ๊ฒ ์ฌ์ฉ ๊ฐ๋ฅ. (20px : ํ, 10px : ์ด) 

grid-row-start / grid-row-end : ์์์ ํ์ ๋ช ๋ฒ์งธ๋ถํฐ ์์ํ๊ณ  ๋๋ผ ๊ฒ์ธ์ง ๊ฒฐ์     
(end๋ ๋ฒ์ ํฌํจ x)

```
grid-row-start: 2; grid-row-end: 4; 
//grid์ row๊ฐ 2ํ๋ถํฐ 3ํ๊น์ง

grid-row: 2 / 4; 
//์์ ๊ฐ์ ์ญํ 
```
grid-column-start / grid-column-end : ์์์ ์ด์ ๋ช ๋ฒ์งธ๋ถํฐ ์์ํ๊ณ  ๋๋ผ ๊ฒ์ธ์ง ๊ฒฐ์     
(end๋ ๋ฒ์ ํฌํจ x) 

-> grid-column: 4 / span 2; : grid์ column์ด 4๋ถํฐ 5๊น์ง ๋ ์ด(span 2)์ ๊ณต๊ฐ ์ฐจ์ง    
(span์ ์ฌ์ฉํ๋ฉด off-by-one error๋ฅผ ๋ง์ ์ ์๋ค. : grid line์ ๋์ ์๋ชป ๊ณ์ฐํ๋ error)

grid-area : row-start / column-start / row-end / column-end; ์ด๋ ๊ฒ ์ฌ์ฉ.    
(grid-row์ grid-column์ ํฉ์น ๊ฒ)

```
grid-area: 2 / 2 / span 3 / span 6; 
//2ํ๋ถํฐ 4ํ๊น์ง, 2์ด๋ถํฐ 8์ด๊น์ง grid ๋ฒ์
```
----------------------------------------------------------------
2021.04.12 learn of CSS (chapter 9) : CSS Grid additional property

grid-template-areas : grid-row-start, grid-row-end, grid-col-start,grid-col-end, and grid-area value์ section ์ด๋ฆ์ ์ง์ ํ  ์ ์๋ค.

justify-items : start, end, center, stretch    
(row axis์ column axis์ ๋ํ ์ ์ ์ค์. ํนํ ์๋ row axis์ ๋ง๊ฒ grid ํญ๋ชฉ์ ๋ฐฐ์นํ๋ค)

justify-content : start, end, center, stretch, space-around, space-between, space-evenly    
(์ ์ฒด grid๋ฅผ row axis๋ฅผ ๋ฐ๋ผ ๋ฐฐ์นํ  ์ ์๋ค.)

-> stretch grid์ height์ด ๋์ผํ๊ฒ ์ ์ง๋๋ค.

justify-self : start, end, center, stretch    
(ํ ์ถ์ ๋ํด ๊ฐ๋ณ grid ์์น ์ง์ )

align-items : start, end, center, stretch     
(์ ์ฒด grid๋ฅผ column axis์ ๋ฐ๋ผ ๋ฐฐ์นํ๋๋ก ํ๋ค.)

align-content : start, end, center, stretch, space-around, space-between, space-evenly     
(column axis์ ๋ฐ๋ผ ์์์ ์๋๋ก ๋ฐฐ์นํ๋ค.)

align-self : start, end, center, stretch     
(์ด ์ถ์ ๋ํด ๊ฐ๋ณ grid ์์น ์ง์ )

implicit vs explicit grid

-> ํ์ผํ๊ณผ ๊ฐ์ web์ ๊ฒฝ์ฐ, ์์ดํ์ ๊ฒ์์ฐฝ์ ์๋ ฅํ  ๋,    
์ฐ๋ฆฌ๊ฐ ์ผ๋ง๋ ๋ง์ ์ ๋ณด๋ฅผ ํ์ํ  ์ง ๋ชจ๋ฅด๋ ๊ฒฝ์ฐ๊ฐ ๋ง๋ค.

-> ์๋ฅผ ๋ค์ด, ๊ฐ๋ฐ์๊ฐ 3์ด 5ํ์ grid๋ฅผ ์ง์ ํ์ ๋,    
๊ฒ์ ๊ฒฐ๊ณผ๊ฐ 30๊ฐ์ ์์ดํ์ ๋ฐํํ๋ฉด?

-> implicit grid๊ฐ ๊ทธ ์๋ฆฌ๋ฅผ ์ฐจ์งํ๋ค.

grid-auto-rows : implicit grid์ ํฌ๊ธฐ๋ฅผ ์ค์ ํ๋ค.    
(ํ) grid-template-rows์ ๊ฐ์ ์์ฑ์ ์ ์ํด์ ์ค์ ํ๋ค. (px, %, fr, repeat)

grid-auto-columns :implicit grid์ ํฌ๊ธฐ๋ฅผ ์ค์ ํ๋ค. (์ด)

grid-auto-flow : row, column, dense     
(ํ์ด ๋๋๋ง ๋๋ ์์๋ฅผ ์ง์ ํ  ์ ์๋ค. dense์ ๊ฒฝ์ฐ, row๋ column๊ณผ ๊ฐ์ด ์ธ ์ ์๋ค.)

-----------------------------------------------------------------
2021.04.16 learn of CSS (chapter 3 added)

[href]{color: magenta;} ์ด๋ ๊ฒ attribute๋ฅผ ์ค์ ํ  ์ ์๋ค.     
(tag, class, id์ ๊ฐ์ด ์ค์  ๊ฐ๋ฅํ๋ค)

```
a[href*='beijing'] {
	color: lightblue;
	}
```
์ด๋ ๊ฒ ํน์  href๋ง ๊ฐ์ง๊ณ  ์๋ ๋์์ ์ค์ ์ ๋ฐ๊ฟ ์ ์๋ค.

Pseudo-class : ์ฌ์ฉ์๊ฐ ํด๋น ์์๋ฅผ ํ์ฑํ ํ๊ฑฐ๋ ์ํธ์์ฉ์ ํ๋ฉด ๊ทธ ์์๊ฐ ๋ณํํ๋ ์๋์ ํ๊ฒ ํ๋ค.

-> :hover, :focus, :visited, :disabled, :active ๋ฑ์ด ์๋ค.

------------------------------------------------------------------
2021.04.19 learn of CSS (chapter 10) : CSS transition

-> ์๊ฐ์ ์ธ ๋ณํ ๋ถ๋ถ์ ๋ค๋ฃฌ๋ค!!    
(์๋ฅผ ๋ค์ด, ๋ฒํผ ์์ ๋ง์ฐ์ค๋ฅผ ์ฌ๋ ค ๋์ผ๋ฉด ์์ด ๋ณํ๋ ๋ฑ)

transition-property: color; (๋ณํํ  ์์ฑ)

transition-duration: 1s; (๋ณํํ๋ ๋ฐ ๊ฑธ๋ฆฌ๋ ์๊ฐ)

transition-timing-function : ease-in (์ฒ์์ ์ฒ์ฒํ, ๋์ค์ ๋น ๋ฅด๊ฒ), ease-out, ease-in-out, linear (์ ํ ์๋๋ฅผ ์ค์ ํ๋ค.)

transition-delay : ๋ณํํ๊ธฐ ์ , ์ ๊น ๋ฉ์ถ๋ ์๊ฐ

transition : ์ 4๊ฐ์ง ์์ฑ์ ํญ์ ๊ฐ์ด ๋ค๋๋ ๊ฒฝ์ฐ๊ฐ ๋ง์ผ๋ฏ๋ก, ํ๋ฒ์ ํํ ๊ฐ๋ฅํ๋ค. (์์ ์ค์! ์์ ์์๋๋ก์    
(property, duration, timing, delay))

transition: color 1s linear, font-size 750ms ease-in 100ms;      
-> ๋ ์์ฑ์ ๋์์ ๋ณํ. 1์ด๋์ ๋ณํ, ๋๋จธ์ง ์์ฑ๋ค..

transition: all 750ms ease-in 100ms;     
-> all ์ด๋ ์์ฑ์ ์ด์ฉํด์ ์ ์ฉํ  ์ ์๋ ๋ชจ๋  ์์ฑ์ ํน์ฑ์ ๋์ผํ๊ฒ ์ค์ ํ๋ค.

------------------------------------------------------------------------
2021.04.25 learn of CSS (chapter 11) : Relative Measurements

->  ํ๋ฉด ํฌ๊ธฐ(ํ๋ธ๋ฆฟ, ์ค๋งํธํฐ, pc ๋ฑ)์ ์๊ด์์ด ์ปจํ์ธ ๋ฅผ ๋ณผ ์ ์์๊น?
```
background-image: url('camel-background.png');  // ๋ฐฐ๊ฒฝ ์ด๋ฏธ์ง ์ค์ 

background-position: center;                    // ์ด๋ฏธ์ง๋ฅผ ์์ ์ค์ฌ์ ๋ง์ถ๋ค.
  
background-size: cover;                         // ์์์ด ์์ ํฌ๊ธฐ๋ฅผ ์ด๊ณผํ๋ฉด ์ด๊ณผํ์ง ์๋ ๋ฒ์๋ง 
  
background-repeat: no-repeat;                   // ์ปดํ์ผ๋ฌ๊ฐ ์ด๋ฏธ์ง๋ฅผ ๋ฐ๋ณตํ์ง ์๊ฒ ํ๋ค.
```
-------------------------------------------------------------------------
2021.05.04 learn of CSS (chapter 12) : Relative Web Design

media queries : ์น ์ฌ์ดํธ์ ์ปจํ์ธ ๋ฅผ ๋ค๋ฅธํ๋ฉด ํฌ๊ธฐ์ ๋ง๊ฒ ์กฐ์      
-> ํ์ฌ ํ๋ฉด์ ํฌ๊ธฐ๋ฅผ ๊ฐ์ง, ํ๋ฉด ๋๋น์ ๋ฐ๋ผ ๋ค๋ฅธ CSS ์คํ์ผ ์กฐ์ 

```
@media only screen and (max-width: 480px) {
  body {
    font-size: 12px;
  }
}

// 480pixel ๋ณด๋ค ์์ ํ๋ฉด์ ๋ํ ์ ์(๋๋ต์ ์ธ ์ค๋งํธํฐ์ ๊ฐ๋ก ๊ธธ์ด)
```
