---
layout: page
title: 자바 Print 종류
---

## **System.out.println();**

**자바의 기본적인 출력명령어이다.**

```Java
System.out.println("Number의 값은 ? : " + num);

System.out.println("Character의 값은 ? : " + character);
```

***

## **System.out.print();**

**이 또한 자바의 출력명령어이다.**

**println과의 차이점은 줄바꿈을 따로 해주지 않는다는 것이다.**

```Java
System.out.print("Number3의 값은 ? : " + num3);
```

***

## **System.out.printf();**

**printf()는 지시자를 통해 변수의 값을**

**여러 가지 형식으로 변환하여 출력할 수 있다.**

```Java
System.out.printf("Number4의 값은 ? : %d\n", num4);
```