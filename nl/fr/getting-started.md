---

copyright:
  years: 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Tutoriel d'initiation
{:#getting-started}

Avec {{site.data.keyword.appserver_full}}, vous pouvez définir un environnement Liberty ou un environnement WebSphere Application Server Traditional préconfiguré, en quelques minutes. Ce tutoriel d'initiation vous guide dans la procédure de mise à disposition d'un environnement WebSphere Application Server sur une machine virtuelle, qui s'effectue en quelques étapes.
{: shortdesc}

## Avant de commencer
{: #prereqs}

Si vous voulez un environnement disposant de plus de ressources de machines virtuelles dédiées, de type contrat de réservation ou environnement à service exclusif, contactez IBM Sales avant de créer le service. Découvrez ces options plus en détail dans la rubrique [A propos](index.html).

### Migration d'un environnement WebSphere existant

Pour faire migrer un environnement WebSphere Application Server Network Deployment existant vers ce service, utilisez [WebSphere Configuration Migration Tool for {{site.data.keyword.cloud_notm}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window}. Cet outil télécharge la configuration de profil et les applications pour votre serveur autonome ou vos noeuds de cellule sur une instance de service dans {{site.data.keyword.cloud_notm}}. Pour obtenir une présentation de la migration de cloud et une procédure expliquant de manière détaillée comment utiliser cet outil, voir le [guide WebSphere Configuration Migration Tool for IBM Cloud![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window} sur WASdev.

Les étapes de création d'un nouvel environnement dans {{site.data.keyword.appserver_full}} sont décrites ci-après.

## Etape 1 : création du service
{: #create}

1. Accédez à la page [{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server) du catalogue {{site.data.keyword.cloud_notm}}.
1. Connectez-vous avec votre ID IBMid ou inscrivez-vous pour un compte {{site.data.keyword.cloud_notm}}.
1. Sur la page du catalogue, passez en revue les sélections pour la configuration de service.

  Pour des environnements avec tarification à l'utilisation, utilisez les sélections par défaut ou modifiez-les pour les adapter à vos besoins.

  Si vous disposez d'un environnement de type contrat de réservation ou d'un environnement à service exclusif, tenez compte des options suivantes :

  * **Contrat de réservation :** sous **Sélectionnez une région/un emplacement où effectuer le déploiement**, vérifiez que la région sélectionnée correspond bien à celle de votre contrat.

  * **Environnement à service exclusif : ** sous **Sélectionnez une région/un emplacement où effectuer le déploiement**, vérifiez que la zone sélectionnée est la région dans laquelle votre environnement à service exclusif est déployé. Sous **Environnement**, sélectionnez votre environnement à service exclusif. Par défaut, l'environnement public doit s'afficher.

    Si votre environnement à service exclusif n'est pas répertorié, vérifiez que vous êtes bien dans la bonne région et que votre organisation a accès à votre environnement à service exclusif.
    {: tip}
1. Sélectionnez le plan de tarification pour l'édition de {{site.data.keyword.appserver_short}} que vous voulez déployer.
1. Cliquez sur **Créer**.


## Etape 2 : choix de votre environnement (Network Deployment uniquement)
{: #choose_env}

Les plans {{site.data.keyword.appserver_short}} Base et Liberty Core n'ayant que des serveurs uniques, si vous les choisissez, vous pouvez sauter cette étape.

Pour le plan Network Deployment, choisissez le profil et l'architecture pour votre environnement.

* **Profil :** choisissez {{site.data.keyword.appserver_short}} Traditional ou Liberty
* **Architecture :** choisissez un environnement à serveur unique ou un environnement en cluster avec cellules traditionnelles ou collectivités Liberty


## Etape 3 : dimensionnement de vos machines virtuelles
{: #vm_sizing}

Vous pouvez dimensionner la machine virtuelle individuellement pour chaque composant de votre environnement. Les machines virtuelle sont mémorisées en blocs de ressources de [taille standard](index.html#vm-size).

Cliquez sur l'onglet pour le composant (serveur, gestionnaire de déploiement ou noeud d'application, par exemple) et sélectionnez la taille standard pour la machine virtuelle.

## Etape 4 : mise à disposition de votre environnement
{: #service_profile}

Vérifiez les informations figurant dans le récapitulatif de la configuration du service, dont la durée estimée pour la mise à disposition.

**Contrat de réservation :** assurez-vous que l'option **Facturation** est définie sur _Contrat de réservation_. Si l'option n'est pas visible, assurez-vous que le nom de [votre organisation](../../account/orgs_spaces.html){:new_window} est exactement le même, casse et espaces blancs compris, que le nom d'organisation pour votre contrat. Si vous mettez à disposition le service sans sélectionner la facturation avec contrat de réservation, la facturation Paiement à la carte est utilisée.

Cliquez sur **Mettre à disposition** pour configurer votre environnement {{site.data.keyword.appserver_short}}.

## Etapes suivantes
{: #anchor_value}

Découvrez comment accéder à votre nouvel environnement {{site.data.keyword.appserver_short}} et à le gérer, dans la rubrique [Accès au système](systemAccess.html).
