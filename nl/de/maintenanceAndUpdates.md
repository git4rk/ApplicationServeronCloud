---

copyright:
  years: 2017, 2018
lastupdated: "2018-08-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Umgebung aktualisieren
{: #updating-your-environment}

## Wartungsstrategie
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} wird regelmäßig aktualisiert, sodass sichergestellt ist, dass neue Serviceinstanzen mit den aktuellen Fixpacks und Patches erstellt werden. Die Cloud bietet eine einfache und schnelle Bereitstellung neuer Serviceinstanzen für das Middleware-Management.

Sie können eine Instanz von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} mit der aktuellen oder einer vorherigen Fixpackstufe (n oder n-1) für eine bestimmte Produktversion erstellen. Das aktuelle Fixpack umfasst die neuesten Aktualisierungen und Features, das vorherige Fixpack ist jedoch möglicherweise erforderlich, um die Hybrid Cloud-Bereitstellungsanforderungen zu erfüllen.

Bei der Erstellung einer neuen Instanz können Sie eine der folgenden Fixpackstufen auf der Registerkarte **Serviceprofil** in der Serviceinstanz auswählen:

**Liberty**
  * 18.0.0.2
  * 18.0.0.1

**WebSphere Application Server (klassisch)**
  * 9.0.0.8
  * 9.0.0.7
  * 8.5.5.14
  * 8.5.5.13

## Fixes und Fixpack-Aktualisierungen anwenden
{:#applying-fixes}

Die schnellste Möglichkeit, eine Aktualisierung auf die neueste Wartungsstufe durchzuführen ist die Erstellung einer neuen Instanz. Wenn Sie jedoch Serviceinstanzen über einen längeren Zeitraum hinweg beibehalten möchten, können Sie Wartungsoperationen für die vorhandene Installation vornehmen, indem Sie das bereitgestellte Script `installService.sh` ausführen oder indem Sie IBM Installation Manager verwenden, wie in den folgenden Abschnitten beschrieben.

### Aktualisierung mit dem Script 'installService.sh'

Die Serviceinstanz ist mit einem Installation Manager-Repository konfiguriert, das häufig mit verfügbaren Sicherheitsfixes und WebSphere Application Server-Fixpacks aktualisiert wird. Sie können das Script `/home/virtuser/installService.sh` verwenden, um diese Fixes und Fixpacks anzuwenden. Sie müssen das Script als Rootbenutzer ausführen.

Die Menge an Plattenspeicher, die für die Installation der Aktualisierungen erforderlich ist, variiert abhängig von den installierten Aktualisierungstypen. Wenn nur die vorläufigen Fixes installiert werden, ist 1 GB freier Speicherplatz auf der virtuellen Maschine erforderlich. Für die Installation von Fixpacks sind 1,3 GB an Plattenspeicherplatz erforderlich.

Durch die Ausführung des Scripts werden die folgenden Aktionen durchgeführt:

* Stoppt alle aktiven Instanzen von WebSphere Application Server und IBM HTTP Server.
* Installiert wahlweise die neuesten Fixpacks für Installation Manager, WebSphere Application Server, IBM HTTP Server und das Java&trade;-SDK.
* Installiert die neuesten vorläufigen Fixes für WebSphere, IBM HTTP Server und das Java&trade;-SDK.
* Startet alle Instanzen neu.

#### Optionen
* **`-fixpacks`**

    Führt für alle Pakete eine Aktualisierung auf das neueste Fixpack durch.
* **`-noprompt`**

    Zeigt vor der Aktualisierung keine Eingabeaufforderung zur Bestätigung an.

#### Syntaxbeispiele

```
./installService.sh -?
```
{:.codeblock}

Zeigt den Hilfetext an.


```
./installService.sh
```
{:.codeblock}

Installiert alle anwendbaren vorläufigen Fixes, jedoch keine Fixpacks.


```
./installService.sh -fixpacks
```
{:.codeblock}

Installiert alle verfügbaren Fixpacks und anschließend alle anwendbaren vorläufigen Fixes.

### Aktualisierung mit Installation Manager
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} wird im Verzeichnis `/home/virtuser/IBM/Installation Manager` installiert und kann direkt zur Anwendung von Fixes und Fixpacks ausgeführt werden.

**Probleme vermeiden:** Da die Installation der zugrunde liegenden Binärdateien als `virtuser` ausgeführt wird, d. h. als virtueller Benutzer mit begrenzter Administratorberechtigung, müssen Sie sicherstellen, dass Installation Manager stets als `virtuser` ausgeführt wird.

## System-Updates für virtuelle Maschinen anwenden
{:#vm-system-updates}

Die Anwendung von Systemaktualisierungen für eine virtuelle Maschine ähnelt der Aktualisierung eines physischen Red Hat Enterprise Linux&reg;-Systems (RHEL-Systems). Mithilfe des Yum-Paketmanagers können Sie Pakete installieren, aktualisieren, deinstallieren und verwalten. Systeme mit WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} werden so konfiguriert, dass sie Aktualisierungen vom IBM Red Hat Satellite-Server erhalten, der geschützte, sichere Pakete über das Red Hat-Netz bereitstellt. Der Satellite-Server wird von IBM verwaltet und kann von Ihrem System aus nicht geändert werden.

Weitere Informationen finden Sie in [Paketaktualisierungen in Red Hat Enterprise Linux anwenden](https://access.redhat.com/articles/11258#rhel6){: new_window} und in [Yum, der Red Hat-Paketmanager](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}.
