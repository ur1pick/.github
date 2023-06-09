# Kafe (ShortURLs & Analytics)

Role 👩‍💻: Frontend, Infra, PM, UIUX Designer
Skill(Dev) 💻: Chart.js, JS(ES6), React, TailwindCSS, react-cookie
Skill(Ops) 🛠️: Docker, Kubernetes, PublicCloud, VM
기간 📆: 2022년 11월 1일 → 2022년 12월 13일
더 자세한 내용 🔗: https://bit.ly/41YrjP2

![Untitled](Untitled.png)

<aside>
<img src="Frame_12.png" alt="Frame_12.png" width="40px" /> 안녕하세요 단축 URL 서비스 Kafe를 개발한 카카오 클라우드 스쿨 1기 개발자과정 1조 ur1pick입니다.

</aside>

![Untitled](Untitled%201.png)

<aside>
<img src="Frame_12%201.png" alt="Frame_12%201.png" width="40px" /> Kafe는 단축 URL을 커피처럼 빠르게 생성부터 분석까지 다양한 기능을 제공하는 서비스입니다.

서비스 도메인은 kafe.one입니다. ~~현재 aws를 통해 서비스 중이므로 접속하셔서 같이 봐주시면 좋을 것 같습니다.~~ (22년12월13일 이후 외부로 서비스는 하고 있지 않습니다. 🙅‍♀️)

</aside>

![Untitled](Untitled%202.png)

![Untitled](Untitled%203.png)

![Untitled](Untitled%204.png)

<aside>
<img src="Frame_12%202.png" alt="Frame_12%202.png" width="40px" /> 프로젝트를 진행하기에 앞서, 저희는 기존 단축 URL서비스들이 가지고 있던 문제점들에 대해 파악했습니다.

</aside>

![Untitled](Untitled%205.png)

<aside>
<img src="Frame_12%203.png" alt="Frame_12%203.png" width="40px" /> 그 결과, 카카오 DevTalk을 통하여, 이전에 카카오에서 단축 URL 서비스가 외부로 제공되었었지만, 원본소스가 스팸이나 바이러스 등 사용자에게 좋지 않은 경험을 주는 컨텐츠가 90% 이상이었고 이런 이유로 카카오에서도 해당 서비스를 내부에서만 사용하고 있다는 것을 확인하였습니다.

</aside>

![Untitled](Untitled%206.png)

<aside>
<img src="Frame_12%204.png" alt="Frame_12%204.png" width="40px" /> 또 다른 문제점으로는 카카오 단축 URL을 사용하고 있는 Client들은 한 번 만들어진 단축 URL의 원주소를 변경하지 못한다는 문제점을 겪고 있던 것을 확인하였습니다.

</aside>

![Untitled](Untitled%207.png)

