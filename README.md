# 🎯 챌린지 코스 사이드 프로젝트

* 아래 요구사항은 내용을 직접 기입하셔도 좋고, 링크로 공유해주셔도 좋습니다.

### 1단계 - 컨벤션

- 코드컨벤션 문서를 공유해주세요

- 깃 브랜치 전략 관련 문서를 공유해주세요

### 코드 컨벤션
- [해당 컨벤션](https://phantom-quasar-da4.notion.site/d9320b5fc7754dce9aeb48f5f8b8d201) 을 따른다. ([Google Java Style Guide](https://google.github.io/styleguide/javaguide.html) 와 [네이버 핵데이 컨벤션](https://naver.github.io/hackday-conventions-java) 을 참조하여 정리함)

### 깃 브랜치 전략
- [Github flow](https://docs.github.com/en/get-started/quickstart/github-flow) 를 따른다.

### 작업 순서

1. 이슈를 등록한다.
    - 큰 이슈를 **작은 이슈**로 쪼갠다. (PR 이나 리뷰하기도 쉬워지고, 팀 작업이면 병렬적 수행이 가능해짐)
    - 이슈 내용으로는 **왜 필요한지**를 꼭 기술한다.
    - 이슈는 프로젝트에서 진행상황을 확인할 수 있다. (`Todo`, `In Progress`, `Done`)
2. 작업을 한다.
    - 이슈를 진행한다.
    - `branch` 는 이슈와 관련있게 만든다.
    - `In Progress` 로 설정한다.
3. 작업이 완료되면 PR 요청을 한다.
    - `closes #이슈넘버` 를 통해서 관련 이슈를 linking 한다.
    - **왜 필요한지**는 이슈를 통해서 나타낸다.
    - **어떻게 해결했는지**에 대해 기술한다.
    - 리뷰를 받고 개선한다.
4. 리뷰가 끝나면 머지한다.
    - `Create a merge commit` 을 이용한다. (`no fast forward` 임)
    - `Squash and merge`, `Rebase and merge` 는 금한다.

### 커밋 컨벤션
- [Udacity Git Commit Style](https://udacity.github.io/git-styleguide) 을 따른다.

### URL 디자인
- REST 를 따른다.
    - URL 을 통해 리소스를 식별한다.
    - 리소스는 복수형 명사를 이용해 표현한다.
    - 행위는 Method 를 통해 표현한다.
        - 단, 리소스에 행위가 필요할 경우. 해당 URL 뒤에 동사를 써서 행위를 표시한다.

### 코드 설계
- OOP 를 지키도록 노력한다.
- setter, getter 메서드를 되도록 사용하지 않는다. (feat. OOP)
- lombok 을 사용하지 않는다.
- 패키지 구조는 도메인 별로 구성한다.
   ```
   member
       ㄴ domain
           ㄴ repository
       ㄴ service
           ㄴ dto
       ㄴ ui
   orders
       ㄴ domain
           ㄴ repository
       ㄴ service
           ㄴ dto
       ㄴ ui
  ```
- DI 방식은 `private final` 과 생성자를 통한 주입을 이용한다.(순환참조 방지)
- dto 는 필요할 때마다 생성한다. 필드가 비슷하더라도 의도가 다르다면 새로 만든다.
- custom 예외는 단순 메시지가 아닌 전달할 정보가 있어서 관리하기 편리해질 때 만든다.
- NPE 가 발생하지 않도록 주의하며 작성한다.

### 2단계 - 이벤트 스토밍

- 이벤트스토밍이란 DDD 를 하기 위해 필요한 복잡한 도메인 지식을 다른 도메인 관련한 사람들과 함께 서로 습득하는 방법이다.
- 도메인 지식을 제대로 빠른 시간에 재밌게 습득할 수 있다.
- 개발자들은 이를 토대로 DDD 를 할 수 있다.


### 3단계 - 이력서

- 이력서를 공유해주세요 
