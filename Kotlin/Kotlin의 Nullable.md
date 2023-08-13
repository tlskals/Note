
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



여기서 잠깐

String은 분명 값 타입이 아닌 참조 타입이다.

그리고 참조 타입은 null을 값으로 할당 받을 수 있는데 왜  