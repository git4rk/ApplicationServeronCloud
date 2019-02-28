---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 製品情報
{: #about}

{{site.data.keyword.appserver_full}} を使用すると、{{site.data.keyword.Bluemix_notm}} でホストされるクラウド環境で、事前構成済みの WebSphere Application Server Liberty、Traditional Network Deployment、および Traditional WebSphere Java EE インスタンスを迅速にセットアップできます。
{: shortdesc}

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の概要
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} は、事前構成された Traditional WebSphere および Liberty サーバーを利用者に提供します。 これは、ゲスト・オペレーティング・システムへの root アクセス権限を持つ仮想マシン・ゲストでホストされます。 サービスを作成するときに、_Liberty_、_Traditional ND_、または _Traditional WebSphere_ のいずれかを選択します。

**注:** 利用者は、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} インスタンスを作成するときに、現行のフィックスパック・レベルまたは 1 つ古いバージョン [(n または n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} を選択できるようになりました。

使い慣れた WebSphere 管理操作を使用し、基盤オペレーティング・システムへの全アクセス権限を持つことができます。 既存のスクリプトを再使用可能で、独自のフレームワークまたはサード・パーティーのフレームワークで動作させるために必要なシステム微調整を行います。 オンプレミスの WebSphere 構成と同様に、WebSphere Application Server Liberty、ND、または Traditional のサービスを管理するために、管理センターと管理コンソールが提供されています。

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment プランは、2 つ以上の仮想マシンを使用する WebSphere Application Server Network Deployment セル環境で構成されています。 1 つ目の仮想マシンには、Deployment Manager と IBM HTTP Server が含まれており、残りの仮想マシンには、Deployment Manager に統合されたカスタム・ノード (ノード・エージェント) が含まれています。 既存の wsadmin スクリプトを使用して WebSphere 構成を作成するか、WebSphere 管理コンソールを使用して手動で環境を作成します。 これらの新機能により、すべてのミドルウェア・エンタープライズ・アプリケーションの重要な側面であるクラスター環境をセットアップすることができます。 クライアントは、トポロジーをクラスター化して、2 つ以上のインスタンスに要求をロード・バランシングすることを選択できるようになりました。

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment Plan には、Liberty 集合の使用も含まれます。 Liberty 集合は、Liberty プロファイル (サーバー) のグループの管理ドメインであり、2 つ以上の仮想マシンで構成されています。 1 つ目の仮想マシンには、Liberty 集合の制御点である集合コントローラー Liberty サーバーが含まれています。 Liberty 集合に加え、この仮想マシンには、Web ブラウザーからアプリケーションへのアクセスが可能な IBM HTTP Server も含まれています。 残りの仮想マシンは、集合メンバーが常駐する集合ホスト (Liberty プロファイル・サーバー) です。 Liberty 管理センター機能も、Liberty コントローラー・サーバーで有効になります。

次の図は、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment セル環境と Liberty 集合環境のアーキテクチャーを示しています。

図 1. Network Deployment セルと Liberty 集合のアーキテクチャー

![図 1. Network Deployment セルと Liberty 集合のアーキテクチャー](images/CellCollectiveDiagram.gif)

**注**: 上の_図 1_ で、Deployment Manager または集合コントローラーと IBM HTTP Server との連結を表すパターンは、開発およびテストの目的を想定しています。 また、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、実動適用および運用上の必要性に合わせたインストール済みソフトウェアの再構成を、オンプレミスの場合と同様に自由に行うことができます。 さらに、厳密な実働要件については、IBM 営業担当員にご連絡ください。隔離されたネットワーキングおよび計算リソースを提供する単一テナントの IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} オファリングについてご説明します。


## 稼働環境
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} は、利用者がアプリケーションをデプロイするための共有環境にゲスト (仮想マシン) を戻すサービスです。 VPN によって、汎用ポート・スキャンや他の一方的なネットワーク・ベースの攻撃からパブリック・サービスが保護されます。 ただし、サービス・インスタンスへのアクセスに使用するサービス VPN は、
複数の {{site.data.keyword.Bluemix_notm}}
組織およびユーザーの間で共有される可能性があるため、注意する必要があります。 仮想マシンでは、IaaS リソースの共有プールから、計算、メモリー、および入出力のリソースを提供します。

