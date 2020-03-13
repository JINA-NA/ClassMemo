# 1. layout짜기 

## layout 짜기

- 실습파일명: a_basic_layout_01.html



margin: 위 오른쪽 아래 왼쪽;
```margin: auto``` 가운데

```magin: 200px auto``` 위아래 200px, 좌우 중앙 정렬.

height: auto;   따라오는 내용의 길이에 따라서 자동으로 늘어나거나 줄어듦.





---

em : 1em=16px

pt : 웹에서는 잘 쓰지않는 개념. 
		일러/포샵 같은 그래픽 프로그램에서는 12pt=12px(동일한 값이다)
		웹에서는 16px=12pt



웹에서 쓰는 단위

px, %, em, vem, vw, vh, pc ...



inline : 크기값이 없다. 줄바꿈 없다. 여백 없다. a span input label select

block: 크기값 있다. 줄바꿈 있따. 여백있다. ul ol li h1~6 p form 



- 자손선택자   #box
- 자손선택자   #box > ul > li        -> 쉽게 생각하면 직계 자손만 선택하는 거야! 



블럭: 기본값

인라인 : 옆으로 자연스럽게 나열. ex) strong

인라인을 담는 용기가 블럭이라는 거지.



float는 형제끼리만 속성 부여.

float와 clear는 같이 속성을 부여하지 않는다.



%은 소숫점 6자리까지 인식한다.



**유사하지만 다른 속성**
margin/padding
border/outline

**<참고자료>**

html 속성 모음 사이트  https://htmlreference.io/
css 속성 모음 사이트  https://cssreference.io/

w3schools.com  https://www.w3schools.com/     -> 파악하는 용도로만 사용하고, 실제로는 사용 자제하길...
MDN  https://developer.mozilla.org/ko/   





---

## MPBO 이해하기

- 파일명: a_basic_mpbo.html



```min-height``` 최소 높이값

```max-height```  최대 높이값



위좌우아래px
위아래px 좌우px
위px 좌우px 아래px
위px 오른px 아래px 왼px -> 시계방향

box-sizing:border-box;

box-sizing:content-box; 기본값



margin만 태그중에서 마이너스 값 가능.
padding은 마이너스가 불가능.

margin은 auto 속성값 있음.
padding은 auto 속성값 없음.

margin: auto; 와 float:left  가 같이 작성하게 되면, margin:auto는 안 먹고, float: left만 먹게된다. 작성 순서 상관없이.

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









# 2. pen tool(일러스트레이터)

# 3. 패스파인더, 얼라인











---

- screenshot : 스크롤 내리면서까지 스크린샷하는 크롬 전용 확장프로그램