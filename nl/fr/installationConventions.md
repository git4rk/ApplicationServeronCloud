---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Conventions d'installation
{: #installation_conventions}

## Conseils relatifs à l'administration
{: admin_tips}

Quand vous administrez votre environnement {{site.data.keyword.appserver_full}} et que vous avez besoin de déterminer l'utilisateur dont vous devez vous servir, il est important de bien comprendre les concepts suivants :

 * Vous pouvez appliquer la maintenance en utilisant [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window}, qui se trouve dans le répertoire `/home/virtuser/IBM/Installation Manager`. Etant donné que les fichiers binaires sous-jacents sont installés en tant que `virtuser` (utilisateur administrateur virtuel, doté de droits limités), prenez soin d'installer tous les groupes de correctifs et tous les correctifs temporaires en tant que `virtuser`.

 * Toutefois, quand vous démarrez et arrêtez des serveurs depuis la ligne de commande, veillez à utiliser `wsadmin`, l'ID d'administrateur WebSphere Administrative, et non `virtuser`.

## Conventions d'installation de la cellule
{: cell_installation_conventions}

Une cellule WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} est installée et configurée conformément à une structure de répertoire normalisée. La liste suivante répertorie quelques-uns des paramètres importants.  Pour la liste complète des paramètres, voir `/etc/virtualimage.properties`.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Conventions d'installation de la collectivité Liberty

Une collectivité Liberty est installée et configurée conformément à une structure de répertoire normalisée. La liste suivante répertorie quelques-uns des paramètres importants.  Pour la liste complète des paramètres, voir `/etc/virtualimage.properties`.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
