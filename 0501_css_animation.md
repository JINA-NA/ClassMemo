# css

## transition  vs  animation

-  transition은 단회성, animation은 연속성
  - 단회성: 특정한 조건이 줬을 때, 한번에 한 기능을 처리한다.
- 쉽다면 transition이 쉽지

---

## transition

```css
transition-[기능] : ... ;

transition-property: ... ;
transition-duration: .. ;
transition-timing-function: ..;
transition-delya: ... ;
```

**property** 
: 속성명 . (필수기재. 이거 안쓰면 안됨)
all  /  css속성명(margin,color...)

**duration**
 : 지속시간
1s  /  0.5s  /  1000ms   /  500ms

*js에서는 s는 안 먹고, ms만 먹어서 선생님은 ms단위를 사용하는 편.

**timing-function** 
: 시간에 따른 함수/속도처리방식
ease  /  ease-in  / ease-out  /  ease-in-out  /  linear  / cubic-bezier()

- timing-function 에서 가능한 속성값
  - ease : 빨라지다가 느려지는  거
  - ease-in : 천천히 가다가 훅 빨라짐
  - ease-out  : 처음에 빠르다가 느려짐
  - ease-in-out : 빨라지다가 느려지는 거. ease와는  그 비율이 다름
  - linear : 같은 속도로
  - cubic-bezier(  ,  ,  ,  )
    - 참고자료 https://cubic-bezier.com/#.17,.67,.83,.67
    - 크롬 관리자모드에서도 직접적으 바꿀 수도 있다.

 **delay** 
: 지연시간
지속시간과 표현방식 동일(시간 단위로 설정)





## animation

```css
animation-name: ... ;
animation-direction: ...;
animation-delay: ...;
animation-duration: ...;
animation-iteration-count: ...;
animation-play-state: ...;
animation-fill-mode: ...;
```

**animation-name** : animation을 처리할 이름

**animation-direction** : 종료 후 재처리 방법?

- normal : 한 방향으로 진행
- reverse : 역순으로 진행
- alternative : 왔다리갔다리  진행

**animation-delay** : 지연시간

**animation-duration**   : 지속시간

**animation-iteration-count**   : 반복횟수

- 원하는 반복 숫자
- infinite

**animation-play-state**   : 재생 / 정지

- running : 재생 
- paused : 정지

**animation-fill-mode**   : 동작 전/후에 처리되는 값

- backwards : 첫 장면으로 돌아와서 끝나는 거
- forwards : 마지막 장면으로 끝나는 거



**@keyframes** [animation-name] **{}**

   : 선택자에 animation 기능을 수행할 이름을 지정하고, 지정된 이름의 기능을 별도로 수행명령내용을 따로 처리..

   : 중괄호 안에 속성을 기재하지 않고, @charset 처럼 밖에 따로 기재한다.

```css
@keyframes first {
	/* from {transform:translate(0);}
	to {transform: translate(30rem);} */
	0% {transform:translate(0);}
	5% {transform: translate(2rem);}
	50% {transform: translate(15rem, 5rem);}
	75% {transform: translate(30rem, 30rem);}
	100% {transform: translate(30rem);}
}
```

- 0~100%는 애니메이션 지속 시간 중 해당 시간의 순간임. from과 to로도 값을 줄 수 있지만,  얘네들은 시작과 끝만 있어서 중간 부분의 애니메이션을 줄 수가 없어서 이렇게 주는거야.
- first 라고 써있는 건, animation-name을 기재하는 곳이야. 꼭 같아야만 동작하니까 유의할 것!











---

## 추가적으로

*transform / translate / transition / transparent : 비슷비슷한 단어 헷갈리니까 잘 기억할 것!

---

