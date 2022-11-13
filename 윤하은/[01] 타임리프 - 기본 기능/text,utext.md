# 텍스트 - text, utext

### 텍스트 출력

- 텍스트를 출력하는 기능은 타임리프의 가장 기본 기능이다.
- 타임리프는 기본적으로 html 태그의 속성에 기능을 정의해서 동작함
    - span 태그 내에서 th:text 를 추가해서 태그의 속성에 기능을 정의함
- html 태그의 속성에 th:text 기능을 추가할 때
    
    ```html
    <span th:text="${data}">
    ```
    
- html 태그의 속성이 아니라 html 콘텐츠 영역안에서 직접 데이터를 출력할 때
    - 태그의 속성에서 사용하는게 아니라 그냥 html 콘텐츠 영역안에서 출력 → 즉, html 일반 태그내에서 바로 출력하고 싶을 때
    
    ```html
    <li>[[${data}]]</li>
    ```
    
- span

### BasicController.class

- hello/thymeleaf/basic 패키지 하위에 생성
- @RequestMapping 클래스 레벨에서 해줌 → 메소드의 RequestMappin
- textBasic 메소드
    - “http://localhost:8080/basic/text-basic” 에 대한 요청을 처리하는 메소드
    - model 파라미터로 받아와서 model에 데이터를 넣어줌
    - “basic/text-basic” 뷰 반환

### text-basic.html 뷰 생성

- resources/templates/basic 패키지 생성해서 하위에 text-basic.html 생성

### Escape

- html에서 사용하는 특수문자를 html 엔티티로 변경하는 것
- th:text , [[...]] (타임리프 텍스트 출력 기능) 은 이스케이스를 기본적으로 제공
- < → &lt;
- > → &gt;

### Unescape

- 이스케이프를 예외적으로 사용하지 않기 위한 방법
- th:text → th:utext
- [[…]] → [(…)]
- th:inline=”none” // `<span th:inline=”none”>[[…]]</span>`
    - 타임리프는 [[…]] 을 해석하기 때문에 화면에 문자 그대로 보여줄 수 없음
    - 이 태그 안에서는 타임리프가 해석하지 말라는 옵션
- ❗❗ escape를 기본으로 하고 예외적인 경우 꼭 필요한 경우에만  unescape 를 사용하자 ❗❗
