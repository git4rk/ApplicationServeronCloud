---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 最新更新
{: #latest_updates}

服务的最新更新的列表。

## 2018 年 10 月 24 日：自带许可证计费现可用于保留合同和单租户环境。

如果您拥有现有 WebSphere Application Server 许可证，那么现在可以在保留合同或单租户环境中使用这些许可证。按自带许可证计费的环境提供与标准保留合同或单租户环境相同的功能，但是费率更低。要使用自带许可，请[联系 IBM 销售](reportingIssues.html#contacting-sales)。

## 2018 年 8 月 22 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 现在，在供应新服务实例时，传统 WebSphere Application Server 的 8.5.5.14 修订包可用。除了 8.5.5.14 外，传统 WebSphere Application Server 的其他修订包（例如，9.0.0.8、9.0.0.7 和 8.5.5.13）也可用于供应。
* 集成了其他服务维护。

## 2018 年 7 月 16 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 现在，在供应新服务实例时，传统 WebSphere Application Server 的 9.0.0.8 修订包版本可用。除了 9.0.0.8 外，传统 WebSphere Application Server 的其他修订包版本（例如，9.0.0.7、8.5.5.13 和 8.5.5.12）也可用于供应。
* 现在，在供应新服务实例时，WebSphere Application Server Liberty 的 18.0.0.2 修订包版本可用。除了 18.0.0.2 外，WebSphere Application Server Liberty 的 18.0.0.1 修订包版本也可用于供应。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=ibm10717691){: new_window}。
* 解决了 IBM SDK Java Technology Edition 中影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=ibm10718297){: new_window}。

## 2018 年 6 月 13 日：保留合同计费现在可用

使用保留合同计费时，可以购买预付费的每月预订，以保证对以物理方式保留的计算资源块进行访问。这些服务块已保留供您专用，不能视为是可供其他任何 {{site.data.keyword.appserver_full}} 用户使用的容量。您可以在一个月内以所选的任何方式使用服务块小时数，并根据典型的现买现付预订模型对任何超额量进行收费。

要了解有关保留合同计费的更多信息，请参阅[计费选项](index.html#billing-options)。

## 2018 年 3 月 30 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 现在，在供应新服务实例时，传统 WebSphere Application Server 的 9.0.0.7 修订包版本可用。除了 9.0.0.7 外，传统 WebSphere Application Server 的其他修订包版本（例如，9.0.0.6、8.5.5.13 和 8.5.5.12）也可用于供应。
* 现在，在供应新服务实例时，WebSphere Application Server Liberty 的 18.0.0.1 修订包版本可用。除了 18.0.0.1 外，WebSphere Application Server Liberty 的 17.0.0.4 修订包版本也可用于供应。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window}，包括：
  * IBM® Java SDK 中的多个漏洞
  * 导致 IBM WebSphere Application Server 针对管理控制台提供的安全性可能低于预期的漏洞。
  * 导致使用“表单登录”的 IBM WebSphere Application Server 安装可能允许远程攻击者执行电子欺骗攻击的漏洞。
  * 导致 IBM WebSphere Application Server 可能允许本地攻击者获取敏感信息的漏洞，此漏洞是由于处理应用程序请求不当引起的，可能允许未经授权的访问来读取文件。
  * 导致在多个产品中使用的 Apache Commons FileUpload 可能允许远程攻击者在系统上执行任意代码的漏洞，此漏洞是由于对 FileUpload 库的 DiskFileItem 类中不可信数据进行反序列化引起的。远程攻击者可能利用此漏洞在当前进程的上下文中执行任意代码。
  * 导致 Intel Haswell Xeon、AMD PRO 和 ARM Cortex A57 CPU 可能允许经认证的本地攻击者获取敏感信息的漏洞，此漏洞是由于 CPU 推测转移指令执行功能中的边界检查旁路引起的。通过执行有针对性的高速缓存端通道攻击，攻击者可能利用此漏洞来跨越 syscall 边界，并从 CPU 虚拟内存中读取数据。
* 集成了其他服务维护。

## 2018 年 1 月 8 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

