# css- background image

### background-color

배경색



### background-image

#### img  vs  background-image

- img와 비슷한 개념이지만, img경우는 글자처럼 html 요소 내부에 담아서 사용한다.

- background-image의 경우는 배경 색상대신 이미지로 대체하는 기능이다.
- img는 새로고침의 경우 매번 새로 불러오는 형식
- bgi는 임시로 저장해서 새로고침해도 추가 데이터를 소모하지 않는다.
- img는 자주 변경하는 영역에서 많이 사용
- bgi는 디자이너가 주로 사용, 한 번 세팅하고나서 크게 변하지 않는 영역

- ```css
  <img src="이미지의 위치" alt="대체이미지 텍스트">
   -> html에서 작성
  
  <background-image: url('이미지의 위치')>
   -> css에서 작성
  
  *이미지의 위치는 현재 작성중인 css파일의 위치를 기준으로 이미지가 있는 상대 경로를 입력한다.
  ```

  

### background-repeat

```css
background-repeat: no-repeat
background-repeat: repeat-x
background-repeat: repeat-y
background-repeat: repeat (기본값)
```



### background-position

```css
background-position: 100% 0 /* x좌표 y좌표 */ 오른쪽상단
backgroun-position: 50% 50% /* 가운데 중간 */

```

```css
background-position: left top /*가능은 하되, 권장하지 않음*/
```

```css
background-position-x /*위로 올라갈수록 마이너스값*/
background-position-y 
```

* 주의할  점:  이미지의 x좌표와 position의 좌표가 같이 ... 아 뭐라해야되지? ​ 0 이면.... 기존에 알던 다른 그냥 position과 달라....... 

- %로 값을 부여할 경우, 안의 내용물(이미지)도 같이 배치되는데,

  px(rem,vw..등 %를 제외한 나머지 단위)로 값을 주면, 내용 이미지는 0 0 좌표를 기준으로 위치를 이동한다. 
  
  

### background-size

```css
.bg_box_01 {width: 400px; height: 100px; 
		background-image: url('../../img/background/bgi_landscape_01.jpg');
		background-repeat: no-repeat; 
		background-position: 0 50%;
		background-size: 100% auto;}
```

```css
background-size: contain /*이미지를 모두 보게 만들기-빈공간 생김*/
background-size: cover  /*빈 공간 없이 꽉차게 처리-이미지가 잘림*/
```



### background-clip

배경이미지의 영역을 어디까지 포함할것인가?

```css
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
background-clip: text; -webkit-background-clip: text;
				 color: transparent; 
				/*마지막 속성은 ie에서 아예 안 먹음*/
```

border-box: 외곽선의 영역까지 이미지를 담는다.
padding-box: padding 영역까지 이미지 담는다.(border 영역은 제외)
content-box: 내용만 담을 수 있는 영역(padding,border 영역은 제외)
text: 글씨의 영역만큼 이미지로 마스크처리하는 기능(쉽게 말해, 클리핑마스크)
         단, 글씨의 색상은 투명이여야 한다. ie에서 모든 버전에서 지원x



### background-attatchment

```css
background-attatchment: scroll /*스크롤 따라서 왔다갔다 거림*/
background-attatchment: fixed /*스크롤 따라서 왔다갔다 안 거림*/
```

배경이미지 중복해서 삽입하기

```css
background-image: url('../../img/background/bgi_landscape_02.jpg'),				url('../../img/document.png');
background-size: cover, 100px auto;
background-position: 50% 50%, 50% 50%;
```



### IR 기법, IS 기법

#### IR기법

image-replace

내용을 text대신 이미지로 대체하여 보이게 하는 기법.

```css
.in_box > span {
	display: block; /* none쓰면 안돼. 보이진않되 읽혀야돼*/
	width: 0; height: 0;
	overflow: hidden;}
```



#### IS기법

image-sprite

여러개의 이미지를 하나의 이미지로 저장하여 브라우저의 속도를 올릴 수 있는 기능이다.
아이콘 이미지를 한 캔버스에 저장하고 한번에 하는 거!

- 이미지는 작은 이미지를 여러 개를 따로 띄우는 거 보다, 여러개를 한번에 띄우는 형태가 로딩 속도가 더 빠르다.
- 여러개의 이미지를  관리하는 것보다, 하나의 이미지로 관리하는 게 더 효율성이 높다. 
- 파일 하나하나 이름짓는 거 하며, 유실 됐을  때 찾는 거 하며...생각해봐.. ! 얼마나 빡칠지!
- 단, 하나의 이미지에 들어있는 형태들은 유사이미지여야한다. 
- 또한, 각각의 좌표는 별도의 관리가 되는 것이 좋다.

- 단위는 px보다 rem을 권장하지만, 사실 px과 rem 둘 다 쓰는 게 가장 베스트!

  vscode 단축키 alt+z : px to rem 

**x나 y좌표가 같을 때**

```css
.part_03 li:nth-child(4) > a {background-position: -605px -116px;}
.part_03 li:nth-child(4) > a:hover {background-position-x: -701px;} /*y값은 동일하고 x값만 변화될 때 이처럼 사용할 수도 있다.*/
```

```css
.part_04 li:nth-child(2) > a {background-position: -252px -165px;}
.part_04 li:nth-child(2) > a:hover {background-position-x: -91px;}
.part_04 li:nth-child(2) > a:focus {background-position-x: -293px;}
.part_04 li:nth-child(2) > a:active {background-position-x: -51px;}
```

순서가 중요하당~ 

그냥   ->    :hover   ->    :focus    ->     :active 순으로 작성해야 다 먹어용~



---

## 추가 꿀팁

### 파일명 한번에 바꾸는 프로그램

 darknamer



### 포토샵 액션

action 패널 열기 -> action 추가하고 동작하기

-> file -> automate -> batch

-> action 실행할 폴더 선택하고 각종 옵션 설정 후 OK



### 브라우저에 따라 수행되는지!?

https://caniuse.com/  브라우저별로 지원하는 속성을 검색할 수 있다