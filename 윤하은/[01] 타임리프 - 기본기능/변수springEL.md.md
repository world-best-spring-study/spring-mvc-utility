# 변수 - springEL 표현식

SPRING 내부에서 객체를 접근하는 문법이 있는데 THYMELEAF에서 이 문법을 그대로 가져다씀

1. 자바 빈 프로퍼티 접근법 . 으로 필드에 접근
    
    ```jsx
    ${users[0].username}
    ```
    
2. 문자를 넣는 스타일
    
    ```jsx
    ${users[0]['username']}
    ```
    
3. 직접 메소드 호출해서 접근
    
    ```jsx
    {users[0].getUsername()}
    ```
    

+) 지역 변수 선언 

- `th:with`
- 선언한 태그 안에서만 사용 가능