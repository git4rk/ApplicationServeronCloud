---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Informazioni
{: #about}

{{site.data.keyword.appserver_full}} aiuta a impostare rapidamente un'istanza WebSphere Application Server Liberty, Traditional Network Deployment o Traditional WebSphere Java EE preconfigurata in un ambiente cloud ospitato su {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

## Panoramica di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} fornisce ai consumatori i server Traditional WebSphere e Liberty. È ospitato su guest macchina virtuale con accesso root al
sistema operativo guest. Quando crei il tuo servizio, scegli tra _Liberty_, _Traditional ND_ o _Traditional WebSphere_.

**Nota:** i consumatori possono ora scegliere tra il livello di fix pack corrente o una versione precedente [(n o n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} quando crei un'istanza di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.

Ti verrà offerta una classica esperienza di amministrazione WebSphere e avrai accesso completo al sistema operativo
sottostante. Puoi riutilizzare i tuoi script esistenti e apportare quelle piccole modifiche al
sistema di cui hai bisogno per lavorare con il tuo framework o con quello di terze parti. Admin Center e Admin Console sono forniti per amministrare il tuo servizio WebSphere Application Server Liberty, ND o tradizionale, proprio come le tue configurazioni WebSphere installate in loco.

Il piano WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment consiste in un ambiente di cella WebSphere Application Server Network Deployment con due o più macchine virtuali. La prima macchina virtuale contiene il Deployment Manager e IBM HTTP Server e le restanti macchine virtuali contengono nodi personalizzati (agent nodo) federati al Deployment Manager. Utilizza i tuoi script wsadmin esistenti per creare la tua configurazione WebSphere o utilizza la console di gestione WebSphere per configurare manualmente l'ambiente. Queste nuove funzionalità consentono agli utenti di impostare un ambiente in cluster per l'elevata disponibilità, il che è un aspetto critico per ogni applicazione aziendale middleware. I clienti possono ora scegliere di organizzare in cluster una topologica per bilanciare il carico delle richieste tra due o più istanze.

Il piano WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment include anche l'utilizzo di un collettivo Liberty. Il collettivo Liberty è un dominio amministrativo per un gruppo di profili Liberty (server) ed è costituito da due o più macchine virtuali. La prima macchina virtuale contiene il server Liberty Controller collettivo, che è un punto di controllo per il collettivo Liberty. Oltre al collettivo Liberty, questa macchina virtuale contiene anche IBM HTTP Server, che consente l'accesso alle tue applicazioni da un browser web. Le restanti macchine virtuali sono gli host collettivi in cui risiedono i membri collettivi (server del profilo Liberty). La funzione Liberty Admin Center è anche abilitata sul server di controller Liberty.

La seguente figura mostra l'architettura degli ambienti della cella WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment e del collettivo Liberty.

Figura 1. Architettura della cella Network Deployment e del collettivo Liberty

![Figura 1. Architettura della cella Network Deployment e del collettivo Liberty](images/CellCollectiveDiagram.gif)

**Nota**: nella precedente _Figura 1_, il pattern che descrive la collocazione del Deployment Manager o del controller collettivo con IBM HTTP Server è destinato a scopi di sviluppo e verifica. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} ti fornisce inoltre la libertà di riconfigurare il software pre-installato per soddisfare le tue esigenze operative e le applicazioni di produzione, proprio come faresti in loco. Inoltre, per rigorosi requisiti di produzione, contatta il rappresentante del settore Vendite di IBM in merito alla nostra offerta IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} a singolo tenant, che offre risorse di calcolo e di rete isolate.


## Ambiente operativo
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} è un servizio che restituisce i guest (macchine virtuali) in un ambiente condiviso per consentire agli utilizzatori di distribuire le applicazioni. Una VPN
protegge il servizio pubblico da scansioni di porta generiche e altri attacchi indesiderati basati sulla rete. Tuttavia, è importante notare che la VPN del servizio che usi per accedere alla tua istanza del servizio potrebbe essere
condivisa tra più organizzazioni e utenti
{{site.data.keyword.Bluemix_notm}}. Le macchine virtuali
forniscono risorse di elaborazione, memoria e I/O, che provengono da un pool condiviso di
risorse IaaS.

