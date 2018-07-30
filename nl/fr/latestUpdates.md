---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Dernières mises à jour
{: #latest_updates}

Liste des dernières mises à jour du service.

## 13 juin 2018 : la facturation de contrat avec réservation est désormais disponible

Avec une facturation de contrat avec réservation, vous achetez un abonnement mensuel prépayé qui garantit l'accès à des blocs de ressources de calcul qui vous sont physiquement réservés. Ces blocs de service sont mis de côté pour votre utilisation exclusive et ne peuvent être considérés comme disponibles pour les autres utilisateurs du serveur {{site.data.keyword.appserver_full}}. Vous pouvez utiliser vos heures de bloc de service du mois comme vous le souhaitez, tous les dépassements éventuels vous étant facturés selon le modèle d'abonnement standard de tarification à l'utilisation.

Pour en savoir plus sur la facturation de contrat avec réservation, voir [Options de facturation](index.html#billing-options).

## 30 mars 2018 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Le groupe de correctifs version 9.0.0.7 de Traditional WebSphere Application Server est désormais disponible quand vous mettez à disposition une nouvelle instance de service. En plus de la version 9.0.0.7, d'autres versions de Traditional WebSphere Application Server, telles les versions 9.0.0.6, 8.5.5.13 et 8.5.5.12, sont disponibles pour la mise à disposition.
* Le groupe de correctifs version 18.0.0.1 de WebSphere Application Server Liberty est désormais disponible quand vous mettez à disposition une nouvelle instance de service. En plus de la version 18.0.0.1, le groupe de correctifs version 17.0.0.4 de WebSphere Application Server Liberty est disponible pour la mise à disposition.
* Correction de [plusieurs vulnérabilités de sécurité]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Plusieurs vulnérabilités dans IBM® Java SDK
  * Vulnérabilité lors de la fourniture par IBM WebSphere Application Server d'une sécurité plus faible que celle attendue lors de l'utilisation de la console d'administration.
  * Vulnérabilité dans laquelle des installations IBM WebSphere Application Server utilisant une connexion par formulaire pouvaient autoriser un agresseur à distance à effectuer des attaques d'usurpation.
  * Vulnérabilité dans laquelle IBM WebSphere Application Server pouvait permettre à un agresseur local d'obtenir des informations sensibles, causée par le traitement inapproprié de demandes en provenance d'applications, pouvant permettre un accès en lecture non autorisé à un fichier.
  * Vulnérabilité dans laquelle Apache Commons FileUpload, utilisé dans plusieurs produits différents, pouvait autoriser un agresseur à distance à exécuter un code arbitraire sur le système, causée par la désérialisation de données non sécurisées dans la classe DiskFileItem de la bibliothèque FileUpload. Un agresseur à distance pouvait exploiter cette vulnérabilité pour exécuter un code arbitraire dans le contexte du processus actuel.
  * Vulnérabilité dans laquelle les unités centrales Intel Haswell Xeon, AMD PRO et ARM Cortex A57 pouvaient permettre à un agresseur local authentifié d'obtenir des informations sensibles, causée par le contournement de la vérification des limites dans la fonction d'exécution des instructions de branchement spéculatives des unités centrales. En conduisant des attaques par canal auxiliaire visant le cache, un agresseur pouvait exploiter cette vulnérabilité pour traverser la limite syscall et lire les données à partir de la mémoire virtuelle de l'unité centrale.
* Diverses maintenances de service ont été intégrées.

## 8 janvier 2018 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Le groupe de correctifs version 9.0.0.6 de Traditional WebSphere Application Server est désormais disponible quand vous mettez à disposition une nouvelle instance de service. En plus de la version 9.0.0.6, d'autres versions de Traditional WebSphere Application Server, telles les versions 9.0.0.5, 8.5.5.12 et 8.5.5.11, sont disponibles pour la mise à disposition.
* Le groupe de correctifs version 17.0.0.4 de WebSphere Application Server Liberty est désormais disponible quand vous mettez à disposition une nouvelle instance de service. En plus de la version 17.0.0.4, le groupe de correctifs version 17.0.0.3 de WebSphere Application Server Liberty est disponible pour la mise à disposition.
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité dans laquelle OpenSAML pouvait permettre à un agresseur à distance authentifié d'obtenir des informations sensibles, causée par une erreur lors de l'analyse d'entités XML.
  * Vulnérabilité dans laquelle Apache HTTP Server pouvait permettre à un agresseur à distance d'obtenir des informations sensibles, causée par une faille dans la méthode HTTP OPTIONS, également connue sous le nom d'Optionsbleed.
  * Vulnérabilité dans laquelle Apache Portable Runtime Utility (APR-util) risquait un déni de service, causée par un échec de validation de l'intégrité des fichiers de base de données SDBM utilisés par les fonctions apr_sdbm*().
* Diverses maintenances de service ont été intégrées.

## 21 décembre 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Ajout de la fonction WebSphere Application Server in IBM Cloud Migration à Dallas, Londres et Sydney. Cette fonction fournit une migration de bout en bout complète depuis les environnements sur site v7, v8 ou v8.5.5 existants vers les environnements v9 s'exécutant dans IBM Cloud. Pour plus d'informations, voir [WebSphere Configuration Migration Tool for IBM Cloud](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud).
* Diverses maintenances de service ont été intégrées.

## 27 octobre 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Ajout de la possibilité de mettre à disposition un niveau de groupe de correctifs plus ancien [(n-1)](maintenanceAndUpdates.html#maintenance-strategy){: new_window} via l'onglet Profil de service du tableau de bord de service {{site.data.keyword.Bluemix_notm}} ou par le biais de l'API REST.
* Le groupe de correctifs version 9.0.0.5 de Traditional WebSphere Application Server est désormais disponible quand vous mettez à disposition une nouvelle instance de service. En plus de la version 9.0.0.5, d'autres versions de Traditional WebSphere Application Server, telles les versions 9.0.0.4, 8.5.5.12, et 8.5.5.11, sont disponibles pour la mise à disposition.
* Le groupe de correctifs version 17.0.0.3 de WebSphere Application Server Liberty est désormais disponible quand vous mettez à disposition une nouvelle instance de service. En plus de la version 17.0.0.3, le groupe de correctifs version 17.0.0.2 de WebSphere Application Server Liberty est disponible pour la mise à disposition.
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité dans laquelle IBM WebSphere Application Server risquait de créer des fichiers en utilisant les droits par défaut au lieu des droits personnalisés lors de l'utilisation de scripts de démarrage personnalisés
  * Vulnérabilité dans laquelle IBM WebSphere Application Server Proxy Server ou le routeur ODR (On-Demand-Router) pouvaient permettre à un agresseur local d'obtenir des informations sensibles, causée par la mise en cache de données périmées, remises ensuite en service.
  * Vulnérabilité dans laquelle IBM WebSphere Application Server était susceptible de subir une attaque Cross-site Scripting. Cette vulnérabilité permettait aux utilisateurs d'imbriquer du code JavaScript dans l'interface utilisateur Web, modifiant ainsi la fonctionnalité prévue et entraînant potentiellement la divulgation des données d'identification au sein d'une session sécurisée.
  * Vulnérabilité lors de la fourniture par IBM WebSphere Application Server d'une sécurité plus faible que celle attendue après utilisation de la console d'administration pour mettre à jour les paramètres de liaisons de sécurité des services Web.
  * Vulnérabilité lors de la fourniture par IBM WebSphere Application Server Version 9.0.0.4 d'une sécurité plus faible que celle attendue après utilisation de la commande PasswordUtil pour activer le chiffrement de mot de passe AES.
  * Vulnérabilité dans laquelle Apache MyFaces Server pouvait permettre à un agresseur à distance d'obtenir des informations sensibles,
  * Vulnérabilité dans laquelle IBM WebSphere Application Server pouvait permettre à un agresseur à distance d'obtenir des informations sensibles, causée par une gestion impropre des erreurs par MyFaces dans JSF.
* Diverses maintenances de service ont été intégrées.

## 30 août 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.

## 30 juin 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 8.5.5.12 ou 9.0.0.4 soit installé avec les nouvelles instances de Traditional WebSphere Application Server.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 17.0.0.2 soit installé avec les nouvelles instances de WebSphere Application Server Liberty (plans Core et ND).
* Ajout d'une fonction [Advanced VPN Configuration Management](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#advancedVPN){: new_window} qui vous permet de créer et de gérer des configurations VPN multiples dans les régions de Londres et de Sydney.
* Optimisation de la fonction d'[accès public à Internet](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#publicInternetAccess){: new_window} qui permet aux clients de mieux gérer leur adresse IP publique.
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window} dans IBM SDK Java Technology Edition qui affectent WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité non spécifiée liée au composant Java SE AWT qui pouvait permettre à un agresseur non authentifié de prendre le contrôle du système.
  * Vulnérabilité non spécifiée liée au composant Java SE JCE qui pouvait permettre à un agresseur non authentifié de prendre le contrôle du système.
  * Vulnérabilité non spécifiée liée au composant Java SE JAXP qui pouvait permettre à un agresseur non authentifié de créer un déni de service ayant un impact important sur la disponibilité via des vecteurs d'attaque inconnus. 
  * Vulnérabilité non spécifiée liée au composant Java SE Networking qui pouvait permettre une attaque d'un agresseur non authentifié ayant peu d'impact sur la confidentialité ou sur l'intégrité et aucun impact sur la disponibilité.
  * Vulnérabilité non spécifiée liée au composant Java SE Networking qui pouvait permettre une attaque d'un agresseur non authentifié n'ayant pas d'impact sur la confidentialité et la disponibilité et peu d'impact sur l'intégrité.
  * Vulnérabilité non spécifiée liée au composant Java SE Security qui pouvait permettre une attaque d'un agresseur non authentifié n'ayant pas d'impact sur la confidentialité et la disponibilité et peu d'impact sur l'intégrité.
  * Vulnérabilité dans une erreur XML External Entity Injection (XXE) lors du traitement de données XML. Un agresseur à distance pouvait exploiter cette vulnérabilité pour exposer des informations hautement sensibles ou consommer des ressources mémoire.
  * Problème au cours duquel zlib était vulnérable à un déni de service, causé par une arithmétique de pointeur hors limites dans inftrees.c.
  * Problème au cours duquel zlib était vulnérable à un déni de service, causé par un décalage vers la gauche non défini d'un nombre négatif.
  * Problème au cours duquel zlib était vulnérable à un déni de service, causé par un pointeur hors limites au format big endian.

## 25 mai 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.
* Ajout d'une fonction [Advanced VPN Configuration Management](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#advancedVPN){: new_window} qui vous permet de créer et de gérer des configurations VPN multiples dans la région de Francfort.
* Mise à niveau des fichiers binaires de {{site.data.keyword.Bluemix_notm}} de façon à ce que JDK 8 soit installé avec les nouvelles instances du service.
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité de sécurité potentielle avec l'adaptateur de ressources WebSphere Application Server MQ JCA.
  * Vulnérabilité non spécifiée liée au composant Libraries qui pourrait permettre à un agresseur à distance d'obtenir des informations sensibles et aurait un impact élevé sur la confidentialité via des vecteurs d'attaque inconnus.

## 21 avril 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité dans laquelle WebSphere Application Server configuré avec OpenID Connect (OIDC) Trust Association Interceptor (TAI) pouvait permettre à un utilisateur d'obtenir des privilèges élevés sur le système.
  * Vulnérabilité dans laquelle WebSphere Application Server pouvait fournir une sécurité plus faible que celle attendue, permettant à un agresseur à distance d'exploiter cette faiblesse pour obtenir des informations sensibles et obtenir un accès non autorisé à la console d'administration.
  * Problème au cours duquel WebSphere Application Server était vulnérable à une falsification de requête intersites pouvant permettre à un agresseur d'exécuter des attaques malveillantes et non autorisées depuis un utilisateur certifié par le site Web.


## 15 mars 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 8.5.5.11 ou 9.0.0.3 soit installé avec les nouvelles instances de Traditional WebSphere Application Server.
* Correction de [plusieurs vulnérabilités de sécurité](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité non spécifiée liée au composant Libraries qui n'a pas d'impact sur la confidentialité, un impact élevé sur l'intégrité et aucun impact sur la disponibilité.
  * Vulnérabilité non spécifiée liée au composant Libraries qui pourrait permettre à un agresseur à distance d'obtenir des informations sensibles et aurait un impact élevé sur la confidentialité via des vecteurs d'attaque inconnus.
  * Vulnérabilité non spécifiée liée au composant Libraries qui pourrait permettre à un agresseur à distance de créer un déni de service et aurait un impact faible sur la disponibilité via des vecteurs d'attaque inconnus.
  * Vulnérabilité dans OpenSSL qui pourrait permettre à un agresseur à distance d'obtenir des informations sensibles, générée par une erreur dans le chiffrement DES/3DES et utilisée dans le cadre du protocole SSL/TLS.
  * Vulnérabilité qui permet aux utilisateurs d'imbriquer du code JavaScript arbitraire dans l'interface utilisateur Web, modifiant ainsi la fonctionnalité prévue et susceptible d'entraîner la divulgation des données d'identification dans une session digne de confiance.
  * Vulnérabilité dans Apache HTTPD en matière d'attaques de fractionnement de réponse HTTP, générée par la validation incorrecte de l'entrée fournie par l'utilisateur.
  * Vulnérabilité dans Samba, susceptible de permettre à un agresseur à distance authentifié d'obtenir des privilèges élevés sur le système, générée par l'échec du traitement de la somme de contrôle PAC.
  * Vulnérabilité dans Samba, susceptible de permettre à un agresseur à distance authentifié d'obtenir des privilèges élevés sur le système, générée par l'acheminement d'un ticket d'octroi d'autorisations vers un autre service lors de l'authentification Kerberos.
  * Vulnérabilité dans Samba face au dépassement de mémoire tampon basée sur des segments, générée par un défaut d'encapsulation d'entier dans la fonction ndr_pull_dnsp_name().


## 10 février 2017 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 8.5.5.11 ou 9.0.0.2 soit installé avec les nouvelles instances de Traditional WebSphere Application Server.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 16.0.0.4 soit installé avec les nouvelles instances de WebSphere Application Server Liberty (plans Core et ND).
* Correction de [plusieurs vulnérabilités de sécurité](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité de déni de service, générée par l'autorisation d'exécution accordée aux objets sérialisés provenant de sources non fiables, ce qui entraîne la consommation de ressources.
  * L'utilisation de demandes SOAP incorrectement formées, susceptibles de permettre à un agresseur à distance d'obtenir des informations sensibles.


## 16 décembre 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Diverses maintenances de service ont été intégrées.
* Correction de [plusieurs vulnérabilités de sécurité](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window} dans IBM SDK Java Technology Edition qui affectent WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité non spécifiée dans Oracle Java SE et Java SE Embedded liée au composant Hotspot qui a un impact élevé sur la confidentialité, l'intégrité et la disponibilité.
  * Vulnérabilité non spécifiée dans Oracle Java SE et Java SE Embedded liée au composant Networking, susceptible de permettre à un agresseur à distance d'obtenir des informations sensibles et qui a un impact élevé sur la confidentialité via des vecteurs d'attaque inconnus.
  *  Vulnérabilité en matière de cross-site scripting dans IBM WebSphere Application Server qui permet aux utilisateurs d'imbriquer du code JavaScript arbitraire dans l'interface utilisateur Web, modifiant ainsi la fonctionnalité prévue et susceptible d'entraîner la divulgation des données d'identification dans une session digne de confiance.


## 8 novembre 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Ajout d'une fonctionnalité permettant aux clients de demander une adresse [IP publique](networkEnvironment.html#networkEnvironment) pour leur machine virtuelle WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window} affectant WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité dans IBM WebSphere Application Server qui peut permettre aux agresseurs à distance d'exécuter du code Java arbitraire avec un objet sérialisé à partir de sources non fiables.
  * Vulnérabilité de déni de service due à une lecture hors limites de la fonction TS_OBJ_print_bio. Un agresseur à distance peut exploiter cette vulnérabilité en utilisant un fichier d'horodatage spécialement conçu pour provoquer l'arrêt de l'application.
  * Vulnérabilité potentielle dans OpenSSL qui peut permettre à un agresseur à distance d'obtenir des informations sensibles, causées par une erreur dans le Triple-DES sur le chiffrement par bloc de 64 bits, utilisé dans le cadre du protocole SSL/TLS. En capturant de grandes quantités de trafic chiffré entre le serveur SSL/TLS et le client, un agresseur à distance capable de mener une attaque d'interposition (man in the middle) peut exploiter cette vulnérabilité pour récupérer les données en clair et obtenir des informations confidentielles. Cette vulnérabilité est connue sous le nom d'attaque SWEET32 Birthday.
  * OpenSSL est vulnérable à un déni de service. En demandant à plusieurs reprises la renégociation, un agresseur à distance authentifié peut envoyer une extension de demande d'état OCSP trop grande pour consommer toutes les ressources de mémoire disponibles.
  * OpenSSL est vulnérable à un déni de service, causé par un dépassement d'entier dans la fonction MDC2_Update. En utilisant des vecteurs d'attaque inconnus, un agresseur à distance peut exploiter cette vulnérabilité pour déclencher une écriture hors limites et provoquer l'arrêt de l'application.
  * Vulnérabilité potentielle dans OpenSSL qui permet à un agresseur à distance d'obtenir des informations sensibles, provoquée par une erreur dans l'implémentation DSA qui permet le suivi d'un chemin de code temporel non constant pour certaines opérations. Un agresseur peut exploiter cette vulnérabilité en utilisant une attaque de synchronisation de cache pour récupérer la clé DSA privée.
  * OpenSSL est vulnérable à un déni de service, causé par des vérifications de longueur de message manquantes lors de l'analyse des certificats. Un agresseur à distance authentifié peut exploiter cette vulnérabilité pour déclencher une lecture hors limites et provoquer un déni de service.

## 19 septembre 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 16.0.0.3 soit installé sur les nouvelles instances de WebSphere Application Server Liberty (plans Core et ND).
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window} affectant WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité dans IBM WebSphere Application Server Liberty qui peut permettre à un agresseur à distance de mener des attaques de phishing.
  * Vulnérabilité dans IBM WebSphere Application Server Liberty sur le cross-site scripting dans les clients OpenID Connect.
  * Vulnérabilité potentielle dans IBM WebSphere Application Server Liberty qui peut permettre à un agresseur à distance d'obtenir des informations sensibles, causée par une mauvaise gestion des exceptions lorsqu'une page d'erreur par défaut n'existe pas.
  * Vulnérabilité dans Apache Tomcat à un déni de service, provoquée par une erreur dans le composant Apache Commons FileUpload.
  * Vulnérabilité dans IBM WebSphere Application Server et IBM WebSphere Application Server Liberty qui peut permettre à un agresseur à distance d'obtenir des informations sensibles, causée par le traitement inapproprié des réponses sous certaines conditions.
  * Vulnérabilité non spécifiée liée au composant Networking qui n'a pas d'impact sur la confidentialité, un impact faible sur l'intégrité et aucune disponibilité.

## 17 août 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de la version 8.5.5.9 à 8.5.5.10
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window} affectant WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilités Apache Struts impactant la console d'administration WebSphere Application Server et WebSphere Application Server Hypervisor Edition.
  * Déni potentiel de la vulnérabilité du service avec IBM WebSphere Application Server lors de l'utilisation de services SIP.
  * Plusieurs vulnérabilités pouvant impacter IBM HTTP Server utilisé par WebSphere Application Server.
  * Vulnérabilité permettant le réacheminement du trafic HTTP avec les applications CGI, pouvant impacter IBM HTTP Server (IHS). Cette vulnérabilité est connue comme étant "HTTPOXY".
  * Vulnérabilité de divulgation d'informations dans IBM WebSphere Application Server.
  * Vulnérabilité potentielle de contournement de la sécurité dans IBM WebSphere Application Server qui ne se produit que dans les environnements dans lesquels la propriété personnalisée webcontainer HttpSessionIdReuse est activée.


## 24 juin 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Nouvelle possibilité pour les clients de choisir entre V8.5 et V9.0 lors de la création d'une nouvelle instance _Traditional ND_ ou _Traditional WebSphere_.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de façon à ce que le groupe de correctifs 16.0.0.2 soit installé sur les nouvelles instances de WebSphere Application Server Liberty (plans Core et ND). 16.0.0.2 est le groupe de correctifs qui suit 8.5.5.9. En ce qui concerne 16.0.0.2, toutes les fonctions facultatives Liberty autorisées prises en charge pour ces plans sont installées par défaut.
* Correction de [plusieurs vulnérabilités de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window} affectant WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, incluant :
  * Vulnérabilité XML External Entity Injection (XXE) dans Apache Standard Taglibs qui affecte IBM WebSphere Application Server.
  * Possibilité d'une faiblesse de sécurité lors de l'utilisation de la fonction API Discovery appliquée au profil WebSphere Application Server Liberty et des documents Swagger.
  * Vulnérabilité potentielle de divulgation d'informations dans le centre d'administration pour IBM WebSphere Application Server Liberty.
  * Vulnérabilité potentielle de fractionnement des réponses HTTP dans IBM WebSphere Application Server.
  * Vulnérabilités OpenSSL révélées le 3 mai 2016 par OpenSSL Project.

## 13 juin 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Nouvelle possibilité pour les clients de générer, mettre à disposition, gérer et supprimer des instances de machine virtuelle via la création d'une application ou d'un script qui utilise des API RESTful de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.
* Nouvelle fonction qui permet à un client d'avoir un nombre fixe d'instances STOPPED ne comportant pas plus de 10 adresses IP ou 64 Go de mémoire. Les clients sont désormais facturés pour les instances accumulées à l'état STOPPED à un taux réduit de 5 %.

## 26 avril 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Correction de [vulnérabilités potentielles en matière de sécurité](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window} dans WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} si FIPS 140-2 est activé, et de plusieurs vulnérabilités dans Samba - dont Badlock.
* Diverses maintenances de service ont été intégrées.

## 15 avril 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de la version 8.5.5.8 à la version 8.5.5.9
* Correction d'une vulnérabilité à une attaque [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window} dans Liberty for Java for IBM {{site.data.keyword.Bluemix_notm}} affectant les consommateurs utilisant le client OpenID Connect (OIDC).
* Diverses maintenances de service ont été intégrées.

## 19 février 2016 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Ajout d'une option pour les clients avec des applications gourmandes en mémoire leur permettant de redimensionner leur environnement avec des machines
virtuelles
plus grandes. Les clients peuvent sélectionner la taille de ressource spécifique d'un composant WebSphere Application Server ou d'un seul système en leur
allouant des machines virtuelles dotés de jusqu'à 32 Go de mémoire RAM.
* Mise à niveau des fichiers binaires de {{site.data.keyword.Bluemix_notm}} de la version 8.5.5.7 à 8.5.5.8
* Correction de plusieurs vulnérabilités dans IBM SDK Java Technology Edition affectant WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}, désignées par l'acronyme [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}.
* Correction d'une vulnérabilité à une attaque par [Cross-site scripting](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window} affectant les consommateurs de la sortie du fournisseur OAuth.
* Diverses maintenances de service ont été intégrées.

