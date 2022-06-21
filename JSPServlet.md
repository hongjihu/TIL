## JSP VS Servlet

- Servlet와 JSP의 개념

기능의 큰차이는 없지만 역할의 차이정도 만 있다.

- Servlet

  - 웹기반의 요청에 대한 동적인 처리가 가능한 Server Side 에서 돌아가는 Java Program
  - JAVA코드 안에 html 코드 (하나의 클래스)
  - 웹개발을 위해 만든 표준

- JSP

  - JAVA 언어를 기반으로하는 Server Side 스크립트 언어
  - HTML 코드안에 JAVA코드
  - Servlet를 보완하고 기술을 확장한 스크립트 방식 표준
  - Servlet의 모든기능 +추가적인 기능

  

​	![jsp-definition](C:\Users\User\Downloads\jsp-definition.png)

### Servlet와 JSP의 차이

Servlet

- Java 코드 안에 HTML 코드 (하나의 클래스)
  data processing(Controller)에 좋다.
  즉 DB와의 통신, Business Logic 호출, 데이터를 읽고 확인하는 작업 등에 유용하다.
  Servlet이 수정된 경우 Java 코드를 컴파일(.class 파일 생성)한 후 동적인 페이지를 처리하기 때문에 전체 코드를 업데이트하고 다시 컴파일한 후 재배포하는 작업이 필요하다. (개발 생산성 저하)

JSP

- HTML 코드 안에 Java 코드
  presentation(View)에 좋다.
  즉 요청 결과를 나타내는 HTML 작성하는데 유용하다.
  JSP가 수정된 경우 재배포할 필요가 없이 WAS가 알아서 처리한다. (쉬운 배포)



### Servlet 와 JSP의 관계

JSP만을 이용하는 모델![servlet-jsp-model1](C:\Users\User\Downloads\servlet-jsp-model1.png)



- JSP가 사용자의 요청을 받아 Java Bean(DTO, DAO)을 호출하여 적절한 동적인 페이지를 생성한다.
- 특징
  - 개발속도가 빠르다
  - 배우기 쉽다
  - 프레젠테이션 로직과 비즈니스로직이 공존한다.
  - JSP 코드가 복잡해져 유지보수가 어려워진다.

### JSP 와 Servlet 을 모두 이용하는 모델 (MVC Architecture)

- JSP와 Servlet을 모두 사용하여 프레젠테이션 로직(View)과 비즈니스 로직(Controller)을 분리한다.
  View(보여지는 부분)는 HTML이 중심이 되는 JSP를 사용
  Controller(다른 자바 클래스에 데이터를 넘겨주는 부분)는 Java 코드가 중심이 되는 Servlet을 사용
  Model은 Java Beans로, DTO와 DAO를 통해 Mysql과 같은 Data Storage에 접근



### 참고자료

https://gmlwjd9405.github.io/2018/11/04/servlet-vs-jsp.html