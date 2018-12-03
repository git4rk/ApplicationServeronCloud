---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 最新更新項目
{: #latest_updates}

服務最新更新項目的清單。

## 2018 年 10 月 24 日：自帶授權計費現在可用於保留合約及單一承租戶環境

如果您有現有的 WebSphere Application Server 授權，您現在可以在保留合約或單一承租戶環境中使用這些授權。使用自帶授權計費的環境，所提供的權益與標準保留合約或單一承租戶環境相同，但是以折價的費率計費。若要使用自帶授權，請[與 IBM 銷售人員聯絡](reportingIssues.html#contacting-sales)。

## 2018 年 8 月 22 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 當您佈建新的服務實例後，傳統 WebSphere Application Server 的 8.5.5.14 修正套件版本現在可供使用。除了 8.5.5.14 之外，傳統 WebSphere Application Server 的其他修正套件（例如 9.0.0.8、9.0.0.7 及 8.5.5.13）也可用於佈建。
* 整合式細項服務維護。

## 2018 年 7 月 16 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 當您佈建新的服務實例後，傳統 WebSphere Application Server 的 9.0.0.8 修正套件版本現在可供使用。除了 9.0.0.8 之外，傳統 WebSphere Application Server 的其他修正套件版本（例如 9.0.0.7、8.5.5.13 及 8.5.5.12）也可用於佈建。
* 當您佈建新的服務實例後，WebSphere Application Server Liberty 的 18.0.0.2 修正套件版本現在可供使用。除了 18.0.0.2 之外，WebSphere Application Server Liberty 的 18.0.0.1 修正套件版本也可用於佈建。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=ibm10717691){: new_window}。
* 已解決 IBM SDK Java Technology Edition 中會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 運行的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=ibm10718297){: new_window}。

## 2018 年 6 月 13 日：保留合約計費現在可供使用

透過保留合約計費，您可以購買按月預付訂閱，以保證存取實際保留可計算資源區塊。這些服務區塊會擱置供您專用，因此不能視為任何其他 {{site.data.keyword.appserver_full}} 使用者的可用容量。您可以利用所選擇的方式來使用整個月的服務區塊小時，並根據一般隨收隨付制訂閱模型向您收取任何超額的費用。

若要進一步瞭解保留合約計費，請參閱[計費選項](index.html#billing-options)。

## 2018 年 3 月 30 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 當您佈建新的服務實例後，傳統 WebSphere Application Server 的 9.0.0.7 修正套件版本現在可供使用。除了 9.0.0.7 之外，傳統 WebSphere Application Server 的其他修正套件版本（例如 9.0.0.6、8.5.5.13 及 8.5.5.12）也可用於佈建。
* 當您佈建新的服務實例後，WebSphere Application Server Liberty 的 18.0.0.1 修正套件版本現在可供使用。除了 18.0.0.1 之外，WebSphere Application Server Liberty 的 17.0.0.4 修正套件版本也可用於佈建。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞]( http://www.ibm.com/support/docview.wss?uid=swg22010172){: new_window}，包括：
  * IBM® Java SDK 中的多個漏洞
  * IBM WebSphere Application Server 針對「管理主控台」提供之安全可能不如預期的漏洞。
  * 使用「表單登入」的 IBM WebSphere Application Server 安裝可能容許遠端攻擊者處理盜用攻擊的漏洞。
  * IBM WebSphere Application Server 可能容許本端攻擊者取得機密性資訊的漏洞，這是不當處理應用程式要求所導致，進而可能容許未獲授權即讀取檔案的存取。
  * 如同在數個產品中所使用，Apache Commons FileUpload 可能容許遠端攻擊者在系統上執行任意碼的漏洞，這是解除序列化 FileUpload 程式庫之 DiskFileItem 類別中的未授信資料所導致。遠端攻擊者可能會惡意探索此漏洞，以在現行處理程序的環境定義下執行任意碼。
  * Intel Haswell Xeon、AMD PRO 及 ARM Cortex A57 CPU 可能容許本端已鑑別攻擊者取得機密性資訊的漏洞，這是 CPU 推測分支指令執行特性中的界限檢查略過所導致。透過處理已設定目標的快取側通道攻擊，攻擊者可能會惡意探索此漏洞，以跨越 syscall 界限並從 CPU 虛擬記憶體中讀取資料。
* 整合式細項服務維護。

## 2018 年 1 月 8 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 當您佈建新的服務實例後，傳統 WebSphere Application Server 的 9.0.0.6 修正套件版本現在可供使用。除了 9.0.0.6 之外，傳統 WebSphere Application Server 的其他修正套件版本（例如 9.0.0.5、8.5.5.12 及 8.5.5.11）也可用於佈建。
* 當您佈建新的服務實例後，WebSphere Application Server Liberty 的 17.0.0.4 修正套件版本現在可供使用。除了 17.0.0.4 之外，WebSphere Application Server Liberty 的 17.0.0.3 修正套件版本也可用於佈建。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22013153){: new_window}，包括：
  * OpenSAML 可能容許遠端已鑑別攻擊者取得機密性資訊的漏洞，這是剖析 XML 實體時的錯誤所導致。
  * Apache HTTP Server 可能容許遠端攻擊者取得機密性資訊的漏洞，這是 HTTP OPTIONS 方法中的缺失（又稱為 Optionsbleed）所導致。
  * Apache Portable Runtime Utility (APR-util) 容易遭到拒絕服務攻擊的漏洞，這是無法驗證 apr_sdbm*() 函數所使用之 SDBM 資料庫檔案的完整性而導致。
