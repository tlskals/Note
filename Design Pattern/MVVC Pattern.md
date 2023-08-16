
# MVVM Pattern

MVVM 패턴이란 디자인 패턴 중 하나로

우리가 흔히 알고 있는 MVC 패턴과 유사하다.

MVVM 패턴은 주로 iOS 애플리케이션 개발에 사용되며,

기존 UIKit에서 SwiftUI로 넘어오면서 점차 늘어가는 추세이다.

# Why MVVM?

그렇다면 왜 기존에 사용하던 MVC 에서 새롭게 나온 MVVM으로 바뀌어가는 걸까?

## UIKit의 MVC




이 사진은 MVC 패턴의 구조이다.

UIkit의 MVC에서는 ViewController가 가장 중요한 역할을 맡는다.

ViewContoller는 View와 Model을 모두 소유하고 있으며,

Model의 notification 및 View와 유저 간의 상호작용을 전달하는 방식도 모두

Controller에 대한 Deleagtion 방식으로 이루어져 있다.

이러한 방식은 각 계층의 결합도를 증가시켜 재사용성과 테스트 측면에서

불리하다.

또한 View Controller는 너무 많은 임무를 떠안고 있다.

View Controller는 비지니스 로직을 가지면서, 

View에 대한 설정, 수정 등의 코드를 갖고 있기 때문에

안 그래도 강한 결합을 더더욱 분리하기 힘들게 된다.

## SwiftUI의 MVVM



이 사진은 MVVM 패턴의 구조이다.

MVC 패턴이 View <-> Controller <-> Model로 구성되어 있다면,

MVVM 패턴은 View -> View Model -> Model로 구성되어 있다.

이 패턴은 Controller가 중간에서 모두를 소유하는 구조가 아닌

View는 View Model을 소유하고, View Model은 Model을 소유하는 구조이다.

또한 MVC 패턴에서는 Controller가 주체가 되었다면,

MVVM에서는 View가 주체가 되어 화면을 주도한다.

이러한 방식은 각 계층을 모듈화 시켜 UI와 비지니스 로직을 독립적으로 테스트 할 수 있다.

또한 View와 ViewModel이 1:N 관계이므로 중복되는 로직을 모듈화하여

재사용에도 용이하다.

# MVVM 패턴의 구성


## View

MVVM 패턴에서 View는 UI에 대한 코드 및 생명주기 코드를 다룬다.

또한 ViewModel로부터 가져온 데이터를 어떻게 배치할지, 특정 상황에 따라

View Controller의 어떤 메서드를 사용할지에 대해서도 가지고있다.


## View Model

MVVM 패턴에서 View Model은 애플리케이션의 비지니스 로직을 담고 있다.

View에서 이벤트가 발생하면 그에 맞는 비지니스 로직을 수행하고,

Model이 갖고 있는 데이터에 변화를 준다.

또한 Model이 변경되면 자동으로 View 또한 변경될 수 있도록

<strong>데이터 바인딩</strong>을