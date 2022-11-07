# 🎯 챌린지 코스 사이드 프로젝트

* 아래 요구사항은 내용을 직접 기입하셔도 좋고, 링크로 공유해주셔도 좋습니다.

## 1단계 - 컨벤션

- 코드컨벤션 문서를 공유해주세요

- 깃 브랜치 전략 관련 문서를 공유해주세요

### 작업 방식

1. 작업을 시작하기 전 issue(Todo)를 생성한다.
2. 작업을 시작하고 In Progress로 이동한다.
3. 작업을 마친 후 PR을 한다.
    - assignee(reviewer)가 있는 경우 리뷰를 반영해서 개선한다.
    - assignee(reviewer) 없는 경우 다른 사람의 코드라 생각하고 셀프 리뷰를 한다.
4. Approve가 되었으면 스쿼시 머지와 함께 issue를 닫는다.
5. 이후 해결한 이슈를 Done으로 이동한다.

### 코드 컨벤션

- [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html) 를 따른다.

### 커밋 컨벤션

- [AngularJS Git Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153) 를 따른다.

### 깃 브랜치 전략

- [Git-flow](https://techblog.woowahan.com/2553/) 를 따른다.

### API URL

- Restful하게 설계한다.
    - 자원(Resource)는 URI로 표현한다.
    - 행위(Verb)는 HTTP Method로 표현한다.
- 자원(Resource)은 복수형으로 표시한다.
    - 예시) `/orders`
- 여러 단어로 이루어진 경우 하이픈을 사용한다. (Kebab Case)
    - 예시) `/delivery-orders`
- 컬렉션을 필터링 할 경우 쿼리 파라미터를 사용한다.

### 코드 설계

- DTO 구성
    - `XXXRequest`, `XXXResponse` 형태로 클래스명을 작성한다.

- 패키지 설계 기준
    - 바운디드 컨텍스트 기준으로 패키지를 분리한다. 컨텍스트별로 아래와 같은 구조를 가진다.
        - ui
        - application
        - domain
        - infra
        - exception
        - dto
    - Entity, Repository는 domain layer에 위치한다.
    - RepositoryImpl, 외부와의 통신을 위한 Client 등은 infra layer에 위치한다.
    - exception에는 각 컨텍스트에서 사용될 커스텀 예외가 위치한다.

- 객체 참조
    - 같은 aggregate내에서는 객체를 직접 참조한다.
    - 다른 aggregate의 엔티티를 직접 참조하지 않고 ID로 간접 참조한다.
    - 여러 aggregate를 필요로 하는 로직은 도메인 서비스에서 구현한다.
    - 1:N 관계에서 비즈니스 로직 상 1에서 N에 접근해야할 경우
        - `@OneToMany`
        - cascade = CascadeType.PERSIST
        - ophanRemoval = true
    - 그 외에는 `@ManyToOne`을 통해 연관관계를 설정한다.

## 2단계 - 이벤트 스토밍

- 이벤트스토밍 내용을 공유해주세요


## 3단계 - 이력서

- challenage-course-1기 슬랙 PR 알림 메시지에 댓글로 링크 공유했습니다.
