---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Environnements à service exclusif
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}}:Single Tenant Environment est une offre à service exclusif qui fournit aux clients avec une charge de travail WebSphere isolée un environnement hybride intégré complet et des données sécurisées. Ce guide d'initiation est conçu pour identifier les éléments clé permettant d'aider les clients à accéder à leur serveur WebSphere Application Server et à le gérer dans l'environnement à service exclusif {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment.
{: shortdesc}


## Logiciels recommandés
{: #recommended_software}

Vous devez disposer du logiciel suivant pour accéder à votre environnement à service exclusif :
* Navigateur Web pris en charge par {{site.data.keyword.Bluemix_notm}} :
    * Chrome : la dernière version disponible pour votre système d'exploitation
    * Firefox : la dernière version disponible pour votre système d'exploitation ou la dernière version ESR (Extended Support Release)
    * Internet Explorer : version 10 ou 11
    * Safari : la dernière version pour Mac
* Interface de ligne de commande Cloud Foundry, version 6.5.1 ou ultérieure (vous pouvez utiliser la dernière édition)
* Git Bash (recommandé)
    * Téléchargez et installez [Git Bash](https://git-scm.com/downloads){: new_window}


## Présentation de l'environnement à service exclusif WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment
{: #overviewSTE}

L'offre WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant propose aux consommateurs une instance privée du service qui leur est propre, un réseau privé et des ressources isolées. Bien que l'offre soit gérée de façon indépendante, les tableaux de bord du service et de l'instance de service créée sont accessibles via une région {{site.data.keyword.Bluemix_notm}} publique spécifique, comme indiqué dans la figure ci-après :

Figure 1. Architecture de l'environnement à service exclusif WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment

![Figure 1. Architecture d'un environnement à service exclusif](images/WASaaS.png)


## Gestion de l'organisation
{: #organization_management}

L'environnement à service exclusif WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment est configuré selon les spécifications indiquées dans votre commande. Si vous avez fourni dans cette dernière un ou plusieurs noms d'organisation {{site.data.keyword.Bluemix_notm}}, vous pouvez accéder à votre environnement dès maintenant. Si vous n'avez pas encore indiqué de noms d'organisation ou si voulez changer ce paramètre, ouvrez un [ticket de demande de service ](reportingIssues.html#reporting_issues) pour **Services d'application** depuis la console {{site.data.keyword.Bluemix_notm}} de votre région. Vous trouverez le nom de l'organisation (ORG) dans l'angle supérieur droit de la console {{site.data.keyword.Bluemix_notm}}, comme illustré dans la figure suivante :

Figure 2. Emplacement du nom de l'organisation

![Figure 2. Emplacement du nom de l'organisation](images/myORG.png)


**Remarque :** pour savoir comment accéder à votre environnement à service exclusif, voir la rubrique [Accès à l'environnement à service exclusif](singleTenantAccess.html#singleTenantEnvironment).
