---

copyright:
  years: 2017, 2019
lastupdated: "2019-03-28"

keywords: update, fix pack, fixpack, version, whats new, new in release

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 最新更新情報
{: #latest_updates}

サービスの最新更新情報のリスト。

## 2019 年 4 月 5 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 9.0.0.11 フィックスパックを使用できるようになりました。9.0.0.11 に加えて、WebSphere Application Server traditional の他のフィックスパック (9.0.0.10、8.5.5.15、8.5.5.14 など) もプロビジョニングのために使用できます。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server Liberty の 19.0.0.3 フィックスパック・バージョンを使用できるようになりました。19.0.0.3 に加えて、WebSphere Application Server Liberty の 18.0.0.4 フィックスパック・バージョンもプロビジョニングのために使用できます。
* 各種サービス・メンテナンスを統合しました。

## 2019 年 3 月 7 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 8.5.5.15 フィックスパックを使用できるようになりました。8.5.5.15 に加えて、WebSphere Application Server traditional の他のフィックスパック (9.0.0.9、9.0.0.10、8.5.5.14 など) もプロビジョニングのために使用できます。
* 各種サービス・メンテナンスを統合しました。

## 2019 年 1 月 16 日: REST API 実装用の API エンドポイント URL を更新しました

ダラスの地域接頭部が `ng` から `us-south` に変更されました。 他の地域接頭部は同じままです。 REST API エンドポイント URL が `https://wasaas-broker.<region>.bluemix.net/wasaas-broker/api` から `https://wasaas-broker.<region>.websphereappsvr.cloud.ibm.com/wasaas-broker/api` に変更されました。 `bluemix.net` URL は引き続きサポートされますが、REST API を使用してサービス・インスタンスを管理している場合は、`websphereappsvr.cloud.ibm.com` を使用するように REST API エンドポイント URL を変更する必要があります。

REST API エンドポイント URL について詳しくは、[システム・アクセス](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access#system_access)を参照してください。

## 2018 年 12 月 14 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の  9.0.0.10 フィックスパックを使用できるようになりました。 9.0.0.10 に加えて、WebSphere Application Server traditional の他のフィックスパック (9.0.0.9、8.5.5.14、8.5.5.13 など) もプロビジョニングのために使用できます。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server Liberty の 18.0.0.4 フィックスパック・バージョンを使用できるようになりました。 18.0.0.4 に加えて、WebSphere Application Server Liberty の 18.0.0.3 フィックスパック・バージョンもプロビジョニングのために使用できます。
* 各種サービス・メンテナンスを統合しました。

## 2018 年 10 月 24 日: 予約契約およびシングル・テナント環境で、「独自ライセンス使用」請求処理が使用できるようになりました。

既存の WebSphere Application Server ライセンスがある場合は、それらのライセンスを予約契約またはシングル・テナント環境で使用できるようになりました。 「独自ライセンス使用」請求処理を行う環境では、標準予約契約またはシングル・テナント環境と同じメリットが提供されますが、請求レートは低くされています。 「独自ライセンス使用」を使用するには、[IBM 営業担当員にお問い合わせください](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。

## 2018 年 8 月 22 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 8.5.5.14 フィックスパックを使用できるようになりました。 8.5.5.14 に加えて、WebSphere Application Server traditional の他のフィックスパック (9.0.0.8、9.0.0.7、8.5.5.13 など) もプロビジョニングのために使用できます。
* 各種サービス・メンテナンスを統合しました。

## 2018 年 7 月 16 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 9.0.0.8 フィックスパック・バージョンを使用できるようになりました。 9.0.0.8 に加えて、WebSphere Application Server traditional の他のフィックスパック・バージョン (9.0.0.7、8.5.5.13、8.5.5.12 など) もプロビジョニングのために使用できます。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server Liberty の 18.0.0.2 フィックスパック・バージョンを使用できるようになりました。 18.0.0.2 に加えて、WebSphere Application Server Liberty の 18.0.0.1 フィックスパック・バージョンもプロビジョニングのために使用できます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、[いくつかのセキュリティー脆弱性](https://www-01.ibm.com/support/docview.wss?uid=ibm10717691){: new_window}に対処しました。
* IBM SDK Java Technology Edition では、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=ibm10718297){: new_window}に対処しました。

## 2018 年 6 月 13 日: 予約契約課金を使用できるようになりました

予約契約課金では、月額前払のサブスクリプション料金を支払います。これにより、物理的に予約された計算リソースのブロックへのアクセスが保証されます。 これらのサービス・ブロックは、そのユーザー専用として予約され、{{site.data.keyword.appserver_full}} の他のユーザーに対して使用できる容量ではなくなります。 その月の間、選択した任意の方法でサービス・ブロック時間を使用できます。このとき、通常の従量制課金サブスクリプション・モデルに従い超過料金が請求されます。

予約契約課金について詳しくは、[課金オプション](/docs/services/ApplicationServeronCloud?topic=wasaas-about#billing-options)を参照してください。

## 2018 年 3 月 30 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 9.0.0.7 フィックスパック・バージョンを使用できるようになりました。 9.0.0.7 に加えて、WebSphere Application Server traditional の他のフィックスパック・バージョン (9.0.0.6、8.5.5.13、8.5.5.12 など) もプロビジョニングのために使用できます。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server Liberty の 18.0.0.1 フィックスパック・バージョンを使用できるようになりました。 18.0.0.1 に加えて、WebSphere Application Server Liberty の 17.0.0.4 フィックスパック・バージョンもプロビジョニングのために使用できます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window}に対処しました。
  * IBM® Java SDK の複数の脆弱性。
  * 管理コンソールに対して IBM WebSphere Application Server で発生する可能性がある、予想を下回るセキュリティーの脆弱性。
  * フォーム・ログインを使用して IBM WebSphere Application Server をインストールする場合に発生する可能性がある、リモート攻撃者がスプーフィング攻撃を実行できる脆弱性。
  * アプリケーションの要求の不適切な処理が原因で (これにより、無許可アクセスでファイルを読み取ることができる可能性がある)、IBM WebSphere Application Server で発生する可能性がある、ローカル攻撃者が機密情報を入手できる脆弱性。
  * FileUpload ライブラリーの DiskFileItem クラスの非信頼データのデシリアライゼーションが原因で、複数の製品で使用される Apache Commons FileUpload で発生する可能性がある、リモート攻撃者がシステムで任意のコードを実行できる脆弱性。 リモート攻撃者は、この脆弱性を悪用して、現行プロセスのコンテキストで任意のコードを実行する可能性があります。
  * CPU の分岐命令の危険な実行機能の境界検査をバイパスすることが原因で、Intel Haswell Xeon、AMD PRO、および ARM Cortex A57 の各 CPU で発生する可能性がある、ローカルの認証済み攻撃者が機密情報を入手できる脆弱性。 攻撃者は、ターゲットとしたキャッシュのサイドチャネル攻撃を実行することでこの脆弱点を悪用し、シスコール (syscall) の境界を超えて、CPU 仮想メモリーのデータを読み取る可能性があります。
* 各種サービス・メンテナンスを統合しました。

## 2018 年 1 月 8 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 9.0.0.6 フィックスパック・バージョンを使用できるようになりました。 9.0.0.6 に加えて、WebSphere Application Server traditional の他のフィックスパック・バージョン (9.0.0.5、8.5.5.12、8.5.5.11 など) もプロビジョニングのために使用できます。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server Liberty の 17.0.0.4 フィックスパック・バージョンを使用できるようになりました。 17.0.0.4 に加えて、WebSphere Application Server Liberty の 17.0.0.3 フィックスパック・バージョンもプロビジョニングのために使用できます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window}に対処しました。
  * XML エンティティー解析時のエラーが原因で、OpenSAML で発生する可能性がある、リモートの認証済み攻撃者が機密情報を入手できる脆弱性。
  * HTTP OPTIONS メソッド (別名 Optionsbleed) の不具合が原因で、Apache HTTP Server で発生する可能性がある、リモート・アタッカーが機密情報を入手できる脆弱性。
  * apr_sdbm*() 関数で使用される SDBM データベース・ファイルの整合性検証の失敗が原因で、Apache Portable Runtime Utility (APR-util) で発生する可能性がある、サービス妨害を受ける脆弱性。
* 各種サービス・メンテナンスを統合しました。

## 2017 年 12 月 21 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* ダラス、ロンドン、およびシドニーで、WebSphere Application Server in IBM Cloud マイグレーション機能が追加されました。 この機能により、既存の v7、v8、または v8.5.5 オンプレミス環境から IBM Cloud での v9 環境への完全なエンドツーエンドのマイグレーションが実現します。 詳しくは、[WebSphere Configuration Migration Tool for IBM Cloud](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud) を参照してください。
* 各種サービス・メンテナンスを統合しました。

## 2017 年 10 月 27 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* {{site.data.keyword.Bluemix_notm}} サービス・ダッシュボードの「サービス・プロファイル」タブを通じて、または REST API を通じて、以前のフィックスパック・レベル [(n-1)](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window} をプロビジョンできるようになりました。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server traditional の 9.0.0.5 フィックスパック・バージョンを使用できるようになりました。 9.0.0.5 に加えて、WebSphere Application Server traditional の他のフィックスパック・バージョン (9.0.0.4、8.5.5.12、8.5.5.11 など) もプロビジョニングのために使用できます。
* 新しいサービス・インスタンスをプロビジョンするとき、WebSphere Application Server Liberty の 17.0.0.3 フィックスパック・バージョンを使用できるようになりました。 17.0.0.3 に加えて、WebSphere Application Server Liberty の 17.0.0.2 フィックスパック・バージョンもプロビジョニングのために使用できます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window}に対処しました。
  * カスタム・スタートアップ・スクリプトの使用時に IBM WebSphere Application Server で発生する可能性がある、カスタマイズ済みのアクセス権ではなくデフォルトのアクセス権を使用してファイルが作成される脆弱性。
  * 失効したデータがキャッシュされ、取得されることが原因で、IBM WebSphere Application Server Proxy Server またはオンデマンド・ルーター (ODR) で発生する可能性がある、ローカル攻撃者が機密情報を入手できる脆弱性。
  * クロスサイト・スクリプティング攻撃に対する IBM WebSphere Application Server の脆弱性。 この脆弱性により、ユーザーは Web UI に任意の JavaScript コードを埋め込むことができ、機能を故意に変更できます。それが原因で、信頼されたセッション内で資格情報の漏えいが発生する恐れがあります。
  * 管理コンソールを使用して Web サービスのセキュリティー・バインディング設定を更新した後に、IBM WebSphere Application Server で発生する可能性がある、予想を下回るセキュリティーの脆弱性。
  * PasswordUtil コマンドを使用して AES パスワードの暗号化を有効にした後に、IBM WebSphere Application Server バージョン 9.0.0.4 で発生する可能性がある、予想を下回るセキュリティーの脆弱性。
  * Apache MyFaces で発生する可能性がある、リモート攻撃者が機密情報を入手できる脆弱性。
  * JSF の MyFaces による不適切なエラー処理が原因で、IBM WebSphere Application Server で発生する可能性がある、リモート攻撃者が機密情報を取得できる脆弱性。
* 各種サービス・メンテナンスを統合しました。

## 2017 年 8 月 30 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。

## 2017 年 6 月 30 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server traditional の新しいインスタンスにフィックスパック 8.5.5.12 や 9.0.0.4 がインストールされるようになりました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server Liberty (Core および ND Plans) の新しいインスタンスにフィックスパック 17.0.0.2 がインストールされるようになりました。
* ロンドンおよびシドニー地域で、複数の VPN 構成の作成および管理に使用できる[拡張 VPN 構成管理](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#advancedVPN){: new_window}機能が追加されました。
* [パブリック・インターネット・アクセス](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#publicInternetAccess){: new_window}機能に機能拡張が追加され、クライアントがパブリック IP アドレスをより適切に管理できるようになりました。
* IBM SDK Java Technology Edition では、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、以下のような[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window}に対処しました。
  * 非認証の攻撃者がシステムを制御できる可能性がある Java SE AWT コンポーネントの詳細不明の脆弱性。
  * 非認証の攻撃者がシステムを制御できる可能性がある Java SE JCE コンポーネントの詳細不明の脆弱性。
  * 非認証の攻撃者が、不明な攻撃ベクトルを使用してサービス妨害を実行でき、その結果、高可用性が影響を受ける可能性がある、Java SE JAXP コンポーネントの詳細不明の脆弱性。
  * 非認証の攻撃者が攻撃しても機密性への影響は低く、整合性への影響も低く、また可用性への影響はない Java SE Networking コンポーネントの詳細不明の脆弱性。
  * 非認証の攻撃者が攻撃しても機密性への影響はなく、整合性への影響は低く、また可用性への影響はない Java SE Networking コンポーネントの詳細不明の脆弱性。
  * 非認証の攻撃者が攻撃しても機密性への影響はなく、整合性への影響は低く、また可用性への影響はない Java SE Security コンポーネントの詳細不明の脆弱性。
  * XML データの処理時に発生する XML External Entity Injection (XXE) エラーに対する脆弱性。 リモート攻撃者は、この脆弱性を悪用して、機密度の高い情報を漏えいさせる可能性や、メモリー・リソースを浪費させる可能性があります。
  * inftrees.c での境界外ポインターの算術演算が原因で発生する、サービス妨害に対する zlib の脆弱性の問題。
  * 負数の未定義の左シフトが原因で発生する、サービス妨害に対する zlib の脆弱性の問題。
  * ビッグ・エンディアンの境界外ポインターが原因で発生する、サービス妨害に対する zlib の脆弱性の問題。

## 2017 年 5 月 25 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。
* フランクフルト地域で、複数の VPN 構成の作成および管理に使用できる[拡張 VPN 構成管理](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#advancedVPN){: new_window}機能が追加されました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、サービスの新しいすべてのインスタンスで JDK 8 がインストールされるようになりました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window}に対処しました。
  * WebSphere Application Server MQ JCA リソース・アダプターにあった潜在的なセキュリティーの脆弱性。
  * リモート・アタッカーが不明な攻撃ベクトルを使用して機密情報を取得し、その結果、機密性に高い影響を与える可能性がある、Libraries コンポーネントの詳細不明の脆弱性。

## 2017 年 8 月 21 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window}に対処しました。
  * OpenID Connect (OIDC) Trust Association Interceptor (TAI) が構成された WebSphere Application Serverで発生する可能性のある、ユーザーがシステムの上位特権を取得できる脆弱性。
  * WebSphere Application Server で発生する可能性のある、予想を下回るセキュリティーの脆弱性。 リモート攻撃者は、この脆弱性を悪用して、機密情報を入手する可能性、および管理コンソールに無許可アクセスする可能性があります。
  * クロスサイト・リクエスト・フォージェリーに対する WebSphere Application Server の脆弱性の問題。これが原因で、攻撃者は、Web サイトが信頼しているユーザーからの送信により、悪意のあるアクションや不正なアクションを実行する可能性があります。


## 2017 年 3 月 15 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server traditional の新しいインスタンスにフィックスパック 8.5.5.11 や 9.0.0.3 がインストールされるようになりました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window}に対処しました。
  * 機密性への影響はなく、保全性に対する高い影響があり、可用性への影響はない、Libraries コンポーネントの詳細不明の脆弱性。
  * リモート・アタッカーが不明な攻撃ベクトルを使用して機密情報を取得し、その結果、機密性に高い影響を与える可能性がある、Libraries コンポーネントの詳細不明の脆弱性。
  * リモート・アタッカーが不明な攻撃ベクトルを使用してサービス妨害を引き起こし、その結果、可用性を低くする影響を与える可能性のある、Libraries コンポーネントの詳細不明の脆弱性。
  * SSL/TLS プロトコルの一部として使用される DES/3DES 暗号で発生するエラーに起因し、リモート・アタッカーが機密情報を取得する可能性のある、OpenSSL の脆弱性。
  * ユーザーが Web UI に任意の JavaScript コードを埋め込むことができるため、信頼されたセッション内で資格情報の漏えいにつながる恐れのある、機能を故意に変更できるという脆弱性。
  * ユーザー入力の不適切な検証によって引き起こされる、Apache HTTPD から HTTP 応答の分割アタックに存在する脆弱性。
  * PAC チェックサム処理の失敗により、リモートで認証されたアタッカーがシステム上で高い権限を得る可能性のある、Samba 内の脆弱性。
  * Kerberos 認証使用時にチケット許可チケット (TGT、Ticket Granting Ticket) を他のサービスに転送することにより、リモートで認証されたアタッカーがシステム上で高い権限を得る可能性のある、Samba 内の脆弱性。
  * ndr_pull_dnsp_name() 関数の整数ラップ・フローが原因で生じるヒープ・ベースのバッファー・オーバーフローに対する、Samba 内の脆弱性。


## 2017 年 2 月 10 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server traditional の新しいインスタンスにフィックスパック 8.5.5.11 や 9.0.0.2 がインストールされるようになりました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server Liberty (Core および ND Plans) の新しいインスタンスにフィックスパック 16.0.0.4 がインストールされるようになりました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} では、以下のような[いくつかのセキュリティー脆弱性](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window}に対処しました。
  * 信頼できないソースからのシリアライズド・オブジェクトを実行し、リソースの消費を引き起こすことによる、サービス妨害の脆弱性。
  * リモート・アタッカーが機密情報を取得する可能性がある、不正な SOAP 要求の使用。


## 2016 年 12 月 16 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 各種サービス・メンテナンスを統合しました。
* IBM SDK Java Technology Edition では、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、以下のような[いくつかのセキュリティー脆弱性](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window}に対処しました。
  * 機密性、保全性、および可用性に対して高い影響がある、Hotspot コンポーネントに関連する、Oracle Java SE および Java SE Embedded にある未指定の脆弱性。
  * 不明な攻撃ベクトルを使用して、リモート・アタッカーが機密情報を取得する可能性があり、その結果、機密性に高い影響を与える、Networking コンポーネントに関連する Oracle Java SE および Java SE Embedded にある未指定の脆弱性。
  *  ユーザーが任意の JavaScript コードを Web UI に埋め込むことができる、IBM WebSphere Application Server のクロスサイト・スクリプティングの脆弱性。 このコードは、意図された機能を潜在的に変更し、トラステッド・セッション内で資格情報の漏えいにつながる可能性があります。


## 2016 年 11 月 8 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* お客様が WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM 用の[パブリック IP](/docs/services/ApplicationServeronCloud?topic=wasaas-networkEnvironment#networkEnvironment) アドレスを要求できる機能を追加しました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、以下を含む[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window}についての対処を行いました。
  * リモート・アタッカーが信頼できないソースからシリアライズド・オブジェクトを使用して任意の Java コードを実行できる恐れのある、IBM WebSphere Application Server の脆弱性。
  * TS_OBJ_print_bio 機能での領域外メモリー参照に起因する、サービス妨害の脆弱性。 特別に作成したタイム・スタンプ・ファイルを使用してリモート・アタッカーがこの脆弱性を悪用し、アプリケーションを異常終了させる恐れがあります。
  * SSL/TLS プロトコルの一部として使用される 64 ビットのブロック暗号の Triple-DES で発生するエラーに起因し、リモート・アタッカーが機密情報を取得できる危険性のある、OpenSSL の潜在的な脆弱性。 SSL/TLS サーバーとクライアント間の暗号化されたトラフィックを大量に取り込むことで、中間攻撃を行う能力を持つリモート・アタッカーがこの脆弱性を悪用し、非暗号化テキストのデータを復旧して機密情報を入手できる危険性があります。 この脆弱性は SWEET32 Birthday アタックとしても知られています。
  * OpenSSL には、サービス妨害に対する脆弱性があります。 再ネゴシエーションを繰り返し要求することで、認証されたリモート・アタッカーが過大な OCSP 状況確認要求を送信し、使用可能なメモリー・リソースをすべて消費してしまう危険性があります。
  * OpenSSL には、MDC2_Update 機能における整数オーバーフローに起因する、サービス妨害に対する脆弱性があります。 不明の攻撃ベクトルを使用することで、リモート・アタッカーがこの脆弱性を悪用して領域外メモリーへの書き出しをトリガーし、アプリケーションを異常終了させる恐れがあります。
  * 特定の操作に対する非定時間 codepath のフォローを許可する DSA 実装で発生するエラーに起因し、リモート・アタッカーが機密情報を取得できる危険性のある、OpenSSL の潜在的な脆弱性。 アタッカーがキャッシュ・タイミング攻撃を使用してこの脆弱性を悪用し、DSA 秘密鍵を復旧する恐れがあります。
  * OpenSSL には、証明書の構文解析時のメッセージ長チェックの欠落に起因する、サービス妨害に対する脆弱性があります。 認証済みのリモート・アタッカーがこの脆弱性を悪用して領域外メモリー参照をトリガーし、サービス妨害を引き起こす可能性があります。

## 2016 年 9 月 19 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server Liberty (Core プランおよび ND プラン) の新規インスタンスはフィックスパック 16.0.0.3 を使用するようになりました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、以下を含む[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window}についての対処を行いました。
  * リモート・アタッカーがフィッシング攻撃を実行できる恐れのある、IBM WebSphere Application Server Liberty の脆弱性。
  * OpenID Connect クライアントでのクロスサイト・スクリプティングに対する、IBM WebSphere Application Server Liberty の脆弱性。
  * デフォルトのエラー・ページが存在しない場合に例外が適切に取り扱われないことに起因し、リモート・アタッカーが機密情報を取得できる危険性のある、IBM WebSphere Application Server Liberty における潜在的な脆弱性。
  * Apache Commons FileUpload コンポーネントでのエラーに起因する、サービス妨害に対する Apache Tomcat の脆弱性。
  * 特定の条件で応答が不適切に取り扱われることに起因し、リモート・アタッカーが機密情報を取得できる危険性のある、IBM WebSphere Application Server および IBM WebSphere Application Server Liberty の脆弱性。
  * 機密性への影響はなく、保全性の影響は少なく、可用性のない、ネットワーキング・コンポーネントの詳細不明の脆弱性。

## 2016 年 8 月 17 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} が 8.5.5.9 から 8.5.5.10 にアップグレードされました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、以下を含む[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window}についての対処を行いました。
  * WebSphere Application Server および WebSphere Application Server Hypervisor Edition 管理コンソールに影響を与える Apache Struts の脆弱性。
  * ユーザーが SIP サービスを使用する IBM WebSphere Application Server の潜在的なサービス妨害の脆弱性。
  * WebSphere Application Server に使用される IBM HTTP Server に影響を与える可能性のあるいくつかの脆弱性。
  * IBM HTTP Server (IHS) に影響を与える可能性のある CGI アプリケーションを使用した HTTP トラフィックのリダイレクトを許可する脆弱性。 この脆弱性は「HTTPOXY」と呼ばれます。
  * IBM WebSphere Application Server 内の情報開示に対する脆弱性。
  * IBM WebSphere Application Server 内でセキュリティー制限を潜在的に迂回する脆弱性 (これは Web コンテナー・カスタム・プロパティー `HttpSessionIdReuse` を使用可能にする環境でのみ発生します)。


## 2016 年 6 月 24 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* 新規の _Traditional ND_ または _Traditional WebSphere_ インスタンスを作成するときに、お客様が V8.5 と V9.0 のどちらかを選択できる機能が追加されました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} がアップグレードされ、WebSphere Application Server Liberty (Core プランおよび ND プラン) の新規インスタンスはフィックスパック 16.0.0.2 を使用するようになりました。 16.0.0.2 は、8.5.5.9 の後の次のフィックスパックです。 16.0.0.2 以降は、これらのプランでサポートされる、使用許諾のある Liberty オプション・フィーチャーすべてがデフォルトでインストールされます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を与える、以下を含む[いくつかのセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window}についての対処を行いました。
  * IBM WebSphere Application Server に影響を与える、Apache Standard Taglibs の XML External Entity Injection (XXE) の脆弱性。
  * WebSphere Application Server Liberty プロファイル API Discovery フィーチャーおよび Swagger の資料のセキュリティーが、予想より脆弱である可能性。
  * IBM WebSphere Application Server Liberty の管理センター内の情報開示に関する潜在的な脆弱性。
  * IBM WebSphere Application Server で HTTP 応答が分割されるという潜在的な脆弱性。
  * 2016 年 5 月 3 日に OpenSSL プロジェクトによって明らかになった OpenSSL の脆弱性。

## 2016 年 6 月 13 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} RESTful API を使用したアプリケーションまたはスクリプトの作成によりお客様が仮想マシン・インスタンスの構築、プロビジョン、管理、および削除を行える機能が追加されました。
* IP アドレス 10 個およびメモリー 64 GB を超えない決まった数の停止インスタンスを持つことができる機能が追加されました。 停止状態の累積インスタンスについては、5 % 減額して課金されるようになりました。

## 2016 年 4 月 26 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* FIPS 140-2 が有効な場合の WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} における[潜在的なセキュリティー脆弱性](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window}と、Samba における複数の脆弱性 (Badlock を含む) について対処を行いました。
* 各種サービス・メンテナンスを統合しました。

## 2016 年 4 月 15 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新

* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} が 8.5.5.8 から 8.5.5.9 にアップグレードされました。
* OpenID Connect (OIDC) クライアントを使用する利用者に影響を及ぼす、{{site.data.keyword.Bluemix_notm}} の Liberty for Java における[クロスサイト・スクリプティング](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window}の脆弱性についての対処を行いました。
* 各種サービス・メンテナンスを統合しました。

## 2016 年 2 月 19 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新
* メモリーを大量に使用するアプリケーションを使用するクライアントのために、より大きな仮想マシンによって環境を「適正化」するオプションを追加しました。 クライアントは、所定の WebSphere Application Server コンポーネントまたは単一システムの特定のリソース・サイズを、最大 32 GB RAM 仮想マシンまで選択することができます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} が 8.5.5.7 から 8.5.5.8 にアップグレードされました。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に影響を及ぼし、一般に [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window} と呼ばれている、IBM SDK Java Technology Edition における複数の脆弱性について、対処を行いました。
* OAuth プロバイダー出力の利用者に影響を及ぼす[クロスサイト・スクリプティング](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window}の脆弱性について、対処を行いました。
* 各種サービス・メンテナンスを統合しました。

## 2015 年 12 月 11 日: WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の更新
* 正式な製品名が、IBM Application Server on Cloud in {{site.data.keyword.Bluemix_notm}} から IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} に変更されました
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment プランに新機能が追加されました。 このプランは、2 つ以上の仮想マシンを使用する WebSphere Application Server Network Deployment セル環境で構成されています。 これらの新機能により、ユーザーは高可用性、フェイルオーバー、およびスケーラビリティーに対してクラスター環境をセットアップすることができます。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Liberty Core プランに新機能が追加されました。 このプランには、Liberty プロファイル (サーバー) のグループの管理ドメインであり、2 つ以上の仮想マシンで構成される Liberty 集合の使用が含まれています
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} が 8.5.5.6 から 8.5.5.7 に更新されました
* Java オブジェクトのデシリアライゼーションの処理に関する [Apache Commons Collections の脆弱性](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window}についての対処を行いました。
* [HTTP レスポンス分割攻撃](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}を可能にする可能性のある脆弱性についての対処を行いました。
* 各種サービス・メンテナンスを統合しました。

## 2015 年 10 月 15 日: Application Server on Cloud の更新
* 次の 2 つの新しいプランが追加されました。
  * [WebSphere Application Server Traditional V9 ベータ](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* 各種サービス・メンテナンス
