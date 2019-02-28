---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Installationskonventionen
{: #installation_conventions}

## Verwaltungstipps
{: admin_tips}

Wenn Sie bei der Verwaltung Ihrer {{site.data.keyword.appserver_full}}-Umgebung bestimmen müssen, welcher Benutzer verwendet werden soll, sind die folgenden Konzepte von zentraler Bedeutung:

 * Für die Wartung kann das Tool [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} verwendet werden, das im Verzeichnis `/home/virtuser/IBM/Installation Manager` installiert ist. Da die Installation der zugrunde liegenden Binärdateien als `virtuser` ausgeführt wird, d. h. als virtueller Benutzer mit begrenzter Administratorberechtigung, müssen Sie sicherstellen, dass die Installation aller Fixpacks und vorläufigen Fixes als `virtuser` ausgeführt wird.

 * Für das Starten und Stoppen von Servern über die Befehlszeile muss jedoch die WebSphere-Administrator-ID `wsadmin` verwendet werden, nicht `virtuser`.

## Konventionen bei der Installation von Zellen
{: cell_installation_conventions}

Eine Zelle von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} wird mit einer standardisierten Verzeichnisstruktur installiert und konfiguriert. Die folgende Liste enthält die wichtigsten Einstellungen.  Eine vollständige Liste der Einstellungen finden Sie in der Datei `/etc/virtualimage.properties`.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Konventionen bei der Installation von Liberty-Verbünden

Ein Liberty-Verbund wird unter Verwendung einer standardisierten Verzeichnisstruktur installiert und konfiguriert. Die folgende Liste enthält die wichtigsten Einstellungen.  Eine vollständige Liste der Einstellungen finden Sie in der Datei `/etc/virtualimage.properties`.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