計算、メモリー、および入出力の個々のリソースは共有環境で仮想マシンによって実行されるため、サービス構成が異なる可能性があります。 特定の各サービス・インスタンスの構成は、IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} サービスのダッシュボードおよびポータルから表示できます。

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} は、仮想マシン・インスタンスを提供します。 それらのインスタンスにより、クライアントは単純なポータルを使用してエンタープライズの WebSphere Application Server デプロイメントを一貫性のある反復可能な方法で作成および管理し、非常に柔軟にアプリケーションをチューニングします。 ユーザーは、事前構成済みの WebSphere Application Server Liberty、ND、または Traditional の仮想マシンを、ホストされたクラウド環境で稼働させることができます。 ユーザーは既存の WebSphere Application Server アプリケーションを {{site.data.keyword.Bluemix_notm}} にマイグレーションし、基盤 OS およびミドルウェアを完全に制御できます。

## 仮想マシンのサイジング
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} は T シャツ形式のサイジングを提供しています。これにより、より大きな仮想マシンをプロビジョンすることで、メモリーを大量に使用するアプリケーション用の環境を適切なサイズにすることができます。 WebSphere Application Server を実行するためにプロビジョンする各仮想マシンは、予想されるリソースのニーズに応じて個別にサイズを変更できます。

仮想マシンは、*ブロック*単位でサイズと料金が決まります。 T シャツ・サイズのブロックごとに、仮想マシンに次のリソースがプロビジョンされます。
* 1 つの仮想 CPU (vCPU)
* 2 GB の RAM
* 12.5 GB のハード・ディスク・スペース (単一ブロックの VM に対して 12.0 GB)


| T シャツ | ブロック | vCPU | RAM (GB) | HD (GB) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
| S | 1 | 1 | 2 | 12 |
| M | 2 | 2 | 4 | 25 |
| L | 4 | 4 | 8 | 50 |
| XL | 8 | 8 | 16 | 100 |
| XXL | 16 | 16 | 32 | 200 |
{: caption="表 1. T シャツ・サイズ当たりのブロック" caption-side="top"}

各サーバーまたはノードは、単一の仮想マシンにプロビジョンされます。 例えば、Network Deployment プランで、デプロイメント・マネージャー用に M サイズ (2 ブロック) の仮想マシンを 1 つプロビジョンし、アプリケーション・ノード用に S サイズ (1 ブロック) の仮想マシンを 8 つプロビジョンすると、合計で 10 ブロックの料金が発生します。

