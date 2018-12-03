---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Ambienti a singolo tenant
{: #getting_startedSTE}

L'ambiente a singolo tenant {{site.data.keyword.appserver_full}} fornisce ai clienti un carico di lavoro WebSphere isolato, un ambiente ibrido completamente integrato e dei dati protetti. Questa guida introduttiva è progettata per identificare gli elementi chiave che ti aiuteranno ad accedere e gestire il tuo ambiente a singolo tenant.
{: shortdesc}

## Ordinazione di un ambiente a singolo tenant
{:#ordering}

Gli ambienti a singolo tenant non possono essere creati tramite il catalogo {{site.data.keyword.Bluemix_notm}} e devono essere ordinati contattando il settore Vendite IBM. Quando ordini il tuo ambiente, puoi scegliere da un ambiente a singolo tenant standard oppure BYOL (bring-your-own-license). Gli ambienti a singolo tenant standard includono tutta l'infrastruttura e le licenze WebSphere Application Server necessarie. Negli ambienti a singolo tenant BYOL (bring-your-own-license), puoi utilizzare licenze WebSphere Application Server separate.

Per ordinare un ambiente a singolo tenant, [contatta il settore Vendite IBM](reportingIssues.html#contacting-sales). Il team di vendita può aiutarti nella configurazione di un ambiente personalizzato in base alle tue esigenze. 

## Panoramica di WebSphere Application Server in un ambiente a singolo tenant {{site.data.keyword.Bluemix_notm}}
{: #overviewSTE}

L'ambiente a singolo tenant ti fornisce l'istanza del servizio, rete privata e risorse isolate. Sebbene l'offerta sia gestita in modo indipendente, i dashboard del servizio e dell'istanza del servizio creata sono accessibili attraverso una specifica regione pubblica {{site.data.keyword.Bluemix_notm}} come indicato nella seguente figura. 

Figura 1. Architettura di WebSphere Application Server in un ambiente a singolo tenant {{site.data.keyword.Bluemix_notm}}

![Figura 1. Architettura di un ambiente a singolo tenant](images/WASaaS.png)


## Gestione organizzazione
{: #organization_management}

WebSphere Application Server in un ambiente a singolo tenant {{site.data.keyword.Bluemix_notm}} viene configurato in base al tuo ordine. Se hai fornito uno o più nomi organizzazione {{site.data.keyword.Bluemix_notm}} come parte dell'ordine, puoi iniziare subito ad accedere al tuo ambiente. Se non hai fornito un nome organizzazione o se vuoi modificare questa impostazione, apri un [ticket di supporto](reportingIssues.html#reporting_issues) per i **Servizi dell'applicazione** dalla console {{site.data.keyword.Bluemix_notm}} della tua regione. Puoi trovare il tuo nome organizzazione nella console {{site.data.keyword.Bluemix_notm}} andando su **Gestisci > Account > Organizzazioni Cloud Foundry**.

**Nota:** per accedere al tuo ambiente a singolo tenant, vedi [Accesso all'ambiente a singolo tenant](singleTenantAccess.html#singleTenantEnvironment).
