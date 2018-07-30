---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-06"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Ambiente di rete
{: #networkEnvironment}

Dopo aver eseguito il provisioning della tua istanza del servizio {{site.data.keyword.appserver_full}}, puoi accedere alla tua VM in diversi modi. Puoi collegarti tramite una VPN sicura per ottenere l'accesso SSH, alla console di gestione WebSphere tradizionale e all'applicazione per la tua VM. Puoi anche collegare la tua VM a internet con un indirizzo IP pubblico.

Il seguente diagramma illustra questi percorsi di rete:

Figura 1. Vista client di una rete a più tenant con IP pubblico

![Figura 1. Vista client di una rete a più tenant con IP pubblico](images/wasaas_multi_tenantPublicIP.gif)

## Accesso VPN
{: #vpnAccess}

Dopo aver eseguito il provisioning di un'istanza del servizio WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} dal dashboard del servizio nell'interfaccia utente {{site.data.keyword.Bluemix_notm}}, puoi stabilire una connessione OpenVPN espandendo il menu a discesa e scaricando la tua configurazione VPN utilizzando il pulsante **Download VPN Configuration**. La configurazione VPN contiene un file **.ovpn** e i certificati che vengono utilizzati per l'autenticazione con il server OpenVPN. Una volta stabilita la connessione OpenVPN, puoi accedere alla tua VM tramite SSH. Puoi anche accedere al Liberty Admin Center, alla console di gestione WebSphere tradizionale e alle applicazioni.

La configurazione VPN è applicabile alla tua organizzazione e regione. È valida per un anno dal momento in cui viene creata. È possibile stabilire contemporaneamente più connessioni client OpenVPN utilizzando la stessa configurazione VPN.

**Nota:** la configurazione VPN è valida solo se la tua organizzazione contiene sottoscrizioni **attive**. Quando viene eliminata l'ultima sottoscrizione per un'organizzazione, tutte le configurazioni VPN per l'organizzazione vengono sospese. Le configurazioni VPN non scadute vengono riattivate automaticamente quando si attiva un nuova sottoscrizione.

## Gestione della configurazione VPN avanzata
{: #advancedVPN}

Nella maggior parte dei casi, ti serve una sola configurazione VPN che puoi scaricare utilizzando il pulsante **Download VPN Configuration**. Tuttavia, la pagina di gestione VPN avanzata, a cui si accede utilizzando il pulsante **Advanced VPN Management** dal dashboard del servizio nell'interfaccia utente {{site.data.keyword.Bluemix_notm}}, ti consente di creare e gestire più configurazioni VPN. Avere più configurazioni potrebbe essere utile per passare senza problemi a una nuova configurazione VPN quando quella vecchia sta per scadere. Puoi anche richiedere più configurazioni VPN per gestire l'accesso alle tue VM con diversi individui o team nella tua organizzazione.   

**Nota:** ti è consentito un **massimo** di 10 configurazioni VPN attive per la tua organizzazione in qualsiasi momento.

Se le tue configurazioni VPN sono compromesse o scadute, puoi revocare la configurazione VPN utilizzando la pagina di gestione VPN avanzata. Inoltre, da una prospettiva di controllo, puoi visualizzare una cronologia di tutte le attività di gestione VPN e scaricare le configurazioni VPN attive create in precedenza dalla pagina di gestione VPN avanzata.

Tutte le funzioni disponibili nel dashboard del servizio dell'interfaccia utente {{site.data.keyword.Bluemix_notm}} possono anche essere controllate da script utilizzando le nostre API REST. Per ulteriori informazioni, vedi la [Documentazione API REST](https://wasaas-broker.ng.bluemix.net/wasaas-broker/api#/){: new_window} di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.


## Accesso Internet pubblico
{: #publicInternetAccess}

Facoltativamente, puoi gestire l'accesso a Internet pubblico dal dashboard del servizio nell'interfaccia utente {{site.data.keyword.Bluemix_notm}}. Puoi **richiedere** un indirizzo IP pubblico dal pool e **aprire** la connessione da Internet alla tua istanza del servizio WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}. Al contrario, puoi **chiudere** l'accesso dalla tua istanza del servizio a Internet e **restituire** l'indirizzo IP pubblico al pool.

Per **richiedere** un indirizzo IP pubblico e **aprire** una connessione, segui queste istruzioni:

1. Fai clic su **Manage Public IP Access** nel dashboard del servizio dell'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
2. Viene visualizzato l'indirizzo IP per il tuo host, ma non il tuo indirizzo IP pubblico. Fai clic su **Request Public IP Address**.

    **Nota:** ritorni al dashboard del servizio con un IP pubblico assegnato. Tuttavia, viene visualizzato il seguente messaggio:

    > **Access is currently closed. Click Manage Public IP to Open Access.**
3. Fai clic su **Manage Public IP Access** nel dashboard del servizio dell'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
4. Vengono visualizzati gli indirizzi IP per il tuo host e il tuo nuovo IP pubblico, ma l'accesso è chiuso. Fai clic su **Open Access**.

    **Nota:** ritorni al dashboard del servizio che visualizza il seguente messaggio:

    > **Access is currently open. Click Manage Public IP to Close Access.**

Per **chiudere** una connessione e **restituire** un indirizzo IP pubblico, segui le seguenti istruzioni:

1. Fai clic su **Manage Public IP Access** nel dashboard del servizio dell'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
2. Fai clic su **Close Access**.

    **Nota:** ritorni al dashboard del servizio che visualizza il seguente messaggio:

    > **Access is currently closed. Click Manage Public IP to Open Access.**
3. Fai clic su **Manage Public IP Access** nel dashboard del servizio dell'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
4. Fai clic su **Return Public IP Address**.

    **Nota:** ritorni al dashboard del servizio in cui viene visualizzato l'indirizzo IP del tuo host con il seguente messaggio:

    > **Returned Public IP.**

## Porte IP pubblico
{: #publicIPports}

Quando apri l'accesso al tuo IP pubblico, l'indirizzo IP viene associato alla tua VM e le porte 80 e 443 vengono aperte al gateway. Tuttavia, per impostazione predefinita, i server Liberty Core e WebSphere Base tradizionale non aprono le porte 80 e 443. Al contrario, le porte 80 e 443 sono aperte per impostazione predefinita su IBM HTTP Server. Pertanto, potresti dover configurare i tuoi server Liberty Core e WebSphere Base tradizionale per ascoltare il traffico dell'applicazione sulla porta 80/443 quando utilizzi un IP pubblico.
* Per configurare il tuo server Liberty Core, consulta [Configurare il server Liberty Core per l'accesso pubblico](networkEnvironment.html#configureLibertyForPublicAccess).
* Per configurare il tuo server WebSphere Base tradizionale, aggiungi una catena di trasporto del contenitore web in ascolto sulla porta 80/443 come descritto in [Configurazione delle catene di trasporto](http://www.ibm.com/support/knowledgecenter/SSEQTP_8.5.5//com.ibm.websphere.nd.doc/ae/trun_chain_transport.html){: new_window}.

**Prevenzione dei problemi:** Linux riserva le porte con un numero minore di 1024 per gli utenti privilegiati, come ad esempio **root**. Tuttavia, è prassi comune eseguire i server WebSphere Base tradizionali come utente **non root**. Pertanto, quando aggiungi una catena di trasporto del contenitore web, modifica la tua configurazione **iptables** come utente **root**. In particolare, reindirizza le porte limitate 80 e 443 a un'altra porta superiore a 1024, ad esempio 9080 e 9443. I seguenti comandi forniscono un esempio di questo processo:

```
-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 9080
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9080 -j ACCEPT

-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 9443
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
```

**Nota:** le modifiche a **iptables** sono effimere. Ad esempio, se il tuo guest viene riavviato o se il servizio **iptables** viene riavviato, le regole vengono automaticamente cancellate e reimpostate. Per salvare le regole in modo che siano persistenti quando viene avviato il servizio iptables o riavviato il guest, utilizza il seguente comando come utente **root**:

```
-bash-4.1# service iptables save
iptables: Saving firewall rules to /etc/sysconfig/iptables:[  OK  ]

bash-4.1# cat /etc/sysconfig/iptables
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*nat
:PREROUTING ACCEPT [0:0]
:POSTROUTING ACCEPT [23:1706]
:OUTPUT ACCEPT [23:1706]
-A PREROUTING -p tcp -m tcp --dport 80 -j REDIRECT --to-ports 9080
-A PREROUTING -p tcp -m tcp --dport 443 -j REDIRECT --to-ports 9443
COMMIT
# Completed on Wed May 31 19:44:11 2017
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*filter
:INPUT DROP [0:0]
:FORWARD DROP [0:0]
:OUTPUT DROP [0:0]
-A INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 9080 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 80 -j ACCEPT

```


**Nota:** le **iptables** vengono richiamate su richieste che transitano sull'interfaccia esterna del guest. Le richieste che transitano sul loopback locale (127.0.0.1) non vengono elaborate dalle **iptables**, pertanto i reindirizzamenti delle porte, come indicato in precedenza, non vengono richiamate sul loopback.

## Porte IP privato VPN
{: #privateIPports}

Collega il tuo indirizzo IP privato della VM tramite la connessione VPN. Liberty Admin Center (9080, 9443), la console di gestione WebSphere tradizionale (9060, 9043), SSH (22) e le porte diverse da 80/443 sono accessibili solo tramite la connessione VPN come rappresentato nella Figura 1. Consulta il Liberty Core di esempio **server.xml** e **ibm-web-bnd.xml** per i dettagli sulla separazione di Liberty Admin Center dalle tue porte dell'applicazione.

**Prevenzione dei problemi:** per i server Liberty Core e WebSphere Base tradizionale, le porte del firewall sono pre-configurate quando esegui il provisioning della tua VM. Tuttavia, per le configurazioni di Network Deployment in cui il Deployment manager o il Controller collettivo viene collocato con IBM HTTP Server, potresti dover aprire le porte nel firewall. Consulta [Porte firewall](systemAccess.html#firewall_ports) per i dettagli.

## Configurazione di un server Liberty Core per un accesso IP pubblico
{: #configureLibertyForPublicAccess}

Devi configurare Liberty Core per ascoltare il traffico dell'applicazione sulla porta 80/443 quando utilizzi l'IP pubblico.

Per impostazione predefinita, Liberty è configurato con il Liberty Admin Center e le applicazioni disponibili nell'host virtuale **default_host**, associato a **defaultHttpEndpoint** nella porta 9080 e 9443. Riconfigura il tuo server per separare il Liberty Admin Center dall'endpoint e dall'host virtuale dell'applicazione e rendili disponibili su porte diverse.

Il seguente frammento è un esempio di modifiche di configurazione server.xml:

```    
    <!-- open port 9080/9443 for incoming http connections -->
    <httpEndpoint id="defaultHttpEndpoint"
        host="*"
        httpPort="9080"
        httpsPort="9443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!-- define a new endpoint for public app traffic -->
    <httpEndpoint id="publicHttpEndpoint"
        host="*"
        httpPort="80"
        httpsPort="443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!–- restrict default_host to vpn so the Liberty Admin Center is not public -->
    <virtualHost id="default_host" allowFromEndpointRef="defaultHttpEndpoint">
      <hostAlias>*:9080</hostAlias>
      <hostAlias>*:9443</hostAlias>
    </virtualHost>

    <virtualHost id="external_host">
      <hostAlias>*:80</hostAlias>
      <hostAlias>*:443</hostAlias>
    </virtualHost>
```
{: codeblock}

Adesso associa la tua applicazione all'host virtuale **external_host** includendo il seguente frammento nel file **WEB-INF/ibm-web-bnd.xml** della tua applicazione:

```
    <?xml version="1.0" encoding="UTF-8"?>
    <web-bnd
        xmlns="http://websphere.ibm.com/xml/ns/javaee"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://websphere.ibm.com/xml/ns/javaee   
        http://websphere.ibm.com/xml/ns/javaee/ibm-web-bnd_1_0.xsd"
        version="1.0">

        <virtual-host name="external_host" />
    </web-bnd>
```
{: codeblock}

## Configurazione di DNS
{: #dnsConfig}

È importante notare che le VM di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} sono configurate con due resolver DNS. I resolver sono configurati nel file **/etc/resolv.conf** sulla VM. Il server DNS primario è un server non autorevole fornito dal servizio WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}. Il server DNS secondario è un server non autorevole fornito da {{site.data.keyword.Bluemix_notm}}.

Ti consigliamo di esaminare la configurazione DNS per vedere se soddisfa le tue esigenze. Puoi aggiornare il file **/etc/resolv.conf** per fare riferimento al server DNS di tua scelta se quelli forniti da IBM non soddisfano i tuoi requisiti.

**Nota:** le vecchie VM di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} potrebbero avere solo un server DNS primario configurato nel file **/etc/resolv.conf**. Se vuoi una soluzione ad alta disponibilità, puoi rilasciare la VM e fornirne una nuova o aggiornare il file **/etc/resolv.conf** per aggiungere un server DNS secondario. Questo può essere il tuo server DNS preferito o quello fornito da {{site.data.keyword.Bluemix_notm}} (10.0.80.11).


## Apertura delle porte per i nuovi server sui nodi personalizzati
{: #serversOnCustom}

Quando crei un server su un nodo personalizzato, le porte aggiuntive richieste dal server devono essere aperte sulle VM del Deployment Manager e del nodo personalizzato prima di avviare il server. Dopo aver creato il server, ma prima di avviarlo, apri le porte eseguendo lo script `openWASPorts.sh`:

 1. Accedi a ogni VM del Deployment Manager e del nodo personalizzato come utente root.
 1. Esegui lo script `/opt/IBM/WebSphere/AppServer/virtual/bin/openWASPorts.sh` per aprire le porte.
 
Dopo aver eseguito lo script, puoi avviare il server dalla console di gestione del Deployment Manager.
