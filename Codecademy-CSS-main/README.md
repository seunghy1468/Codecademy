# 🥔 CSS

	1. 선택자 (selectors)
		- Universal : *
		- Type : Tag
		- ID : #id
		- Class : .class
		- State : :
		- Attribute : []   
Tag 옆에 state나 attribute를 사용할 수 있다.  

CSS의 기본형태
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
/* ^를 사용하면 href 중에서 naver로 시작하는 부분만 적용 */
a[href^="naver"] {
  color : purple;
}

/* $를 사용하면 href 중에서 .co.kr로 끝나는 부분만 적용 */
a[href$=".co.kr"] {
  color : blue;
```

구체적으로 설정하면 우선순위 높다!
```
#special {
  color : pink;
}
/* id가 special인 녀석 중 li만! */
li#special {
  color : purple;
}
```
🥑 Display와 Position 완벽 이해 중요!!
-----------------------------------
```
/* span은 내용이 있어야 눈에 보인다. */
/* display */
div {
  background: red;
  display: inline-block;  
}

span {
  background: blue;
  display: block;
}
/*inline, inline-block, block 구별 중요!*/
```


단, !important 쓰지 않도록 한다.
-------------------------------------------------------
2021.03.30 ~ 2021.04.01 Learn CSS (chapter 1) : Intro to CSS

inline Style : 속성을 바꾸는 가장 빠른방법. (html code에 추가하는 방법)   
-> 여러 요소를 스타일링하려면 일일히 추가해야한다.

반드시 link 필요(head에 위치, href, type, rel=stylesheet 3요소 포함)

multiple classes : class="name1 name2" (HTML)

.name1 {...}, .name2 {...} (CSS)

우선순위 : id > class > 일반 elements tag, id와 class는 애초 용도가 다르다.

Chaining selectors -> h1.special {} : h1 tag 중, special이란 class가 지정 된 녀석들만 적용

Nested Elements -> .special h5 {} : special class가 지정된 tag 안에 h5 요소만 

Multiple selectors -> h5, p {} : h5와 p tag 모두

------------------------------------------------------------

2021.04.02 learn CSS (chapter 2) : elements of CSS

opacity : 투명도 조절(불투명0~1투명)

!important : 무시할 수 없다. (같은 tag가 각각 class, !important로 정의 되었을 경우, class로 정의되었을 경우에도 !important가 선언된 속성을 가진다.)

padding: 6px 11px 4px 9px; (top부터 시계방향으로), padding: 5px 10px; (top, bottom / left, light)

margin : padding과 같은 rule

resetting defaults : margin이랑 padding 0으로 설정(초기 값 재설정)

visibility : (hidden, visible 속성 중 선택)

-------------------------------------------------------------
2021.04.03 learn CSS (chapter 3) : box model of CSS

box model을 설정함에 있어 border의 두께, margin 등에 따라 box model의 크기가 달라진다   
(정확한 값 측정 어려움)

width + padding + border = actual rendered width   

box-sizing: border-box; -> 앞의 치수 문제 방지한다   
(tag를 * 로 하면 모든 box model에 적용)

-------------------------------------------------------------
2021.04.03 learn CSS (chapter 4) : display and positioning of CSS

HTML 요소의 위치 설정 : position, display, z-index, float, clear

position : static(default), relative(default에서 얼마나 떨어져 있는지   
top, bottom, left, right로 조절), fixed (스크롤을 내려도 고정된 채로 유지)   

z-index : 보이는 순서를 정함 (정수로 표현, 수가 클수록 앞에 있음)

inline : 요소만 들어갈 수 있는 공간만을 차지.    
block : 왠만한 tag는 대부분 block이다.    
inline-block : widtg와 height으로 지정된 공간에 inline으로 요소가 존재.   

float : left or right (여러 요소들의 높이가 다르면 요소들이 부딪힐 수 있다.)

--------------------------------------------------------------
2021.04.03 learn CSS (chapter5) : color of CSS

foreground(color) vs background(background-color)

color : 명칭, hex, rgb

HSL : Hue(색조), Saturation(채도) and lightness(밝기) + opacity = hsla or rgba 로 적용 가능(a,b,c,d)

---------------------------------------------------------------
2021.04.05 learn CSS (chapter6) : typography of CSS

typography : 페이지에 텍스트를 배열하는 기술, 외부 링크를 연결하는 법도 다룬다.

font-weight : 명칭(normal, bold)도 가능하지만 100의 배수로 가중치를 부여할 수 있다.   
(100 to 900)

word-spacing : em 간격으로 정의하는 게 좋다. default : 0.25em    
(글의 크기에 따라 자동으로 바뀌기 때문에)

letter-spacing : 음절 하나하나의 간격을 설정

line heghit = font-size(글자크기) + leading(위글자와의 사이 간격), 1.x 혹은 pixel로 표현가능

serif (굴곡짐 ex) times new roman) vs sans-serif (곧고 평평 ex) arial)

fallback font : 사용자의 컴퓨터에 글꼴이 없는 경우 사용

-> h1 {
// h1에 Garamond 사용, 만약 없는 경우 times 사용, 또 없으면 사용자 컴퓨터에 있는 serif 사용
  ```
  font-family: "Garamond", "Times", serif;
  ```
}

linking font : 원하는 글꼴의 href를 link tag를 통해 head tag에 추가하면 사용할 수 있다.   
-> google fonts 이용

font-face : link를 사용하지 않고 외부 글꼴 사용 가능

--> 잘 사용 안하는게 좋다.. 그러나 font-face를 수정하여 로컬처럼 사용할 수 있다.

```
@font-face {
  src: url("relative-path") format('format');
}
```

-----------------------------------------------------------
2021.04.05 ~ 2021.04.08 learn of CSS (chapter 7) : flexbox of CSS

flexbox : 개별 또는 그룹으로 element를 배치하는 데 용이.   
즉 요소의 위치를 조정하는데 아주 쉬운 방법! (1차원에서 요소를 정렬할 때 유용함)    
flexbox -> flex containers (item이 포함된 page의 element) , flex items

display: flex; -> 요소를 block level container 안에 flex items가 있는 상태로 넣는다.

inilne-flex : 하나의 줄에 여러개의 요소를 배열한다.    
(container width가 정해져 있는 경우, 그 안의 child는 container width를 넘을 수 없다.)

justify-content : 주 축을 따라 띄워서 배열  
(flex-start : 상위 container의 왼쪽부터 오른쪽으로 차례대로 배열.   
flex-end, center, space-around (요소사이에 동일한 공간만큼 띄워져 배열)    
space-between (space-around와 같으나, 첫 요소 앞이나 마지막 요소 뒤에는 공간 존재 x)

align-items : 수직으로 배열하도록 한다.  
(baseline: 위아래에 일정한 간격으로 배열됨    
flex-start : 맨 위에 배열됨    
flex-end : 맨 끝에 배열됨   
center : 가운데에 배열됨       
stretch : 위아래로 모든공간 차지하며 )

flex-grow : 요소의 크기를 container에 맞게 조절 가능하다.     
(정수로 표현 ex)    
```
flex-grow: 1; 
```
container가 매우 클 때, 요소의 크기를 키울 때 사용)   
-> 기본 값 : 0

flex-shrink : 요소의 크기를 flex-grow와 마찬가지로 조절 가능하다.     
container가 매우 작을 때, 요소의 크기를 줄일 때 사용한다.    
-> 기본 값 : 1

flex-basis : flex 항목의 너비를 조정하는 방법. pixel 단위로 조정

flex : (flex-grow, flex-shrink, flex-basis) 세 가지를 한꺼번에 정의 가능.    
-> flex: 2 1 150px; 이런식으로 사용할 수 있다.

flex: 2 150px; -> 이런식으로 정의하면, flex-shrink 속성은 x

flex-wrap : 요소가 container에 맞게 축소되지 않고 다음 행으로 이동시킬 때 사용  
(wrap : 다음 줄로 이동, wrap-reverse : wrap과 같지만 행의 순서가 뒤바뀜, nowrap)

align-content : 여러 행이 있는 경우, 행의 위쪽과 아래쪽을 띄울 수 있다.    
(flex-start, flex-end, center, space-between, space-around, stretch)

flex-direction : 요소를 행 또는 열로 배열 가능하도록 한다.  
(row, row-reverse, column, column-reverse)

flex-flow : flex-wrap, flex-direction 속성을 한줄로 선언할 때 사용    
-> flex-flow: column wrap; 이런식으로 사용된다. (입력 순서 상관 x)

flex container들은 display: flex or display: inline-flex을 중첩어 선언할 수 있다.

```
align-content는 여러 줄들 사이의 간격을 지정하며, 
align-items는 컨테이너 안에서 어떻게 모든 요소들이 정렬하는지를 지정한다.
한 줄만 있는 경우, align-content는 효과 x
반드시 비교할 수 있어야 한다.

