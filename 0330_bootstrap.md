# bootstrap

유사한 다른 프레임워크 : 벌마, susy, boburn 

http://bootstrapk.com/

이쁘고 쉽게 만드는 것

설치는 nodejs 처럼





## 부트스트랩 CDN

```html
<!-- 합쳐지고 최소화된 최신 CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">

<!-- 부가적인 테마 -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap-theme.min.css">
```

head 안에 붙여넣기

홈페이지에서 위의 코드를 html 문서에 작성한다. 이 때, 반드시 코딩작업할 때 인터넷이 연결되어있어야한다!



## css

### 모바일우선

```html
<meta name="viewport" content="width=device-width, initial-scale=1,  minmum-scale=0.5, maximum-scale=3, user-scalable=yes">
```

기본 스케일

확대를 어디까지 가능하게 할것이냐

확대를 가능하게 할 것이냐



### 콘테이너

```html
<div class="wrap container"></div>
```

container에 대한 css속성은 이미 부트스트랩에 내장되어있기 때문에 따로 css속성을 작성할 필요가 없다.



```html
<div class="container">
  ...
</div>

//뷰포트 전체폭까지 늘어나는 최대폭 콘테이너를 위해
<div class="container-fluid">
  ...
</div>
```



### 그리드 옵션

브라우저 전체 너비를 100으로 잡고 12등분. 100/12=8.333333333

```html
<div class="col-xs-12 col-sm-3 col-md-3 col-lg-2">
```

12등분 했을 때 곱하기2만큼 분할.

xs : 스마트폰
sm: 태블릿
md: pc 중 작은 거
 lg: pc 중 큰거





### 컬럼 오프셋하기







