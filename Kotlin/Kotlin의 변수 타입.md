
Kotlin은 자바와 다르게 변수의 타입을 따로 지정하지 않아도

컴파일 오류가 발생하지 않는다.

그렇다면 기본적으로 값을 입력했을 때 지정되는 Default 값은 무엇일까?

# 숫자형 변수

숫자형 변수에는 여러가지의 종류가 있다.

|타입|메모리 크기|값의 범위|
|-----|-----|-----|
|byte|1 byte|-2<sup>7</sup> ~ (2<sup>7</sup>-1)|
|short|2 byte|-2<sup>15</sup> ~ (2<sup>15</sup>-1)|
|int|4 byte|-2<sup>31</sup> ~ (2<sup>31</sup>-1)|
|long|8 byte|-2<sup>63</sup> ~ (2<sup>63</sup>-1)|
|float|4 btye|-3.4 x 10<sup>38</sup> ~ 3.4 x 10<sup>38</sup>|
|double|8 byte|-1.7 x 10<sup>308</sup> ~ 1.7 x 10<sup>308</sup>|

## 정수

정수 타입 number라는 변수를 선언해보았다.

```kotlin
var number = 10
```

결과

![varint](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/varint.PNG)

정수를 입력하면 기본 타입이 Int로 설정되는 것을 볼 수 있다.

만약 다른 타입의 정수를 사용하고 싶다면 변수 명 뒤에 타입을 선언해주면 된다.

```kotlin
var byte : Byte = 1 // Byte  
var short : Short = 1 // Short  
var long : Long = 1 // Long
```

## 실수

실수 타입 number라는 변수를 선언해보았다.

```kotlin
var number = 10.101010
```

결과

![vardouble](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/vardouble.PNG)

실수를 입력하면 기본 타입이 Double로 설정되는 것을 볼 수 있다.

만약 Float 타입의 실수를 사용하고 싶다면 값 뒤에 F를 붙여주면 된다.

```kotlin
var number = 10.101010F
```

-----

# 논리형 변수

논리형 변수인 Boolean을 자바에서 선언하기 위해서는

```java
boolean quiz = true;
```

이런 식으로 변수 선언이 반드시 필요하다.

하지만 Kotlin에서는 다르다.

```kotlin
var quiz = true
```

이게 끝이다.

![varboolean](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/varboolean.PNG)

변수에 할당된 값이 true / false의 경우 자동으로 식별한다.

-----