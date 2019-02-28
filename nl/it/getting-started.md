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


# Esercitazione introduttiva
{:#getting-started}

Con {{site.data.keyword.appserver_full}}, puoi impostare un ambiente WebSphere Application Server tradizionale o Liberty preconfigurato in pochi minuti. Questa esercitazione introduttiva ti guida nel provisioning di un ambiente WebSphere Application Server su una macchina virtuale attraverso pochi passi.
{: shortdesc}

## Prima di iniziare
{: #prereqs}

Se vuoi un ambiente con più risorse dedicate della macchina virtuale, come un contratto di riserva o un ambiente a singolo tenant, contatta il settore Vendite IBM prima di creare il servizio. Scopri di più su queste opzioni in [Informazioni](/docs/services/ApplicationServeronCloud?topic=wasaas-about#about).

### Migrazione di un ambiente WebSphere esistente

Per eseguire la migrazione di un ambiente WebSphere Application Server Network Deployment esistente a questo servizio, utilizza il [WebSphere Configuration Migration Tool for {{site.data.keyword.cloud_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window}. Lo strumento carica le applicazioni e la configurazione del profilo per il server autonomo o i nodi cella a un'istanza di servizio in {{site.data.keyword.cloud_notm}}. Per una panoramica della migrazione cloud e istruzioni dettagliate sull'utilizzo dello strumento, vedi [la guida per WebSphere Configuration Migration Tool for IBM Cloud ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window}  on WASdev.

I seguenti passi ti guidano nella creazione di un nuovo ambiente in {{site.data.keyword.appserver_full}}.

## Passo 1: crea il servizio
{: #create}

1. Vai alla pagina [{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server) nel catalogo {{site.data.keyword.cloud_notm}}.
1. Accedi con il tuo ID IBM o registrarti per un account {{site.data.keyword.cloud_notm}}.
1. Nella pagina del catalogo, rivedi le selezioni per la configurazione del servizio.

  Per gli ambienti con pagamento a consumo, utilizza le selezioni predefinite o modificale in base alle tue esigenze.

  Se hai un contratto di riserva o un ambiente a singolo tenant, presta particolare attenzione alle seguenti opzioni.

  * **Contratto di riserva:** in **Scegli una regione/ubicazione in cui distribuire**, verifica che la regione selezionata sia la regione corretta per il tuo contratto.

  * **Ambiente a singolo tenant:** in **Scegli una regione/ubicazione in cui distribuire**, verifica che la regione selezionata sia la regione in cui viene distribuito il tuo ambiente a singolo tenant. In **Ambiente**, seleziona il tuo ambiente a singolo tenant. Per impostazione predefinita, potrebbe essere mostrato l'ambiente pubblico.

    Se il tuo ambiente non viene elencato, verifica di essere nella regione corretta e che la tua organizzazione abbia accesso al tuo ambiente a singolo tenant.
    {: tip}
1. Seleziona il piano dei prezzi per l'edizione di {{site.data.keyword.appserver_short}} che vuoi distribuire.
1. Fai clic su **Crea**.


## Passo 2: scegli il tuo ambiente (solo Network Deployment)
{: #choose_env}

I piani {{site.data.keyword.appserver_short}} Base e Liberty Core prevedono solo server singoli, quindi se hai scelto questi piani, puoi saltare questo passo.

Per il piano Network Deployment, scegli il profilo e l'architettura per il tuo ambiente.

* **Profilo:** scegli {{site.data.keyword.appserver_short}} Traditional o Liberty
* **Architettura:** scegli un ambiente a server singolo o un ambiente cluster con celle tradizionali o collettivi Liberty


## Passo 3: dimensiona le tue macchine virtuali
{: #vm_sizing}

Puoi dimensionare individualmente la macchina virtuale per ciascun componente nel tuo ambiente. Le macchine virtuali sono suddivise in [dimensioni T-shirt](/docs/services/ApplicationServeronCloud?topic=wasaas-about#vm-size) di blocchi di risorse.

Fai clic sulla scheda relativa al componente, ad esempio il server, il Deployment Manager o il nodo dell'applicazione e seleziona la dimensione T-shirt per sua la macchina virtuale.

## Passo 4: esegui il provisioning del tuo ambiente
{: #service_profile}

Rivedi i dettagli nel riepilogo della configurazione del servizio, compreso il tempo stimato necessario per eseguire il provisioning.

**Contratto di riserva:** assicurati che l'opzione **Fatturazione** sia impostata su _Contratto di riserva_. Se non vedi l'opzione, verifica che [la tua organizzazione](/docs/account?topic=account-orgsspacesusers){:new_window} sia esattamente uguale, compresi maiuscole/minuscole e spazi vuoti, al nome dell'organizzazione per il tuo contratto. Se esegui il provisioning del servizio senza selezionare la fatturazione del contratto di riserva, viene utilizzata la fatturazione con pagamento a consumo.

Fai clic su **Provisioning** per impostare il tuo ambiente {{site.data.keyword.appserver_short}}.

## Passi successivi
{: #anchor_value}

Scopri come accedere e gestire il tuo nuovo ambiente {{site.data.keyword.appserver_short}} in [Accesso al sistema](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access).
