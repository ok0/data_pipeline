# AWS Lambda
## 1. Labmda Architecture?
### 1.1. 개념
![high-level perspectiv](http://lambda-architecture.net/img/la-overview_small.png)
1. 시스템에 입력되는 **data**는 Batch layer와 Speed Layer에 전달.
2. **Batch Layer**는 2가지 function을 수행한다.
   2.1. Master dataset 관리.
   2.2. batch 작업을 통한 데이터 생성 관리.
3. **Serving layer**는 짧은 시간(low-latency)안에 질의가 종료될 수 있도록 데이터를 인덱싱.
4. **Speed layer**는 최근 데이터만을 관리하여, serving layer의 지연(high-latency)을 보정한다.
5. 배치 처리 된 데이터와 실시간 데이터를 병합하여 **조회(query)**한다.

### 1.2. Layer

#### 1.2.1. Batch layer
* 배치 레이어의 저장소에는 가공하지 않은 원본 데이터를 저장한다.
* 데이터가 사용 된 이후에도 삭제하지 않는다.
   - Batch view의 데이터 오계산 또는 유실.
   - 새로운 view를 만들고 싶을 때.

#### 1.2.2. Serving Layer
* batch 작업을 통해 저장된 데이터를 조회할 수 있는 view를 제공한다.
* 데이터에 대한 갱신은 Batch Layer에서의 작업을 통해 이루어져야 무결성을 보존할 수 있다.

#### 1.2.3. Speed layer
* 최근 데이터에 대한 view를 제공한다.
   - Batch View와 중복되는 데이터가 없어야한다.
* 실시간 데이터를 관리하므로 퍼포먼스에 대한 신경을 써야한다.

#### 1.2.4. 빅데이터에 적용 된 아키텍쳐
![](https://knoldernarayan.files.wordpress.com/2017/01/lambda-architecture-2-800.jpg)
* 배치 작업을 통한 데이터와 실시간 데이터를 **merge**하여 필요한 데이터를 얻는다.
****

## 2. AWS의 Lambda
## 2.1. AWS Lambda 사용 사례
* 실시간 파일 처리
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-RealTimeFileProcessing.a59577de4b6471674a540b878b0b684e0249a18c.png)

* 웹 어플리케이션
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-WebApplications%202.c7f8cf38e12cb1daae9965ca048e10d676094dc1.png)

* 실시간 스트림 처리
![](https://d1.awsstatic.com/product-marketing/Lambda/Diagrams/product-page-diagram_Lambda-RealTimeStreamProcessing.d79d55b5f3a5d6b58142a6c0fc8a29eadc81c02b.png)
****