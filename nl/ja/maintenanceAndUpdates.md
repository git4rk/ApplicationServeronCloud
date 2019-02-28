---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 環境の更新
{: #updating-your-environment}

## 保守方針
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} は定期的に更新されており、新しいサービス・インスタンスが最新のフィックスパックとパッチを使用して作成されるようにしています。 クラウドによって、ミドルウェア管理で新しいサービス・インスタンスの容易かつ迅速なプロビジョンが実現されます。

特定の製品バージョンの現行または以前のフィックスパック・レベル (n または n-1) で WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} のインスタンスを作成できます。 現行のフィックスパックを使用すると、最新の更新および機能を利用できますが、ハイブリッド・クラウド・デプロイメントの要件に準拠するために以前のフィックスパックが必要になる場合もあります。

新しいインスタンスを作成する場合、サービス・インスタンスの**「サービス・プロファイル」**タブで、次のフィックスパック・レベルのいずれかを選択できます。

**Liberty**
  * 18.0.0.4
  * 18.0.0.3

**WebSphere Application Server traditional**
  * 9.0.0.10
  * 9.0.0.9
  * 8.5.5.14
  * 8.5.5.13

## フィックスおよびフィックスパックの更新の適用
{:#applying-fixes}

最新のメンテナンス・レベルに更新する最速の方法は、新しいインスタンスを作成することです。 ただし、存続期間の長いサービス・インスタンスを保持する場合は、次のセクションの説明に従い、提供されている `installService.sh` スクリプトを実行することで、または IBM Installation Manager を使用することで既存のインストールに対してメンテナンスを適用できます。

### installService.sh スクリプトを使用して更新する

サービス・インスタンスには、使用可能なセキュリティー・フィックスおよび WebSphere Application Server フィックスパックにより頻繁に更新される Installation Manager リポジトリーが構成されています。 `/home/virtuser/installService.sh` スクリプトを使用して、これらのフィックスおよびフィックスパックを適用できます。 このスクリプトは root ユーザーとして実行する必要があります。

更新をインストールする場合に必要なディスク・スペースの量は、インストールする更新のタイプによって異なります。 暫定修正のみインストールする場合、仮想マシン上に 1 GB の空き領域が必要です。 フィックスパックをインストールする場合、必要なディスク・スペースは 1.3 GB に増えます。

スクリプトを実行すると、次のアクションが実行されます。

* 実行中のすべての WebSphere Application Server インスタンスおよび IBM HTTP Server インスタンスが停止されます。
* オプションで、Installation Manager、WebSphere Application Server、IBM HTTP Server、および Java&trade; SDK 用の最新のフィックスパックがインストールされます。
* WebSphere、IBM HTTP Server、および Java&trade; SDK 用の最新の暫定修正がインストールされます。
* すべてのインスタンスが再始動されます。

#### オプション
* **`-fixpacks`**

    すべてのパッケージを最新のフィックスパックに更新します。
* **`-noprompt`**

    更新の前に確認のプロンプトが表示されなくなります。

#### 構文の例

```
./installService.sh -?
```
{:.codeblock}

ヘルプ・テキストを表示します。


```
./installService.sh
```
{:.codeblock}

適用可能なすべての暫定修正をインストールしますが、フィックスパックはインストールしません。


```
./installService.sh -fixpacks
```
{:.codeblock}

使用可能なすべてのフィックスパックをインストールし、その後、適用可能なすべての暫定修正をインストールします。

### Installation Manager を使用して更新する
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} は、`/home/virtuser/IBM/Installation Manager` ディレクトリーにインストールされ、フィックスおよびフィックスパックを適用するために直接実行できます。

**問題の回避:** 基礎となるバイナリー・ファイルは `virtuser` (制限付き管理仮想ユーザー) としてインストールされているため、Installation Manager も常に `virtuser` として実行する必要があります。

## 仮想マシンへのシステムの更新の適用
{:#vm-system-updates}

仮想マシンにシステムの更新を適用するのは、物理的な Red Hat Enterprise Linux&reg; (RHEL) システムを更新するのと似ています。 Yum パッケージ・マネージャーを使用することで、パッケージをインストール、更新、アンインストール、および管理できます。 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} システムは、IBM の Red Hat Satellite サーバーから更新を受信するように構成されており、これにより、Red Hat ネットワークから非常に安全なパッケージが提供されます。 Satellite サーバーは、IBM により管理されており、ご使用のシステムからは変更できません。

詳しくは、[
Applying package updates on Red Hat Enterprise Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} および
[Yum, the Red Hat package manager](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window} を参照してください。