*  现在，在供应新服务实例时，传统 WebSphere Application Server 的 9.0.0.6 修订包版本可用。除了 9.0.0.6 外，传统 WebSphere Application Server 的其他修订包版本（例如，9.0.0.5、8.5.5.12 和 8.5.5.11）也可用于供应。
* 现在，在供应新服务实例时，WebSphere Application Server Liberty 的 17.0.0.4 修订包版本可用。除了 17.0.0.4 外，WebSphere Application Server Liberty 的 17.0.0.3 修订包版本也可用于供应。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window}，包括：
  * 导致 OpenSAML 可能允许经认证的远程攻击者获取敏感信息的漏洞，此漏洞是由于解析 XML 实体时的错误引起的。
  * 导致 Apache HTTP Server 可能允许远程攻击者获取敏感信息的漏洞，此漏洞是由于 HTTP OPTIONS 方法中的缺陷（称为 Optionsbleed）引起的。
  * 导致 Apache 可移植运行时实用程序 (APR-util) 易受拒绝服务攻击的漏洞，此漏洞是由于未能验证 apr_sdbm*() 函数所使用的 SDBM 数据库文件的完整性引起的。
* 集成了其他服务维护。

## 2017 年 12 月 21 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 在达拉斯、伦敦和悉尼添加了 WebSphere Application Server in IBM Cloud 迁移功能。此功能提供从现有 V7、V8 或 V8.5.5 内部部署环境到 IBM Cloud 中 V9 环境的完整端到端迁移。有关更多信息，请参阅 [WebSphere Configuration Migration Tool for IBM Cloud](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud)。
* 集成了其他服务维护。

## 2017 年 10 月 27 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 添加了通过 {{site.data.keyword.Bluemix_notm}} 服务仪表板的“服务概要文件”选项卡或通过 REST API 来供应较旧修订包级别 [(n-1)](maintenanceAndUpdates.html#maintenance-strategy){: new_window} 的功能。
*  现在，在供应新服务实例时，传统 WebSphere Application Server 的 9.0.0.5 修订包版本可用。除了 9.0.0.5 外，传统 WebSphere Application Server 的其他修订包版本（例如，9.0.0.4、8.5.5.12 和 8.5.5.11）也可用于供应。
* 现在，在供应新服务实例时，WebSphere Application Server Liberty 的 17.0.0.3 修订包版本可用。除了 17.0.0.3 外，WebSphere Application Server Liberty 的 17.0.0.2 修订包版本也可用于供应。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window}，包括：
  * 导致在使用定制启动脚本时，IBM WebSphere Application Server 可能使用缺省许可权而不是定制许可权来创建文件的漏洞。
  * 导致 IBM WebSphere Application Server 代理服务器或按需路由器 (ODR) 可能允许本地攻击者获取敏感信息的漏洞，此漏洞是由于高速缓存了旧数据并随后提供这些数据引起的。
  * 导致 IBM WebSphere Application Server 易受跨站点脚本攻击的漏洞。此漏洞允许用户在 Web UI 中嵌入任意 JavaScript 代码来改变目标功能，可能会导致在可信会话中泄露凭证。
  * 导致 IBM WebSphere Application Server 在您使用管理控制台来更新 Web Service 安全性绑定设置后，提供的安全性可能低于预期的漏洞。
  * 导致 IBM WebSphere Application Server V9.0.0.4 在您使用 PasswordUtil 命令来启用 AES 密码加密后，提供的安全性可能低于预期的漏洞。
  * 导致 Apache MyFaces 可能允许远程攻击者获取敏感信息的漏洞。
  * 导致 IBM WebSphere Application Server 可能允许远程攻击者获取敏感信息的漏洞，此漏洞是由于 JSF 中 MyFaces 处理错误不当引起的。
* 集成了其他服务维护。

## 2017 年 8 月 30 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。

