---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-18"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# 入門チュートリアル
{:#getting-started}

{{site.data.keyword.appserver_full}} を使用すると、事前構成済みの WebSphere Application Server traditional または Liberty 環境を数分でセットアップできます。 この入門チュートリアルでは、数回の手順で仮想マシンに WebSphere Application Server 環境をプロビジョンする方法をガイドします。
{: shortdesc}

## 始めに
{: #prereqs}

予約契約やシングル・テナント環境など、専用の仮想マシン・リソースを備えた環境が必要な場合は、サービスを作成する前に IBM 営業担当員にお問い合わせください。 これらのオプションについて詳しくは、[製品情報](/docs/services/ApplicationServeronCloud?topic=wasaas-about#about)を参照してください。

### 既存の WebSphere 環境のマイグレーション

既存の WebSphere Application Server Network Deployment 環境をこのサービスにマイグレーションするには、[WebSphere Configuration Migration Tool for {{site.data.keyword.cloud_notm}} ({{site.data.keyword.cloud_notm}} 用の WebSphere 構成マイグレーション・ツール) ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン ")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window} を使用します。 このツールは、スタンドアロン・サーバーまたはセル・ノードのプロファイル構成とアプリケーションを、{{site.data.keyword.cloud_notm}} のサービス・インスタンスにアップロードします。 クラウド・マイグレーションの概要と、このツールを使用したステップバイステップのウォークスルーについては、 WASdev の[WebSphere Configuration Migration Tool for IBM Cloud guide (IBM Cloud 用の WebSphere 構成マイグレーション・ツール・ガイド) ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window} を参照してください。

以下のステップでは、{{site.data.keyword.appserver_full}} で新しい環境を作成する方法を説明します。

## ステップ 1: サービスの作成
{: #create}

1. {{site.data.keyword.cloud_notm}} カタログの「[{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server)」ページに移動します。
1. IBMid を使用してログインするか、{{site.data.keyword.cloud_notm}} アカウントを登録します。
1. カタログ・ページで、サービス構成の選択内容を確認します。

  従量課金 (PAYG) 環境では、デフォルトの選択内容を使用するか、必要に応じて選択内容を変更します。

  予約契約またはシングル・テナント環境を使用する場合、以下のオプションに注意してください。

  * **予約契約:** **「デプロイする地域/ロケーションの選択」**で、選択されている地域が契約の正しい地域であることを確認します。

  * **シングル・テナント環境:** **「デプロイする地域/ロケーションの選択」**で、選択されている地域がシングル・テナント環境をデプロイする地域であることを確認します。 **「環境」**で、目的のシングル・テナント環境を選択します。 デフォルトでは、パブリック環境が表示される場合があります。

    目的のシングル・テナント環境がリストされない場合、正しい地域を選択していること、および組織にそのシングル・テナント環境へのアクセス権限があることを確認してください。
    {: tip}
1. デプロイする {{site.data.keyword.appserver_short}} のエディションの料金プランを選択します。
1. **「作成」**をクリックします。


## ステップ 2: 環境の選択 (Network Deployment のみ)
{: #choose_env}

{{site.data.keyword.appserver_short}} Base および Liberty Core プランでは、1 つのサーバーのみ使用されます。したがって、これらのプランを選択する場合、このステップはスキップしてかまいません。

Network Deployment プランの場合、環境のプロファイルおよびアーキテクチャーを選択します。

* **プロファイル:** {{site.data.keyword.appserver_short}} traditional または Liberty を選択します。
* **アーキテクチャー:** シングル・サーバー環境、あるいは traditional セルまたは Liberty 集合によるクラスター環境を選択します。


## ステップ 3: 仮想マシンのサイジング
{: #vm_sizing}

環境内のコンポーネントごとに仮想マシンを個別にサイジングできます。 仮想マシンは、リソース・ブロックの [T シャツ・サイズ](/docs/services/ApplicationServeronCloud?topic=wasaas-about#vm-size)でチャンク化されます。

コンポーネント (サーバー、デプロイメント・マネージャー、アプリケーション・ノードなど) のタブをクリックし、その仮想マシンの T シャツ・サイズを選択します。

## ステップ 4: 環境のプロビジョン
{: #service_profile}

サービス構成サマリーで詳細 (プロビジョンに要する推定時間など) を確認します。

**予約契約:** **「請求処理」**オプションが、「_予約契約_ 」に設定されていることを確認します。 このオプションが表示されていない場合は、[お客様の組織](/docs/account?topic=account-orgsspacesusers){:new_window}が、空白文字や大/小文字も含めて、契約上の組織名と完全に一致することを確認してください。 「予約契約」請求処理を選択せずにサービスをプロビジョンする場合は、「従量課金 (PAYG)」請求処理が使用されます。

**「プロビジョン」**をクリックして {{site.data.keyword.appserver_short}} 環境をセットアップします。

## 次のステップ
{: #anchor_value}

[システム・アクセス](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access)で、新しい {{site.data.keyword.appserver_short}} 環境のアクセス方法および管理方法を学習します。
