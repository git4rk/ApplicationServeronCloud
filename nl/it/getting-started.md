---

copyright:
  years: 2018
lastupdated: "2018-06-08"

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

Se vuoi un ambiente con più risorse dedicate della macchina virtuale, come un contratto di riserva o un ambiente a singolo tenant, dovrai contattare il settore Vendite IBM prima di creare il servizio. Scopri di più su queste opzioni in [Informazioni](index.html).

## Passo 1: crea il servizio
{: #create}

1. Vai alla pagina [{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) nel catalogo {{site.data.keyword.cloud_notm}}.
1. Accedi con il tuo ID IBM o registrarti per un account {{site.data.keyword.cloud_notm}}.
1. Nella pagina del catalogo, rivedi le selezioni per la configurazione del servizio.

  Per gli ambienti con pagamento a consumo, utilizza le selezioni predefinite o modificale in base alle tue esigenze. Se hai un contratto di riserva o un ambiente a singolo tenant, presta particolare attenzione alle seguenti opzioni.

  * **Contratto di riserva:** in **Scegli una regione/ubicazione in cui distribuire**, verifica che la regione selezionata sia la regione corretta per il tuo contratto.

  * **Ambiente a singolo tenant:** in **Scegli una regione/ubicazione in cui distribuire**, verifica che la regione selezionata sia la regione in cui viene distribuito il tuo ambiente a singolo tenant. In **Ambiente**, seleziona il tuo ambiente a singolo tenant. Per impostazione predefinita, potrebbe essere mostrato l'ambiente pubblico.

    Se non vedi elencato il tuo ambiente a singolo tenant, verifica di essere nella regione corretta e che la tua organizzazione abbia accesso al tuo ambiente a singolo tenant.
    {: tip}
1. Seleziona il piano dei prezzi per l'edizione di {{site.data.keyword.appserver_short}} che vuoi distribuire.
1. Fai clic su **Crea**.


## Passo 2: scegli il tuo ambiente
{: #choose_env}

I piani {{site.data.keyword.appserver_short}} Base e Liberty Core prevedono solo server singoli, quindi se hai scelto questi piani, puoi saltare questo passo.

Per il piano Network Deployment, scegli il profilo e l'architettura per il tuo ambiente.

* **Profilo:** scegli {{site.data.keyword.appserver_short}} tradizionale o Liberty
* **Architettura:** scegli un ambiente a server singolo o un ambiente cluster con celle tradizionali o collettivi Liberty


## Passo 3: dimensiona le tue macchine virtuali
{: #vm_sizing}

Puoi dimensionare individualmente la macchina virtuale per ciascun componente nel tuo ambiente. Il dimensionamento delle macchine virtuali è suddiviso in più parti in [dimensioni T-shirt](index.html#vm-size) di blocchi di risorse.

Fai clic sulla scheda relativa al componente, ad esempio il server, il Deployment Manager o il nodo dell'applicazione e seleziona la dimensione T-shirt per sua la macchina virtuale.

## Passo 4: esegui il provisioning del tuo ambiente
{: #service_profile}

Rivedi i dettagli nel riepilogo della configurazione del servizio, compreso il tempo stimato necessario per eseguire il provisioning. Fai clic su **Provisioning** per impostare il tuo ambiente {{site.data.keyword.appserver_short}}.

## Passi successivi
{: #anchor_value}

Scopri come accedere e gestire il tuo nuovo ambiente {{site.data.keyword.appserver_short}} in [Accesso al sistema](systemAccess.html).
