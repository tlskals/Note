
## init()

Kotlin에서 Init 메서드는 클래스의 초기화 프로세스 중 일부이다.

init은 내용은 클래스 초기화 중에 실행할 코드를 정의할 수 있으며,

인스턴스가 생성될 때 기본 생성자 호출과 보조 생성자의 사이에 실행된다.

이 기능은 속성을 초기화하거나 클래스의 인스턴스가 생성될 때 마다 실행할

코드가 있는 경우에 유용하게 사용된다.

코드로 이해해보자

```kotlin
fun main() {  
    var test = OpenApps()  
}  
class OpenApps() {  
    init {  
        println("Loading.. 1/3")  
    }  
    init {  
        println("Loading.. 2/3")  
    }  
    init {  
        println("Loading.. 3/3")  
    }  
    init {  
        println("Starting!!")  
    }  
}
```

OpenApps 라는 클래스를 정의하고

그 안에 init을 4개나 