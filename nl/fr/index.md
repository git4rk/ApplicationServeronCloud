---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# A propos
{: #about}

{{site.data.keyword.appserver_full}} permet une configuration rapide sur une instance WebSphere Application Server Liberty, Traditional Network Deployment ou Traditional WebSphere Java EE préconfigurée dans un environnement de cloud hébergé sur {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

## Présentation de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} fournit aux consommateurs des serveurs Traditional WebSphere et Liberty préconfigurés. Il est hébergé sur des invités de machine virtuelle avec les droits d'accès de l'utilisateur root au système d'exploitation invité. Quand vous créez votre service, choisissez entre _Liberty_, _Traditional ND_ ou _Traditional WebSphere_.

**Remarque :** les consommateurs sont maintenant en mesure de choisir entre le niveau de groupe de correctifs actuel et une version plus ancienne [(n ou n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} quand vous créez un serveur WebSphere Application Server dans une instance {{site.data.keyword.Bluemix_notm}}.

Vous êtes initié à l'administration WebSphere et disposez d'un accès complet au système d'exploitation sous-jacent. Vous pouvez réutiliser vos scripts existants et apporter de petites personnalisations au système afin de travailler avec vos propres infrastructures ou des infrastructures tierces. Le centre d'administration et les consoles d'administration vous permettent d'administrer votre service WebSphere Application Server Liberty ou Traditional, de la même façon que vos configurations WebSphere sur site.

Le plan WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment se compose d'un environnement de cellule WebSphere Application Server Network Deployment avec deux machines virtuelles, ou plus. La première machine virtuelle contient le gestionnaire de déploiement et IBM HTTP Server ; les autres machines virtuelles contiennent les noeuds personnalisés (agents de noeud) fédérés dans le gestionnaire de déploiement. Utilisez les scripts wsadmin existants pour créer votre configuration WebSphere ou servez-vous de la console d'administration WebSphere pour configurer manuellement l'environnement. Ces nouvelles fonctionnalités permettent aux utilisateurs de créer un environnement en cluster, aspect essentiel de toute application d'entreprise middleware. Les clients peuvent désormais choisir de mettre en cluster une topologie afin d'équilibrer la charge des demandes entre deux instances, ou plus.

Le plan WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment inclut aussi l'utilisation d'une collectivité Liberty. Cette dernière, qui est un domaine d'administration pour un groupe de profils Liberty (serveurs), se
compose de deux machines virtuelles, ou plus. La première machine virtuelle contient le serveur Liberty du contrôleur de collectivité, qui constitue un point de contrôle pour la collectivité Liberty. En plus de la collectivité Liberty, cette machine virtuelle contient également le serveur IBM HTTP Server, qui permet l'accès à vos applications depuis un navigateur Web. Les autres machines virtuelles sont les hôtes de collectivité sur lesquels résident les membres de collectivité (serveurs de profil Liberty). Le centre d'administration Liberty est également activé sur le serveur du contrôleur Liberty.

La figure suivante présente l'architecture de WebSphere Application Server dans les environnements de cellule de déploiement réseau {{site.data.keyword.Bluemix_notm}} et de collectivité Liberty.

Figure 1. Cellule de déploiement réseau et architecture de collectivité Liberty

![Figure 1. Architecture de cellule de déploiement réseau et de collectivité Liberty](images/CellCollectiveDiagram.gif)

**Remarque** : dans la _figure 1_ ci-dessus, le modèle qui représente la collocation du gestionnaire de déploiement ou du contrôleur de collectivité avec IBM HTTP Server est destiné au développement et au test. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} vous donne également la liberté de reconfigurer le logiciel préinstallé pour répondre à vos besoins en matière d'applications et de production ; tout comme vous le feriez sur place. En outre, pour les exigences de production les plus strictes, contactez votre ingénieur commercial IBM qui peut vous informer sur notre offre IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} à service exclusif, qui propose des ressources isolées en réseau et en calcul.


## Environnement d'exploitation
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} est un service qui renvoie des invités (machines virtuelles) dans un environnement partagé sur lesquels les consommateurs peuvent déployer des applications. Un réseau privé virtuel protège le service public des analyses de port générique et d'autres attaques indésirables via le réseau. Toutefois, il est important que vous vous rappeliez que le réseau privé virtuel du service que vous utilisez pour accéder à votre instance de service peut être partagé par plusieurs organisations et utilisateurs {{site.data.keyword.Bluemix_notm}}. Les machines virtuelles fournissent des ressources de traitement, de mémoire et d'E-S provenant d'un pool partagé de ressources IaaS.

Etant donné que les ressources de traitement, de mémoire et d'E-S sont exécutées par des machines virtuelles dans un environnement partagé, les configurations de service peuvent varier. Vous pouvez examiner la configuration de chaque instance de service spécifique dans les portails et les tableaux de bord des services IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} fournit des instances de machine virtuelle. Avec ces instances, les clients utilisent un simple portail pour créer et gérer les déploiements WebSphere Application Server en entreprise de manière cohérente et reproductible, tout en bénéficiant d'une souplesse substantielle pour paramétrer leurs applications. Les utilisateurs peuvent exploiter des machines virtuelles WebSphere Application Server Liberty, ND, ou Traditional préconfigurées, dans un environnement de cloud hébergé. Les utilisateurs peuvent faire migrer les applications WebSphere Application Server existantes vers {{site.data.keyword.Bluemix_notm}} et contrôler complètement le système d'exploitation et le middleware sous-jacents.

## Dimensionnement de machine virtuelle
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} fournit un dimensionnement de taille standard qui vous permet de redimensionner correctement les environnement pour les applications gourmandes en mémoire en mettant à disposition des machines virtuelles plus grandes. Chaque machine virtuelle mise à disposition pour exécuter WebSphere Application Server peut être dimensionnée de façon indépendante, selon les besoins en ressources attendues.

