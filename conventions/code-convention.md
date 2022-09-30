# 코드 컨벤션

- [캠퍼스 핵데이 Java 코딩 컨벤션]  
  (https://naver.github.io/hackday-conventions-java/) 의 자동서식을 따르고 추가적으로 컨벤션은 아래에 따른다.

## 코드 컨벤션 예시

### 패키지 이름은 소문자 구성  
- 패키지 이름은 소문자를 사용하여 작성한다.
- 단어별 구분을 위해 언더스코어 '_' 나 대문자를 섞지 않는다.


### 클래스, 인터페이스 이름에 대문자 카멜 표기법 적용

자바는 기본적으로 변수, 메소드 클래스, 인터페이스는 카멜 표기법을 사용한다.
단, 변수나 메소드는 소문자 카멜 표기법을 사용한다.

```
// 변수
int username;
private void start() { 

}

// Good Exemples
public class Reservation;
public class AccessToken;

// Bad Exemples
public class reservation;
public class Accesstoken;
```

### 클래스 이름에 명사 사용

- 클래스 이름은 명사나 명사절로 짓는다.

### 인터페이스 이름에 명사/형용사 사용

- 인터페이스(interface)의 이름은 명사/명사절로 혹은 형용사/형용사절로 짓는다.

### 테스트 클래스는 Test로 끝남

- JUnit 등으로 작성한 테스트 코드를 담은 클래스는 'Test’을 마지막에 붙인다.

```
// Good Exemples
public class WatcherTest {
```

### 상수

- 상수는 대문자와 언더스코어로 구성[constant_uppercase]

```
public final int UNLIMITED = -1;
public final String POSTAL_CODE_EXPRESSION = “POST”;
```

### 제한자 선언의 순서

- 클래스/메서드/멤버변수의 제한자는 Java Language Specification에서 명시한 아래의 순서로 쓴다.

```
public protected private abstract static final transient volatile synchronized native strictfp
```

### 들여쓰기

- 탭의 크기는 4개의 스페이스

### 조건/반복문에 중괄호 필수 사용

- 조건, 반복문이 한 줄로 끝더라도 중괄호를 활용한다.

```
// Good Examples
if (exp == null) {
    return false;
}

for (char ch : exp.toCharArray()) {

    if (ch == 0) {
        return false;
    }

}

// Bad Examples
if (exp == null) return false;

for (char ch : exp.toCharArray()) if (ch == 0) return false;
```

