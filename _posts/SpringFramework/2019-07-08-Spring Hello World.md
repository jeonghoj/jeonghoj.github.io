---
layout: post
title: "Spring Hello World"
date: 2019-07-08 12:28
categories: SpringFramework
comments: true
---

Spring 프로젝트를 해보자.

먼저 시작은 Hello world 부터!

STS도 있지만 IntelliJ가 더 익숙해서 IntelliJ IDEA로 프로젝트를 시작.

Create Project

Type은 *Maven Project
JAVA는 8버전으로

플러그인은 

spring-boot-starter-web  
spring-boot-starter-thymeleaf  
spring-boot-devtools  

를 추가한다.

Commend Line에서 Spring을 run 하려면 해당 경로로 가서 
```
#maven을 이용하여 run 
$./mvnw spring-boot:run
```
[참고](https://docs.spring.io/spring-boot/docs/current/reference/html/using-boot-running-your-application.html)

그리고 src/main/java에
GreetingController.java 추가
```java
@Controller
public class GreetingController {
    @GetMapping("/greeting")
    public String greeting(@RequestParam(name="name",required = false,defaultValue = "world") String name, Model model){
        model.addAttribute("name",name);
        return "greeting";
    }
}
```
HelloworldApplication.java 추가

```java
@SpringBootApplication
public class HelloworldApplication {

    public static void main(String[] args) {
        SpringApplication.run(HelloworldApplication.class, args);
    }

}
```

src/main/resources/templates에  
greeting.html 추가

```html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>Hello world</title>
</head>
<body>
<p th:text="'Hello, ' + ${name} + '!!'"></p>
</body>
</html>

```

http://localhost:8080/greeting 에 가면  
hello world를 볼 수 있다.


*Maven은 node의 NPM같이 프로젝트 빌드를 자동화해주는 툴.
플러그인 기반으로 동작
pom.xml 사용

[참고](https://jeong-pro.tistory.com/168)


[참고](https://madplay.github.io/post/create-springboot-project-in-intellij)
