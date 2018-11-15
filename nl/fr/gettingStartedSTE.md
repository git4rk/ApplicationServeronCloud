---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-25"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Environnements à service exclusif
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}}:Single Tenant Environment fournit aux clients avec une charge de travail WebSphere isolée un environnement hybride intégré complet et des données sécurisées. Ce guide d'initiation est conçu pour identifier les éléments clé permettant d'aider les clients à accéder à leur serveur WebSphere Application Server et à le gérer dans l'environnement à service exclusif {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment.
{: shortdesc}

## Commande d'un environnement à service exclusif
{:#ordering}

Les environnements à service exclusif ne peuvent pas être créés via le catalogue {{site.data.keyword.Bluemix_notm}} et doivent être commandés en contact IBM Sales. Lorsque vous commandez votre environnement, vous pouvez choisir un environnement à service exclusif standard ou BYOL. Les environnements à service exclusif standard incluent toutes les licences d'infrastructure et WebSphere Application Server requises. Les environnements à service exclusif BYOL vous permettent d'utiliser des licences WebSphere Application Server distinctes.

Pour commander un environnement à service exclusif, [contactez IBM Sales](reportingIssues.html#contacting-sales). L'équipe commerciale peut vous aider à installer et configurer un environnement adapté à vos besoins. 

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