-------------------------------------------------------------------------
2021.04.09~2021.04.12 learn of CSS (chapter 8) : CSS Grid

CSS Grid : 2차원 레이아웃에 가장 유용하다.    
(행과 열에 걸쳐 요소를 정렬하고 이동할 때 많은 도구 제공)

grid를 만들려면, grid container와 grid items가 필요하다.   
display를 grid or inline-grid로 설정.

grid-template-columns : grid의 열 정의.    
-> grid-template-columns: 100px 50% 200px; 이런식으로 백분율로도 쓸 수 있다. 

grid-template-rows : grid의 행 정의. 위와 같이 columns 처럼 쓸 수 있다.

grid-template : columns와 rows 를 대체할 수 있다.    
-> grid-template: 200px 300px (행) / 20% 10% 70% (열); (grid 경계 넘어갈 수 있다.)

gird-template를 fr 이란 단위로도 쓸 수 있다!    
(분수의 개념. grid 경계에 맞게 나누어진다.)
```
grid-template: 1fr 1fr 1fr / 3fr 50% 1fr;
```

repeat : 반복해서 요소를 배열할 수 있다.    
```
grid-template-columns: repeat(3, 100px); 
// 100px 짜리 3개 열로 배열.     
```
(repeat(2, 100px 20px); 2개의 value 설정 가능-> 100 20 100 20px)

