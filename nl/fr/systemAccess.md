---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

keywords: rest api, access, dashboard, openvpn, vpn, ssh, openssh, command path, admin, manage server, console, firewall port, web server, plugin, plug-in, ssl

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Accès au système
{: #system_access}

Découvrez les méthodes de création et de gestion d'une instance de service et explorez les diverses façons d'accéder et de configurer l'accès à vos systèmes.
{: shortdesc}

## Utilisation de l'API REST dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
{: #restapi_usage}

Les instances dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} sont créées, provisionnées, gérées et supprimées de l'une des façons suivantes :

* Depuis le tableau de bord du service et le catalogue {{site.data.keyword.Bluemix_notm}}.
* A partir de la création d'une application ou d'un script utilisant des API RESTful.

En utilisant des API REST compatibles Swagger 2.0, les clients ont accès à la même fonction que celle fournie via le portail et le tableau de bord. Pour plus d'informations sur les ressources et API REST prises en charge, voir la documentation {{site.data.keyword.Bluemix_notm}} [WebSphere Application Server in IBM Cloud API](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window}. Pour un code exemple démontrant l'utilisation des API REST, téléchargez WebSphere Application Server hébergé par Git dans {{site.data.keyword.Bluemix_notm}} [WebSphere-in-IBM-Cloud/WebSphere-In-IBM-Cloud-API-Examples/REST API Samples](https://github.com/IBM-Cloud/WebSphere-in-IBM-Cloud/tree/master/WebSphere-In-IBM-Cloud-API-Examples){: new_window}.

**Remarque :** après création d'une instance de service, selon la taille standard qui est créée, votre service risque de ne pas être immédiatement prêt à être utilisé. Il est recommandé de faire une requête sur la zone **Statut** de l'élément JSON retourné pour déterminer l'état actuel de l'instance de service.

**Remarque :** l'URL **apiEndpoint** référencée dans les [exemples d'API REST ](https://github.com/IBM-Cloud/WebSphere-in-IBM-Cloud/tree/master/WebSphere-In-IBM-Cloud-API-Examples){: new_window} pointe sur la région Dallas. Si vous utilisez d'autres régions, assurez-vous que votre application se réfère à la bonne URL **apiEndpoint**.

*Tableau 1. Implémentation des URL de noeud final d'API pour l'implémentation d'API REST*

| **Nom de région** | **Préfixe de région** | **URL du noeud final d'API** |       
|:-------------:|:--------------:|:-------------:|
| Dallas | `us-south` | https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Londres | `eu-gb` | https://wasaas-broker.eu-gb.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Francfort | `eu-de` | https://wasaas-broker.eu-de.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Sydney | `au-syd` | https://wasaas-broker.au-syd.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |

## Tableau de bord du service
{: #service_dashboard}

Une fois votre instance de service créée, vous êtes ramené au tableau de bord du service. Vous pouvez revenir au tableau de bord du service à tout moment en cliquant sur l'icône du service dans le tableau de bord de votre organisation.
Depuis le tableau de bord du service, vous pouvez accéder aux éléments suivants :

* Un lien vers cette documentation
* Un lien permettant de télécharger le fichier de configuration OpenVPN
* La possibilité de démarrer et d'arrêter la machine virtuelle. La machine virtuelle est démarrée initialement
* Le nom d'hôte
* L'administrateur et le mot de passe de l'administrateur
* Une clé SSH privée
* Le nom et le mot de passe de l'administrateur WebSphere&reg;
* Les URL du centre d'administration et de la console d'administration


## Configuration d'openVPN pour les instances WebSphere Application Server dans {{site.data.keyword.Bluemix_notm}}
{: #setup_openvpn}

OpenVPN est requis pour accéder à toute machine virtuelle WebSphere Application Server dans {{site.data.keyword.Bluemix_notm}}. Il doit être installé et exécuté avec des privilèges d'administrateur.

### Configuration d'openVPN sous Windows

1. Téléchargez le programme d'installation Windows openVPN pour votre architecture système depuis le site Web openVPN :
  * Systèmes 64 bits : [openvpn-install-2.3.4-I001-x86_64.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-x86_64.exe){: new_window}
  * Systèmes 32 bits :  [openvpn-install-2.3.4-I001-i686.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-i686.exe){: new_window}
2. Prenez soin d'[effectuer l'exécution en tant qu'administrateur Windows](https://technet.microsoft.com/magazine/ff431742.aspx){: new_window} et vérifiez qu'openVPN est installé.
3. Téléchargez les fichiers de configuration VPN depuis le lien de téléchargement OpenVPN de l'instance WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, fourni dans le tableau de bord de service. Décompressez les quatre fichiers vers le répertoire `{répertoire_OpenVPN}\config`. Par exemple :

  ```  
  C:\Program Files\OpenVPN\Config
  ```

4. Lancez le programme client openVPN "OpenVPN GUI". Prenez soin de sélectionner **Exécuter en tant qu'administrateur Windows** lorsque vous lancez le programme. Sinon, il se peut que vous ne puissiez pas vous connecter.

### Configuration d'openVPN sous Linux

1. Pour installer openVPN, suivez les [instructions openVPN pour Linux](https://openvpn.net/index.php/access-server/docs/admin-guides/182-how-to-connect-to-access-server-with-linux-clients.html){: new_window}.

   Si vous devez télécharger et installer manuellement le gestionnaire de packages RPM, accédez à la [page de téléchargement d'openVPN unix/linux](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html){: new_window}. Vous aurez peut-être besoin de l'aide de votre administrateur Linux.
3. Téléchargez les fichiers de configuration VPN depuis le lien de téléchargement OpenVPN de l'instance WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, fourni dans le tableau de bord de service. Procédez à l'extraction des fichiers dans le répertoire à partir duquel vous prévoyez de démarrer le client openVPN. Les quatre fichiers doivent se trouver dans le même répertoire.
3. Démarrez le programme client openVPN. Ouvrez une fenêtre de terminal et accédez au répertoire contenant les fichiers de configuration. Exécutez la commande suivante en tant que root :

  ```
  openvpn --config vt-wasaas-wasaas.ovpn
  ```
  {: .codeblock}  

### Configuration d'openVPN sous Mac
1. Une méthode consiste à installer le logiciel open source [Tunnelblick](https://tunnelblick.net/){: new_window}.
2. Procédez à l'extraction des fichiers de configuration du réseau privé virtuel depuis le service WebSphere. Tunnelblick vous invite à entrer le mot de passe de l'administrateur pour Mac et ajoute la configuration à l'ensemble de réseaux privés virtuels que vous pouvez utiliser pour vous connecter.
3. Connectez-vous au réseau privé virtuel pour pouvoir accéder à votre machine virtuelle. Après votre premier accès, Tunnelblick met en cache la configuration pour que vous puissiez vous connecter depuis Tunnelblick. Vous pouvez placer une icône dans la barre de menu pour un accès facile


## Utilisation de SSH pour accéder aux machines virtuelles WebSphere Application in {{site.data.keyword.Bluemix_notm}}
{: #using_ssh}

Ces instructions supposent que vous utilisez OpenSSH comme client. OpenSSH est généralement disponible sur Linux ou dans Cygwin s'exécutant sous Windows. Il peut aussi être installé en vue de son exécution depuis une invite de commande Windows.

Pour vérifier l'installation d'OpenSSH, exécutez la commande suivante.
  ```
  ssh -V
  ```
  {: codeblock}

Le message suivant est un exemple de la réponse :
  ```
  OpenSSH_6.6p1, OpenSSL 1.0.1g 7 Apr 2014
  ```

Procédez comme suit pour configurer l'accès SSH à votre serveur WebSphere Application Server dans les machines virtuelles {{site.data.keyword.Bluemix_notm}}.

1. Examinez le message d'avertissement qui s'affiche la première fois que vous vous connectez : "L'authenticité de l'hôte x.x.x.x n'a pas pu être établie". Ce message est normal. A l'invite, sélectionnez Oui. La clé publique est à présent installée sur votre machine virtuelle pour l'utilisateur **virtuser**.
2. Connectez-vous à **virtuser** en utilisant la clé privée. Pour de meilleurs résultats, utilisez la méthode d'authentification par clé privée.
3. Copiez le contenu de la clé privée dans un fichier.
4. Connectez-vous via SSH en exécutant la commande suivante.

  ```
  ssh virtuser@169.53.246.xxx -i /path/privateKeyFileName
  ```
  {: codeblock}

5. Obtenez les droits d'accès sysadmin complets en basculant de l'utilisateur **virtuser** à l'utilisateur **root** via la commande suivante.

  ```
  sudo su root
  ```
  {: codeblock}

6. Si vous rencontrez des problèmes lors de l'accès au système avec la clé SSH privée, utilisez le mot de passe root fourni. Connectez-vous en tant que root en exécutant la commande suivante et soumettez le mot de passe :

  ```
  ssh root@169.53.246.x
  ```
  {: codeblock}

7. Que vous accédiez au système avec la clé ssh privée ou le mot de passe root, changez immédiatement le mot de passe root.
8. Pour simplifier vos commandes SSH, créez un fichier nommé `config` dans le répertoire `%HOME%/.ssh`. Par exemple :

   ```
   Host VM1
      Hostname 169.53.246.xxx
      User virtuser
      IdentityFile /path/privateKeyFileName
   ```
   {: codeblock}

9. Exécutez la commande suivante en tant que **virtuser**.

   ```
   ssh VM1
   ```
   {: codeblock}

## Chemins système
{: #system_paths}

* Les commandes Liberty peuvent être émises depuis `/opt/IBM/WebSphere/Liberty/bin`.
* L'emplacement du profil de serveur Liberty est `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1`.
* Les fichiers produit système du serveur WebSphere Application Server Traditional, qui sont partagés par tous les profils, se trouvent dans `/opt/IBM/WebSphere/AppServer/`.
* Les commandes du serveur WebSphere Application Server Traditional peuvent être émises depuis l'emplacement de profil par défaut dans `/opt/IBM/WebSphere/Profiles/Default<profile_type><profile_number>/bin`, où :
  * `<profile_type>` est une valeur de `AppSrv`, `Dmgr`, `Custom`, `AdminAgent`, `JobMgr` ou `SecureProxySrv`.
  * `<profile_number>` est un numéro séquentiel qui est utilisé pour créer un nom de profil unique.


## Gestion des serveurs depuis la ligne de commande
{: #start_servers}

**Evitez les problèmes :** quand vous gérez les serveurs WebSphere depuis la ligne de commande, veillez à utiliser **wsadmin**, l'ID d'administrateur WebSphere, et non **virtuser**. Quand vous gérez le serveur IHS depuis la ligne de commande, prenez soin de vous servir de **root**.

## Utilisation des liens vers le centre d'administration et vers la console d'administration
{: #console_links}

Lorsque vous cliquez sur le lien vers le centre d'administration ou la console d'administration, il se peut qu'un avertissement indiquant que la *connexion n'est pas sécurisée* s'affiche. Le message exact varie selon le navigateur, tout comme les étapes permettant de contourner ou d'éliminer l'avertissement.

Etant donné que vous utilisez des liens fournis par {{site.data.keyword.IBM}}, vous pouvez ignorer l'avertissement et vous connecter sans crainte. Votre navigateur peut proposer de stocker une exception de sécurité ; c'est la façon la plus facile d'éviter l'avertissement à l'avenir.

Vous pouvez aussi exporter le certificat de signataire entrant, puis l'importer dans votre navigateur en tant que certificat racine accrédité. Cette option nécessite que vous ajoutiez une entrée dans votre fichier *hosts* pour mapper l'adresse IP de la machine virtuelle au nom usuel de l'émetteur du certificat. Ce nom est au format suivant : `wl<pureapplication.ibmcloud.com`. Si vous utilisez le nom d'hôte à la place de l'adresse IP dans l'adresse URL, vous pouvez vous connecter correctement. Vous devez ensuite accéder au centre d'administration ou à la console d'administration avec ce nom d'hôte, au lieu de l'adresse IP dans l'adresse URL.

Enfin, les clients installent souvent leurs propres certificats racine pour les applications externes. Pour plus d'informations, voir la documentation [WebSphere Application Server](https://www.ibm.com/support/knowledgecenter/SSAW57_9.0.0/com.ibm.websphere.nd.multiplatform.doc/ae/tsec_securecomm.html){: new_window} ou [Liberty Core](https://www.ibm.com/support/knowledgecenter/SSD28V_9.0.0/com.ibm.websphere.wlp.core.doc/ae/twlp_sec_comm.html){: new_window} dans IBM Knowledge Center.

## Ports de pare-feu
{: #firewall_ports}

Il peut être nécessaire d'ouvrir des ports sur le pare-feu afin d'autoriser l'accès à des applications et des bases de données. Vous pouvez ouvrir les ports de pare-feu en utilisant le script `openFirewallPorts.sh`, que vous pouvez trouver aux emplacements suivants.
  * Sur chaque serveur WebSphere Application Server d'un noeud {{site.data.keyword.Bluemix_notm}}, le script `openFirewallPorts.sh` est présent dans le répertoire `WAS_HOME/virtual/bin`.
  * Sur chaque hôte de la collectivité Liberty, `openFirewallPorts.sh` se trouve dans le répertoire `WAS_HOME/virtual/bin`.

### Utilisation

Exécutez le script `openFirewallPorts.sh` en utilisant la syntaxe de commande suivante.

  ```
  openFirewallPorts.sh -ports <PORT>:<PROTOCOL>,... -persist true|false
  ```
  {: codeblock}

où :
* Port est un numéro de port
* PROTOCOL est TCP ou UDP
* `-persist` est `true` ou `false`

Vous pouvez spécifier plusieurs ports différents dans une liste, en les séparant par des virgules.

**Remarque **: Le port source (sport) et le port de destination (dport) du port ouvert sont tous deux ouverts dans les sections INPUT et OUTPUT du pare-feu. Vous devez exécuter ce script en tant que root en utilisant `sudo`. Vous pouvez aussi modifier iptables directement.

## Configuration du serveur Web
{: #configure_webserver}

Lorsque vous mettez à disposition une cellule ou une collectivité, vous recevez un environnement préconfiguré. Plus précisément, pour une cellule de déploiement de réseau traditionnel, vous recevez l'environnement suivant :

* Un gestionnaire de déploiement colocalisé avec IBM HTTP Server à des fins de développement et de tests.
* Un noeud personnalisé fédéré au gestionnaire de déploiement.
* Le gestionnaire de déploiement, le serveur IHS et l'agent de noeud tous initialement mis à disposition à l'état STARTED.

Si le serveur Web doit traiter toutes les requêtes des utilisateurs, vous devrez peut-être générer et diffuser le plug-in après le déploiement de votre application.

**Evitez les problèmes :** avant de générer et de propager le plug-in, assurez-vous que les tâches préalables suivantes sont terminées.

* Dans votre environnement Windows, Linux ou MAC local, assurez-vous que [openVPN](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#setup_openvpn) est configuré et démarré, et que vous êtes connecté à la région appropriée.
* A partir du serveur WebSphere Application Server dans le tableau de bord du service {{site.data.keyword.Bluemix_notm}}, cliquez sur **Ouvrir la console d'administration** et connectez-vous avec wsadmin et le mot de passe administrateur fourni dans le tableau de bord de service.
* Depuis la console d'administration, créez un serveur d'applications (***server1***, par exemple), car le gestionnaire de déploiement est fédéré avec un noeud personnalisé vide.
* Démarrez le serveur que vous avez créé.
* Pendant l'installation de l'application, assurez-vous que les modules de votre application sont mappés au serveur que vous venez de démarrer et au serveur Web (***webserver1***, par exemple).

Les étapes de haut niveau suivantes supposent que les tâches préalables sont terminées.

1. Dans la console d'administration, générez le plug-in à partir de l'option Environnement.
   1. Choisissez **Environment > Mettre à jour la configuration du plug-in du serveur Web global**.
   2. Cliquez sur **OK** ou **Remplacer pour générer un nouveau fichier de configuration de plug-in**.
2. A partir du gestionnaire de déploiement, copiez le plug-in dans la configuration du serveur Web.

  ```
   cp /opt/IBM/WebSphere/Profiles/DefaultDmgr01/config/cells/plugin-cfg.xml /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
  ```
  {: codeblock}
3. Ouvrez le fichier `httpd.conf` dans `IHS_HOME/conf` (`/opt/IBM/WebSphere/HTTPServer/conf`, par exemple) et assurez-vous que les deux lignes suivantes existent.

    ```
    LoadModule was_ap22_module /opt/IBM/WebSphere/Plugins/bin/64bits/mod_was_ap22_http.so
    WebSpherePluginConfig /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
    ```
    {: codeblock}  
4. Ouvrez les ports en exécutant les commandes suivantes.

   ```
   export serverPorts=2810:TCP,2810:UDP,8880:TCP,8880:UDP,9101:TCP,9101:UDP,9061:TCP,9061:UDP,9080:TCP,9080:UDP,9354:TCP,9354:UDP,9044:TCP,9044:UDP,9443:TCP,9443:UDP,5060:TCP,5060:UDP,5061:TCP,5061:UDP,11005:TCP,11005:UDP,11007:TCP,11007:UDP,9633:TCP,9633:UDP,7276:TCP,7276:UDP,7286:TCP,7286:UDP,5558:TCP,5558:UDP,5578:TCP,5578:UDP

   sudo /opt/IBM/WebSphere/AppServer/virtual/bin/openFirewallPorts.sh -ports $serverPorts -persist true
   ```
   {: codeblock}
5. Arrêtez et démarrez le serveur Web en exécutant les commandes suivantes :
    ```
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k stop
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k start
    ```
    {: codeblock}
8. Accédez à votre application via le plug-in.
  ```
   http://169.53.246.xxx/contextRoot/
  ```
  {: codeblock}

**Remarque :** les étapes indiquées représentent l'une des nombreuses méthodes de configuration d'un serveur Web. Si vous avez besoin d'aide supplémentaire, consultez [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/search/configure%20web%20server?scope=SSAW57_9.0.0){: new_window}.

Si vous ne pouvez pas accéder à votre application, vous êtes probablement confronté à un problème d'accès au port sur votre pare-feu. Par conséquent, vous devrez peut-être redémarrer l'un des serveurs suivants : le serveur d'applications, l'agent de noeud, le serveur Web et le gestionnaire de déploiement. De plus, il est possible que vous deviez accéder au tableau de bord du service WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} et redémarrer chaque machine virtuelle.
{: tip}

## Configuration SSL
{: #ssl_configuration}

WebSphere Application Server Traditional et Liberty sont configurés avec le protocole [SSL_TLSv2](https://www.ibm.com/support/knowledgecenter/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/protocols.html){: new_window}. Vous pouvez changer le protocole en modifiant la configuration SSL.

### WebSphere Application Server Traditional
{: #ssl-was}

1. Ouvrez le fichier `security.xml` dans le répertoire `/opt/IBM/WebSphere/Profiles/<profile_name>/config/cell/<cell_name>` et modifiez la ligne suivante.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}

2. Ouvrez le fichier `ssl.client.props` dans le répertoire `/opt/IBM/WebSphere/Profiles/<profile_name>/properties` et modifiez la ligne suivante.

   ```
   com.ibm.ssl.protocol=SSL_TLSv2
   ```
   {: codeblock}

### Liberty
{: #ssl-liberty}

1. Ouvrez le fichier `server.xml` dans le répertoire `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` et modifiez la ligne suivante dans l'élément de configuration SSL `defaultSSLConfig`.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}
