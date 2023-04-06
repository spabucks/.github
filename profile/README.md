# 프로젝트명
> 스타벅스 클론 코딩 '스파벅스' 팀 입니다! 

신세계 I&C 주관의 스파로스 아카데미에서 진행한 스타벅스 온라인 스토어 클론 코딩 프로젝트이며 웹앱 형태로 구현했습니다.

## 링크 : http://sphabucks.xyz
PC환경에서 접속하신 경우 f12를 눌러 개발자모드를 켜 주신 후 기기 툴바 전환(ctrl + shift + m)을 실행해주세요.


## 멤버
* 팀장 : 주영민(BE)
* 팀원
  * FE : 김민경, 김효은
  * BE : 김지욱, 정승훈


## 클론코딩 주제(스타벅스 온라인 스토어)
|경로|주제|
|:-:|:-:|
|스타벅스 모바일 어플리케이션에서<br>order탭에 있는 쇼핑하러 가기 버튼으로 접속|스타벅스 온라인 스토어(모바일 웹)을<br>구현하는 것이 목표|
|<img src = "https://user-images.githubusercontent.com/90381800/228540848-46946a3f-5507-4e2f-a11f-bf9510330504.png" width="200px" height="500px">|<img src = "https://user-images.githubusercontent.com/90381800/228541721-2c4df1d0-b1cd-47bc-90f9-d6bcc1575a67.png" width="200px" height="500px">|


## 기능

|메인|검색|전체상품|
|:-:|:-:|:-:|
|![메인](https://user-images.githubusercontent.com/90381800/230259182-1ebc2ebd-1f73-4098-a91e-7191a5c761dd.gif)|![검색](https://user-images.githubusercontent.com/90381800/230259196-ed1c184c-22b2-4651-8be3-7fad85df4e02.gif)|![전체상품](https://user-images.githubusercontent.com/90381800/230259207-c4ebd1b2-57eb-4454-8c21-1803fcdaed7a.gif)|
|회원가입|장바구니|로그인|
|미정|![장바구니](https://user-images.githubusercontent.com/90381800/230259251-f9289e83-f3c5-42c9-8469-c0f7cd79ab14.gif)|![로그인](https://user-images.githubusercontent.com/90381800/230259259-62c5a510-7396-4d83-b75c-2e429b79ff76.gif)|


## 설치 방법

OS X & 리눅스, 윈도우:

1. GitHub Repository에서 fork 버튼을 누른다. 
2. GitHub Access Token 발급 후 Secrets 등록한다.
3. [환경설정](#enviroment) 설정


BackEnd
```sh
 - Java 11 이상 (이 프로젝트에 빌드 된 버전은 17 버전입니다.)
 http://34.22.69.135:8080/swagger-ui/index.html ( Swagger API )
```

## BackEnd 개발 환경 설정

```sh
./gradlew -x build
```



## 페이지 접근 권한
|권한|이름|
|:-:|:-:|
|USER|로그인한 유저|
|GUEST|게스트|

## Enviroment


|권한 이름|내용|
|:-:|:-:|
|$DB_USERNAME|DB 이름|
|$DB_PWD|DB 비밀번호|
|$SCHEMA_NAME| SCHEMA 이름|
|$PORT|포트번호|
|$IP|아이피|
|$ADMIN_MAIL_ID| 메일 아이디 |
|$ADMIN_MAIL_PWD| 메일 비밀번호|
|SECRETKEY| Encryption Key |

- application.yml 설정
```
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    username: ${{ DB_USERNAME }}
    url: jdbc:mysql://${{ IP }}:${{ PORT }}/${{ SCHEMA_NAME }}
    password: {{ DB_PWD }}
  jpa:
    properties:
      hibernate:
        dialect: org.hibernate.dialect.MySQL5Dialect
        format_sql: true
    hibernate:
      ddl-auto: update
  data:
    redis:
      host: ${{ IP }}
      port: ${{ PORT }}
SECRET_KEY: ${{ SECRETKEY }}
```

- email.properties 설정
```
mail.smtp.socketFactory.class=javax.net.ssl.SSLSocketFactory
mail.smtp.socketFactory.fallback=false
mail.smtp.socketFactory.port=465
mail.smtp.starttls.required=true
mail.smtp.starttls.enable=true
mail.smtp.port=465
mail.smtp.auth=true

AdminMail.id={ADMIN_MAIL_ID}
AdminMail.password={ADMIN_MAIL_PWD}
```


## 기여 방법

1. (<https://github.com/yourname/yourproject/fork>)을 포크합니다.
2. (`git checkout -b feature/fooBar`) 명령어로 새 브랜치를 만드세요.
3. (`git commit -am 'Add some fooBar'`) 명령어로 커밋하세요.
4. (`git push origin feature/fooBar`) 명령어로 브랜치에 푸시하세요. 
5. 풀리퀘스트를 보내주세요.

### Tech stack
Back-end  
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat&logo=Spring Boot&logoColor=white" />
<img src="https://img.shields.io/badge/Spring-6DB33F?style=flat&logo=Spring&logoColor=white" />
<img src="https://img.shields.io/badge/Spring Security-6DB33F?style=flat&logo=Spring Security&logoColor=white" />
<img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white" />
<img src="https://img.shields.io/badge/JWT-000000?style=flat&logo=JWT&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white" />

FrontEnt  
<img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=white" />
<img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white" />
<img src="https://img.shields.io/badge/Recoil-5A29E4?style=flat&logo=Recoil&logoColor=white" />
<img src="https://img.shields.io/badge/Axios-000000?style=flat&logo=Axios&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=HTML5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=CSS3&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=white" />


Tool  
<img src="https://img.shields.io/badge/IntelliJ IDEA-000000?style=flat&logo=IntelliJ IDEA&logoColor=white" />
<img src="https://img.shields.io/badge/Visual Studio Code-007ACC?style=flat&logo=Visual Studio Code&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=flat&logo=GitHub Actions&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white" />
<img src="https://img.shields.io/badge/Google Cloud-4285F4?style=flat&logo=Google Cloud&logoColor=white" />




<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki
