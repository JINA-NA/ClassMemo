# jQuery

## 확인 및 생성 api

api란? '기능'이라는 의미. 

---

**참고사이트**

다양한 제이쿼리 api 모음  jquery cheat sheet   https://oscarotero.com/jquery/

---

## DOM 관련

### html

기존 내용을 지우고 태그 생성

1. ( ) 비어있으면 내부에 있는 것을 확인하는 것
2. ( 매개변수 ) 내용이 있으면 태그를 삭제하고 입력(생성)하라는 것

### text

기존  내용을 지우고 글자  생성

1. ( ) 비어있으면 확인하는 것.

2. ( 매개변수 ) 내용이 있으면 문자를 삭제하고 입력(생성)하라는 것.

```javascript
gnbList.eq(i).html('<a href="#">' + gnbListText + '</a>');
//----> 코드로 입력됨

gnbList.eq(i).text('<a href="#">' + gnbListText + '</a>');
//----> 텍스트로 입력돼서 창에 코드 그대로 <a href="#">어떤 내용</a> 이런식으로 보여짐

```

### wrap

1. ( ) 비어있으면 확인
2. ( ) 내용 있으면 감싸는 영역을 생성

### contents

내용 요소를 확인하는 것. 코드와 텍스트 모두

### append , appendTo

1.뜯어서 (매개변수) 뒤에 담아라

```javascript
headBox.append(h1);    //headBox 내부 뒤에 h1을 담아라
h1.appendTo(headBox);   // h1을 headBox 내부 뒤에 담아라
```

2.코드를 직접적으로 입력할 경우에는 생성해라

```javascript
gnbBox.prepend('<div class="gnb_btn><button type="button">메뉴</button></div>');
```

! 유의 !

```
(  a  ).prepend(  b  )    :  a와 b는 부모관계. 
							 a 내부에 첫번째로 b를 만들어라 		
```

### prepend , prependTo

뜯어서 (매개변수) 앞에 담아라

to의 유무에 따라서 주체가 달라지는 것!

```javascript
headBox.prepend(h1);    //headBox 내부 앞에 h1을 담아라
h1.prependTo(headBox);   // h1을 headBox 내부 앞에 담아라
```

### attr

속성

1. ( ) 비어있으면 가져오는  거
2. ( 매개변수 ) 내용있으면 변경한다. 

### val

form요소 내부의 value 값을 확인 또는 변경

### before , after

선택자 형제로 전/후 추가 요소를 담는 기능

*css에서 :before :after는  부모-자식관계인데, jq에서는 형제관계이다.

### remove

아예 삭제하는 거 

ex)쓰레기통을 버리라고 했을 때, 쓰레기통 자체를 버리는  거

### empty

내부를 비우는 것

ex) 쓰레기통 비우라고 했을 때, 쓰레기통 안의 쓰레기만 버리는 거

### clone

선택 요소를 복제, 'true' 를 함께 사용하면 내용 요소의 기능을 포함하여 복제함

### hasClass

선택 요소에 해당  class 이름의 유무 판단 

ture /  false 로 결과값 도출

### is

선택 요소에 class를 제외한 속성의 유무를 판단



### 

## 크기 관련

### width

### height

### innerWidth

### outerWidth

### innerHeight

### outerHeight

### ture

### addClass , removeClass

class 이름값을 추가/삭제하는 거



### scrollTop

스크롤의 위치를 물어본다

### offsetTop



## 디자인 관련

추가 자료

jQuery에서 사용되는 animate 기능  http://easings.net

---

### css

1회성

- css에서 transition 기능을 쓰고, js에서 animate 기능을 중복 적용하면 서로 충돌일으켜서 제대로 구현이 안 될 수 있다.

### animate

```html
<script src="../js/base/jquery-ui.min.js"></script>
```

위의 jQuery UI 소스가 없으면 animate 는 기능하지 않는다!!



### 이벤트

어떤 행동을 취하는 모든 것을 이벤트라고 한다. 기존의 형태에서 무언가 변화가 일어나는 형태

### show

### hide

### fadeIn

### fadeOut

### slideDown

### slideUp

---



## 보충

jQuery 호출하는 함수

- 어떤 것을 사용하든 무방하다.
- 사람마다 다를 수 있다.

```javascript
$.ready(function(){});
$(functioin(){});
$(document).ready(function(){});
```

