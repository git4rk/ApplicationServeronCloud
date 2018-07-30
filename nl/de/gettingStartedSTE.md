---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Single-Tenant-Umgebungen
{: #getting_startedSTE}

Bei der Single-Tenant-Umgebung von {{site.data.keyword.appserver_full}} handelt es sich um ein Angebot, das Kunden eine isolierte WebSphere-Workload, eine voll integrierte Hybridumgebung und geschützte Daten bietet. In dieser Anleitung zur Einführung werden zentrale Elemente beschrieben, die Kunden beim Zugriff auf die Single-Tenant-Umgebung von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} und bei deren Verwaltung unterstützen.
{: shortdesc}


## Empfohlene Software
{: #recommended_software}

Für den Zugriff auf die Single-Tenant-Umgebung ist die folgende Sofware erforderlich:
* Von {{site.data.keyword.Bluemix_notm}} unterstützter Web-Browser:
    * Chrome: neueste Version für das verwendete Betriebssystem
    * Firefox: neueste Version für das verwendete Betriebssystem oder neueste ESR-Version
    * Internet Explorer: Version 10 oder 11
    * Safari: neueste Version für Mac
* Cloud Foundry-Befehlszeilenschnittstelle Version 6.5.1 oder höher (das neueste Release kann verwendet werden)
* Git Bash (empfohlen)
    * [Git Bash](https://git-scm.com/downloads){: new_window} herunterladen und installieren


## Übersicht zu WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single-Tenant-Umgebung
{: #overviewSTE}

Mit dem Single-Tenant-Angebot von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} stehen Kunden eine eigene private Instanz des Service, privater Netzbetrieb und isolierte Ressourcen zur Verfügung. Obwohl das Angebot unabhängig verwaltet wird, kann auf den Service und die erstellten Serviceinstanzdashboards über eine spezielle öffentliche {{site.data.keyword.Bluemix_notm}}-Region zugegriffen werden, wie in der folgenden Abbildung dargestellt:

Abbildung 1. WebSphere Application Server-Architektur in {{site.data.keyword.Bluemix_notm}}: Single-Tenant-Umgebung

![Abbildung 1. Architektur einer Single-Tenant-Umgebung](images/WASaaS.png)


## Organisationsverwaltung
{: #organization_management}

Die Single-Tenant-Umgebung von WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} wird Ihrer Bestellung entsprechend konfiguriert. Wenn Sie im Rahmen der Bestellung einen oder mehrere {{site.data.keyword.Bluemix_notm}}-Organisationsnamen angegeben haben, können Sie sofort auf die Umgebung zugreifen. Wenn Sie keinen Organisationsnamen angegeben haben oder wenn Sie diese Einstellung ändern möchten, öffnen Sie ein [Support-Ticket](reportingIssues.html#reporting_issues) für **Application Services** in der {{site.data.keyword.Bluemix_notm}}-Konsole Ihrer Region. Der Organisationsname (ORG) befindet sich in der rechten oberen Ecke der {{site.data.keyword.Bluemix_notm}}-Konsole, wie in der folgenden Abbildung dargestellt:

Abbildung 2. Position der Organisationsnamen

![Abbildung 2. Position der Organisationsnamen](images/myORG.png)


**Hinweis:** Informationen zum Zugriff auf die Single-Tenant-Umgebung finden Sie in [Zugriff auf die Single-Tenant-Umgebung](singleTenantAccess.html#singleTenantEnvironment).
