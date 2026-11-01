---
lng_pair: id_typescript
title: "TypeScript 정리"

author: 한동관
category: 프론트엔드
tags: [TypeScript]
img: ":cover-ts.png"

permalink: /posts/typescript/
date: 2026-11-01 11:00:00 +0900
---
<!-- outline-start -->

잔디로그 웹 화면을 TypeScript로 만들면서 쓴 문법을 9페이지로 정리했습니다. 예제는 모두 잔디로그 코드에서 가져왔습니다.<!-- outline-end -->

## 배운 내용

- `'ok' | 'bad'`처럼 값 자체를 타입으로 쓰면 오타가 난 값은 실행 전에 막힙니다.
- 배지 종류마다 필요한 값이 달라서 `kind`로 구분하는 유니온으로 묶었습니다. `switch (a.kind)`로 나누면 각 경우에 있는 속성만 쓸 수 있습니다.
- 반환 타입을 `v is ErrorCode`로 적은 함수가 참을 돌려주면, 그 뒤로 그 값은 `ErrorCode`로 다뤄집니다.
- `unknown`은 검사하기 전에는 아무 속성도 쓸 수 없어서 `any`보다 안전합니다.
- `Record<ErrorCode, ErrorCategory>`로 표를 만들면 오류 코드를 새로 추가했을 때 표에 빠뜨린 것을 바로 알 수 있습니다.
- `noUncheckedIndexedAccess`를 켜면 배열에서 꺼낸 값에 `undefined`가 붙어서, 비었을 때의 값을 정해야 합니다.
- 서버 응답 타입은 GraphQL Code Generator가 스키마에서 만들어 줍니다.

## 정리한 페이지

노션에 정리한 페이지입니다. 누르면 노션으로 이동합니다.

1. [타입 표기와 타입 별칭](https://www.notion.so/40bba972198d81de8a9ad9d6f17d121c)
2. [객체 타입과 props](https://www.notion.so/40bba972198d812699e3ed1dd218888f)
3. [유니온 · 리터럴 타입과 판별 유니온](https://www.notion.so/40bba972198d816c837bd39279551758)
4. [타입 가드 (v is T)](https://www.notion.so/40bba972198d81588d69d4bfba8e4783)
5. [제네릭](https://www.notion.so/40bba972198d8130b3f3cf898c5af4b1)
6. [유틸리티 타입과 as const](https://www.notion.so/40bba972198d813a8fcec2a115ffe74c)
7. [tsconfig와 strict 옵션](https://www.notion.so/40bba972198d814e8ecdfe906f3198e2)
8. [GraphQL 타입 자동 생성 (codegen)](https://www.notion.so/40bba972198d8183a527deab71b2d162)
9. [프로젝트 적용 — 잔디로그](https://www.notion.so/40bba972198d81cf81d6e4acf8c71cb0)

사용한 것: TypeScript 5.9, GraphQL Code Generator
