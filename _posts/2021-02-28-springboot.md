---
layout: page
title: SpringBoot
---
## **Controller**

**컨트롤러는 사용자의 요청을 처리 한 후 지정된 뷰에 모델 객체를 넘겨주는 역할을 한다.**

***

## **Service**

**Service 가 Client 의 요청에 대한 올바른 정보를 제공하기 위한 처리를 하는데,**
**이것을 비지니스 로직을 처리한다고 말한다.**

1) Client 가 Request 를 보낸다.

2) Request URL에 알맞은 Controller 가 수신한다.

3) Controller 는 넘어온 요청을 처리하기 위해 Service 를 호출한다.

4) Service 는 알맞은 정보를 가공하여 Controller 에게 데이터를 넘긴다.

5) Controller 는 Service 의 결과물을 Client 에게 전달해준다.







