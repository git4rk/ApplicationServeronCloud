---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 네트워크 환경
{: #networkEnvironment}

{{site.data.keyword.appserver_full}} 서비스 인스턴스가 프로비저닝되면 다양한 방법으로 VM에 액세스할 수 있습니다. 보안 VPN을 통해 사용자의 VM에 대한 SSH, Traditional WebSphere Admin Console 및 애플리케이션 액세스를 확보할 수 있습니다. 공인 IP 주소로 VM을 인터넷에 연결할 수도 있습니다.

다음 다이어그램에 해당 네트워크 경로가 표시됩니다.

그림 1. 공인 IP로 네트워킹하는 멀티 테넌트의 클라이언트 보기

![그림 1. 공인 IP가 있는 멀티 테넌트 네트워킹의 클라이언트 보기](images/wasaas_multi_tenant_publicIP.png)

## VPN 액세스
{: #vpnAccess}

{{site.data.keyword.Bluemix_notm}} UI의 서비스 대시보드에서 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 서비스 인스턴스를 프로비저닝한 후 OpenVPN 연결을 설정할 수 있습니다. 연결을 작성하려면 드롭 다운 메뉴를 펼치고 **VPN 구성 다운로드**를 클릭하여 VPN 구성을 다운로드하십시오. VPN 구성에는 `.ovpn` 파일 및 OpenVPN 서버에 인증하는 데 사용되는 인증서가 포함되어 있습니다. OpenVPN 연결이 설정되면 SSH를 통해 VM에 액세스할 수 있습니다. 또한, Liberty Admin Center, Traditional WebSphere Admin Console 및 애플리케이션에 액세스할 수 있습니다.

VPN 구성의 범위를 사용자 조직과 지역으로 지정합니다. 작성된 때부터 1년 동안 유효합니다. 동일한 VPN 구성을 사용하여 다중 OpenVPN 클라이언트 연결을 동시에 설정할 수 있습니다.

**참고:** VPN 구성은 조직에 **활성** 구독이 포함된 경우에만 유효합니다. 조직의 마지막 구독이 삭제되면 조직에 대한 모든 VPN 구성이 일시중단됩니다. 새 구독이 활성화되면 만료되지 않은 VPN 구성이 자동으로 다시 활성화됩니다.

## 고급 VPN 구성 관리
{: #advancedVPN}

대부분의 경우 **VPN 구성 다운로드** 단추를 사용하여 다운로드할 수 있는 단일 VPN 구성만 필요합니다. 그러나 서비스 대시보드에서 **고급 VPN 관리**를 클릭하여 액세스하는 고급 VPN 관리 페이지에서 여러 VPN 구성을 작성하고 관리할 수 있습니다. 구성이 여러 개인 경우 이전의 한 VPN 구성이 거의 만료될 때 새 구성으로 원활하게 전환하는 데 도움이 될 수 있습니다. 사용자 조직에서 서로 다른 개인이나 팀 단위로 VM에 대한 액세스를 관리하도록 여러 VPN 구성을 요청할 수도 있습니다.  

**참고:** 조직에 대해 언제든 **최대** 10개의 활성 VPN 구성이 허용됩니다.

VPN 구성이 손상되거나 만료된 경우 고급 VPN 관리 페이지에서 VPN 구성을 취소할 수 있습니다. 또한 감사 퍼스펙티브에서는 모든 VPN 관리 활동의 히스토리를 보고 고급 VPN 관리 페이지에서 이전에 작성된 활성 VPN 구성을 다운로드할 수 있습니다.

{{site.data.keyword.Bluemix_notm}} UI의 서비스 대시보드에서 사용 가능한 모든 기능은 REST API를 사용하여 스크립트화할 수도 있습니다. 자세한 정보는 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API 문서](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window}를 참조하십시오.


## 공용 인터넷 액세스
{: #publicInternetAccess}

선택적으로 {{site.data.keyword.Bluemix_notm}} UI의 서비스 대시보드에서 공용 인터넷 액세스를 관리할 수 있습니다. 풀에서 공인 IP 주소를 **요청**하고 인터넷에서 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 서비스 인스턴스로의 연결을 **열** 수 있습니다. 반대로 서비스 인스턴스에서 인터넷으로의 액세스를 **닫고** 공인 IP 주소를 풀로 **리턴**할 수 있습니다.

### 공인 IP 주소를 요청하고 연결 열기
{: #request-open-ip}

1. {{site.data.keyword.Bluemix_notm}} 콘솔의 서비스 대시보드에서 **공인 IP 액세스 관리**를 클릭하십시오.
2. 호스트의 IP 주소가 표시되지만 이는 공인 IP 주소가 아닙니다. **공인 IP 주소 요청**을 클릭하십시오.

    서비스 대시보드로 돌아가고 공인 IP가 지정됩니다. 그러나 다음 메시지가 표시됩니다.

    > _현재 액세스가 닫혀 있습니다. 공인 IP 관리를 클릭하여 액세스를 여십시오._
3. 서비스 대시보드에서 **공인 IP 액세스 관리**를 클릭하십시오.
4. 호스트의 IP 주소와 새 공인 IP가 표시되지만 액세스는 닫힙니다. **액세스 열기**를 클릭하십시오.

    서비스 대시보드로 돌아가고 다음 메시지가 표시됩니다.

    > _현재 액세스가 열려 있습니다. 공인 IP 관리를 클릭하여 액세스를 닫으십시오._

### 연결을 닫고 공인 IP 주소 리턴
{: #close-return-ip}

1. 서비스 대시보드에서 **공인 IP 액세스 관리**를 클릭하십시오.
2. **액세스 닫기**를 클릭하십시오.

    서비스 대시보드로 돌아가고 다음 메시지가 표시됩니다.

    > _현재 액세스가 닫혀 있습니다. 공인 IP 관리를 클릭하여 액세스를 여십시오._
3. {{site.data.keyword.Bluemix_notm}} UI의 서비스 대시보드에서 **공인 IP 액세스 관리**를 클릭하십시오.
4. **공인 IP 주소 리턴**을 클릭하십시오.

    호스트의 IP 주소와 다음 메시지가 표시된 서비스 대시보드로 돌아갑니다.

    > _공인 IP가 리턴됨._

## 공인 IP 포트
{: #publicIPports}

공인 IP에 대한 액세스를 열 때는 IP 주소가 사용자의 VM과 연관되며 포트 80 및 443이 게이트웨이에서 열립니다. 그러나 기본적으로 Liberty Core 및 Traditional WebSphere 기본 서버는 포트 80 및 443을 열지 않습니다. 반대로 포트 80 및 443이 IBM HTTP Server에서 기본적으로 열립니다. 따라서 공인 IP를 사용할 때는 Liberty Core 및 Traditional WebSphere 기본 서버가 포트 80 및 443에서 애플리케이션 트래픽을 청취하도록 구성해야 할 수 있습니다.
* Liberty Core 서버를 구성하려면 [공인 액세스용으로 Liberty Core 서버 구성](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#configureLibertyForPublicAccess)을 참조하십시오.
* Traditional WebSphere 기본 서버를 구성하려면 [전송 체인 구성](http://www.ibm.com/support/knowledgecenter/SSEQTP_9.0.0/com.ibm.websphere.base.doc/ae/trun_chain_transport.html){: new_window}에 설명된 대로 포트 80 및 443에서 청취하는 웹 컨테이너 전송 체인을 추가하십시오.

**문제 예방:** Linux는 **root**와 같은 권한 있는 사용자를 위해 1024보다 작은 포트를 예약합니다. 그러나 일반적으로 Traditional WebSphere Base 서버를 **non-root** 사용자로 실행합니다. 그러나 웹 컨테이너 전송 체인을 추가하는 경우 **iptables** 구성을 **root** 사용자로 변경하십시오. 특히 제한된 포트 80 및 443을 1024보다 큰 다른 포트(예: 9080 및 9443)로 경로 재지정하십시오. 다음 명령은 이 프로세스의 예제를 제공합니다.

```
-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 9080
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9080 -j ACCEPT

-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 9443
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
```

**참고:** **iptables**에 대한 변경사항은 유효 기간이 짧습니다. 예를 들어 게스트가 다시 부팅되거나 **iptables** 서비스가 다시 시작되는 경우 규칙은 자동으로 비워지고 재설정됩니다. iptables 서비스가 시작되거나 게스트가 다시 부팅될 때 규칙이 지속되도록 하기 위해 규칙을 저장하려면 **root** 사용자로 다음 명령을 사용하십시오.

```
-bash-4.1# service iptables save
iptables: Saving firewall rules to /etc/sysconfig/iptables:[  OK  ]

bash-4.1# cat /etc/sysconfig/iptables
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*nat
:PREROUTING ACCEPT [0:0]
:POSTROUTING ACCEPT [23:1706]
:OUTPUT ACCEPT [23:1706]
-A PREROUTING -p tcp -m tcp --dport 80 -j REDIRECT --to-ports 9080
-A PREROUTING -p tcp -m tcp --dport 443 -j REDIRECT --to-ports 9443
COMMIT
# Completed on Wed May 31 19:44:11 2017
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*filter
:INPUT DROP [0:0]
:FORWARD DROP [0:0]
:OUTPUT DROP [0:0]
-A INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 9080 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 80 -j ACCEPT

```


**참고:** 게스트의 외부 인터페이스를 통해 이동하는 요청에 대해 **iptables**가 호출됩니다. 로컬 루프백(127.0.0.1)을 통해 이동하는 요청은 **iptables**에 의해 처리되지 않으므로 앞서 언급했듯이 포트 경로 재지정은 루프백을 통해 호출되지 않습니다.

## VPN 사설 IP 포트
{: #privateIPports}

VPN 연결을 통해 VM의 사설 IP 주소에 연결합니다. Liberty Admin Center(9080, 9443), Traditional WebSphere Admin Console(9060, 9043), SSH(22) 및 80/443 이외의 포트만 그림 1에 표현된 대로 VPN 연결을 통해 액세스 가능합니다. 애플리케이션 포트에서 Liberty Admin Center 분리하기에 대한 세부사항은 샘플 Liberty Core **server.xml** 및 **ibm-web-bnd.xml**을 참조하십시오.

**문제 예방:** Liberty Core 및 Traditional WebSphere Base 서버의 경우, VM이 프로비저닝될 때 방화벽 포트가 사전 구성됩니다. 그러나 배치 관리자 또는 Collective Controller가 IBM HTTP Server와 함께 배치된 Network Deployment 구성의 경우, 방화벽에 포트를 열어야 할 수 있습니다. 세부사항은 [방화벽 포트](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#firewall_ports)를 참조하십시오.

## 공인 IP 액세스용으로 Liberty Core 서버 구성
{: #configureLibertyForPublicAccess}

공인 IP를 사용할 때는 Liberty Core가 포트 80 및 443에서 애플리케이션 트래픽을 청취하도록 구성해야 합니다.

기본적으로 Liberty는 Liberty Admin Center 및 **default_host** 가상 호스트에서 사용 가능한 애플리케이션과 함께 구성되며, 포트 9080 및 9443의 **defaultHttpEndpoint**와 연관되어 있습니다. 애플리케이션 가상 호스트 및 엔드포인트에서 Liberty Admin Center를 분리하도록 서버를 다시 구성하여 별도의 포트에서 사용 가능하게 하십시오.

다음 스니펫은 server.xml 구성 조정의 예입니다.

```    
    <!-- open port 9080/9443 for incoming http connections -->
    <httpEndpoint id="defaultHttpEndpoint"
        host="*"
        httpPort="9080"
        httpsPort="9443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!-- define a new endpoint for public app traffic -->
    <httpEndpoint id="publicHttpEndpoint"
        host="*"
        httpPort="80"
        httpsPort="443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!–- restrict default_host to vpn so the Liberty Admin Center is not public -->
    <virtualHost id="default_host" allowFromEndpointRef="defaultHttpEndpoint">
      <hostAlias>*:9080</hostAlias>
      <hostAlias>*:9443</hostAlias>
    </virtualHost>

    <virtualHost id="external_host">
      <hostAlias>*:80</hostAlias>
      <hostAlias>*:443</hostAlias>
    </virtualHost>
```
{: codeblock}

이제 애플리케이션의 `WEB-INF/ibm-web-bnd.xml` 파일에 다음 스니펫을 포함시켜 애플리케이션을 `external_host` 가상 호스트와 연관시키십시오.

```
    <?xml version="1.0" encoding="UTF-8"?>
    <web-bnd
        xmlns="http://websphere.ibm.com/xml/ns/javaee"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://websphere.ibm.com/xml/ns/javaee   
        http://websphere.ibm.com/xml/ns/javaee/ibm-web-bnd_1_0.xsd"
        version="1.0">

        <virtual-host name="external_host" />
    </web-bnd>
```
{: codeblock}

## DNS 구성
{: #dnsConfig}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM은 두 개의 DNS 분석기를 사용하여 구성된다는 것을 유의해야 합니다. 분석기는 VM의 **/etc/resolv.conf** 파일에 구성됩니다. 기본 DNS 서버는 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 서비스에서 제공되는 권한 없는 서버입니다. 보조 DNS 서버는 {{site.data.keyword.Bluemix_notm}}에서 제공되는 권한 없는 서버입니다.

DNS 구성을 검토하여 사용자 요구사항에 맞는지 확인하는 것이 좋습니다. IBM에서 제공한 항목이 사용자 요구사항을 충족하지 않는 경우 사용자가 선택한 DNS 서버를 참조하도록 `/etc/resolv.conf` 파일을 업데이트할 수 있습니다.

**참고:** 이전 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM에서는 `/etc/resolv.conf` 파일에 기본 DNS 서버만 구성할 수 있었습니다. HA 솔루션을 원하는 경우 VM을 해제하고 새 VM을 프로비저닝하거나 `/etc/resolv.conf` 파일을 업데이트하여 보조 DNS 서버를 추가할 수 있습니다. 보조 DNS 서버는 선호하는 DNS 서버이거나 {{site.data.keyword.Bluemix_notm}}(10.0.80.11)에서 제공하는 DNS 서버일 수 있습니다.


## 사용자 정의 노드에서 새 서버에 대한 포트 열기
{: #serversOnCustom}

사용자 정의 노드에서 서버를 작성하는 경우 서버를 시작하기 전에 서버에 필요한 추가 포트가 배치 관리자 또는 사용자 정의 노드 VM에 열려 있어야 합니다. 서버를 작성한 후 서버를 시작하기 전에 `openWASPorts.sh` 스크립트를 실행하여 포트를 여십시오.

 1. 루트 사용자로 각 배치 관리자 및 사용자 정의 VM에 로그인하십시오.
 1. `/opt/IBM/WebSphere/AppServer/virtual/bin/openWASPorts.sh` 스크립트를 실행하여 포트를 여십시오.

스크립트를 실행한 후에 배치 관리자 도메인 콘솔에서 서버를 시작할 수 있습니다.