## 2017 年 6 月 30 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 FP8.5.5.12 或 FP9.0.0.4 可以随传统 WebSphere Application Server 的新实例一起安装。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 FP17.0.0.2 可以随 WebSphere Application Server Liberty（Core 和 ND 套餐）的新实例一起安装。
* 添加了[高级 VPN 配置管理](networkEnvironment.html#advancedVPN){: new_window}功能，以允许在伦敦和悉尼区域中创建和管理多个 VPN 配置。
* 向[公用因特网访问](networkEnvironment.html#publicInternetAccess){: new_window}功能添加了增强功能，以允许客户更好地管理其公共 IP 地址。
* 解决了 IBM SDK Java Technology Edition 中影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window}，包括：
  * Java SE AWT 组件的不明确漏洞，此漏洞可能允许未经认证的攻击者控制系统。
  * Java SE JCE 组件的不明确漏洞，此漏洞可能允许未经认证的攻击者控制系统。
  * Java SE JAXP 组件的不明确漏洞，此漏洞可能允许未经认证的攻击者使用未知攻击向量生成拒绝服务，从而导致高可用性影响。
  * Java SE Networking 组件的不明确漏洞，此漏洞可能允许未经认证的攻击者带来低机密性影响、低完整性影响和无可用性影响。
  * Java SE Networking 组件的不明确漏洞，此漏洞可能允许未经认证的攻击者带来无机密性影响、低完整性影响和无可用性影响。
  * Java SE Security 组件的不明确漏洞，此漏洞可能允许未经认证的攻击者带来无机密性影响、低完整性影响和无可用性影响。
  * 导致处理 XML 数据时发生 XML 外部实体注入 (XXE) 错误的漏洞。远程攻击者可利用此漏洞来公开高敏感性信息或使用内存资源。
  * 导致 zlib 易受拒绝服务攻击的问题，此问题是由于 inftrees.c 中的越界指针算术引起的。
  * 导致 zlib 易受拒绝服务攻击的问题，此问题是由于未定义的负数左移引起的。
  * 导致 zlib 易受拒绝服务攻击的问题，此问题是由于大尾数法越界指针引起的。

## 2017 年 5 月 25 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。
* 添加了[高级 VPN 配置管理](networkEnvironment.html#advancedVPN){: new_window}功能，以允许在法兰克福区域中创建和管理多个 VPN 配置。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 JDK 8 可以随服务的所有新实例一起安装。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window}，包括：
  * WebSphere Application Server MQ JCA 资源适配器的潜在安全漏洞。
  * 库组件的不明确漏洞，此漏洞可能允许远程攻击者使用未知攻击向量获取敏感信息，从而导致高机密性影响。

## 2017 年 4 月 21 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window}，包括：
  * 导致配置了 OpenID Connect (OIDC) 信任关联拦截器 (TAI) 的 WebSphere Application Server 可能允许用户在系统上获取提升特权的漏洞。
  * 导致 WebSphere Application Server 提供的安全性可能低于预期的漏洞。远程攻击者可能利用此漏洞来获取敏感信息，并获得对管理控制台的未经授权的访问。
  * 导致 WebSphere Application Server 易受跨站点请求伪造攻击的问题，此问题可能允许攻击者执行通过 Web 站点信任的用户传输的恶意和未经授权的操作。


## 2017 年 3 月 15 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 FP8.5.5.11 或 FP9.0.0.3 可以随传统 WebSphere Application Server 的新实例一起安装。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window}，包括：
  * 库组件的不明确漏洞，此漏洞存在无机密性影响、高完整性影响和无可用性影响。
  * 库组件的不明确漏洞，此漏洞可能允许远程攻击者使用未知攻击向量获取敏感信息，从而导致高机密性影响。
  * 库组件的不明确漏洞，此漏洞可能允许远程攻击者使用未知攻击向量生成拒绝服务，从而导致低可用性影响。
  * OpenSSL 中可能允许远程攻击者获取敏感信息的漏洞，此漏洞是由于用作 SSL/TLS 协议一部分的 DES/3DES 密码中的错误引起的。
  * 允许用户在 Web UI 中嵌入任意 JavaScript 代码来改变目标功能的漏洞，此漏洞可能会导致在可信会话中泄露凭证。
  * Apache HTTPD 中会受到 HTTP 响应分割攻击的漏洞，此漏洞是由对用户提供的输入不正确验证引起的。
  * Samba 中允许经过认证的远程攻击者获取对系统的提升特权的漏洞，此漏洞是由于处理 PAC 校验和失败引起的。
  * Samba 中允许经过认证的远程攻击者获取对系统的提升特权的漏洞，此漏洞是由于使用 Kerberos 认证时将凭单授权凭单 (TGT) 转发给其他服务引起的。
  * Samba 中会导致基于堆的缓冲区溢出的漏洞，此漏洞是由 ndr_pull_dnsp_name() 函数中的整数包装缺陷引起的。


## 2017 年 2 月 10 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 FP8.5.5.11 或 FP9.0.0.2 可以随传统 WebSphere Application Server 的新实例一起安装。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 FP16.0.0.4 可以随 WebSphere Application Server Liberty（Core 和 ND 套餐）的新实例一起安装。
* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中的[若干安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window}，包括：
  * 会导致拒绝服务的漏洞，此漏洞是由允许运行来自不可信源的序列化对象引起的，会造成资源耗用。
  * 使用格式不正确的 SOAP 请求，这可能会允许远程攻击者获取敏感信息。


## 2016 年 12 月 16 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 集成了其他服务维护。
* 解决了 IBM SDK Java Technology Edition 中影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window}，包括：
  * Oracle Java SE 和 Java SE Embedded 中与热点组件相关的不明确漏洞，此漏洞存在高机密性影响、高完整性影响和高可用性影响。
  * Oracle Java SE 和 Java SE Embedded 中与联网组件相关的不明确漏洞，此漏洞可能允许远程攻击者使用未知攻击向量获取敏感信息，从而导致高机密性影响。
  *  IBM WebSphere Application Server 中的跨站点脚本编制漏洞，此漏洞允许用户在 Web UI 中嵌入任意 JavaScript 代码。此代码可能会潜在改变目标功能，从而导致在可信会话中泄露凭证。


## 2016 年 11 月 8 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已添加客户机为 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM 请求[公共 IP](networkEnvironment.html#networkEnvironment) 地址的功能 
* 解决了影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window}，包括：
  * IBM WebSphere Application Server 中可能允许远程攻击者使用不可信源的序列化对象执行任意 Java 代码的漏洞。
  * 由 TS_OBJ_print_bio 函数中的越界读取导致的拒绝服务漏洞。远程攻击者可能使用特制的时间戳记文件，利用此漏洞来导致应用程序崩溃。
  * OpenSSL 中可能允许远程攻击者获取敏感信息的潜在漏洞，此漏洞是由于用作 SSL/TLS 协议一部分的 64 位块密码上三重 DES 中的错误引起的。通过捕获 SSL/TLS 服务器和客户机之间的大量加密流量，能够进行中间人攻击的远程攻击者可能利用此漏洞恢复纯文本数据与获取敏感信息。此漏洞称为“SWEET32 生日”攻击。
  * OpenSSL 中拒绝服务漏洞。远程认证攻击者通过重复请求重谈，可能发送过量的 OCSP 状态请求扩展，以使用所有可用内存资源。
  * OpenSSL 中拒绝服务漏洞，这是由 MDC2_Update 函数中整数溢出导致的。远程攻击者使用未知的攻击向量，利用此漏洞发出越界写入，导致应用程序崩溃。
  * OpenSSL 中允许远程攻击者获取敏感信息的潜在漏洞，这是由于 DSA 实施中允许特定操作的非常量时间代码路径追踪错误引起的。攻击者可能使用高速缓存时序攻击，利用此漏洞来恢复专用 DSA 密钥。
  * OpenSSL 中拒绝服务漏洞，这是由解析证书时没有进行消息长度检查导致的。远程认证攻击者可利用此漏洞发出越界读取，并导致拒绝服务。

