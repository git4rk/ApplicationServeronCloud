---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 싱글 테넌트 환경
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}}: 싱글 테넌트 환경은 고객에게 격리된 WebSphere 워크로드, 완전히 통합된 하이브리드 환경 및 보안 데이터를 제공하는 오퍼링입니다. 이 시작하기 안내서는 {{site.data.keyword.Bluemix_notm}}: 싱글 테넌트 환경에서 클라이언트가 WebSphere Application Server에 액세스하고 이를 관리하는 데 도움이 되는 주요 요소를 식별하도록 설계되었습니다.
{: shortdesc}


## 권장 소프트웨어
{: #recommended_software}

싱글 테넌트 환경에 액세스하려면 다음 소프트웨어가 필요합니다.
* {{site.data.keyword.Bluemix_notm}}에서 지원하는 웹 브라우저:
    * Chrome: 사용자 운영 체제용 최신 버전
    * Firefox: 사용자 운영 체제용 최신 버전 또는 최신 ESR 버전
    * Internet Explorer: 버전 10 또는 11
    * Safari: Mac용 최신 버전
* Cloud Foundry 명령행 인터페이스, 버전 6.5.1 이상(최신 릴리스 사용 가능)
* Git Bash(권장)
    * [Git Bash](https://git-scm.com/downloads){: new_window} 다운로드 및 설치


## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: 싱글 테넌트 환경의 개요
{: #overviewSTE}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: 싱글 테넌트 오퍼링은 고객에게 고유의 개인 서비스 인스턴스, 개인 네트워킹 및 격리된 리소스를 제공합니다. 이 오퍼링은 독립적으로 관리되지만 서비스 및 작성된 서비스 인스턴스 대시보드는 다음 그림에 표시된 대로 특정 {{site.data.keyword.Bluemix_notm}} 공용 지역을 통해 액세스할 수 있습니다.

그림 1. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: 싱글 테넌트 환경의 아키텍처

![그림 1. 싱글 테넌트 환경의 아키텍처](images/WASaaS.png)


## 조직 관리
{: #organization_management}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: 싱글 테넌트 환경은 사용자 주문에 따라 구성됩니다. 하나 이상의 {{site.data.keyword.Bluemix_notm}} 조직 이름을 주문의 일부로 제공한 경우 지금 사용자 환경에 액세스할 수 있습니다. 하나 이상의 조직 이름을 제공하지 않았거나 이 설정을 변경하려는 경우 사용자 지역의 {{site.data.keyword.Bluemix_notm}} 콘솔에서 **애플리케이션 서비스**에 대한 [지원 티켓](reportingIssues.html#reporting_issues)을 여십시오. 조직 이름(ORG)은 다음 그림에 표시된 대로 {{site.data.keyword.Bluemix_notm}} 콘솔의 오른쪽 상단에 있습니다.

그림 2. 조직 이름의 위치

![그림 2. ORG 이름의 위치](images/myORG.png)


**참고:** 싱글 테넌트 환경에 액세스하려면 [싱글 테넌트 환경 액세스](singleTenantAccess.html#singleTenantEnvironment)를 참조하십시오.
