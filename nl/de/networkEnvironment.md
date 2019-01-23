---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Netzumgebung
{: #networkEnvironment}

Nach der Bereitstellung der {{site.data.keyword.appserver_full}}-Serviceinstanz stehen Ihnen mehrere Möglichkeiten für den Zugriff auf die virtuelle Maschine zur Verfügung. Sie können über ein sicheres VPN eine Verbindung herstellen, um über SSH, die klassische WebSphere-Administrationskonsole oder Anwendungen auf eine VM zuzugreifen+++. Außerdem kann die VM über eine öffentliche IP-Adresse mit dem Internet verbunden werden.

Im folgenden Diagramm sind die Netzpfade dargestellt:

Abbildung 1. Clientansicht des Multi-Tenant-Netzbetriebs mit öffentlicher IP-Adresse

![Abbildung 1. Clientansicht des Multi-Tenant-Netzbetriebs mit öffentlicher IP-Adresse](images/wasaas_multi_tenant_publicIP.png)

## VPN-Zugriff
{: #vpnAccess}

Nachdem Sie eine Serviceinstanz von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} über das Service-Dashboard in der {{site.data.keyword.Bluemix_notm}}-Benutzerschnittstelle bereitgestellt haben, können Sie eine OpenVPN-Verbindung einrichten. Für die Erstellung der Verbindung erweitern Sie das Dropdown-Menü und klicken auf **VPN-Konfiguration herunterladen**, um Ihre VPN-Konfiguration herunterzuladen. Die VPN-Konfiguration enthält eine `.ovpn`-Datei und Zertifikate, die für die Authentifizierung beim OpenVPN-Server verwendet werden. Nach dem Einrichten der OpenVPN-Verbindung können Sie über SSH auf Ihre virtuelle Maschine zugreifen. Darüber hinaus können Sie auf das Liberty Admin Center, die klassische WebSphere-Administrationskonsole und Anwendungen zugreifen.

Die VPN-Konfiguration wird an Ihre Organisation und Region angepasst. Sie ist vom Erstellungszeitpunkt an für einen Zeitraum von einem Jahr gültig. Mehrere OpenVPN-Clientverbindungen können gleichzeitig eingerichtet werden, indem dieselbe VPN-Konfiguration verwendet wird.

**Hinweis:** Die VPN-Konfiguration ist nur gültig, wenn Ihre Organisation **aktive** Abonnements enthält. Wenn das letzte Abonnement für eine Organisation gelöscht wird, werden alle VPN-Konfigurationen für diese Organisation ausgesetzt. Nicht abgelaufene VPN-Konfigurationen werden automatisch erneut aktiviert, sobald ein neues Abonnement aktiv wird.

## Erweiterte VPN-Konfigurationsverwaltung
{: #advancedVPN}

In den meisten Fällen benötigen Sie nur eine einzelne VPN-Konfiguration, die Sie über die Schaltfläche **VPN-Konfiguration herunterladen** herunterladen können. Auf der Seite für die erweiterte VPN-Verwaltung, auf die Sie über die Schaltfläche **Erweiterte VPN-Verwaltung** im Service-Dashboard zugreifen können, ist es jedoch möglich, mehrere VPN-Konfigurationen zu erstellen und zu verwalten. Mehrere Konfigurationen können nützlich sein, um einen reibungslosen Übergang auf eine neue VPN-Konfiguration zu ermöglichen, wenn die alte Konfiguration abläuft. Darüber hinaus können Sie mehrere VPN-Konfigurationen anfordern, um den Zugriff auf Ihre virtuellen Maschinen für mehrere Personen oder Teams in Ihrer Organisation zu verwalten.  

**Hinweis:** Es sind jeweils **maximal** 10 aktive VPN-Konfigurationen für Ihre Organisation gleichzeitig zulässig.

Wenn Ihre VPN-Konfigurationen beeinträchtigt oder abgelaufen sind, können Sie VPN-Konfigurationen über die Seite für die erweiterte VPN-Verwaltung widerrufen. Zu Auditzwecken können Sie über die Seite für die erweiterte VPN-Verwaltung auch ein Verlaufsprotokoll der gesamten VPN-Verwaltungsaktivitäten anzeigen und zuvor erstellte, aktive VPN-Konfigurationen herunterladen.

Alle Features, die über das Service-Dashboard in der {{site.data.keyword.Bluemix_notm}}-Benutzerschnittstelle verfügbar sind, können auch scriptgesteuert mit den REST-APIs ausgeführt werden. Weitere Informationen finen Sie in der {{site.data.keyword.Bluemix_notm}} [REST-API-Dokumentation](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window} zu WebSphere Application Server. 


## Zugriff auf das öffentliche Internet
{: #publicInternetAccess}

Sie können den Zugriff auf das öffentliche Internet wahlweise über das Service-Dashboard in der {{site.data.keyword.Bluemix_notm}}-Benutzerschnittstelle verwalten. Sie können eine öffentliche IP-Adresse aus dem Pool **anfordern** und die Verbindung vom Internet zu Ihrer Serviceinstanz von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} **öffnen**. Umgekehrt können Sie den Zugriff von Ihrer Serviceinstanz auf das Internet **schließen** und die öffentliche IP-Adresse an den Pool **zurückgeben**.

### Öffentliche IP-Adresse anfordern und Verbindung öffnen
{: #request-open-ip}

1. Klicken Sie auf **Zugriff auf öffentliche IP-Adresse verwalten** im Service-Dashboard in der {{site.data.keyword.Bluemix_notm}}-Konsole.
2. Die IP-Adresse für Ihren Host wird angezeigt, nicht jedoch Ihre öffentliche IP-Adresse. Klicken Sie auf **Öffentliche IP-Adresse anfordern**.

    Das Service-Dashboard wird mit einer zugewiesenen öffentlichen IP-Adresse erneut aufgerufen. Es wird jedoch die folgende Nachricht angezeigt:

    > _Zugriff aktuell geschlossen. Auf 'Zugriff auf öffentliche IP-Adresse verwalten' klicken, um den Zugriff zu öffnen._
3. Klicken Sie auf **Zugriff auf öffentliche IP-Adresse verwalten** im Service-Dashboard.
4. Die IP-Adressen für Ihren Host und die neue öffentliche IP-Adresse werden angezeigt, der Zugriff ist jedoch geschlossen. Klicken Sie auf **Zugriff öffnen**.

    Das Service-Dashboard wird erneut aufgerufen und die folgende Nachricht wird angezeigt:

    > _Zugriff aktuell geöffnet. Auf 'Zugriff auf öffentliche IP-Adresse verwalten' klicken, um den Zugriff zu schließen._

### Verbindung schließen und öffentliche IP-Adresse zurückgeben
{: #close-return-ip}

1. Klicken Sie auf **Zugriff auf öffentliche IP-Adresse verwalten** im Service-Dashboard.
2. Klicken Sie auf **Zugriff schließen**.

    Das Service-Dashboard wird erneut aufgerufen und die folgende Nachricht wird angezeigt:

    > _Zugriff aktuell geschlossen. Auf 'Zugriff auf öffentliche IP-Adresse verwalten' klicken, um den Zugriff zu öffnen._
3. Klicken Sie auf **Zugriff auf öffentliche IP-Adresse verwalten** im Service-Dashboard in der {{site.data.keyword.Bluemix_notm}}-Benutzerschnittstelle.
4. Klicken Sie auf **Öffentliche IP-Adresse zurückgeben**.

    Das Service-Dashboard wird erneut aufgerufen und die IP-Adresse Ihres Hosts wird zusammen mit der folgenden Nachricht angezeigt:

    > _Öffentliche IP-Adresse zurückgegeben._

## Öffentliche IP-Ports
{: #publicIPports}

Wenn Sie den Zugriff auf die öffentliche IP öffnen, wird die IP-Adresse der VM zugeordnet, und die Ports 80 und 443 werden am Gateway geöffnet. Die Ports 80 und 443 werden von Servern mit Liberty Core und Servern mit klassischem WebSphere Base jedoch nicht standardmäßig geöffnet. Im IBM HTTP Server werden diese Ports dagegen standardmäßig geöffnet. Deshalb müssen Sie Server mit Liberty Core und Server mit klassischem WebSphere Base bei der Verwendung einer öffentlichen IP-Adresse möglicherweise so konfigurieren, dass sie an Port 80 und 443 für Anwendungsdatenverkehr empfangsbereit sind.
* Informationen zur Konfiguration des Liberty Core-Servers finden Sie in [Liberty Core-Server für öffentlichen Zugriff konfigurieren](networkEnvironment.html#configureLibertyForPublicAccess).
* Fügen Sie zum Konfigurieren des Servers mit klassischem WebSphere Base eine Web-Container-Transportkette hinzu, die an Port 80 und 443 empfangsbereit ist. Weitere Informationen hierzu finden Sie in [Transportketten konfigurieren](http://www.ibm.com/support/knowledgecenter/SSEQTP_8.5.5//com.ibm.websphere.nd.doc/ae/trun_chain_transport.html){: new_window}.

**Probleme vermeiden:** Linux reserviert Ports mit einer Nummer unter 1024 für privilegierte Benutzer wie z. B. **root**. Es ist jedoch ein allgemein übliches Verfahren, klassische WebSphere Base-Server als **non-root**-Benutzer auszuführen. Ändern Sie daher beim Hinzufügen einer Web-Container-Transportkette die **iptables**-Konfiguration als **root**-Benutzer. Adressieren Sie speziell die eingeschränkten Ports 80 und 443 in andere Ports über 1024 um (z. B. 9080 und 9443). Die folgenden Befehle stellen ein Beispiel für diesen Prozess dar:

```
-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 9080
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9080 -j ACCEPT

-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 9443
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
```

**Hinweis:** Änderungen an **iptables** sind temporär. Beispiel: Bei einem Neustart des Gastsystems oder wenn der **iptables**-Service erneut gestartet wird, werden die Regeln automatisch gelöscht und zurückgesetzt. Wenn die Regeln so gespeichert werden sollen, dass sie beim Starten des iptables-Service oder bei einem Neustart des Gastsystems bestehen bleiben, verwenden Sie den folgenden Befehl als **root**-Benutzer:

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


**Hinweis:** **iptables** wird bei Anforderungen aufgerufen, die über die externe Schnittstelle des Gastsystems gesendet werden. Anforderungen, die über das lokale Loopback (127.0.0.1) gesendet werden, werden nicht von **iptables** verarbeitet; d. h., die oben beschriebene Umadressierung von Ports wird über Loopback nicht aufgerufen.

## VPN-Ports für private IP
{: #privateIPports}

Über die VPN-Verbindung können Sie eine Verbindung zur privaten IP-Adresse der VM herstellen. Der Zugriff auf das Liberty Admin Center (9080, 9443), die klassische WebSphere-Administrationskonsole (9060, 9043), SSH (22) und andere Ports als 80 und 443 ist nur über die VPN-Verbindung möglich (siehe Abbildung 1). Informationen dazu, wie Sie das Liberty Admin Center von den Anwendungsports trennen können, enthalten die Liberty Core-Beispieldateien **server.xml** und **ibm-web-bnd.xml**.

**Störungen vermeiden**: Im Falle von Servern mit Liberty Core und Servern mit klassischem WebSphere Base sind die Firewall-Ports bei der Bereitstellung der VM vorkonfiguriert. Bei Network Deployment-Konfigurationen, in denen der Deployment Manager oder der Verbundcontroller mit dem IBM HTTP Server kollokiert ist, müssen jedoch möglicherweise Ports an der Firewall geöffnet werden. Einzelheiten hierzu finden Sie in [Firewall-Ports](systemAccess.html#firewall_ports).

## Liberty Core-Server für Zugriff auf öffentliche IP-Adresse konfigurieren
{: #configureLibertyForPublicAccess}

Bei Verwendung einer öffentlichen IP-Adresse müssen Sie den Liberty Core-Server so konfigurieren, dass er für Anwendungsdatenverker an Port 80 und 443 empfangsbereit ist.

Liberty ist standardmäßig so konfiguriert, dass das Liberty Admin Center und die Anwendungen auf dem virtuellen Host **default_host** zur Verfügung stehen, der **defaultHttpEndpoint** an Port 9080 und 9443 zugeordnet wird. Rekonfigurieren Sie den Server, um das Liberty Admin Center vom virtuellen Host und Endpunkt der Anwendungen zu trennen und an separaten Ports verfügbar zu machen.

Das folgende Snippet ist ein Beispiel für Konfigurationsanpassungen an der Datei 'server.xml':

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

Ordnen Sie nun Ihre Anwendung dem virtuellen Host `external_host` zu, indem Sie das folgende Snippet in die Datei `WEB-INF/ibm-web-bnd.xml` der Anwendung einfügen:

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

## DNS konfigurieren
{: #dnsConfig}

Beachten Sie, dass virtuelle Maschinen von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} mit zwei DNS-Resolvern konfiguriert werden. Die Resolver werden in der Datei **/etc/resolv.conf** auf der virtuellen Maschine konfiguriert. Beim primären DNS-Server handelt es sich um einen nicht autoritativen Server, der vom WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}-Service bereitgestellt wird. Beim sekundären DNS-Server handelt es sich um einen nicht autoritativen Server, der von {{site.data.keyword.Bluemix_notm}} bereitgestellt wird.

Es wird empfohlen, die DNS-Konfiguration zu überprüfen, um festzustellen, ob sie den jeweiligen Anforderungen entspricht. Sie können die Datei `/etc/resolv.conf` so aktualisieren, dass der bevorzugte DNS-Server referenziert wird, falls die von IBM bereitgestellten DNS-Server den jeweiligen Anforderungen nicht entsprechen.

**Hinweis:** Für ältere virtuelle Maschinen von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} ist möglicherweise nur ein primärer DNS-Server in der Datei `/etc/resolv.conf` konfiguriert. Für eine Hochverfügbarkeitslösung können Sie entweder die virtuelle Maschine freigeben und eine neue bereitstellen oder die Datei `/etc/resolv.conf` so aktualisieren, dass ein sekundärer DNS-Server hinzugefügt wird. Bei dem sekundären DNS-Server kann es sich um den bevorzugten DNS-Server oder um den von {{site.data.keyword.Bluemix_notm}} bereitgestellten (10.0.80.11) handeln.


## Ports für neue Server auf angepassten Knoten öffnen
{: #serversOnCustom}

Wenn Sie einen Server auf einem angepassten Knoten erstellen, müssen die zusätzlichen Ports, die für den Server erforderlich sind, auf den virtuellen Maschinen des Deployment Managers und des angepassten Knotens geöffnet werden, bevor der Server gestartet wird. Öffnen Sie nach der Erstellung - aber vor dem Starten - des Servers die Ports, indem Sie das Script `openWASPorts.sh` ausführen.

 1. Melden Sie sich bei jeder virtuellen Maschine des Deployment Managers und des angepassten Knotens als Rootbenutzer an.
 1. Führen Sie das Script `/opt/IBM/WebSphere/AppServer/virtual/bin/openWASPorts.sh` aus, um die Ports zu öffnen.

Nach der Ausführung des Scripts können Sie den Server über die Deployment Manager-Administrationskonsole starten.
