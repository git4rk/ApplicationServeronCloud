---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# シングル・テナント環境
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}}: シングル・テナント環境は、独立した WebSphere ワークロード、完全統合されたハイブリッド環境、およびセキュア・データをお客様に提供するオファリングです。この入門ガイドの目的は、お客様が WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: シングル・テナント環境にアクセスして、管理できるよう支援する主要要素を示すことです。
{: shortdesc}


## 推奨ソフトウェア
{: #recommended_software}

シングル・テナント環境にアクセスするには、次のソフトウェアが必要です。
* {{site.data.keyword.Bluemix_notm}} でサポートされている Web ブラウザー:
    * Chrome: ご使用のオペレーティング・システム用の最新バージョン
    * Firefox: ご使用のオペレーティング・システム用の最新バージョンまたは最新の ESR バージョン
    * Internet Explorer: バージョン 10 または 11
    * Safari: Mac 用の最新バージョン
* Cloud Foundry コマンド・ライン・インターフェースのバージョン 6.5.1 以降 (最新リリースを使用できます)
* Git Bash (推奨)
    * [Git Bash](https://git-scm.com/downloads){: new_window} をダウンロードし、インストールしてください。


## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: シングル・テナント環境の概要
{: #overviewSTE}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: シングル・テナント・オファリングにより、利用者は、サービスの専用プライベート・インスタンス、プライベート・ネットワーキング、および独立したリソースを利用できます。このオファリングは独立して管理されますが、サービスおよび作成されたサービス・インスタンス・ダッシュボードには、以下の図に示すように、特定の {{site.data.keyword.Bluemix_notm}} パブリック地域を介してアクセスできます。

図 1. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: シングル・テナント環境のアーキテクチャー

![図 1. シングル・テナント環境のアーキテクチャー](images/WASaaS.png)


## 組織管理
{: #organization_management}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: シングル・テナント環境は、お客様のオーダーに従って構成されます。オーダーの一部として 1 つ以上の {{site.data.keyword.Bluemix_notm}} 組織名を指定した場合、ただちに環境へのアクセスを開始できます。1 つ以上の組織名を指定しなかった場合、またはこの設定を変更する場合、地域の {{site.data.keyword.Bluemix_notm}} コンソールから**アプリケーション・サービス**の[サポート・チケット](reportingIssues.html#reporting_issues)をオープンします。次の図に示されているように、組織名 (ORG) は {{site.data.keyword.Bluemix_notm}} コンソールの右上隅で見つけることができます。

図 2. 組織名の場所

![図 2. ORG 名の場所](images/myORG.png)


**注:** シングル・テナント環境へのアクセス方法については、[シングル・テナント環境へのアクセス](singleTenantAccess.html#singleTenantEnvironment)を参照してください。
