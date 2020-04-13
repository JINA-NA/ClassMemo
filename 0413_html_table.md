# 일러스트

## 패턴

저장한 패턴 사이즈 조절하기

1.  swatches에서 패턴 더블클릭해서 속성 변경
2. scale 툴에서 transforem object 체크 해제 & transform patterns 체크 후 사이즈 조정
3. rotatee 툴에서 transforem object 체크 해제 &  transform pattern 체크



## path profile

width-tool 툴 이용하여 동일한 선에서 선의 두께를 바꿀 수 있다.
만든 path profile을 저장해서 사용할 수도 있다.



## symbol

enable guides for 9-slice scaling : 웹페이지에서 도형이 줄거나 늘어날 때 분할해서 용이하게하기 위해 사용하는 기능.

symbol 끊기 : expand해서 하는 거 보다, symbol 패널에 보면 break link to symbol 사용해서 깨기



## character

leading(행간) : 첫 줄은 간격이 적용되지 않음.  
*line-height: css에서. 첫 줄도 간격이 적용된다는 점에서 leading이랑 다름

anti-aliasing



## 인쇄시 주의사항

1. stroke, 글씨 깨기
2. k=100은 qr코드,바코드를 제외한 곳에 사용 자제
3. overprint view 확인
4. 일러스트 버전 확인

---

---



# html

## table 구조 이해

실습 파일 : a_basic_table.html

```html
<table>
    <caption>표 제목</caption> 
    <tr> <th>1</th> <th>2</th> <th>3</th> </tr>
    <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
    <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
    <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
</table>

/* 첫번째 줄의 tr의 cell 갯수 = 그 이후 줄의 tr cell의 갯수*/
```

```css
{border-spacing: 0;} //td와 td 사이에 기본적으로 생기는 간격을 없애는 속성
{border-collapse: collapse;} //겹치는 부분에서 border값 중복되지 않게 하는 속성
```

th는 font-weight 기본값이 bold.

caption의 위치는 table 밖에 위치한다.



과거에는 ```<table summary="테이블에 대한 들을 수 있는 내용">```을 작성해야했어. 근데 html5에서는 안 쓰기로 해서 안 써.  근데 안 쓰는 게 아니라, caption 태그 안에 좀 더 디테일하게 작성을 해줘야 듣는 사람들이 편하지



### thead / tbody / tfoot

```html
<thead>
       <tr> <th>1</th> <th>2</th> <th>3</th> </tr>
     </thead>

     <tbody>
       <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
       <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
       <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
     </tbody>

     <tfoot> <!--  tfoot은 생략할 수도 있다. -->
       <tr> <td>1</td> <td>2</td> <td>3</td> </tr>
     </tfoot>
```



```html
<colgroup>
    <col class="col1">
	<col span="2" class="col1">
</colgroup>
```

col: 칼럼

```html
<col class="col2" span="2">  //두개의 열에 속성을 한꺼번에 적용하겠다.
```





---

---

# 찾아보기

## wai-aria

## trella

 : 협업툴

## notion

: 협업툴 & 자료 정리









