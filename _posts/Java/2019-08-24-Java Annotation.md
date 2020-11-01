---
layout: post
title: "Java Annotation"
date: 2019-08-24 19:49
categories: Java
comments: true
---

@Target
에노테이션을 적용할 위치

@Retention
어느 시점까지 에노테이션이 유효한지를 결정.

@Retention(RetentionPolicy.RUNTIME) // 컴파일 이후에도 JVM에 의해서 참조가 가능
@Retention(RetentionPolicy.CLASS) // 컴파일러가 클래스를 참조할 때까지 유효
@Retention(RetentionPolicy.SOURCE) // 어노테이션 정보는 컴파일 이후 없어짐


@Inherited
자식 클래스가 에노테이션을 상속받을 수 있음.

@Repeatable
반복적으로 에노테이션을 선언할 수 있음.