## 2016 年 9 月 19 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 WebSphere Application Server Liberty（Core 和 ND 套餐）的新实例可以使用 FP16.0.0.3。
* 解决了影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window}，包括：
  *  IBM WebSphere Application Server Liberty 中允许远程攻击者进行钓鱼攻击的漏洞。
  * IBM WebSphere Application Server Liberty 中跨站点在 OpenID Connect 客户机进行脚本编制的漏洞。
  * IBM WebSphere Application Server Liberty 中允许远程攻击者获取敏感信息的潜在漏洞，这是由于缺省错误页面不存在时不正当地处理异常导致的。
  * Apache Tomcat 中拒绝服务漏洞，由 Apache Commons FileUpload 组件中的错误导致。
  * IBM WebSphere Application Server 和 IBM WebSphere Application Server Liberty 中的漏洞，该漏洞可能允许远程攻击者获取敏感信息，由特定条件下对响应的不当处理导致的。
  * 联网组件的不明确漏洞，此漏洞存在无机密性影响、低完整性影响和无可用性影响。

## 2016 年 8 月 17 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 将 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 从 8.5.5.9 升级到了 8.5.5.10
* 解决了影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window}，包括：
  * 对 WebSphere Application Server 和 WebSphere Application Server Hypervisor Edition 管理控制台有影响的 Apache Struts 漏洞。
  * 使用 SIP 服务时 IBM WebSphere Application Server 中潜在的拒绝服务漏洞。
  * 对 WebSphere Application Server 使用的 IBM HTTP Server 可能有影响的若干漏洞。
  * 可重定向 CGI 应用程序的 HTTP 流量的漏洞，其可能会影响 IBM HTTP Server (IHS)。此漏洞称为“HTTPOXY”。
  * IBM WebSphere Application Server 中的信息披露漏洞。
  * IBM WebSphere Application Server 中潜在的绕过安全限制漏洞（只有启用了 Web 容器定制属性 `HttpSessionIdReuse` 的环境才会出现此漏洞）。


