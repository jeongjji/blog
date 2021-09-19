---
layout: page
title: 어노테이션 annotation
---

## @RestController

RestController란 스프링프레임워크 4.x 버전 이상부터 사용가능한 어노테이션으로 @Controller에 @ResponseBody가 결합된 어노테이션이다. 컨트롤러 클래스에 @RestController를 붙이면, 컨트롤러 클래스 하위 메서드에 @ResponseBody 어노테이션을 붙이지 않아도 문자열과 JSON 등을 전송할 수 있다.

@Controller와 달리 @RestController는 컨트롤러 클래스의 각 메서드마다 @ResponseBody를 추가할 필요가 없어졌다.

---

## @Getter, @Setter

Lombok에서 가장 많이 쓰이는 어노테이션으로 말 그대로 Get하는 메소드와 Set하는 메소드를 자동으로 생성해준다.

예를 들어 name이라는 변수 위에 @Getter와 @Setter를 달아주면

```java
@Getter @Setter
private String name;
```

getName과 setName이라는 메서드를 사용 가능하다.

```java
user.setName("아리아나 그란데");

System.out.println(user.getName);
```

---

## @RequiredArgsConstructor

@RequiredArgsConstructor은 초기화 되지않은 final 필드나, @NonNull 이 붙은 필드값을 파라미터로 받는 생성자를 생성해 줍니다. 주로 의존성 주입(Dependency Injection) 편의성을 위해서 사용되곤 합니다.

쉽게 말해, final이나 @ntNull이 붙은 필드에 의존성 주입을 시켜주는 어노테이션이다.

---

## @AllArgsConstructor

@AllArgsConstructor은 final이나 @NotNull이 붙은 필드에 생성자를 자동으로 생성해주는 @RequiredArgsConstructor와 달리 모든 필드를 파라미터로 받는 생성자를 자동으로 생성해준다.

---

## @Data

@Getter, @Setter, @RequiredArgsConstructor, @ToString, @EqualsAndHashCode을 한꺼번에 설정해주는 매우 유용한 어노테이션이다.

클래스 레벨에서 @Data 어노테이션을 붙여주면, 모든 필드를 대상으로 접근자와 설정자가 자동으로 생성되고, final 또는 @NonNull 필드 값을 파라미터로 받는 생성자가 만들어지며, toStirng, equals, hashCode 메소드가 자동으로 만들어진다.
