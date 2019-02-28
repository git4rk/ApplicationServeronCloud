---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 정보
{: #about}

{{site.data.keyword.appserver_full}}는 {{site.data.keyword.Bluemix_notm}}의 호스팅된 클라우드 환경에서 사전 구성된 WebSphere Application Server Liberty, Traditional Network Deployment 또는 Traditional WebSphere Java EE 인스턴스의 빠른 설정을 용이하게 합니다.
{: shortdesc}

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 개요
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}는 사전 구성된 Traditional WebSphere 및 Liberty 서버를 이용자에게 제공합니다. 이는 게스트 운영 체제에 대한 루트 액세스 권한이 있는 가상 머신 게스트에서 호스팅됩니다. 서비스를 작성할 때는 _Liberty_, _Traditional ND_ 또는 _Traditional WebSphere_ 중에서 선택하십시오.

**참고:** 이제 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 인스턴스를 작성할 때 이용자가 현재 수정팩 레벨 또는 이전 버전[(n 또는 n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} 사이에서 선택할 수 있습니다.

사용자에게 비슷한 WebSphere 관리 환경이 제공되며 기본 운영 체제에 대한 전체 액세스 권한이 있습니다. 기존 스크립트를 재사용하고 자체 프레임워크 또는 서드파티 프레임워크에서 작업하도록 필요에 따라 시스템을 약간 수정할 수 있습니다. 온프레미스 WebSphere 구성과 마찬가지로 WebSphere Application Server Liberty, ND 또는 Traditional 서비스를 관리하도록 Admin Center와 Admin Console이 제공됩니다.

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 플랜은 둘 이상의 가상 머신이 있는 WebSphere Application Server Network Deployment 셀 환경으로 구성됩니다. 첫 번째 가상 머신에는 배치 관리자와 IBM HTTP Server가 포함되어 있고, 나머지 가상 머신에는 배치 관리자에 연합된 사용자 정의 노드(노드 에이전트)가 포함되어 있습니다. 기존 wsadmin 스크립트를 사용하여 WebSphere 구성을 작성하거나 WebSphere Admin Console을 사용하여 수동으로 환경을 구성하십시오. 이러한 새 기능을 통해 사용자가 클러스터 환경을 설정할 수 있으며, 이는 미들웨어 엔터프라이즈 애플리케이션의 중요한 측면입니다. 이제 클라이언트는 토폴로지를 클러스터링하여 두 개 이상의 인스턴스에서 요청을 로드 밸런싱하도록 선택할 수 있습니다.

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 플랜에도 Liberty Collective를 사용할 수 있습니다. Liberty Collective는 Liberty Profile 그룹에 대한 관리 도메인이며 둘 이상의 가상 머신으로 구성되어 있습니다. 첫 번째 가상 머신에는 Liberty Collective의 제어점인 Collective Controlle Liberty 서버가 포함됩니다. Liberty Collective 외에도 이 가상 머신에는 웹 브라우저에서 애플리케이션에 액세스할 수 있게 하는 IBM HTTP Server도 포함됩니다. 나머지 가상 머신은 집합체(collective) 멤버가 있는 집합체 호스트(Liberty 프로파일 서버)입니다. Liberty 제어기 서버에서는 Liberty Admin Center 기능도 사용됩니다.

다음 그림은 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 셀과 Liberty Collective 환경의 아키텍처를 보여줍니다.

그림 1. Network Deployment 셀 및 Liberty Collective 아키텍처

![그림 1. Network Deployment 셀 및 Liberty Collective의 아키텍처](images/CellCollectiveDiagram.gif)

**참고**: 위의 _그림 1_에서 IBM HTTP Server와 함께 Collective Controller 또는 배치 관리자의 배치를 표현하는 패턴은 개발 및 테스트 목적입니다. 또한 온프레미스에서와 마찬가지로 사용자는 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}를 사용하여 프로덕션 애플리케이션 및 운영상의 요구사항을 충족할 수 있도록 사전 설치된 소프트웨어를 자유롭게 재구성할 수도 있습니다. 또한 가장 엄격한 프로덕션 요구사항에 대해서는 격리된 네트워킹 및 컴퓨팅 리소스를 제공하는 싱글 테넌트 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 오퍼링에 대해 알려줄 수 있는 IBM 영업 담당자에게 문의하십시오.


