# if문과 변수 타입

지난 번에 var와 val에 대해서 공부했다.


var는 가변인 변수 타입을 지정할 때 사용하며,</br>
val는 불변인 변수 타입을 지정할 때 사용한다.

그렇다면 이러한 변수 타입들을 조건문인 if에 넣어보면 어떻게 될까?

## if + var

```kotlin
var thirsty = true  
  
if (thirsty){  
    print("물을 마신다.")  
}
```

먼저 가변 변수인 var를 넣어보았다.

varThirsty

Android Studio에서 제안이 들어온다.

이 코드를 실행하면 다음과 같은 결과가 나온다.

varThirstyResult

## if + val

당