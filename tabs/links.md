---
layout: links
published: false
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_links

# seo
#meta_description: ""

###########################################################
#                Links Page Data
###########################################################
page_data:
  main:
    header: "링크"
    info: "정리해 둔 기록과, 배우면서 계속 열어본 곳들입니다."

  # To change order of the Categories, simply change order. (you don't need to change list order.)
  category:
    - title: "내 기록"
      type: id_mine
      color: "#62b462"
    - title: "레퍼런스"
      type: id_reference
      color: "gray"
    - title: "도구"
      type: id_tool
      color: "#F4A273"

  list:
    # 내 기록
    - type: id_mine
      title: "학습내용 정리 (노션)"
      url: "https://www.notion.so/248ba972198d829f9f4581ed74b4eb5c"
      info: "웹과 자바 학습 기록 48페이지와 프로젝트 케이스 스터디를 모아둔 곳입니다. 페이지마다 설명 · 관련 소스 파일 · 사용된 주요 기술 · 주요 소스 코드 순서로 되어 있습니다."

    # 레퍼런스
    - type: id_reference
      title: "MDN Web Docs"
      url: "https://developer.mozilla.org/ko/"
      info: "HTML · CSS · JavaScript를 찾아볼 때 제일 먼저 여는 곳입니다. 브라우저별 지원 범위까지 같이 나옵니다."
    - type: id_reference
      title: "W3Schools"
      url: "https://www.w3schools.com/"
      info: "문법을 빨리 확인하고 예제를 바로 실행해 볼 때 씁니다."
    - type: id_reference
      title: "Spring 공식 문서"
      url: "https://spring.io/projects/spring-boot"
      info: "잔디로그 백엔드를 Spring Boot와 Spring for GraphQL로 잡으면서 계속 보고 있습니다."
    - type: id_reference
      title: "NEIS 교육정보 개방 포털"
      url: "https://open.neis.go.kr/"
      info: "미니홈피의 급식 정보를 받아온 공공 API입니다. 학교 코드를 먼저 받고 그 코드로 급식을 다시 부르는 2단 조회 구조입니다."

    # 도구
    - type: id_tool
      title: "Jekyll"
      url: "https://jekyllrb.com/"
      info: "이 사이트를 만든 정적 사이트 생성기입니다."
    - type: id_tool
      title: "Expo"
      url: "https://docs.expo.dev/"
      info: "Young Trip 프로토타입을 React Native + Expo로 만들고 있습니다."
    - type: id_tool
      title: "Notion API"
      url: "https://developers.notion.com/"
      info: "학습 기록을 손으로 옮기지 않고 스크립트로 올리려고 썼습니다."
---
