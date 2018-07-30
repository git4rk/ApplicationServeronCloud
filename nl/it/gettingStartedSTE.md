---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Ambienti a singolo tenant
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}}:Single Tenant Environment è un'offerta che fornisce ai clienti un carico di lavoro WebSphere isolato, un ambiente ibrido completamente integrato e protezione dei dati. Questa guida introduttiva è progettata per identificare gli elementi chiave che aiutano i clienti ad accedere e gestire il loro WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment.
{: shortdesc}


## Software consigliato
{: #recommended_software}

Per accedere al tuo ambiente a singolo tenant, avrai bisogno del seguente software:
* Un browser web supportato da {{site.data.keyword.Bluemix_notm}}:
    * Chrome: la versione più recente per il tuo sistema operativo
    * Firefox: la versione più recente per il tuo sistema operativo o l'ultima versione ESR
    * Internet Explorer: versione 10 o 11
    * Safari: la versione più recente per il Mac
* Interfaccia riga di comando Cloud Foundry, versione 6.5.1 o successiva (puoi utilizzare l'ultima release)
* Git Bash (consigliato)
    * Scarica e installa [Git Bash](https://git-scm.com/downloads){: new_window}


## Panoramica di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment
{: #overviewSTE}

L'offerta di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment fornisce ai consumatori la loro istanza privata del servizio, rete privata e risorse isolate. Sebbene l'offerta sia gestita in modo indipendente, i dashboard del servizio e dell'istanza del servizio creata sono accessibili attraverso una specifica regione pubblica {{site.data.keyword.Bluemix_notm}} come indicato nella seguente figura:

Figura 1. Architettura di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment

![Figura 1. Architettura dell'ambiente a singolo tenant](images/WASaaS.png)


## Gestione organizzazione
{: #organization_management}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment viene configurato un base al tuo ordine. Se hai fornito uno o più nomi organizzazione {{site.data.keyword.Bluemix_notm}} come parte dell'ordine, puoi iniziare subito ad accedere al tuo ambiente. Se non hai fornito uno o più nomi organizzazione o se vuoi modificare questa impostazione, apri un [ticket di supporto](reportingIssues.html#reporting_issues) per i **Servizi dell'applicazione** dalla console {{site.data.keyword.Bluemix_notm}} della tua regione. Il nome organizzazione (ORG) può essere trovato nell'angolo superiore destro della console {{site.data.keyword.Bluemix_notm}} come mostrato nella seguente figura:

Figura 2. Posizione del nome organizzazione

![Figura2 . Posizione del nome ORG](images/myORG.png)


**Nota:** per accedere al tuo ambiente a singolo tenant, vedi [Accesso all'ambiente a singolo tenant](singleTenantAccess.html#singleTenantEnvironment).
