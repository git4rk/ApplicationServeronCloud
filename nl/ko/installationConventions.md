---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 설치 규칙
{: #installation_conventions}

## 관리 팁
{: admin_tips}

{{site.data.keyword.appserver_full}} 환경을 관리하고 사용할 사용자를 판별해야 하는 경우 다음 개념을 이해하는 것이 중요합니다.

 * */home/virtuser/IBM/Installation Manager* 디렉토리에 설치된
[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window}를 사용하여 유지보수를 적용할 수 있습니다. 기본 바이너리가 제한된 관리 가상 사용자인 **virtuser**로 설치되므로 모든 수정팩과 임시 수정사항이 **virtuser**로 설치됩니다.

 * 그러나 명령행에서 서버를 시작하고 중지할 때는 **virtuser**가 아닌 WebSphere Administrative ID인 **wsadmin**을 사용해야 합니다. 

## 셀 설치 규칙
{: cell_installation_conventions}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 셀은 표준화된 디렉토리 구조에 따라 설치되고 구성됩니다. 다음 목록은 몇 가지 중요한 설정을 표시합니다.  설정의 전체 목록은 /etc/virtualimage.properties를 참조하십시오.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Liberty Collective 설치 규칙

표준화된 디렉토리 구조에 따라 Liberty Collective가 설치되어 구성됩니다. 다음 목록은 몇 가지 중요한 설정을 표시합니다.  설정의 전체 목록은 /etc/virtualimage.properties를 참조하십시오.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
