---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 單一承租戶環境存取
{: #singleTenantEnvironment}


下列步驟討論如何存取「單一承租戶環境」，以及建立服務實例的方法。
{: shortdesc}


## 存取單一承租戶環境
{: #accessSTE}

1. 在瀏覽器中，移至 [{{site.data.keyword.cloud_notm}} 型錄](https://console.bluemix.net/catalog/){: new_window}。

2. 按一下**登入**，然後使用您的 IBM ID 登入。

6. 在「型錄」搜尋過濾器中，輸入 **WebSphere Application Server**。

    ![替代文字](images/filter.png "搜尋過濾器")

7. 在**應用程式服務**下，按一下 **WebSphere Application Server** 磚。

    ![替代文字](images/iconWAS.png "WebSphere Application Server 磚")

8. 在**環境**功能表中，選取單一承租戶環境。

    ![替代文字](images/environmentSTE.png "單一承租戶環境名稱")

    **避免麻煩：**公用環境可能會顯示為預設值。顯示正確的環境名稱，會假設您登入正確的地區，以及容許存取「單一承租戶環境」的組織成員。

    **附註：**如果您選取其中一個公用環境，則可能會產生每小時費用。因此，如果您看不到「單一承租戶環境」名稱，則請開立「支援問題單」（如[取得客戶支援](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window}頁面所定義）。

9. 選取適當的方案，然後按一下**建立**。

    ![替代文字](images/createSTE.png "選擇方案並建立服務")


**附註：**每小時定價不適用於「單一承租戶環境」。「單一承租戶環境」包括稱為配額的固定**區塊**數目。小型環境包含 64 個區塊。中型包含 128 個區塊，而大型包含 256 個區塊。

**區塊**定義如下：
  * 1 個 vCPU
  * 12.5 GB 的磁碟[1]
  * 2 GB RAM

[1] *技術上而言，小型系統只包含 12 GB 的磁碟。中型系統包含 25 GB 的磁碟，而大型包含 50 GB，依此類推。*

對於您建立的每一部虛擬機器，指定您想要的 T 恤尺碼：S、M、L、XL 或 XXL，其對應於 1、2、4、8 及 16 個區塊。當您選取 T 恤尺碼時，會從配額中減少對應的區塊數目。

例如，假設您有一個包含 64 個區塊的小型環境。在此環境內，您所配置的服務實例針對共 60 個已使用區塊包含兩個 XXL、三個 XL 及一個 L。如果您針對新的 Liberty Core 訂閱選取中型 T 恤尺碼，則可能會顯示一則訊息，指出您仍然可用的配額及區塊數目：

> **此服務的「單一承租戶」記憶體配額為 64 個區塊。包括您的現行配置，您還剩下 2 個區塊。若要增加記憶體配額，請聯絡「IBM 銷售人員」。**


## 專用網路環境
{: #private_network}

佈建「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶環境」之後，您可以下載 VPN 認證，並建立 OpenVPN 連線。如需相關資訊，請參閱下列鏈結：

* [VPN 存取](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#vpnAccess){: new_window}
* [設定 OpenVPN](https://console.bluemix.net/docs/services/ApplicationServeronCloud/systemAccess.html#setup_openvpn){: new_window}

## 管理單一承租戶環境
{: #manageSTE}

若要在現有「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶環境」中新增額外容量，或若要在另一個資料中心內訂購容量，請聯絡「美國電話客服中心」、當地 IBM 業務代表或「IBM 事業夥伴」。若要知道您的業務代表或夥伴，請致電 800-426-4968。如需相關資訊，請聯絡「美國電話客服中心」。電話：800-IBM-CALL (426-2255) 傳真：800-2IBM-FAX (242-6329)。


## 支援單一承租戶環境
{: #supportingSTE}

如果您遇到問題，請開立「支援問題單」（如[取得客戶支援](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window}頁面所定義）來取得協助。
