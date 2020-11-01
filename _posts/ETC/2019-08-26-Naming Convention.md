---
layout: post
title: "Naming Convention"
date: 2019-08-26 23:48
categories: ETC
comments: true
---

HTML

공통 규칙
- 네이밍 첫 시작에 숫자, 대문자, 특수문자의 사용을 지양한다.
- `형태_의미_상태` 순서로 조합. 이 3단계를 넘지 않도록 권장.
- prefix, subfix, suffix 를 잘 활용하자.

id/class 규칙

id는 카멜케이스 class는 언더 스코어 방식을 사용.

```
<input id="userId" class="user_id">
```


attribute 우선 순위

순서	속성
1	 rel
2	 type
3	 href, src
4	 width, height
5	 target
6	 id
7	 name
8	 class
9	 style
10	 title, alt
11 	 기타 attribute


참고
http://darum.daum.net/convention/html/html_convention