* 整合式細項服務維護。

## 2017 年 12 月 21 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已在達拉斯、倫敦及雪梨新增「WebSphere Application Server in IBM Cloud 移轉特性」。此特性提供從現有第 7 版、第 8 版或 8.5.5 版內部部署環境到 IBM Cloud 中第 9 版環境的完整端對端移轉。如需相關資訊，請參閱 [WebSphere Configuration Migration Tool for IBM Cloud](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud)。
* 整合式細項服務維護。

## 2017 年 10 月 27 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 新增了透過「{{site.data.keyword.Bluemix_notm}} 服務儀表板」中的「服務設定檔」標籤或透過 REST API 來佈建較舊的修正套件層次 [(n-1)](maintenanceAndUpdates.html#maintenance-strategy){: new_window} 的能力。
* 當您佈建新的服務實例後，傳統 WebSphere Application Server 的 9.0.0.5 修正套件版本現在可供使用。除了 9.0.0.5 之外，傳統 WebSphere Application Server 的其他修正套件版本（例如 9.0.0.4、8.5.5.12 及 8.5.5.11）也可用於佈建。
* 當您佈建新的服務實例後，WebSphere Application Server Liberty 的 17.0.0.3 修正套件版本現在可供使用。除了 17.0.0.3 之外，WebSphere Application Server Liberty 的 17.0.0.2 修正套件版本也可用於佈建。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22010172){: new_window}，包括：
  * IBM WebSphere Application Server 可能會使用預設許可權，而非使用自訂啟動 Script 時的自訂許可權來建立檔案的漏洞。
  * 「IBM WebSphere Application Server Proxy 伺服器」或「隨需應變路由器 (ODR)」可能容許本端攻擊者取得機密性資訊的漏洞，這是快取後提供舊資料所導致。
  * IBM WebSphere Application Server 容易遭到跨網站 Script 攻擊的漏洞。此漏洞容許使用者在 Web 使用者介面中內嵌任意 JavaScript 程式碼，因此可能會變更想要的功能，而導致在授信階段作業內揭露認證。
  * IBM WebSphere Application Server 在您使用「管理主控台」更新 Web 服務安全連結設定之後，所提供的安全可能不如預期的漏洞。
  * IBM WebSphere Application Server 9.0.0.4 版在您使用 PasswordUtil 指令啟用 AES 密碼加密之後，所提供的安全可能不如預期的漏洞。
  * Apache MyFaces 可能容許遠端攻擊者取得機密性資訊的漏洞。
  * IBM WebSphere Application Server 可能容許遠端攻擊者取得機密性資訊的漏洞，這是 JSF 中 MyFaces 不當錯誤處理所導致。