## 운영 환경
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}는 이용자가 애플리케이션을 배치할 수 있도록 공유 환경에서 게스트(가상 머신)를 리턴하는 서비스입니다. VPN은 일반 포트 스캔 및 기타 원치 않는 네트워크 기반 공격으로부터 공용 서비스를 보호합니다. 하지만 서비스 인스턴스에 액세스하는 데 사용하는 서비스 VPN은 여러 {{site.data.keyword.Bluemix_notm}} 조직 및 사용자 간에 공유될 수 있음을 유의하십시오. 가상 머신은 IaaS 리소스의 공유 풀에서 오는 컴퓨팅, 메모리 및 I/O 리소스를 제공합니다.

공유 환경에서 가상 머신이 특정 컴퓨팅, 메모리 및 I/O 리소스를 실행하므로 서비스 구성이 다를 수 있습니다. 각각의 특정 서비스 인스턴스의 구성은 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 서비스 대시보드 및 포털을 통해 볼 수 있습니다.

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}는 가상 머신 인스턴스를 제공합니다. 이러한 인스턴스로 클라이언트는 단순 포털을 사용하여 애플리케이션 조정에 중요한 유연성이 있으며 일관성 있고 반복 가능한 방식으로 엔터프라이즈 WebSphere Application Server 배치를 작성하고 관리합니다. 사용자는 호스팅된 클라우드 환경에서 사전 구성된 WebSphere Application Server Liberty, ND 또는 Traditional 가상 머신에서 시작해서 실행할 수 있습니다. 사용자는 기존 WebSphere Application Server 애플리케이션을 {{site.data.keyword.Bluemix_notm}}로 마이그레이션하고 기본 OS 및 미들웨어의 전체 제어를 수행할 수 있습니다.

## 가상 머신 크기 조정
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}는 대형 가상 머신을 프로비저닝하여 메모리 집약적인 애플리케이션에 적정 크기의 환경을 제공할 수 있도록 티셔츠 크기 조정을 제공합니다. WebSphere Application Server를 실행하기 위해 프로비저닝하는 각 가상 머신의 크기를 예상되는 리소스 요구에 맞게 독립적으로 조정할 수 있습니다.

가상 머신 크기를 조정하고 *블록 수*에 따라 가격을 책정합니다. 티셔츠 크기의 각 블록에 대해 가상 머신은 다음 리소스로 프로비저닝됩니다.
* 가상 CPU(vCPU) 1개
* 2GB RAM
* 하드 드라이브 공간 12.5GB(단일 블록 VM의 경우 12.0GB)


| 티셔츠 | 블록 수 | vCPU | RAM(GB) | HD(GB) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
|S |1 |1 |2 |12 |
|M |2 |2 |4 |25 |
|L |4 |4 |8 |50 |
|XL |8 |8 |16 |100 |
|XXL |16 |16 |32 |200 |
{: caption="표1. 티셔츠 크기당 블록 수" caption-side="top"}

각 서버나 노드가 단일 가상 머신에 프로비저닝됩니다. 예를 들어 Network Deployment 플랜에서 애플리케이션 노드의 배치 관리자 및 8개의 S 가상 머신(블록 1개)에 대해 하나의 M 가상 머신(블록 2개)을 프로비저닝하는 경우 총 10개의 블록에 대해 요금이 부과됩니다.

