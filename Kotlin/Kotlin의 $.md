
변수 값을 설정하고 해당 변수 값을 포함한 구문을 출력한다고 생각해보자.

출력 값은 "나의 나이는 (변수 값) 살 입니다."

이걸 자바로 표현하면 다음과 같다.

```java
public static void main(String[] args) {  
    int age = 30;  
    System.out.println("나의 나이는 " + age + "살 입니다.");  
}
```

다음은 위 조건문에서 변수에 +1 한 값을 출력한다고 생각해보자.

```java
    public static void main(String[] args) {  
        int age = 30;  
        System.out.println("나의 나이는 " + (age+1) + "살 입니다.");  
    }  
}
```

