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

여기서 중요한 점은 