
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

그 후 tlskals이라는 값을 할당하고