# 1. ASWS API GATEWAY란?
* Amazon API Gateway는 어떤 규모에서든 개발자가 API를 생성, 유지 관리, 모니터링 및 보호할 수 있게 해주는 AWS 서비스.
* Client가 AWS 서비스에 액세스 할 수 있는 일관된 **RESTful API**를 제공.
![](https://t1.daumcdn.net/cfile/tistory/2242BF48574AC88102)
* MSA(Micro Service Architecture)에 대해서도 찾아 볼 것.

## 1.1. REST? / RESTful?
### 1.1.1. REST
   - **Re**presentational **S**tate **T**ransfer의 약자로, 소프트웨어 프로그램 개발 아키텍쳐.
   - Representational(대표적인) State(상태) Transfer(전달)
   - 무엇이 대표적인가?
      + '자원'의 대표를 뜻한다.(=대표 자원)
      + '자원'은 시스템이 관리하는 모든 것이 될 수 있다. 심지어 시스템 자체도 '자원'이 될 수 있다.
      + 머스트잇 개발자들을 대표한다면 '개발팀'.
      
   - 상태 전달
      + 요청된 자원의 상태를 전달.
      + 상태라 함은 요청 시점의 자원의 '상태'.
      + WWW에서는 URI를 통해 자원을 지정하고, HTTP Method를 통하여 행위를 지시한다.

   - REST를 정의하는 6가지 조건.
      + Client - server
      + Stateless : 각각의 요청은 독립적이어야 한다. 현재의 요청이 다음의 요청에 영향을 주어선 안된다. 
         * '없음'이란 오브젝트에 직관적으로 접근함을 뜻한다.
         * Session같은 context 정보를 신경 쓸 필요 없다.
      + Cacheable
         * Http HEAD의 "Last-modified, E-Tag" 등을 사용하여 Client에 자체 캐싱된 데이터를 사용하도록 유도한다.
      + Layered System : LB가 대표적이며, 클라이언트가 서버에 어떤식으로(어떤곳에) 연결되었는지 알 수 없다.
      + Code on demand
         * optional
         * 서버는 클라이언트 로컬에서 실행 가능한 코드를 전송한다.(javascript..)
      + 인터페이스 일관성 : 아키텍쳐를 작은 단위로 분리함으로써 Client-Server가 독립적으로 개선될 수 있게한다.
      + **프로그램 처리 방식에 일관성을 부여하고, 서버의 부담을 줄인다.**

### 1.1.2. RESTful
* REST를 REST답게 사용하기 위한 방법.
   - REST는 아키텍쳐 원리를 따르는 시스템.
   - REST의 6가지 조건을 충복하기 위한 가이드 라인.

* www에서의 RESTful

| CURD   | HTTP Method | URL           | Description               |
|:------:|:-----------:|:------------- |:--------------------------|
| Read	 | GET         | /resource     | resource들의 목록을 표시    |
| Read   | GET         | /resource/:id | resource 하나의 내용을 표시 |
| Create | POST        | /resource     | resource를 생성            |
| Update | PUT         | /resource/:id | resource를 수정            |
| Delete | DELETE      | /resource/:id | resource를 삭제            ||

****

# 2. 내용
## 2.1. 내용
* 내용
   - 내용
   - 내용

## 2.2. 내용
* 내용
   - 내용
   - 내용

## 2.3. 내용
* 내용
   - 내용
   - 내용

****

# 3. 내용
## 3.1. 내용 
* 내용

## 3.2. 내용 
* 내용

## 3.3. 내용 
* 내용