## 課金オプション
{: #billing-options}

ブロック当たりの料金は、選択する課金オプションによって決まります。
* **[従量制課金](#pay-as-you-go):** 時間単位で使用されるブロック当たりの料金が決まる使用量ベースの課金
* **[予約契約](#reserve-contract):** 予約済みリソースに対する月額前払サブスクリプション料金

### 従量制課金
{: #pay-as-you-go}

別の課金オプションについて IBM 営業担当員に問い合わせずに IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} サービスをプロビジョンすると、従量制課金が適用されます。 月単位の課金期間中、各ブロックが使用された全時間または一部の時間について課金が行われます。 最小の課金は、ブロック時間の 1/4 で設定されます。

**注**: 一定量の計算、メモリー、および入出力のリソースのために、停止状態のインスタンスに対しては、時間単位のブロック率の 5% が削減されて課金されます。 サービス内では、停止状態のインスタンスは 10 個の IP アドレスまたは 64 GB のメモリーに制限されます。

#### プランの料金設定

ブロック当たりの料金は、選択した WebSphere Application Server プランによって異なります。

次の表に、T シャツ・サイズの各仮想マシンの時間当たりの合計料金をリストします。 これらの料金は、2016 年 4 月 1 日現在の IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} プランの料金で、US ドル (USD) で示されています。 お住まいの地域での現在の料金については、カタログを参照してください。

| T シャツ | ブロック | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
| S | 1 | $0.21 | $0.30 |  $0.70 |
| M | 2 | $0.42 | $0.60 |  $1.40 |
| L | 4 | $0.84 | $1.20 |  $2.80 |
| XL | 8 | $1.68 | $2.40 |  $5.60 |
| XXL | 16 | $3.36 | $4.80 |  $11.20 |
{: caption="表 2. Liberty Core プラン" caption-side="top"}


### 予約契約
{:#reserve-contract}

予約契約課金では、月額前払のサブスクリプション料金を支払います。これにより、物理的に予約された計算リソースのブロックへのアクセスが保証されます。 これらのサービス・ブロックは、そのユーザー専用として予約され、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の他のユーザーに対して使用できる容量ではなくなります。 既存の WebSphere Application Server ライセンスがある場合は、それらのライセンスを使用する請求レートの低い、「独自ライセンス使用」の予約契約を選択できます。 予約契約課金をセットアップするには、[IBM 営業担当員にお問い合わせ](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)ください。

サブスクリプションは、8 ブロック単位で増やすことができます。 合計ブロック時間は、その月の時間数に基づきますが、その月の間はずっとブロック時間を使用できます。 例えば、30 日の月は、換算すると 720 時間で、これに 8 ブロックのサブスクリプションを乗算すると、ブロック時間は合計 5,760 となります。

  ```
30 日 * 24 時間 (1 日) * 8 ブロック = 5,760 ブロック時間
  ```

さまざまな作業負荷の需要に応じて、いつどのようにブロックを使用するか調整できます。例えば、4 ブロック使用し、12 ブロックに増やし、その後 8 ブロックに減らすことなどができます。 その月の合計ブロック時間内であれば、追加料金はかかりません。

各環境をプロビジョンするときに、予約契約ブロックを使用するか、従量課金 (PAYG) 請求処理を使用するかを選択できます。

**注:** サービス・インスタンスを削除すると、そのブロックが新規サービス・インスタンスで使用できるようになるまで、約 30 分間待機する必要があります。

#### 超過

使用量がサブスクリプションの月単位のブロック時間を超過した場合、従量制課金モデルに従い超過料金が発生します。この場合、使用した超過ブロック時間に対してのみ課金が行われます。 ブロック使用量は、全時間または一部の時間に基づき計算されます (最小使用量はブロック時間の 1/4)。

従量制課金モデルのブロックは、予約された容量ではなく、共通リソース・プールから取得されます。

#### 柔軟な使用のための比例配分率

予約契約課金のブロックは WebSphere Application Server Network Deployment プランに基づきますが、他のプランでもブロックを使用できます。 他のプランでは、使用量は比例配分されます。このため、これが残りの予約契約ブロック時間に反映されると、プランの比例配分率により 1 ブロック時間削減されます。

次の表は、各プランの比例配分率、および比例配分が計算された後の実際のブロック時間当たりの有効料金を示しています。 お住まいの地域の現在の料金については、[IBM 営業担当員にお問い合わせ](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)ください。

| プラン | 比例配分率 | 比例配分後の料金/時間 |
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0.3 | $0.21 |
| WebSphere Application Server Base  | 0.43 | $0.30 |
| WebSphere Application Server Network Deployment | 1.0 | $0.70 |
{: caption="表 3. プラン別のブロック時間の比例配分率" caption-side="top"}

例えば、M サイズ (2 ブロック) の WebSphere Application Server Base インスタンスが 51 時間実行されたとします。 予約契約で使用されたブロック時間を計算するには、実際のブロック時間に比例配分率を乗算します。この計算を行うと、合計ブロック時間は 43.86 となります。

```
2 ブロック * 51 時間 * 比例配分率 0.43 = 比例配分されたブロック時間 43.86
```

合計コストは同じままですが、比例配分されたプランの実際のブロック時間をより多く使用できます。これは、予約契約ブロック時間から差し引かれるためです。
{:.tip}
