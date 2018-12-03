---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Convenzioni di installazione
{: #installation_conventions}

## Consigli di amministrazione
{: admin_tips}

Quando amministri il tuo ambiente {{site.data.keyword.appserver_full}} e hai bisogno di determinare quale utente utilizzare, è importante comprendere i seguenti concetti:

 * La manutenzione può essere applicata utilizzando [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window}, è installato nella directory `/home/virtuser/IBM/Installation Manager`. Poiché i file binari sottostanti sono installati come `virtuser`, un utente virtuale amministrativo limitato, assicurati che tutti i fix pack e tutte le correzioni temporanee vengano installati come `virtuser`.

 * Tuttavia, quando avvii e arresti i server dalla riga di comando, assicurati di utilizzare `wsadmin`, ossia l'ID amministrativo WebSphere, e non `virtuser`.

## Convenzioni di installazione della cella
{: cell_installation_conventions}

Una cella WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} viene installata e configurata rispettando una struttura di directory standardizzata. Il seguente elenco annota alcune importanti impostazioni.  Consulta `/etc/virtualimage.properties` per un elenco completo di impostazioni. 

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Convenzioni di installazione del collettivo Liberty

Un collettivo Liberty viene installato e configurato rispettando una struttura di directory standardizzata. Il seguente elenco annota alcune importanti impostazioni.  Consulta `/etc/virtualimage.properties` per un elenco completo di impostazioni. 

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
