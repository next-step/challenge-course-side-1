## 커밋 컨벤션
### 커밋 메시지 구조
```
[commit type]: [commit message] ([issue nubmer])  // 제목 

body // 본문
```

### 제목
```
[commit type]: [commit message] ([issue nubmer])
```

- commit type


| 구분자   | 작업 유형            |
| -------- | -------------------- |
| feat     | 기능 구현            |
| fix      | 버그 수정            |
| docs     | 문서, 주석 관련 작업 |
| refactor | 리팩토링             |
| test     | 테스트 관련 작업     |
| chore    | 기타 작업                     |

- commit message
    - 이번 커밋에서 작업한 내용을 간단하게 설명함
- issue number
    - 깃허브 이슈 넘버 혹은 지라 티켓 넘버를 작성함

### 본문
- 제목과 본문 사이 한 줄을 개행하여 분리한다.
- 본문은 필요한 경우에 작성하고, **무엇을 왜 했는지**(what과 why)를 중점으로 작성한다. 