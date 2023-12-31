
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

그 안에 init을 4개나 집어넣었다.

main 함수를 실행하면 나오는 결과는 다음과 같다.

![resultinit](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/resultinit.PNG)

main 함수가 실행될 때마다 test 변수에 있는 OpenApps 클래스가

초기화되며 init의 내용이 실행된다.

또한 위 결과처럼 init은 한 클래스 안에서 여러 개를 사용할 수 있으며,

위에서 정의된 내용부터 실행된다.

------------------

# init에 대한 의문점들

## init은 메서드인가?

결론부터 말하면 init은 메서드가 아닌 Kotlin만의 고유한 특수 기능이다.

이 내용을 ChatGPT한테 물어봤다.

Q . 코틀린의 init은 메서드야?

A. 

![ChatGPTinit1](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/ChatGPTinit1.PNG)
![ChatGPTinit2](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/ChatGPTinit2.PNG)


<strong>여기서 의문이 들었다.<br>
아니 어짜피 클래스 안에 초기화 메서드를 넣어놓으면 인스턴스가 생성될 때마다 실행될텐데 굳이 init이 필요한가? </strong>

## init과 일반적인 초기화 메서드와의 차이

Q . 그럼 regularMethod처럼 함수를 넣으면 되는거아니야? 굳이 init이라는게 필요해?

A.

![ChatGPTinit3](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/ChatGPTinit3.PNG)

이해해보자면 

1. 인스턴스의 초기 상태를 설정하는데 유용하다.
2. 메서드는 호출되서 실행되지만, init은 자동으로 실행된다.
3. 초기화 목적으로만 사용되기 때문에 가독성이 좋아진다.
4. 협업을 할 때 일관된 패턴을 사용하면 다른 개발자가 이해하기 쉽다.
5. 생성자 인수를 기반으로 초기화해야 하는 클래스에서 인수를 다시 전달할 필요가 없다.

5번 내용에 대해서 더 자세히 설명하자면 다음과 같다.

```kotlin
class Person(val name: String, val age: Int) {
	fun initPerson() {
	println("Creating a person named $name, aged $age")
	}
}

class Person(val name: String, val age: Int) {
	init {
		println("Creating a person named $name, aged $age")
		}
	}
```

첫 번째 예시에서는 Person 클래스를 초기화 할 때마다

initPerson 메서드를 호출하고 name과 age를 전달해야 하지만,

두 번째 예시에서는 다시 전달할 필요가 없다.

즉, init을 사용하면 코드가 더 일관되고 간소화될 수 있으며,

추가 매개변수 전달 없이 생성자 인수에 직접 접근할 수 있다.

--------------