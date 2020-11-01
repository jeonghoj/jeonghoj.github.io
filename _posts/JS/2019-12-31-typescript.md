---
layout: post
title: "typescript"
date: 2019-12-31 11:10
categories: JS
comments: true
---

# Typescript

## Why TypeScript?

JS는 엄격한 규칙이 없고 사용하기 쉽지만 큰 프로젝트나 팀으로 일할때 불편한 점이 많다.

큰 프로젝트를 하거나 팀으로 일하거나 버그를 최소화 하기 위해 TypeScript 가 등장하였다.

예측가능하고 읽기 쉬운 코드를 만드는데 도움이 된다.

## interface vs class

interface는 컴파일할때 나타나지 않지만,

class는 컴파일하면 포함된다.

interface는 typescript 측면에서는 안전하지만, (컴파일 시 타입 안전 보증. 컴파일 후 변환 결과에는 나타나지 않음)

react, express, node를 쓸때는 class를 사용해야한다.

### classes on typescript

타입스크립트를 이용한 class에서는 access modifier를 지원하여

캡슐화를 할 수 있도록 해준다.