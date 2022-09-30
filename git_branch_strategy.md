# 깃 브랜치 전략
***

## 전략 선택
***
- 많은 브랜치를 사용하는 git-flow 보다는, 브랜치를 간소화하여 혼동을 줄이고 역할이 보다 명확한 github-flow 전략을 사용한다

## 사용법
***
1. Master Branch의 어느것이든 배포가 가능하다.

2. 새로운 일을 시작하기 위해 Branch를 Master에서 딴다면 이름은 어떤 작업인지 명확하게 명시한다.

3. Local Branch에 수시로 커밋하고 이 내용을 원격 Branch에 수시로 Push한다.

4. 피드백이나 도움이 필요할 때 혹은 자신의 Branch가 merge할 준비가 되었다면, PR을 생성하여 공유한다.

5. PR 리뷰 후에는 다른 사람의 동의를 얻고 Master에 Merge한다.

6. Master Branch로 Merge나 Push가 이루어지면 즉시 배포해야한다.


## 레퍼런스
***

- [Git-Flow란? 그리고 Github-Flow, Gitlab-Flow와 비교해보자](https://youngtoad.tistory.com/46)