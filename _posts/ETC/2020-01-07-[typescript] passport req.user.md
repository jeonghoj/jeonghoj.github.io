---
layout: post
title: "[typescript] passport req.user"
date: 2020-01-07 13:53
categories: ETC
comments: true
---
Typescript에서 passport 사용하던 도중

req.user를 통해 유저 정보를 가져오는데에서 문제가 발생했다.

```
TS2339 : Property 'name' does not exist on type 'User'
```

@types/passport 에서 Request의 user(req.user)에 어떤 property가 들어갈 지를 알려주는 interface를 이미 정의해놓았다.

따라서 내가 다른 property를 추가해도 이미 정의가 되었기 때문에,

property를 인식하지 못하고 컴파일 에러가 난다.


따라서 req.user에 들어갈 수 있는 property를 추가 해주어야 정상적으로 컴파일 된다.

```
declare global {
  // eslint-disable-next-line @typescript-eslint/no-namespace
  namespace Express {
    interface User {
      id: number;
      username: string;
    }
  }
}
```

passport 설정 파일 상단에 이와 같이 

User에 어떤 property가 들어갈지 정의해주어 문제를 해결했다.