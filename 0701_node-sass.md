# node-sass

## libsass

prepros가 내 노트북에 안 깔려서 선생님 알려주신 대안.

이 방법이 더 쉽긴한데, 초보자가 사용하기에  prepros가 더 편하니까(node-sass시작하는 코드를 외우기 싫어서) .

근데 써보니까 이 방법이 처음에 코드만 쓰면 더 편하기도 해...

### 설치방법

```bash
npm install --global node-sass
```



### 컴파일하는 방법

```bash
node-sass --watch scss --output css
```

scss를 사용할 때, 반드시 위의 코드를 켜놓고 저장해서 css로 자동으로 컴파일이 되면서, html 문서에 반영이 된다.



### 속성

```bash
nested, expanded, compact, compressed
```





### 더 많은 정보는

http://poiemaweb.com/sass-basics