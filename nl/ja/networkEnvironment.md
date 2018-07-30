---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-06"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# ネットワーク環境
{: #networkEnvironment}

{{site.data.keyword.appserver_full}} のサービス・インスタンスがプロビジョンされた後、いくつかの方法で VM にアクセスできます。 セキュアな VPN で接続し、SSH、従来の WebSphere 管理コンソール、およびアプリケーションから VM にアクセスすることができます。 また、パブリック IP アドレスを使用して VM をインターネットに接続することも可能です。

以下の図は、これらのネットワーク・パスを示しています。

図 1. パブリック IP を使用したマルチテナント・ネットワーキングのクライアント・ビュー

![図 1. パブリック IP を使用したマルチテナント・ネットワーキングのクライアント・ビュー](images/wasaas_multi_tenantPublicIP.gif)

## VPN アクセス
{: #vpnAccess}

{{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードから WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} のサービス・インスタンスをプロビジョンした後、ドロップダウン・メニューを展開し、**「VPN 構成のダウンロード」**ボタンを使用して VPN 構成をダウンロードすることで OpenVPN 接続を確立できます。VPN 構成には、OpenVPN サーバーでの認証に使用される **.ovpn** ファイルと証明書が含まれます。OpenVPN 接続が確立された後、SSH を通じて VM にアクセスできます。また、Liberty 管理センター、従来の WebSphere 管理コンソール、およびアプリケーションへのアクセスも可能です。

VPN 構成の適用範囲は組織と地域です。作成された時点から 1 年間有効です。同じ VPN 構成を使用して、同時に複数の OpenVPN クライアント接続を確立できます。

**注:** VPN 構成は、組織に**アクティブ**なサブスクリプションが含まれる場合にのみ有効です。組織の最後のサブスクリプションが削除されると、組織のすべての VPN 構成が中断されます。期限内の VPN 構成は、新規サブスクリプションがアクティブになると自動的に再アクティブ化されます。

## 拡張 VPN 構成管理
{: #advancedVPN}

ほとんどの場合、**「VPN 構成のダウンロード」**ボタンを使用してダウンロードできる 1 つの VPN 構成のみ必要です。ただし、{{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードから**「拡張 VPN 管理」**ボタンを使用してアクセスできる「拡張 VPN 管理」ページを使用すると、複数の VPN 構成を作成し、管理できます。複数の VPN 構成があると、古い VPN 構成が期限切れ間近のときに、新しい VPN 構成にスムーズに移行でき便利です。また、組織の各個人やチームによる VM へのアクセスを管理するために、複数の VPN 構成を要求することもできます。  

**注:** 組織で、**最大** 10 個のアクティブ VPN 構成をいつでも使用できます。

VPN 構成が漏えいした場合、または期限切れになった場合、「拡張 VPN 管理」ページを使用して VPN 構成を取り消すことができます。さらに、監査の観点から、すべての VPN 管理アクティビティーの履歴を表示し、「拡張 VPN 管理」ページで以前に作成されたアクティブな VPN 構成をダウンロードできます。

{{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードから使用できるすべての機能は、REST API を使用してスクリプト化することもできます。詳しくは、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API の資料](https://wasaas-broker.ng.bluemix.net/wasaas-broker/api#/){: new_window}を参照してください。


## パブリック・インターネット・アクセス
{: #publicInternetAccess}

オプションで、{{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードからパブリック・インターネット・アクセスを管理できます。プールのパブリック IP アドレスを**要求**し、インターネットから WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} サービス・インスタンスへの接続を**オープン**することができます。反対に、サービス・インスタンスからインターネットへのアクセスを**クローズ**し、パブリック IP アドレスをプールに**返却**することもできます。

パブリック IP アドレスを**要求**し、接続を**オープン**するには、次の手順に従います。

1. {{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードで**「パブリック IP へのアクセスを管理」**をクリックします。
2. パブリック IP アドレスではない、ホストの IP アドレスが表示されます。**「パブリック IP アドレスを要求」**をクリックします。

    **注:** パブリック IP が割り当てられたサービス・ダッシュボードに戻ります。ただし、次のメッセージが表示されます。

    > **アクセスは現在クローズ状態です。アクセスをオープンするには「パブリック IP へのアクセスを管理」をクリックしてください。**
3. {{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードで**「パブリック IP へのアクセスを管理」**をクリックします。
4. ホストの IP アドレスと新しいパブリック IP が表示されますが、アクセスはクローズ状態です。**「アクセスのオープン」**をクリックします。

    **注:** サービス・ダッシュボードに戻ります。次のメッセージが表示されます。

    > **アクセスは現在オープン状態です。アクセスをクローズするには「パブリック IP へのアクセスを管理」をクリックしてください。**

接続を**クローズ**し、パブリック IP アドレスを**返却**するには、次の手順に従います。

1. {{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードで**「パブリック IP へのアクセスを管理」**をクリックします。
2. **「アクセスのクローズ」**をクリックします。

    **注:** サービス・ダッシュボードに戻ります。次のメッセージが表示されます。

    > **アクセスは現在クローズ状態です。アクセスをオープンするには「パブリック IP へのアクセスを管理」をクリックしてください。**
3. {{site.data.keyword.Bluemix_notm}} UI のサービス・ダッシュボードで**「パブリック IP へのアクセスを管理」**をクリックします。
4. **「パブリック IP アドレスを返却」**をクリックします。

    **注:** サービス・ダッシュボードに戻ります。ホストの IP アドレスと次のメッセージが表示されます。

    > **パブリック IP を返却しました。**

## パブリック IP ポート
{: #publicIPports}

パブリック IP へのアクセスを開くと、その IP アドレスはご使用の VM と関連付けられ、ゲートウェイでポート 80 とポート 443 が開きます。 ただし、デフォルトで、Liberty Core および従来の WebSphere Base サーバーは、ポート 80 とポート 443 を開きません。 IBM HTTP Server では、デフォルトでポート 80 とポート 443 は開きます。 このため、パブリック IP の使用時にポート 80/443 でアプリケーション・トラフィックを listen するよう Liberty Core および従来の WebSphere Base サーバーを構成する必要が生じる可能性があります。
* Liberty Core サーバーを構成するには、[パブリック・アクセス用に Liberty Core サーバーを構成する (Configure Liberty Core Server for public access)](networkEnvironment.html#configureLibertyForPublicAccess)を参照してください。
* 従来の WebSphere Base サーバーを構成するには、ポート 80/443 で listen する Web コンテナー・トランスポート・チェーンを追加します。この説明については、[Configuring transport chains](http://www.ibm.com/support/knowledgecenter/SSEQTP_8.5.5//com.ibm.websphere.nd.doc/ae/trun_chain_transport.html){: new_window} を参照してください。

**問題の回避:** Linux では、**root** などの特権ユーザーのために 1024 未満のポートが予約されています。ただし、従来型 WebSphere Base サーバーは**非 root** ユーザーとして実行するのが一般的です。このため、Web コンテナー・トランスポート・チェーンを追加するとき、**iptables**の構成を **root** ユーザーとして変更します。特に、制限付きポートである 80 と 443 を、1024 より上の別ポート (9080 や 9443 など) に指定変更します。次のコマンドは、このプロセスの例です。

```
-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 9080
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9080 -j ACCEPT

-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 9443
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
```

**注:** **iptables** の変更は一時的なものです。例えば、ゲストがリブートすると、または **iptables** サービスが再始動すると、ルールが自動的にフラッシュされ、リセットされます。iptables サービスが再始動しても、またはゲストがリブートしてもルールが永続するようにそれらのルールを保存するには、**root** ユーザーとして次のコマンドを使用します。

```
-bash-4.1# service iptables save
iptables: Saving firewall rules to /etc/sysconfig/iptables:[  OK  ]

bash-4.1# cat /etc/sysconfig/iptables
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*nat
:PREROUTING ACCEPT [0:0]
:POSTROUTING ACCEPT [23:1706]
:OUTPUT ACCEPT [23:1706]
-A PREROUTING -p tcp -m tcp --dport 80 -j REDIRECT --to-ports 9080
-A PREROUTING -p tcp -m tcp --dport 443 -j REDIRECT --to-ports 9443
COMMIT
# Completed on Wed May 31 19:44:11 2017
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*filter
:INPUT DROP [0:0]
:FORWARD DROP [0:0]
:OUTPUT DROP [0:0]
-A INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 9080 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 80 -j ACCEPT

```


**注:** ゲストの外部インターフェースを経由する要求に対して **iptables** が呼び出されます。ローカル・ループバック (127.0.0.1) を経由する要求は **iptables** で処理されないため、前述したポートの指定変更はループバックでは呼び出されません。

## VPN のプライベート IP ポート
{: #privateIPports}

VM のプライベート IP アドレスには、VPN 接続を使用して接続します。 図 1 に示すとおり、Liberty 管理センター (9080, 9443)、従来の WebSphere 管理コンソール (9060, 9043)、SSH (22)、および 80/443 以外のポートには、VPN 接続でのみアクセス可能です。Liberty 管理センターとアプリケーション・ポートの分離について詳しくは、サンプルの Liberty Core **server.xml** および **ibm-web-bnd.xml** を参照してください。

**問題の回避:** Liberty Core および従来の WebSphere Base サーバーの場合、VM がプロビジョンされる際にファイアウォール・ポートは事前構成されています。 ただし、Deployment Manager または集合コントローラーが IBM HTTP Server と連結されている Network Deployment の構成においては、ファイアウォールでポートを開く必要がある可能性があります。 詳細については、[ファイアウォール・ポート](systemAccess.html#firewall_ports)を参照してください。

## Liberty Core サーバーをパブリック IP アクセス用に構成する
{: #configureLibertyForPublicAccess}

パブリック IP の使用時にポート 80/443 でアプリケーション・トラフィックを listen するよう Liberty Core を構成する必要があります。

デフォルトで、Liberty は、Liberty 管理センター、およびポート 9080 および 9443 の **defaultHttpEndpoint** と関連付けられている **default_host** 仮想ホストで使用可能なアプリケーションで構成されます。 Liberty 管理センターをアプリケーションの仮想ホストおよびエンドポイントと分離するようにご使用のサーバーを再構成し、それらを別のポートで使用可能にしてください。

以下のスニペットは、server.xml 構成の調整の例です。

```    
    <!-- open port 9080/9443 for incoming http connections -->
    <httpEndpoint id="defaultHttpEndpoint"
        host="*"
        httpPort="9080"
        httpsPort="9443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!-- define a new endpoint for public app traffic -->
    <httpEndpoint id="publicHttpEndpoint"
        host="*"
        httpPort="80"
        httpsPort="443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!–- restrict default_host to vpn so the Liberty Admin Center is not public -->
    <virtualHost id="default_host" allowFromEndpointRef="defaultHttpEndpoint">
      <hostAlias>*:9080</hostAlias>
      <hostAlias>*:9443</hostAlias>
    </virtualHost>

    <virtualHost id="external_host">
      <hostAlias>*:80</hostAlias>
      <hostAlias>*:443</hostAlias>
    </virtualHost>
```
{: codeblock}

次に、以下のスニペットをアプリケーションの **WEB-INF/ibm-web-bnd.xml** ファイルに含めることで、アプリケーションを **external_host** 仮想ホストと関連付けます。

```
    <?xml version="1.0" encoding="UTF-8"?>
    <web-bnd
        xmlns="http://websphere.ibm.com/xml/ns/javaee"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://websphere.ibm.com/xml/ns/javaee   
        http://websphere.ibm.com/xml/ns/javaee/ibm-web-bnd_1_0.xsd"
        version="1.0">

        <virtual-host name="external_host" />
    </web-bnd>
```
{: codeblock}

## DNS の構成
{: #dnsConfig}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM には 2 つの DNS リゾルバーが構成されていますが、この点に注目することが重要です。これらのリゾルバーは、VM の **/etc/resolv.conf** ファイルで構成されています。プライマリー DNS サーバーは、WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} サービスで提供される権限のないサーバーです。セカンダリー DNS サーバーは、{{site.data.keyword.Bluemix_notm}} で提供される権限のないサーバーです。

DNS 構成がニーズに合っているかどうか確認することをお勧めします。IBM 提供の DNS サーバーが要件を満たしていない場合、**/etc/resolv.conf** ファイルを更新して任意の DNS サーバーを参照できます。

**注:** 古い WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM では、プライマリー DNS サーバーのみ **/etc/resolv.conf** ファイルで構成されている場合があります。HA ソリューションが必要な場合、VM をリリースし、新しい VM をプロビジョンするか、**/etc/resolv.conf** ファイルを更新してセカンダリー DNS サーバーを追加します。この DNS サーバーを優先 DNS サーバーにすることも、{{site.data.keyword.Bluemix_notm}} で提供されている DNS サーバー (10.0.80.11) を優先 DNS サーバーにすることもできます。


## カスタム・ノード上の新規サーバー用のポートをオープンする
{: #serversOnCustom}

カスタム・ノードでサーバーを作成した場合、そのサーバーを始動する前に、そのサーバーが必要とする追加ポートを、デプロイメント・マネージャーおよびカスタム・ノード VM でオープンする必要があります。サーバーを作成した後、サーバーを始動する前に `openWASPorts.sh` スクリプトを実行してポートをオープンします。

 1. 各デプロイメント・マネージャーおよびカスタム VM に root ユーザーとしてログインします。
 1. `/opt/IBM/WebSphere/AppServer/virtual/bin/openWASPorts.sh` スクリプトを実行してポートをオープンします。
 
スクリプトを実行した後、デプロイメント・マネージャーの管理コンソールからサーバーを始動できます。
