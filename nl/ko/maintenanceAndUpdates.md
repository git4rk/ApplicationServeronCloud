---

copyright:
  years: 2017, 2018
lastupdated: "2018-08-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 환경 업데이트
{: #updating-your-environment}

## 유지보수 전략
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}}는 현재 수정팩과 패치로 새 서비스 인스턴스를 작성할 수 있도록 주기적으로 업데이트됩니다. 미들웨어 관리 시 클라우드를 통해 새 서비스 인스턴스를 쉽고 빠르게 프로비저닝할 수 있습니다.

특정 제품 버전에서는 현재 또는 이전 수정팩 레벨(n 또는 n-1)로 {{site.data.keyword.Bluemix_notm}} 인스턴스에 WebSphere Application Server를 작성할 수 있습니다. 현재 수정팩을 사용하면 최신 업데이트와 기능을 제공하지만 이전 수정팩을 사용하는 경우 하이브리드 클라우드 배치 요구사항을 준수해야 할 수 있습니다.

새 인스턴스를 작성할 때 서비스 인스턴스의 **서비스 프로파일** 탭에서 다음 수정팩 레벨을 선택할 수 있습니다.

**Liberty**
  * 18.0.0.2
  * 18.0.0.1

**WebSphere Application Server Traditional**
  * 9.0.0.8
  * 9.0.0.7
  * 8.5.5.14
  * 8.5.5.13

## 수정사항 및 수정팩 업데이트 적용
{:#applying-fixes}

최신 유지보수 레벨로 업데이트하는 가장 빠른 방법은 새 인스턴스를 작성하는 것입니다. 그러나 장기간 사용된 서비스 인스턴스를 유지하려면 다음 절에서 설명된 대로 제공된 `installService.sh` 스크립트를 실행하거나 IBM Installation Manager를 사용하여 기존 설치에 유지보수를 적용할 수 있습니다.

### installService.sh 스크립트를 사용하여 업데이트

서비스 인스턴스는 사용 가능한 보안 수정사항 및 WebSphere Application Server 수정팩으로 자주 업데이트되는 Installation Manager 저장소로 구성됩니다. `/home/virtuser/installService.sh` 스크립트를 사용하여 이러한 수정사항과 수정팩을 적용할 수 있습니다. 스크립트는 루트 사용자로 실행되어야 합니다.

업데이트를 설치하는 데 필요한 디스크 공간 크기는 설치하는 업데이트 유형에 따라 다릅니다. 임시 수정사항을 설치하려면 가상 머신의 경우 1GB의 여유 공간이 필요합니다. 수정팩을 설치하는 경우 필요한 디스크 공간이 1.3GB로 늘어납니다.

스크립트를 실행하면 다음 조치를 수행합니다.

* 실행 중인 모든 WebSphere Application Server 및 IBM HTTP Server 인스턴스 중지
* 선택적으로 Installation Manager, WebSphere Application Server, IBM HTTP Server 및 Java&trade; SDK에 대한 최신 수정팩 설치
* WebSphere, IBM HTTP Server 및 Java&trade; SDK에 대한 최신 임시 수정사항 설치
* 모든 인스턴스 다시 시작

#### 옵션
* **`-fixpacks`**

    모든 패키지를 최신 수정팩으로 업데이트합니다.
* **`-noprompt`**

    업데이트하기 전에 확인 메시지를 표시하지 않습니다.

#### 구문 예제

```
./installService.sh -?
```
{:.codeblock}

도움말 텍스트를 표시합니다.


```
./installService.sh
```
{:.codeblock}

적용 가능한 모든 임시 수정사항을 설치하지만 수정팩은 설치하지 않습니다.


```
./installService.sh -fixpacks
```
{:.codeblock}

사용 가능한 모든 수정팩을 설치하고 적용 가능한 모든 임시 수정사항을 설치합니다.

### Installation Manager를 사용하여 업데이트
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window}는 `/home/virtuser/IBM/Installation Manager` 디렉토리에 설치되어 있으며 이를 직접 실행하여 수정사항과 수정팩을 적용할 수 있습니다.

**문제 예방:** 기본 바이너리 파일이 제한된 관리 가상 사용자인 `virtuser`로 설치되기 때문에 Installation Manager는 항상 `virtuser`로 실행되어야 합니다.

## 가상 머신에 시스템 업데이트 적용
{:#vm-system-updates}

가상 머신에 시스템 업데이트를 적용하는 것은 실제 RHEL(Red Hat Enterprise Linux&reg;) 시스템을 업데이트하는 것과 유사합니다. Yum 패키지 관리자를 사용하여 패키지를 설치, 업데이트, 설치 제거하고 그렇지 않은 경우 패키지를 관리할 수 있습니다. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 시스템은 IBM의 Red Hat Satellite 서버에서 업데이트를 받도록 구성되어 있습니다. 이 서버는 Red Hat 네트워크에서 안전한 패키지를 제공합니다. Satellite 서버는 IBM에서 관리하며 사용자 시스템에서 수정할 수 없습니다.

자세한 정보는 [Red Hat Enterprise Linux에서 패키지 업데이트 적용](https://access.redhat.com/articles/11258#rhel6){: new_window} 및 [Red Hat 패키지 관리자 Yum](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}을 참조하십시오.