Poiché le specifiche risorse di elaborazione, memoria e I/O sono eseguite da macchine virtuali in un ambiente condiviso, le configurazioni del servizio possono variare. Le configurazioni per ciascuna specifica istanza del servizio possono essere visualizzate mediante i portali e i dashboard del servizio IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} fornisce istanze della macchina virtuale. Con queste istanze, i clienti utilizzano un portale semplice per creare e gestire le distribuzioni di WebSphere Application Server aziendale in un modo coerente, ripetibile con flessibilità significativa per ottimizzare le loro applicazioni. Gli utenti possono iniziare a lavorare su un WebSphere Application Server Liberty preconfigurato, ND o su macchine virtuali tradizionali in un ambiente cloud ospitato. Gli utenti possono migrare le applicazioni WebSphere Application Server esistenti su {{site.data.keyword.Bluemix_notm}} e prendere il controllo completo del sottostante SO e middleware.

## Dimensionamento della macchina virtuale
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} fornisce il dimensionamento T-shirt che ti consente di dimensionare correttamente gli ambienti per le applicazioni a uso intensivo di memoria mediante il provisioning di macchine virtuali più grandi. Ogni macchina virtuale che fornisci per eseguire WebSphere Application Server può essere dimensionata in modo indipendente in base alle esigenze delle risorse previste.

Le macchine virtuali sono dimensionate e prezzate in *blocchi*. Per ogni blocco nella dimensione T-shirt, la macchina virtuale viene fornita con le seguenti risorse.
* 1 CPU virtuale (vCPU)
* 2 GB di RAM
* 12,5 GB di spazio su disco rigido (12 GB per le VM a singolo blocco)


| T-Shirt | Blocchi | vCPU | RAM (GB) | HD (GB) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
| S | 1 | 1 | 2 | 12 |
| M | 2 | 2 | 4 | 25 |
| L | 4 | 4 | 8 | 50 |
| XL | 8 | 8 | 16 | 100 |
| XXL | 16 | 16 | 32 | 200 |
{: caption="Tabella 1. Blocchi per dimensione T-shirt" caption-side="top"}

Ogni server o nodo viene fornito in una singola macchina virtuale. Ad esempio, nel piano Network Deployment, se esegui il provisioning di una macchina virtuale M (2 blocchi) per il tuo Deployment Manager e 8 macchine virtuali S (1 blocco) per i nodi dell'applicazione, ti vengono addebitati un totale di 10 blocchi.

