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

# 安裝慣例
{: #installation_conventions}

## 管理提示
{: admin_tips}

如果您管理 {{site.data.keyword.appserver_full}} 環境，而且需要判斷要使用的使用者，請務必瞭解下列概念：

 * 使用 `/home/virtuser/IBM/Installation Manager` 目錄中所安裝的 [Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window}，可以套用維護。因為是以 `virtuser`（有限管理虛擬使用者）身分安裝基礎二進位檔，所以請確定以 `virtuser` 身分安裝所有修正套件及臨時修正程式。

 * 不過，當您從指令行啟動及停止伺服器時，請務必使用 `wsadmin`（WebSphere 管理 ID），而非 `virtuser`。

## Cell 安裝慣例
{: cell_installation_conventions}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Cell 是遵循標準化目錄結構所安裝及配置。下列清單記錄一些重要的設定。如需完整的設定清單，請參閱 `/etc/virtualimage.properties`。

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Liberty 群體安裝慣例

Liberty Collective 是遵循標準化目錄結構所安裝及配置。下列清單記錄一些重要的設定。如需完整的設定清單，請參閱 `/etc/virtualimage.properties`。

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
