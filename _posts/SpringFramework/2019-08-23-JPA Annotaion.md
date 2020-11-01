---
layout: post
title: "JPA"
date: 2019-08-23 23:44
categories: SpringFramework
comments: true
---

# JPA Annotaion

@Id

@Column

@OneToOne


---

# JPA Projection

Spring JPA Projection

Projection 뜻대로 엔티티의 전체 데이터 중에서 일부 데이터만 가져오는 기능.

인터페이스 기반으로 구현. 

이 인터페이스로 Repo에 반환값을 명시하면 데이터를 커스텀해서 가져올 수 있다.

프로젝션은 Closed와 Open 형이 있는데,

Open형은 Spring Data가 최적화를 하지 못하므로

Closed형으로 핸들링이 안될 경우에만 사용하도록 한다.


nested projection

참고 : 
https://www.logicbig.com/tutorials/spring-framework/spring-data/nested-properties-resolution.html
https://engkimbs.tistory.com/836
