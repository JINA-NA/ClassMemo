# 1. layout짜기 

## layout 짜기

- 실습 파일명: a_basic_layout_01.html



```height: auto;```   하위로 따라오는 자식들의 내용의 길이에 따라서 자동으로 늘어나거나 줄어듦.

```min-height``` 최소 높이값

```max-height```  최대 높이값



---

### 웹에서 쓰는 단위

px, %, em, vem, vw, vh, pc ...

em : 1em=16px

pt : 웹에서는 잘 쓰지않는 개념. 
		일러/포샵 같은 그래픽 프로그램에서는 12pt=12px(동일한 값이다)
		웹에서는 16px=12pt

---

### inline  vs  block

**inline** : 
크기값이 없다. 줄바꿈 없다. 여백 없다. a, span, input, label, select

**block **: 
크기값 있다. 줄바꿈 있다. 여백있다. ul, ol, li, h1~6, p, form 

*inline은 반드시 block 태그 안에 담겨져야 한다.*



### 자손선택자  vs   자식선택자

**자손선택자** :   #box

**자식선택자** :   #box > ul > li        -> 쉽게 생각하면 바로 위의 부모/바로 위의 자식만 아껴주는거지! 



### float

float는 형제끼리만 속성 부여.

float와 clear는 같이 속성을 부여하지 않는다.



### 소소한 팁

- %은 소숫점 6자리까지 인식한다. ex)33.333333%





---

---

## MPBO 이해하기

- 실습 파일명: a_basic_mpbo.html



### margin

위좌우아래px
위아래px 좌우px
위px 좌우px 아래px
위px 오른px 아래px 왼px -> 시계방향



### padding

```box-sizing: border-box;``` 박스의 크기는 그대로 유지한 채 내용 영역이 줄어듦

```box-sizing: content-box;``` 이 속성을 기재하지않는다면 기본으로 처리되는 기본값. 나(콘텐츠 영역)이 커지는 것.



### margin  vs  padding

margin만 태그중에서 마이너스 값 가능.
padding은 마이너스가 불가능.

margin은 auto 속성값 있음.
padding은 auto 속성값 없음.

margin: auto; 와 float:left  가 같이 작성하게 되면, margin:auto는 안 먹고, float: left만 먹게된다. 작성 순서 상관없이.



### border  vs  outline

border-width : 선두께
border-style : solid | dotted | dashed | 

border: 선두께 스타일 컬러;
border-image : 보더에 이미지를 집어넣겠다.

margin, padding, border 은 면적과 부피를 가진다.그래서 다른 개체들을 밀어낼 수 있다. 
outline 은 면적은 가지나 부피는 가지지않는다. 안개같은 존재.

```css
outline
```

offset: 동일한 간격       ->  익스플로러에서는 안 먹는 속성. 그래서 익스플로러에서 확인하면 안 먹음.
focus 잡을 때 활성화가 됐다는 것을 보여주는 용도로 사용한다.







---

**<참고자료>**

html 속성 모음 사이트  https://htmlreference.io/
css 속성 모음 사이트  https://cssreference.io/

w3schools.com  https://www.w3schools.com/     -> 파악하는 용도로만 사용하고, 실제로는 사용 자제하길...
MDN  https://developer.mozilla.org/ko/   



---

- screenshot : 스크롤 내리면서까지 스크린샷하는 크롬 전용 확장프로그램