<aside>
<img src="Frame_12%205.png" alt="Frame_12%205.png" width="40px" /> 저희는 DevTalk을 통해 확인한 단축 URL 악용과 원본 URL 수정이 불가능하다는 두 가지 문제를 해결하여 “[기술과 사람이 만드는 더 나은 서비스](https://www.kakaocorp.com/page/kakao/kakaoCulture)” 를 개발하고자 하였습니다.

</aside>

![Untitled](Untitled%208.png)

![Untitled](Untitled%209.png)

<aside>
<img src="Frame_12%206.png" alt="Frame_12%206.png" width="40px" /> 문제정의 이후 저희는 안전한 단축 URL 서비스와 단축 URL을 통해 얻은 통계 데이터를 분석하여 사용자에게 제공하고자 했습니다.

</aside>

![Untitled](Untitled%2010.png)

<aside>
<img src="Frame_12%207.png" alt="Frame_12%207.png" width="40px" /> 옵션을 설정하는 사용자 지정의 단축 URL 생성 기능과 앞서 말씀드린 두가지 문제점을 보완한 악성 URL에 대한 필터링 기능과 원본 URL 수정 기능을 통해 안전한 단축 URL서비스를 제공합니다. 해당 기능은 SpringBoot, RabbitMQ, Selenium, QueryDSL을 통해 구현했습니다.

</aside>

![Untitled](Untitled%2011.png)

<aside>
<img src="Frame_12%208.png" alt="Frame_12%208.png" width="40px" /> 접속자 및 유입 경로에 대한 통계 데이터를 시각화한 대시보드 기능과 주간 접속자 추이에 관한 리포트를 메일로 발송하는 기능을 통해 단축 URL에 대한 분석 서비스를 제공하려고 합니다. 해당 기능은 ELK 스택, React, Chart.js, Matplotlib 등 을 통해 구현했습니다.

</aside>

![Untitled](Untitled%2012.png)

![Untitled](Untitled%2013.png)

<aside>
<img src="Frame_12%209.png" alt="Frame_12%209.png" width="40px" /> 저희 서비스의 핵심 기능은 
첫번째, 단축 URL 커스텀 기능
두번째, 단축 URL 악용 문제를 해결하기 위한 필터링 기능
첫번째, 단축 URL을 통해 얻은 통계데이터를 시각화하여 제공하는 기능입니다.

</aside>

![Untitled](Untitled%2014.png)

<aside>
<img src="Frame_12%2010.png" alt="Frame_12%2010.png" width="40px" /> 첫번째, 단축 URL 커스텀 기능은
사용자가 원하는 단축 URL 주소를 지정하거나 유효기간 및 비밀번호를 설정할 수 있습니다.

</aside>

![Untitled](Untitled%2015.png)

<aside>
<img src="Frame_12%2011.png" alt="Frame_12%2011.png" width="40px" /> 생성한 URL에 대해서 원주소를 수정하거나 유효기간 및 비밀번호도 수정 가능합니다.

</aside>

![Untitled](Untitled%2016.png)

<aside>
<img src="Frame_12%2012.png" alt="Frame_12%2012.png" width="40px" /> 그리고 활성화된 URL을 비활성화 상태로 변경할 수도 있습니다.

</aside>

![Untitled](Untitled%2017.png)

<aside>
<img src="Frame_12%2013.png" alt="Frame_12%2013.png" width="40px" /> 다음 악성 URL 필터링 기능은 4단계로 이루어져 있습니다.

첫번째,  블랙리스트 기반 필터링입니다.

블랙리스트는 피시탱크에서 제공하는 피싱사이트 목록을 AWS Lambda를 이용하여 매시간 업데이트하고 있고, 관리자가 추가할 수도 있습니다.

두번째, 화이트리스트 기반 필터링 입니다.

접속자 기준 상위 50위에 있는 도메인이면 안전하다고 판단합니다.

세번째로 인증서 유효성 기반 필터링을 거치게 되고

마지막으로 유사도 분석을 통한 필터링을 거칩니다.

피싱 사이트들은 검증된 도메인과 최대한 유사하게 보이려는점을 역이용하여 검증된 도메인과의 유사도 분석을 통해 악성 URL인지 판단합니다.

</aside>

![Untitled](Untitled%2018.png)

<aside>
<img src="Frame_12%2014.png" alt="Frame_12%2014.png" width="40px" /> 통계 데이터는 단축 URL을 이용하는 로그, kafe 서비스에 접속하는 로그를 로그스태시의 그록디버거를 통해 패턴을 분석한 후 엘라스틱서치에 저장합니다.

이렇게 저장된 데이터는 사용자 대시보드 및 주간 리포트,키바나에서 사용됩니다.

</aside>

![Untitled](Untitled%2019.png)

<aside>
<img src="Frame_12%2015.png" alt="Frame_12%2015.png" width="40px" /> 사용자 대시보드에서는 ip 기반 국가별 접속량, useragent 기반의 브라우저, 디바이스, sns와같은 유입경로 데이터와 timestamp 기반의 트래픽 데이터들을
React Chart.js를 통해 시각화합니다.

</aside>

![Untitled](Untitled%2020.png)

<aside>
<img src="Frame_12%2016.png" alt="Frame_12%2016.png" width="40px" /> 주간 리포트에서는 브라우저, 디바이스, sns 기반의 유입경로 데이터와
요일별 트래픽 데이터들을 맽플랏라이브러리를 통해 시각화해서 사용자에게 메일로 발송합니다.

</aside>

![Untitled](Untitled%2021.png)

<aside>
<img src="Frame_12%2017.png" alt="Frame_12%2017.png" width="40px" /> 관리자 대시보드에서는 kafe 서비스에 접속하는 로그를 기반으로

국가별 접속량과 유입경로 데이터 그리고 시간별 트래픽 데이터를 Kibana를 통해 시각화합니다.

</aside>

### 🎥 시연영상

[KakaoTalk_Video_2022-12-18-04-13-56.mov](KakaoTalk_Video_2022-12-18-04-13-56.mov)

![Untitled](Untitled%2022.png)

<aside>
<img src="Frame_12%2018.png" alt="Frame_12%2018.png" width="40px" /> 저희 서비스를 구성하는 아키텍처에 대해 설명 드리겠습니다.

</aside>

![Untitled](Untitled%2023.png)

<aside>
<img src="Frame_12%2019.png" alt="Frame_12%2019.png" width="40px" /> 초기 개발단계의 로컬 환경 및 클라우드 환경을 기반으로 하여
쿠버네티스, 스프링, AWS 등 여러 가지 소프트웨어나 서비스, 라이브러리를 사용하였습니다.

</aside>

![Untitled](Untitled%2024.png)

<aside>
<img src="Frame_12%2020.png" alt="Frame_12%2020.png" width="40px" /> 현재 AWS에 적용되어 있는 저희 서비스의 클라우드 아키텍처 입니다.
서비스에 맞추어 여러 리소스를 사용중입니다.

</aside>

![Untitled](Untitled%2025.png)

<aside>
<img src="Frame_12%2021.png" alt="Frame_12%2021.png" width="40px" /> S3 버킷은 서비스에 필요한 이미지 및 ELB 로그를 저장하는 목적으로 사용하고 있습니다.

</aside>

![Untitled](Untitled%2026.png)

<aside>
<img src="Frame_12%2022.png" alt="Frame_12%2022.png" width="40px" /> EFS 스토리지는 Kubernetes Persistent Volume을 위해 사용중입니다.

</aside>

![Untitled](Untitled%2027.png)

<aside>
<img src="Frame_12%2023.png" alt="Frame_12%2023.png" width="40px" /> AWS Lambda 같은 경우는 주기적으로 블랙리스트를 업데이트 하는 작업에 사용하고 있으며,
이를 위해 클라우드워치 이벤트 브릿지를 통한 트리거를 설정하였습니다.

</aside>

![Untitled](Untitled%2028.png)

<aside>
<img src="Frame_12%2024.png" alt="Frame_12%2024.png" width="40px" /> CloudWatch는 트리거뿐만 아니라 EC2 인스턴스들의 리소스를 모니터링 하는 용도로도 사용하고 있습니다.

</aside>

![Untitled](Untitled%2029.png)

<aside>
<img src="Frame_12%2025.png" alt="Frame_12%2025.png" width="40px" /> VPC 및 EKS 클러스터의 구조는 화면과 같으며 이는 AWS에서 제공하는 코드형 인프라인 CloudFormation을 이용하여 구축하였습니다.

</aside>

![Untitled](Untitled%2030.png)

<aside>
<img src="Frame_12%2026.png" alt="Frame_12%2026.png" width="40px" /> EKS에서 사용하는 워커 노드는 EC2 인스턴스로 구성중입니다.

</aside>

![Untitled](Untitled%2031.png)

<aside>
<img src="Frame_12%2027.png" alt="Frame_12%2027.png" width="40px" /> 저희 서비스는 프론트엔드, 백엔드, 데이터베이스까지의 모든 영역을 현재 EKS 상에서 배포하고 있습니다.
서비스를 위한 다양한 Pod 뿐 아니라 영속성 유지가 필요한 데이터베이스, 클러스터 내부 리소스 모니터링을 위한 도구도 전부 컨테이너 환경에서 동작하고 있습니다.

</aside>

![Untitled](Untitled%2032.png)

<aside>
<img src="Frame_12%2028.png" alt="Frame_12%2028.png" width="40px" /> 단축 URL 생성 과정입니다.

</aside>

![Untitled](Untitled%2033.png)

<aside>
<img src="Frame_12%2029.png" alt="Frame_12%2029.png" width="40px" /> 사용자는 단축 URL 생성 요청을 서버로 전송합니다.
이는 EKS에서 ingress 생성 시 자동으로 프로비저닝 되는 ALB를 통해 로드밸런싱 되며

</aside>

![Untitled](Untitled%2034.png)

<aside>
<img src="Frame_12%2030.png" alt="Frame_12%2030.png" width="40px" /> 서비스 로직을 담당하는 Pod에 도달합니다. 해당 요청을 해석하여 적절한 단축 URL을 생성합니다.

</aside>

![Untitled](Untitled%2035.png)

<aside>
<img src="Frame_12%2031.png" alt="Frame_12%2031.png" width="40px" /> 이후 MySQL에서 제공하는 Operator를 이용한 데이터베이스 클러스터에 필요한 내용을 저장합니다. 
마지막으로 생성된 단축 URL은 요청을 보낸 사용자에게 응답됩니다. 이런 과정을 통해 사용자는 간단하게 단축 URL을 생성할 수 있습니다.

</aside>

![Untitled](Untitled%2036.png)

<aside>
<img src="Frame_12%2032.png" alt="Frame_12%2032.png" width="40px" /> 통계 데이터는 단축 URL을 이용하는 로그, kafe 서비스에 접속하는 로그를 로그스태시의 그록디버거를 통해 패턴을 분석한 후 엘라스틱서치에 저장합니다.

이렇게 저장된 데이터는 사용자 대시보드 및 주간 리포트,키바나에서 사용됩니다.

</aside>

![Untitled](Untitled%2037.png)

<aside>
<img src="Frame_12%2033.png" alt="Frame_12%2033.png" width="40px" /> 만약 원주소가 악성 URL이라고 가정해보겠습니다.

URL 생성 과정은 동일하지만, 앞에서 말씀 드렸던 4단계의 필터링을 통해 악성 URL로 판별되면 별도의 작업이 생성 됩니다. 이는 RabbitMQ를 사용하여 비동기적으로 처리합니다. 

작업 메시지가 메세지 큐에 적재되고, 이를 사이트 프리뷰를 생성하는 모듈이 처리합니다.
해당 프리뷰 생성 모듈은 별도로 실행중인 Selenium 서버를 통해 사이트 스크린샷을 생성합니다.
생성된 스크린샷은 S3 버킷에 저장되고, 이에 대한 정보는 데이터베이스에 자동 갱신됩니다.

</aside>

![Untitled](Untitled%2038.png)

<aside>
<img src="Frame_12%2034.png" alt="Frame_12%2034.png" width="40px" /> 이후, 사용자가 단축 URL에 접근 시 리다이렉트를 담당하는 모듈은 저장된 단축 URL 정보를 조회하여
사용자에게 제공합니다.
만약, 목적지 주소가 악성 사이트라면 즉시 리다이렉트 응답을 보내는 것이 아닌 앞서 생성되었던 사이트 프리뷰를 제공하는 경고창을 표시하여, 사용자가 스스로 사이트 접속 여부를 판단할 수 있게 합니다.
본 서비스에서 실제로 제공하고 있는 경고창입니다.
단축 URL의 원주소와 셀레니움을 통해 생성된 해당 사이트의 스크린샷을 확인할 수 있습니다.

</aside>

![Untitled](Untitled%2039.png)

<aside>
<img src="Frame_12%2035.png" alt="Frame_12%2035.png" width="40px" /> 현재 클러스터 내부 파드에 대한 리소스 모니터링에 Prometheus를 사용하고 있습니다.
각 워커 노드 그룹에 데몬셋을 통해 배포된 node-exporter를 통해 메트릭 정보를 Prometheus로  수집하고 저장합니다.
이렇게 수집된 파드 리소스에 대한 메트릭 데이터는 Grafana를 통해 시각화하여 서비스 유지를 위해 활용하고 있습니다.

</aside>

![Untitled](Untitled%2040.png)

<aside>
<img src="Frame_12%2036.png" alt="Frame_12%2036.png" width="40px" /> 현재 화면에 나오는 대시보드가 저희가 실제로 사용중인 Grafana 대시보드 입니다.
앞서 모니터링에 CloudWatch를 사용한다고 말씀드렸는데, CloudWatch는 현재 노드그룹과 gitlab 등 인스턴스에 대한 메트릭 정보만 수집하여 모니터링 중이지만
CloudWatch 사용에 대한 비용을 절감하기 위해서 EKS 클러스터 내부 파드에 대한 리소스 정보는 prometheus를 통해 수집중입니다.

</aside>

![Untitled](Untitled%2041.png)

<aside>
<img src="Frame_12%2037.png" alt="Frame_12%2037.png" width="40px" /> CI/CD 파이프라인에 대해 간단히 설명드리겠습니다.
저희 팀은 CI/CD를 위해 GitLab을 이용하였으며, 현재 AWS 환경에 별도로 GitLab 서버를 구동하는 인스턴스를 생성하여 사용 중입니다.
GitLab 하나로 여러 기능을 한번에 활용할 수 있었고 익숙한 UI였기에 선택했습니다.
GitLab Agent와 Runner를 환경에 배포하여 CI/CD 작업을 수행하고 있으며,
이에 대한 동작은 yaml 파일로 관리 가능합니다.

</aside>

![Untitled](Untitled%2042.png)

![Untitled](Untitled%2043.png)

<aside>
<img src="Frame_12%2038.png" alt="Frame_12%2038.png" width="40px" /> 전체적인 일정관리는 구글 스프레드시트로 진행했습니다.

</aside>

![Untitled](Untitled%2044.png)

<aside>
<img src="Frame_12%2039.png" alt="Frame_12%2039.png" width="40px" /> 스프레드시트 내용을 기반으로 보기 쉽게 도식화하여 설명드리자면
전체 일정을 로컬환경에서의 테스트 기간과 클라우드 마이그레이션 기간
두단락으로 나눠서 진행하였습니다

</aside>

![Untitled](Untitled%2045.png)

<aside>
<img src="Frame_12%2040.png" alt="Frame_12%2040.png" width="40px" /> 업무 관리는 노션으로 진행했는데 업무별 문서 산출물을 동시에 관리할 수 있어서 좋았습니다.

</aside>

![Untitled](Untitled%2046.png)

![Untitled](Untitled%2047.png)

<aside>
<img src="Frame_12%2041.png" alt="Frame_12%2041.png" width="40px" /> 현재 악성 URL 필터링 중 유사도 분석 과정에서 편집거리 알고리즘만 단독으로 사용하고 있는데
다른 알고리즘도 함께 사용하면 정확도를 더 높일 수 있을것 같습니다.

두번째로 로그 데이터가 geopoint로 변환이 되지 않아 Elasticsearch 쿼리를 두 번씩 사용하고 있는데, 해당 부분은 엘라스틱서치와 연동되는 Spring 모듈이 시작될 때, 인덱스 타입을 지정해 놓으면 해결될 것으로 예상됩니다.

현재 인프라 일부를 코드형으로 구성했는데 나중에는 테라폼을 통해 인프라부터 서비스까지 전체를
코드로 관리, 배포하여 자동화까지 구축해보고 싶습니다.

</aside>

![Untitled](Untitled%2048.png)

<aside>
☕ 저희는 6개월동안 개발부터 클라우드까지 전반으로 교육을 받으면서 힘들었지만 많이 성장할 수 있었습니다. 뿐만아니라 업무를 위한 업무 즉 문서 작업 및 일정 관리에 중점을 두어 프로젝트를  진행했고 이를 통해 실제 업무환경에서 잘 적응할 수 있다는 자신감을 얻었습니다.

</aside>
