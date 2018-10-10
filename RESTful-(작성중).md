# 1. REST? / RESTful?
## 1.1. REST
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

   - REST를 정의하는 6가지 제한.
      + Client - server
      + Stateless : 각각의 요청은 독립적이어야 한다. 현재의 요청이 다음의 요청에 영향을 주어선 안된다. 
         * '없음'이란 오브젝트에 직관적으로 접근함을 뜻한다.
         * '요청'을 처리하는데 필요한 모든 정보가 '요청'에 포함되어있다.
         * Session같은 context 정보를 신경 쓸 필요 없다.
      + Cacheable
         * Http HEAD의 "Last-modified, E-Tag" 등을 사용하여 Client에 자체 캐싱된 데이터를 사용하도록 유도한다.
      + Layered System : LB가 대표적이며, 클라이언트가 서버에 어떤식으로(어떤곳에) 연결되었는지 알 수 없다.
      + Code on demand
         * optional
         * 서버는 클라이언트 로컬에서 실행 가능한 코드를 전송한다.(javascript..)
      + 인터페이스 일관성 : 아키텍쳐를 작은 단위로 분리함으로써 Client-Server가 독립적으로 개선될 수 있게한다.

   - REST의 목표
      + Interface의 범용성
      + 요소의 독립성
      + Server - Client 상호 규모 확장.
      + 매개 요소를 통한 지연 감소, 보안, 레거시 시스템 캡슐화

**프로그램 처리 방식에 일관성을 부여하고, 서버의 부담을 줄인다.**

## 1.2. RESTful
* REST를 REST답게 사용하기 위한 방법
   - REST 아키텍쳐 원리를 따르는 시스템.
   - REST의 6가지 조건을 충복하기 위한 가이드 라인.
* 공식적인 표준은 없다. REST는 그 자체로 표준은 아니지만 RESTful 구현은 HTTP, URI, JSON 및 XML 과 같은 표준을 사용.

****

# 2. Web service API에 적용 된 REST
* REST 아키텍쳐 원리를 따르는 API를 RESTful API라고 한다.

## 2.1. 가이드
- URL 기반(주로 Clean URL)

| Uncleaned URL                                                   | Clean URL                                 |
|:----------------------------------------------------------------|:------------------------------------------|
| http://example.com/index.php?page=name                          | http://example.com/name                   |
| http://example.com/about.html                                   | http://example.com/about                  |
| http://example.com/index.php?page=consulting/marketing          | http://example.com/consulting/marketing   |
| http://example.com/products?category=12&pid=25                  | http://example.com/products/12/25         |
| http://example.com/cgi-bin/feed.cgi?feed=news&frm=rss           | http://example.com/news.rss               |
| http://example.com/services/index.jsp?category=legal&id=patents | http://example.com/services/legal/patents |
| http://example.com/kb/index.php?cat=8&id=41                     | http://example.com/kb/8/41                |
| http://example.com/index.php?mod=profiles&id=193                | http://example.com/profiles/193           |
| http://en.wikipedia.org/w/index.php?title=Clean_URL             | http://en.wikipedia.org/wiki/Clean_URL    ||

* 행동은 HTTP Method를 통해 표현.

| CURD   | HTTP Method | URL           | Description               |
|:------:|:-----------:|:------------- |:--------------------------|
| Read	 | GET         | /resource     | resource들의 목록을 표시    |
| Read   | GET         | /resource/:id | resource 하나의 내용을 표시 |
| Create | POST        | /resource     | resource를 생성            |
| Update | PUT         | /resource/:id | resource를 수정            |
| Delete | DELETE      | /resource/:id | resource를 삭제            ||

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