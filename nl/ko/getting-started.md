---

copyright:
  years: 2018
lastupdated: "2018-09-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# 시작하기 튜토리얼
{:#getting-started}

{{site.data.keyword.appserver_full}}를 사용하여 사전 구성된 WebSphere Application Server Traditional 또는 Liberty 환경을 수 분 내로 설정할 수 있습니다. 이 시작하기 튜토리얼은 단 몇 단계만으로 WebSphere Application Server 환경을 가상 머신에 프로비저닝하는 과정을 안내합니다.
{: shortdesc}

## 시작하기 전에
{: #prereqs}

예비 계약 또는 Single Tenant Environment와 같은 더 많은 전용 가상 머신 리소스가 있는 환경을 원하는 경우 서비스를 작성하기 전에 IBM 영업 담당자에게 문의해야 합니다. [정보](index.html)에서 이러한 옵션을 자세히 알아보십시오.

### 기존 WebSphere 환경 마이그레이션

기존 WebSphere Application Server Network Deployment 환경을 이 서비스로 마이그레이션하려면 [{{site.data.keyword.cloud_notm}}용 WebSphere 구성 마이그레이션 도구 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window}를 사용하십시오. 도구는 {{site.data.keyword.cloud_notm}}의 서비스 인스턴스로 독립형 서버 또는 셀 노드에 대한 프로파일 구성 및 애플리케이션을 업로드합니다. 도구를 사용하는 방법에 대한 단계별 안내와 클라우드 마이그레이션에 대한 개요는 WASdev에서 [IBM Cloud용 WebSphere 구성 마이그레이션 도구 안내서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window}를 참조하십시오.

다음 단계에서는 {{site.data.keyword.appserver_full}}에서 새 환경을 작성하는 과정을 안내합니다.

## 1단계: 서비스 작성
{: #create}

1. {{site.data.keyword.cloud_notm}} 카탈로그의 [{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) 페이지로 이동하십시오.
1. IBM ID로 로그인하거나 {{site.data.keyword.cloud_notm}} 계정으로 로그인하십시오.
1. 카탈로그 페이지에서 서비스 구성에 대한 선택사항을 검토하십시오.

  종량과금제 환경에서는 기본 선택사항을 사용하거나 사용자 요구에 맞게 선택사항을 수정하십시오.

  예비 계약 또는 Single Tenant Environment가 있는 경우 다음 옵션에 주의하십시오.

  * **예비 계약:** **배치할 지역/위치 선택**에서 선택한 지역이 사용자 계약에 맞는 지역인지 확인하십시오.

  * **Single Tenant Environment:** **배치할 지역/위치 선택**에서 선택한 지역이 Single Tenant Environment가 배치되는 지역인지 확인하십시오. **환경**에서 Single Tenant Environment를 선택하십시오. 기본적으로 공용 환경이 표시될 수 있습니다.

    Single Tenant Environment가 나열되지 않으면 사용자가 올바른 지역에 있는지와 사용자 조직이 Single Tenant Environment에 액세스할 수 있는지 확인하십시오.
    {: tip}
1. 배치할 {{site.data.keyword.appserver_short}} 에디션에 대한 가격 플랜을 선택하십시오.
1. **작성**을 클릭하십시오.


## 2단계: 환경 선택(Network Deployment만 해당)
{: #choose_env}

{{site.data.keyword.appserver_short}} Base 및 Liberty Core 플랜에는 단일 서버만 있으므로 해당 플랜을 선택한 경우 이 단계를 건너뛸 수 있습니다.

Network Deployment 플랜의 경우 사용자 환경의 프로파일과 아키텍처를 선택하십시오.

* **프로파일:** {{site.data.keyword.appserver_short}} Traditional 또는 Liberty 선택
* **아키텍처:** Traditional 셀 또는 Liberty Collective가 있는 단일 서버 환경 또는 클러스터 환경 선택


## 3단계: 가상 머신 크기 조정
{: #vm_sizing}

환경의 각 컴포넌트에 대한 가상 머신의 크기를 개별적으로 조정할 수 있습니다. 가상 머신 크기 조정은 [티셔츠 크기](index.html#vm-size)의 리소스 블록으로 분할됩니다.

서버, 배치 관리자 또는 애플리케이션 노드와 같은 컴포넌트의 탭을 클릭하고 가상 머신의 티셔츠 크기를 선택하십시오.

## 4단계: 환경 프로비저닝
{: #service_profile}

서비스 구성 요약에서 프로비저닝하는 데 걸리는 예상 시간 등의 세부사항을 검토하십시오.

**예비 계약:** **청구** 옵션이 _예비 계약_으로 설정되었는지 확인하십시오. 옵션이 나타나지 않으면 [사용자 조직](../../account/orgs_spaces.html){:new_window}이 계약의 조직 이름과 대소문자 및 공백을 포함하여 정확히 동일한지 확인하십시오. 예비 계약 청구를 선택하지 않고 서비스를 프로비저닝하는 경우 종량과금제 청구를 사용합니다.

**프로비저닝**을 클릭하여 {{site.data.keyword.appserver_short}} 환경을 설정하십시오.

## 다음 단계
{: #anchor_value}

[시스템 액세스](systemAccess.html)에서 새 {{site.data.keyword.appserver_short}} 환경에 액세스하고 환경을 관리하는 방법에 대해 알아봅니다.
