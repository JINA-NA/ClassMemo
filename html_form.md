# form

## 1차 기억해야할 순서

1. 보안의 처리 방법을 어떻게 할 것이냐(<strong>post, get,</strong> delet, 

2. 연결될 파일(서버파일) - id와 비밀번호를 입력하고 나서 로그인 버튼을 누르잖아. 데이터베이스와 사용자를 중매해주는 매개체를 서버파일이라고 한다. 예)php, jsp, asp ... 

3. 웹 표준에 맞게 절자체 맞게 정확하게 해야한다.

4. 접근성 고려해야한다.

5. 각 기능별 형태를 이해해야한다.(입력, 선택 및 체크, 버튼, 멀티, 기타 ...)



## 구조

```html
<div class="form_01">
	<form action="#" method="post"></form>
</div>
```

## form

**action**
연결될 파일(서버파일)의 경로

**method**

- get : 알려져도 되는 자료. 공개. (ex.검색창)

- post : 숨기고 싶은 자료. 비공개. (ex. 로그인)



```html
<form action="#" method="post">
	<fieldset>
		<legend>해당하는 영역의 제목(나라마다 전설의 영웅들이 존재하지)</legend>
		<input type="text" value="" />
		<input type="button" />
	</fieldset>
</form>

```

**fieldset**
form을 한 번 더 감싸는 것

**legend** 
영역의 제목. 나라마다 전설의 영웅들이 존재하지. h처럼 반드시 써야한다. 보여주기 싫으면 hidden을 해라. 안쓰면 안돼.



## **input**

- 싱글태그
-  inline-block 요소

- type 

  **<기본적으로 모든 브라우저에서 작동하는 기능>**

  <입력하는 기능>

  - text : 직접 글자 입력
  - password
  - hidden: 기존에 입력되어 있었던  텍스트를 보여주되 감춘다. 예)개인정보수정 시에

  

  <체크하는 기능>

  - checkbox : 중복 선택 가능
    - checked="checked"   기본적으로 체크가 되어있게 하는 속성
  - radio : 무조건 선택해야 한다. 단일 선택

  

  <버튼의 기능>

  - submit : 데이터를 확인하고 전송. 예)로그인버튼
  - reset : 재설정, 취소               -->  사실상 submit이랑 reset은 한 페이지 내에 한번씩 사용하게 되더라구
  - image : 이미지형 submit (현재 사용x)
  - button : 버튼. 예)아이디 중복확인 버튼, 주소 검색, 우편번호 검색
  - file : 파일 첨부 버튼

  

  <멀티 - input 태그 내에 들어가는 속성이 아니라 따로 있는 태그> 

  - textarea : 카톡창 처럼 텍스트를 쓸  수 있다
  - select, option : 예)패밀리 사이트
  - button

  

  **<html5에서부터 추가된 기능>**- 일부 기능은 익스플로러에서 작동하지 않을 수 있다.

  <입력>

  - number :  예)수량 변경할때 해당 숫자를 직접 기입할  수 있도록
  - range : 예) 폰에서 음량 버튼 조절
  - tel : 전화번호
  - email : 이메일
    - @ 존재유무로 이메일인지 아닌지 확인한다.
  - search
  - url : 
    - http:// 의 존재유무로 url인지 아닌지 확인한다.

  

  <체크>

  - color: 
  - datalist : 예) 배송기사님께 남기고 싶은 말

  

```html
<label for="serachArea">검색할 내용을 입력하세요</label>
<input type="text" id="serachArea" name="search" value="" placeholder="내용을 입력하세요"/>
```

***웹 접근성을 위해***

**id**
마이크로 링크. 반드시 id여야한다.

**label**
이름을 다는 기능 . ```label``` 과 연동되는 이름

**name**
사용자에게 받은 데이터를 서버파일의 어떤 구역으로 보낼지 하는 것
*name =" " 속성값을 반드시 백엔드 개발자와 협의해야한다.

**value**
작성한 데이터를 저장하는 것. 대게 속성값은 비워둔다. 사람들이 어떤 걸 입력할 지 모르니까.

**placeholder** 
사용자가 내용을 입력하기 전에 행동을 불러일으키는 가이드를 삽입하는 문구

**required**

입력하라고 한 사항들 입력 안하고 확인버튼 누를 경우, 입력하라고 경고창(?) 나오는 속성

이 태그의 속성값은 required 로 같다. 속성과 속성값이 같을 경우 생략해도 된다. ```required ```라고만 써도 됨(아래 코드 참고)

```html
<input type="search" id="searchArea" name="searchArea" value="" / placeholder="검색할 내용을 입력하세요" required />
```



---



---

---

## 추가적인  내용

마이크로 링크: 지금 현재 페이지 안에서 왔다갔다 하는 거. ex)탑 버튼

```
{a href = "#headBox"}
```



---

**<참고 사이트>**

codepen.io : form의 요소들의 디자인을 모아놓은 사이트

w3c.org/tr : 검색창에서 html 검색.