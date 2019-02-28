---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Environnement réseau
{: #networkEnvironment}

Une fois votre instance de service {{site.data.keyword.appserver_full}} mise à disposition, vous pouvez accéder à votre machine virtuelle de plusieurs façons. Vous pouvez vous connecter via un VPN (réseau privé virtuel) sécurisé pour obtenir le SSH, la console d'administration WebSphere traditionnelle et l'accès aux applications sur votre machine virtuelle. Vous pouvez également connecter votre machine virtuelle à Internet avec une adresse IP publique.

Le diagramme suivant montre ces chemins réseau :

Figure 1. Vue client d'un environnement réseau à service partagé avec adresses IP publique

![Figure 1. Vue client d'un environnement réseau à service partagé avec adresses IP publiques](images/wasaas_multi_tenant_publicIP.png)

## Accès au VPN (réseau privé virtuel)
{: #vpnAccess}

Après avoir configuré une instance de service WebSphere Application Server dans {{site.data.keyword.Bluemix_notm}} à partir du tableau de bord du service de l'interface utilisateur graphique {{site.data.keyword.Bluemix_notm}}, vous pouvez établir une connexion OpenVPN. Pour créer la connexion, développez le menu déroulant puis cliquez sur **Télécharger la configuration du VPN** pour télécharger votre configuration VPN. La configuration VPN contient un fichier `.ovpn` et des certificats qui sont utilisés pour l'authentification avec le serveur OpenVPN. Une fois la connexion OpenVPN établie, vous pouvez accéder à votre machine virtuelle via SSH. Vous pouvez également accéder à votre centre d'administration Liberty, à la console d'administration WebSphere traditionnelle et aux applications.

La configuration VPN est étendue à votre organisation et votre région. Elle est valide pendant un an, à partir de la date de sa création. Des connexions client OpenVPN multiples peuvent être établies simultanément en utilisant la même configuration VPN.

**Remarque :** votre configuration VPN n'est valide que si votre organisation contient des abonnements **actifs**. Quand le dernier abonnement pour une organisation est supprimé, toutes les configurations VPN pour cette organisation sont suspendues. Les configurations VPN non arrivées à expiration sont automatiquement réactivées quand un nouvel abonnement devient actif.

## Gestion de configuration VPN avancée
{: #advancedVPN}

Dans la plupart des cas, vous n'avez besoin que d'une seule configuration VPN que vous pouvez télécharger en utilisant le bouton **Télécharger la configuration du VPN**. Toutefois, la page de gestion VPN avancée, à laquelle vous accédez en cliquant sur **Gestion avancée du VPN** depuis le tableau de bord du service, vous permet de créer et de gérer des configurations VPN multiples. Le fait d'avoir plusieurs configurations différentes peut être utile pour effectuer une transition en douceur vers une nouvelle configuration VPN quand la plus ancienne est sur le point d'expirer. Vous pouvez aussi demander des configurations VPN multiples pour gérer l'accès à vos machines virtuelles avec des personnes ou des équipes différentes de votre organisation.  

**Remarque :** 10 configurations VPN actives **au maximum** sont possibles pour votre organisation à tout moment.

Si votre configuration VPN est compromise ou a expiré, vous pouvez la révoquer en utilisant la page de gestion VPN avancée. De plus, pour ce qui est de l'audit, vous pouvez afficher un historique de toute l'activité de gestion VPN et télécharger les configurations VPN actives qui ont été créées précédemment depuis la page de gestion VPN avancée.

Toutes les fonctions disponibles depuis le tableau de bord du service de l'interface utilisateur graphique {{site.data.keyword.Bluemix_notm}} peuvent également être gérées par des scripts en utilisant les API REST. Pour plus d'informations, voir la documentation {{site.data.keyword.Bluemix_notm}} [WebSphere Application Server in IBM Cloud API](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window}.


## Accès public à Internet
{: #publicInternetAccess}

Si vous le souhaitez, vous pouvez gérer l'accès Internet public depuis le tableau de bord du service de l'interface utilisateur graphique {{site.data.keyword.Bluemix_notm}}. Vous pouvez **demander** une adresse IP publique depuis le pool et **ouvrir** la connexion depuis Internet vers votre serveur WebSphere Application Server dans votre instance de service {{site.data.keyword.Bluemix_notm}}. Inversement, vous pouvez **fermer** l'accès depuis votre instance sur Internet et **retourner** l'adresse IP publique dans le pool.

### Demande d'une adresse IP publique et ouverture d'une connexion
{: #request-open-ip}

1. Cliquez sur **Gérer l'accès IP public** sur le tableau de bord du service dans la console {{site.data.keyword.Bluemix_notm}}.
2. L'adresse IP de votre hôte est affichée mais pas votre adresse IP publique. Cliquez sur **Demander une adresse IP publique**.

    Vous retournez au tableau de bord du service avec une IP publique affectée. Toutefois, le message suivant s'affiche :

    > _L'accès est actuellement fermé. Cliquez sur Gérer l'accès IP public pour ouvrir l'accès._
3. Cliquez sur **Gérer l'accès IP public** sur le tableau de bord du service.
4. Les adresses IP pour votre hôte et votre nouvelle IP publique s'affichent mais l'accès est fermé. Cliquez sur **Ouvrir l'accès**.

    Vous retournez au tableau de bord du service, avec le message suivant affiché :

    > _L'accès est actuellement ouvert. Cliquez sur Gérer l'accès IP public pour fermer l'accès._

### Fermeture d'une connexion et retour à une adresse IP publique
{: #close-return-ip}

1. Cliquez sur **Gérer l'accès IP public** sur le tableau de bord du service.
2. Cliquez sur **Fermer l'accès**.

    Vous retournez au tableau de bord du service, avec le message suivant affiché :

    > _L'accès est actuellement fermé. Cliquez sur Gérer l'accès IP public pour ouvrir l'accès._
3. Cliquez sur **Gérer l'accès IP public** sur le tableau de bord du service de l'interface utilisateur graphique {{site.data.keyword.Bluemix_notm}}.
4. Cliquez sur **Renvoyer l'adresse IP publique**.

    Vous retournez au tableau de bord du service où apparaît l'adresse IP de votre hôte, avec le message suivant affiché :

    > _IP public renvoyé._

## Ports d'adresses IP publiques
{: #publicIPports}

Lorsque vous ouvrez l'accès à votre IP publique, l'adresse IP est associée à votre machine virtuelle et les ports 80 et 443 sont ouverts à la passerelle. Toutefois, par défaut, Liberty Core et les serveurs WebSphere Base traditionnels n'ouvrent pas les ports 80 et 443. À l'inverse, les ports 80 et 443 sont ouverts par défaut sur le serveur IBM HTTP. Par conséquent, vous devrez peut-être configurer vos serveurs Liberty Core et WebSphere Base traditionnels pour écouter le trafic d'application sur les ports 80 et 443 lorsque vous utilisez une adresse IP publique.
* Pour configurer votre serveur Liberty Core, voir [Configurer le serveur Liberty Core pour l'accès public](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#configureLibertyForPublicAccess).
* Pour configurer votre serveur WebSphere Base traditionnel, ajoutez une chaîne de transport de conteneur Web qui écoute les ports 80 et 443, comme décrit dans [Configuration des chaînes de transport](http://www.ibm.com/support/knowledgecenter/SSEQTP_9.0.0/com.ibm.websphere.base.doc/ae/trun_chain_transport.html){: new_window}.

**Evitez les problèmes :** Linux réserve les ports plus petits que 1024 pour les utilisateurs privilégies, comme **root**. Toutefois, il est de pratique courante d'exécuter les serveurs WebSphere Base traditionnels en tant qu'**utilisateur non root**. Ainsi, quand vous ajoutez une chaîne de transport de conteneur Web, changez votre configuration **iptables** afin de mettre en oeuvre l'utilisateur **root**. Plus précisément, redirigez les ports 80 et 443 restreints vers un autre port au-dessus de 1024, comme 9080 et 9443. Les commandes suivantes fournissent un exemple de ce processus :

```
-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 9080
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9080 -j ACCEPT

-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 9443
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
```

**Remarque :** les changements apportés à **iptables** sont éphémères. Ainsi, si votre invité est réinitialisé ou si le service **iptables** est redémarré, les règles sont automatiquement vidées et redémarrées. Pour sauvegarder les règles afin qu'elles soient conservées quand le service iptables est redémarré ou l'invité réinitialisé, utilisez la commande ci-après en tant qu'utilisateur **root** :

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


**Remarque :** les services **iptables** sont invoqués via des demandes qui circulent sur l'interface externe de l'invité. Les demandes qui sont acheminées sur la boucle loopback locale (127.0.0.1) n'étant pas traitées par **iptables**, la redirection des ports, comme indiqué précédemment, ne sera pas invoquée sur une boucle loopback.

## Ports d'adresses IP privées de réseau privé virtuel
{: #privateIPports}

Vous vous connectez à l'adresse IP privée de votre machine virtuelle sur la connexion de réseau privé virtuel. Votre centre d'administration Liberty (9080, 9443), la console d'administration WebSphere traditionnelle (9060, 9043), SSH (22) et les ports autres que 80 et 443 ne sont accessibles que par la connexion VPN, comme illustré Figure 1. Voir l'exemple Liberty Core **server.xml** et **ibm-web-bnd.xml** pour plus de détails sur la séparation du centre d'administration Liberty d'avec vos ports d'application.

**Evitez les problèmes :** pour les serveurs Liberty Core et WebSphere Base traditionnels, les ports de pare-feu sont préconfigurés lorsque votre machine virtuelle est configurée. Toutefois, pour les configurations de déploiement réseau où le gestionnaire de déploiement ou le contrôleur collectif est localisé avec IBM HTTP Server, vous devrez peut-être ouvrir des ports sur le pare-feu. Voir [Ports de pare-feu](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#firewall_ports) pour plus de détails.

## Configuration d'un serveur Liberty Core pour un accès par IP publique
{: #configureLibertyForPublicAccess}

Vous devez configurer Liberty Core pour écouter le trafic d'application sur les ports 80 et 443 lorsque vous utilisez une adresse IP publique.

Par défaut, Liberty est configuré avec le centre d'administration Liberty et les applications disponibles sur l'hôte virtuel **default_host** qui est associé au **defaultHttpEndpoint** sur les ports 9080 et 9443. Reconfigurez votre serveur pour séparer le centre d'administration Liberty de l'hôte virtuel d'application et du noeud final et pour les rendre disponibles sur des ports distincts.

Le fragment de code suivant est un exemple de réglages de configuration de server.xml :

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

Ensuite, associez votre application à l'hôte virtuel `external_host` en incluant le fragment suivant dans le fichier `WEB-INF/ibm-web-bnd.xml` de votre application :

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

## Configuration des serveurs DNS
{: #dnsConfig}

Il est important de noter que les serveurs WebSphere Application Server des machines virtuelles {{site.data.keyword.Bluemix_notm}} sont configurés avec deux résolveurs DNS, qui sont eux-mêmes configurés dans le fichier **/etc/resolv.conf** de la machine virtuelle. Le serveur DNS principal est un serveur autre qu'un serveur de référence qui est fourni par WebSphere Application Server dans le service {{site.data.keyword.Bluemix_notm}}. Le serveur DNS secondaire est un serveur autre qu'un serveur de référence qui est fourni par {{site.data.keyword.Bluemix_notm}}.

Prenez connaissance de la configuration DNS pour vous assurer qu'elle correspond à vos besoins. Vous pouvez mettre à jour le fichier `/etc/resolv.conf` pour référencer le serveur DNS de votre choix si les serveurs fournis par IBM ne répondent pas à vos exigences.

**Remarque :** un serveur WebSphere Application Server plus ancien dans les machines virtuelles {{site.data.keyword.Bluemix_notm}} peut n'avoir qu'un serveur DNS principal configuré dans le fichier `/etc/resolv.conf`. Si vous voulez une solution à haute disponibilité, vous pouvez soit libérer la machine virtuelle actuelle et en mettre une nouvelle à disposition, soit mettre à jour le fichier `/etc/resolv.conf` pour ajouter un serveur DNS secondaire. Ce serveur DNS secondaire peut être votre serveur DNS préféré ou celui fourni par {{site.data.keyword.Bluemix_notm}} (10.0.80.11).


## Ouverture de ports pour les nouveaux serveurs sur les noeuds personnalisés
{: #serversOnCustom}

Quand vous créez un serveur sur un noeud personnalisé, les ports supplémentaires qui sont requis par le serveur doivent être ouverts sur le gestionnaire de déploiement et les machines virtuelles du noeud personnalisé avant de démarrer le serveur. Après création du serveur mais avant son démarrage, ouvrez les ports en exécutant le script `openWASPorts.sh`.

 1. Connectez-vous à chaque gestionnaire de déploiement et machine virtuelle personnalisée en tant qu'utilisateur root.
 1. Exécutez le script `/opt/IBM/WebSphere/AppServer/virtual/bin/openWASPorts.sh` pour ouvrir les ports.

Après exécution du script, vous pouvez démarrer le serveur depuis la console d'administration du gestionnaire de déploiement.
