---

copyright:
  years: 2017, 2018
lastupdated: "2018-02-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Installation conventions
{: #installation_conventions}

## Administration Tips
{: admin_tips}

When you are administering your WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} environment and need to determine which user to use, it is important to understand the following concepts:

 * Maintenance can be applied by using the [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} installed in the */home/virtuser/IBM/Installation Manager* directory. Since the underlying binaries are installed as **virtuser**, a limited administrative virtual user, ensure that all fix packs and interim fixes are installed as **virtuser**.

 * However, when you start and stop servers from the command line, be sure to use **wsadmin**, the WebSphere Administrative ID, not **virtuser**.

## Cell Installation Conventions
{: cell_installation_conventions}

A WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} cell is installed and configured following a standardized directory structure. The following list notes a few of the important settings.  See /etc/virtualimage.properties for a full list of the settings.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Liberty Collective Installation Conventions

A Liberty collective is installed and configured following a standardized directory structure. The following list notes a few of the important settings.  See /etc/virtualimage.properties for a full list of the settings.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
