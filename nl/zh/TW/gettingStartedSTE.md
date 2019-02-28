---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 單一承租戶環境
{: #getting_startedSTE}

{{site.data.keyword.appserver_full}} Single Tenant Environment 可為客戶提供隔離的 WebSphere 工作負載、完全整合的混合式環境及安全資料。本入門手冊的設計旨在識別重要元素，以協助您存取及管理單一承租戶環境。
{: shortdesc}

## 訂購單一承租戶環境
{:#ordering}

單一承租戶環境無法透過 {{site.data.keyword.Bluemix_notm}} 型錄建立，且必須與 IBM 銷售人員聯絡才能訂購。當您訂購環境時，可以從標準或自帶授權的單一承租戶環境選擇。標準單一承租戶環境包含所有必要的基礎架構及 WebSphere Application Server 授權。在自帶授權的單一承租戶環境中，您可以使用個別的 WebSphere Application Server 授權。

若要訂購單一承租戶環境，請[與 IBM 銷售人員聯絡](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales)。銷售團隊可以協助您設定針對您的需要量身訂做的環境。

## WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment 概觀
{: #overviewSTE}

Single Tenant Environment 供應項目為您提供了自己的專用服務實例、專用網路及隔離資源。雖然供應項目是以獨立的方式管理，但可以透過特定 {{site.data.keyword.Bluemix_notm}} 公用地區來存取服務及建立的服務實例儀表板，如下圖所示。

圖 1. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment 的架構

![圖 1. 單一承租戶環境的架構](images/WASaaS.png)


## 組織管理
{: #organization_management}

WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment 是根據您的訂單所配置。如果您在訂單中提供了一個以上的 {{site.data.keyword.Bluemix_notm}} 組織名稱，便可以立即開始存取環境。如果您未提供組織名稱，或想要變更此設定，請從地區的 {{site.data.keyword.Bluemix_notm}} 主控台中開立**應用程式服務**的[支援問題單](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#reporting_issues)。要在 {{site.data.keyword.Bluemix_notm}} 主控台找到您的組織名稱，請移至**管理 > 帳戶 > Cloud Foundry 組織**。

**附註：**若要存取「單一承租戶環境」，請參閱[單一承租戶環境存取](/docs/services/ApplicationServeronCloud?topic=wasaas-singleTenantEnvironment#singleTenantEnvironment)。
