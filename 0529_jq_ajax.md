# jquery

제이쿼리 외부문서 불러오기

## ajax

```javascript
$.ajax();
```

이렇게 사용하는 메소드를 **유틸리티 메소드** 라고 한다.

```javascript
$.ajax({
		url:'../data/ajaxTest.jason',		//경로
		dataType: 'json', 					//문서 타입
	    success:function(data){				//외부에서 문서불러오기를 성공했다면 다음과 같은 함수기능을 수행하세요.
			console.log(data)	}
});
```

- 







## jason 파일특징

- 주석 안 먹는다.

- 홑따옴표는 취급하지 않는다. 무조건  쌍따옴표 사용!!!



---

## ajax 

jason  파일을 따로 만들어서, js에서 ajax로 불러와서 하는 거....?

바깥에 따로 만들어서 불러와서 처리한다는 거

- 보안
- 작업 용이



ajax라는 아이도 제이쿼리를 통해 만든 애긴 한데, 어려워서 쉽게 만ㄷ르어줬음

