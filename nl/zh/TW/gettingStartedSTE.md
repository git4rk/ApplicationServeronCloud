---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 單一承租戶環境
{: #getting_startedSTE}

「{{site.data.keyword.appserver_full}}：單一承租戶環境」是一種供應項目，可為客戶提供隔離的 WebSphere 工作負載、完全整合的混合式環境及安全資料。本入門手冊的設計旨在識別重要元素，以協助用戶端存取及管理其「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶環境」。
{: shortdesc}


## 建議的軟體
{: #recommended_software}

您需要下列軟體，才能存取「單一承租戶環境」：
* {{site.data.keyword.Bluemix_notm}} 支援的 Web 瀏覽器：
    * Chrome：您作業系統的最新版本
    * Firefox：作業系統的最新版本或最新 ESR 版本
    * Internet Explorer：第 10 版或第 11 版
    * Safari：Mac 的最新版本
* Cloud Foundry 指令行介面 6.5.1 版或更新版本（您可以使用最新版本）
* Git Bash（建議）
    * 下載並安裝 [Git Bash](https://git-scm.com/downloads){: new_window}


## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶環境概觀
{: #overviewSTE}

「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶」供應項目為消費者提供了消費者自己的專用服務實例、專用網路及隔離資源。雖然供應項目是以獨立的方式管理，但可以透過特定 {{site.data.keyword.Bluemix_notm}} 公用地區來存取服務及建立的服務實例儀表板，如下圖所示：

圖 1.「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶環境」的架構

![圖 1. 單一承租戶環境的架構](images/WASaaS.png)


## 組織管理
{: #organization_management}

「WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}：單一承租戶環境」是根據您的訂單所配置。如果您在訂單中提供了一個以上的 {{site.data.keyword.Bluemix_notm}} 組織名稱，便可以立即開始存取環境。如果您未提供一個以上的組織名稱，或想要變更此設定，請從地區的 {{site.data.keyword.Bluemix_notm}} 主控台中開立**應用程式服務**的[支援問題單](reportingIssues.html#reporting_issues)。組織名稱 (ORG) 位於 {{site.data.keyword.Bluemix_notm}} 主控台的右上角，如下圖所示：

圖 2. 組織名稱的位置

![圖 2. ORG 名稱的位置](images/myORG.png)


**附註：**若要存取「單一承租戶環境」，請參閱[單一承租戶環境存取](singleTenantAccess.html#singleTenantEnvironment)。
