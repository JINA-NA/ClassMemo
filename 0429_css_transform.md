# css

## reset.css에 추가한 속성

```css
table,thead,tbody,tfoot,tr,th,td {border: 1px solid #333; border-spacing: 0; border-collapse: collapse;}

form,fieldset,legend {margin:0; padding:0; border:0; outline:0;}

legend {position: absolute; z-index: -1; width: 0; height: 0; overflow: hidden;}
input[type="text"],
input[type="password"],
input[type="url"],
input[type="email"],
input[type="number"],
input[type="tel"],
input[type="date"],
input[type="datetime"],
input[type="week"],
input[type="month"],
input[type="month"] {border: 1px solid #777; box-sizing:border-box; text-indent: 0.5rem; margin: 0; padding: 0;}

textarea {margin:0; padding:0.5rem; box-sizing: border-box; border: 1px solid #777; }

select {border: 1px solid #777; box-sizing:border-box; margin: 0; padding: 0;}
```

## common.css에 추가한 속성

```css
.full a {display: block; width: 100%; height: 100%; background-repeat: no-repeat; background-position: 0 0;}
.full a>span {display: block; position: absolute; z-index: 0; width: 0; height: 0; overflow: hidden;}

/* table ================ */
.table_style thead {background-color: #acf;}
.table_style tfoot {background-color: #ccc;}
.table_style table {border-left:0; border-right: 0;}
.table_style tr>th:first-child, 
.table_style tr>td:first-child {border-left:0;}
.table_style tr>th:last-child, 
.table_style tr>td:last-child {border-right:0;}
```



**appearance**

브라우저마다 다른 버튼모양 등을 통일시키기 위해 강제적으로 바꾸는 속성



## 속성

**border-radius**

꼭짓점에서 둥글리게 r값을 주는 것. 각각의 모서리 r값을 다르게 설정할 수도 있다.

```css
border-radius : 전체 모서리
border-radius : 상단왼쪽 상단오른쪽 하단오른쪽 하단왼쪽 ;
border-radius-top-left : 상단 왼쪽 모서리
border-radius-top-right
border-radius-bottom-left : 하단 왼쪽 모서리
border-radius-bottom-right
*top,bottom 먼저
```

**box-shadow**,  **text-shadow**

```css

```



**transform**

```css
transform: traslate(100px,200px);
transform: scale(1);
transform: rotate($$deg);
transform: skew();
```

단위

- 이동의 경우, px | rem | % ... 다 적용됨
- 크기변경의 경우, 1==100% , 0.5==50% , 3==300%
-  회전의 경우, deg(각도,degree의 약어). 시계방향으로 돈다.

조건

-  block 요소여야한다. float 속성을 적용했을 경우에는 일부 동작 안 되는 것도 있음.


 축

-   x | y | z


-   대부분의 축은 x축을 기본으로 처리(회전은 z축을 기본으로 한다)

  

**filter**

css-animation(transition, animation)



## 추가 자료

nomalize.css

codepen.io

# js

배열함수, 배열메소드



