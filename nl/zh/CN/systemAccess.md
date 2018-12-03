---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 系统访问
{: #system_access}

了解创建和管理服务实例的方法，并探索访问系统和设置系统访问权的方法。
{: shortdesc}

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的 REST API 用法
{: #restapi_usage}

您可以使用以下其中一种方法创建、供应、管理和删除 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的实例：

* 通过 {{site.data.keyword.Bluemix_notm}}“目录”和服务仪表板。
* 通过创建使用 RESTful API 的应用程序或脚本。

通过使用符合 Swagger 2.0 的 REST API，客户可使用与门户网站和仪表板所提供的功能相同的功能。有关支持的 REST API 和资源的更多信息，请参阅 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API 文档](https://wasaas-broker.ng.bluemix.net/wasaas-broker/api#/){: new_window}。有关演示 REST API 用法的样本代码，请下载 Git 托管的 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API 样本](https://github.com/IBM-Cloud/WebSphere-in-Bluemix/tree/master/WebSphere-In-Bluemix-API-Examples){: new_window}。

**注：**创建服务实例之后，根据创建的 T 恤尺寸，您的服务可能无法立即使用。建议您查询 JSON 返回的**状态**字段，以确定服务实例的当前状态。

**注：**[REST API 样本](https://github.com/IBM-Cloud/WebSphere-in-Bluemix/tree/master/WebSphere-In-Bluemix-API-Examples){: new_window}中引用的 **apiEndpoint** URL 指向达拉斯区域。如果您使用的是其他区域，请确保您的应用程序引用相应的 **apiEndpoint**。

*表 1. REST API 实现的 API 端点 URL*

|**区域名称**|**区域前缀**|**API 端点 URL**|       
|:-------------:|:--------------:|:-------------:|
|达拉斯|`ng`|https://wasaas-broker.ng.bluemix.net/wasaas-broker/api|
|伦敦|`eu-gb`|https://wasaas-broker.eu-gb.bluemix.net/wasaas-broker/api|
|法兰克福|`eu-de`|https://wasaas-broker.eu-de.bluemix.net/wasaas-broker/api|
|悉尼|`au-syd`|https://wasaas-broker.au-syd.bluemix.net/wasaas-broker/api|

## 服务仪表板
{: #service_dashboard}

创建服务实例后，您会进入服务仪表板。您可以始终通过单击组织仪表板中的服务图标，返回到服务仪表板。从服务仪表板，您可以访问：

* 此文档的链接
* 用于下载所需 OpenVPN 配置文件的链接
* 启动和停止虚拟机的能力。VM 初始启动
* 主机名
* 管理用户和管理密码
* 专用 SSH 密钥
* WebSphere&reg; 管理用户和管理密码
* 管理中心和管理控制台 URL


## 为 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 实例设置 openVPN
{: #setup_openvpn}

需要 OpenVPN 才能访问任何 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 虚拟机。必须使用管理员权限进行安装和运行。

### 在 Windows 上设置 openVPN

1. 从 openVPN Web 站点下载适用于您的系统体系结构的 openVPN Windows 安装程序：
  * 64 位系统：[openvpn-install-2.3.4-I001-x86_64.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-x86_64.exe){: new_window}
  * 32 位系统：[openvpn-install-2.3.4-I001-i686.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-i686.exe){: new_window}
2. 确保[以 Windows 管理员身份运行](https://technet.microsoft.com/en-us/magazine/ff431742.aspx){: new_window}且已安装 openVPN。
3. 在服务仪表板中，通过 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 实例的 OpenVPN 下载链接来下载 VPN 配置文件。将压缩文件中的全部 4 个文件解压缩到 `{OpenVPN home}\config` 目录。例如：

  ```  
  C:\Program Files\OpenVPN\Config
  ```

4. 启动 openVPN 客户端程序“OpenVPN GUI”。确保选择**以 Windows 管理员身份运行**来启动程序。如果不以管理员身份运行，您可能无法连接。

### 在 Linux 上设置 openVPN

1. 要安装 openVPN，请遵循 [openVPN for Linux 指示信息](https://openvpn.net/index.php/access-server/docs/admin-guides/182-how-to-connect-to-access-server-with-linux-clients.html){: new_window}。

   如果需要手动下载并安装 RPM 软件包管理器，请转至 [openVPN unix/linux 下载](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html){: new_window}。您可能需要 Linux 管理员的帮助。
3. 在服务仪表板中，通过 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 实例的 OpenVPN 下载链接来下载 VPN 配置文件。将文件解压缩到要从中启动 openVPN 客户端的目录。需要全部 4 个文件位于相同目录。
3. 启动 openVPN 客户端程序。打开终端窗口，并转至包含配置文件的目录。以 root 用户身份运行以下命令：

  ```
  openvpn --config vt-wasaas-wasaas.ovpn
  ```
  {: .codeblock}  

### 在 Mac 上设置 openVPN
1. 一种方法是安装 [Tunnelblick](https://tunnelblick.net/){: new_window}（开放式源代码软件产品）。
2. 从 WebSphere 服务抽取 VPN 配置文件。Tunnelblick 提示您输入 Mac 的管理密码，并将配置添加到可以用来连接的 VPN 集。
3. 连接到 VPN 网络，然后可以访问虚拟机。第一次访问后，Tunnelblick 会高速缓存配置，并且可以从 Tunnelblick 进行连接。您可以将图标放在菜单栏上以方便访问。


## 使用 SSH 访问 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM
{: #using_ssh}

这些指示信息假定您使用的是 OpenSSH 作为客户端。OpenSSH 通常适用于 Linux，也适用于在 Windows 上运行的 Cygwin。您还可以安装 OpenSSH，以从 Windows 命令提示符运行。

要验证 OpenSSH 的安装，请运行以下命令。
  ```
  ssh -V
  ```
  {: codeblock}

以下消息是响应示例：
  ```
OpenSSH_6.6p1, OpenSSL 1.0.1g 7 Apr 2014
  ```

使用以下指示信息，设置 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM 的 SSH 访问权。

1. 查看在您第一次连接时出现的警告消息“无法确定主机 x.x.x.x 的真实性”。此消息是正常的。在出现提示时，选择 yes。现在，公用密钥已为用户 **virtuser** 安装在 VM 上。
2. 使用专用密钥登录到 **virtuser**。为了获取最佳结果，请使用专用密钥认证方法。
3. 将专用密钥的内容复制到文件。
4. 运行以下命令，以使用 SSH 进行连接。

  ```
  ssh virtuser@169.53.246.xxx -i /path/privateKeyFileName
  ```
  {: codeblock}

5. 运行以下命令，将 **virtuser** 切换为 **root** 用户，从而获取完整的 sysadmin 权限。

  ```
  sudo su root
  ```
  {: codeblock}

6. 如果您在使用专用 SSH 密钥访问系统时遇到问题，请使用提供的 root 密码。运行以下命令，以 root 用户身份登录，并提供密码。

  ```
  ssh root@169.53.246.x
  ```
  {: codeblock}

7. 无论是使用专用 SSH 密钥还是 root 密码访问系统，请立即更改 root 密码。
8. 要简化 SSH 命令，请在 `%HOME%/.ssh` 目录中创建一个名为 `config` 的文件。例如：

   ```
   Host VM1
      Hostname 169.53.246.xxx
      User virtuser
      IdentityFile /path/privateKeyFileName
   ```
   {: codeblock}

9. 运行以下命令，以 **virtuser** 身份进行连接。

   ```
   ssh VM1
   ```
   {: codeblock}

## 系统路径
{: #system_paths}

* 可以从 `/opt/IBM/WebSphere/Liberty/bin` 发出 Liberty 命令。
* Liberty 服务器概要文件位置为 `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1`。
* 由所有概要文件共享的传统 WebSphere Application Server 核心产品文件位于 `/opt/IBM/WebSphere/AppServer/` 中。
* 传统 WebSphere Application Server 命令可以从 `/opt/IBM/WebSphere/Profiles/Default<profile_type><profile_number>/bin` 中的缺省概要文件位置发出，其中：
  * `<profile_type> 的值为 `AppSrv`、`Dmgr`、`Custom`、`AdminAgent`、`JobMgr` 或 `SecureProxySrv`。
  * `<profile_number>` 是用于创建唯一概要文件名称的序号。


## 通过命令行管理服务器
{: #start_servers}

**应注意的问题：**通过命令行管理 WebSphere 服务器时，请确保使用 **wsadmin**（WebSphere 管理标识），而不要使用 **virtuser**。通过命令行管理 IHS 服务器时，请确保使用 **root** 用户。

## 使用管理中心和管理控制台链接
{: #console_links}

当您单击管理中心或管理控制台的链接时，可能会收到*不可信的连接*警告。确切的消息文本会因浏览器不同而有所不同，按照以下确切的步骤忽略或消除该警告。

因为您使用的是 {{site.data.keyword.IBM}} 提供的链接，所以可以放心忽略该警告并进行连接。如果您的浏览器提供存储安全性异常的操作，那么执行该操作是防止未来出现该警告的最简便方法。

另一种选择是导出入局签署者证书，然后将其导入浏览器中作为可信根证书。此种选择可能需要您在 *hosts* 文件中添加条目，以便将 VM 的 IP 地址映射到证书发行方的通用名称。此名称的格式如下：`wl<pureapplication.ibmcloud.com`。如果您现在在 URL 中使用主机名而非 IP 地址，那么应该正常连接。然后必须在 URL 中使用该主机名而非 IP 地址来访问管理中心或管理控制台。

最后，客户通常会为外部应用程序安装他们自己的根证书。有关更多信息，请参阅 IBM Knowledge Center 中的 [WebSphere Application Server](https://www.ibm.com/support/knowledgecenter/SSAW57_9.0.0/com.ibm.websphere.nd.multiplatform.doc/ae/tsec_securecomm.html){: new_window} 或 [Liberty Core](https://www.ibm.com/support/knowledgecenter/SSD28V_9.0.0/com.ibm.websphere.wlp.core.doc/ae/twlp_sec_comm.html){: new_window} 文档。

## 防火墙端口
{: #firewall_ports}

您可能发现有必要打开防火墙上的端口，以允许访问应用程序和数据库。要打开防火墙端口，可以运行位于以下位置的 `openFirewallPorts.sh` 脚本。
  * 在每个 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 节点上，`openFirewallPorts.sh` 脚本都位于 `WAS_HOME/virtual/bin` 目录中。
  * 在每个 Liberty 集合体主机上，`openFirewallPorts.sh` 都位于 `WAS_HOME/virtual/bin` 目录中。

### 用法

使用以下命令语法，运行 `openFirewallPorts.sh` 脚本。

  ```
  openFirewallPorts.sh -ports <PORT>:<PROTOCOL>,... -persist true|false
  ```
  {: codeblock}

其中：
* PORT 是端口号
* PROTOCOL 是 TCP 或 UDP
* `-persist` 为 `true` 或 `false`

您可以使用逗号分隔列表指定多个端口。

**注**：所有打开端口的 sport 和 dport 已在防火墙的 INPUT 和 OUTPUT 部分打开。您必须使用 `sudo` 以 root 用户身份运行此脚本。还可以直接修改 iptables。

## 配置 Web 服务器
{: #configure_webserver}

供应单元或集合时，您收到预配置环境。尤其是对于传统 Network Deployment 单元，您收到以下环境：

* 与 IBM HTTP Server 并置的 Deployment Manager，用于开发和测试目的。
* 联合到 Deployment Manager 的定制节点。
* 全部初始供应到 STARTED 状态的 Deployment Manager、IHS Server 和 Node Agent。

如果您需要 Web 服务器处理所有用户请求，那么您在部署应用程序之后可能需要生成和传播插件。

**应注意的问题：**在生成和传播插件之前，请确保完成以下先决条件任务。

* 在本地 Windows、Linux 或 MAC 环境下，确保已配置 [openVPN](systemAccess.html#setup_openvpn) 并启动，并且您已经连接到相应的区域。
* 在 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服务仪表板上，单击**打开管理控制台**，然后使用 wsadmin 和服务仪表板中提供的管理密码进行登录。
* 在管理控制台中，创建应用程序服务器（例如，***server1****），因为 Deployment Manager 与空的定制节点联合。
* 启动所创建的服务器。
* 在应用程序安装期间，确保应用程序模块映射到您刚刚启动的服务器和 Web 服务器（例如，***webserver1***）。

以下高级步骤假定先决条件任务已完成。

1. 在“管理控制台”中，通过“环境”选项生成插件。
   1. 选择**环境 > 更新全局 Web 服务器插件配置**。
   2. 单击**确定**或**覆盖以生成新插件配置文件**。
2. 在 Deployment Manager 中，将插件复制到 Web 服务器配置。

  ```
   cp /opt/IBM/WebSphere/Profiles/DefaultDmgr01/config/cells/plugin-cfg.xml /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
  ```
  {: codeblock}
3. 打开 `IHS_HOME/conf`（例如，`/opt/IBM/WebSphere/HTTPServer/conf`）中的 `httpd.conf` 文件，并确保其中包含以下两行。

    ```
        LoadModule was_ap22_module /opt/IBM/WebSphere/Plugins/bin/64bits/mod_was_ap22_http.so
    WebSpherePluginConfig /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
    ```
    {: codeblock}  
4. 运行以下命令来打开端口。

   ```
   export serverPorts=2810:TCP,2810:UDP,8880:TCP,8880:UDP,9101:TCP,9101:UDP,9061:TCP,9061:UDP,9080:TCP,9080:UDP,9354:TCP,9354:UDP,9044:TCP,9044:UDP,9443:TCP,9443:UDP,5060:TCP,5060:UDP,5061:TCP,5061:UDP,11005:TCP,11005:UDP,11007:TCP,11007:UDP,9633:TCP,9633:UDP,7276:TCP,7276:UDP,7286:TCP,7286:UDP,5558:TCP,5558:UDP,5578:TCP,5578:UDP

   sudo /opt/IBM/WebSphere/AppServer/virtual/bin/openFirewallPorts.sh -ports $serverPorts -persist true
  ```
   {: codeblock}
5. 运行以下命令来停止和启动 Web 服务器：
    ```
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k stop
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k start
    ```
    {: codeblock}
8. 通过插件访问应用程序。
  ```
   http://169.53.246.xxx/contextRoot/
  ```
  {: codeblock}

**注：**所提供的步骤表示一种 Web 服务器配置方法，还有其他许多方法可尝试用于配置 Web 服务器。如果需要进一步的帮助，请参阅 [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/search/configure%20web%20server?scope=SSAW57_9.0.0){: new_window}。

如果无法访问应用程序，您的防火墙可能存在端口访问问题。因此，您可能需要重新启动以下任一服务器：应用程序服务器、节点代理程序、Web 服务器和部署管理器。此外，您可能还需要访问 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服务仪表板并重新启动每个虚拟机。
{: tip}

## SSL 配置
{: #ssl_configuration}

WebSphere Application Server Traditional 和 Liberty 是使用 [SSL_TLSv2](https://www.ibm.com/support/knowledgecenter/en/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/protocols.html){: new_window} 协议配置的。您可以通过修改 SSL 配置来更改协议。

### WebSphere Application Server Traditional
{: #ssl-was}

1. 打开 `security.xml` 文件，其位于 `/opt/IBM/WebSphere/Profiles/<profile_name>/config/cell/<cell_name>` 目录中，然后修改以下行。

   ```
  sslProtocol="SSL_TLSv2"
  ```
   {: codeblock}

2. 打开 `ssl.client.props` 文件，其位于 `/opt/IBM/WebSphere/Profiles/<profile_name>/properties` 目录中，然后修改以下行。

   ```
  com.ibm.ssl.protocol=SSL_TLSv2
  ```
   {: codeblock}

### Liberty
{: #ssl-liberty}

1. 打开 `server.xml` 文件，其位于 `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` 目录中，然后修改 `defaultSSLConfig` SSL 配置元素内的以下行。

   ```
  sslProtocol="SSL_TLSv2"
  ```
   {: codeblock}
