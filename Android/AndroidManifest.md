
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

<strong>해당 프로젝트에 적용되는 사양들을 모아놓은 파일이다.

</br또한 이 파일에서 정의 되지 않은 요소는 앱의 구성요소로 인식되지 않아서

사용할 수 없다.</strong>

-----------------------

# Manifest에서 명시하는 내용

