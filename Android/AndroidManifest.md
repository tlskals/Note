
# AndroidManifest란?

Android 프로젝트를 생성하면 기본적으로 MainActivity, res 패키지 등

애플리케이션에 필요한 파일들이 생성된다.

그런데 프로젝트 최상단에 보면 manifests란 폴더가 있고,

그 안에 AndroidManifest.xml 이라는 파일이 존재한다.

그 예시는 다음과 같다.

```xml
<?xml version="1.0" encoding="utf-8"?>  
<manifest xmlns:android="http://schemas.android.com/apk/res/android"  
    xmlns:tools="http://schemas.android.com/tools">  
  
    <application        
	    android:allowBackup="true"  
        android:dataExtractionRules="@xml/data_extraction_rules"  
        android:fullBackupContent="@xml/backup_rules"  
        android:icon="@mipmap/ic_launcher"  
        android:label="@string/app_name"  
        android:roundIcon="@mipmap/ic_launcher_round"  
        android:supportsRtl="true"  
        android:theme="@style/Theme.QuizApp"  
        tools:targetApi="31">  
        <activity            
	        android:name=".QuizeQeustionsActivity"  
            android:exported="false" />  
        <activity            
	        android:name=".MainActivity"  
            android:exported="true"  
            android:screenOrientation="portrait">  
            <intent-filter>                
            <action android:name="android.intent.action.MAIN" />  
  
                <category android:name="android.intent.category.LAUNCHER" />  
            </intent-filter>        
        </activity>    
    </application>  
</manifest>
```

이 XML에는 앱의 이름, Anroid API 버전, 테마 등의 내용과

권한, 보안, 액티비티 등의 내용을 담고있다.

쉽게 말해서 이 AndroidManifest.xml 파일은

<strong>해당 프로젝트에 적용되는 사양들을 모아놓은 파일이다.</strong>

<strong>또한 이 파일에서 정의 되지 않은 요소는 앱의 구성요소로 인식되지 않아서

사용할 수 없다.</strong>

-----------------------

# Manifest에서 명시해야 하는 내용

Manifest에서 정의되는 수 많은 정보 중 반드시 선언되어야 하는 정보들이 있다.

1. 앱의 패키지 이름
2. 앱의 구성 요소 (Activity, Service, Broadcast Recevier, ContentProvider)
3. 앱에서 필요한 권한

```xml
<?xml version="1.0" encoding="utf-8"?>  
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
	package="com.example.alarmmanager"
    xmlns:tools="http://schemas.android.com/tools">  
  
    <uses-permission android:name="android.permission.SET_ALARM" />  
    <uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED" />  
    <uses-permission android:name="android.permission.FOREGROUND_SERVICE" />  
  
    <application        android:allowBackup="true"  
        android:dataExtractionRules="@xml/data_extraction_rules"  
        android:fullBackupContent="@xml/backup_rules"  
        android:icon="@mipmap/ic_launcher"  
        android:label="@string/app_name"  
        android:roundIcon="@mipmap/ic_launcher_round"  
        android:supportsRtl="true"  
        android:theme="@style/Theme.MyApplication"  
        tools:targetApi="31">  
  
  
        <activity            
	        android:name=".MainActivity"  
            android:exported="true">  
            <intent-filter>                
	            <action android:name="android.intent.action.MAIN" />  
                <category android:name="android.intent.category.LAUNCHER"/> 
            </intent-filter>
         </activity>  
        <receiver            
	        android:name=".AlarmReceiver"  
            android:enabled="true"  
            android:exported="false">  
            <intent-filter>                
            <action android:name="com.example.myapplication.ALARM_TRIGGERED" />  
            </intent-filter>
         </receiver>
     </application>
</manifest>
```

## 앱의 패키지 이름

이 코드에서 보면

상단 3번째 줄에

```xml
package="com.example.alarmmanager"
```

이렇게 패키지 명을 명시해 놓고 있다.

물론 여기서 이 패키지명을 명시하지 않아도 로컬에서 애플리케이션을 실행하는데

문제가 발생하진 않는다.

하지만 이게 배포를 하게 된다면 달라진다.

패키지 명은 앱을 식별하는 데 사용되며, 추 후 패키지 이름을 변경할 경우 심각한</br>문제가 발생할 수 있으므로 개발 초기에 명시하는 것이 좋으며,

이는 Google Play 스토어처럼 배포할 때, 앱이 올바르게 식별되어</br>
이로 인해 발생할 수 있는 문제들을 사전에 예방할 수 있다.

또한
