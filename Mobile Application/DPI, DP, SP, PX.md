
스마트폰이 출범한 이후로 수 많은 크기의 디바이스가 시장에 출시되었다.

하지만 각각의 디바이스에 맞게 애플리케이션을 맞춤제작해야 한다면
이는 정말 스마트하지 못한 방식을 것이다.

그렇기 때문에 어떠한 디바이스에서도 적용 가능하게 애플리케이션을</br>
만드는 것은 중요하다.

# DPI (Dot Per Inch)

DPI란 1Inch당 몇 개의 도트로 구성되어 있는지 나타내는 단위이다.

![DPI](https://raw.githubusercontent.com/tlskals/img/main/MobileApplication/DPI.PNG)

위 사진에서 볼 수 있듯, 72 dpi는 가로 세로 각각 72x72 dot로 구성되어 있다.

하지만 애플리케이션에서는 이 dpi를 더 큰 분류로 사용한다.

![AppDPI](https://raw.githubusercontent.com/tlskals/img/main/MobileApplication/AppDPI.PNG)

hdpi / mdpi / xhdpi / xxhdpi / xxxhdpi 로 구성되어 있는 것을 볼 수있다.

이는 아래 사진처럼 각각의 요소가 정해져 있다.

![AndroidDPI](https://raw.githubusercontent.com/tlskals/img/main/MobileApplication/AndroidDPI.png)

------------------

# DP/DIP (Density Indenpendent Pixel)

DP란 안드로이드 디바이스에 존재하는 해상도(hdpi, mdpi 등)을 지원하기 위해 만들어진 단위로, 큰 화면이든 작은 화면이든 같은 비율로 적용된다.

극단적으로 hdpi에서 화면 중간에 절반 크기의 버튼이 있다면,
이는 xxxhdpi에서도 절반 크기의 버튼으로 그려져야 한다.

-----------------

# SP (Scalable Pixel)

DP가 해상도와 상관없이 같은 크기의 뷰를 보기위한 용도라면,

SP는 시스템에 따라 커지거나 작아지는, 즉 스케일이 적용되는 단위이다.

주로 TextSize 등에 사용된다.

--------------------

# PX

PIXEL은 디바이스의 실제 크기나 밀도에 관계 없이 고정된 픽셀 단위를 의미한다.

그렇기 때문에 다양한 크기의 디바이스에서 사용되려면 PX 사용은 가급적 지양해야 한다.

DPI 따라 각 픽셀의 크기 DP와 비교해 볼 수 있다.

```
ldpi - 1dp = 0.75px
mdpi - 1dp = 1px
hdpi - 1dp = 1.5px
xdpi - 1dp = 2px
```

-------------------




