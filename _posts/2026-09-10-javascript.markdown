---
lng_pair: id_javascript
title: "JavaScript 정리"

author: 한동관
category: 프론트엔드
tags: [JavaScript]
img: ":cover-js.png"

permalink: /posts/javascript/
date: 2026-09-10 10:00:00 +0900
---
<!-- outline-start -->

자바스크립트 실습 파일 51개를 10페이지로 정리했습니다. 몇몇 페이지는 처음 짠 코드와 고친 코드를 나란히 놓았습니다.<!-- outline-end -->

## 배운 내용

- 값에 따라 문자열 하나를 고르는 긴 `switch`문은 객체에 키와 값으로 담아 두고 꺼내 쓰면 짧아집니다.
- HTML에 `onclick`을 직접 쓰는 대신 `addEventListener`로 연결하면 이벤트 코드가 JS 파일 한곳에 모입니다.
- `window.onload`는 이미지까지 다 받은 뒤 실행되고, `DOMContentLoaded`는 DOM만 준비되면 실행됩니다.
- `Date`의 `getMonth()`는 0부터 시작합니다. 1월이 0입니다.
- `==`는 타입을 바꿔서 비교하기 때문에 `"1" == 1`이 `true`입니다. 타입까지 같아야 하는 `===`를 씁니다.

## 정리한 페이지

노션에 정리한 페이지입니다. 누르면 노션으로 이동합니다.

1. [자바스크립트 시작과 변수 선언 기술](https://www.notion.so/3d7ba972198d8121b630e56546fe1a80)
2. [연산자를 활용한 값 처리 기술](https://www.notion.so/3d7ba972198d81039282c93a2dbf506c)
3. [형변환과 조건 분기 설계](https://www.notion.so/3d7ba972198d81599226f9c0f44b233e)
4. [다중 분기 처리와 객체 매핑 리팩터링](https://www.notion.so/3d7ba972198d81bcaabbd5ac0914cefc)
5. [반복문을 활용한 반복 처리와 성능 개선](https://www.notion.so/3d7ba972198d81059e17da78b7466519)
6. [내장 객체 활용 (Date · Math · String)](https://www.notion.so/3d7ba972198d8159af81feb4a774d8bf)
7. [배열 자료구조와 데이터 조작 기술](https://www.notion.so/3d7ba972198d8108a99ce2bfe9f3b2f9)
8. [함수 설계 (매개변수 · 반환값 · 재귀)](https://www.notion.so/3d7ba972198d816cbb59c72f6812fb2b)
9. [이벤트 처리와 DOM 인터랙션 설계](https://www.notion.so/3d7ba972198d8176b3abe124e484bebb)
10. [객체 지향 설계 (생성자 함수 → ES6 Class)](https://www.notion.so/3d7ba972198d81949b65f89138edfbfc)
