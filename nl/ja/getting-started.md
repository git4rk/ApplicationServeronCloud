---

copyright:
  years: 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# 入門チュートリアル
{:#getting-started}

{{site.data.keyword.appserver_full}} を使用すると、事前構成済みの WebSphere Application Server traditional または Liberty 環境を数分でセットアップできます。この入門チュートリアルでは、数回の手順で仮想マシンに WebSphere Application Server 環境をプロビジョンする方法をガイドします。
{: shortdesc}

## 始めに
{: #prereqs}

予約契約やシングル・テナント環境など、専用の仮想マシン・リソースを備えた環境が必要な場合は、サービスを作成する前に IBM 営業担当員に問い合わせる必要があります。これらのオプションについて詳しくは、[製品情報](index.html)を参照してください。

## ステップ 1: サービスの作成
{: #create}

1. {{site.data.keyword.cloud_notm}} カタログの「[{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server)」ページに移動します。
1. IBMid を使用してログインするか、{{site.data.keyword.cloud_notm}} アカウントを登録します。
1. カタログ・ページで、サービス構成の選択内容を確認します。

  従量課金 (PAYG) 環境では、デフォルトの選択内容を使用するか、必要に応じて選択内容を変更します。予約契約またはシングル・テナント環境を使用する場合、以下のオプションに注意してください。

  * **予約契約:** **「デプロイする地域/ロケーションの選択」**で、選択されている地域が契約の正しい地域であることを確認します。

  * **シングル・テナント環境:** **「デプロイする地域/ロケーションの選択」**で、選択されている地域がシングル・テナント環境をデプロイする地域であることを確認します。**「環境」**で、目的のシングル・テナント環境を選択します。デフォルトでは、パブリック環境が表示される場合があります。

目的のシングル・テナント環境がリストに表示されない場合、正しい地域を選択していること、および組織にそのシングル・テナント環境へのアクセス権限があることを確認してください。
    {: tip}
1. デプロイする {{site.data.keyword.appserver_short}} のエディションの料金プランを選択します。
1. **「作成」**をクリックします。


## ステップ 2: 環境の選択
{: #choose_env}

{{site.data.keyword.appserver_short}} Base および Liberty Core プランでは、1 つのサーバーのみ使用されます。したがって、これらのプランを選択する場合、このステップはスキップしてかまいません。

Network Deployment プランの場合、環境のプロファイルおよびアーキテクチャーを選択します。

* **プロファイル:** {{site.data.keyword.appserver_short}} traditional または Liberty を選択します。
* **アーキテクチャー:** シングル・サーバー環境、あるいは traditional セルまたは Liberty 集合によるクラスター環境を選択します。


## ステップ 3: 仮想マシンのサイジング
{: #vm_sizing}

環境内のコンポーネントごとに仮想マシンを個別にサイジングできます。仮想マシンのサイジングは、リソース・ブロックの [T シャツ・サイズ](index.html#vm-size)でチャンク化されます。

コンポーネント (サーバー、デプロイメント・マネージャー、アプリケーション・ノードなど) のタブをクリックし、その仮想マシンの T シャツ・サイズを選択します。

## ステップ 4: 環境のプロビジョン
{: #service_profile}

サービス構成サマリーで詳細 (プロビジョンに要する推定時間など) を確認します。**「プロビジョン」**をクリックして {{site.data.keyword.appserver_short}} 環境をセットアップします。

## 次のステップ
{: #anchor_value}

[システム・アクセス](systemAccess.html)で、新しい {{site.data.keyword.appserver_short}} 環境のアクセス方法および管理方法を学習します。
