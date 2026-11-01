---
lng_pair: id_spring
title: "스프링부트 방과후 정리"

author: 한동관
category: 백엔드
tags: [Spring Boot]
img: ":cover-spring.png"

permalink: /posts/spring-boot/
date: 2026-10-30 11:00:00 +0900
---
<!-- outline-start -->

스프링부트 방과후에서 게시판을 만들면서 배운 내용을 11페이지로 정리했습니다. 수업 때 적어 둔 메모를 바탕으로 썼습니다.<!-- outline-end -->

## 정리하다가 고친 것

- `Long` 값을 `!=`로 비교하던 코드를 `equals()`로 바꿨습니다. `Long`도 `String`처럼 객체라서 `!=`는 값이 아니라 같은 객체인지를 비교합니다.
- `META-INF` 폴더가 `META_INF`로 만들어져 있어서 안의 `orm.xml`이 읽히지 않고 있었습니다. 폴더 이름을 고쳤습니다.
- `data.sql`에 글을 추가한 뒤로 맞지 않던 테스트 기댓값 4개를 고쳤습니다. 지금은 테스트 13개가 모두 통과합니다.

## 정리한 페이지

노션에 정리한 페이지입니다. 누르면 노션으로 이동합니다.

1. [프로젝트 시작과 MVC 패턴](https://www.notion.so/409ba972198d81ac82b9c8985a6529db)
2. [게시글 작성 (폼 · DTO · JPA 저장)](https://www.notion.so/409ba972198d8159aa94cdcd0de96d22)
3. [롬복과 로깅으로 리팩터링](https://www.notion.so/409ba972198d819f9542fbd71907bb37)
4. [게시글 조회 (상세 · 목록)](https://www.notion.so/409ba972198d81179e38ea95761ba0df)
5. [게시글 수정 · 삭제와 리다이렉트](https://www.notion.so/409ba972198d8122a1c5d6d3ed55503e)
6. [회원가입 (셀프 실습)](https://www.notion.so/409ba972198d815f9f74c40ca11f63e6)
7. [REST API 컨트롤러](https://www.notion.so/409ba972198d81a1b794e34739b11e34)
8. [서비스 계층과 트랜잭션](https://www.notion.so/409ba972198d81c6898acef68470c552)
9. [테스트 코드 작성](https://www.notion.so/409ba972198d8127a1dccccec1fc734e)
10. [댓글 엔티티와 네이티브 쿼리](https://www.notion.so/409ba972198d811db91fef67ead6b117)
11. [학습 노트 (note.txt)](https://www.notion.so/409ba972198d8109bcfcc82adcd5f625)

사용한 것: Spring Boot, Java 17, Spring Data JPA, H2, Mustache