## 비용 청구 옵션
{: #billing-options}

선택한 비용 청구 옵션에 따른 각 블록의 가격:
* **[종량과금제](#pay-as-you-go):** 사용량 기반 청구, 사용한 블록당 시간당 가격
* **[예비 계약](#reserve-contract):** 예약된 리소스에 대한 선불 월별 구독

### 종량과금제
{: #pay-as-you-go}

종량과금제 가격은 IBM 영업 담당자에게 다른 비용 청구 옵션을 문의하지 않고 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 서비스를 프로비저닝하는 경우에 적용됩니다. 사용량은 월 청구 기간 동안 각 블록이 사용된 전체 또는 부분 시간에 대해 요금이 부과됩니다. 최소 비용 청구는 한 블록 시간의 1/4로 설정됩니다.

**참고**: 특정 양의 컴퓨팅, 메모리 및 입출력 리소스로 인해 중지된 인스턴스의 요금은 5% 감소된 시간당 블록 비율로 부과됩니다. 서비스 내에서 중지된 인스턴스는 10개의 IP 주소 또는 64GB의 메모리로 제한됩니다.

#### 플랜 가격

블록당 가격은 선택한 WebSphere Application Server 플랜에 따라 다릅니다.

다음 표에서는 각 티셔츠 크기 조정된 가상 머신에 대한 시간당 총 가격을 나열합니다. 이 가격은 2016년 4월 1일 기준으로 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 플랜을 표시하며 US 달러(USD)로 나열됩니다. 사용자 지역의 현재 가격은 카탈로그를 참조하십시오.

| 티셔츠 | 블록 수 | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
|S |1 |$0.21 |$0.30 |$0.70 |
|M |2 |$0.42 |$0.60 |$1.40 |
|L |4 |$0.84 |$1.20 |$2.80 |
|XL |8 |$1.68 |$2.40 |$5.60 |
|XXL |16 |$3.36 |$4.80 |$11.20 |
{: caption="표 2. Liberty Core 플랜" caption-side="top"}


### 예비 계약
{:#reserve-contract}

예비 계약 비용 청구를 사용하는 경우 물리적으로 예약된 컴퓨팅 리소스 블록에 액세스하도록 보장하는 선불 월별 구독을 구매합니다. 이러한 서비스 블록은 독점 사용을 위해 따로 설정되고 다른 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 사용자가 사용할 수 있는 용량으로 인식되지 않습니다. 기존 WebSphere Application Server 라이센스가 있는 경우 BYOL(Bring-Your-Own-License) 예비 계약을 선택할 수 있습니다. 이 경우 이 라이센스를 사용하고 청구 비용이 줄어듭니다. 서비스 계약 비용 청구를 설정하려면 [IBM 영업 담당자에게 문의](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)하십시오.

구독은 8블록 단위로 사용할 수 있습니다. 총 블록 시간은 해당 월의 시간을 기반으로 하지만 월중 어느 때라도 블록 시간을 사용할 수 있습니다. 예를 들어, 총 일 수가 30일인 달은 720시간이며, 8블록 구독으로 곱했을 때 총 블록 시간은 5,760시간입니다.

  ```
30 days * 24 hours per day * 8 blocks = 5,760 block hours
  ```

블록을 사용하는 방법과 시기를 조정하여 블록 4개 사용, 블록 12개로 증가한 다음 블록 8개로 감소하는 등 가변적인 워크로드 요구사항을 충족시킬 수 있습니다. 해당 월의 총 블록 시간 내에서 사용하는 한 추가 요금은 부과되지 않습니다.

예비 계약 블록을 사용할 것인지, 또는 각 환경을 프로비저닝할 때 종량과금제 청구를 사용할 것인지 여부를 선택할 수 있습니다.

**참고:** 서비스 인스턴스를 삭제하는 경우 새 서비스 인스턴스를 사용하려면 해당 블록에서 30분을 기다려야 할 수도 있습니다.

#### 초과분

사용량이 구독에서 설정한 월별 블록 시간을 초과하는 경우 종량과금제 비용 청구 모델에 따라 초과분에 요금에 부과되므로 사용한 추가 블록 시간에 대해서만 요금이 부과됩니다. 블록 사용량은 전체 또는 부분 시간제로 측정되며, 최소 사용량은 한 블록 시간의 1/4입니다.

종량과금제 모델의 블록은 예약된 용량이 아니며 공통 리소스 풀에서 옵니다.

#### 유연한 사용을 위한 비례 배분 비율

예비 계약 비용 청구의 블록은 WebSphere Application Server Network Deployment 플랜을 기반으로 하지만 다른 플랜에 대한 블록을 사용할 수도 있습니다. 다른 플랜을 사용하는 경우 사용량이 나머지 예비 계약 블록 시간에 영향을 주는 경우 사용량은 비례 배분되어 한 블록 시간이 플랜의 비례 배분 비율에 따라 감소됩니다.

다음 표에서는 각 플랜의 비례 배분 비율과 비례 배분이 계산된 후 실제 블록 시간당 유효 가격을 보여줍니다. 사용자 지역의 현재 가격은 [IBM 영업 담당자에게 문의](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)하십시오.

| 플랜 | 비례 배분 비율 | 비례 배분 후 가격/시간 |
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0.3 |$0.21 |
| WebSphere Application Server Base  | 0.43 |$0.30 |
| WebSphere Application Server Network Deployment | 1.0 |$0.70 |
{: caption="표 3. 플랜별 블록 시간 비례 배분 비율" caption-side="top"}

예를 들어 51시간 동안 실행되는 M(2블록) WebSphere Application Server Base 인스턴스를 사용할 수 있습니다. 예비 계약에서 사용되는 블록 시간을 계산하려면 실제 블록 시간을 비례 배분 비율로 곱합니다. 그러면 총 블록 시간은 43.86입니다.

```
2 blocks * 51 hours * 0.43 proration = 43.86 prorated block hours
```

총 비용은 동일하게 유지되지만 예비 계약 블록 시간에서 차감되는 시간이 더 적기 때문에 비례 배분된 플랜의 실제 블록 시간을 더 많이 사용할 수 있습니다.
{:.tip}
