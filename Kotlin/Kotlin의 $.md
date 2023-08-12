
변수 값을 설정하고 해당 변수 값을 포함한 구문을 출력한다고 생각해보자.

출력 값은 "나의 나이는 (변수 값) 살 입니다."

이걸 자바로 표현하면 다음과 같다.

```java
public static void main(String[] args) {  
    int age = 30;  
    System.out.println("나의 나이는 " + age + "살 입니다.");  
}
```

다음은 위 조건문에서 변수에 +1 한 값을 출력한다고 생각해보자.

```java
    public static void main(String[] args) {  
        int age = 30;  
        System.out.println("나의 나이는 " + (age+1) + "살 입니다.");  
    }  
}
```

각각의 코드의 출력 결과는 아래와 같다.

java30살

java31살

## $

자바에서 작성한 코드를 코틀린으로 옮겨보았다.

```kotlin
fun main() {  
  
    var age = 30  
    println("나의 나이는" + age + "살 입니다.")  
}
```

```kotlin
fun main() {  
  
    var age = 30  
    println("나의 나이는" + (age+1) + "살 입니다.")  
}
```

그저 변수인 int가 var로 바뀌었을 뿐이다.

하지만 $를 사용하면 출력문을 좀 더 편하게 작성할 수 있다.

다음은 $를 사용한 코드이다.

```kotlin
fun main() {  
  
    var age = 30  
    println("나의 나이는 ${age}살 입니다.")  
}
```

```kotlin
fun main() {  
  
    var age = 30  
    println("나의 나이는 ${age+1}살 입니다.")  
}
```

print문을 "구문" + 변수 + "구문"으로 나누지 않고, </br>
"구문(변수 포함)" 하나로 쉽게 출력할 수 있다.

이 코드의 출력 값은 다음과 같다.

kotlin30살

kotlin31살

-----------------
