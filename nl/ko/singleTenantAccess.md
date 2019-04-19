---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

keywords: single tenant, access, catalog, create service, block, pricing, vpn, openvpn

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Single Tenant Environment 액세스
{: #singleTenantEnvironment}


다음 단계에서는 서비스 인스턴스 작성 방법과 함께 Single Tenant Environment에 액세스하는 방법을 설명합니다.
{: shortdesc}


## Single Tenant Environment 액세스
{: #accessSTE}

1. 브라우저에서 [{{site.data.keyword.cloud_notm}} 카탈로그](https://{DomainName}/catalog/){: new_window}로 이동하십시오.

2. **로그인**을 클릭하고 IBM ID로 로그인하십시오.

6. 카탈로그 검색 필터에 **WebSphere Application Server**를 입력하십시오.

    ![검색 필터](images/filter.png)

7. **애플리케이션 서비스**에서 **WebSphere Application Server** 타일을 클릭하십시오.

    ![WebSphere Application Server 타일](images/iconWAS.png)

8. **환경** 메뉴에서 Single Tenant Environment를 선택하십시오.

    ![Single Tenant Environment 이름](images/environmentSTE.png)

    **문제 예방:** 기본적으로 공용 환경이 표시될 수 있습니다. 올바른 환경 이름이 표시되면 사용자가 올바른 지역에 로그인했으며 Single Tenant Environment에 액세스가 허용된 조직의 구성원임을 알 수 있습니다.

    **참고:** 공용 환경 중 하나를 선택하면 시간당 요금이 부과될 수 있습니다. 따라서 Single Tenant Environment 이름이 표시되지 않으면 [도움 받기](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#reporting_issues){: new_window} 페이지에 설명된 대로 지원 티켓을 여십시오.

9. 적절한 플랜을 선택하고 **작성**을 클릭하십시오.

    ![플랜 선택 및 서비스 작성](images/createSTE.png)


**참고:** 시간당 가격은 Single Tenant Environment에 적용되지 않습니다. Single Tenant Environment에는 할당량이라는 고정된 수의 **블록**이 포함됩니다. 소형 환경에는 64개의 블록이 포함됩니다. 중형 환경에는 128개 블록이 포함되고 대형 환경에는 256개의 블록이 포함됩니다.

**블록**은 다음과 같이 정의됩니다.
  * 1 vCPU
  * 12.5GB 디스크[1]
  * 2GB RAM

[1] *기술적으로 소형 시스템에는 12GB의 디스크만 포함됩니다. 중형 시스템에는 25GB의 디스크가 포함되며 대형 시스템에는 50GB가 포함됩니다.*

작성한 각 가상 머신에 대해 원하는 티셔츠 크기를 S, M, L, XL 또는 XXL로 지정하십시오. 이는 1, 2, 4, 8 및 16개의 블록에 해당됩니다. 티셔츠 크기를 선택하면 해당 블록 수가 할당량에서 차감됩니다.

예를 들어 64개 블록이 포함된 소형 환경이 있다고 가정합니다. 이 환경에서 XXL 2개, XL 3개 및 L 1개가 포함된 사용 블록이 총 60개인 서비스 인스턴스를 구성했습니다. 새 Liberty Core 구독에 대해 중형 티셔츠 크기를 선택한 경우 할당량과 여전히 사용 가능한 블록 수를 나타내는 메시지가 표시됩니다.

> **이 서비스의 싱글 테넌트 메모리 할당량은 블록 64개입니다. 현재 구성을 포함하여 블록 2개가 남아 있습니다. 메모리 할당량을 늘리려면 IBM 영업 담당자에게 문의하십시오.**


## 사설 네트워크 환경
{: #private_network}

Single Tenant Environment가 프로비저닝된 후 VPN 인증 정보를 다운로드하고 OpenVPN 연결을 설정할 수 있습니다. 자세한 정보는 다음 링크를 참조하십시오.

* [VPN 액세스](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#vpnAccess){: new_window}
* [OpenVPN 설정](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#setup_openvpn){: new_window}

## Single Tenant Environment 관리
{: #manageSTE}

기존 Single Tenant Environment에 추가 용량을 추가하거나 다른 데이터 센터에서 용량을 주문하려면 미국 콜 센터, 지역 IBM 담당자 또는 IBM 비즈니스 파트너에게 문의하십시오. 세부사항은 [영업 담당자에게 문의](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)를 참조하십시오.
