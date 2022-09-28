# 0. 개요
- [Google Java Style Guide](https://github.com/JunHoPark93/google-java-styleguide)을 준수합니다.
- [읽기 좋은 코드가 좋은 코드다](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&ejkGb=KOR&barcode=9788979149142) 를 보고 추가적으로 작성하였습니다.

# 1. Naming
- 이름은 매우 구체적인 단어를 사용한다.
  - tmp나 retval 같은 보편적인 이름은 사용하지 않는다.
  ```java
  // 좋은예
  public void downLoadPage()
  // 나쁜예
  public void getPage()
  ```
- 경계를 포함하는 한계값은 min과 max를 사용한다.
   ```java
  // 좋은예
   public static final MAX_ITEMS_IN_CART = 10
  // 나쁜예
   public static final CART_TOO_BIG_LIMIT = 10
   ```

# 2. Format

- 상수에 대한 설명을 주석으로 작성한다.
  - 상수가 무엇을 하는지, 왜 특정한 값을 갖게 되었는지 등을 작성한다.
  ```java
  // 상수값이 2 * num_processors보다 크거나 같으면 된다.
  public static final int NUM_THREADS = 8
  ```
- 조건문에서 인수의 순서를 정한다.
  - 왼쪽은 값이 유동적인 질문을 받는 값
  - 오른쪽은 더 고정적인 값, 비교 대상으로 사용되는 표현
  ```java
  if (length > 10)
  ```

# 3. URL 디자인
- RESTful API 설계를 한다.
  - 리소스(URI)는 동사가 아닌 메서드와 구체적인 이름을 사용한다.
  - kebab-case를 사용한다.
  - 단수가 아닌 복수를 사용한다.

# 4. Structure
- 도메인형 디렉토리 구조로 분리한다.
- project
  - domain
    - controller
    - dto
    - exception
    - repository
    - service
  - commons
    - config