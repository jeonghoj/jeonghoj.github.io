---
layout: post
title: "aws code deploy"
date: 2019-09-03 18:54
categories: SpringFramework
comments: true
---

먼저 Travas Ci 빌드가 Success 했다고 가정.

Code Deploy를 통한 배포 자동화 하기.


1. Travas에서 사용할 사용자 생성.  

IAM에서
- S3 접근 권한 부여
- CodeDeploy 접근 권한 부여

2. AWS S3 생성 
Travis CI에서 빌드된 파일을 담는 역할을 한다.

3. AWS Role 생성
IAM에서 생성된 Crediential Key로 사용자 대신 서비스를 실행한다.

4. Travas와 S3 연동
Travis CI에서 빌드된 파일을 보내는 설정을 진행한다.

.travis.yml에 s3관련 설정을 추가.

파일 갯수가 많아 전송시간이 오래 걸릴 수 있어, zip으로 압축한다.

5. AWS CodeDeploy 설정

CodeDeploy 명령을 수행할 EC2를 선택한다.

6. appspec.yml추가

appspec.yml을 통해 AWS CodeDeploy 설정을 한다.





참고 : 

https://jojoldu.tistory.com/265

https://docs.travis-ci.com/user/deployment/s3/