## Opzioni di fatturazione
{: #billing-options}

La determinazione del prezzo per ciascun blocco dipende dall'opzione di fatturazione che scegli:
* **[Pagamento a consumo](#pay-as-you-go):** fatturazione basata sull'utilizzo, con prezzo in ore per blocco utilizzato
* **[Contratto di riserva](#reserve-contract):** sottoscrizioni mensili prepagate di risorse riservate

### Pagamento a consumo
{: #pay-as-you-go}

La determinazione del prezzo con pagamento a consumo si applica se esegui il provisioning del servizio IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} senza contattare il settore Vendite IBM per delle opzioni di fatturazione alternative. L'utilizzo viene addebitato per l'ora intera o parziale di ogni blocco utilizzato durante il periodo di fatturazione mensile. La fatturazione minima è impostata su 1/4 di un'ora del blocco.

**Note**: a causa di una quantità specifica di risorse di calcolo, memoria e I/O, le istanze arrestate vengono addebitate a un tasso ridotto del 5% del tasso di blocco orario. All'interno del servizio, le istanze arrestate sono limitate a 10 indirizzi IP o a 64 GB di memoria.

#### Prezzi del piano

Il prezzo per ciascun blocco varia a seconda del piano WebSphere Application Server che scegli.

La seguente tabella elenca il prezzo totale all'ora per ogni macchina virtuale con dimensionamento T-shirt. I prezzi rappresentano i piani di IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} a partire al 1° aprile 2016 e sono elencati in dollari americani (USD). Consulta il catalogo per i prezzi correnti nella tua regione.

| T-Shirt | Blocchi | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
| S | 1 | $0,21 | $0,30 |  $0,70 |
| M | 2 | $0,42 | $0,60 |  $1,40 |
| L | 4 | $0,84 | $1,20 |  $2,80 |
| XL | 8 | $1,68 | $2,40 |  $5,60 |
| XXL | 16 | $3,36 | $4,80 |  $11,20 |
{: caption="Tabella 2. Piano Liberty Core" caption-side="top"}


### Contratto di riserva
{:#reserve-contract}

Con la fatturazione del contratto di riserva, acquisti una sottoscrizione mensile prepagata che garantisce l'accesso a blocchi di risorse computazionali riservate fisicamente. Questi blocchi di servizio sono riservati per il tuo uso esclusivo e non possono essere considerati come capacità disponibile per gli altri utenti di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}. Se hai delle licenze WebSphere Application Server esistenti, puoi scegliere un contratto di riserva BYOL (bring-your-own-license), che utilizza queste licenze e ha un tasso di fatturazione ridotto. Per impostare la fatturazione del contratto di riserva, [contatta il settore Vendite IBM](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

Le sottoscrizioni sono disponibili in incrementi di 8 blocchi. Le ore totali del blocco si basano sul numero di ore del mese, ma puoi utilizzare le ore del blocco in qualsiasi momento durante tutto il mese. Ad esempio, un mese di 30 giorni ha 720 ore, che se moltiplicate per una sottoscrizione di 8 blocchi comportano un totale di 5.760 ore del blocco.

  ```
30 giorni * 24 ore al giorno * 8 blocchi = 5.760 ore del blocco
  ```

Puoi personalizzare come e quando utilizzare i blocchi per soddisfare la domanda di carico di lavoro variabile, ad esempio utilizzando 4 blocchi, aumentando fino a 12 blocchi e quindi riducendo a 8 blocchi. Fintanto che rimani sotto le ore del blocco totali nel mese, non ci sono costi aggiuntivi.

Puoi scegliere se utilizzare i tuoi blocchi del contratto di riserva oppure se utilizzare la fatturazione con pagamento a consumo quando esegui il provisioning di ciascun ambiente.

**Nota:** se elimini un'istanza del servizio, potresti dover attendere circa 30 minuti perché i suoi blocchi diventino disponibili alle nuove istanze del servizio.

#### Eccedenze

Se il tuo utilizzo supera le ore del blocco mensili previste nella tua sottoscrizione, l'eccedenza viene addebitata in base al modello di fatturazione di pagamento a consumo, pertanto ti vengono addebitate solo le ore del blocco addizionali che utilizzi. L'utilizzo del blocco viene misurato su base oraria totale o parziale, con un utilizzo minimo di 1/4 di un'ora del blocco.

I blocchi del modello pagamento a consumo non sono risorse riservate e provengono da un pool di risorse comuni.

#### Tassi di ripartizione per un uso flessibile

I blocchi nella fatturazione del contratto di riserva si basano sul piano di WebSphere Application Server Network Deployment, ma puoi utilizzare i blocchi anche per altri piani. Con altri piani, l'utilizzo viene ripartito proporzionalmente in modo che un'ora del blocco sia ridotta dal tasso di ripartizione del piano quando si riflette nelle ore del blocco rimanenti del contratto di riserva.

La seguente tabella mostra i tassi di ripartizione per ciascun piano e il prezzo effettivo per ogni ora reale del blocco dopo il calcolo della ripartizione. Per i prezzi correnti nella tua regione, [contatta il settore Vendite IBM](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

| Piano | Tasso di ripartizione | Prezzo/ora dopo la ripartizione |
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0,3 | $0,21 |
| WebSphere Application Server Base  | 0,43 | $0,30 |
| WebSphere Application Server Network Deployment | 1,0 | $0,70 |
{: caption="Tabella 3. Tassi di ripartizione delle ore del blocco per ogni piano" caption-side="top"}

Ad esempio, potresti avere un'istanza WebSphere Application Server Base con dimensione M (2 blocchi) che viene eseguita per 51 ore. Per calcolare le ore di blocco utilizzate dal contratto di riserva, le ore del blocco effettive vengono moltiplicate per il tasso di ripartizione, per un totale di 43,86 ore del blocco:

```
2 blocchi * 51 ore * ripartizione di 0,43 = 43,86 ore del blocco ripartite proporzionalmente
```

Il costo totale rimane lo stesso, ma puoi utilizzare più ore del blocco reali dei piani ripartiti perché deducono meno dalle ore del blocco del contratto di riserva.
{:.tip}