## 11 décembre 2015 : Mise à jour de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* Le nom officiel du produit IBM Application Server on Cloud in {{site.data.keyword.Bluemix_notm}} a été remplacé par IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}.
* Ajout de nouvelles fonctions au plan WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment. Il se compose d'un environnement de cellule WebSphere Application Server Network Deployment avec deux machines virtuelles, ou plus. Ces nouvelles fonctions permettent aux utilisateurs de configurer un environnement en cluster pour la haute disponibilité, la reprise en ligne et l'évolutivité.
* Ajout de nouvelles fonctions au plan WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Liberty Core. Le plan inclut l'utilisation d'une collectivité Liberty, qui est un domaine d'administration pour un groupe de profils Liberty (serveurs) et qui se compose de deux machines virtuelles, ou plus.
* Mise à niveau des fichiers binaires de WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} de la version 8.5.5.6 à 8.5.5.7.
* Une [vulnérabilité d'Apache Commons Collections](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window} a été traitée pour la désérialisation des objets Java.
* Vulnérabilité permettant une [attaque par séparation de réponse HTTP](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window} a été traitée.
* Diverses maintenances de service ont été intégrées.

## 15 octobre 2015 : Mise à jour d'Application Server on Cloud
* Ajout des deux nouveaux plans suivants :
  * [WebSphere Application Server Traditional V9 Beta](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* Diverses maintenances de service
