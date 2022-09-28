# 1. Github-flow 전략

## Github-flow 전략을 사용한 이유
- Github-flow 전략은 Git-flow의 흐름을 조금 더 간소화 시킨 전략입니다.
- 1인 프로젝트이므로 간단한 전략을 사용하려고 하였습니다.
- github 에서 사용하기에 적합하다고 생각했습니다.

![image](https://user-images.githubusercontent.com/49813916/192207896-6e4fad9a-6a98-4153-8b22-a63a252f3883.png)

## 브랜치 전략

- `master` 브랜치는 언제든 배포 가능 상태를 유지합니다.
- 새로운 브랜치는 항상 `master` 브랜치에서 생성합니다.
    - 브랜치 이름은 자세하고 의도를 명확하게 드러냅니다.
- 기능을 추가할 때에는 `feature/{item}` 브랜치를 생성합니다.
- `master` 브랜치에 merge를 할 때 pull request를 생성합니다.
- merge 이후 요청한 브랜치는 삭제합니다.

참고: [github-flow](https://guides.github.com/introduction/flow/)

# 2. git commit message 컨벤션
## message 구조

```java
#이슈번호 type: 제목
내용
```

## type

- `feat` : 새로운 기능 추가
- `fix`: 버그 수정
- `docs`: 문서 작성 및 수정
- `style`: 코드 형식, 정렬, 주석 등 동작에 영향을 주지 않는 것들
- `refactor`: 코드
- `test`: 테스트 추가 및 수정
- `chore`: 위에 해당되지 않는 모든 변경

참고: [AngularJS Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153)

# 3. PR 규칙

- PR 제목은 #이슈번호 제목으로 합니다.
- 1개의 PR에는 1개의 작업만 넣습니다.
- PR 템플릿을 사용하여 PR 내용을 규격화 합니다.
## PR template 구조
```
## 개요         // 이슈 또는 PR의 대략적인 설명
## 작업사항     // 구체적인 작업 내용
## 고민한 부분  // 작업하면서 고민한 부분 또는 해결되지 않은 문제에 대한 내용
```

참고: [헤이딜러 블로그](https://medium.com/prnd/%ED%97%A4%EC%9D%B4%EB%94%9C%EB%9F%AC-%EA%B0%9C%EB%B0%9C%ED%8C%80-%EB%AA%A8%EB%91%90%EA%B0%80-%ED%96%89%EB%B3%B5%ED%95%9C-%EA%B0%9C%EB%B0%9C-pr%EA%B4%80%EB%A6%AC-%EB%B0%A9%EB%B2%95-7%EA%B0%80%EC%A7%80-1d4cd5d091f0)