## 2016 年 6 月 24 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 为客户新增了在创建新的_传统 ND_ 或_传统 WebSphere_ 实例时，可以选择 V8.5 或 V9.0 的能力。
* 升级了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，以便 WebSphere Application Server Liberty（Core 和 ND 套餐）的新实例可以使用 FP16.0.0.2。16.0.0.2 是 8.5.5.9 之后的下一个修订包。从 16.0.0.2 开始，缺省情况下会安装这些套餐支持的所有授权 Liberty 可选功能部件。
* 解决了影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[若干安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window}，包括：
  * Apache Standard Taglibs 中的 XML 外部实体注入 (XXE) 漏洞，该漏洞会影响到 IBM WebSphere Application Server。
  * WebSphere Application Server Liberty 概要文件 API 发现功能部件和 Swagger 文档的安全性可能低于预期安全性的漏洞。
  * IBM WebSphere Application Server Liberty 管理中心内的潜在信息披露漏洞。
  * IBM WebSphere Application Server 中的潜在 HTTP 响应分割漏洞。
  * 2016 年 5 月 3 日由 OpenSSL Project 披露的 OpenSSL 漏洞。

## 2016 年 6 月 13 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 添加了新功能，使客户可以通过创建使用 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} RESTful API 的应用程序或脚本来构建、供应、管理和删除虚拟机实例。
* 添加了新功能，使客户的固定“已停止”实例数控制为 10 个 IP 地址或 64 GB 内存以内。现在，对于“已停止”状态的累计实例，我们向客户减免 5%。

## 2016 年 4 月 26 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 解决了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中在启用 FIPS 140-2 时的[潜在安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window}以及 Samba 中的多个漏洞（包括 Badlock 漏洞）。
* 集成了其他服务维护。

## 2016 年 4 月 15 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 将 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 从 8.5.5.8 升级到了 8.5.5.9
* 解决了 {{site.data.keyword.Bluemix_notm}} 的 Liberty for Java 中影响客户使用 OpenID Connect (OIDC) 客户机的[跨站点脚本编制](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window}漏洞。
* 集成了其他服务维护。

## 2016 年 2 月 19 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 为应用程序占用大量内存的客户添加了一个选项，以便使用更大型的虚拟机来合理调整其环境的大小。客户可选择具有特定资源大小且最多包含 32 GB RAM 虚拟机的给定 WebSphere Application Server 组件或单个系统。
* 将 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 从 8.5.5.7 升级到了 8.5.5.8
* 解决了 IBM SDK Java Technology Edition 中影响 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的多个漏洞，通常这些漏洞称为 [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}。
* 解决了影响客户使用 OAuth 提供程序输出的[跨站点脚本编制](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window}漏洞。
* 集成了其他服务维护。

## 2015 年 12 月 11 日：更新了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 将正式的产品名称从 IBM Application Server on Cloud in {{site.data.keyword.Bluemix_notm}} 更改为 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 向 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 套餐添加了新功能。该计划包含带有两个或更多虚拟机的 WebSphere Application Server Network Deployment 单元环境。这些新功能允许用户设置集群环境，以用于高可用性、故障转移和可扩展性。
* 向 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Liberty Core 套餐添加了新功能。该计划包含使用 Liberty 集合体，作为 Liberty 概要文件（服务器）组的管理域，该集合由两个或更多虚拟机组成
* 将 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 从 8.5.5.6 升级到了 8.5.5.7
* 解决了用于处理 Java 对象编组的 [Apache Commons Collection 漏洞](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window}。
* 解决了可能允许 [HTTP 响应分割攻击](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}的漏洞。
* 集成了其他服务维护。

## 2015 年 10 月 15 日：更新了 Application Server on Cloud
* 新增了以下两个新计划：
  * [WebSphere Application Server Traditional V9 Beta](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* 其他服务维护
