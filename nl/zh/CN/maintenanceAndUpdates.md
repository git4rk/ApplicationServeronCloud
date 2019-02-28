---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 更新环境
{: #updating-your-environment}

## 维护策略
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} 会定期更新，以确保使用当前的修订包和补丁来创建新的服务实例。云能够简单快捷地为中间件管理供应新服务实例。

可以为特定产品版本创建当前或先前修订包级别（n 或 n-1）的 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 实例。使用当前修订包将提供最新的更新和功能，但可能需要先前的修订包才能符合混合云部署需求。

创建新实例时，可以从服务实例中的**服务概要文件**选项卡上的以下修订包级别中进行选择：

**Liberty**
  * 18.0.0.4
  * 18.0.0.3

**WebSphere Application Server Traditional**
  * 9.0.0.10
  * 9.0.0.9
  * 8.5.5.14
  * 8.5.5.13

## 应用修订和修订包更新
{:#applying-fixes}

更新到最新维护级别的最快方法是创建新实例。但是，如果您希望保留使用时间长的服务实例，那么可以通过运行提供的 `installService.sh` 脚本或使用 IBM Installation Manager，将维护应用于现有安装，如下列各部分中所述。

### 使用 installService.sh 脚本更新

服务实例配置有 Installation Manager 存储库，此存储库通过可用的安全修订和 WebSphere Application Server 修订包频繁更新。可以使用 `/home/virtuser/installService.sh` 脚本来应用这些修订和修订包。必须以 root 用户身份运行此脚本。

安装更新所需的磁盘空间量因您所安装的更新类型而异。仅安装临时修订需要虚拟机上有 1 GB 可用空间。安装修订包会使所需磁盘空间增加到 1.3 GB。

运行脚本会执行以下操作：

* 停止所有正在运行的 WebSphere Application Server 和 IBM HTTP Server 实例
* （可选）安装 Installation Manager、WebSphere Application Server、IBM HTTP Server 和 Java&trade; SDK 的最新修订包
* 安装 WebSphere、IBM HTTP Server 和 Java&trade; SDK 的最新临时修订
* 重新启动所有实例

#### 选项
* **`-fixpacks`**

    将所有包更新到最新的修订包。
* **`-noprompt`**

    在更新前不提示确认。

#### 语法示例

```
./installService.sh -?
```
{:.codeblock}

显示帮助文本。


```
./installService.sh
```
{:.codeblock}

安装所有适用的临时修订，但不安装修订包。


```
./installService.sh -fixpacks
```
{:.codeblock}

安装所有可用的修订包，然后安装所有适用的临时修订。

### 使用 Installation Manager 更新
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} 安装在 `/home/virtuser/IBM/Installation Manager` 目录中，并且可以直接运行以应用修订和修订包。

**应注意的问题：**由于底层二进制文件是以 `virtuser`（受限的管理虚拟用户）身份安装的，因此请确保始终以 `virtuser` 身份运行 Installation Manager。

## 对虚拟机应用系统更新
{:#vm-system-updates}

在虚拟机上应用系统更新类似于更新物理 Red Hat Enterprise Linux&reg; (RHEL) 系统。通过使用 Yum 包管理器，可以安装、更新、卸载和以其他方式管理包。WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 系统配置为接收来自 IBM 的 Red Hat Satellite 服务器的更新，该服务器提供了来自 Red Hat 网络的安全包。Satellite 服务器由 IBM 管理，不能通过自己的系统进行修改。

有关更多信息，请参阅 [Applying package updates on Red Hat Enterprise
Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} 和 [Yum（Red Hat 软件包管理器）](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}。
