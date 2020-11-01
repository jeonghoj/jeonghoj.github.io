---
layout: post
title: "Design Pattern"
date: 2020-01-20 00:27
categories: SoftwareEngineering
comments: true
---
# Design Pattern

## 생성 패턴 (Creational Patterns)

객체 생성에 관련된 패턴

객체의 생성을 캡슐화하여 특정

- **Factory Pattern**

    객체의 생성 처리를 서브 클래스로 분리하여 캡슐화하는 방식

- **Abstract Factory Pattern**

    구체적인 클래스가 아닌, 서로 연관되거나 의존적인 조합을 만들어내는 인터페이스를 제공하는 패턴

- **Singleton Pattern**

    객체를 단 한번만 생성하도록 하고, 그 객체를 어디에서든지 참조할 수 있도록 하는 패턴

## 구조 패턴 (Structural Patterns)

클래스나 객체를 조합해서 더 큰 구조를 만드는 패턴

2개의 인터페이스를 조합해서 단일 인터페이스를 만들거나,

객체를 묶어 새로운 기능을 제공하는 패턴

- **Adapter Pattern**

    직접적으로 호출하지않고 중간에 Adapter를 둬서 호출하는 패턴

    호환성이 없어도 동작할 수 있고, 유지보수가 쉬움

- **Composite Pattern**

    여러 개의 객체를 하나의 객체처럼 다루게 하는 패턴.

    여러개의 객체를 트리 구조로 구성하여 계층적으로 표현 할 수 있음.

- **Decorator**

    Decorator 클래스를 추가하여 기존의 클래스를 Wrapping한다.

    기존 클래스의 기능은 그대로 유지하고 새로운 기능을 추가한다.

- **Proxy**

    Proxy 객체를 통해 기존 객체를 수정하지않고 흐름 제어를 하는 패턴

## 행위 패턴 (Behavioral Patterns)

객체 간의 Communication을 고려한 패턴

- **Observer**

    한 객체가 상태 변화하면 다른 모든 객체도 그 상태가 연동되도록하는 패턴

    일대다 객체 의존관계를 형성

- **State**

    객체의 상태에 따라 객체의 행위가 변화하는 패턴

- **Strategy**

    클래스의 행위나 알고리즘을 캡슐화 하여 실행 될 때 변화하는 패턴

- **Template**

    Abstract class가 구현해야 할 메소드를 정의하고, 
    
    하위 클래스가 abstract class를 상속, 
    
    메소드를 Override하여 구현하는 패턴

    
**reference**

- https://github.com/jobhope/TechnicalNote/blob/master/software_engineering/Design%20Pattern.md

- https://github.com/SantonyChoi/what-happens-when-KR