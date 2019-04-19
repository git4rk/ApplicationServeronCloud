---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-14"

keywords: overview, websphere, liberty, version, cell, collective, vm, virtual machine, t-shirt, block, price, reserve contract

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 關於
{: #about}

{{site.data.keyword.appserver_full}} 可協助您在 {{site.data.keyword.Bluemix_notm}} 管理雲端環境的預先配置 WebSphere Application Server Liberty、傳統 Network Deployment 或傳統 WebSphere Java EE 實例上快速設定。
{: shortdesc}

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 概觀
{: #overview}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 提供消費者預先配置的傳統 WebSphere 及 Liberty 伺服器。它在具有來賓作業系統之 root 存取權的虛擬機器訪客上進行管理。當您建立服務時，可選擇 _Liberty_、_傳統 ND_ 或_傳統 WebSphere_。

**附註：**當您建立任何 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 實例時，消費者現在可以選擇現行修正套件層次或往前一個舊版本[（n 或 n-1）](/docs/services/ApplicationServeronCloud?topic=wasaas-updating-your-environment#maintenance-strategy){: new_window}。

您會有熟悉的 WebSphere 管理經驗，以及具有基礎作業系統的完整存取權。您可以重複使用現有 Script，並進行需要的少量系統調整，以便搭配您自己或協力廠商的架構來使用。「管理中心」及「管理主控台」的提供目的是管理 WebSphere Application Server Liberty、ND 或傳統服務（就像內部部署 WebSphere 配置一樣）。

「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 方案」包含具有兩部以上虛擬機器的 WebSphere Application Server Network Deployment Cell 環境。第一部虛擬機器包含「部署管理程式」和 IBM HTTP Server，而其餘虛擬機器包含與「部署管理程式」聯合的自訂節點（節點代理程式）。使用現有 wsadmin Script 來建立 WebSphere 配置，或使用「WebSphere 管理主控台」來手動配置環境。這些新的功能容許使用者設定叢集環境，這對於任何中介軟體企業應用程式而言都是關鍵的一環。用戶端現在可以選擇對拓蹼進行叢集處理，以針對兩個以上實例的要求進行負載平衡。

「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 方案」也包括使用 Liberty 群體。Liberty 群體是一組 Liberty 設定檔（伺服器）的管理網域，其中包含兩部以上的虛擬機器。第一部虛擬機器包含群體控制器 Liberty 伺服器（即 Liberty 群體的控制點）。除了 Liberty 群體之外，此虛擬機器也包含 IBM HTTP Server，其容許從 Web 瀏覽器存取應用程式。其餘虛擬機器是群體成員所在的群體主機（Liberty Profile 伺服器）。在 Liberty 控制器伺服器上也會啟用「Liberty 管理中心」特性。

下圖顯示 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment Cell 及 Liberty 群體環境的架構。

圖 1. Network Deployment Cell 及 Liberty Collective 的架構

![圖 1. Network Deployment Cell 及 Liberty 群體的架構](images/CellCollectiveDiagram.gif)

**附註**：在上面的_圖 1_ 中，敘述 Deployment Manager 或群體控制器與 IBM HTTP Server 並置的型樣，是針對開發與測試用途。WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 也讓您能自由地重新配置預先安裝的軟體，以符合您的正式作業應用程式和操作需要，就像內部部署一樣。此外，如有最嚴格的正式作業需求，請與您的 IBM 業務代表聯絡，他可以為您介紹我們的單一承租戶 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 供應項目，提供隔離的網路與運算資源。


## 作業環境
{: #operational_environment}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服務會在共用環境中傳回訪客（虛擬機器），讓消費者部署應用程式。VPN 會保護公用服務抵禦通用埠掃描及其他自發網路型攻擊。不過，請一定要注意，您用來存取服務實例的服務 VPN
可能會在多個 {{site.data.keyword.Bluemix_notm}} 組織與使用者之間共用。虛擬機器也會提供運算、記憶體及 I/O 資源，這些來自 IaaS 資源的共用儲存區。

由於在共用環境中，運算、記憶體及 I/O 資源是由虛擬機器執行，因此服務配置可能會不同。透過 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服務儀表板及入口網站，可以檢視每個特定服務實例的配置。

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 提供虛擬機器實例。藉由這些實例，用戶端可使用簡單入口網站，以一致且可重複的方式建立並管理企業 WebSphere Application Server 部署，並極其靈活地調整其應用程式。使用者可在管理雲端環境中的預先配置 WebSphere Application Server Liberty、ND 或傳統虛擬機器上開始進行。使用者可將現有 WebSphere Application Server 應用程式移轉到 {{site.data.keyword.Bluemix_notm}}，並完全控制基礎作業系統及中介軟體。

## 虛擬機器大小調整
{: #vm-size}

IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 提供依 T 恤尺碼分級，因此您可以佈建較大型的虛擬機器，來合理調整使用大量記憶體之應用程式的環境大小。您可以根據預期的資源需求，個別調整您佈建以執行 WebSphere Application Server 的每一部虛擬機器。

虛擬機器的大小及計價是以*區塊* 為單位。針對每一個依 T 恤尺碼的區塊，都會使用下列資源佈建虛擬機器。
* 1 個虛擬 CPU (vCPU)
* 2 GB RAM
* 12.5 GB 的硬碟空間（單一區塊 VM 為 12.0 GB）


| T 恤    | 區塊   | vCPU |RAM (GB) | HD (GB) |
|:-------:|:------:|:----------:|:--------------:|:-------------:|
|S|1|1|2|12|
|M|2|2|4|25|
|L|4|4|8|50|
|XL|8|8|16|100|
|XXL|16|16|32|200|
{: caption="表 1. 每個 T 恤大小的區塊" caption-side="top"}

每一部伺服器或每一個節點都會佈建在單一虛擬機器中。例如，在 Network Deployment 方案中，如果您為部署管理程式佈建一個 M 虛擬機器（2 個區塊）並為應用程式節點佈建 8 個 S 虛擬機器（1 個區塊），則總共會向您收取 10 個區塊的費用。

## 計費選項
{: #billing-options}

每一個區塊的定價取決於您選擇的計費選項：
* **[隨收隨付制](#pay-as-you-go)：**用量型計費，以每個使用區塊的時數計價
* **[保留合約](#reserve-contract)：**保留資源的按月預付訂閱

### 隨收隨付制
{: #pay-as-you-go}

如果您佈建 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 服務，但未與 IBM 銷售人員聯絡，取得替代計費選項，則會套用隨收隨付制定價。用量會以按月計費期間使用之每一個區塊的完整或部分小時計費。計費下限設定為區塊小時的 1/4。

**附註**：由於特定數量的計算、記憶體及 I/O 資源，已停止的實例會被收取每小時區塊費率減價 5% 的費用。在服務內，已停止的實例限制為 10 個 IP 位址或 64 GB 的記憶體。

#### 方案定價

每個區塊的價格會根據您選擇的 WebSphere Application Server 方案而不同。

下表列出每一個依 T 恤尺碼之虛擬機器的每小時總價格。這些價格呈現截至 2016 年 4 月 1 日的 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 方案，並以美元 (USD) 為單位列出。查看您地區中現行價格的型錄。

| T 恤    | 區塊   | Liberty Core | WAS Base | WAS ND |
|:-------:|:------:|:----------:|:------:|:----------:|
|S|1|$0.21|$0.30|$0.70|
|M|2|$0.42|$0.60|$1.40|
|L|4|$0.84|$1.20|$2.80|
|XL|8|$1.68|$2.40|$5.60|
|XXL|16|$3.36|$4.80|$11.20|
{: caption="表 2. Liberty Core 方案" caption-side="top"}


### 保留合約
{:#reserve-contract}

透過保留合約計費，您可以購買每月預付訂閱，以保證存取實際保留可計算資源區塊。這些服務區塊會擱置供您專用，因此不能視為任何其他 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 使用者的可用容量。如果您有現有的 WebSphere Application Server 授權，可以選擇自帶授權保留合約，這樣會使用這些授權，並且會享有折價的計費費率。若要設定保留合約計費，請[與 IBM 銷售人員聯絡](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。

訂閱是以 8 區塊的增量提供。總區塊小時數是根據該月份的小時數，但您可以在整個月的任何時間點使用區塊小時。例如，30 天的月份有 720 個小時，並在乘上 8 區塊的訂閱時產生共 5,760 個區塊小時。

  ```
30 天 * 每天 24 小時 * 8 個區塊 = 5,760 個區塊小時
  ```

您可以修改使用區塊以符合變動工作負載需求的方式及時機，例如使用 4 個區塊、增加為 12 個區塊，然後減少為 8 個區塊。只要您保持低於該月份的總區塊小時數，就不會有任何額外費用。

在您佈建每個環境時，可以選擇要使用保留合約區塊，還是使用隨收隨付制計費。

**附註：**如果您刪除服務實例，可能必須等待大約 30 分鐘，讓它的區塊可供新的服務實例使用。

#### 超額

如果您的用量超出訂閱中的每月區塊小時，則會根據隨收隨付制計費模型收取超額的費用，因此只會向您收取所使用之額外區塊小時的費用。區塊用量的測量基礎是完整或部分小時，而用量下限是區塊小時數 1/4。

隨收隨付制模型的區塊不是保留容量，並且來自共用資源儲存區。

#### 彈性使用的比例分配費率

保留合約計費中的區塊是根據 WebSphere Application Server Network Deployment 方案，但您也可以使用其他方案的區塊。使用其他方案時，會按比例分配用量，因此，會以方案的比例分配費率減少一個區塊小時，而反映在您剩餘的保留合約區塊小時。

下表顯示在計算比例分配之後每一個方案的比例分配費率及每個實際區塊的有效價格。對於地區中的現行價格，請[與 IBM 銷售人員聯絡](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。

| 方案 |比例分配費率| 比例分配後的價格/小時      |
|:-------:|:------:|:------:|
| WebSphere Application Server Liberty Core | 0.3 |$0.21|
| WebSphere Application Server Base  | 0.43 |$0.30|
| WebSphere Application Server Network Deployment | 1.0 |$0.70|
{: caption="表 3：依方案的區塊小時比例分配費率" caption-side="top"}

例如，您可能具有執行 51 小時的 M（2 個區塊）WebSphere Application Server Base 實例。若要計算保留合約中使用的區塊小時，請將實際區塊小時乘上比例分配費率，共有 43.86 個區塊小時：

```
2 個區塊 * 51 小時 * 0.43 比例分配 = 43.86 按比例分配的區塊小時
```

總成本保持不變，但您可以對按比例分配的方案使用較多實際區塊小時，因為它們會從保留合約區塊小時扣除較少。
{:.tip}
