## Swagger란
- Swagger는 Open Api Specification(OAS)를 위한 프레임워크
- API들이 가지고 있는 스펙(spec)을 명세, 관리할 수 있는 프로젝트

## 서브 프로젝트
### Swagger Editor
- 웹 UI에서 yaml형식으로 swagger 스펙을 직접 작성하거나, 미리 작성한 스펙을 불러와서 수정할 수 있는 편집기입니다.
- http://editor.swagger.io

### Swagger UI
- 컴퓨터가 이해한 스웨거 스펙을 개발자(==사람)가 이해할 수 있도록 UI로 표현해 줍니다. 요청과 응답 스펙을 나열해 놓은 단순 문서에 그치지 않고, 각 API를 실제로 요청해 볼 수 있습니다. 개발자들은 이 UI를 이용해서 테스트 데이터를 만든다거나, 자신이 개발하는 애플리케이션에서 보낸 요청의 정상 처리 여부 등을 조회해 볼 수 있습니다.
- http://petstore.swagger.io

### Swagger Codegen
- 스웨거 스펙을 기반으로 서버 또는 클라이언트 SDK(=~ 라이브러리 + 문서 등)를 만들어 줍니다. 즉, 스펙만 있으면 서버 또는 클라이언트 코드를 뚝딱 만들고, 복붙 또는 의존성 관리자로 끼워 넣어서 서비스를 빠르게 개발 할 수 있도록 도와줍니다.

## Swagger 스펙 작성
- Swagger Editor
  + 코드와 문서가 서로 따로 관리되어 문서가 코드의 최신 내용을 정확히 반영하지 못 할 확률이 높다.
- Annotation
  + Annotation 문법을 익혀야 한다.
  + 코드가 완성되기 전에 API 문서를 공개하지 못할 수도 있다.

## YAML
Swagger는 기본적으로 YAML 포맷을 이용해 Docs 문서를 작성한다. 
물론 JSON 포맷으로도 가능하지만, Swagger가 기본으로 채택한 YAML도 살펴볼 필요가 있다.

- XML, C, 파이썬, 펄, RFC2822에서 정의된 e-mail 양식에서 개념을 얻어 만들어진 사람이 쉽게 읽을 수 있는 데이터 직렬화 양식이다.
- YAML Ain’t Markup Language (YAML은 마크업이 아닌 데이터 자체를 중요시 여긴다는 뜻에서 지어진 이름이다.)

## PHP에 설치하는 방법
참고(http://zircote.com/swagger-php/Getting-started.html#installation)
