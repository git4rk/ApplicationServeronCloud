---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Single Tenant Environment
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}}: Single Tenant Environment 产品为客户提供隔离的 WebSphere 工作负载、完全集成的混合环境和安全数据。本入门指南旨在确定有助于客户在 {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment 中访问和管理自己的 WebSphere Application Server 的关键元素。
{: shortdesc}


## 建议的软件
{: #recommended_software}

您需要以下软件来访问 Single Tenant Environment：
* {{site.data.keyword.Bluemix_notm}} 支持的 Web 浏览器：
    * Chrome：适用于您的操作系统的最新版本
    * Firefox：适用于您的操作系统的最新版本或最新的 ESR 版本
    * Internet Explorer：V10 或 V11
    * Safari：适用于 Mac 的最新版本
* Cloud Foundry 命令行界面 V6.5.1 或更高版本（可以使用最新发行版）
* Git Bash（建议）
    * 下载并安装 [Git Bash](https://git-scm.com/downloads){: new_window}


## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment 概述
{: #overviewSTE}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment 产品为使用者提供了自己的专用服务实例、专用网络和隔离资源。虽然该产品是独立管理的，但服务和所创建服务实例的仪表板可以通过特定 {{site.data.keyword.Bluemix_notm}} 公共区域进行访问，如下图中所示：

图 1. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment 的体系结构

![图 1. Single Tenant Environment 的体系结构](images/WASaaS.png)


## 组织管理
{: #organization_management}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment 是根据您的订单配置的。如果在订单中提供了一个或多个 {{site.data.keyword.Bluemix_notm}} 组织名称，那么可以立即开始访问环境。如果未提供一个或多个组织名称，或者如果要更改此设置，请在您所在区域的 {{site.data.keyword.Bluemix_notm}} 控制台中，开具**应用程序服务**的[支持凭单](reportingIssues.html#reporting_issues)。组织名称 (ORG) 可以在 {{site.data.keyword.Bluemix_notm}} 控制台的右上角找到，如下图中所示：

图 2. 组织名称的位置

![图 2. 组织名称的位置](images/myORG.png)


**注：**要访问您的 Single Tenant Environment，请参阅 [Single Tenant Envir onment 访问](singleTenantAccess.html#singleTenantEnvironment)。
