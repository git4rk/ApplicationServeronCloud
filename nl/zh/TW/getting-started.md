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


# 入門指導教學
{:#getting-started}

使用 {{site.data.keyword.appserver_full}}，您可以在幾分鐘內設定預先配置的 WebSphere Application Server 傳統或 Liberty 環境。本入門指導教學將引導您只使用幾個步驟即可在虛擬機器上佈建 WebSphere Application Server 環境。
{: shortdesc}

## 在開始之前
{: #prereqs}

如果您要環境具有更多專用虛擬機器資源（例如保留合約或「單一承租戶環境」），則需要先與 IBM 銷售人員聯絡，再建立服務。若要進一步瞭解這些選項，請參閱[關於](index.html)。

## 步驟 1：建立服務
{: #create}

1. 移至「{{site.data.keyword.cloud_notm}} 型錄」中的 [{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) 頁面。
1. 使用 IBM ID 登入，或註冊 {{site.data.keyword.cloud_notm}} 帳戶。
1. 在型錄頁面上，檢閱服務配置的選取項目。

  針對隨收隨付制環境，使用預設選項，或修改它們以符合您的需求。如果您有保留合約或「單一承租戶環境」，請特別注意下列選項。

  * **保留合約：**在**選擇要在其中部署的地區/位置**下，驗證選取的地區為合約的正確地區。

  * **單一承租戶環境：**在**選擇要在其中部署的地區/位置**下，驗證選取的地區為部署「單一承租戶環境」的地區。在**環境**下，選取「單一承租戶環境」。依預設，可能會顯示公用環境。

    如果未列出「單一承租戶環境」，請確認您位於正確的地區，而且組織可以存取「單一承租戶環境」。
    {: tip}
1. 選取您要部署之 {{site.data.keyword.appserver_short}} 版本的定價方案。
1. 按一下**建立**。


## 步驟 2：選擇環境
{: #choose_env}

{{site.data.keyword.appserver_short}} Base 及 Liberty Core 方案只有單一伺服器，因此，如果您選擇這些方案，則可以跳過此步驟。

針對 Network Deployment 方案，請選擇環境的設定檔及架構。

* **設定檔：**選擇 {{site.data.keyword.appserver_short}} 傳統或 Liberty
* **架構：**選擇單一伺服器環境或具有傳統 Cell 或 Liberty 群體的叢集環境


## 步驟 3：調整虛擬機器大小
{: #vm_sizing}

您可以針對環境中的每一個元件，個別地調整虛擬機器的大小。虛擬機器大小是以資源區塊的 [T 恤尺碼](index.html#vm-size)來分割。

請按一下元件的標籤（例如伺服器、部署管理程式或應用程式節點），並為其虛擬機器選取 T 恤尺碼。

## 步驟 4：佈建環境
{: #service_profile}

請檢閱服務配置摘要中的詳細資料（包括佈建所需的估計時間）。按一下**佈建**來設定 {{site.data.keyword.appserver_short}} 環境。

## 後續步驟
{: #anchor_value}

在[系統存取](systemAccess.html)中瞭解如何存取及管理新的 {{site.data.keyword.appserver_short}} 環境。
