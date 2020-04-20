# css - font

## font-family

```css
font-family: arial, 'myriad_pro', '돋움', dotum, serif
```

- 서체 이름을 쓰는 순서대로 서체가 적용된다.

- 서체에 띄어쓰기가 있거나 한글일 경우 따옴표 안에 기재한다. 또한 한글서체는 영어로도 기재를  해주어야 한다.

- 영문 서체 - 국문 서체 - 한자 서체 ... - 고딕/명조 순으로 대게 기재한다.

- 저렇게 설정을 해줘도 컨트롤 밖의 서체가 적용될 수도 있으므로, 3~4px 정도 여유를 두어야한다.

- 윈도우, 맥 실제 기기에서 적용된 것을 확인해봐야한다.

  


## 웹폰트

어떤 컴퓨터 어떤 환경에서 웹페이지를 열어도 같은 서체로 되게끔 하는 방법

내 컴에서 보이는거랑 다른 컴에서 보이는 거랑 같은 서체로 보이게하고 싶어요!  

구글 폰트 https://fonts.google.com/  

무료 폰트 눈누 https://noonnu.cc/index 

- **웹폰트 html,css에 적용하기**
  - 원하는 서체  선택 ->  embed 에서 link 복사해서 html, css에 기재

- 맥시멈 3개. 이 이상을 적용하면 서버가 느려진다.

  
  
- **로컬 폰트를 웹폰트로 전환하기**

  - 폰트 이름 영어로 바꾸기
  - 구글에 font transfonter 검색
  - https://transfonter.org/
  - 폰트 파일 add -> convert
  - 변환 완료되면, 다운로드 받고, 작업중인 cording 폴더에 fonts 폴더 생성 후 이동
    - base64 체크하면 굵기... 뭐시기...
    - 10MB 이상 되는 파일은 제공을 안해준당ㅠㅠ
    - autohint font, add local rule 체크
    - ttf, woff, svg 등 다 체크
  - 다운받은 파일 중 html 열어 확인
  - 다운받은 파일 중 css 파일을 열어보면, 폰트에 대한 내용을 변경할 수 있다.
    - font-family, font-weight 등 내맘대로 설정할 수 있어
    - .eot: 익스플로러 하위버전에서 사용
    - 
  
  

## font-weight

```css
font-weight: normal;  -> 400
font-weight: bold;  -> 600
font-weight: light;  -> 300
font-weight: 100;
```

- 100~900 / thin / lighter / normal / bold / bolder / black 

속성값 : normal, bold, light, thin ... 등 뿐만 아니라 100,400(normal),900 등 숫자로도 속성값을 줄 수 있다. 다만, 숫자로  속성값을 부여하는  경우에는 상황에 따라 적용이 될 수도 있고, 안 될 수도 있다. 



## font-style

```css
font-styel: normal
font-style: normal //이탤릭체로 디자인된 서체를 사용
font-style: oblique //강제 기울이기
```



## font-size

```css
:root{font-size: 16px;}
font-size: 16px
```

- 부모에게 font-size를 부여하지 않는 이상, font-size: 100% 주면 이 root를 따른다.
- 기본값은 16px = 1rem (root를 안 써도)
- px단위보다 rem 단위를 권장



## text-align

```css
text-align: left
text-align: center
text-align: right
text-align: justify /* 양쪽 맞춤 */
```



## text-transform

```css
text-transform: uppercase /* 전부 대문자로 */
text-transform: lowercase /* 전부 소문자로 */
text-transform: capitalize /* 첫글자만 대문자로 */
```



## line-height(행간)

```css
line-height: 1  /* = 100% */
line-height: 1.2  /* =120% 대게 영문 행간이 이정도 */
```

- 한 줄 일 때는 괜찮은데, 두 줄 이상 되면 좀 그래.. 
- 단위를 사용하지 않아도 동작하기 때문에 정확한 단위 표시를 해야한다.



## letter-spacing(자간)

```css
letter-spacing: 0 /* 변화 없음*/
letter-spacing: 1px;
letter-spacing: -1px; /* 음수도 가능*/
```



## word-spacing(단어 사이 간격.어간)

```css
word-spacing: 1px
word-spacing: -1px /* 음수 가능 */
```

예시)로그인 버튼

```css
button{word-spacing: -0.2rem;}

/* login 이라고 쓰면 '로자인' 이라고 읽음. 그래서 log in 이라고 써야되는데 시각적으로 붙여보이게 하고 싶을 때 어간 조정 */
```



font-stretch

---

위의 font 속성들을 따로따로 쓸 수도 있지만, **한번에 쓸 수도 있다.**

```css
font: [weight] [style] [font-size] / [line-height] [font-family], [font-family] ...;
```



## 말줄임표... 만들기

```css
overflow: hidden; 
white-space : nowrap; /* 의미 없는 공백 */
text-overflow: ellipsis; /* 넘치는 텍스트를 어떻게 할거니?*/
```

overflow: 박스 자체에서 넘치는 것

text-overflow: 넘치는 부분의 글자를 어떻게  할거니?

- ellipsis : '생략'이라는 뜻



## overflow

```css
oveflow: auto; 글자수가 많아지면 스크롤생기고, 적으면 안 생기고
overflow: hidden; 글자가 넘치면 숨김
overflow: scroll;
overflow-y: scroll; /* 세로 스크롤만 생성*/
overflow: visible; 

overflow: visible; overflow-y: scroll; /*브라우저에 따라 스크롤 생성이 다를 수 있으므로 이렇게 작성을 하면 된다.*/
```



## scrollbar

### 스크롤바 숨기는 방법

```css
.overflow>span 
{display: block; width: 100%; height: 100%; background-color: #faa; 
    overflow: visible; overflow-y: scroll;
    padding-right: 20px;}

padding-right를 주는 게 스크롤바 숨기는 키포인트!
분명시 스크롤바 있고, 마우스 스크롤 돌리면 위아래로도 되는데, 옆으로 가서 안 보이게 하는거야~
```





