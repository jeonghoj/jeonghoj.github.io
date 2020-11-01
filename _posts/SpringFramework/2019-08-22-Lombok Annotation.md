---
layout: post
title: "Lombok Annotation"
date: 2019-08-22 22:21
categories: SpringFramework
comments: true
---
Lombok은 자바에서 Model(DTO, VO, Domain) Object를 만들때  
불필요하게 반복되는 Getter Setter ToString등의 코드를  
에노테이션을 통해 생성해주는 라이브러리다.

@Getter @Setter  
자동으로 Getter Setter를 만들어주어 코드를 가독성 좋게 유지할 수 있다.  
다만 Setter의 경우에는 객체의 캡슐화가 옅어지는 측면이 있어 조심하여야 한다.  

@NoArgsConstructor  
파라미터 없는 기본 생성자 생성
@AllArgsConstructor  
모든 필드 값을 파라미터로 받는 생성자 생성
@RequiredArgsConstructor   
final @NonNull 인 필드 값만 파라미터를 받는 생성자 생성

@EqualsAndHashCode(callSuper = true/false)
equals와 hashcode 메소드 자동 생성.
callSuper true일시, 부모 클래스 필드 값들도 동일한지 체크
false일시, 자신의 클래스 필드값만 고려

@ToString(exclude = "필드")

@Data
위의 설정을 다 설정해줌



참고 : https://www.daleseo.com/lombok-popular-annotations/