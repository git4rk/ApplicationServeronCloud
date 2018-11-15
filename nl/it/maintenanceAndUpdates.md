---

copyright:
  years: 2017, 2018
lastupdated: "2018-08-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Aggiornamento del tuo ambiente
{: #updating-your-environment}

## Strategia di manutenzione
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} viene aggiornato regolarmente, garantendo che le nuove istanze del servizio vengano create con i fix pack e le patch correnti. Il cloud offre alla gestione middleware un provisioning facile e rapido
di nuove istanze del servizio.

Puoi creare un'istanza di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} al livello di fix pack corrente o precedente (n o n-1) per una particolare versione del prodotto. L'utilizzo del fix pack corrente fornisce gli aggiornamenti e le funzionalità più recenti, ma potrebbe essere necessario il fix pack precedente per conformarsi ai requisiti di distribuzione del cloud ibrido.

Quando crei una nuova istanza, puoi scegliere tra i seguenti livelli di fix pack nella scheda **Service Profile** dell'istanza del servizio:

**Liberty**
  * 18.0.0.2
  * 18.0.0.1

**WebSphere Application Server tradizionale**
  * 9.0.0.8
  * 9.0.0.7
  * 8.5.5.14
  * 8.5.5.13

## Applicazione di correzioni e aggiornamenti del fix pack
{:#applying-fixes}

Il modo più rapido per effettuare l'aggiornamento al livello di manutenzione più recente è creare una nuova istanza. Tuttavia, se preferisci conservare le istanze del servizio di lunga durata, puoi applicare la manutenzione alla tua installazione esistente eseguendo lo script `installService.sh` fornito o utilizzando IBM Installation Manager come descritto nelle seguenti sezioni.

### Aggiornamento mediante lo script installService.sh

La tua istanza del servizio è configurata con un repository di Installation Manager che viene frequentemente aggiornato con correzioni di sicurezza disponibili e fix pack di WebSphere Application Server. Puoi utilizzare lo script `/home/virtuser/installService.sh` per applicare tali correzioni e fix pack. Lo script deve essere eseguito come utente root.

La quantità di spazio su disco necessaria per installare gli aggiornamenti varia in base ai tipi di aggiornamenti che installi. L'installazione di sole correzioni temporanee richiede 1 GB di spazio libero sulla macchina virtuale. L'installazione dei fix pack aumenta lo spazio su disco richiesto a 1,3 GB.

L'esecuzione dello script effettua le seguenti azioni:

* Arresta tutte le istanze WebSphere Application Server e IBM HTTP Server in esecuzione
* Facoltativamente, installa i fix pack più recenti per Installation Manager, WebSphere Application Server, IBM HTTP Server e l'SDK Java
* Installa le ultime correzioni temporanee per WebSphere, IBM HTTP Server e l'SDK Java
* Riavvia tutte le istanze

#### Opzioni
* **`-fixpacks`**

    Aggiorna tutti i pacchetti al fix pack più recente.
* **`-noprompt`**

    Non richiede conferma prima dell'aggiornamento.

#### Esempi di sintassi

```
./installService.sh -?
```
{:.codeblock}

Visualizza il testo della guida.


```
./installService.sh
```
{:.codeblock}

Installa tutte le correzioni temporanee applicabili, ma nessun fix pack.


```
./installService.sh -fixpacks
```
{:.codeblock}

Installa tutti i fix pack disponibili e quindi installa tutte le correzioni temporanee applicabili.

### Aggiornamento mediante Installation Manager
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} viene installato nella directory `/home/virtuser/IBM/Installation Manager` e può essere eseguito direttamente per applicare le correzioni e i fix pack.

**Prevenzione dei problemi:** poiché i file binari sottostanti vengono installati come **virtuser**, un utente virtuale amministrativo limitato, assicurati che Installation Manager venga eseguito sempre come **virtuser**.

## Applicazione degli aggiornamenti di sistema alle macchine virtuali
{:#vm-system-updates}

L'applicazione degli aggiornamenti di sistema su una macchina virtuale è simile all'aggiornamento di un sistema fisico Red Hat Enterprise Linux (RHEL). Utilizzando il gestore pacchetti Yum, puoi installare, aggiornare, disinstallare e gestire in altro modo i pacchetti. I sistemi WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} sono configurati per ricevere gli aggiornamenti dal server Red Hat Satellite di IBM, che fornisce pacchetti sicuri e protetti dalla rete Red Hat. Il server Satellite è gestito da IBM e non può essere modificato dal tuo sistema.

Per ulteriori informazioni, vedi [Applicazione di aggiornamenti dei pacchetti su Red Hat Enterprise Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} e [Yum: la gestione pacchetti Red Hat](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}.
