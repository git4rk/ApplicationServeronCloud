---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Convenções de Instalação
{: #installation_conventions}

## Dicas de administração
{: admin_tips}

Quando você está administrando o seu ambiente do {{site.data.keyword.appserver_full}} e precisa determinar qual usuário usar, é importante entender os conceitos a seguir:

 * É possível aplicar manutenção usando o [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} instalado no
diretório */home/virtuser/IBM/Installation Manager*. Como os binários subjacentes são instalados como **virtuser**, um usuário virtual administrativo limitado, assegure-se de que todos os fix packs e correções temporárias estejam instalados como **virtuser**.

 * No entanto, ao iniciar e parar servidores da linha de comandos, certifique-se de usar **wsadmin**, o ID administrativo do WebSphere, não **virtuser**.

## Convenções de Instalação de Cél
{: cell_installation_conventions}

Um WebSphere Application Server na célula do {{site.data.keyword.Bluemix_notm}} é instalado e configurado seguindo uma estrutura de diretório padronizada. A lista a seguir indica algumas das configurações importantes.  Veja /etc/virtualimage.properties para obter uma lista completa das configurações.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## convenções de instalação coletiva do Liberty

Um Liberty collective é instalado e configurado seguindo uma estrutura de diretório padronizada. A lista a seguir indica algumas das configurações importantes.  Veja /etc/virtualimage.properties para obter uma lista completa das configurações.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
