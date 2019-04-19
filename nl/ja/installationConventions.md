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

# インストール規則
{: #installation_conventions}

## 管理のヒント
{: admin_tips}

{{site.data.keyword.appserver_full}} 環境を管理していて、どのユーザーがこの環境を使用するか決定する必要がある場合、以下の概念を理解することが重要です。

 * 保守は、`/home/virtuser/IBM/Installation Manager` ディレクトリーにインストールされている、[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} を使用して適用できます。 基礎のバイナリー・ファイルは `virtuser` (制限付き管理仮想ユーザー) としてインストールされているため、すべてのフィックスパックおよび暫定修正は `virtuser` としてインストールするようにしてください。

 * ただし、コマンド・ラインからサーバーを始動および停止する場合、`virtuser` ではなく `wsadmin` (WebSphere 管理 ID) を使用する必要があります。

## セルのインストール規則
{: cell_installation_conventions}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} セルは、標準化されたディレクトリー構造に従ってインストールおよび構成されます。 以下のリストは、いくつかの重要な設定に言及しています。  これらの設定の完全なリストについては、`/etc/virtualimage.properties` を参照してください。

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Liberty 集合のインストール規則

Liberty 集合は、標準化されたディレクトリー構造に従ってインストールおよび構成されます。 以下のリストは、いくつかの重要な設定に言及しています。  これらの設定の完全なリストについては、`/etc/virtualimage.properties` を参照してください。

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
