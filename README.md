<div align="center">
  <h1>자바스크립트 초보자를 위한 튜토리얼 (작성중)</h1>
  <h6>ㅡ 2020년 코로나시대 Javascript는 더 이상 과거의 천대받던 언어가 아닙니다 ㅡ</h6>
</div>

**본 문서**는 Javascript의 세계에 몸을 담고 싶은 사람에게는 `좋은 시작점`이 될 것 이며, Javascript를 기본적으로 다룰줄은 알지만 원하는대로 작동하지 않는것에 대하여 **언어적 문제로 치부하고 불만**을 가지고 있던 당신에게는 `좋은 깨달음`이 될 것 입니다.<br>

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

```
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

## Scope

> **스코프란**

`스코프`는 변수가 접근할 수 있는 **유효 영역**이며, `자바스크립트`는 스코프를 **함수**로 나눌수 있습니다.<br>
또한 스코프는 크게 전역과 지역으로 나눌수 있는데 Strict 모드가 아닐 경우에 전역은 Window 객체를 가르킵니다.

> **예제로 익히기**


## This
## Bind
## Prototype
## Pattern
