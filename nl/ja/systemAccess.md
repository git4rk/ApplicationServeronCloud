---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# システム・アクセス
{: #system_access}

サービス・インスタンスの作成と管理の方法、およびシステムへのアクセスおよびシステムへのアクセスのセットアップ方法について説明します。
{: shortdesc}

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} における REST API の使用法
{: #restapi_usage}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} のインスタンスの作成、プロビジョン、管理、および削除は、以下のいずれかの方法で行われます。

* {{site.data.keyword.Bluemix_notm}} カタログおよびサービス・ダッシュボードから。
* RESTful API を使用したアプリケーションまたはスクリプトの作成から。

Swagger 2.0 準拠 REST API を使用して、クライアントはポータルおよびダッシュボードで提供されるものと同じ機能にアクセスできます。 サポートされる REST API とリソースについて詳しくは、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API の資料](https://wasaas-broker.ng.bluemix.net/wasaas-broker/api#/){: new_window}を参照してください。 REST API の使用法を示すサンプル・コードについては、{{site.data.keyword.Bluemix_notm}} [REST API のサンプル](https://github.com/IBM-Cloud/WebSphere-in-Bluemix/tree/master/WebSphere-In-Bluemix-API-Examples){: new_window}の Git でホストされた WebSphere Application Server をダウンロードしてください。

**注:** サービス・インスタンスを作成した後、作成された T シャツ・サイズによっては、サービスがすぐに使用可能状態にならないことがあります。 戻された JSON の **Status** フィールドを照会してサービス・インスタンスの現在の状態を判別することをお勧めします。

**注: [REST API のサンプル](https://github.com/IBM-Cloud/WebSphere-in-Bluemix/tree/master/WebSphere-In-Bluemix-API-Examples){: new_window}で参照されている ****apiEndpoint** URL は、ダラス地域を指しています。他の地域を使用する場合は、アプリケーションで適切な **apiEndpoint** を参照するようにしてください。

*表 1. REST API 実装の API エンドポイント URL*

| **地域名** | **地域接頭部** | **API エンドポイント URL** |       
|:-------------:|:--------------:|:-------------:|
| ダラス | `ng` | https://wasaas-broker.ng.bluemix.net/wasaas-broker/api  |
| ロンドン | `eu-gb` | https://wasaas-broker.eu-gb.bluemix.net/wasaas-broker/api  |
| フランクフルト | `eu-de` | https://wasaas-broker.eu-de.bluemix.net/wasaas-broker/api  |
| シドニー | `au-syd` | https://wasaas-broker.au-syd.bluemix.net/wasaas-broker/api  |

## サービス・ダッシュボード
{: #service_dashboard}

サービス・インスタンスの作成後は、サービス・ダッシュボードが表示されます。 組織ダッシュボードからは、サービス・アイコンをクリックすることで、
いつでもサービス・ダッシュボードに戻ることができます。
サービス・ダッシュボードからは、次のものにアクセスできます。

* この文書へのリンク
* 必要な OpenVPN 構成ファイルをダウンロードするためのリンク
* 仮想マシンを始動および停止する機能。 最初に VM が起動されます
* ホスト名
* 管理ユーザーと管理パスワード
* SSH 秘密鍵
* WebSphere&reg; 管理ユーザーおよび管理パスワード
* 管理センターと管理コンソール の URL


## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} インスタンス用の openVPN のセットアップ
{: #setup_openvpn}

いずれの WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 仮想マシンにアクセスするにも、OpenVPN が必要です。 管理者特権を使用して OpenVPN がインストールされ、実行されている必要があります。

### Windows での openVPN のセットアップ

1. openVPN Web サイトから、ご使用のシステム・アーキテクチャー用の openVPN Windows インストーラーをダウンロードします。
  * 64 ビット・システム: [openvpn-install-2.3.4-I001-x86_64.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-x86_64.exe){: new_window}
  * 32 ビット・システム: [openvpn-install-2.3.4-I001-i686.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-i686.exe){: new_window}
2. 必ず、[Windows 管理者として実行](https://technet.microsoft.com/en-us/magazine/ff431742.aspx){: new_window}し、OpenVPN をインストールしてください。
3. サービス・ダッシュボードで、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} インスタンスの OpenVPN ダウンロード・リンクから VPN 構成ファイルをダウンロードします。 圧縮ファイル内の 4 ファイルすべてを、`{OpenVPN
home}\config` ディレクトリーに解凍します。 例:

  ```  
  C:\Program Files\OpenVPN\Config
  ```

4. OpenVPN クライアント・プログラム「OpenVPN GUI」を開始します。 必ず、**「管理者として実行」**を選択して、プログラムを開始してください。 そうでないと、接続できない場合があります。

### Linux での openVPN のセットアップ

1. openVPN をインストールするには、[Linux用の openVPN の指示](https://openvpn.net/index.php/access-server/docs/admin-guides/182-how-to-connect-to-access-server-with-linux-clients.html){: new_window}に従います。

   RPM Package Manager を手動でダウンロードしてインストールする必要がある場合には、
[OpenVPN の UNIX/LINUX 用のダウンロード](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html){: new_window}
に移動してください。 Linux 管理者からの支援が必要な場合があります。
3. サービス・ダッシュボードで、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} インスタンスの OpenVPN ダウンロード・リンクから VPN 構成ファイルをダウンロードします。 openVPN クライアントの開始に使用する予定のディレクトリーに、ファイルを解凍します。 4 ファイルがすべて同じディレクトリーにある必要があります。
3. OpenVPN クライアント・プログラムを開始します。 端末ウィンドウを開いて、構成ファイルを含むディレクトリーに移動します。 root として次のコマンドを実行します。

  ```
  openvpn --config vt-wasaas-wasaas.ovpn
  ```
  {: .codeblock}  

### Mac での openVPN のセットアップ
1. 1 つの方法として、オープン・ソース・ソフトウェア製品の [Tunnelblick](https://tunnelblick.net/){: new_window} をインストールする方法があります。
2. WebSphere サービスから VPN 構成ファイルを抽出します。 Tunnelblick によって、Mac の管理パスワードが求められ、接続に使用できる VPN セットにこの構成が追加されます。
3. VPN ネットワークに接続します。その後、仮想マシンにアクセスできます。 最初にユーザーがアクセスした後、Tunnelblick は構成をキャッシュに入れます。ユーザーは Tunnelblick から接続できます。 メニュー・バーにアイコンを配置して、簡単にアクセスすることができます。


## SSH を使用した WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM へのアクセス
{: #using_ssh}

この手順では、クライアントとして OpenSSH を使用していることを想定しています。 OpenSSH は通常、Linux 上で使用でき、Windows 上で実行される Cygwin でも使用できます。 Windows コマンド・プロンプトから実行するようにインストールすることもできます。

OpenSSH のインストールを確認するには、次のコマンドを実行します。
  ```
  ssh -V
  ```
  {: codeblock}

以下のメッセージは応答例です。
  ```
  OpenSSH_6.6p1, OpenSSL 1.0.1g 7 Apr 2014
  ```

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM への SSH アクセスをセットアップするには、以下の手順を使用します。

1. 初めて接続したときに表示される「The authenticity of host x.x.x.x cannot be established.」という警告メッセージを検討します。 このメッセージは正常です。 プロンプトが表示されたら、yes を選択します。 この時点で、VM 上でユーザー**「virtuser」**に公開鍵がインストールされます。
2. 秘密鍵を使用して、**virtuser** にログインします。 秘密鍵認証方式を使用するのが最適です。
3. 秘密鍵の内容をファイルにコピーします。
4. 次のコマンドを実行して、SSH を使用して接続します。

  ```
  ssh virtuser@169.53.246.xxx -i /path/privateKeyFileName
  ```
  {: codeblock}

5. 次のコマンドを実行して **virtuser** から **root** に切り替えることにより、完全な sysadmin 権限を取得します。

  ```
  sudo su root
  ```
  {: codeblock}

6. 秘密 SSH 鍵でシステムにアクセスして問題が発生する場合は、提供された root パスワードを使用します。 次のコマンドを実行して root としてログインし、パスワードを入力します。

  ```
  ssh root@169.53.246.x
  ```
  {: codeblock}

7. システムへのアクセスで秘密 SSH 鍵を使用した場合も、root パスワードを使用した場合も、すぐに root パスワードを変更してください。
8. SSH コマンドを単純化するために、`config` という名前のファイルを `%HOME%/.ssh` ディレクトリーに作成します。 例:

   ```
   Host VM1
      Hostname 169.53.246.xxx
      User virtuser
      IdentityFile /path/privateKeyFileName
   ```
   {: codeblock}

9. 次のコマンドを実行して、**virtuser** として接続します。

   ```
   ssh VM1
   ```
   {: codeblock}

## システム・パス
{: #system_paths}

* Liberty コマンドは、`/opt/IBM/WebSphere/Liberty/bin` から実行可能です。
* Liberty サーバー・プロファイルがある場所は、`/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` です。
* すべてのプロファイルで共有される WebSphere Application Server traditional のコア・プロダクト・ファイルは `/opt/IBM/WebSphere/AppServer/` にあります。
* WebSphere Application Server traditional のコマンドは、`/opt/IBM/WebSphere/Profiles/Default<profile_type><profile_number>/bin` 内のデフォルト・プロファイル・ロケーションから実行できます。
  * `<profile_type>` の値は、`AppSrv`、`Dmgr`、`Custom`、`AdminAgent`、`JobMgr`、または `SecureProxySrv` です。
  * `<profile_number>` は、固有のプロファイル名を作成するために使用される連続番号です。


## コマンド・ラインからのサーバーの管理
{: #start_servers}

**問題の回避:** コマンド・ラインから WebSphere サーバーを管理する場合、**virtuser** ではなく **wsadmin** (WebSphere 管理 ID) を使用する必要があります。 コマンド・ラインから IHS サーバーを管理する場合、**root** を使用する必要があります。

## 管理センターと管理コンソールのリンクの使用
{: #console_links}

管理センターまたは管理コンソールへのリンクをクリックしたときに、*「信頼できない接続」*の警告を受け取ることがあります。 ブラウザーによって、示されるメッセージ・テキストも、警告を回避または除去するための手順も異なります。

{{site.data.keyword.IBM}} 提供のリンクを使用しているため、この警告は無視して接続して問題ありません。 ブラウザーによってセキュリティー例外の保管が提案された場合は、そうすることで、最も簡単にこの警告を以降受け取らないようにすることができます。

もう 1 つのオプションとして、着信した署名者証明書をエクスポートして、トラステッド・ルート証明書としてブラウザーにインポートすることができます。 このオプションでは、*hosts* ファイルに、VM の IP アドレスを証明書発行者の共通名にマップするエントリーを作成する必要があります。 この名前の形式は、`wl<pureapplication.ibmcloud.com` です。 現在、URL で IP アドレスの代わりにホスト名を使用している場合は、スムーズに接続できます。 その後は、URL で IP アドレスではなく、そのホスト名を使用して管理センターまたは管理コンソールにアクセスする必要があります。

最後に、お客様が、外部化したアプリケーションの独自のルート証明書をインストールする場合がよくあります。 詳しくは、IBM Knowledge Center で [WebSphere Application Server](https://www.ibm.com/support/knowledgecenter/SSAW57_9.0.0/com.ibm.websphere.nd.multiplatform.doc/ae/tsec_securecomm.html){: new_window} または [Liberty Core](https://www.ibm.com/support/knowledgecenter/SSD28V_9.0.0/com.ibm.websphere.wlp.core.doc/ae/twlp_sec_comm.html){: new_window} の資料を参照してください。

## ファイアウォール・ポート
{: #firewall_ports}

アプリケーションおよびデータベースへのアクセスを許可するために、ファイアウォール上でポートをオープンすることが必要になる可能性があります。 `openFirewallPorts.sh` スクリプトを使用してファイアウォール・ポートを開くことができます。このスクリプトは、以下の場所にあります。
  * WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} の各ノードには、`WAS_HOME/virtual/bin` ディレクトリーに `openFirewallPorts.sh` スクリプトがあります。
  * 各 Liberty 集合ホスト上には、`WAS_HOME/virtual/bin` ディレクトリーに `openFirewallPorts.sh` があります。

### 使用法

次のコマンド構文を使用して、`openFirewallPorts.sh` スクリプトを実行します。

  ```
  openFirewallPorts.sh -ports <PORT>:<PROTOCOL>,... -persist true|false
  ```
  {: codeblock}

説明:
* PORT はポート番号です。
* PROTOCOL は、TCP または UDP のいずれかです。
* `-persist` は `true` または `false` のいずれかです。

複数のポートをコンマ区切りリストで指定できます。

**注**: オープンしているポートの sport と dport は、ファイアウォールの INPUT セクションと OUTPUT セクションでオープンされます。 このスクリプトは、`sudo` を使用して root として実行する必要があります。 iptables を直接変更することもできます。

## Web サーバーの構成
{: #configure_webserver}

セルまたは集合をプロビジョンする際、事前構成された環境を受け取ります。 特に従来の Network Deployment セルの場合は、以下の環境を受け取ります。

* 開発およびテストの目的で IBM HTTP Server と連結された Deployment Manager。
* Deployment Manager に統合されたカスタム・ノード。
* すべて初期に「開始済み」状態にプロビジョンされている、Deployment Manager、IHS Server、およびノード・エージェント。

Web サーバーですべてのユーザー要求を処理する必要がある場合は、アプリケーションのデプロイ後にプラグインを生成して伝搬する必要があるかもしれません。

**問題の回避:** プラグインの生成と伝搬を行う前に、以下の前提条件タスクが完了していることを確認してください。

* ローカルの Windows、Linux、または MAC 環境で、[openVPN](systemAccess.html#setup_openvpn) が構成済みで開始済みであり、適切な領域への接続が確立されていることを確認します。
* WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} のサービス・ダッシュボードから**管理コンソールを開き**、サービス・ダッシュボードで提供される wsadmin および管理パスワードでログインします。
* Deployment Manager は空のカスタム・ノードと統合されるため、管理コンソールからアプリケーション・サーバー (例えば ***server1*** など) を作成します。
* 作成したサーバーを始動します。
* アプリケーションのインストール時に、アプリケーションのモジュールが、始動したサーバーおよび Web サーバー (例えば***webserver1***) にマップされていることを確認します。

以下の概略的な手順は、前提条件タスクが完了していることを想定しています。

1. 管理コンソールで、環境オプションからプラグインを生成します。
   1. **「環境」>「グローバル Web サーバー・プラグイン構成の更新」**を選択します。
   2. **「OK」**または**「上書きして新規プラグイン構成ファイルを生成 (Overwrite to generate a new plug-in configuration file)」**のいずれかをクリックします。
2. Deployment Manager から、プラグインを Web サーバー構成にコピーします。

  ```
   cp /opt/IBM/WebSphere/Profiles/DefaultDmgr01/config/cells/plugin-cfg.xml /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
  ```
  {: codeblock}
3. `IHS_HOME/conf` 内の `httpd.conf` ファイル (例えば、`/opt/IBM/WebSphere/HTTPServer/conf`) を開き、以下の 2 行が存在することを確認します。

    ```
    LoadModule was_ap22_module /opt/IBM/WebSphere/Plugins/bin/64bits/mod_was_ap22_http.so
    WebSpherePluginConfig /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
    ```
    {: codeblock}  
4. 以下のコマンドを実行して、ポートを開きます。

   ```
   export serverPorts=2810:TCP,2810:UDP,8880:TCP,8880:UDP,9101:TCP,9101:UDP,9061:TCP,9061:UDP,9080:TCP,9080:UDP,9354:TCP,9354:UDP,9044:TCP,9044:UDP,9443:TCP,9443:UDP,5060:TCP,5060:UDP,5061:TCP,5061:UDP,11005:TCP,11005:UDP,11007:TCP,11007:UDP,9633:TCP,9633:UDP,7276:TCP,7276:UDP,7286:TCP,7286:UDP,5558:TCP,5558:UDP,5578:TCP,5578:UDP

   sudo /opt/IBM/WebSphere/AppServer/virtual/bin/openFirewallPorts.sh -ports $serverPorts -persist true
   ```
   {: codeblock}
5. 以下のコマンドを実行して、Web サーバーを停止し、始動します。
    ```
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k stop
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k start
    ```
    {: codeblock}
8. 　プラグインを使用してアプリケーションにアクセスします。
  ```
   http://169.53.246.xxx/contextRoot/
  ```
  {: codeblock}

**注:** Web サーバーを構成しようとしている場合、ここで提供されているステップは、数多くのパスのうちの 1 つを表しています。 さらに支援が必要な場合は、[IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/search/configure%20web%20server?scope=SSAW57_9.0.0){: new_window} を参照してください。

アプリケーションにアクセスできない場合は、ファイアウォールでポート・アクセスの問題が発生していることが考えられます。 このため、アプリケーション・サーバー、ノード・エージェント、Web サーバー、デプロイメント・マネージャーのうちいずれかのサーバーを再始動する必要がある可能性があります。 また、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} のサービス・ダッシュボードにアクセスしてそれぞれの仮想マシンを再始動する必要がある場合もあります。
{: tip}

## SSL 構成
{: #ssl_configuration}

WebSphere Application Server traditional および Liberty には、[SSL_TLSv2](https://www.ibm.com/support/knowledgecenter/en/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/protocols.html){: new_window}プロトコルが構成されています。 SSL 構成を変更することで、プロトコルを変更できます。

### WebSphere Application Server traditional
{: #ssl-was}

1. `/opt/IBM/WebSphere/Profiles/<profile_name>/config/cell/<cell_name>` ディレクトリー内の `security.xml` ファイルを開き、次の行を変更します。

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}

2. `/opt/IBM/WebSphere/Profiles/<profile_name>/properties` ディレクトリー内の `ssl.client.props` ファイルを開き、次の行を変更します。

   ```
   com.ibm.ssl.protocol=SSL_TLSv2
   ```
   {: codeblock}

### Liberty
{: #ssl-liberty}

1. `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` ディレクトリー内の `server.xml` ファイルを開き、`defaultSSLConfig` SSL 構成エレメント内の以下の行を変更します。

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}