* 整合式細項服務維護。

## 2017 年 8 月 30 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。

## 2017 年 6 月 30 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，修正套件 8.5.5.12 或 9.0.0.4 會與新的傳統 WebSphere Application Server 實例一起安裝。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，修正套件 17.0.0.2 會與新的 WebSphere Application Server Liberty（Core 及 ND 方案）實例一起安裝。
* 已新增[進階 VPN 配置管理](networkEnvironment.html#advancedVPN){: new_window}特性，您可以用來在倫敦及雪梨地區建立及管理多個 VPN 配置。
* 已新增[公用網際網路存取](networkEnvironment.html#publicInternetAccess){: new_window}特性的加強功能，容許用戶端更妥善管理其公用 IP 位址。
* 已解決 IBM SDK Java Technology Edition 中會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 運行的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22002169){: new_window}，包括：
  * Java SE AWT 元件的未指定漏洞，可能容許未經鑑別的攻擊者控制系統。
  * Java SE JCE 元件的未指定漏洞，可能容許未經鑑別的攻擊者控制系統。
  * Java SE JAXP 元件的未指定漏洞，可能容許未經鑑別的攻擊者造成拒絕服務，使用不明的攻擊向量而導致高可用性影響。
  * 「Java SE 網路」元件的未指定漏洞，可能容許未經鑑別的攻擊者導致低機密性影響、低完整性影響，且沒有可用性影響。
  * 「Java SE 網路」元件的未指定漏洞，可能容許未經鑑別的攻擊者導致無機密性影響、低完整性影響，且沒有可用性影響。
  * 「Java SE 安全」元件的未指定漏洞，可能容許未經鑑別的攻擊者導致無機密性影響、低完整性影響，且沒有可用性影響。
  * 處理 XML 資料時發生 XML External Entity Injection (XXE) 錯誤的漏洞。遠端攻擊者可能會惡意探索此漏洞，以公開高機密性資訊或耗用記憶體資源。
  * zlib 容易遭到拒絕服務攻擊的問題，這是 inftrees.c 中的超出界限指標算術所導致。
  * zlib 容易遭到拒絕服務攻擊的問題，這是負數的未定義左移所導致。
  * zlib 容易遭到拒絕服務攻擊的問題，這是大序排列法超出界限指標所導致。

## 2017 年 5 月 25 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。
* 已新增[進階 VPN 配置管理](networkEnvironment.html#advancedVPN){: new_window}特性，您可以用來在法蘭克福地區建立及管理多個 VPN 配置。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此 JDK 8 會與所有新的服務實例一起安裝。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22004264){: new_window}，包括：
  * 「WebSphere Application Server MQ JCA 資源」配接器的潛在安全漏洞。
  * Libraries 元件的未指定漏洞，可能容許遠端攻擊者取得機密性資訊，使用不明的攻擊向量而導致高機密性影響。

## 2017 年 4 月 21 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg22000834){: new_window}，包括：
  * 已配置「OpenID Connect (OIDC) 信任關聯攔截程式 (TAI)」的 WebSphere Application Server 可能容許使用者在系統上獲得較高專用權的漏洞。
  * WebSphere Application Server 所提供的安全可能不如預期的漏洞。遠端攻擊者可能會惡意探索此弱點來取得機密性資訊，並且取得管理主控台的未獲授權存取。
  * WebSphere Application Server 容易遭到偽造跨網站要求攻擊的問題，因而可能容許攻擊者執行來自網站所信任之使用者所傳輸的惡意且未獲授權的動作。


## 2017 年 3 月 15 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，修正套件 8.5.5.11 或 9.0.0.3 會與新的傳統 WebSphere Application Server 實例一起安裝。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=swg22000587){: new_window}，包括：
  * Libraries 元件的未指定漏洞，沒有機密性影響、高完整性影響，且沒有可用性影響。
  * Libraries 元件的未指定漏洞，可能容許遠端攻擊者取得機密性資訊，使用不明的攻擊向量而導致高機密性影響。
  * Libraries 元件的未指定漏洞，容許遠端攻擊者造成拒絕服務，使用不明的攻擊向量而導致低可用性影響。
  * OpenSSL 中的漏洞，容許遠端攻擊者取得機密性資訊，這是 DES/3DES 密碼錯誤所導致，用於 SSL/TLS 通訊協定中。
  * 容許使用者在 Web 使用者介面中內嵌任意 JavaScript 程式碼，因此可能會變更想要的功能而導致在授信階段作業內揭露認證的漏洞。
  * Apache HTTPD 到 HTTP 回應分割攻擊中的漏洞，因不正確地驗證使用者所提供的輸入所造成。
  * Samba 中的漏洞，容許遠端已鑑別攻擊者取得系統的較高專用權，因處理 PAC 總和檢查失敗所造成。
  * Samba 中的漏洞，容許遠端已鑑別攻擊者取得系統的較高專用權，因在使用 Kerberos 鑑別時將「授與通行證的通行證 (TGT)」轉遞給其他服務所造成。
  * Samba 中資料堆型緩衝區溢位的漏洞，因 ndr_pull_dnsp_name() 函數中的整數覆蓋缺失所造成。


## 2017 年 2 月 10 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，修正套件 8.5.5.11 或 9.0.0.2 會與新的傳統 WebSphere Application Server 實例一起安裝。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，修正套件 16.0.0.4 會與新的 WebSphere Application Server Liberty（Core 及 ND 方案）實例一起安裝。
* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=swg21997657){: new_window}，包括：
  * 拒絕服務漏洞，因容許來自未授信來源的序列化物件執行並導致資源耗用所造成。
  * 使用形態異常的 SOAP 要求，容許遠端攻擊者取得機密性資訊。


## 2016 年 12 月 16 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 整合式細項服務維護。
* 已解決 IBM SDK Java Technology Edition 中會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 運行的[數個安全漏洞](https://www-01.ibm.com/support/docview.wss?uid=swg21995995){: new_window}，包括：
  * Oracle Java SE 及 Java SE Embedded 中與 Hotspot 元件相關的未指定漏洞，具有高機密性影響、高完整性影響，及高可用性影響。
  * Oracle Java SE 及 Java SE Embedded 中與 Networking 元件相關的未指定漏洞，容許遠端攻擊者取得機密性資訊，使用不明的攻擊向量而導致高機密性影響。
  *  IBM WebSphere Application Server 中的跨網站 Scripting 漏洞，容許使用者在 Web 使用者介面中內嵌任意 JavaScript 程式碼。程式碼可能會變更想要的功能，而導致在授信階段作業內揭露認證。


## 2016 年 11 月 8 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已新增功能，讓客戶為其 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VM 要求[公用 IP](networkEnvironment.html#networkEnvironment) 位址
* 已解決會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21993842){: new_window}，包括：
  * IBM WebSphere Application Server 中的漏洞，可能容許遠端攻擊者從不受信任的來源使用序列化物件執行任意 Java 程式碼。
  * 由 TS_OBJ_print_bio 函數中的超出界限讀取所造成的拒絕服務漏洞。遠端攻擊者可能使用特別精心製作的時間戳記檔案惡意探索此漏洞，導致應用程式當機。
  * OpenSSL 的潛在漏洞，可能容許遠端攻擊者取得機密性資訊，這是 64 位元區塊密碼上的三重 DES 演算法錯誤所導致，用於 SSL/TLS 通訊協定中。透過擷取 SSL/TLS 伺服器與用戶端之間的大量已加密資料流量，可以進行中間人攻擊的遠端攻擊者，可能會惡意探索漏洞，以回復純文字資料及取得機密性資訊。該漏洞即所謂的 SWEET32 生日攻擊。
  * OpenSSL 很容易遭到拒絕服務的攻擊。藉由反覆要求重新協議，通過鑑別的遠端攻擊者可能會傳送超大的 OCSP 狀態要求延伸以耗用所有可用的記憶體資源。
  * OpenSSL 很容易遭到拒絕服務的攻擊，這是由於 MDC2_Update 函數的整數溢位所導致。藉由使用不明攻擊向量，遠端攻擊者可能會惡意探索此漏洞，以觸發超出界限寫入，導致應用程式當機。
  * OpenSSL 的潛在漏洞，容許遠端攻擊者取得機密性資訊，這是 DSA 實作錯誤所導致，它容許針對某些作業遵循非持續不變的時間 codepath。攻擊者可能會使用快取時序 (cache-timing) 攻擊惡意探索此漏洞，以回復私密 DSA 金鑰。
  * OpenSSL 很容易遭到拒絕服務的攻擊，這是由於剖析憑證時遺漏訊息長度檢查所導致。通過鑑別的遠端攻擊者可能會惡意探索此漏洞，以觸發超出界限讀取，導致拒絕服務。

## 2016 年 9 月 19 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，新的 WebSphere Application Server Liberty（Core 及 ND 方案）實例都會使用修正套件 16.0.0.3。
* 已解決會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21990236){: new_window}，包括：
  * IBM WebSphere Application Server 中的漏洞，可能容許遠端攻擊者進行網路釣魚攻擊。
  * IBM WebSphere Application Server 中的漏洞，在 OpenID Connect 用戶端進行跨網站 Scripting。
  * IBM WebSphere Application Server 中的潛在漏洞，可能容許遠端攻擊者取得機密性資訊，這是由於預設錯誤頁面不存在時，不當的異常狀況處理所導致。
  * Apache Tomcat 中的拒絕服務漏洞，這是由於 Apache Commons FileUpload 元件的錯誤所導致。
  * IBM WebSphere Application Server 和 IBM WebSphere Application Server Liberty 中的漏洞，可能容許遠端攻擊者取得機密性資訊，這是由於特定情況下的回應處理不當所導致。
  * 網路元件的未指定漏洞，它沒有機密性影響、低完整性影響，且沒有可用性。

