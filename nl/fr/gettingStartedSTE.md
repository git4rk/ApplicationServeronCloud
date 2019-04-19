---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

keywords: single tenant, websphere, sales, order

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Environnements à service exclusif
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}} Single Tenant Environment fournit aux clients avec une charge de travail WebSphere isolée un environnement hybride intégré complet et des données sécurisées. Ce guide d'initiation est conçu pour vous permettre d'identifier les éléments clé de façon à faciliter l'accès à votre environnement à service exclusif et à le gérer.
{: shortdesc}

## Commande d'un environnement à service exclusif
{:#ordering}

Les environnements à service exclusif ne peuvent pas être créés via le catalogue {{site.data.keyword.Bluemix_notm}} et doivent être commandés en contact IBM Sales. Lorsque vous commandez votre environnement, vous pouvez choisir un environnement à service exclusif standard ou BYOL. Les environnements à service exclusif standard incluent toutes les licences d'infrastructure et WebSphere Application Server requises. Dans les environnements à service exclusif BYOL, vous pouvez utiliser des licences WebSphere Application Server distinctes.

Pour commander un environnement à service exclusif, [contactez IBM Sales](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales). L'équipe commerciale peut vous aider à installer et configurer un environnement adapté à vos besoins.

## Présentation de WebSphere Application Server dans un environnement à service exclusif {{site.data.keyword.Bluemix_notm}}
{: #overviewSTE}

L'environnement à service exclusif vous propose une instance privée du service qui vous est propre, un réseau privé et des ressources isolées. Bien que l'offre soit gérée de façon indépendante, les tableaux de bord du service et de l'instance de service créée sont accessibles via une région {{site.data.keyword.Bluemix_notm}}, comme indiqué dans la figure ci-après.

Figure 1. Architecture de WebSphere Application Server dans un environnement à service exclusif {{site.data.keyword.Bluemix_notm}}

![Figure 1. Architecture d'un environnement à service exclusif](images/WASaaS.png)


## Gestion de l'organisation
{: #organization_management}

Le serveur WebSphere Application Server dans un environnement à service exclusif {{site.data.keyword.Bluemix_notm}} est configuré selon les spécifications indiquées dans votre commande. Si vous avez fourni dans cette dernière un ou plusieurs noms d'organisation {{site.data.keyword.Bluemix_notm}}, vous pouvez accéder à votre environnement dès maintenant. Si vous n'avez pas indiqué de noms d'organisation ou si voulez changer ce paramètre, ouvrez un [ticket de demande de service](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#reporting_issues) pour **Services d'application** depuis la console {{site.data.keyword.Bluemix_notm}} de votre région. Vous pouvez trouver le nom de votre organisation dans la console {{site.data.keyword.Bluemix_notm}} en sélectionnant **Gérer > Compte > Organisations Cloud Foundry**.

**Remarque :** pour savoir comment accéder à votre environnement à service exclusif, voir la rubrique [Accès à l'environnement à service exclusif](/docs/services/ApplicationServeronCloud?topic=wasaas-singleTenantEnvironment#singleTenantEnvironment).