Les machines virtuelles sont dimensionnées et facturées par *blocs*. Pour chaque bloc de taille standard, la machine virtuelle est mise à disposition avec les ressources suivantes.
* 1 UC virtuelle
* 2 Go de RAM
* 12,5 Go d'espace de disque dur (12,0 Go pour les machines virtuelles à bloc unique)


| Tailles standard | Blocs | UC virtuelle | Mémoire RAM (Go) | Disque dur (Go) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
| S | 1 | 1 | 2 | 12 |
| M | 2 | 2 | 4 | 25 |
| L | 4 | 4 | 8 | 50 |
| XL | 8 | 8 | 16 | 100 |
| XXL | 16 | 16 | 32 | 200 |
{: caption="Tableau 1. Blocs par tailles standard" caption-side="top"}

Chaque serveur ou noeud est mis à disposition dans une machine virtuelle unique. Ainsi, dans le plan Network Deployment, si vous mettez à disposition une machine virtuelle de taille M (2 blocs) pour votre gestionnaire de déploiement et 8 machines virtuelles de taille S (1 bloc) pour les noeuds d'application, vous serez facturé pour un total de 10 blocs.

## Options de facturation
{: #billing-options}

La tarification pour chaque bloc dépend de l'option de facturation que vous avez choisie :
* **[Facturation à l'utilisation](#pay-as-you-go) :** tarification basée sur l'utilisation, facturée en heures par bloc
* **[Contrat de réservation](#reserve-contract) :** abonnement mensuel prépayé portant sur des ressources réservées

### Facturation à l'utilisation
{: #pay-as-you-go}

La tarification à l'utilisation s'applique si vous mettez à disposition le serveur IBM WebSphere Application Server dans le service {{site.data.keyword.Bluemix_notm}} sans avoir contacté IBM Sales pour choisir d'autres options de facturation. Toute heure (partielle ou complète) d'utilisation de chaque bloc est décomptée durant la période de facturation mensuelle. La facturation minimale est fixée à 1/4 d'heure de bloc.

**Remarque** : du fait d'un volume spécifique de ressources de calcul, de mémoire et d'entrée/sortie, les instances arrêtées sont facturées à un taux réduit, correspondant à 5 % du taux de bloc horaire. Dans le service, les instances arrêtées sont limitées à 10 adresses IP ou 64 Go de mémoire.

#### Tarification des plans

Le prix par bloc varie selon le plan WebSphere Application Server que vous avez choisi.

Le tableau ci-après répertorie le prix total par heure pour chaque machine virtuelle associée à l'une des tailles standard existantes. Les prix indiqués correspondent aux différents plans IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, au 1er avril 2016, en dollars US. Voir le catalogue pour les prix actuels de votre région.

| Tailles standard | Blocs | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
| S | 1 | 0,21 $ | 0,30 $ |  0,70 $ |
| M | 2 | 0,42 $ | 0,60 $ |  1,40 $ |
| L | 4 | 0,84 $ | 1,20 $ |  2,80 $ |
| XL | 8 | 1,68 $ | 2,40 $ |  5,60 $ |
| XXL | 16 | 3,36 $ | 4,80 $ |  11,20 $ |
{: caption="Tableau 2. Plan Liberty Core" caption-side="top"}


### Contrat de réservation
{:#reserve-contract}

Avec une facturation de contrat de réservation, vous achetez un abonnement mensuel prépayé qui garantit l'accès à des blocs de ressources de calcul qui vous sont physiquement réservés. Ces blocs de service sont mis de côté pour votre utilisation exclusive et ne peuvent être considérés comme disponibles pour les autres utilisateurs du serveur WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}. Si vous disposez de licences WebSphere Application Server, vous pouvez choisir un contrat de réservation BYOL (bring-your-own-license), qui utilise ces licences et propose un taux de facturation réduit. Pour configurer une facturation de contrat de réservation, [contactez IBM Sales](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

Les abonnements sont disponibles par incréments de 8 blocs. Le total des heures de bloc repose sur le nombre d'heures dans le mois, mais vous pouvez utiliser les heures de bloc à toute période du mois. Ainsi, un mois de 30 jours se compose de 720 heures qui, lorsqu'elles sont multipliées par un abonnement de 8 blocs, donnent un total de 5760 heures de bloc.

  ```
30 jours * 24 heures par jour * 8 blocs = 5760 heures de bloc
  ```

Vous pouvez personnaliser la façon et le moment dont vous utilisez les blocs afin de répondre à une demande de charge de travail variable (utilisation de 4 blocs, augmentation à 12 blocs puis réduction à 8 blocs, par exemple). Tant que vous restez sous le nombre total d'heures de bloc mensuelles, aucun supplément ne vous est facturé.

Vous pouvez choisir d'utiliser vos blocs de contrat de réservation ou une facturation Paiement à la carte lorsque vous mettez à disposition chaque environnement.

**Remarque :** si vous supprimez une instance de service, vous devrez peut-être attendre environ 30 minutes pour que ses blocs deviennent disponibles pour les nouvelles instances de service.

#### Dépassements

Si votre utilisation est supérieure aux heures de bloc mensuelles de votre abonnement, un dépassement vous est facturé, calculé selon le modèle de tarification à l'utilisation, ce qui fait que vous ne payez que les heures de bloc supplémentaires dont vous vous êtes effectivement servi. L'utilisation des blocs est mesurée sur une base horaire, complète ou partielle, avec un seuil minimal fixé à 1/4 d'heure de bloc.

Les blocs provenant du modèle de tarification à l'utilisation ne correspondent pas à une capacité réservée et sont tirés d'un pool de ressources communes.

#### Taux calculés au prorata pour une utilisation souple

Les blocs inclus dans une facturation de contrat de réservation reposent sur le plan WebSphere Application Server Network Deployment, mais vous pouvez aussi vous en servir pour d'autres plans. Avec ces autres plans, l'utilisation est répartie au prorata, ce qui fait qu'une heure de bloc est réduite via le taux de proratisation quand elle se reflète dans les heures de bloc restantes dans le contrat de réservation.

Le tableau suivant affiche les taux de proratisation pour chaque plan et le prix effectif par heure de bloc réellement utilisée une fois le calcul au prorata effectué. Pour les prix actuels de votre région, [contactez IBM Sales](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales).

| Plan | Taux de proratisation | Prix/heure après proratisation |
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0,3 | 0,21 $ |
| WebSphere Application Server Base  | 0,43 | 0,30 $ |
| WebSphere Application Server Network Deployment | 1,0 | 0,70 $ |
{: caption="Tableau 3. Taux de proratisation par heure de bloc et par plan" caption-side="top"}

Ainsi, vous pouvez avoir une instance WebSphere Application Server Base de taille M (2 blocs) qui s'exécute pendant 51 heures. Pour calculer les heures de bloc utilisées depuis votre contrat de réservation, les heures de bloc effectives sont multipliées par le taux de proratisation, ce qui donne un total de 43,86 heures de bloc :

```
2 blocs * 51 heures * 0,43 (taux de proratisation) = 43,86 heures (calculées au prorata)
```

Le coût total reste le même, mais vous pouvez utiliser plus d'heures de bloc effectives en provenance des plans avec calcul au prorata, car un nombre moindre d'heures est déduit de vos heures de bloc incluses dans votre contrat de réservation.
{:.tip}
