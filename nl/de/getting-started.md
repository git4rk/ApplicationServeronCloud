---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-18"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Lernprogramm - Einführung
{:#getting-started}

Mit {{site.data.keyword.appserver_full}} können Sie innerhalb von Minuten eine vorkonfigurierte klassische WebSphere Application Server-Umgebung oder eine vorkonfigurierte WebSphere Application Server Liberty-Umgebung einrichten. Dieses Einführungslernprogramm enthält eine Anleitung, mit der Sie in nur wenigen Schritten eine WebSphere Application Server-Umgebung auf einer virtuellen Maschine einrichten können.
{: shortdesc}

## Vorbereitungen
{: #prereqs}

Wenn Sie eine Umgebung mit virtuellen Maschinenressourcen einrichten möchten, die in einem höheren Maß dediziert sind, wie z. B. im Rahmen eines Reservierungsvertrags oder einer Single-Tenant-Umgebung, wenden Sie sich an den IBM Vertrieb, bevor Sie den Service erstellen. Weitere Einzelheiten zu diesen Optionen finden Sie im Abschnitt [Informationen](/docs/services/ApplicationServeronCloud?topic=wasaas-about#about).

### Vorhandene WebSphere-Umgebung migrieren

Wenn Sie eine vorhandene WebSphere Application Server Network Deployment-Umgebung in diesen Service migrieren möchten, verwenden Sie das [WebSphere Configuration Migration Tool for {{site.data.keyword.cloud_notm}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window}. Mit dem Tool werden die Profilkonfiguration und die Anwendungen für den eigenständigen Server oder die Zellenknoten in einer Serviceinstanz in {{site.data.keyword.cloud_notm}} hochgeladen. Eine Übersicht über die Cloud-Migration und eine Anleitung zur Verwendung des Tools in einzelnen Schritten finden Sie im [Handbuch zum WebSphere Configuration Migration Tool for IBM Cloud ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window} in WASdev.

Im Folgenden werden die einzelnen Schritte zur Erstellung einer neuen Umgebung in {{site.data.keyword.appserver_full}} beschrieben.

## Schritt 1: Service erstellen
{: #create}

1. Rufen Sie die [{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server)-Seite im {{site.data.keyword.cloud_notm}}-Katalog auf.
1. Melden Sie sich mit Ihrer IBMid an oder führen Sie eine Anmeldung für ein {{site.data.keyword.cloud_notm}}-Konto durch.
1. Überprüfen Sie auf der Katalogseite die Auswahlmöglichkeiten für die Servicekonfiguration.

  Verwenden Sie für nutzungsabhängige Umgebungen die Standardoptionen oder ändern Sie sie nach Bedarf.

  Wenn Sie einen Reservierungsvertrag oder eine Single-Tenant-Umgebung verwenden, beachten Sie die nachfolgend beschriebenen Optionen sorgfältig.

  * **Reservierungsvertrag:** Vergewissern Sie sich, dass es sich bei der unter **Region/Standort für Bereitstellung auswählen** ausgewählten Region um die korrekte Region für Ihren Vertrag handelt.

  * **Single-Tenant-Umgebung:** Vergewissern Sie sich, dass es sich bei der unter **Region/Standort für Bereitstellung auswählen** ausgewählten Region um die Region der Bereitstellung Ihrer Single-Tenant-Umgebung handelt. Wählen Sie unter **Umgebung** Ihre Single-Tenant-Umgebung aus. Standardmäßig wird möglicherweise die öffentliche Umgebung angezeigt.

    Wenn Ihre Single-Tenant-Umgebung nicht aufgeführt ist, überprüfen Sie, ob Sie sich in der korrekten Region befinden und ob Ihre Organisation über Zugriff auf Ihre Single-Tenant-Umgebung verfügt.
    {: tip}
1. Wählen Sie den Preisstrukturplan für die {{site.data.keyword.appserver_short}}-Edition aus, die Sie bereitstellen möchten.
1. Klicken Sie auf **Erstellen**.


## Schritt 2: Umgebung auswählen (nur Network Deployment)
{: #choose_env}

Der {{site.data.keyword.appserver_short}} Base- und der Liberty Core-Plan umfassen nur Einzelserver, d. h., bei der Verwendung dieser Pläne können Sie diesen Schritt überspringen.

Wählen Sie für den Network Deployment-Plan das Profil und die Architektur für Ihre Umgebung aus.

* **Profil:** Wählen Sie {{site.data.keyword.appserver_short}} (klassisch) oder WebSphere Application Server Liberty aus.
* **Architektur:** Wählen Sie eine Einzelserverumgebung oder eine Clusterumgebung mit traditionellen Zellen oder Liberty-Verbünden aus.


## Schritt 3: Größe der virtuellen Maschine bestimmen
{: #vm_sizing}

Die Größe der virtuellen Maschine kann für jede Komponente in der Umgebung individuell bestimmt werden. Virtuelle Maschinen sind in Ressourcenblöcke unterteilt, die in [T-Shirt-Größen](/docs/services/ApplicationServeronCloud?topic=wasaas-about#vm-size) angegeben werden.

Klicken Sie auf die Registerkarte für die jeweilige Komponente, z. B. den Server, den Bereitstellungsmanager oder den Anwendungsknoten, und wählen Sie die T-Shirt-Größe für die zugehörige virtuelle Maschine aus.

## Schritt 4: Umgebung bereitstellen
{: #service_profile}

Überprüfen Sie die Details in der Servicekonfigurationszusammenfassung einschließlich der geschätzten Zeit für die Bereitstellung.

**Reservierungsvertrag:** Stellen Sie sicher, dass für die Option **Abrechnung** die Einstellung _Reservierungsvertrag_ ausgewählt ist. Wenn diese Option nicht angezeigt wird, stellen Sie sicher, dass der für [Ihre Organisation](/docs/account?topic=account-orgsspacesusers){:new_window} eingegebene Name exakt mit dem Organisationsnamen des Vertrags übereinstimmt, einschließlich Groß-/Kleinschreibung und Leerzeichen. Wenn Sie diesen Service bereitstellen, ohne die Abrechnung im Rahmen eines Reservierungsvertrags auszuwählen, wird eine nutzungsabhängige Abrechnung verwendet.

Klicken Sie auf **Bereitstellen**, um die {{site.data.keyword.appserver_short}}-Umgebung einzurichten.

## Weitere Schritte
{: #anchor_value}

Informationen zum Zugriff auf die neue {{site.data.keyword.appserver_short}}-Umgebung sowie zur Verwaltung finden Sie in [Systemzugriff](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access).
