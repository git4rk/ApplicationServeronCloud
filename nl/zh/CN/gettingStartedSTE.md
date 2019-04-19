---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

keywords: single tenant, websphere, sales, order

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Single Tenant Environment
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}} Single Tenant Environment 为客户提供隔离的 WebSphere 工作负载、完全集成的混合环境和安全数据。本入门指南旨在让您了解哪些关键元素有助于访问和管理您的 Single Tenant Environment。
{: shortdesc}

## 订购 Single Tenant Environment
{:#ordering}

Single Tenant Environment 无法通过 {{site.data.keyword.Bluemix_notm}} 目录创建，必须通过联系 IBM 销售人员订购。订购环境时，您可以选择标准或自带许可证的 Single Tenant Environment。标准的 Single Tenant Environment 包括所有所需的基础架构和 WebSphere Application Server 许可证。在自带许可证的 Single Tenant Environment 中，您可以使用单独的 WebSphere Application Server 许可证。

要订购 Single Tenant Environment，请[联系 IBM 销售人员](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。销售团队可以协助您设置符合您需求的环境。

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment 概述
{: #overviewSTE}

Single Tenant Environment 可以让您拥有自己的专用服务实例、专用网络和隔离资源。虽然该产品是独立管理的，但服务和所创建服务实例的仪表板可以通过特定 {{site.data.keyword.Bluemix_notm}} 公共区域进行访问，如下图所示。

图 1. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment 的体系结构

![图 1. Single Tenant Environment 的体系结构](images/WASaaS.png)


## 组织管理
{: #organization_management}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment 是根据您的订单配置的。如果在订单中提供了一个或多个 {{site.data.keyword.Bluemix_notm}} 组织名称，那么可以立即开始访问环境。如果未提供组织名称，或者如果要更改此设置，请在您所在区域的 {{site.data.keyword.Bluemix_notm}} 控制台中，开具**应用程序服务**的[支持凭单](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#reporting_issues)。要在 {{site.data.keyword.Bluemix_notm}} 控制台中查找您的组织名称，请转至**管理 > 帐户 > Cloud Foundry 组织**。

**注：**要访问您的 Single Tenant Environment，请参阅 [Single Tenant Environment 访问](/docs/services/ApplicationServeronCloud?topic=wasaas-singleTenantEnvironment#singleTenantEnvironment)。
