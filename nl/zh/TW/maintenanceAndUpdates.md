---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 更新環境
{: #updating-your-environment}

## 維護策略
{: #maintenance-strategy}

定期更新 {{site.data.keyword.appserver_full}}，確保使用現行修正套件及修補程式來建立新的服務實例。雲端為中介軟體管理帶來了輕鬆而快速的新服務實例佈建。

您可以在特定產品版本的現行或前一個修正套件層次（n 或 n-1）建立 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 實例。使用現行修正套件可提供最新更新項目及特性，但可能需要前一個修正套件，才能符合混合式雲端部署需求。

當您建立新的實例時，可以在服務實例的**服務設定檔**標籤上，從下列修正套件層次中進行選擇：

**Liberty **
  * 18.0.0.4
  * 18.0.0.3

**WebSphere Application Server 傳統**
  * 9.0.0.10
  * 9.0.0.9
  * 8.5.5.14
  * 8.5.5.13

## 套用修正程式及修正套件更新項目
{:#applying-fixes}

更新最新維護層次的最快速方式是建立新的實例。不過，如果您偏好保留長期存在的服務實例，則可以執行所提供的 `installService.sh` Script，或如下列各節所述使用 IBM Installation Manager，以將維護套用至現有安裝。

### 使用 installService.sh Script 更新

您的服務實例已配置使用可用安全修正程式及 WebSphere Application Server 修正套件經常更新的 Installation Manager 儲存庫。您可以使用 `/home/virtuser/installService.sh` Script 來套用這些修正程式及修正套件。Script 必須以 root 使用者身分執行。

取決於您安裝的更新項目類型，安裝更新項目所需的磁碟空間量會不同。在虛擬機器上，僅安裝臨時修正程式需要 1 GB 的可用空間。安裝修正套件則將所需磁碟空間增加到 1.3 GB。

執行 Script 會執行下列動作：

* 停止所有執行中的 WebSphere Application Server 及 IBM HTTP Server 實例
* （選用）安裝 Installation Manager、WebSphere Application Server、IBM HTTP Server 及 Java&trade; SDK 的最新修正套件
* 安裝 WebSphere、IBM HTTP Server 及 Java&trade; SDK 的最新臨時修正程式
* 重新啟動所有實例

#### 選項
* **`-fixpacks`**

    將所有套件更新至最新的修正套件。
* **`-noprompt`**

    更新之前，不提示確認。

#### 語法範例

```
./installService.sh -?
```
{:.codeblock}

顯示說明文字。


```
./installService.sh
```
{:.codeblock}

安裝所有適用的臨時修正程式，但無修正套件。


```
./installService.sh -fixpacks
```
{:.codeblock}

安裝所有可用的修正套件，然後安裝所有適用的臨時修正程式。

### 使用 Installation Manager 更新
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} 安裝在 `/home/virtuser/IBM/Installation Manager` 目錄中，而且可以直接執行以套用修正程式及修正套件。

**避免麻煩：**因為是以 `virtuser`（有限管理虛擬使用者）身分安裝基礎二進位檔，所以請確保一律以 `virtuser` 身分執行 Installation Manager。

## 將系統更新項目套用至虛擬機器
{:#vm-system-updates}

在虛擬機器上套用系統更新項目類似於更新實體 Red Hat Enterprise Linux&reg; (RHEL) 系統。使用 Yum 套件管理程式，即可安裝、更新、解除安裝以及管理套件。WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 系統配置為接收來自 IBM Red Hat Satellite Server 的更新項目，而該伺服器從 Red Hat 網路提供安全的套件。Satellite Server 由 IBM 管理，且無法從您的系統修改。

如需相關資訊，請參閱 [Applying package updates on Red Hat Enterprise Linux 6](https://access.redhat.com/articles/11258#rhel6){: new_window} 及 [Yum](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}（Red Hat 套件管理程式）。
