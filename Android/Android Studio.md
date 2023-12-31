
# Android Studio란?

안드로이드 공식 문서의 설명이다.

Android 스튜디오는 Android 앱 개발을 위한 공식 통합 개발 환경(IDE)입니다. </br>Android 스튜디오는 IntelliJ IDEA의 강력한 코드 편집기와 개발자 도구를 기반으로</br> Android 앱을 빌드할 때 생산성을 높여주는 다음과 같은 다양한 기능을 제공합니다.

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

Android Studio는 아래 링크에서 설치할 수 있다.

### https://developer.android.com/studio

아래 링크에서는 지난 버전을 골라 설치할 수 있다.
### https://developer.android.com/studio/archive?hl=ko


------

# Android Studio Main

Android Studio를 설치 후 실행하면 나타나는 화면은 다음과 같다.

![Android Studio Main](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/AndroidStudioMain.png)


-----

## New Project

Main 화면에서 New Project를 클릭하면 나오는 화면은 다음과 같다.

### Phone and Tablet

핸드폰과 태블릿 프로그램을 위한 템플릿

![Phone and Tablet](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/NewProject.PNG)


### Wear OS

시계 프로그램을 위한 템플릿


![WearOS](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/WearOS.PNG)


### Android TV

Android TV 프로그램을 위한 템플릿

![Android TV](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/AndroidTV.PNG)

### Automotive

차량옹 프로그램을 위함 템플릿

![Automotive](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/Automotive.PNG)


----------

# Project 시작하기

내가 제작하고 싶은 앱에 맞는 템플릿을 선택하면 다음 창이 나온다.

![Empty Activity](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/EmptyActivity.PNG)

## Name

해당 프로젝트의 이름

## Package name

스토어에 앱을 출시하려면 고유한 패키지명을 가지고 있어야 한다.</br>
또한 Package명은 소문자로만 작성해야 한다.

## Save loaction

해당 프로젝트가 저장될 Local 위치

## Language

Java / Kotlin을 선택할 수 있으며,</br>
Java의 주인인 Oracle과 Google간의 문제로</br>
Google에서 안드로이드의 언어를 Kotlin으로 지정했기 때문에 Kotlin을 선택하면 된다.

## Minimum SDK (Software Development Kit)

모든 Android기기는 각각의 안드로이드 버전을 가지고 있다.</br>
2023년 8월 3일 기준 Android14가 최신 버전이며,</br>
Android Studio에서 제작할 수 있는 최고 버전은 Android12이다.</br>
또한 Android12 지정했을 때 나오는 현재 보급률은 31.3%이다. 

즉, 68.7%의 기기에서 Android12를 제작한 앱을 사용할 수 없다는 뜻이다.

이는 앱을 설계할 때 중요한 요소이며, 상위 버전에서는 하위 버전을 포함하고 있으니,</br>
범용적이면서 내가 구상한 앱에 필요한 요소가 있는지 확인 후 선택해야 한다.


------

# Android Studio

![Android Studio](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/AndroidStudio.PNG)

누가 Jetbrains 에서 만든 언어가 아니랄까봐</br>
IntelliJ의 화면과 99%는 똑같다.

## MainActivity.kt

![Main Activity](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/MainActivity.PNG)

Project Run에 관한 파일이다. (자바로 치면 ServerApplication.java 파일이 되겠다.)</br>
확장자인 kt는 Kotlin을 의미한다.

## activity_main.xml

![activity_main.xml](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/ActivityMain.PNG)

음.. Java 프로젝트에서는 볼 수 없었던 파일이다.</br>
해당 파일은 애플리케이션의 UI(User Interface)에 관한 파일이다.

MainActivity.kt의 코드에서 setContentView라는 메서드를 이용하여 해당 프로젝트와 연동된다.

```kotlin
class MainActivity : AppCompatActivity() {  
    override fun onCreate(savedInstanceState: Bundle?) {  
        super.onCreate(savedInstanceState)  
        setContentView(R.layout.activity_main)  
    }  
}
```

-------

# Android Emulator

Android Studio에서 생성한 애플리케이션을 Android Emulator를 이용하여
테스트 해볼 수 있다.

![Emulator](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/Emulator.PNG)

![VirtualDevices](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/VirtualDevices.PNG)

이제 Create Virtual Device...를  눌러 Emulator의 설정을 고르면 된다.

## Select Hardware

![SelectHardware](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/SelectHardware.PNG)

Device의 Hardware를 선택하는 공간이다.

좌측에 어떤 기기를 사용할 것 인지에 대한 Category가 있으며,</br>
Category를 설정한 후에는 세부 설정을 진행할 수 있다.

Play Store 부분을 보면 특정 기기에서는 Play Store 애플리케이션 마크가 적용되어 있는데, 이는 해당 설정을 적용했을 때 Play Store를 설치할 수 있으며, Play Store 확장자를 이용할 수 있다.


## System Image

![SystemImage](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/SystemImage.PNG)

Android Studio 버전을 선택하는 공간이다.

현재 PC에 맞는 시스템 버전을 골라야 하며, Intel 사용자가 AMD 버전을 골랐을 경우</br>
다음과 같이 우측 하단에 Recommendation으로 메세지를 표기해준다.

![SystemImageRecommendation](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/SystemImageRecommendation.PNG)

자신에게 맞는 시스템을 선택했다면 Download 버튼을 클릭한다.

아래와 같은 License Agreement 창이 나오고 동의를 누르면,</br>
해당 버전의 System이 설치된다.

![LicenseAgreement](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/LicenseAgreement.PNG)

![ComponentInstaller](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/ComponentInstaller.PNG)

설치가 완료되었다면 다음과 같이 시스템 버전을 선택 후 Next로 넘어가면 된다.

![SystemImageInstalled](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/SystemImageInstalled.PNG)

## Android Virtual Device

![AndroidVirtualDevice](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/AndroidVirtualDevice.PNG)

생성할 Virtual Device의 세부 설정을 선택하는 공간이다.

해당 기기의 이름을 선택할 수 있고, </br>
가로, 세로 등의 세부 설정을 할 수 있다.

또한 하단의 Show Advanced Settings를 눌러 더 세세한 부분까지 설정할 수 있다.

![ShowAdvancedSettings](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/ShowAdvancedSettings.PNG)

또한 위에서 설정한 모든 사항은 언제든 수정이 가능하다.

Finish를 누르면 처음 화면으로 돌아온다.

보이는 이미지와 같이 내가 생성한 Device가 추가된 것을 볼 수 있으며,</br>
Android Studio 상단의 run 아이콘이 활성화 된 것을 확인할 수 있다.

![DeviceAdded](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/DeviceAdded.PNG)

-------

# Error 발생

내가 생성한 Device를 선택하고 Run 버튼을 누르니 Error가 발생했다.

![BuildError](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/BuildError.PNG)

```
Failed to install the following Android SDK packages as some licences have not been accepted. build-tools;30.0.2 Android SDK Build-Tools 30.0.2
```

내용을 보고 구글링을 해보니 SDK License에서 문제가 생긴 듯 하다.

Settings에 들어가서 확인해 보았다.

![SDKSettings](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/SDKSettings.PNG)

License에 관련된 내용이 Google Play Licensing Library뿐이라 먼저 설치해 보았다.

![LicenseInstalled](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/LicenseInstalled.PNG)

다시 Run 버튼을 클릭하여 정상적으로 설치했는지 확인해 보았다.

![EmulatorRun](https://raw.githubusercontent.com/tlskals/img/main/AndroidStudio/EmulatorRun.PNG)

Error가 사라지고 Application이 정상적으로 실행된다.

----------------


