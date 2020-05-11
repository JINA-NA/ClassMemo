# jQuery 

## display

### display: block / :none / :toggle

- css을 직접적으로 컨트롤

- ```javascript
  //display:none
  btn.eq(1).on('click', function(e){
  	e.preventDefault();
  	dpBox.css({ 'display':'none' });		
  });
  ```

  ```javascript
  //display: toggle - 조건문을 통해 기능구현
  btn.eq(2).on('click', function(e){
  	e.preventDefault();
  	var dpV = dpBox.css('display');
  	
  	if(dpV === 'block'){
  		dpBox.css( {'display':'none'} );
  	}else{
  		dpBox.css({'display':'block'});
  	}
  });
  ```

  

---

### preventDefault 

: ```<button>```이나 ```<a>```에 기본적으로 있는 이벤트 속성을 초기화 시키는 기능. 

: ```button``` 같은 경우 submit 등의 기본적으로 있는 거를 기능을 안되게 한다.

: ```a``` 같은 경우 기본적으로 a의 기능인 페이지 이동을 동작하지 못하게 한다.

---

### show / hide / toggle

- css를 jq를 통해 컨트롤

- 확 나타났다가 확 사라지는 기능

- 작동 시간 구현 가능!

- ```javascript
  btn.eq(5).on('click', function(e){
  	e.preventDefault();
  	dpBox.toggle(2000);
  });
  ```

  

---

### fadeIn / fadeOut / fadeToggle

- 서서히 나타났다가 서서히 사라지는 기능.
- 단점 : 반응속도가 느리다.(애니메이션이 기본적으로 있어서)

- 솔루션: ```stop( )``` 메소드를 삽입한다. 그러면 여러번 반복해서 클릭했을 때 순서대로 차례차례 다 진행되는 게 아니라, 끊기면서? 진행된다

- ```javascript
  btn.eq(8).on('click', function(e){
  	e.preventDefault();
  	dpBox.stop().fadeToggle(500);
  });
  ```

  

---

### slideDown / slideUp / slideToggle

-  시간은 기재 안 할 시 기본적으로 0.1초 정도임.

- ```javascript
  btn.eq(11).on('click', function(e){
  	e.preventDefault();
  	dpBox.slideToggle(1000);
  });
  ```

  

---

### addClass / removeClass / hasClass / toggleClass

- 이 기능들은 시각적으로 변화하는 속성은 (일단은) 없지만, 코드 내용에서 class 이름을 추가/삭제 하는 기능이다
- class 이름이 추가/삭제 됨에 따라서 css문서에 해당 class가 있다면 그 css가 먹으면서 시각적인 변화가 일어나게 할 수도 있다.

---

**toggleClass**

```javascript
//1번 방법
var dpA = dpBox.attr('class');
var dpS = dpA.split('');
console.log(dpS);
if(dps[1] == 'action')

//2번 방법
var dpAc = dpBox.hasClass('action');
	if(dpAc === false){
		dpBox.addClass('action');
	}else{
		dpBox.removeClass('action');
	}
	
//3번 방법
dpAc === false ? dpBox.addClass('action') : dpBox.removeClass('action');
	
//4번 방법
!dpAc ? dpBox.addClass('action') : dpBox.removeClass('action');

//5번 방법
dpBox.toggleClass('action');
```

- hasclass : class 이름의 유무를 판단



### ! 

느낌표를 앞에 붙이면 해당 기능을 뒤집으라는  의미

---