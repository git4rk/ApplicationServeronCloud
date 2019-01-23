---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Ultimi aggiornamenti
{: #latest_updates}

Un elenco degli aggiornamenti più recenti al servizio.

## 16 gennaio 2019: URL endpoint API aggiornati per l'implementazione dell'API REST

Il prefisso della regione per Dallas è stato modificato da `ng` a `us-south`. Gli altri prefissi di regione non hanno subito variazioni. Gli URL endpoint API REST sono stati modificati da `https://wasaas-broker.<region>.bluemix.net/wasaas-broker/api` a `https://wasaas-broker.<region>.websphereappsvr.cloud.ibm.com/wasaas-broker/api`. Gli URL `bluemix.net` continueranno a essere supportati ma dovresti modificare gli URL endpoint API REST per utilizzare `websphereappsvr.cloud.ibm.com` se utilizzi le API REST per gestire le tue istanze del servizio.

Per ulteriori informazioni sugli URL endpoint API REST, vedi [Accesso al sistema](systemAccess.html#system_access).

## 14 dicembre 2018: WebSphere Application Server aggiornato in {{site.data.keyword.Bluemix_notm}}
* Il fix pack 9.0.0.10 di Traditional WebSphere Application Server è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 9.0.0.10, per il provisioning sono disponibili anche altri fix pack di Traditional WebSphere Application Server, come 9.0.0.9, 8.5.5.14 e 8.5.5.13.
* La versione del fix pack 18.0.0.4 di WebSphere Application Server Liberty è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 18.0.0.4, è disponibile per il provisioning la versione del fix pack 18.0.0.3 di WebSphere Application Server Liberty.
* Manutenzione dei servizi vari integrata.

## 24 ottobre 2018: la fatturazione BYOL (bring-your-own-license) è ora disponibile per ambienti a singolo tenant e contratto di riserva

Se hai delle licenze WebSphere Application Server esistenti, puoi ora utilizzarle nei tuoi ambienti a singolo tenant o contratto di riserva. Gli ambienti con la fatturazione BYOL (bring-your-own-license) offrono gli stessi vantaggi degli ambienti a singolo tenant o contratto di riserva ma vengono fatturati a un tasso ridotto. Per utilizzare le licenze BYOL (bring-your-own license), [contatta il settore vendite IBM](reportingIssues.html#contacting-sales).

## 22 agosto 2018: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Il fix pack 8.5.5.14 di Traditional WebSphere Application Server è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 8.5.5.14, per il provisioning sono disponibili anche altri fix pack di Traditional WebSphere Application Server, come 9.0.0.8, 9.0.0.7 e 8.5.5.13.
* Manutenzione dei servizi vari integrata.

## 16 luglio 2018: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* La versione del fix pack 9.0.0.8 di Traditional WebSphere Application Server è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 9.0.0.8, per il provisioning sono disponibili anche altre versioni del fix pack di Traditional WebSphere Application Server, come 9.0.0.7, 8.5.5.13 e 8.5.5.12.
* La versione del fix pack 18.0.0.2 di WebSphere Application Server Liberty è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 18.0.0.2, per il provisioning è disponibile la versione del fix pack 18.0.0.1 di WebSphere Application Server Liberty.
* Sono state risolte [diverse vulnerabilità di sicurezza](https://www-01.ibm.com/support/docview.wss?uid=ibm10717691){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=ibm10718297){: new_window} in IBM SDK Java Technology Edition che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.

## 13 giugno 2018: è ora disponibile la fatturazione del contratto di riserva

Con la fatturazione del contratto di riserva, acquisti una sottoscrizione mensile prepagata che garantisce l'accesso a blocchi di risorse computazionali riservate fisicamente. Questi blocchi di servizio sono riservati per il tuo uso esclusivo e non possono essere considerati come capacità disponibile per gli altri utenti di {{site.data.keyword.appserver_full}}. Puoi utilizzare le ore del blocco di servizio in qualsiasi modo tu scelga per tutto il mese, con eventuali eccedenze da addebitare in base al tipico modello di sottoscrizione di pagamento a consumo.

Per ulteriori informazioni sulla fatturazione del contratto di riserva, vedi [Opzioni di fatturazione](index.html#billing-options).

## 30 marzo 2018: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* La versione del fix pack 9.0.0.7 di Traditional WebSphere Application Server è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 9.0.0.7, per il provisioning sono disponibili anche altre versioni del fix pack di Traditional WebSphere Application Server, come 9.0.0.6, 8.5.5.13 e 8.5.5.12.
* La versione del fix pack 18.0.0.1 di WebSphere Application Server Liberty è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 18.0.0.1, è disponibile per il provisioning la versione del fix pack 17.0.0.4 di WebSphere Application Server Liberty.
* Sono state risolte [diverse vulnerabilità di sicurezza]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Vulnerabilità multiple nell'SDK Java IBM®
  * Una vulnerabilità in cui IBM WebSphere Application Server potrebbe fornire una sicurezza più debole del previsto per la Console di gestione.
  * Una vulnerabilità in cui le installazioni di IBM WebSphere Application Server che utilizzano Form Login potrebbero consentire a un aggressore in remoto di effettuare attacchi di spoofing.
  * Una vulnerabilità in cui IBM WebSphere Application Server potrebbe consentire a un aggressore locale di ottenere informazioni sensibili, causata da una gestione impropria delle richieste dell'applicazione, che potrebbe consentire l'accesso non autorizzato alla lettura di un file.
  * Una vulnerabilità in cui Apache Commons FileUpload, come utilizzato in diversi prodotti, potrebbe consentire a aggressore in remoto di eseguire codice arbitrario sul sistema, causata dalla deserializzazione di dati non attendibili nella classe DiskFileItem della libreria FileUpload. Un aggressore in remoto può sfruttare questa vulnerabilità per eseguire codice arbitrario nel contesto del processo corrente.
  * Una vulnerabilità in cui le CPU Intel Haswell Xeon, AMD PRO e ARM Cortex A57 potrebbero consentire a un aggressore autenticato locale di ottenere informazioni sensibili, causata da un ignoramento del controllo dei limiti nella funzione di esecuzione dell'istruzione di branch speculativa della CPU. Effettuando attacchi mirati al canale sul lato cache, un aggressore potrebbe sfruttare questa vulnerabilità per attraversare il limite di chiamate di sistema e leggere i dati dalla memoria virtuale della CPU.
* Manutenzione dei servizi vari integrata.

## 8 gennaio 2018: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* La versione del fix pack 9.0.0.6 di Traditional WebSphere Application Server è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 9.0.0.6, per il provisioning sono disponibili anche altre versioni del fix pack di Traditional WebSphere Application Server, come 9.0.0.5, 8.5.5.12 e 8.5.5.11.
* La versione del fix pack 17.0.0.4 di WebSphere Application Server Liberty è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 17.0.0.4, è disponibile per il provisioning la versione del fix pack 17.0.0.3 di WebSphere Application Server Liberty.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità in cui OpenSAML potrebbe consentire a un aggressore autenticato in remoto di ottenere informazioni sensibili, causata da un errore durante l'analisi delle entità XML.
  * Una vulnerabilità in cui Apache HTTP Server potrebbe consentire a un aggressore in remoto di ottenere informazioni sensibili, causata da un errore nel metodo HTTP OPTIONS denominato Optionsbleed.
  * Una vulnerabilità in cui Apache Portable Runtime Utility (APR-util) è vulnerabile a un DoS (Denial of Service), causata della mancata convalida dell'integrità dei file di database SDBM utilizzati dalle funzioni apr_sdbm*().
* Manutenzione dei servizi vari integrata.

## 21 dicembre 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Aggiunta della funzione di migrazione di WebSphere Application Server in IBM Cloud a Dallas, Londra e Sydney. Questa funzione fornisce una migrazione end-to-end completa dagli ambienti in loco della v7, v8 o v8.5.5 esistenti agli ambienti della v9 in IBM Cloud. Per ulteriori informazioni, vedi [WebSphere Configuration Migration Tool for IBM Cloud](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud).
* Manutenzione dei servizi vari integrata.

## 27 ottobre 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* È stata aggiunta la possibilità di fornire un livello di fix pack precedente [(n-1)](maintenanceAndUpdates.html#maintenance-strategy){: new_window} attraverso la scheda Service Profile del dashboard del servizio {{site.data.keyword.Bluemix_notm}} o tramite l'API REST.
* La versione del fix pack 9.0.0.5 di Traditional WebSphere Application Server è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 9.0.0.5, per il provisioning sono disponibili anche altre versioni del fix pack di Traditional WebSphere Application Server, come 9.0.0.4, 8.5.5.12 e 8.5.5.11.
* La versione del fix pack 17.0.0.3 di WebSphere Application Server Liberty è ora disponibile quando esegui il provisioning di una nuova istanza del servizio. Oltre alla 17.0.0.3, è disponibile per il provisioning la versione del fix pack 17.0.0.2 di WebSphere Application Server Liberty.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità in cui IBM WebSphere Application Server potrebbe creare file utilizzando le autorizzazioni predefinite invece delle autorizzazioni personalizzate quando vengono utilizzati gli script di avvio personalizzati.
  * Una vulnerabilità in cui il server proxy o il router on-demand (ODR) di IBM WebSphere Application Server potrebbe consentire a un aggressore locale di ottenere informazioni sensibili, causata da dati obsoleti che vengono memorizzati nella cache e quindi pubblicati.
  * Una vulnerabilità in cui IBM WebSphere Application Server è vulnerabile agli script cross-site. Questa vulnerabilità consente agli utenti di incorporare codice JavaScript arbitrario nell'interfaccia utente web, alterando così la funzionalità prevista che potrebbe portare alla divulgazione delle credenziali all'interno di una sessione attendibile.
  * Una vulnerabilità in cui IBM WebSphere Application Server potrebbe fornire una sicurezza più debole del previsto dopo l'utilizzo della Console di gestione per aggiornare le impostazioni dei bind di sicurezza dei servizi web.
  * Una vulnerabilità in cui IBM WebSphere Application Server versione 9.0.0.4 potrebbe fornire una sicurezza più debole del previsto dopo l'utilizzo del comando PasswordUtil per abilitare la crittografia della password AES.
  * Una vulnerabilità in cui Apache MyFaces potrebbe consentire a un aggressore in remoto di ottenere informazioni sensibili.
  * Una vulnerabilità in cui IBM WebSphere Application Server potrebbe consentire a un aggressore in remoto di ottenere informazioni sensibili, causata da una gestione degli errori non corretta da parte di MyFaces in JSF.
* Manutenzione dei servizi vari integrata.

## 30 agosto 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.

## 30 giugno 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che il fix pack 8.5.5.12 o 9.0.0.4 venga installato con le nuove istanze di Traditional WebSphere Application Server.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che il fix pack 17.0.0.2 venga installato con le nuove istanze di WebSphere Application Server Liberty (piani Core e ND).
* È stata aggiunta una funzione di [Gestione della configurazione VPN avanzata](networkEnvironment.html#advancedVPN){: new_window} che puoi utilizzare per creare e gestire più configurazioni VPN nelle regioni di Londra e Sydney.
* Sono stati aggiunti miglioramenti alla funzione di [Accesso Internet pubblico](networkEnvironment.html#publicInternetAccess){: new_window} che consente ai clienti di gestire meglio il loro indirizzo IP pubblico.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window} in IBM SDK Java Technology Edition che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità non specificata per il componente AWT di Java SE che potrebbe consentire a un aggressore non autenticato di assumere il controllo del sistema.
  * Una vulnerabilità non specificata per il componente JCE di Java SE che potrebbe consentire a un aggressore non autenticato di assumere il controllo del sistema.
  * Una vulnerabilità non specificata per il componente JAXP di Java SE che potrebbe consentire a un aggressore non autenticato di causare un attacco DoS (Denial of Service), comportando un alto impatto sulla disponibilità tramite vettori di attacco sconosciuti.
  * Una vulnerabilità non specificata per il componente di rete di Java SE che potrebbe consentire a un aggressore non autenticato di causare un basso impatto sulla riservatezza, un basso impatto sull'integrità e nessun impatto sulla disponibilità.
  * Una vulnerabilità non specificata per il componente di rete di Java SE che potrebbe consentire a un aggressore non autenticato di causare nessun impatto sulla riservatezza, un basso impatto sull'integrità e nessun impatto sulla disponibilità.
  * Una vulnerabilità non specificata per il componente di sicurezza di Java SE che potrebbe consentire a un aggressore non autenticato di causare nessun impatto sulla riservatezza, un basso impatto sull'integrità e nessun impatto sulla disponibilità.
  * Una vulnerabilità a un errore XML XXE (XML Entity Injection) durante l'elaborazione dei dati XML. Un aggressore in remoto può sfruttare questa vulnerabilità per esporre informazioni altamente sensibili o consumare risorse di memoria.
  * Un problema in cui zlib è vulnerabile a un DoS (Denial of Service), causato da un aritmetico del puntatore fuori limite in inftrees.c.
  * Un problema in cui zlib è vulnerabile a un DoS (Denial of Service), causato da uno spostamento a sinistra non definito di un numero negativo.
  * Un problema in cui zlib è vulnerabile a un DoS (Denial of Service), causato da un puntatore fuori limite big-endian.

## 25 maggio 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.
* È stata aggiunta una funzione di [Gestione della configurazione VPN avanzata](networkEnvironment.html#advancedVPN){: new_window} che puoi utilizzare per creare e gestire più configurazioni VPN nella regione di Francoforte.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che JDK 8 venga installato con tutte le nuove istanze del servizio.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una potenziale vulnerabilità di sicurezza con l'adattatore di risorse JCA MQ di WebSphere Application Server.
  * Una vulnerabilità non specificata per il componente Librerie che potrebbe consentire a un aggressore in remoto di ottenere informazioni sensibili, comportando un alto impatto sulla riservatezza tramite vettori di attacco sconosciuti.

## 21 aprile 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità in cui WebSphere Application Server configurato con OpenID Connect (OIDC) Trust Association Interceptor (TAI) potrebbe consentire a un utente di ottenere privilegi elevati sul sistema.
  * Una vulnerabilità in cui WebSphere Application Server potrebbe fornire una sicurezza più debole del previsto. Un aggressore in remoto potrebbe sfruttare questa debolezza per ottenere informazioni sensibili e l'accesso non autorizzato alla console di gestione.
  * Un problema in cui WebSphere Application Server è vulnerabile a Cross-Site Request Forgery che potrebbe consentire a un aggressore di eseguire azioni dannose e non autorizzate trasmesse da un utente considerato attendibile dal sito web.


## 15 marzo 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che il fix pack 8.5.5.11 o 9.0.0.3 venga installato con le nuove istanze di Traditional WebSphere Application Server.
* Sono state risolte [diverse vulnerabilità di sicurezza](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità non specificata per il componente Librerie che ha un alto impatto sull'integrità e nessun impatto sulla riservatezza e sulla disponibilità.
  * Una vulnerabilità non specificata per il componente Librerie che potrebbe consentire a un aggressore in remoto di ottenere informazioni sensibili, comportando un alto impatto sulla riservatezza tramite vettori di attacco sconosciuti.
  * Una vulnerabilità non specificata per il componente Librerie che potrebbe consentire a un aggressore in remoto di causare un attacco DoS (Denial of Service), comportando un basso impatto sulla disponibilità tramite vettori di attacco sconosciuti.
  * Una vulnerabilità in OpenSSL può consentire a un aggressore in remoto di ottenere informazioni sensibili, causata da un errore nella crittografia DES/3DES, utilizzata come parte del protocollo SSL/TLS.
  * Una vulnerabilità che consente agli utenti di incorporare codice JavaScript arbitrario nell'interfaccia utente Web alterando così la funzionalità desiderata che potrebbe portare a divulgare le credenziali in una sessione attendibile.
  * Una vulnerabilità in Apache HTTPD per gli attacchi di suddivisione della risposta HTTP, causata da una convalida impropria dell'input fornito dall'utente.
  * Una vulnerabilità in Samba che potrebbe consentire a un aggressore autenticato in remoto di ottenere privilegi elevati sul sistema, causata dall'errore di gestione del checksum PAC.
  * Una vulnerabilità in Samba che potrebbe consentire a un aggressore autenticato in remoto di ottenere privilegi elevati sul sistema, causata dall'inoltro di un TGT (Ticket Granting Ticket) a un altro servizio quando utilizzi l'autenticazione Kerberos.
  * Una vulnerabilità in Samba in un overflow di buffer basato su heap, causata da un problema di integer wrap nella funzione ndr_pull_dnsp_name().


## 10 febbraio 2017: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che il fix pack 8.5.5.11 o 9.0.0.2 venga installato con le nuove istanze di Traditional WebSphere Application Server.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che il fix pack 16.0.0.4 venga installato con le nuove istanze di WebSphere Application Server Liberty (piani Core e ND).
* Sono state risolte [diverse vulnerabilità di sicurezza](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità a DoS (Denial of Service), causata dall'esecuzione di oggetti serializzati provenienti fonti non attendibili provocando così il consumo di risorse.
  * L'utilizzo di richieste SOAP con formato errato, che potrebbe consentire a un aggressore remoto di ottenere informazioni sensibili.


## 16 dicembre 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Manutenzione dei servizi vari integrata.
* Sono state risolte [diverse vulnerabilità di sicurezza](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window} in IBM SDK Java Technology Edition che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità non specificata in Oracle Java SE e Java SE Embedded correlata al componente Hotspot che ha un alto impatto sulla riservatezza, un alto impatto sull'integrità e un alto impatto sulla disponibilità.
  * Una vulnerabilità non specificata in Oracle Java SE e Java SE Embedded correlata al componente Rete che potrebbe consentire a un aggressore remoto di ottenere informazioni sensibili comportando un alto impatto sulla riservatezza tramite vettori di attacco sconosciuti.
  *  Una vulnerabilità cross-site scripting in IBM WebSphere Application Server che consente agli utenti di incorporare codice JavaScript arbitrario nell'interfaccia utente Web. Il codice può, potenzialmente, alterare la funzionalità prevista, portando a divulgare le credenziali in una sessione attendibile.


## 8 novembre 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Aggiunta la capacità per i clienti di richiedere un indirizzo [IP pubblico](networkEnvironment.html#networkEnvironment) per le loro VM di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window} che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità in IBM WebSphere Application Server che può consentire ad aggressori in remoto di eseguire il codice Java arbitrario con un oggetto serializzato da origini non attendibili.
  * Una vulnerabilità DoS (Denial of Service) causata da una lettura non compresa nell'intervallo nella funzione TS_OBJ_print_bio. Un aggressore in remoto può avvalersi di questa vulnerabilità utilizzando un file di data/ora creato appositamente per causare l'arresto anomalo dell'applicazione.
  * Una vulnerabilità potenziale in OpenSSL che può consentire a un aggressore in remoto di ottenere informazioni sensibili, causata da un errore nel Triple-DES nella crittografia a blocchi a 64-bit, utilizzato come parte del protocollo SSL/TLS. Acquisendo una grande quantità di traffico crittografato tra il server e il client SSL/TLS, un aggressore in remoto in grado di effettuare un attacco MiTM (Man-in-the-Middle) può sfruttare questa vulnerabilità per recuperare i dati di testo non crittografato e ottenere informazioni sensibili. Questa vulnerabilità è conosciuta come attacco SWEET32 Birthday.
  * OpenSSL è vulnerabile a DoS (Denial of Service). Richiedendo ripetutamente la rinegoziazione, un aggressore autenticato in remoto potrebbe inviare un'estensione della richiesta dello stato OCSP eccessivamente grande per consumare tutte le risorse di memoria disponibili.
  * OpenSSL è vulnerabile a DoS (Denial of Service), causato da un overflow di numeri interi nella funzione MDC2_Update. Utilizzando dei vettori di attacco sconosciuti, un aggressore in remoto può avvalersi di questa vulnerabilità per attivare una scrittura non compresa nell'intervallo e causare l'arresto anomalo dell'applicazione.
  * Una vulnerabilità potenziale in OpenSSL che consente a un aggressore in remoto di ottenere informazioni sensibili, causata da un errore nell'implementazione DSA che consente l'aggiunta di un percorso di codice dell'ora non costante per alcune operazioni. Un aggressore in remoto può avvalersi di questa vulnerabilità utilizzando un attacco di timing nella cache per recuperare la chiave DSA privata.
  * OpenSSL è vulnerabile a DoS (Denial of Service), causato dalla mancanza dei controlli di lunghezza del messaggio durante l'analisi dei certificati. Un aggressore autenticato in remoto può avvalersi di questa vulnerabilità per attivare una lettura compresa nell'intervallo e causare un attacco Denial of Service.

## 19 settembre 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che le nuove istanze di WebSphere Application Server Liberty (piani Core e ND) utilizzino il fix pack 16.0.0.3.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window} che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità in IBM WebSphere Application Server Liberty che può consentire ad aggressori in remoto di effettuare attacchi di pishing.
  * Una vulnerabilità in IBM WebSphere Application Server Liberty di XSS (Cross-Site Scripting) nei client OpenID Connect.
  * Una vulnerabilità potenziale in IBM WebSphere Application Server Liberty che può consentire ad aggressori in remoto di ottenere informazioni sensibili causata dalla gestione non corretta delle eccezioni quando una pagina dell'errore predefinita non esiste.
  * Un vulnerabilità in Apache Tomcat per un DoS (Denial of Service), causata da un errore nel componente Apache Commons FileUpload.
  * Una vulnerabilità in IBM WebSphere Application Server e IBM WebSphere Application Server Liberty che può consentire ad aggressori in remoto di ottenere informazioni sensibili, causata dalla gestione non corretta delle risposte in alcune condizioni.
  * Una vulnerabilità non specificata per il componente di rete che non ha un impatto di confidenzialità, di bassa integrazione e nessuna disponibilità.

## 17 settembre 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}  da 8.5.5.9 a 8.5.5.10
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window} che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Le vulnerabilità Apache Struts che riguardano WebSphere Application Server e la console di gestione WebSphere Application Server Hypervisor Edition.
  * Una vulnerabilità DoS (Denial of Service) potenziale con IBM WebSphere Application Server quando utilizzi i servizi SIP.
  * Le vulnerabilità server che potevano riguardare il IBM HTTP Server utilizzato da WebSphere Application Server.
  * Una vulnerabilità che consente il reindirizzamento del traffico HTTP con le applicazioni CGI che può influenzare il IBM HTTP Server (IHS). Questa vulnerabilità è conosciuta come "HTTPOXY".
  * Una vulnerabilità di divulgazione delle informazioni in IBM WebSphere Application Server.
  * Una vulnerabilità di sicurezza di bypass potenziale in IBM WebSphere Application Server che si verifica solo negli ambienti con la proprietà personalizzata di contenitore `HttpSessionIdReuse` abilitata.


## 24 giugno 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Aggiunta la possibilità per i clienti di scegliere tra la V8.5 e la V9.0 quando creano una nuova istanza _Traditional ND_ o _Traditional WebSphere_.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} in modo che le nuove istanze di WebSphere Application Server Liberty (piani Core e ND) utilizzino il fix pack 16.0.0.2. 16.0.0.2 è il fix pack successivo a 8.5.5.9. Come parte di 16.0.0.2, tutte le funzioni facoltative intitolate Liberty supportate per questi piani sono installate per impostazione predefinita.
* Sono state risolte [diverse vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window} che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, tra cui:
  * Una vulnerabilità XML External Entity Injection (XXE) in Apache Standard Taglibs che riguardava IBM WebSphere Application Server.
  * Una sicurezza potenziale più debole del previsto per la funzione WebSphere Application Server Liberty profile API Discovery e della documentazione Swagger.
  * Una vulnerabilità di divulgazione delle informazioni potenziale nel Admin Center per IBM WebSphere Application Server Liberty.
  * Una vulnerabilità di suddivisione della risposta HTTP in IBM WebSphere Application Server.
  * Le vulnerabilità OpenSSL divulgate il 3 maggio 2016 dal progetto OpenSSL.

## 13 giugno 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Aggiunta la possibilità per i clienti di creare, fornire, gestire ed eliminare istanze della macchina virtuale attraverso la creazione di un'applicazione o script che utilizza le API RESTful di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.
* Aggiunta la funzione che consente a un cliente di avere un numero fisso di istanze ARRESTATE con non più di 10 indirizzi IP o 64 GB di memoria. Ai clienti vengono ora addebitate le istanze accumulate nello stato ARRESTATO a un tasso ridotto del 5%.

## 26 aprile 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Sono state risolte [potenziali vulnerabilità di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window} in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} con FIPS 140-2 abilitato e altre vulnerabilità in Samba - incluso Badlock.
* Manutenzione dei servizi vari integrata.

## 15 aprile 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} da 8.5.5.8 a 8.5.5.9
* È stata risolta una vulnerabilità [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window} in Liberty for Java per {{site.data.keyword.Bluemix_notm}} che influiva sui clienti che utilizzano il client OpenID Connect (OIDC).
* Manutenzione dei servizi vari integrata.

## 19 febbraio 2016: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Aggiunta un'opzione per i clienti con applicazioni intensive di memoria per "dimensionare correttamente" il loro ambiente con grandi macchine virtuali. I clienti possono selezionare la dimensione della risorsa specifica di un determinato componente di WebSphere Application Server o un singolo sistema fino a 32 GB RAM di macchine virtuali.
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} da 8.5.5.7 a 8.5.5.8
* Sono state risolte diverse vulnerabilità in IBM SDK Java Technology Edition che influivano su WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} a cui si fa comunemente riferimento come [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}.
* È stata risolta una vulnerabilità [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window} che influenzava l'output del provider OAuth dei clienti.
* Manutenzione dei servizi vari integrata.

## 11 dicembre 2015: aggiornamento di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* È stato modificato il nome del prodotto ufficiale da IBM Application Server on Cloud in {{site.data.keyword.Bluemix_notm}} a IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Sono state aggiunte delle nuove funzionalità al piano di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment. Il piano consiste in un ambiente di cella WebSphere Application Server Network Deployment con due o più macchine virtuali. Queste nuove funzionalità consentono agli utenti di impostare un ambiente in cluster per l'elevata disponibilità, il failover e la scalabilità.
* Sono state aggiunte delle nuove funzionalità al piano di WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Liberty Core. Il piano include l'utilizzo di un collettivo Liberty, che è un dominio amministrativo per un gruppo di profili Liberty (server) e consiste in due o più macchine virtuali
* È stato aggiornato WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} da 8.5.5.6 a 8.5.5.7
* È stata risolta una [vulnerabilità di Apache Commons Collections](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window} per
gestire la deserializzazione di oggetti Java.
* È stata risolta una vulnerabilità che potrebbe consentire un [attacco HTTP
Response Splitting](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}.
* Manutenzione dei servizi vari integrata.

## 15 ottobre 2015: Application Server on Cloud aggiornato
* Sono stati aggiunti i seguenti due nuovi piani:
  * [WebSphere Application Server Traditional V9 Beta](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* Manutenzione di servizio varia
