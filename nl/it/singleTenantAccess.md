---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Accesso all'ambiente a singolo tenant
{: #singleTenantEnvironment}


I seguenti passi illustrano come accedere al tuo ambiente a singolo tenant, insieme ai metodi di creazione di un'istanza del servizio.
{: shortdesc}


## Accesso al tuo ambiente a singolo tenant
{: #accessSTE}

1. Nel tuo browser, vai al [Catalogo {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/catalog/){: new_window}.

2. Fai clic su **Accedi** e accedi con il tuo ID IBM.

6. Nel filtro di ricerca del catalogo, immetti **WebSphere Application Server**.

    ![alt text](images/filter.png "Filtro di ricerca")

7. In **Servizi dell'applicazione**, fai clic sul tile **WebSphere Application Server**.

    ![alt text](images/iconWAS.png "Tile WebSphere Application Server")

8. Nel menu **Ambiente**, seleziona il tuo ambiente a singolo tenant. 

    ![alt text](images/environmentSTE.png "Nome ambiente a singolo tenant")

    **Prevenzione dei problemi:** l'ambiente pubblico potrebbe essere mostrato come predefinito. La visualizzazione del nome ambiente corretto presuppone che tu abbia effettuato l'accesso alla regione corretta e che sia un membro di un'organizzazione autorizzata ad accedere al tuo ambiente a singolo tenant.

    **Nota:** se selezioni uno degli ambienti pubblici, potresti incorrere in un addebito orario. Pertanto, se non vedi il nome del tuo ambiente a singolo tenant, apri un ticket di supporto come definito nella pagina [Richiesta di assistenza clienti](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window}.

9. Seleziona il piano appropriato e fai clic su **Crea**.

    ![alt text](images/createSTE.png "Scegli un piano e crea il tuo servizio")


**Nota:** il prezzo orario non si applica per gli ambienti a singolo tenant. Un ambiente a singolo tenant include un numero fisso di **blocchi** che vengono denominati quota. Un ambiente piccolo contiene 64 blocchi. Un ambiente medio contiene 128 blocchi e un ambiente grande contiene 256 blocchi.

Un **blocco** è definito come segue:
  * 1 vCPU
  * 12,5 GB di disco[1]
  * 2 GB di RAM

[1] *Tecnicamente, un sistema piccolo contiene solo 12 GB di disco. Un sistema medio contiene 25 GB di disco, un sistema grande contiene 50 GB e così via.*

Per ogni macchina virtuale che crei, specifica la dimensione T-shirt desiderata: S, M, L, XL o XXL, che corrisponde a 1, 2, 4, 8 e blocchi. Quando selezioni una dimensione T-shirt, il numero corrispondente di blocchi viene decrementato dalla tua quota.

Ad esempio, supponiamo che tu abbia un ambiente piccolo, che contiene 64 blocchi. All'interno di questo ambiente, hai configurato istanze del servizio che contengono due XXL, tre XL e 1 L per un totale di 60 blocchi utilizzati. Se selezioni una dimensione T-shirt media per una nuova sottoscrizione Liberty Core, potrebbe essere visualizzato un messaggio che indica la tua quota e il numero di blocchi ancora disponibili:

> **La tua quota di memoria a singolo tenant per questo servizio è di 64 blocchi. Compresa la tua configurazione corrente, hai 2 blocchi rimanenti. Per aumentare la tua quota di memoria, contatta il settore Vendite IBM.**


## Ambiente di rete privata
{: #private_network}

Dopo il provisioning di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment, puoi scaricare le tue credenziali VPN e stabilire una connessione OpenVPN. Per ulteriori informazioni, vedi i seguenti link:

* [Accesso VPN](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#vpnAccess){: new_window}
* [Configurazione di OpenVPN](https://console.bluemix.net/docs/services/ApplicationServeronCloud/systemAccess.html#setup_openvpn){: new_window}

## Gestione del tuo ambiente a singolo tenant
{: #manageSTE}

Per aggiungere ulteriore capacità al tuo WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment esistente o per ordinare capacità in un altro datacenter, contatta i call center (in Nord America), il tuo rappresentante IBM locale o il tuo Business Partner IBM. Per identificare il rappresentante o il partner, chiama il numero 800-426-4968. Per ulteriori informazioni, contatta i call center (in Nord America). Telefono: 800-IBM-CALL (426-2255) Fax: 800-2IBM-FAX (242-6329).


## Supporto del tuo ambiente a singolo tenant
{: #supportingSTE}

Se riscontri dei problemi, puoi ricevere assistenza aprendo un ticket di supporto come definito nella pagina [Richiesta di assistenza clienti](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window}.
