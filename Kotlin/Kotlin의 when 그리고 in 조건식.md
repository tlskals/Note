Kotlin에서는 when이라는 메서드가 존재한다.

쉽게 생각하면 자바의 switch/case라고 보면 된다.

## when

when 수 많은 조건을 나열하고 할당된 변수가 조건에 만족할 때

그 조건에 만족하는 명령어를 실행한다.

조건을 설정해보자

Temperatures 라는 변수를 설정하고,

이 값이 30보다 크면 Hot!이라는 값을 출력,
20~30 사이의 값이라면 Cool!
20 이하의 값이라면 Cold! 를 출력한다.

이 조건을 if문으로 코드를 작성해보았다.

```kotlin
fun main() {  
  
    var Temperatures = 25  
  
    if (Temperatures > 30)  
        println("Hot!")  
    else if ((Temperatures >= 20 && Temperatures <= 30))  
        println("Cool!")  
    else println("Cold!")  
}
```

위 코드에서 Temperatures 값은 25이기 때문에 Cool! 이라는 결과 값이 출력된다.

이번에는 when문으로 코드를 작성해보았다.

```kotlin
fun main() {  
  
    var Temperatures = 25  
    
    when {  
        Temperatures > 30 -> println("Hot!")  
        Temperatures in 20..30 -> println("Cool!")  
        else -> println("Cold!")  
    }  
}
```

 위의 두 코드는 같은 결과 값을 출력한다.

여기서 중요한 점은 in 20..30 이다.

자바에서 20보다 크거나 같고 30보다 작거나 같다는 조건을 설정하려면

위의 if문 else if 처럼 두 조건을 &&으로 묶어서 사용해야 한다.

반면 코틀린에서는 in 20..30으로 간단하게 표현할 수 있다.

좀 더 공부해보기 위해 새로운 조건을 설정해보았다.

```kotlin
fun main() {  
  
    var a : Any = 12.34  
  
    when(a){  
        is Int -> println("$a 의 변수 타입은 Int이다.")  
        is Double -> println("$a 의 변수 타입은 Double이다.")  
        else -> println("$a 의 변수 타입은 Int나 Double이 아니다.")  
    }  
}
```

위 코드에서 a의 변수 타입은 double이므로 출력 값은 다음과 같다.

whendouble

변수 a의 값을 String으로 바꾸어 보았다.

```kotlin
fun main() {  
  
    var a : Any = 12.34  
  
    when(a){  
        is Int -> println("$a 의 변수 타입은 Int이다.")  
        is Double -> println("$a 의 변수 타입은 Double이다.")  
        else -> println("$a 의 변수 타입은 Int나 Double이 아니다.")  
    }  
}

```

이 코드의 실행 결과는 다음과 같다.



-------------
## in 조건식

in 조건 식은 다음과 같다.

```kotlin
in x..y
```

이 조건의 x,y를 포함해서 x와 y 사이를 나타낸다.

이 조건을 역으로 설정하기 위해서는 간단하게 자바처럼 in 앞에 !를 추가하면 된다.

```kotlin
!in x..y
```

이 조건은 x,y를 포함해서 x와 y 사이를 제외한 모든 값을 의미한다.

-------------