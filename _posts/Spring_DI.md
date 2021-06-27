---
title: Spring-DI(의존성 주입)
---
DI(Dependency Injection)란 스프링이 다른 프레임워크와 차별화되어 제공하는 의존 관계 주입 기능으로,
객체를 직접 생성하는 게 아니라 외부에서 생성한 후 주입 시켜주는 방식이다.

DI(의존성 주입)를 통해서 모듈 간의 결합도가 낮아지고 유연성이 높아진다.


의존성 주입의 대표적인 예로는 외부에서 생성 된 객체를 setter()나 생성자를 통해 사용하는 방법이 있다.
즉, A 객체에서 B, C객체를 사용(의존)할 때 A 객체에서 직접 생성 하는 것이 아니라 외부(IOC컨테이너)에서 생성된 B, C객체를 조립(주입)시켜 setter 혹은 생성자를 통해 사용하는 방식이다.

***

## 생성자 주입
```java
public class TestController {
    private final TestService testService;
    
    public TestController(TestService testService) { // 생성자
        this.testService = testService;
    }
}
```

컨트롤러 class에 testService객체를 생성자를 통해 주입함으로써
컨트롤러에서 testService(서비스)의 매서드를 사용할 수 있다.

생성자가 2개 이상일 때는 @Autowired 어노테이션을 붙여줘야 한다.

스프링부트에서 가장 권장하고 있는 방식이다.

***

## 필드 주입
```java
public class TestController {

    @Autowired
    private TestService testservice;

}
```

가장 편리한 주입 방식이다. 
필드에 @Autowired 어노테이션을 붙여주면 의존성이 주입된다.

***

## 세터 주입(setter)
```java
public class TestController {
    private Testservice testservice;

    public void set_Testservice(Testservice testservice) {
        this.testservice = testservice;
    }
}
```

세터를 통한 주입 방식이다.

***

## 생성자 주입 방식의 장점

스프링부트가 생성자 주입 사용을 권장하는 이유는 다음과 같다.

**1. 순환 참조 방지**

**2. final 선언 가능**

**3. 테스트 코드 작성 용이**