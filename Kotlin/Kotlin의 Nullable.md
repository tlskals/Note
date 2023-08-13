
# Nullable

Nullable이란 쉽게 말해서 null을 가질 수 없는 데이터 타입들이</br>
값으로 null을 가질 수 있게 하는 것이다.

대표적으로 값 타입(Value Type)들이 이에 해당한다.</br>
ex) int, double, bool 등

-------------------

# Kotlin의 Nullable

다음 코드를 살펴보자

```kotlin
fun main() {  
  
    var name : String = "tlskals"  
    name = null  

}
```

name이라는 변수를 생성하고 해당 변수의 타입을 String으로 명시했다.

그 후 tlskals이라는 값을 할당하고, 값을 null로 변경하는 코드이다.

당연히 컴파일 오류가 발생한다.

nullName

-----------------------

여기서 잠깐

String은 분명 값 타입이 아닌 참조 타입이다.

그리고 참조 타입은 null을 값으로 할당 받을 수 있는데 왜 컴파일 오류가 발생할까?

## String의 타입

ChatGPT에게 물어봤다.

<strong>Q.  String은 참조 타입인데 왜 null 값을 할당 받지 못하는 거야?</strong>

A. 

ChatGPTString


한마디로 String은 자주 사용되는 타입이라 다른 참조 타입과는 다르게 null을 넣었을 때 </br>
문제 발생 확률이 높아서 프로그램 내에서 의도적으로 컴파일 오류를 발생시키는 것이다.

----------------------------

다시 코드로 넘어와서 그렇다면 nullable 설정은 어떻게 하는 것일까?

간단하다. Type 뒤에 '?' 를 넣어주면 된다.

```kotlin
fun main() {  
  
    var name1 : String? = "tlskals"  
    name1 = null  
  
}
```

당연히 컴파일 오류가 발생하지 않는다.

name1Null

------------------------------

# Nullable 응용

그렇다면 nullable을 응용해보자.

## 변수의 Property에 넣어보기

```kotlin
fun main() {  
  
    var name : String? = "tlskals"  
    name = null  
    }
```

위 코드에서 name의 길이를 계산해보자.

```kotlin
fun main() {  
  
    var name : String? = "tlskals"  
    name = null  
  
    var len = name.length  
  
}
```

lenname

당연히 컴파일 에러가 발생한다.

해결하려면 name.length를 name?.length로 변경하면 된다.

```kotlin
fun main() {  
  
    var name : String? = "tlskals"  
    name = null  
  
    var len = name?.length  
  
}
```

---------------------

# 엘비스 연산자 (Elvis Operation)

엘비스 연산자는 ?:로 표현된다.

만약 좌항의 값이 null이 아니라면 그 값을 리턴하고, null이라면 우항의 값을 리턴한다.

코드로 알아보자.