## 2016 年 8 月 17 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已將 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 從 8.5.5.9 升級到 8.5.5.10。
* 已解決會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21988710){: new_window}，包括：
  * 影響 WebSphere Application Server 及「WebSphere Application Server Hypervisor Edition 管理主控台」的 Apache Struts 漏洞。
  * 使用 SIP 服務時的 IBM WebSphere Application Server 的潛在拒絕服務漏洞。
  * 可能會影響 WebSphere Application Server 所使用 IBM HTTP Server 的數個漏洞。
  * 容許重新導向 CGI 應用程式的 HTTP 資料傳輸流量的漏洞，而 CGI 應用程式可能會影響 IBM HTTP Server (IHS)。此漏洞稱為 "HTTPOXY"。
  * IBM WebSphere Application Server 中的「資訊揭露漏洞」。
  * IBM WebSphere Application Server 中僅發生在已啟用 Web 容器自訂內容 `HttpSessionIdReuse` 的環境中的潛在略過安全限制漏洞。


## 2016 年 6 月 24 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 新增的功能可讓客戶在建立新的_傳統 ND_ 或_傳統 WebSphere_ 實例時，選擇 8.5 版或 9.0 版。
* 已升級 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}，因此，新的 WebSphere Application Server Liberty（Core 及 ND 方案）實例都會使用修正套件 16.0.0.2。16.0.0.2 是 8.5.5.9 之後的下一個修正套件。從 16.0.0.2 開始，預設會安裝為這些方案支援的所有授權 Liberty 選購特性。
* 已解決會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 的[數個安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21984977){: new_window}，包括：
  * Apache Standard Taglibs 中的 XML External Entity Injection (XXE) 漏洞，會影響 IBM WebSphere Application Server。
  * 使用 WebSphere Application Server Liberty Profile API Discovery 功能和 Swagger 文件時，安全可能不如預期。
  * IBM WebSphere Application Server Liberty 的「管理中心」可能有資訊揭露的漏洞。
  * IBM WebSphere Application Server 中可能有 HTTP 回應分割的漏洞。
  * OpenSSL Project 於 2016 年 5 月 3 日揭露的 OpenSSL 漏洞。