minmax : 전체 grid 크기에 따라 크기가 달라진다.    
```
minmax(100px, 300px); 
// 100px에서 300px 
```
grid-gap : grid 요소 '사이'에 margin을 준다.   
(시작과 끝에 margin을 주지 않는다.)         
-> grid-column-gap: 10px; : '열' 에 margin을 10px 만큼 삽입

-> grid-gap: 20px 10px; : 이렇게 사용 가능. (20px : 행, 10px : 열) 

grid-row-start / grid-row-end : 요소의 행을 몇 번째부터 시작하고 끝낼 것인지 결정    
(end는 범위 포함 x)

```
grid-row-start: 2; grid-row-end: 4; 
//grid의 row가 2행부터 3행까지

grid-row: 2 / 4; 
//위와 같은 역할
```
grid-column-start / grid-column-end : 요소의 열을 몇 번째부터 시작하고 끝낼 것인지 결정    
(end는 범위 포함 x) 

-> grid-column: 4 / span 2; : grid의 column이 4부터 5까지 두 열(span 2)의 공간 차지    
(span을 사용하면 off-by-one error를 막을 수 있다. : grid line의 끝을 잘못 계산하는 error)

grid-area : row-start / column-start / row-end / column-end; 이렇게 사용.    
(grid-row와 grid-column을 합친 것)

```
grid-area: 2 / 2 / span 3 / span 6; 
//2행부터 4행까지, 2열부터 8열까지 grid 범위
```
----------------------------------------------------------------
2021.04.12 learn of CSS (chapter 9) : CSS Grid additional property

grid-template-areas : grid-row-start, grid-row-end, grid-col-start,grid-col-end, and grid-area value의 section 이름을 지정할 수 있다.

justify-items : start, end, center, stretch    
(row axis와 column axis에 대한 정의 중요. 특히 얘는 row axis에 맞게 grid 항목을 배치한다)

justify-content : start, end, center, stretch, space-around, space-between, space-evenly    
(전체 grid를 row axis를 따라 배치할 수 있다.)

