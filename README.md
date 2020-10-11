<div align="center">
  <h1>자바스크립트 초보자를 위한 튜토리얼 (작성중)</h1>
  <h6>ㅡ 2020년 코로나시대 Javascript는 더 이상 과거의 천대받던 언어가 아닙니다 ㅡ</h6>
</div>

**본 문서**는 Javascript의 세계에 몸을 담고 싶은 사람에게는 `좋은 시작점`이 될 것 이며, Javascript를 기본적으로 다룰줄은 알지만 **원하는대로** 작동하지 않는것에 대하여 **언어적 문제로 치부하고 불만**을 가지고 있던 당신에게는 `좋은 깨달음`이 될 것 입니다.<br>

많은것을 준비하지는 않았습니다, **하나하나 천천히** 읽어보다가 이해가 되지 않으면 `또 다른 여정`을 떠나다 오셔도 좋습니다.

## 학습전 요구사항

1. `Javascript` 말고 다른 언어를 사용한적이 있다.
2. 크롬 `개발자 도구`를 간단하게 사용할 수 있다.
3. 개발에 필요한 `IDE`를 이미 사용할줄 안다.

## Contents

- [Object](#Object)
- [Scope](#Scope)
- [This](#This)
- [Bind](#Bind)
- [Prototype](#Prototype)
- [Pattern](#Pattern)
  - [Assignment](#Assignment)
  - [Closer](#Pattern)
  - [MVC](#MVC)

## Object

<details>
<summary>클릭하여 펼쳐서 내용 확인하기</summary>
<br>
	
> **오브젝트란**

`오브젝트(Ojbect)` 한글로는 **객체**,

**Javascript**에서 모든 데이터와 함수는 이 `객체`라고 불리는 **녀석을 기반**으로 만들어졌습니다,<br>
당연히 앞으로 **당신이 만들게 될 데이터와 함수**들도 예외는 아닙니다, 중요하니 잘 기억해두세요.

> **구조 확인**

그럼 간단하게 오브젝트의 구조를 보겠습니다, 브라우저 **개발자 도구 콘솔**에 다음과 같은 커맨드를 입력하세요.

```Javascript
console.dir(Object);
```

그럼 아래와 같이 **트리구조**의 형태로 Object의 내부를 볼 수 있게 됩니다.

```Javascript
ƒ Object()
  arguments: (...)
  assign: ƒ assign()
  caller: (...)
  create: ƒ create()
  defineProperties: ƒ defineProperties()
  defineProperty: ƒ defineProperty()
  entries: ƒ entries()
  freeze: ƒ freeze()
  .
  .
  .
```

그리고 초반에 말한것 처럼 함수 또한 **최종 프로토타입**을 보면 `오브젝트`를 기반하에 있는걸 볼 수 있습니다.

```Javascript
console.dir(Function);

ƒ Function()
	arguments: (...)
	caller: (...)
	length: 1
	name: "Function"
	prototype: ƒ ()
	__proto__: ƒ ()
		__proto__: Object
```

</details>

## Scope

<details>
<summary>클릭하여 펼쳐서 내용 확인하기</summary>
<br>
	
> **스코프란**

`스코프`는 변수가 접근할 수 있는 **유효 영역**이며, `자바스크립트`는 스코프를 **함수**로 나눌수 있습니다.<br>
또한 스코프는 크게 **전역과 지역**으로 나눌수 있는데 **Strict 모드**가 아닐 경우에 전역은 `Window` 객체를 가르킵니다.

> **예제로 익히기**

이곳에 다양한 `스코프`의 흐름을 익힐 수 있는 **예제**들을 준비하였습니다,<br>
하나하나 코드를 읽어보며 **어떤 값**이 나올지 판단해보세요. *( Strict 모드 기준 아님 )*

**(1). 전역과 지역**
```Javascript
var dollar = "1";

(function Func(){
	var dollar = "2";
	console.log(dollar);
})();
```
```Javascript
2
```

**(2). 전역과 파라미터**
```Javascript
var dollar = "1";

(function Func(dollar){
	console.log(dollar);
})("2");
```

**(3). 전역과 객체**
```Javascript
var dollar = "1";

({
	dollar : "2",
	Func : function(){
		console.log(dollar);
	}
}).Func();
```

</details>

## This

<details>
<summary>클릭하여 펼쳐서 내용 확인하기</summary>
<br>
	
> **많은 이들이 간과하는 것**

많은 사람들이 `Javascript`를 이용하면서 **간과**하는 것 중 하나가 바로 `This`를 간단하게 생각하는 것 입니다.<br>
하지만 지금부터 **정말 제대로 다루려면** 기존에 타언어에서 썼던 `This`에 관한 편견과 로직을 모두 잊어야합니다.

> **This란**

`This`는 **사용하는** This를 가지고 있는 **함수**를 호출하기 전에 거쳤던 **객체**를 의미합니다.<br>
*( 위에 말이 가장 핵심 입니다, 이해가 안되면 수십번 읽고 계속해서 학습을 진행하시길 권장합니다. )*

> **예제로 익히기**

**(1). 단독 함수 호출시**
```Javascript
var dollar = 1;

function trans(){
	var dollar = 2;
	this.dollar = 3;
	console.log(dollar);
}
console.log(dollar);
```

</details>

## Bind
## Prototype
## Pattern
