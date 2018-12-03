---

copyright:
  years: 2017, 2018
lastupdated: "2018-08-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Mise à jour de votre environnement
{: #updating-your-environment}

## Stratégie de maintenance
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} est mis à jour régulièrement de façon à garantir que les nouvelles instances de service sont créées avec les groupes de correctifs et les correctifs les plus récents. Le cloud met à la disposition des équipes de gestion du middleware de nouvelles instances de service facilement et rapidement.

Vous pouvez créer une instance WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} au niveau du groupe de correctifs actuel ou à un niveau précédent (n ou n-1) pour une version de produit particulière. L'utilisation du groupe de correctifs actuel fournit les dernières mises à jour et fonctions, mais le groupe de correctifs précédent peut être nécessaire pour se conformer aux exigences d'un déploiement de cloud hybride.

Quand vous créez une nouvelle instance, vous pouvez choisir l'un des niveaux de groupe de correctifs suivants sur l'onglet **Profil de service** de l'instance de service :

**Liberty**
  * 18.0.0.2
  * 18.0.0.1

**WebSphere Application Server Traditional**
  * 9.0.0.8
  * 9.0.0.7
  * 8.5.5.14
  * 8.5.5.13

## Applications des mises à jour de correctifs et de groupes de correctifs
{:#applying-fixes}

La façon la plus rapide d'appliquer une mise à jour sur le dernier niveau de maintenance est de créer une nouvelle instance. Toutefois, si vous préférez conserver des instances de service à long terme, vous pouvez appliquer une maintenance sur l'installation existante en exécutant le script `installService.sh` fourni ou en vous servant d'IBM Installation Manager, comme décrit dans les sections suivantes.

### Mise à jour en utilisant le script installService.sh

Votre instance de service est configurée avec un référentiel Installation Manager qui est fréquemment mis à jour avec les correctifs de sécurité et les groupes de correctifs WebSphere Application Server disponibles. Vous pouvez utiliser le script `/home/virtuser/installService.sh` pour appliquer ces correctifs et groupes de correctifs. Le script doit être exécuté en tant qu'utilisateur racine.

La quantité d'espace disque requise pour installer les mises à jour varie selon les types de mises à jour que vous installez. L'installation des seuls correctifs temporaires nécessite 1 Go d'espace libre sur la machine virtuelle. Ce chiffre passe à 1,3 Go si vous installez les groupes de correctifs.

L'exécution du script génère les actions suivantes :

* Arrêt de toutes les instances WebSphere Application Server et IBM HTTP Server en cours d'exécution
* Installation facultative des derniers groupes de correctifs pour Installation Manager, WebSphere Application Server, IBM HTTP Server et Java&trade; SDK
* Installation des derniers correctifs temporaires pour WebSphere, IBM HTTP Server et Java&trade; SDK
* Redémarrage de toutes les instances

#### Options
* **`-fixpacks`**

    Met tous les packages au niveau du dernier groupe de correctifs.
* **`-noprompt`**

    Ne demande pas confirmation avant de procéder à la mise à jour.

#### Exemples de syntaxe

```
./installService.sh -?
```
{:.codeblock}

Affiche le texte d'aide.


```
./installService.sh
```
{:.codeblock}

Installe tous les correctifs temporaires applicables mais aucun groupe de correctifs.


```
./installService.sh -fixpacks
```
{:.codeblock}

Installe tous les groupes de correctifs disponibles puis tous les correctifs temporaires applicables.

### Mise à jour en utilisant Installation Manager
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} est installé dans le répertoire `/home/virtuser/IBM/Installation Manager` et peut être exécuté directement pour appliquer les correctifs et groupes de correctifs.

**Evitez les problèmes : ** puisque les fichiers binaires sous-jacents sont installés en tant que `virtuser` (utilisateur administrateur virtuel, doté de droits limités), assurez-vous qu'Installation Manager est toujours exécuté en tant que `virtuser`.

## Application des mises à jour système sur vos machines virtuelles
{:#vm-system-updates}

L'application des mises à jour système sur une machine virtuelle est similaire à la mise à jour d'un système RHEL (Red Hat Enterprise Linux&reg;). En utilisant le gestionnaire de package Yum, vous pouvez installer, mettre à jour, désinstaller et gérer les packages. Les systèmes WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} sont configurés pour recevoir des mises à jour du serveur Red Hat Satellite d'IBM, qui fournit des packages fiables et sécurisés depuis le réseau Red Hat. Le serveur Satellite est géré par IBM et ne peut être modifié depuis votre système.

Pour plus d'informations, voir [Applying package updates on Red Hat Enterprise Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} et [Yum, the Red Hat package manager](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}.