## 2016 年 6 月 13 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 新增了透過建立使用 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} RESTful API 的應用程式或 Script，讓客戶建置、佈建、管理及刪除虛擬機器實例的能力。
* 已新增功能，讓客戶有固定數目的已停止實例，且不超過 10 個 IP 位址或 64 GB 的記憶體。客戶現在會針對已停止狀態的累計實例被收取減價 5% 的費用。

## 2016 年 4 月 26 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已解決 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 中，啟用 FIPS 140-2 時的[潛在安全漏洞](http://www-01.ibm.com/support/docview.wss?uid=swg21982128){: new_window}，以及 Samba 中的數項漏洞 - 包括 Badlock。
* 整合式細項服務維護。

## 2016 年 4 月 15 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}

* 已將 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 從 8.5.5.8 升級到 8.5.5.9。
* 解決了 {{site.data.keyword.Bluemix_notm}} 的 Liberty for Java 中，影響使用 OpenID Connect (OIDC) 用戶端之消費者的[跨網站 Script 編制](http://www-01.ibm.com/support/docview.wss?uid=swg21981221){: new_window}漏洞。
* 整合式細項服務維護。

## 2016 年 2 月 19 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 為應用程式佔用大量記憶體的用戶端新增了一個選項，以套用更大型的虛擬機器來合理調整其環境的大小。用戶端可以選取具有特定資源大小、且最多包含 32 GB RAM 虛擬機器的給定 WebSphere Application Server 元件或單一系統。
* 已將 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 從 8.5.5.7 升級到 8.5.5.8。
* 已解決 IBM SDK Java Technology Edition 中會影響 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 運行的多個漏洞，通常將其稱為 [SLOTH](http://www-01.ibm.com/support/docview.wss?uid=swg21977244){: new_window}。
* 解決了影響消費者使用 OAuth 提供者輸出的[跨網站 Script 編制](http://www-01.ibm.com/support/docview.wss?uid=swg21976337){: new_window}漏洞。
* 整合式細項服務維護。

## 2015 年 12 月 11 日：已更新 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 已將正式產品名稱從 IBM Application Server on Cloud in {{site.data.keyword.Bluemix_notm}} 變更為 IBM WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
* 已新增 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Network Deployment 方案的新功能。此方案包含具有兩個以上虛擬機器的 WebSphere Application Server Network Deployment Cell 環境。這些新的功能容許使用者設定叢集環境以獲得高可用性、失效接手及可擴充性。
* 已新增 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Liberty Core 方案的新功能。此方案包括如何使用 Liberty Collective，而這是一組 Liberty 設定檔（伺服器）的管理網域，並且包含兩個以上的虛擬機器。
* 已將 WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} 從 8.5.5.6 升級到 8.5.5.7。
* 已解決處理 Java 物件解除序列化的 [Apache Commons Collections 漏洞](https://www.us-cert.gov/ncas/current-activity/2015/11/13/Apache-Commons-Collections-Java-Library-Vulnerability){: new_window}。
* 已解決可容許 [HTTP 回應分割攻擊](http://www-01.ibm.com/support/docview.wss?uid=swg21972254){: new_window}的漏洞。
* 整合式細項服務維護。

## 2015 年 10 月 15 日：已更新 Application Server on Cloud
* 新增下列兩個新方案：
  * [WebSphere Application Server 傳統版第 9 版測試版](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/websphere.shtml){: new_window}
  * WebSphere Application Server ND
* 細項服務維護
