---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

keywords: install, installation manager, im, wsadmin, cell, collective, websphere, liberty, virtual image

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 安装约定
{: #installation_conventions}

## 管理提示
{: admin_tips}

在管理 {{site.data.keyword.appserver_full}} 环境并需要确定要使用哪个用户时，了解以下概念很重要：

 * 可以使用安装在 `/home/virtuser/IBM/Installation Manager` 目录中的 [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} 来应用维护。由于底层二进制文件是以 `virtuser`（受限的管理虚拟用户）身份安装的，因此请确保以 `virtuser` 身份安装所有修订包和临时修订。

 * 但是，通过命令行启动和停止服务器时，请确保使用 `wsadmin`（WebSphere 管理标识），而不要使用 `virtuser`。

## 单元安装约定
{: cell_installation_conventions}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 单元已安装，并且已遵循标准化目录结构进行配置。以下列表记录了一些重要的设置。请参阅 `/etc/virtualimage.properties`，以获取设置的完整列表。

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Liberty 集合体安装约定

Liberty 集合体已安装，并且已遵循标准化目录结构进行配置。以下列表记录了一些重要的设置。请参阅 `/etc/virtualimage.properties`，以获取设置的完整列表。

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
