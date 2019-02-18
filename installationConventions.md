---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Installation conventions
{: #installation_conventions}

## Administration tips
{: admin_tips}

When you are administering your {{site.data.keyword.appserver_full}} environment and need to determine which user to use, it is important to understand the following concepts:

 * Maintenance can be applied by using [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window}, which is installed in the `/home/virtuser/IBM/Installation Manager` directory. Since the underlying binary files are installed as `virtuser`, a limited administrative virtual user, ensure that all fix packs and interim fixes are installed as `virtuser`.

 * However, when you start and stop servers from the command line, be sure to use `wsadmin`, the WebSphere Administrative ID, not `virtuser`.

## Cell installation conventions
{: cell_installation_conventions}

A WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} cell is installed and configured following a standardized directory structure. The following list notes a few of the important settings.  See `/etc/virtualimage.properties` for a full list of the settings.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Liberty collective installation conventions

A Liberty collective is installed and configured following a standardized directory structure. The following list notes a few of the important settings.  See `/etc/virtualimage.properties` for a full list of the settings.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
