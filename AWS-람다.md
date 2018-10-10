# AWS Lambda
## 1. Lambda?
* 람다 대수 : 네임 바인딩과 대입의 방법을 이용하여 함수 정의, 함수 적용, 귀납적 함수 추상화를 수행하고 수학 연산을 표현하는 형식 체계이다.
   - 함수형 프로그래밍의 핵심 개념.
****

## 2. Lambda Architecture?
### 2.1. 개념
![high-level perspectiv](http://lambda-architecture.net/img/la-overview_small.png)
1. 시스템에 입력되는 **data**는 Batch layer와 Speed Layer에 전달.
2. **Batch Layer**는 2가지 function을 수행한다.
   2.1. Master dataset 관리.
   2.2. batch 작업을 통한 데이터 생성 관리.
3. **Serving layer**는 짧은 시간(low-latency)안에 질의가 종료될 수 있도록 데이터를 인덱싱.
4. **Speed layer**는 최근 데이터만을 관리하여, serving layer의 지연(high-latency)을 보정한다.
5. 배치 처리 된 데이터와 실시간 데이터를 병합하여 **조회(query)**한다.

### 2.2. Layer
#### 2.2.1. Batch layer
* 배치 레이어의 저장소에는 가공하지 않은 원본 데이터를 저장한다.
* 데이터가 사용 된 이후에도 삭제하지 않는다.
   - Batch view의 데이터 오계산 또는 유실.
   - 새로운 view를 만들고 싶을 때.

#### 2.2.2. Serving Layer
* batch 작업을 통해 저장된 데이터를 조회할 수 있는 view를 제공한다.
* 데이터에 대한 갱신은 Batch Layer에서의 작업을 통해 이루어져야 무결성을 보존할 수 있다.

#### 2.2.3. Speed layer
* 최근 데이터에 대한 view를 제공한다.
   - Batch View와 중복되는 데이터가 없어야한다.
* 실시간 데이터를 관리하므로 퍼포먼스에 대한 신경을 써야한다.

#### 2.2.4. 빅데이터에 적용 된 아키텍쳐
![](https://knoldernarayan.files.wordpress.com/2017/01/lambda-architecture-2-800.jpg)
* 배치 작업을 통한 데이터와 실시간 데이터를 **merge**하여 필요한 데이터를 얻는다.
****

## 3. AWS의 Lambda
### 3.1. AWS Lambda 작동 방식 / 사용 사례
* 작동방식
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-HowItWorks.68a0bcacfcf46fccf04b97f16b686ea44494303f.png)

* 실시간 파일 처리
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-RealTimeFileProcessing.a59577de4b6471674a540b878b0b684e0249a18c.png)

* 웹 어플리케이션
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-WebApplications%202.c7f8cf38e12cb1daae9965ca048e10d676094dc1.png)

* 실시간 스트림 처리
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-RealTimeStreamProcessing.d79d55b5f3a5d6b58142a6c0fc8a29eadc81c02b.png)

## 3.2. AWS Lambda란 ?
###### Run code without thinking about servers. Pay only for the compute time you consume.
* 서버를 프로비저닝하거나 관리할 필요 없이 코드 실행.
* 사용한 컴퓨팅 시간만큼만 비용을 지불하고, 이외 시간에는 요금이 부과되지 않음.
* 코드를 업로드하기만 하면, 높은 가용성으로 코드를 실행 및 확장.
* 다른 AWS 서비스에서 코드를 자동으로 트리거 하도록 설정하거나 웹 또는 모바일 APP에서 직접 호출 가능.

### 3.3. AWS Lambda 장점
* Serverless
   - 인프라에 대한 걱정 없이 코드 실행 가능.
* Continous Scaling
   - 트리거를 이용해 자동으로 확장/축소 가능.
   - 코드는 병렬로 실행되고, 각 트리거를 개별적으로 처리되기 때문에 정확한 workload에 맞게 조정.
* Subsecond metering
   - 100ms 단위로 코드 실행시간을 측정.
   - 트리거되는 회수 측정.
   - 코드가 실행되지 않을 때는 요금이 부과되지 않는다.

****