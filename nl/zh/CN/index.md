---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 关于
{: #about}

{{site.data.keyword.appserver_full}} 有助于您在 {{site.data.keyword.Bluemix_notm}} 上的托管云环境中快速设置预配置的 WebSphere Application Server Liberty、传统 Network Deployment 或传统 WebSphere Java EE 实例。
{: shortdesc}

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 概述
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 为使用者提供预配置的传统 WebSphere 和 Liberty 服务器。
该服务在虚拟机上托管，具有根访问权的虚拟机访客可以访问访客操作系统。创建服务时，请在 _Liberty_、_传统 ND_ 或_传统 WebSphere_ 之间进行选择。

**注：**现在，当您创建任何 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 实例时，使用者能够选择当前修订包级别或旧版本 [（n 或 n-1）](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window}。

为您提供了熟悉的 WebSphere 管理体验，并且您对底层的操作系统具有完全访问权。您可以复用现有脚本，并视需要进行一些系统微调，以便与您自己的或第三方的框架搭配使用。系统提供了管理中心和管理控制台来管理 WebSphere Application Server Liberty、ND 或传统服务，就像内部部署 WebSphere 配置那样。

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 套餐包含带有两个或更多虚拟机的 WebSphere Application Server Network Deployment 单元环境。第一个虚拟机包含 Deployment Manager 和 IBM HTTP Server，而其余的虚拟机包含联合到 Deployment Manager 的定制节点（节点代理程序）。使用现有的 wsadmin 脚本来创建 WebSphere 配置，或者使用 WebSphere 管理控制台来手动配置环境。这些新功能允许用户设置集群环境，这是任何中间件企业应用程序的一个关键方面。现在，客户可以选择建立拓扑集群，以实现两个或更多实例之间的请求负载平衡。


WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 套餐还包含使用 Liberty 集合体。Liberty 集合体是 Liberty Profile（服务器）组的管理域，由两个或更多虚拟机组成。第一个虚拟机包含集合体控制器 Liberty 服务器，这是 Liberty 集合体的控制点。除了 Liberty 集合体之外，此虚拟机还包含 IBM HTTP Server，后者允许从 Web 浏览器访问应用程序。其余的虚拟机是集合体成员（Liberty Profile 服务器）所在的集合体主机。同时还在 Liberty 控制器服务器上启用了 Liberty 管理中心功能。

下图显示了 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 单元和 Liberty 集合体环境的体系结构。

图 1. Network Deployment 单元和 Liberty 集合体的体系结构

![图 1. Network Deployment 单元和 Liberty 集合体的体系结构](images/CellCollectiveDiagram.gif)

**注**：在以上_图 1_ 中，描述 Deployment Manager 或集合体控制器与 IBM HTTP Server 的并置的模式用于开发和测试目的。WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 还允许您重新配置预安装的软件，以满足生产应用程序和操作需求，就像内部部署一样。有关最严格生产需求，请联系 IBM 销售代表，他们可以介绍单租户 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 产品，该产品提供单独的网络和计算资源。


## 运营环境
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 是一种在共享环境中返回访客（虚拟机）供使用者部署应用程序的服务。VPN 可以使公共服务不用进行通用端口扫描，还可以使其免于遭受其他基于主动网络的攻击。但是，值得注意的是您用来访问服务实例的服务 VPN 可
能在多个 {{site.data.keyword.Bluemix_notm}} 组织和用户之间进行共享。虚拟机可提供计算资源、内存资源和 I/O 资源，这些资源都来自于 IaaS 资源共享池。

由于虚拟机在共享环境中运行特定的计算资源、内存资源和 I/O 资源，因此服务配置可能会所有不同。通过 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服务仪表板和门户网站，可查看每个特定服务实例的配置。

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 提供虚拟机实例。通过这些实例，客户可使用简单门户网站，以一致且可重复的方式创建并管理企业 WebSphere Application Server 部署，并极其自由地调整其应用程序。用户可对托管云环境中的预配置 WebSphere Application Server Liberty、ND 或传统虚拟机快速入门和熟悉运用。用户可将现有 WebSphere Application Server 应用程序迁移到 {{site.data.keyword.Bluemix_notm}}，并完全控制底层操作系统和中间件。

## 虚拟机大小调整
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 提供了 T 恤尺寸调整功能，以便可以针对应用程序占用大量内存的环境，通过供应更大型的虚拟机来合理调整环境大小。为运行 WebSphere Application Server 而供应的每个虚拟机的大小都可以根据预期资源需求进行独立调整。

虚拟机的大小调整和定价单位为*块*。对于 T 恤尺寸中的每个块，将为虚拟机供应以下资源。
* 1 个虚拟 CPU (vCPU)
* 2 GB RAM
* 12.5 GB 硬盘驱动器空间（单块 VM 为 12.0 GB）


|T 恤|块数|vCPU 数|RAM (GB)|HD (GB)|
|:-------:|:------:|:----------:|:--------------:|:-------------:|
|S|1|1|2|12|
|M|2|2|4|25|
|L|4|4|8|50|
|XL|8|8|16|100|
|XXL|16|16|32|200|
{: caption="表 1. 每种 T 恤尺寸的块数" caption-side="top"}

每个服务器或节点都在单个虚拟机中进行供应。例如，在 Network Deployment 套餐中，如果为 Deployment Manager 供应 1 个 M 号虚拟机（2 个块），为应用程序节点供应 8 个 S 号虚拟机（1 个块），那么将总共收取 10 个块的费用。

## 计费选项
{: #billing-options}

每个块的定价取决于您选择的计费选项：
* **[现收现付](#pay-as-you-go)：**基于使用量计费，按使用的每个块的小时数定价
* **[保留合同](#reserve-contract)：**预付费的每月保留资源预订

### 现买现付
{: #pay-as-you-go}

如果并未联系 IBM 销售人员来获取替代的计费选项就供应 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服务，那么将应用现收现付定价。按每月结算周期内使用的每个块的整小时或不足一小时收费。最小计费设置为 1/4 个块小时。

**注**：由于特定的计算、内存和 I/O 资源量，对停止的实例收费时，会在每小时块费率的基础上减免 5%。在该服务中，停止的实例限制为 10 个 IP 地址或 64 GB 内存。

#### 套餐定价

每个块的价格根据您选择的 WebSphere Application Server 套餐而异。

下表列出了每个 T 恤尺寸的虚拟机每小时的总价格。价格表示 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 套餐截至 2016 年 4 月 1 日的价格，以美元 (USD) 表示。请参阅您所在区域中当前价格的目录。

|T 恤|块数|Liberty Core|WAS Base|WAS ND|
|:-------:|:------:|:----------:|:------:|:----------:|
|S|1|$0.21|$0.30|$0.70|
|M|2|$0.42|$0.60|$1.40|
|L|4|$0.84|$1.20|$2.80|
|XL|8|$1.68|$2.40|$5.60|
|XXL|16|$3.36|$4.80|$11.20|
{: caption="表 2. Liberty Core 套餐" caption-side="top"}


### 保留合同
{:#reserve-contract}

使用保留合同计费时，可以购买预付费的每月预订，以保证对以物理方式保留的计算资源块进行访问。这些服务块已保留供您专用，不能视为是可供其他任何 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 用户使用的容量。如果您拥有现有 WebSphere Application Server 许可证，那么您可以选择自带许可证的保留合同，该合同将使用这些许可证，并且计费费率更低。要设置保留合同计费，请[联系 IBM 销售人员](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。

预订以 8 个块为增量提供。总块小时数基于一个月中的小时数，但您可以在整个月内的任何时间点使用块小时数。例如，一个月有 30 天，共 720 小时，此小时数乘以 8 个块的预订，得出的总数为 5,760 个块小时。

  ```
30 天 * 24 小时/天 * 8 个块 = 5,760 个块小时
  ```

可以定制如何以及何时使用块以满足可变工作负载需求，例如先使用 4 个块，接着增加到 12 个块，然后又减少到 8 个块。只要不超出一个月内的总块小时数，便无需额外付费。

供应每个环境时，您可以选择使用保留合同块或者现收现付计费。

**注：**如果删除服务实例，那么您可能需要等待大约 30 分钟，然后其块才可用于新的服务实例。

#### 超额

如果使用量超过预订中的每月块小时数，那么会根据按使用量计费模型来收取超额费用，所以只会向您收取使用的额外块小时数的费用。块使用量按整小时或不足一小时计算，最小使用量为 1/4 个块小时。

现收现付模型中的块不是保留容量，而是来自公共资源池。

#### 分摊比率，使用灵活

保留合同计费中的块数基于 WebSphere Application Server Network Deployment 套餐，但您也可以使用其他套餐的块。对于其他套餐，将按比例分摊使用量，这样当一个块小时反映在剩余保留合同块小时中时，将按套餐的分摊比率减去一个块小时。

下表显示了每个套餐的分摊比率以及计算的按比例分摊后每个实际块小时的生效价格。对于您所在区域的当前价格，请[联系 IBM 销售人员](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。

|套餐|分摊比率|按比例分摊后的价格/小时|
|:-------:|:------:|:------:|
|WebSphere Application Server Liberty Core|0.3|$0.21|
|WebSphere Application Server Base|0.43|$0.30|
|WebSphere Application Server Network Deployment|1.0|$0.70|
{: caption="表 3. 按套餐列出的块小时分摊比率" caption-side="top"}

例如，您可能有一个 M 号（2 个块）WebSphere Application Server Base 实例运行了 51 小时。要计算保留合同中使用的块小时数，请将实际的块小时数乘以分摊比率，得出总计为 43.86 个块小时：

```
2 个块 * 51 个小时 * 0.43 分摊比率 = 43.86 个按比例分摊的块小时
```

总成本保持不变，但您可以使用按比例分摊的套餐的更多实际块小时数，因为从保留合同块小时数中扣除的更少。
{:.tip}
