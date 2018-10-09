## Swagger란
* Swagger는 Open Api Specification(OAS)를 위한 프레임워크 입니다.
API들이 가지고 있는 스펙(spec)을 명세, 관리할 수 있는 프로젝트 입니다. 협업을 진행하거나 이미 만들어져 있는 프로젝트에 대해 유지보수를 진행하게 된다면 구축되어 있는 API서버가 어떤 스펙을 가지고 있는지 파악해야 합니다. 이러한 스펙을 정리하기 위해 API 문서화 작업을 하게 되며, 위의 과정을 직접 손으로 하게되는 경우 작업에 착수하기 전에 API의 명세와 문서를 작성하고,  API가 수정될 때 마다 문서도 같이 수정해줘야 하는  불편함을 조금이나마 줄여주기 위해 개발된 것이 "Swagger Project" 입니다.



## 서브 프로젝트
### Swagger Editor
- 웹 UI에서 yaml형식으로 swagger 스펙을 직접 작성하거나, 미리 작성한 스펙을 불러와서 수정할 수 있는 편집기입니다.
- http://editor.swagger.io

### Swagger UI
- 컴퓨터가 이해한 스웨거 스펙을 개발자(==사람)가 이해할 수 있도록 UI로 표현해 줍니다. 요청과 응답 스펙을 나열해 놓은 단순 문서에 그치지 않고, 각 API를 실제로 요청해 볼 수 있습니다. 개발자들은 이 UI를 이용해서 테스트 데이터를 만든다거나, 자신이 개발하는 애플리케이션에서 보낸 요청의 정상 처리 여부 등을 조회해 볼 수 있습니다.
- http://petstore.swagger.io

### Swagger Codegen
- 스웨거 스펙을 기반으로 서버 또는 클라이언트 SDK(=~ 라이브러리 + 문서 등)를 만들어 줍니다. 즉, 스펙만 있으면 서버 또는 클라이언트 코드를 뚝딱 만들고, 복붙 또는 의존성 관리자로 끼워 넣어서 서비스를 빠르게 개발 할 수 있도록 도와줍니다.

참고(http://blog.appkr.kr/work-n-play/learn-n-think/serving-swagger-api-in-php-project/)

## Swagger 스펙 작성
스웨거 스펙 정의 언어(IDL INTERFACE DEFINITION LANGUAGE) 문법을 익혀, Swagger Editor에서 직접 작성하면 됩니다. 또 하나의 방법은 API 서버 프로젝트에 특별한 패키지를 설치하고, 코드에서 Annotation으로 API 문서를 쓴 후, Annotation을 스웨거 스펙으로 변경하는 특별한 명령을 실행하는 방법입니다.

직접 쓰는 방법은 코드와 문서가 서로 따로 관리되어 문서가 코드의 최신 내용을 정확히 반영하지 못한다거나, 또는 반대의 경우가 발생할 소지가 큽니다. 반면, Annotation 등을 이용하는 방법은 코드와 문서가 같이 존재하므로 앞서 지적한 문제는 덜하겠지만, Annotation 문법을 익혀야 하며, 자칫 코드가 완성되기 전에 API 문서를 공개하지 못하는 함정에 빠지기 쉽습니다.

API는 약속입니다. 두 모듈을 개발하는 개발자들, 즉 서버와 클라이언트 개발자들이 미리 정의한 약속에 따라 개발을 한다면, 어느 한 쪽의 모듈 개발이 끝날 때까지 다른 모듈 개발자가 기다려야 하는 것이 아니라, 약속에 맞추어서 병렬로 개발할 수 있습니다. 인터페이스가 변경되지 않는 한, 상호 독립적으로 개발하고, 상호 독립적으로 빌드/패키징하고, 상호 독립적으로 배포할 수 있습니다.

정리하자면, 후자를 택한다 해도, API 서버 프로젝트의 HTTP 컨트롤러에서 더미 응답을 제공하는 최소 수준만 코드 작업하고, Annotation을 써서 빠르게 클라이언트 API를 정의할 수 있습니다. 나중에 약간의 변경이 생기더라도, 약속을 빨리 정하는 것이 개발 기간, 품질, 팀웍 모든 면에서 낫다는 점을 경험으로 배웠습니다. 스웨거는 과거의 “Code first” 개발 방식이 아니라, “Document first and generate boilerplate”, 즉 RAD RAPID APPLICATION DEVELOPMENT를 추구하는 현대적인 애플리케이션 개발 방식을 담고 있습니다.

참고(http://blog.appkr.kr/work-n-play/learn-n-think/serving-swagger-api-in-php-project/)
ㅁ
## YAML
Swagger는 기본적으로 YAML 포맷을 이용해 Docs 문서를 작성한다. 
물론 JSON 포맷으로도 가능하지만, Swagger가 기본으로 채택한 YAML도 살펴볼 필요가 있다.

- XML, C, 파이썬, 펄, RFC2822에서 정의된 e-mail 양식에서 개념을 얻어 만들어진 사람이 쉽게 읽을 수 있는 데이터 직렬화 양식이다.
- YAML Ain’t Markup Language (YAML은 마크업이 아닌 데이터 자체를 중요시 여긴다는 뜻에서 지어진 이름이다.)

참고(http://sanghaklee.tistory.com/50)

## PHP에 설치하는 방법
참고(http://zircote.com/swagger-php/Getting-started.html#installation)
