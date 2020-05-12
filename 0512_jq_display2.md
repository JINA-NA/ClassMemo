# jQuery

## event

### scroll()

스크롤이 움직임에 따라서 이벤트가 발생한다.

### scrollTop()

- 매개변수가 비어있으면 값을 확인
- 매개변수에 값이 있으면, 해당 값으로 이동

도큐먼트에서 **스크롤**의 위치를 알려준다. 기준은 스크롤의 상단 라인이다.

animate( ) 메소드 내에도 해당 기능 사용 가능.

내가 필요한 곳으로 이동하게 한다.

---

헤드박스 있다가 픽스드 되는 기능

```
$(document).on('scroll',function(e){
	
	var myScroll = $(this).scrollTop();
	console.log(myScroll);

	if (myScroll > 100) {
		$('#headBox').css({ 'position':'fixed', 'top':0 });
	}else{
		$('#headBox').removeAttr('style');
	}

});
```



### offset( ).top 

브라우저 상단에서부터 **원하는 개체**가 얼만큼 떨어져 있는지 확인하는 기능

### offset( ).left

브라우저 왼쪽에서부터 **원하는 개체**가 얼만큼 떨어져 있는지 확인하는 기능





---

## 더 나아가

영상무료 사이트

https://www.pond5.com/free

https://coverr.co/