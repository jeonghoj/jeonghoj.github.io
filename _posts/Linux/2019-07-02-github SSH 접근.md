---
layout: post
title: "리눅스에서 github 쓸때 ssh로 접근"
date: 2019-07-02 13:21
categories: Linux
comments: true
---

SSH를 사용하는 이유는 보안적으로 안전하게 통신을 하기 위함이다.

SSH는 공개키와 비밀키를 이용해서 모든 문자열을 암호화하여 통신한다.

~~사실 HTTPS로 클론하면 아이디 암호 치기가 귀찮다~~


순서는 다음과 같다.

1. SSH 키 생성
```
$ssh-keygen -t rsa -b 4096 -C "comment"
```
파일 경로는 default로
passphrase는 넣어도 되고 안넣어도 되고

2. SSH 등록
```
# 기본 생성 경로
$ssh-add ~/.ssh/id_rsa
```

3. github에 ssh 공개키 등록
```
$cat ~/.ssh/id_rsa.pub
```
내용을 복사하여

https://github.com/settings/keys 에 ssh 공개키 등록


reference : https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
