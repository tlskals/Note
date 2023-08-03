
# Android Studio란?

Android 스튜디오는 Android 앱 개발을 위한 공식 통합 개발 환경(IDE)입니다. Android 스튜디오는 IntelliJ IDEA의 강력한 코드 편집기와 개발자 도구를 기반으로 Android 앱을 빌드할 때 생산성을 높여주는 다음과 같은 다양한 기능을 제공합니다.

- 유연한 Gradle 기반 빌드 시스템
- 빠르고 기능이 풍부한 에뮬레이터
- 모든 Android 기기용으로 개발할 수 있는 통합 환경
- 에뮬레이터와 실제 기기에서 구성 가능한 함수를 실시간으로 업데이트할 수 있는 실시간 편집
- 일반적인 앱 기능을 빌드하고 샘플 코드를 가져오는 데 도움이 되는 코드 템플릿과 GitHub 통합
- 광범위한 테스트 도구 및 프레임워크
- 성능, 사용성, 버전 호환성 및 기타 문제를 파악하는 린트 도구
- C++ 및 NDK 지원
- Google 클라우드 메시징과 App Engine을 간편하게 통합하는 Google Cloud Platform을 기본적으로 지원

-----

# Android Studio 설치

Android Studio는 아래 링크에서 설치할 수 있습니다.

### https://developer.android.com/studio/archive?hl=ko


------

# Android Studio Main

Android Studio를 설치 후 실행하면 나타나는 화면은 다음과 같습니다.

![Android Studio Main](https://raw.githubusercontent.com/tlskals/img/main/img/AndroidStudioMain.png)


-----

## New Project

Main 화면에서 New Project를 클릭하면 나오는 화면은 다음과 같습니다.

### Phone and Tablet

핸드폰과 태블릿 프로그램을 위한 템플릿

![Phone and Tablet](https://raw.githubusercontent.com/tlskals/img/main/img/NewProject.PNG)


### Wear OS

시계 프로그램을 위한 템플릿


![WearOS](https://raw.githubusercontent.com/tlskals/img/main/img/WearOS.PNG)


### Android TV

Android TV 프로그램을 위한 템플릿

![Android TV](https://raw.githubusercontent.com/tlskals/img/main/img/AndroidTV.PNG)

### Automotive

차량옹 프로그램을 위함 템플릿

![Automotive](https://raw.githubusercontent.com/tlskals/img/main/img/Automotive.PNG)


----------

# Project 시작하기

내가 제작하고 싶은 앱에 맞는 템플릿을 선택하면 다음 창이 나옵니다.

![Empty Activity](https://raw.githubusercontent.com/tlskals/img/main/img/EmptyActivity.PNG)

## Name

해당 프로젝트의 이름

## Package name

스토어에 앱을 출시하려면 고유한 패키지명을 가지고 있어야 한다.
또한 Package명은 소문자로만 작성해야 한다.

## Save loaction

해당 프로젝트가 저장될 Local 위치

## Language

Java / Kotlin을 선택할 수 있으며,
Java의 주인인 Oracle과 Google간의 문제로
Google에서 안드로이드의 언어를 Kotlin으로 지정했기 때문에 Kotlin을 선택하면 된다.

## Minimum SDK

모든 Android기기는 각각의 안드로이드 버전을 가지고 있다.
2023년 8월 기준 Android14가 최신 버전이며, 해당 SDKㄹ