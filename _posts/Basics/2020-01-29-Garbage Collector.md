---
# layout: post
title: "Garbage Collector"
date: 2020-01-29 15:28
categories: Basics
comments: true
tags: 
 - basics
---

# GC란

- 자동 메모리 관리 기법중 하나.

- 프로그램에서 동적으로 할당했던 메모리 중에서,

  더이상 사용하지 않는 부분을 해제하는 기능

# 작동 원리

더이상 사용되지 않는, 접근되지 않는 data object를 찾아 할당된 자원을 회수한다.

# 장단점

## 장점

프로그래머가 동적으로 할당된 메모리를 관리하지 않아도 되므로 다음과 같은 버그를 제거할 수 있다.

- 유효하지 않은 포인터 접근
    - 이미 해제된 메모리에 접근하는 버그
    - 만약 이 메모리가 해제되고 다른값이 할당되었다면, 읽어올때 잘못된 값을 읽어온다.
- 이중 해제
    - 이미 해제되었는데 또 해제하는 버그
- 메모리 누수
    - 메모리가 해제되지않고 남아있는 버그

## 단점

- 어떤 메모리를 해제할지 결정하는 비용. 즉 오버헤드 부담
- 언제 메모리 해제가 일어나는지, 점유시간은 얼마나 되는지 예측 어려움.


**reference**

- [한wiki](https://ko.wikipedia.org/wiki/%EC%93%B0%EB%A0%88%EA%B8%B0_%EC%88%98%EC%A7%91_(%EC%BB%B4%ED%93%A8%ED%84%B0_%EA%B3%BC%ED%95%99))

- [영wiki](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science))