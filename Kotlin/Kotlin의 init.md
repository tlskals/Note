
## init()

Kotlin에서 Init 메서드는 클래스의 초기화 프로세스 중 일부이다.

init 메서드는 내용은 클래스 초기화 중에 실행할 코드를 정의할 수 있으며,

init에 정의된 내용은 기본 생성자 생성과 보조 생성자의 사이에 실행된다.

코드로 이해해보자

```kotlin
fun main() {  
    var test = OpenApps()  
}  
class OpenApps() {  
    init {  
        println("Loading..")  
    }  
}
```