-> stretch grid의 height이 동일하게 유지된다.

justify-self : start, end, center, stretch    
(행 축에 대해 개별 grid 위치 지정)

align-items : start, end, center, stretch     
(전체 grid를 column axis에 따라 배치하도록 한다.)

align-content : start, end, center, stretch, space-around, space-between, space-evenly     
(column axis에 따라 위에서 아래로 배치한다.)

align-self : start, end, center, stretch     
(열 축에 대해 개별 grid 위치 지정)

implicit vs explicit grid

-> 홈쇼핑과 같은 web의 경우, 아이템을 검색창에 입력할 때,    
우리가 얼마나 많은 정보를 표시할 지 모르는 경우가 많다.

-> 예를 들어, 개발자가 3열 5행의 grid를 지정했을 때,    
검색 결과가 30개의 아이템을 반환하면?

-> implicit grid가 그 자리를 차지한다.

grid-auto-rows : implicit grid의 크기를 설정한다.    
(행) grid-template-rows와 같은 속성을 정의해서 설정한다. (px, %, fr, repeat)

grid-auto-columns :implicit grid의 크기를 설정한다. (열)

grid-auto-flow : row, column, dense     
(행이 랜더링 되는 순서를 지정할 수 있다. dense의 경우, row나 column과 같이 쓸 수 있다.)

-----------------------------------------------------------------
2021.04.16 learn of CSS (chapter 3 added)

[href]{color: magenta;} 이렇게 attribute를 설정할 수 있다.     
(tag, class, id와 같이 설정 가능하다)

```
a[href*='beijing'] {
	color: lightblue;
	}
```
이렇게 특정 href만 가지고 있는 녀석의 설정을 바꿀 수 있다.

Pseudo-class : 사용자가 해당 요소를 활성화 하거나 상호작용을 하면 그 요소가 변화하는 작동을 하게 한다.

-> :hover, :focus, :visited, :disabled, :active 등이 있다.

------------------------------------------------------------------
2021.04.19 learn of CSS (chapter 10) : CSS transition

-> 시각적인 변화 부분을 다룬다!!    
(예를 들어, 버튼 위에 마우스를 올려 놓으면 색이 변하는 등)

transition-property: color; (변환할 속성)

transition-duration: 1s; (변환하는 데 걸리는 시간)

transition-timing-function : ease-in (처음은 천천히, 나중은 빠르게), ease-out, ease-in-out, linear (전환 속도를 설정한다.)

transition-delay : 변화하기 전, 잠깐 멈추는 시간

transition : 위 4가지 속성은 항상 같이 다니는 경우가 많으므로, 한번에 표현 가능하다. (순서 중요! 위의 순서대로임    
(property, duration, timing, delay))

transition: color 1s linear, font-size 750ms ease-in 100ms;      
-> 두 속성을 동시에 변환. 1초동안 변환, 나머지 속성들..

transition: all 750ms ease-in 100ms;     
-> all 이란 속성을 이용해서 적용할 수 있는 모든 속성의 특성을 동일하게 설정한다.

------------------------------------------------------------------------
2021.04.25 learn of CSS (chapter 11) : Relative Measurements

->  화면 크기(태블릿, 스마트폰, pc 등)에 상관없이 컨텐츠를 볼 수 있을까?
```
background-image: url('camel-background.png');  // 배경 이미지 설정

background-position: center;                    // 이미지를 요소 중심에 맞춘다.
  
background-size: cover;                         // 영상이 요소 크기를 초과하면 초과하지 않는 범위만 
  
background-repeat: no-repeat;                   // 컴파일러가 이미지를 반복하지 않게 한다.
```
-------------------------------------------------------------------------
2021.05.04 learn of CSS (chapter 12) : Relative Web Design

media queries : 웹 사이트의 컨텐츠를 다른화면 크기에 맞게 조정     
-> 현재 화면의 크기를 감지, 화면 너비에 따라 다른 CSS 스타일 조정

```
@media only screen and (max-width: 480px) {
  body {
    font-size: 12px;
  }
}

// 480pixel 보다 작은 화면에 대한 정의(대략적인 스마트폰의 가로 길이)
```
