---

copyright:
  years: 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# 入门教程
{:#getting-started}

通过 {{site.data.keyword.appserver_full}}，您可以在几分钟内就设置好预配置的 WebSphere Application Server 传统环境或 Liberty 环境。本入门教程将指导您如何只通过几个步骤，就在虚拟机上供应 WebSphere Application Server 环境。
{: shortdesc}

## 开始之前
{: #prereqs}

如果您需要的是具有更多专用虚拟机资源的环境（例如，保留合同或 Single Tenant Environment），您将需要在创建服务之前联系 IBM 销售人员。在[关于](index.html)中了解有关这些选项的更多信息。

## 步骤 1：创建服务
{: #create}

1. 转至 {{site.data.keyword.cloud_notm}}“目录”中的 [{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) 页面。
1. 使用 IBM 标识登录，或注册 {{site.data.keyword.cloud_notm}} 帐户。
1. 在目录页面上，查看用于服务配置的选择。

  对于现买现付环境，请使用缺省选择或根据您的需求进行修改。如果您有保留合同或 Single Tenant Environment，请特别注意以下选项。

  * **保留合同：**在**选择要部署的区域/位置**下，验证所选区域是否为合同的正确区域。

  * **Single Tenant Environment：**在**选择要部署的区域/位置**下，验证所选区域是否为部署了 Single Tenant Environment 的区域。在**环境**下，选择您的 Single Tenant Environment。缺省情况下，可能会显示公共环境。

    如果未列出您的 Single Tenant Environment，请检查您是否位于正确的区域中，以及您的组织是否有权访问您的 Single Tenant Environment。
    {: tip}
1. 针对要部署的 {{site.data.keyword.appserver_short}} 版本选择价格套餐。
1. 单击**创建**。


## 步骤 2：选择环境
{: #choose_env}

{{site.data.keyword.appserver_short}} Base 和 Liberty Core 套餐仅具有单服务器，因此，如果您选择了这些套餐，那么可以跳过此步骤。

对于 Network Deployment 套餐，请选择适用于您环境的概要文件和体系结构。

* **概要文件：**选择 {{site.data.keyword.appserver_short}} 传统或 Liberty
* **体系结构：**选择单服务器环境或具有传统单元或 Liberty 集合体的集群环境


## 步骤 3：调整虚拟机的大小
{: #vm_sizing}

可以针对环境中的每个组件单独调整虚拟机的大小。虚拟机大小调整以资源块的 [T 恤尺寸](index.html#vm-size)进行分块。

单击组件（例如，服务器、Deployment Manager 或应用程序节点）的对应选项卡，然后选择其虚拟机的 T 恤尺寸。

## 步骤 4：供应环境
{: #service_profile}

复查服务配置摘要中的详细信息，包括供应所需的估算时间。单击**供应**以设置 {{site.data.keyword.appserver_short}} 环境。

## 后续步骤
{: #anchor_value}

了解如何在[系统访问](systemAccess.html)中访问和管理新的 {{site.data.keyword.appserver_short}} 环境。
