Kotlin에서는 when이라는 메서드가 존재한다.

쉽게 생각하면 자바의 switch/case라고 보면 된다.

## when

when 수 많은 조건을 나열하고 할당된 변수가 조건에 만족할 때

그 조건에 만족하는 명령어를 실행한다.

먼저 if 조건문을 선언해보자

```kotlin
var Temperatures = 30
```

Temperatures 라는 변수를 선언하고 30이라는 값을 할당했다.

```kotlin
when(Temperatures) {
30>= ->
}
```