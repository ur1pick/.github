# Kafe (ShortURLs & Analytics)

![Kafe](https://github.com/ur1pick/.github/assets/80504636/7b57785b-91b5-41a0-b6c6-6c94eb878634)

### 🔗 **~~[배포물 바로가기](https://kafe.one)~~**
(22년12월13일 이후 외부로 서비스는 하고 있지 않습니다. 🙅‍♀️)

### 🎥 **[시연 영상 바로가기](https://youtu.be/2shrlOw4nhw)**

<br>

**🗂 GitHub Repository**
- 🏭 [Backend](https://github.com/ur1pick/kafe_backend)

- 🖼 [Frontend](https://github.com/ur1pick/kafe_frontend)

<br/>

**목차**

- [프로젝트 소개](#intro)
- [기술 스택](#stack)
- [아키텍처](#architecture)
- [구현 기능](#function)
- [회고](#retrospective)

<br>

# <span id="intro">📋 프로젝트 소개</span>

단축 URL이 스미싱 수단으로 악용되는 문제를 해결하기 위해 필터링 기능을 추가한 단축 URL 웹 서비스를 개발하여 On-premise 환경에서 테스트 후 클라우드로의 마이그레이션과 퍼블릭 클라우드에서의 인프라 구성 및 서비스 배포를 목표로 한 프로젝트

<br>

# <span id="stack">🚀 기술 스택</span>

| Java | SpringBoot | Selenium |
| :---: | :---: | :---: |
| <img width="50" alt="Java" src="https://user-images.githubusercontent.com/80504636/231357444-f19f60b4-b037-4243-9fd0-7335f805e1ab.png"> | <img width="60" alt="SpringBoot" src="https://user-images.githubusercontent.com/80504636/231356152-2eb8bc40-a505-41db-8b48-34cb08307872.png"> | <img width="60" alt="Untitled 1" src="https://github.com/ur1pick/.github/assets/80504636/51e9f561-30e0-4c39-85bf-18f11848c576"> | 

| JavaScript | React | Chart.js |
| :---: | :---: | :---: |
| <img width="50" alt="Untitled 1" src="https://github.com/ur1pick/.github/assets/80504636/383e8ac0-1ab6-4c8b-81bd-2cb32b1c8e8a"> | <img width="60" alt="Untitled 1" src="https://user-images.githubusercontent.com/80504636/231356159-a1ed8d6a-1945-4c86-8a82-41295fad3d40.png"> | <img width="60" alt="Untitled 1" src="https://github.com/ur1pick/.github/assets/80504636/32ad955c-7c55-4e15-a3f5-855a3397051f"> |


| MySQL |  RabbitMQ |
| :---: | :---: | 
| <img width="60" alt="Untitled 1" src="https://github.com/ur1pick/.github/assets/80504636/54b7c318-ddd2-45c5-b0c9-c88bca9a0138"> | <img width="50" alt="Untitled 1" src="https://user-images.githubusercontent.com/80504636/231356154-4dd57ef2-a2e8-467d-a9ec-dda5860ebbfb.png"> |

| Docker | Kubernetes | AWS | 
| :---: | :---: | :---: |
| <img width="60" alt="Untitled 1" src="https://user-images.githubusercontent.com/80504636/231356165-0f68a283-1f64-433b-939e-d4e582530535.png">  | <img width="60" alt="Untitled 1" src="https://user-images.githubusercontent.com/80504636/231356166-2fd54dfa-b3c7-42b3-97f3-955a27b5e550.png"> | <img width="60" alt="Untitled 1" src="https://user-images.githubusercontent.com/80504636/231358883-af99f506-36b0-4912-961c-7f7d5bcc1e12.png">


<br>

# <span id="architecture">🏗 아키텍처</span>

## 클라우드 아키텍처
![aws](https://github.com/ur1pick/.github/assets/80504636/907fb6da-da44-44c4-8f42-9f8775b72146)

## 백엔드 흐름도
![backend-flow](https://github.com/ur1pick/.github/assets/80504636/2a231b22-abb0-461e-b0b5-a994419cff74)

# <span id="function">🧩 구현 기능</span>

## 1️⃣  단축 URL 커스텀 기능
![Custom1](https://github.com/ur1pick/.github/assets/80504636/6979c915-1d9c-46ea-bf69-463492590141)

> **☕️** 사용자가 원하는 단축 URL 주소를 지정하거나 유효기간 및 비밀번호를 설정할 수 있습니다.

<br>

![Custom2](https://github.com/ur1pick/.github/assets/80504636/dbc3afc4-578d-4a52-ae6e-6030cb1f3b31)

> **☕️** 생성한 URL에 대해서 원주소를 수정하거나 유효기간 및 비밀번호도 수정 가능합니다.

<br>


![Custom3](https://github.com/ur1pick/.github/assets/80504636/5850774c-0755-4349-8f61-2dc590a18da8)

> **☕️** 그리고 활성화된 URL을 비활성화 상태로 변경할 수도 있습니다.

<br>

## 2️⃣ 단축 URL 악용 문제를 해결하기 위한 필터링 기능
![filtering](https://github.com/ur1pick/.github/assets/80504636/2377b8eb-918a-4693-83c8-f8ef908c7f39)

악성 URL 필터링 기능은 4단계로 이루어져 있습니다.

- 첫번째,  블랙리스트 기반 필터링입니다.

    블랙리스트는 피시탱크에서 제공하는 피싱사이트 목록을 AWS Lambda를 이용하여 매시간 업데이트하고 있고, 관리자가 추가할 수도 있습니다.

- 두번째, 화이트리스트 기반 필터링 입니다.

    접속자 기준 상위 50위에 있는 도메인이면 안전하다고 판단합니다.

- 세번째로 인증서 유효성 기반 필터링을 거치게 되고

- 마지막으로 유사도 분석을 통한 필터링을 거칩니다.

피싱 사이트들은 검증된 도메인과 최대한 유사하게 보이려는점을 역이용하여 검증된 도메인과의 유사도 분석을 통해 악성 URL인지 판단합니다.

<br>

## 3️⃣ 단축 URL을 통해 얻은 통계데이터를 시각화하여 제공하는 기능

![dashboard1](https://github.com/ur1pick/.github/assets/80504636/9bdd2260-fe73-4207-87f8-b16d9b624b8f)

> **☕️** 통계 데이터는 단축 URL을 이용하는 로그, kafe 서비스에 접속하는 로그를 logstash의 GROK debugger를 통해 패턴을 분석한 후 elasticsearch에 저장합니다.이렇게 저장된 데이터는 사용자 대시보드 및 주간 리포트와 Kibana에서 사용됩니다.

<br>

![dashboard2](https://github.com/ur1pick/.github/assets/80504636/219f8135-7f5c-4b88-9ade-6f50f3846bac)

> **☕️** 사용자 대시보드에서는 ip 기반 국가별 접속량, useragent 기반의 브라우저, 디바이스, sns와같은 유입경로 데이터와 timestamp 기반의 트래픽 데이터들을 React Chart.js를 통해 시각화합니다.

<br>

![dashboard3](https://github.com/ur1pick/.github/assets/80504636/7f1da4e7-911e-4d5e-90d6-c7047ffb1417)

> **☕️** 주간 리포트에서는 브라우저, 디바이스, sns 기반의 유입경로 데이터와 요일별 트래픽 데이터들을 matplotlib를 통해 시각화해서 사용자에게 메일로 발송합니다.

<br>

![dashboard4](https://github.com/ur1pick/.github/assets/80504636/c8aed3a3-e660-41b2-8491-d0aa53ca39cf)

> **☕️** 관리자 대시보드에서는 kafe 서비스에 접속하는 로그를 기반으로 국가별 접속량과 유입경로 데이터 그리고 시간별 트래픽 데이터를 Kibana를 통해 시각화합니다.

<br>

# <span id="retrospective">💬 회고</span>

![retro](https://github.com/ur1pick/.github/assets/80504636/3963fcbb-6a15-4e55-859d-0932c3e2ce3b)
