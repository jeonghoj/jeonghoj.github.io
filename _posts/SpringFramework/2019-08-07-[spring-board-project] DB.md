---
layout: post
title: "[spring-board-project] DB"
date: 2019-08-07 00:00
categories: SpringFramework
comments: true
---

```
# root로 접속

# 유저 생성
>create user '유저 ID'@'IP주소' identified by '패스워드'

# DB 권한 부여
>grant all privileges on "DB이름".* to '유저 ID'@'IP주소';

# mysql 변경사항 적용
>FLUSH PRIVILEGES;

# cf) 유저 삭제
>drop user '유저 ID'@'IP주소';

```
cf) vm에서 host ip를 가리킬 때 주소는 192.168.xxx.1이다.

---
SQL file import
```
mysql -u root -p < filename.sql
```

---

SQL change password policy

1. mysql 터미널에서 변수 수정

```
# 임시방편. 재시작하면 다시 바뀐다.
SET GLOBAL validate_password.policy=LOW;
SET GLOBAL validate_password.length=4;
```

2. my.cnf 수정

```
[mysqld]
...

#추가
validate_password.policy=LOW
validate_password.length=4
```

---

mysql-connector-java 5.1.X KST 타임존을 인식하지 못하는 이슈

```
# 추가
[mysqld]
default-time-zone=Asia/Seoul
```


---

nodejs mysql 연결 문제

mysql8 패스워드 동작방식이 아직 지원 안하는모양

alter user identified with mysql_native_password 로 바꿔줘서 해결.

또는 mysql 설치시 패스워드 정책을 legacy 모드로 바꿀것
