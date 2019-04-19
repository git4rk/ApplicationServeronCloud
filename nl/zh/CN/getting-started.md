---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-18"

keywords: migrate websphere, create service, profile, architecture, vm, virtual machine, provision

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# 入门教程
{: #getting-started}

通过 {{site.data.keyword.appserver_full}}，您可以在几分钟内就设置好预配置的 WebSphere Application Server Traditional 环境或 Liberty 环境。本入门教程将指导您如何只通过几个步骤，就在虚拟机上供应 WebSphere Application Server 环境。
{: shortdesc}

## 开始之前
{: #prereqs}

如果需要具有更多专用虚拟机资源的环境（例如，保留合同或 Single Tenant Environment），请在创建服务之前联系 IBM 销售人员。在[关于](/docs/services/ApplicationServeronCloud?topic=wasaas-about#about)中了解有关这些选项的更多信息。

### 迁移现有 WebSphere 环境

要将现有的 WebSphere Application Server Network Deployment 环境迁移到此服务，请使用 [WebSphere Configuration Migration Tool for {{site.data.keyword.cloud_notm}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){:new_window}。该工具会将单机服务器或单元节点的概要文件配置和应用程序上传到 {{site.data.keyword.cloud_notm}} 中的服务实例内。有关云迁移的概述和使用此工具的分步说明，请参阅 WASdev 上的
[WebSphere Configuration Migration Tool for IBM Cloud guide ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){:new_window}。

下面的步骤将指导您在 {{site.data.keyword.appserver_full}} 中逐步创建新环境。

## 步骤 1：创建服务
{: #create}

1. 转至 {{site.data.keyword.cloud_notm}}“目录”中的 [{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server) 页面。
1. 使用 IBM 标识登录，或注册 {{site.data.keyword.cloud_notm}} 帐户。
1. 在目录页面上，查看用于服务配置的选择。

  对于现收现付环境，请使用缺省选择或根据您的需求进行修改。

  如果您有保留合同或 Single Tenant Environment，请特别注意以下选项。

  * **保留合同：**在**选择要部署的区域/位置**下，验证所选区域是否为合同的正确区域。

  * **Single Tenant Environment：**在**选择要部署的区域/位置**下，验证所选区域是否为部署了 Single Tenant Environment 的区域。在**环境**下，选择您的 Single Tenant Environment。缺省情况下，可能会显示公共环境。

    如果您的 Single Tenant Environment 未列出，请检查您是否位于正确的区域中，以及您的组织是否有权访问您的 Single Tenant Environment。
    {: tip}
1. 针对要部署的 {{site.data.keyword.appserver_short}} 版本选择价格套餐。
1. 单击**创建**。


## 步骤 2：选择您的环境（仅限 Network Deployment）
{: #choose_env}

{{site.data.keyword.appserver_short}} Base 和 Liberty Core 套餐仅具有单服务器。因此，如果选择了这些套餐，那么可以跳过此步骤。

对于 Network Deployment 套餐，请选择适用于您环境的概要文件和体系结构。

* **概要文件：**选择 {{site.data.keyword.appserver_short}} 传统或 Liberty
* **体系结构：**选择单服务器环境或具有传统单元或 Liberty 集合体的集群环境


## 步骤 3：调整虚拟机的大小
{: #vm_sizing}

可以针对环境中的每个组件单独调整虚拟机的大小。虚拟机以资源块的 [T 恤尺寸](/docs/services/ApplicationServeronCloud?topic=wasaas-about#vm-size)进行分块。

单击组件（例如，服务器、Deployment Manager 或应用程序节点）的对应选项卡，然后选择其虚拟机的 T 恤尺寸。

## 步骤 4：供应环境
{: #service_profile}

复查服务配置摘要中的详细信息，包括供应所需的估算时间。

**保留合同：**确保**计费**选项设置为_保留合同_。如果您没有看到此选项，请验证[您的组织名称](/docs/account?topic=account-orgsspacesusers){:new_window}与合同上的组织名称是否完全一致，包括大小写和空格。如果您供应服务时没有选择保留合同计费，那么将使用现收现付计费。

单击**供应**以设置 {{site.data.keyword.appserver_short}} 环境。

## 后续步骤
{: #anchor_value}

了解如何在[系统访问](/docs/services/ApplicationServeronCloud?topic=wasaas-system_access)中访问和管理新的 {{site.data.keyword.appserver_short}} 环境。
