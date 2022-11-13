# URL 링크

바인딩…

### 타임리프 url 생성

- @{…} 문법 사용

### 단순 url

- @{/hello} → /hello

### 쿼리 파라미터

- @{/hello(param1=${param1}, param2={param2})} → /hello?param1=data1&param2=data2

### 경로변수

- @{/hello/{param1}/{param2}(param1=${param1}, param2=${param2})} → /hello/data1/data2

### 쿼리 파라미터 + 경로변수

- @{/hello/{param1}(param1=${param1}, param2=${param2})} → /hello/data1?param2=data2