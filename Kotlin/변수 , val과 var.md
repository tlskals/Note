
# 변수

Kotlin에서 변수 선언에는 val (Value) / var (variable)을 사용한다.

각각에 대해서 이해해보자.

-----------

# var (variable)

먼저 var에 대한 설명이다.

이해하기 쉽게 코드를 작성하였다.

```kotlin
fun main() {  
    var myName = "시나민"  
    print("내 이름은 " + myName)  
}
```

이 코드를 실행시키면 다음과 같은 결과가 나온다.

![var결과1](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/var결과1.PNG)

이번에는 myName이라는 변수에 값을 할당한 코드이다.

```kotlin
fun main() {  
    var myName = "시나민"  
    myName = "시나민이 아닙니다."  
    print("내 이름은 " + myName)  
}
```

이 코드의 결과 값은 다음과 같다.

![var결과2](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/var결과2.PNG)

**즉 var 라는 변수는 중간에 값을 수정이 가능하다.

------

# val (Value)

다음으로 val에 대한 설명이다.

이 또한 이해하기 쉽게 코드를 작성하였다.

```kotlin
fun main() {  
    var myName = "시나민"  
    print("내 이름은 " + myName)  
}
```

위 코드의 결과 값은 다음과 같다.

![val결과](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/val결과.PNG)

var 변수 초기 결과와 같은 결과가 나온다.

var 때와 마찬가지로 myName의 값을 수정해보았다.

![val수정](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/val수정.PNG)

왜 빨간 줄이 뜨는지 마우스를 대보았다.

![valErrorLog](https://raw.githubusercontent.com/tlskals/img/main/Kotlin/valErrorLog.PNG)

Val Cannot be reassigned

한국말로 번역하면 "val는 재 할당 될 수 없다."

**즉 val 라는 변수는 중간에 값을 수정이 불가능하다.

---------

# val는 상수인가?

앞서 보았듯이 val라는 변수는 값은 한 번 할당되면 재 할당이 불가능하다.

그렇다면 val는 변수가 아닌 상수인가? 라는 의문이 들었다.

Google에 검색해보았다.

valGoogling

대부분의 포스팅에서 val는 상수로 정의하고 있다.

그런데 어떤 블로그에서 신기한 내용을 발견했다.

https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=rndrnjs2003&logNo=221328830006

이 블로그의 내용을 보자면

**"val는 상수가 아닌 변수이지만 내부에 setter를 갖고 있지 않아 수정이 불가능 할 뿐이다."** 라는 이야기다.

이 부분에 대해 좀 더 의구심이 생겨 ChatGPT를 사용했다.

질문 : Val는 변수야? 상수야?

답변은 다음과 같았다.

