# 1. 코드컨벤션

전체적인 구조는 [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html) 따릅니다.

### 들여쓰기
* 좀 더 가독성있게 코드를 보기 위해 들여쓰기 2 -> 4 변경

```
Tab Size : 4

Indent : 4

Continuation indent : 8
```

탭은 사용하지 않음

### 블럭

1. 블럭 괄호 안에 문자가 없다면 개행없이 사용할 수 있음

    ```swift
    void doNothing() {}
    ```

2. 블럭 괄호 안에 한 줄이라도 존재한다면 한 줄로 개행없이 사용하지 않음

    ```swift
    void doNothing() { doSomething(); } // X
    ```


### 명명 규칙

1. 변수와 함수는 `카멜 케이스`
2. 상수는 영문 대문자
3. 클래스명은 `파스칼 케이스`
4. 패키지는 항상 소문자로 사용

# 커밋 컨벤션

커밋 메시지는 [AngularJS Git Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153) 따름
* 커밋 포맷
  ```
  <type>(<scope>): <subject>
  <BLANK LINE>
  <body>
  <BLANK LINE>
  <footer>
  ```

# 2. 깃브랜치 전략

혼자서 프로젝트를 진행하기 때문에 간단하게 사용가능한 브랜치 전략인 [github-flow](https://subicura.com/git/guide/github-flow.html#github-flow-%E1%84%87%E1%85%A1%E1%86%BC%E1%84%89%E1%85%B5%E1%86%A8) 를 사용

* `feature`나 `master`가 존재하지 않기에 브랜치에 대한 내용을 자세히 작성
* `staging` 공간이 필요해진다면 `git-flow`나 `gitlab-flow`로 전환 가능

# 3. API 컨벤션

REST API로 구성합니다.

### REST API 네이밍

- 동사 표현 대신 명사를 사용
- 명사는 단수를 사용하지 않고 모두 복수로 표현

    ```java
    GET /users
    GET /users/:id
    ```

- 리소스가 길어진다면 밑줄 대신 하이픈(-)으로 표현
- 필드명 카멜케이스 준수

### REST API 조회 조건

- 동일한 자원에 대한 필터링 조건은 pathVariable을 사용하지 않고 `쿼리 파라미터` 를 사용

    ```java
    /users?gender=male (O)
    /users/gender/male (x)
    ```


### Http status code

status code를 통해 API 대한 정확한 수행 상태 정보를 리턴

### 성공 시 반환 구조
* 예시

  ```java
  200 OK

  {
    "user": { 
          /* ... user entity ... */ 
      }
  }
  ```

### 에러 시 반환 구조
* 예시

  ```java
  400 Bad Request

  {
    "code": "error.code",
    "message": "example message",
    "description": "description"
  }
  ```

## 패키지 구조

- 도메인 기준으로 코드를 리팩터링
- DDD에 대한 학습이 필요

- 기본 구조
  ```
  Presentation (요청을 서비스로 위임하며 응답을 반환) 
  Application  (트랜잭션 관리, DTO 변환, 도메인 간 연계)
  Domain       (비즈니스 규칙, 도메인 정보)
  Infra        (일반화된 기술적 기능 제공 ex)Spring data jpa)
  ```
