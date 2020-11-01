---
layout: post
title: "Spring boot DB 접근"
date: 2019-08-22 14:31
categories: SpringFramework
comments: true
---

Spring boot에서 DB에 접근하기 위해 여러가지 라이브러리와 방법들이 있어 정리하고자 한다.

# Hibernate ORM

자바 플랫폼을 위한 ORM 라이브러리 이다.

## ORM이란

Object Relation Mapping  
DB와 OOP 언어 사이의 비호환 데이터를 변환하는 프로그래밍 기법

RDB는 테이블을 사용하고  
OOP는 클래스를 사용한다  
객체 간의 관계를 바탕으로 SQL을 자동으로 생성하여 불일치를 해결한다.

### 장단점

장점 : 생산성 향상, 재사용 유지보수성 향상, DBMS 종속성 감소
단점 : ORM으로만 서비스 구축은 힘들다.

# JPA
Java Persistance API




참고
https://zetawiki.com/wiki/%ED%95%98%EC%9D%B4%EB%B2%84%EB%84%A4%EC%9D%B4%ED%8A%B8_ORM
https://zetawiki.com/wiki/%EA%B0%9D%EC%B2%B4%EA%B4%80%EA%B3%84%EB%A7%A4%ED%95%91_ORM
https://gmlwjd9405.github.io/2019/02/01/orm.html

