---
title: AEM 6.2 Cumulative Fix Pack
description: Experience Manager 6.2 Cumulative Fix Pack 版本注意事項。深入了解 Experience Manager 元件中各類 Cumulative Fix Pack 所修復的問題。
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: 894a2a98b9d1a135a2f488f2167ec3302c122339
workflow-type: tm+mt
source-wordcount: '19975'
ht-degree: 100%

---

# AEM 6.2 Cumulative Fix Pack 發行說明{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## 發行資訊 {#release-information}

| **產品** | Adobe Experience Manager |
|---|---|
| **版本** | 6.2 |
| **發行** | [Cumulative Fix Pack 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **必備條件** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **正式發行** | 2019 年 6 月 6 日 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe 針對發行修正推出單一交付模式。Adobe 現在改採每個月發行一個 Cumulative Fix Pack (CFP) 的方式 (可能因通過品質檢查的情況而異)，而非針對個別問題發行 Hotfix。CFP 是多個修正的彙總式內容套件。CFP 主要包含錯誤修正，但也可能包含 Feature Pack。比起發行個別 Hotfix，這種方式的優點如下：

* 本質上為累積性質 (例如 CFP 包含透過先前版本 CFP 提供的修正)
* 提高品質保證
* 簡化安裝程序 (使用者以無相依性的單一套件安裝 CFP 即可，但最新版 Service Pack 除外)

如需更多有關 CFP 和其他發行版本的相關資訊，請參閱[維護版本工具](https://docs.adobe.com/content/docs/zh-Hant/aem/6-2/deploy/maintenance-release-vehicle-definitions.html)。

## 關於發行版本 {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 為重要更新，是 AEM 6.2 的最後一個 Cumulative Fix Pack，包含自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式發行以來累積的重要客戶修正。

>[!CAUTION]
>
>如果未確認與已安裝的 Feature Pack 之間的相容性就套用 CFP，可能會導致系統失敗或遺失自訂設定，上述情況可能需要從備份復原才能解決。

>[!NOTE]
>
>* AEM Cumulative Fix Pack 6.2 SP1-CFP10 隨附新的 Sling `discovery-  api` 套件組合 Johnzon 1.0.0。此外，在 CRX 存放庫中為 */var/discovery* 節點新增了服務使用者 sling-discovery，其具有讀取和寫入權限。
   >
   >
* 新增 Apache Commons **org.apache.commons/commons-email/1.5** 的電子郵件套件組合，取代了 **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**。
   >
   >
* Adobe 建議針對 AEM 執行個體上有大量使用者的客戶，透過安裝資料夾來部署 CFP。

>



## 包括的問題 {#issues-included}

本節列出此版 CFP 中所包含的所有問題和 Hotfix。

此外，此版 CFP 也包含[先前版本 Cumulative Fix Pack](#previous) 提供的 Hotfix。

### 整合 {#integration}

* 反向移植多個 Campaign 目標定位個人化改善項目。NPR-29163：CQ-4264126 的 Hotfix
* com.day.cq.personalization.impl.TeaserResourceEventHandler 進入無限迴圈，並造成發佈執行個體上的節點更新。NPR-28561：CQ-4263096 的 Hotfix

### DAM - 一般 {#dam-general}

* 無法在特定 dam 資料夾中顯示/隱藏非管理員使用者的複製按鈕。NPR-29026：CQ-4265361 的 Hotfix

### 漏洞 {#vulnerability}

* CSRF 保護架構對 AEM Foundation 表單無效。NPR-28612：GRANITE-22231 的 Hotfix

### 表單 {#forms}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package}

>[!NOTE]
>
>針對 AEM Forms 客戶，必須先安裝任何 AEM Service Pack、Cumulative Fix Pack 或 Feature Pack，才能安裝 AEM Forms 附加套件。

>[!NOTE]
>
>AEM Forms 附加元件套件用於協助讓表單功能與 AEM Service Pack 和 Cumulative Fix Pack 一致。因此，必須先安裝任何 AEM Service Pack、Cumulative Fix Pack 或 Feature Pack，才能安裝 AEM Forms 附加套件。

#### 調適型表單 {#adaptive-forms}

* iOS 12.1 裝置上的手寫元件可用性問題。NPR- 29082：CQ-4261765 的 Hotfix

#### Forms - 文件安全性 {#forms-document-security}

* 使用 PDF 進階電子簽名 (PAdES) 驗證的 PDF 中，所有簽名都會擲回 InvalidOperationException。NPR-27848：CQ-4244837 的 Hotfix

#### Forms - 通信{#forms-correspondence}

* 以 PDF 預覽信函時，置於主版頁面的文字欄位沒有遵循從資料索引標籤輸入的值或資料連結指定的值。NPR-29239：CQ-4266856 的 Hotfix。

#### Forms -互動式通訊 {#forms-interactive-communication}

* 新增縮寫符號字元時，信函中預填的欄位會顯示為 ASCII 字元，而非一般字母。NPR-28863：CQ-4262900 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer}

* Forms JEE 安裝程式中沒有新的 AEM Forms 修正。

## 先前版本 Cumulative Fix Pack 中包含的 Hotfix 和 Feature Pack{#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 為重要更新，包含自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 為 AEM 6.2 啟用對 MS Translator API v3.0 的支援
* 成功安裝所有 SP、CFP 和 HF 的套件後，會新增記錄訊息。

### 資產 {#assets}

* 如果缺少「編輯 ACL」權限，則無法為 DAM 資料夾重新命名。NPR-27555：CQ-104652 的 Hotfix
* 6.2.1 CFP 17 及更新版本中的影像預設集編輯器工具沒有回應。NPR-28147：CQ-4261041 的 Hotfix

### 網站 {#sites}

* 連結檢查程式沒有完成工作，且因沒有回應的連結而卡住。NPR-27373：CQ-4256030 的 Hotfix
* 因為一個額外的根路徑中斷了區段的路徑，導致區段檔案無法正確載入。NPR-28014：CQ-4260332 的 Hotfix

### 整合 {#integration-1}

* LiveCopy 繼承取消無法在目標容器上正常運作。NPR-28129：CQ-4259813 的 Hotfix
* 系統沒有針對目標元件考慮 cq:actions。NPR-27616：CQ-4257497 的 Hotfix

* 用於中斷繼承的圖示顯示不一致。NPR-27671：CQ-4257779 的 Hotfix

### Felix {#felix}

* 在 AEM 6.2 SP1 執行個體上安裝 CFP 18 後，Web 控制台元件詳細資訊會因 500 錯誤而失敗。NPR-28350：CQ-4261095 的 Hotfix

### 轉換 {#translation}

* MS Translator 升級為 API v3.0 後，AEM 6.3 啟用了對 MS Translator 服務的支援。NPR-28123：CQ-4259096 的 Hotfix

### UI - Foundation {#ui-foundation}

* OOTB 網站日曆顯示不正確的日期。NPR-28392

### Granite {#granite}

* 使用 sling:basename 的資源套件組合不會使字典失效。NPR-27624

### 維持 {#sustenance}

* 套件管理器活動記錄應擷取至獨立的記錄檔中。NPR-27323：Granite-14866 的 Hotfix
* 安裝完成時，會在 error.log 中顯示的標準化詞句/用語/記錄行。NPR-27835
* Granite 套件外掛程式會選擇依存於較低版本的 org.apache.sling.i18n。CQ-4263245 的 Hotfix
* 在 6.2SP1-CFP15 之後安裝最新 CFP 時，會刪除 com.adobe.cq.com.adobe.cq.ui.commons 套件組合。CQ-4258808 的 Hotfix

### 表單 {#forms-1}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-1}

#### 調適型表單 {#adaptive-forms-1}

* AEM 表單出現 XML 插入漏洞。NPR-27843：CQ-4257315 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer-1}

* Forms JEE 安裝程式中沒有新的 AEM Forms 修正。

### 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included}

下列文字記錄 CFP 中包含的 OSGI 套件組合和內容套件清單。

AEM 6.2 SP1-CFP19 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/cfp19_osgi_bundles.txt)

AEM 6.2SP1-CFP19 中包含的內容套件清單

[取得檔案](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 為重要更新，包含自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 新增 DAM CommandLineProcess 支援，用於終止長時間執行的程式。
* 修正 ReplicationEventListener 中的工作階段洩漏問題。
* 新增對核心頁面元件的重新導向支援。

### 資產 {#assets-1}

* 進行大量擷取期間 Camera RAW 處理程序會卡住，最終封鎖所有工作流程處理。NPR-26990：NPR-23860 的 Hotfix
* 下載功能會透過 assetdownload servlet 運用 AEM Assets 讓匿名使用者下載所有資產。NPR-27054、CQ-4254732 的 Hotfix
* AEM 的電子郵件範本主旨行裡的特殊字元看起來不完整。NPR-26470：CQ-4252368 的 Hotfix

### 網站 {#sites-1}

* 由於 ConfigPostProcessor 類別的行為不正確，暫停上層映像時會將子頁面中的 cq:LiveRelationship 混合類型移除。NPR-26745：CQ-4254163 的 Hotfix
* 新增對核心頁面元件的重新導向支援。NPR-26576：CQ-110529 的 Hotfix
* 將 ContextHub 遷移至 jquery 3。NPR-26956：CQ-4255472 的 Hotfix
* 錨點輸入欄位會出現在對話方塊上的瀏覽器可見區段中，直到最大化為止。NPR-26852：CQ-4255019 的 Hotfix
* 複製貼上文字時會在內容片段中插入不需要的 &lt;br>。NPR-26660：CRTE-151 的 Hotfix
* 傳統網站管理員不會針對某些頁面在右窗格中轉譯清單。NPR-27247：CQ-4251621 的 Hotfix
* (傳統 UI) 嘗試移動/重新命名頁面時，會產生「移動頁面時發生錯誤」錯誤。NPR-27179：CQ-4235907 的 Hotfix

### 整合 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever 遊走整個樹狀結構以收集可用的品牌。NPR-27060：CQ-4255790 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components}

* Foundation 清單元件的搜尋功能問題。NPR-26817：CQ-4250324 的 Hotfix

### 平台 {#platform}

* 由於特殊字元長破折號，Publisher 在排清快取時發生問題。NPR-27199：CQ-4242790 的 Hotfix

### Granite {#granite-1}

* 套件驗證器沒有驗證 CFP/SP 中包含的套件。NPR-26775：Granite-22825 的 Hotfix

### 複寫 {#replication}

* ReplicationListener 中發生 JCR 工作階段洩漏。NPR-27063：CQ-4232088 的 Hotfix

### 表單 {#forms-2}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-2}

* Forms 附加套件中沒有新的 AEM Forms 修正。

### Forms JEE 安裝程式 {#forms-jee-installer-2}

* Forms JEE 安裝程式中沒有新的 AEM Forms 修正。

#### 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-1}

AEM 6.2 SP1-CFP18 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/62cfp18updated_bundles.txt)

AEM 6.2 SP1-CFP18 中包含的內容套件清單

[取得檔案](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 為重要更新，包含自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 新增對 at-integration.js 中無網站延伸模組 URL 的支援
* 從 S7 雲端服務設定中移除 S7 輪詢匯入工具。
* 變更受眾檢視以支援多租用戶使用者實作的資料夾結構。
* 更新至 jqueryui clientlib v1.12.1。

### 資產 {#assets-2}

* 若要從資產 UI 啟動工作流程，使用者必須擁有寫入/刪除/修改權限。NPR-25688：CQ-4250140 的 Hotfix
* 即使是沒有「複寫」權限的使用者，也可看到發佈和取消發佈按鈕。NPR-25094
* (工作流程) 智慧型標記資產工作流程不會透過 AEM Proxy 設定處理。NPR-25915：CQ-4248202 的 Hotfix
* 從 S7 雲端服務設定中移除 S7 輪詢匯入工具。NPR-25239：CQ-95236 的 Hotfix

### 網站 {#sites-2}

* 從「編輯器 -> 頁面資訊」啟動的工作流程會在裝載中包含內容路徑。NPR-26389：CQ-76804 的 Hotfix
* (外部連結檢查器) 無效的 https 連結會顯示為有效的連結。NPR-25541：CQ-4201333 的 Hotfix
* (傳統 UI) 在 Live Copy 下建立獨立頁面時，頁面會建立為 Live Copy。NPR-25610：CQ-4249801 的 Hotfix
* 啟動頁面時，與 Design Importer 元件相關聯的發佈資源發生問題。NPR-25638：CQ-102532 的 Hotfix
* RTE Rich Text 文字工具列覆蓋選取清單。NPR-25165：CQ-4248948 的 Hotfix
* 將 ContextHub 遷移至 jquery 3。NPR-25059：Granite-19902 的 Hotfix
* 針對巢狀的 parsys 元件，一律從多個可用元件中套用滿足設計的第一個元件 (最短巢狀路徑)。如需詳細資訊，請參閱[設計路徑解析](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html)。NPR-25250：CQ-4246276 的 Hotfix

### 整合 {#integration-3}

* 若使用 OOTB 目標整合，將元件設為目標時會轉譯整個頁面，而非空的目標元件。NPR-25273：CQ-4248003 的 Hotfix
* 在目標定位模式中，中斷繼承仍會顯示元件為已定位，而在編輯模式中繼承沒有中斷。NPR-25324：CQ-4248162 的 Hotfix
* 已在頁面上定義個人化項目且已解析受眾時，對應的體驗會以編輯模式顯示。NPR-25731：CQ-4249465 的 Hotfix
* 使用 AEM 搭配非預設的內容路徑時，會出現錯誤的宣傳預告 URL。NPR-25971：CQ-4250953 的 Hotfix
* 使用輸出時產生空白轉譯。NPR-25295：CQ-4246792 的 Hotfix
* 頁面啟動時，從製作環境刪除的體驗都不會從發佈網站中移除。NPR-24869：CQ-4247832 的 Hotfix

### DAM - DM 用戶端{#dam-dm-client}

* (Chrome、Firefox) VideoPlayer 會忽略支援觸控功能的裝置上的滑鼠點按。CQ-4247370 的 Hotfix

### 平台 {#platform-1}

* 允許設定取得/釋出套件的重試次數上限。NPR-25328：Granite-22376 的 Hotfix
* 發生覆寫錯誤時未正確記錄。NPR-25308：CQ-4249402 的 Hotfix
* 將 Forms AEM 6.2 Forms CFP8 安裝至 CFP14 會導致 Apache POI 失敗。NPR-25053：Granite-21771 的 Hotfix

### Granite {#granite-2}

* 使用者同步程序失敗，出現 OakConstraint0022 例外狀況。NPR-25729：Oak-7428 的 Hotfix

### 社群 {#communities}

* cq-social-as-provider 套件組合的開頭不是 mongo 驅動程式 3.x 版。NPR-26271：CQ-4252710 的 Hotfix

### UI - Foundation {#ui-foundation-1}

* 更新至 jqueryui clientlib v1.12.1。NPR-25090：Granite-21981、CQ-4248897 的 Hotfix

* (Omnisearch)：「Title」屬性容易遭受網站中的跨網站指令碼 (XSS) 攻擊。NPR-24994：Granite-19933 的 Hotfix

### 表單 {#forms-3}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-3}

#### 調適型表單 {#adaptive-forms-2}

* 從調適型表單提交資料時編碼錯誤。NPR-25539

#### 表單 - 管理{#forms-management}

* 發佈頁面時，不相關的表單資產會報告為參考。NPR-26167：CQ-4251004 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-3}

#### 文件安全性 {#document-security}

* 變數會填入為「清單」資料類型，子類型為字串，但會收到「無法強制轉型物件」錯誤。NPR-26194：CQ-4252287 的 Hotfix
* 安裝 6.2-SP1-CFP15 後，無法存取浮水印設定。NPR-26130：CQ-4250984 的 Hotfix

### 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-2}

AEM 6.2 SP1-CFP17 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/62cfp17updated_bundles.txt)

AEM 6.2SP1-CFP17 中包含的內容套件清單

[取得檔案](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 為重要更新，包含自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* Day CQ Mail Service 新增 STARTTLS 支援。
* 修正設定檔彈出視窗中 ContextHub 圖示的對齊方式。
* 下拉式元件會顯示/隱藏功能的修正。
* 升級至最新的 Jackson 2.8.11 版

### 資產 {#assets-3}

* 無法從清單檢視起始工作流程。NPR-24393：CQ-4245788 的 Hotfix
* (Firefox/Chrome) 無法下載「資產共用」頁面中的資產。NPR-24523：CQ-4224408 的 Hotfix
* 提高 AEM 中視訊預覽的預設畫質。NPR-24148：CQ-4244310 的 Hotfix

### 整合 {#integration-4}

* 在發佈執行個體上將元件設為目標時，顯示目標元件之前的預設體驗時會出現閃爍畫面。NPR-23992：CQ-4242038 的 Hotfix
* 頁面啟動時，從製作環境刪除的體驗都不會從發佈網站中移除。NPR-24869：CQ-4247832 的 Hotfix

### 平台 {#platform-2}

* 修補 clientlib 中 jQuery 1.12.4 以包含安全性修正。NPR-24129：Granite-20058 的 Hotfix
* Day CQ Mail Service 新增 STARTTLS 支援。NPR-23941：CQ-4240397 的 Hotfix
* 刪除預設的 MERGE_PRESERVE aclHandling。NPR-24593：Granite-21889 的 Hotfix
* 請求中包含無效的查詢參數時，LineChecker 無法將連結外部化。NPR-24127：CQ-4241893 的 Hotfix

### MSM {#msm}

* 針對跨網站指令碼攻擊 (XSS) 的主動式 Hotfix。NPR-21893：CQ-4223385 的 Hotfix
* MSM LiveRelationship：如果 BlueprintConfig 位於根，則有效 RolloutConfig 會有錯誤。NPR-23999：CQ-4243000 的 Hotfix

### 網站 {#sites-3}

* 在 Live Copy 區域中建立新體驗時，必須中斷繼承才能進行設定。NPR-24995、CQ-4248209 的 Hotfix
* (觸控式 UI) 鎖定或解除鎖定頁面時，頂端工具列上的數個圖示會消失。NPR-23954：CQ-4243345 的 Hotfix
* ContextHub 中的欄位未正確對齊。NPR-23958
* 鎖定的頁面上的發佈動作會中斷製作。NPR-23970：CQ-4243203 的 Hotfix
* /etc/reports/ 中的 OOTB 報表無法正常運作，且沒有顯示歷史資料圖表。NPR-20035：CQ-4220180 的 Hotfix
* 在專案上起始「請求啟動」工作流程時，建立啟動會失敗。NPR-24255：CQ-4245030 的 Hotfix
* CFP10 安裝後，電子郵件會忽略 HTML 標記和屬性。NPR-24287：CQ-4240028 的 Hotfix
* TagPicker：標記中繼資料結構標記欄位中的標記建議會查詢可標記的節點，因此需要花很長的時間載入。NPR-24347：CQ-4244291 的 Hotfix
* Salesforce 整合因 Proxy 設定而失敗。NPR-24418：CQ-4245300 的 Hotfix
* (WCM) 建立修訂期間出現例外狀況，PageManager 在將頁面維持在簽入狀態。NPR-24565：CQ-4246203 的 Hotfix
* 套用 CFP14 後，「裝置模擬器」按鈕從編輯和預覽模式中消失。NPR-24566：CQ-4247060 的 Hotfix
* (傳統 UI) 在對話方塊中進行製作後，完整的標記會顯示為空白。NPR-24688、CQ-4246407 的 Hotfix
* 無法在第一次嘗試時建立版本。NPR-24774：CQ-4232176 的 Hotfix
* /etc/reports/ 中的 OOTB 報表無法正常運作，且沒有顯示歷史資料圖表。NPR-24138：CQ-4220180 的 Hotfix

### 漏洞 {#vulnerability-1}

* Salesforce 整合容易遭受伺服器端請求偽造 (SSRF) 攻擊。NPR-24289：CQ-4245277 的 Hotfix
* ReportingServicesProxyServlet 中出現伺服器端請求偽造 (SSRF) 漏洞。NPR-24657：CQ-4246880 的 Hotfix

### Granite {#granite-3}

* 中繼資料讀取作業不會終止。NPR-24240：Granite-19866 的 Hotfix
* 將 Jetty 更新為 9.4.11.v20180605 以修正漏洞。NPR-25033：Granite-22120 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components-1}

* 排序頁面時 PageComparator 擲回 ClassCastException。NPR-24123：CQ-4244048 的 Hotfix
* 表單下拉式元件的顯示/隱藏功能未如預期運作。NPR-24562：CQ-4222853 的 Hotfix

### 使用者介面{#user-interface}

* 由於管理搜尋功能中有大量請求，出現高 CPU 使用量問題。NPR-23588：Granite-21286 的 Hotfix
* (傳統 UI) 如果相關的表單資料模型服務設為空白欄位，元件會顯示預設值。NPR-21903：GRANITE-19744 的 Hotfix
* 沒有 FormData 可用於請求時，多欄位會擲出 NPE。NPR-24513：Granite-21055 的 Hotfix

## 表單 {#forms-4}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-4}

#### 核心 {#core}

* (OSGI) AEM Forms OSGI 受到 Jackson 資料繫結安全性警報影響。NPR-24274：CQ-4230245 的 Hotfix

#### 版權管理 {#rights-management}

* 安裝 AEM 6.2 SP1-CFP14 後 Apache POI 失敗。NPR-25054、NPR-25052：CQ-4245898、CQ-4244778 的 Hotfix

#### HTML5 表單 {#html-forms}

* 在 HTML 預覽中預填多行欄位時沒有填入資料。NPR-23357：CQ-4244212 的 Hotfix
* 透過預設預覽來預覽信函時，版面片段對應沒有顯示，而按一下預覽按鈕時，同樣的版面片段對應則會正確顯示。NPR-22993：CQ-4237745 的 Hotfix
* 將社會安全號碼模式套用至範本時，文字欄位的 HTML 預覽出現問題。NPR-23205

#### 調適型表單 {#adaptive-forms-3}

* 將 AEM 表單新增至 parsys 元件時發生「Guidelib 未定義」錯誤。NPR-24269：CQ-4244546 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Shell 指令碼檔案中的視窗行結尾導致 LCM 無法在 UNIX 中執行。NPR-22958

### 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-3}

AEM 6.2 SP1-CFP16 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

AEM 6.2SP1-CFP16 中包含的內容套件清單

[取得檔案](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 為重要更新，包含自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* Foundation 表格中的主動式安全性修復，用於維持設計的一致性。
* 新增對 typeHint 的支援，可將值儲存為字串。
* 為 Forms 預填服務提供增強的安全性
* 更新至最新版 adobe-reader-extensions-dsc.jar 檔案，以取得 Reader 延伸模組中的修正。
* 調整驗證勾點以針對提升數輸入考慮「:invalid」項目。

### 資產 {#assets-4}

* EmbedXMP 資料一律對 Ptiff 產生程序設為「作用中」。NPR-22776：CQ-4234498 的 Hotfix
* 無法在多值欄位中設定多個預設值。NPR-22900：CQ-4239000 的 Hotfix
* (Dynamic Media) 選取「動態轉譯」核取方塊時，下載的 zip 檔案會以零位元組檔案產生原始 TIFF 影像。NPR-22410：CQ-4198471 的 Hotfix
* (觸控式 UI) 欄檢視中資產的預設上傳位置。NPR-23475：CQ-4237057 的 Hotfix

### 整合 {#integration-5}

* 在「目標」模式中，作者不需要取消繼承即可修改從 Blueprint 繼承的元件。NPR-22751：CQ-4237907 的 Hotfix
* 路徑變數未正確編碼，導致非永久性跨網站指令碼 (XSS)。NPR-22851

### MSM {#msm-1}

* 含有多個轉出設定的 LiveCopy 轉出期間，如果根底下出現 ResourceNameConflict，則轉出流程會終止，且不包含所有分支。NPR-22842：CQ-4236188 的 Hotfix

### 平台 {#platform-3}

* 在一個反向應用程式請求中實作輪詢限制。NPR-23351：Granite-21135 的 Hotfix****
* 自訂記錄器沒有反映訊息模式變更。NPR-23486：CQ-4241974 的 Hotfix

### 網站 {#sites-4}

* 在 RTF 編輯器的文字中，無法建立帶有空格或其他特殊字元的文件連結。NPR-22289：CQ-4224321 的 Hotfix
* 以巨大值 (10000000000) 儲存區段時，會將提升值設為 0，進而引發錯誤訊息。NPR-22524：CQ-4237006 的 Hotfix
* 無法在多欄位元件中按一下「新增項目」。NPR-22552：CQ-4237404 的 Hotfix
* 區段具有長標題時看不到水平捲軸。NPR-22615：CQ-4237001 的 Hotfix
* 載入空受眾會產生錯誤的 JavaScript 程式碼。NPR-22974：CQ-4238734 的 Hotfix
* 排程啟動或停用時工作流程標題是強制項目，因此自訂工作流程標題不會在時間軸中翻譯。NPR-23121：CQ-4237552 的 Hotfix
* 請求修正 Sites 中目標區段的相關問題。NPR-23128
* (Firefox) 所選角色的核取方塊不正確。NPR-23345
* 不同模式的標籤隨著圖示一起顯示。NPR-23275
* 將元件從 AEM 6.0 移轉到 AEM 6.2 時，出現「無效的遞迴選擇器值」錯誤。NPR-23503：CQ-4241258 的 Hotfix

### 社群 {#communities-1}

* 由於向群組傳送訊息失敗，系統沒有觸發 Web 和郵件通知。NPR-23447：CQ-4242880 的 Hotfix

### 轉換 {#translation-1}

* 在翻譯設定上將資產設定為「不翻譯」時，系統會建立資產語言副本。NPR-22540：CQ-4237962 的 Hotfix

### 使用者介面{#user-interface-1}

* 搭配連字號查詢使用 Omnisearch 時會傳回伺服器錯誤。NPR-22999：Granite-19674 的 Hotfix
* 日期挑選器不支援手動設定隱藏欄位所設定的外部類型提示。變更類型提示會出現對話錯誤。NPR-23333：Granite-21194 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components-2}

* 為提高安全性，已棄用 CAPTCHA 元件，若您正使用 CAPTCHA 元件，則安裝 6.2 SP2-CFP15 或更新版本後，會顯示「Captcha 元件已棄用且不應再使用。」訊息。為提高安全性，AEM 元件可供自訂以包含 reCAPTCHA NPR-22151：CQ-4220052 的 Hotfix
* WCM Foundation 元件「表格」容易受到儲存型跨網站指令碼攻擊。NPR-23206：CQ-4240760 的 Hotfix

### 漏洞 {#vulnerability-2}

* 管理員 UI 專案連結中有跨網站指令碼 (XSS)。NPR-23272：CQ-4241795 的 Hotfix

## 表單 {#forms-5}

### Forms 附加元件套件 {#forms-add-on-package-5}

#### 通信管理 {#correspondence-management}

* 透過預設預覽來預覽信函時，版面片段對應沒有顯示，而按一下預覽按鈕時，同樣的版面片段對應則會正確顯示。NPR-23335：CQ-4237745 的 Hotfix
* 與 XDP 中所定義繫結對應的信函中的資料，不會在使用直接信函 URL 時填入。NPR-24145：CQ-4244290 的 Hotfix

#### 行動表單 {#mobile-forms}

* (通信管理) 使用目標 XML 載入信函時，資料未妥善對齊。NPR-22993：CQ-4237663 的 Hotfix

#### Reader 延伸模組服務 {#reader-extensions-service}

* 無法在 Adobe PDF 上套用 Reader 延伸模組。NPR-23067

#### Forms Manager {#forms-manager}

* 重新發佈網站頁面時，不會發佈內嵌在網站中的表單。NPR-23014：CQ-4236566 的 Hotfix

#### 漏洞 {#vulnerability-3}

* 跨網站指令碼的主動式 Hotfix。NPR-20624：CQ-4206055 的 Hotfix
* Forms Manager 的附註索引標籤中出現儲存型跨網站指令碼 (XSS) 漏洞。NPR-27157：CQ-4255556 的 Hotfix

#### 加密服務 {#encryption-service}

* (OSGI) [JEE]使用「驗證 PDF 程序」來進行驗證時，帶有附件的 PDF 之簽名狀態不正確。NPR-23269、NPR-23737

### Forms JEE 安裝程式 {#forms-jee-installer-5}

#### 核心 {#core-1}

* 應修正 Core-ext 靜態程式碼分析中報告的問題。NPR-13947

#### PDFG 服務 {#pdfg-service}

* HTML 轉 PDF 轉換器無法運作。NPR-21545

### 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-4}

下列文字記錄 CFP 中包含的 OSGI 套件組合和內容套件清單。

AEM 6.2 SP1-CFP15 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6_2cfp15updated_bundles.txt)

AEM 6.2SP1-CFP15 中包含的內容套件清單

[取得檔案](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 改善資產中繼資料屬性的可編輯性。
* 重新設定已處於過期狀態的資產之密碼過期通知工作。
* 自訂觸控式 UI 控制台以延伸其他地區設定。
* 更新 cq-msm-core 以有效進行 Livecopyindex 同步。
* 簡化各種轉出的複寫功能。

### 資產 {#assets-5}

* 使用者無法下載含有免責聲明和檔名很長的資產。NPR-22163：CQ-4235274 的 Hotfix
* 使用快速工具列動作開啟資產的屬性時，單引號字元導致 Bulkview 中的中繼資料無法更新，且 UI 會完全損壞。NPR-22317、NPR-22353：CQ-4236990、CQ-4236469 的 Hotfix
* 資產到期通知工作不會停用過期的資產。NPR-22346：CQ-4237188 的 Hotfix
* 透過 Safari 在 Assets 中使用數位版權管理時，資產下載失敗。NPR-22378：CQ-4236460 的 Hotfix
* 小型影像的 Web 轉譯像素大小不正確。NPR-22435：CQ-4236742 的 Hotfix

### 網站 {#sites-5}

* (觸控式 UI) 移動的標記會顯示在頁面屬性中的新舊位置。NPR-21921、CQ-4238598 的 Hotfix
* (觸控式 UI) RTF 編輯器從 &lt;a> 標記中移除了 ID 以外的所有屬性。NPR-22045：CQ-4234133 的 Hotfix
* 使用 CTRL+V 直接在 RTF 編輯器中貼上內容會略過分行符號。NPR-22117：CUI-5881 的 Hotfix
* (觸控式 UI) 無法在命名空間底下顯示超過 40 個標記。NPR-22290：CQ-99114 的 Hotfix
* RSS 摘要問題，AEM 6.2 的連接埠 -1。NPR-22158：CQ-4233339 的 Hotfix
* (IE) 首次在 RTF 欄位中編寫任何字元時，都會在字元尾端新增一個空格。NPR-22443：CQ-4235343 的 Hotfix
* 嘗試比對套件名稱時，Java Use 物件會因為套件宣告中的尾端空格字元而凍結 SightlyJavaCompilerService。NPR-22557：Granite-20836 的 Hotfix
* 觸控式 UI 控制台不會揀選新的語言以用於標記。NPR-22250：CQ-4239194 的 Hotfix

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) 必須先為對開本設定發佈日期和封面日期欄位，才能上傳至 DPS。NPR-22484

### 商務 {#commerce}

* 商務建立目錄精靈中有多個跨網站指令碼 (XSS) 漏洞。NPR-22344：CQ-4237017 的 Hotfix

### MSM {#msm-2}

* 長時間進行索引更新期間，LiveCopyIndex 同步會導致執行緒擁塞。NPR-22214：CQ-90667 的 Hotfix
* 編輯 LiveCopy 中的其他欄位時會停用 cq:cugEnabled 屬性，因此會導致頁面沒有受到保護。NPR-22246：CQ-4236050 的 Hotfix
* 頁面暫停時，「頁面轉出」動作無法更新子項。NPR-22483：CQ-4236956 的 Hotfix
* 轉出主版中已移動的結構會導致錯誤的 cq:moveTarget。NPR-22373：CQ-4232536 的 Hotfix

### 整合 {#integration-6}

* 嘗試排序選件選擇器程式庫中的選件時，會導致行為不穩定。NPR-22208：CQ-4235439 的 Hotfix
* 長時間執行查詢期間 TargetContentImpl 導致 AEM 變得緩慢。NPR-22361：CQ-4236907 的 Hotfix
* 目標引擎 (mbox.js、at.js) 沒有使用損害 URL 而使用包含冒號的 URL，這可能因為某些部署而失敗。NPR-22366：CQ-4237854 的 Hotfix
* 頁面個人化需要直接在品牌節點上發佈。NPR-22370：CQ-4236895 的 Hotfix

### Foundation {#foundation}

* Apache Sling Scripting Sightly Model 使用提供者套件組合 **org.apache.sling.scripting.sightly.models.provider/1.0.18**。NPR-22614：Sling-5944、Sling-6866 的 Hotfix

### 專案 {#projects}

* 工作流程啟動器無法接受 String 的 TypeHint 值。NPR-22436：CQ-4237855 的 Hotfix

### 轉換 {#translation-2}

* 發現預覽功能出現問題。NPR-22201：CQ-4223753 的 Hotfix

### 使用者介面{#user-interface-2}

* (傳統 UI) 如果相關的表單資料模型服務設為空白欄位，元件會顯示預設值。NPR-21903：GRANITE-19744 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components-3}

* 發佈指向 Adobe Campaigns 中匯入工具頁面的 Live Copy 頁面時發生錯誤。NPR-22470：CQ-4237164 的 Hotfix
* 開啟體驗片段編輯器時發生 JavaScript 錯誤。NPR-22598：CQ-4238415 的 Hotfix

### 工作流程 {#workflow}

* Day CQ 工作流程電子郵件通知服務會針對 WorkflowCompleted 和 WorkflowAborted 通知，對每個 Mongo 節點觸發一封電子郵件。NPR-22486：CQ-4238172 的 Hotfix

## 表單 {#forms-6}

### Forms 附加元件套件 {#forms-add-on-package-6}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

#### 調適型表單 {#adaptive-forms-4}

* IE11 和 Chrome 之間調適型表單中的下拉式清單預留位置值不一致。NPR-22405：CQ-4227096 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer-6}

#### 安裝 LCM {#install-lcm}

* 在安裝程式和 LCM 中將 Jsafe Jar 更新至 Cryptoj 6.1.3.1。NPR-22744

### 包含的 Feature Pack {#feature-packs-included}

#### 處理程序管理 {#process-management}

* (HTML 工作區) 使用者認領任務時，系統會重新整理該特定使用者的佇列計數，但除非重新整理頁面，否則不會為其他使用者重新整理。NPR-19778：CQ-4233665 的 Hotfix

### CFP14 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-cfp}

AEM 6.2 SP1-CFP14 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6_2cfp14updated_bundles.txt)

AEM 6.2SP1-CFP14 中包含的內容套件清單

[取得檔案](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
AEM Cumulative Fix Pack 6.2 SP1-CFP13 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 使用 AT.js 作為用戶端程式庫時，啟用「目標元件設定」中的「靜態參數」欄位設定。
* 下拉式元件會顯示/隱藏功能的修正。
* 修正使用目標同步受眾時的問題。
* 提高「通信管理」的多功能性以容納特殊字元。

### 資產 {#assets-6}

* 版本清除無法移除舊版資產。NPR-21682：CQ-4212996 的 Hotfix
* 在可重新排列的資料夾底下重新排列資料夾無法持續。NPR-21964：CQ-4231761 的 Hotfix

### 網站 {#sites-6}

* (觸控式 UI) (傳統 UI) HTL 和核心元件有多個跨網站指令碼 (XSS) 漏洞。NPR-21532：CQ-4232305 和 CQ-4232511 的 Hotfix
* 在 Internet Explorer 11 中，在選取的文字上建立/格式化內容 (例如指派/移除新的清單樣式) 的功能無法正常運作。NPR-21533：CQ-4230689 的 Hotfix
* (Safari) 使用者無法在資產尋找器面板中檢視所有資產。NPR-21981：CQ-4213720 的 Hotfix
* Time Warp 傳回「RecursionTooDeepException」錯誤並出現亂碼頁面，且即使變更日期，也不會建立新版本。NPR-21707：CQ-4199536 的 Hotfix
* 在編輯器中載入頁面時，WorkflowStatusprovider (pageinfo.json) 會載入三次，導致 AEM 執行個體執行速度緩慢。NPR-21778：CQ-59232 的 Hotfix

### 整合 {#integration-7}

* 無法在 AEM 中以製作目標模式建立「行動類型與瀏覽器」的受眾。NPR-21676、NPR-21681：CQ-4232100 的 Hotfix
* 重新整理目標元件期間延遲較高的情況下，可在元件完全重新整理之前新增另一個選件。NPR-21744：CQ-4233158/CQ-4234293 的 Hotfix
* 使用者無法查看 mbox 呼叫中的測試「靜態參數」值，而透過雲端設定中作為用戶端程式庫的 AT.js 進行測試時可看到這些值。NPR-21930：CQ-4234520 的 Hotfix

### 平台 {#platform-4}

* 使用者或群組數目很多時，使用者同步作業出現效能問題。NPR-20431：CQ-4223282 的 Hotfix
* 使用 Sling Distribution 進行使用者同步時，沒有同步使用者。NPR-21911：Granite-20404 的 Hotfix
* 無法在搜尋摘要中醒目提示停用字詞 (在 Geometrixx 頁面上)。NPR-21835：Granite-21067 的 Hotfix\
   注意：此修正需要 Oak CFP 1.4.20 或更新版本。

### 轉換 {#translation-3}

* 建立翻譯專案時，發起人使用者 ID 缺少 jcr 屬性。NPR-21715：CQ-4230713 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components-4}

* 表單下拉式元件的顯示/隱藏功能未如預期運作。NPR-22164：CQ-4235288 的 Hotfix

## 表單 {#forms-7}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

### Forms 附加元件套件 {#forms-add-on-package-7}

#### 調適型表單 {#adaptive-forms-5}

* 調適型表單中出現 XML 外部實體插入 (XXE)。NPR-21982：CQ-109878 的 Hotfix
* (iOS11) 按一下檔案附件元件時，檔案附件會開啟相機而非裝置檔案瀏覽器。NPR-21926：CQ-4214348 的 Hotfix
* 主題建立 UI 中缺少標題會導致發生例外狀況，而且無法轉譯對話方塊。CQ-4236143 的 Hotfix

#### 通信管理 {#correspondence-management-1}

* 轉譯包含特殊字元的 xml 資料時發生問題。NPR-21712：CQ-4229137 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer-7}

#### 組合器服務 {#assembler-service}

* 使用 6.2.0-ASM-1017-003 產生的 PDF 檔案損毀。NPR-21427：CQ-4228046 的 Hotfix

#### PDFG 服務 {#pdfg-service-1}

* PNG、JPEG 和 TIFF 檔案的未預期頁面大小 (PDF) 導致 OCR 失敗。NPR-19489：CQ-4209079 的 Hotfix

## CFP13 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-cfp-1}

AEM 6.2 SP1-CFP13 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/cfp13_bundlecompare-list.txt)

AEM 6.2SP1-CFP13 中包含的內容套件清單

[取得檔案](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 改善多值欄位的中繼資料處理。
* 支援翻譯工作流程中的多字元 (兩個以上) 國家/地區代碼。
* 改善含有多個巢狀元件的頁面轉譯。
* 改善 AEM 和 Adobe Digital Publishing Suite 之間資產發佈日期的同步處理。

### 資產 {#assets-7}

* OmniSearch 中有過多字元會造成 AEM 伺服器當機。NPR-21083：CQ-4223602 的 Hotfix
* 在中繼資料結構的多值欄位中，第二個選項中指定的值沒有附加至 CRX-de 中先前指定的值。NPR-21220：CQ-4224526 的 Hotfix
* 透過 Safari 在 Assets 中使用數位版權管理時，資產下載失敗。NPR-21387：CQ-4230287 的 Hotfix

### 網站 {#sites-7}

* (DAM) (傳統 UI) AEM CQ 製作/發佈快速入門中，某些 SWF 檔案具有多個跨網站指令碼 (XSS) 漏洞。NPR-21073、NPR-21074：NPR-20612 的 Hotfix
* 標記選取器不翻譯提供多種語言版本的標記。NPR-21221：CQ-78855 的 Hotfix
* AEM 文章控制台出現轉譯問題，使用多個巢狀元件導致其速度變得緩慢。NPR-21271：CQ-4224158 的 Hotfix

### 整合 {#integration-8}

* 新增 Target 架構時，無法在編輯器的「選取模式」清單中使用「目標定位」模式。NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) AEM 中對開本的發佈日期與 Folio Producer 中顯示的日期不一致。NPR-21145

### MSM {#msm-3}

* 刪除 LC 中的第一個本機頁面後，Live Copy 重設程序會停止。NPR-21276：CQ-4229743 的 Hotfix

### 平台 {#platform-5}

* 升級至 AEM 6.3 後，找不到參考標記實作為指令碼的自訂 taglib。NPR-20149：Granite-18433 的 Hotfix

### 轉換 {#translation-4}

* 翻譯工作流程因為 lang_country 代碼長度超過 2 個字元而失敗。NPR-21088：CQ-4197439 的 Hotfix
* 專案完成之前，不應允許將資產頁面重新提交至翻譯專案。NPR-21219：CQ-4209908 的 Hotfix

### 使用者介面{#user-interface-3}

* 提交表單期間，選取元件不會刪除目標屬性。NPR-21163：GRANITE-14125 的 Hotfix
* HTTP.encodePathOfURI 展開時會對加號「+」進行雙重編碼。NPR-21417：GRANITE-16340 的 Hotfix

### 漏洞 {#vulnerability-4}

* DAM 中繼資料編輯器中有跨網站指令碼 (XSS)。NPR-21434：CQ-83472 的 Hotfix
* 多個 SWF 檔案容易受到跨網站指令碼 (XSS) 攻擊。NPR-20612：CQ-4213297 的 Hotfix

## 表單 {#forms-8}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

### Forms 附加元件套件 {#forms-add-on-package-8}

#### 通信管理 {#correspondence-management-2}

* (IE11) HTML 內容的初始轉譯只會在左側進行，而右側會在載入完整 UI 後間歇性載入。NPR-21554
* 安裝 AEM 6.2 SP1-CFP9 後，會停用信函預覽提交按鈕。NPR-21547
* 選取資產連結類型時，「資產選擇器」視窗不會在「編輯信函資料繫結」精靈中開啟。NPR-21164：CQ-4194567 的 Hotfix
* 若要編輯內嵌或可編輯的文字模組，請點一下相關的「編輯」圖示，或在信函預覽中按兩下相關的文字模組。NPR-21402

#### 調適型表單 {#adaptive-forms-6}

* AEM Forms 按鈕元件顯示 type=&quot;button&quot; 而非 type=&quot;submit&quot;。NPR-21007
* 為可重複面板新增或刪除新面板時，資料仍持續存在。NPR-21408

### Forms JEE 安裝程式 {#forms-jee-installer-8}

#### 核心 {#core-2}

* 升級至最新的 Java 8 Update 131 時會擲回例外狀況：「JsafeJCE 提供者已停用，FIPS 140 要求的自我完整性檢查失敗」。NPR-21355

   **請注意：**&#x200B;此 NPR 需要其他設定，如需詳細資訊，請參閱[最新版 Java 8 更新](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr)。

* 在核心、加密、簽名和檔案安全性中，將 jsafe jar 更新為 cryptoj 6.1.3.1。NPR-21360、NPR-21361、NPR-21356、NPR-21358

#### 安裝 LCM {#install-lcm-1}

* 在安裝程式和 LCM 中將 Jsafe Jar 更新至 Cryptoj 6.1.3.1。NPR-21362

#### PDFG 服務 {#pdfg-service-2}

* 在 PDFG 中將 Jsafe Jar 更新至 Cryptoj 6.1.3.1。NPR-21359

#### 處理程序管理 {#process-management-1}

* (HTML 工作區) 啟用欄調整大小功能，讓名稱類別不會顯示為截斷。NPR-19770：CQ-4233668 的 Hotfix

#### Reader 延伸模組服務 {#reader-extensions-service-1}

* 在 RE 中將 Jsafe Jar 更新至 Cryptoj 6.1.3.1。NPR-21357

## CFP12.1 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-cfp-2}

AEM 6.2 SP1-CFP12.1 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

AEM 6.2 SP1-CFP12.1 中包含的內容套件清單

[取得檔案](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 更新 cq-msm-core 以有效進行 Livecopyindex 同步。
* 改善編輯內容片段的效率。
* 在套件管理器中提供用於偵測 ACL 權限的驗證選項。
* 引入 Campaign 的功能以包含用於客戶通信的電子郵件 ID。
* 改善 Dynamic Media 檔案的視訊編碼功能。
* Sightly 元件和 LiveCopy 中的修正。

### 資產 {#assets-8}

* Dynamic Media 視訊編碼無法對名稱中包含空格的檔案進行編碼。NPR-20818：CQ-102469 的 Hotfix
* AEM CQ 製作/發佈快速入門中，某些 SWF 檔案具有多個跨網站指令碼 (XSS) 漏洞。NPR-21071、NPR-21072
* 使用者無法下載含有免責聲明和檔名很長的資產。NPR-20255：CQ-4222139 的 Hotfix

### 網站 {#sites-8}

* AEM 和 Campaign整合：若在 Adobe Campaign 中重寫特殊連結，會導致客戶無法在其電子郵件中傳送 mailto: 超連結。NPR-20787：CQ-4225760 的 Hotfix
* (觸控式 UI) 語言設為法文時，AEM 會出現可用性疑慮和效能問題。NPR-20854：CQ-4227628 的 Hotfix
* 在 RTE 中連結使用了連結外掛程式的編碼資產檔案時，會傳回空白連結。NPR-20626、NPR-21059：CQ-4223011 的 Hotfix
* 內容片段中繼資料編輯器會阻止內容作者儲存內容片段的變更。NPR-20641：CQ-4224755 的 Hotfix
* 頁面屬性別名導致請求發佈/請求取消發佈。NPR-20731：CQ-4226227 的 Hotfix
* 編碼 RTE 元素中的連結時出現文字元件問題。NPR-20755：CQ-4224321 的 Hotfix

### 平台 {#platform-6}

* ResourceResolverImpl.map() 沒有叫用 ResourceDecorator。NPR-20788：GRANITE-19718 的 Hotfix
* org.apache.sling.i18n.DefaultLocaleResolver 無法透過 org.apache.sling.engine.SlingRequestProcessor 處理請求。NPR-20706：CQ-94880 的 Hotfix
* 請求在套件管理器中新增驗證選項，以偵測是否對特定套件變更了任何 ACL 權限。CQ-4229196 的 Hotfix

### 整合 {#integration-9}

* (Search&amp;Promote) 內容套件的不明確篩選條件定義會導致安裝時覆寫路徑。NPR-20808：CQ-4227615 的 Hotfix

### 工作流程 {#workflow-1}

* AEM 生產伺服器部署的穩定性問題。NPR-20979：Granite-19104 的 Hotfix

### 專案 {#projects-1}

* (觸控式 UI) 無法將團隊成員新增至專案。NPR-20990：CQ-4205375 的 Hotfix

### WCM-Foundation 元件 {#wcm-foundation-components-5}

* Sightly 影像元件「link to」會因為缺少 .html 副檔名而產生 403 錯誤。NPR-20823：CQ-4195909 的 Hotfix
* 在使用 LiveCopy 的Blueprint 網站上，嘗試刪除表單元件會擲回 NullPointerException 並新增回該表單元件，而非將其刪除。NPR-20855：CQ-4204628 的 Hotfix
* 長時間進行索引更新期間，LiveCopyIndex 同步會導致執行緒擁塞。NPR-20634：CQ-90667 的 Hotfix

### 安全性 {#security}

* 主動式 XSS 程式庫更新。NPR-21174
* 升級至 Apache Commons Email 1.5，為傳送電子郵件程序提供簡化的 API。NPR-20509：Granite-18240 的 Hotfix
* 套用至 Apache Sling XSS Protection API 的安全性修補程式，可消除 XSS 略過的可能性。NPR-21290：GRANITE-19924 的 Hotfix
* XSSAPI#getValidHref 函數中出現 XSS 略過問題NPR-21174：Granite-19924 的 Hotfix

### 行動應用程式 {#mobile-apps}

* 修正 AEM 中針對 OOTB 資產的 curl Head 請求問題。NPR-20511：CQ-4221520 和 CQ-103024 的 Hotfix

## 表單 {#forms-9}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

AEM Forms 的關鍵重點為：

* 啟用 Workbench 使用者的憑證驗證功能。
* 通信管理、HTML5 表單和 AEM 表單工作區的可用性修正。

### Forms 附加元件套件 {#forms-add-on-package-9}

#### HTML5 表單 {#html-forms-1}

* iOS 10 和 11 裝置上的手寫元件可用性問題。NPR- 21092

#### 通信管理 {#correspondence-management-3}

* (通信 UI) 按一下後停用提交按鈕。NPR-21078

### Forms JEE 安裝程式 {#forms-jee-installer-9}

#### 組合器服務 {#assembler-service-1}

* docConverter 無法產生 PDF/A，並出現「『stEvt:action』元素的首碼『stEvt』未繫結」錯誤。NPR-21032：CQ-4222540 的 Hotfix
* 系統擲回例外狀況並出現名稱 java.lang.IllegalArgumentException 訊息：叫用 OMPFSubmission/PDFA/PDFtoPDFA 服務時無列舉常數 com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE。這會導致在伺服器重新啟動之前無法完成短期簽名驗證處理程序。NPR-20792

#### Workbench {#workbench}

* 為 Workbench 使用者啟用憑證驗證。NPR-17548：CQ-4214486 的 Hotfix

#### 處理程序管理 {#process-management-2}

* 以 dataref 轉譯行動表單時，準備資料處理程序會叫用多次。NPR-19801：CQ-4230427、CQ-4230400 的 Hotfix

## CFP11 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-cfp-3}

AEM 6.2 SP1-CFP11 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

AEM 6.2 SP1-CFP11 中包含的內容套件清單

[取得檔案](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 新增用於測試的 onDialogLoaded 公用程式函數。
* 為 ClientLibraryProxyServlet 新增前端單元測試和設定。
* 多影像就地編輯器元件中的效能修正。
* Apache Sling JCR ResourceBundleProvider 中的設定更新。

### 資產 {#assets-9}

* 如果停用資產更新工作流程，資產預覽會無法運作。NPR-20543：CQ-4204986 的 Hotfix
* Granite 中新增類別的轉譯問題：類別屬性 (cq-damadmin-admin-assets-upload)。NPR-20514：CQ-4219238 的 Hotfix
* 標題中有特殊字元的縮圖資產會在的 alt 屬性中顯示 java 物件 NPR-20347：CQ-4223620 的 Hotfix
* 由於授權問題，以 Adobe 專屬代碼取代了版本比較代碼。NPR-20273：CQ-4223758 的 Hotfix
* 上傳含有多個 Alpha 層的 CMYK PSB 檔案時發生處理問題。NPR-20251：CQ-4220869 的 Hotfix
* 除非伺服器在 in org.apache.sling.i18n 2.5.6 中重新啟動，否則國際化字典無法運作。NPR-20525：Granite 的 Hotfix- 19490
* 沒有根據具有預設執行緒傾印收集器設定 (預設 AEM 啟動) 的排程器週期產生執行緒傾印。NPR-20288：Granite-19488 / GRANITE-12741 / CQ-90647 的 Hotfix。

### 網站 {#sites-9}

* 如果在開啟儲存的搜尋後變更修改日期篩選條件，就不會對結果造成影響，且顯示的結果與修改日期篩選條件先前儲存的值相同。NPR-19739：CQ-4219425 的 Hotfix
* 含有巢狀元件的頁面無法載入。NPR-20312
* 刪除工作流程套件時，會觸發刪除工作流請求。NPR-20266：CQ-4221686 的 Hotfix
* (觸控式 UI) 作業系統剪貼簿和內部 AEM 剪貼簿出現複製/貼上問題。NPR-20228：CQ-4220383 的 Hotfix
* 載入多個資產 (超過100個) 時，清單檢視的 AEM 執行個體會變得緩慢。NPR-20034：CQ-4222695 的 Hotfix
* (觸控式 UI) 透過傳統 UI 控制台刪除啟動會導致所有頁面都無法編輯。NPR-20520：CQ-4225074 的 Hotfix
* Target 下拉式清單無法搭配有多個 RTE 元件的對話方塊運作。NPR-20345：CQ-4220981 的 Hotfix

### 平台 {#platform-7}

* 使用匿名工作階段存取時，ClientLibraryProxyServlet 不會在發佈執行個體上對用戶端程式庫提出 Proxy 請求，且會擲回 HTTP 404 找不到錯誤。NPR-20195：Granite-14409 的 Hotfix

### 整合 {#integration-10}

* 目標引擎選為 Adobe Target 會導致元件無法載入，並在伺服器記錄中擲回錯誤。NPR-20058：CQ-88071、CQ-109698、CQ-4201600 的 Hotfix

### 商務 {#commerce-1}

* 建立相同頁面的產品時，不會顯示確認或重新導向快顯訊息。NPR-20257：CQ-4223414 的 Hotfix

### 使用者介面{#user-interface-4}

* 如果「日期挑選器」是多欄位中的一個欄位，編輯元件時，儲存在日期欄位中的值不會持續存在。NPR-20077：GRANITE-19147 的 Hotfix
* 觸發連續查詢時沒有中止先前的查詢，導致了錯誤的結果。NPR-20397：GRANITE-19306 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components-6}

* 即使從多影像就地編輯器元件中移除影像後，ImageMap 屬性仍然存在。NPR-20142：CQ-4222982 的 Hotfix

## 表單 {#forms-10}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

### Forms 附加元件套件 {#forms-add-on-package-10}

#### 調適型表單 {#adaptive-forms-7}

* 透過 UI 變更時，valueCommit 指令碼會對 DropDownList 執行兩次。NPR-19989：CQ-110212 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer-10}

**處理程序管理**

* CFP 套件包含 AEM Forms HTML 工作區 2.2.26 版。NPR-20099
* 將行動表單設為以 PDF 檢視時，預填的表單無法運作。NPR-20566

**版權管理**

* 「CAC/共同驗證憑證選取對話方塊」應將採用增強金鑰使用方法 (EKU) 的憑證顯示為客戶端驗證或智慧卡登入。NPR-20708
* Forms JEE 支援 PKCS#11 相互驗證。NPR-15001

## CFP10 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-cfp-4}

AEM CFP 6.2 SP1-CFP10 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/bundle-list-cfp10.txt)

AEM CFP 6.2 SP1-CFP10 中包含的內容套件清單

[取得檔案](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 調整 Analytics 傳統 UI 的密碼輸入設定。
* 修正 ContextHub 的獨立持久性快取。
* 精確計算資產維度。
* 將資產發佈至 Brand Portal 時最佳化 AEM 效能。
* 對畫布節點中 Resourcetype 值的修正。
* 針對文件片段內容啟用區分大小寫和特殊字元搜尋功能。
* 增強調適型表單，可在 Safari 中附加 PDF 作為附件。\
   提供新的 Dynamic Media，可連接至新的 Dynamic Media 發佈基礎架構，以達到更快速、擴展性更高的複寫。

### 資產 {#assets-10}

* AEM Assets 無法擷取 InDesign 資產的子資產參考，包括資產的重複連結。NPR-19006：CQ-4204186 的 Hotfix
* 排序選項無法用於「商務」底下集合內的資產。NPR-19508：CQ-4213622 的 Hotfix
* 與現有資產名稱相同的資產移至同樣位置時，資產的 cq:lastReplicationAction 值會在兩者之間交換，進而導致建立錯誤的中繼資料。NPR-19531
* 儘管所有資產都已正確發佈，發佈大量資產時仍會顯示錯誤訊息。NPR-19629：CQ-4219611 的 Hotfix
* 靜態轉譯會以固定維度列出，不會反映實際轉譯的大小。NPR-20004
* 將多個資產 (超過 4 個) 發佈至 Brand Portal 時，AEM 執行個體會變得緩慢。NPR-20009

### 網站 {#sites-10}

* 使用者嘗試發佈/取消發佈/建立其他使用者鎖定的頁面版本時，AEM 會顯示非預期的行為。NPR-19249；CQ-4215298 和 CQ-4203856 的 Hotfix
* 手動提升巢狀啟動時，子頁面會遭到刪除。NPR-19704
* 初始化期間 ContextHub 儲存覆寫預設持久層時，出現持續性問題。NPR-19979：CQ-4218399 的 Hotfix
* 內容片段與其他按鈕重疊。NPR-19980：CQ-4221519 的 Hotfix
* 在網站管理員中使用別名檢視時，不會顯示網站頁面。NPR-20053：CQ-4221478 的 Hotfix
* 發佈指向 Adobe Campaigns 中匯入工具頁面的 Live Copy 頁面時發生錯誤。NPR-20066：CQ-4220846 的 Hotfix

### 平台 {#platform-8}

* 將 Apache POI 升級至 3.16 版，以支援將 PPT 投影片的背景影像包含在轉譯中。NPR-18286
* 在同一個資料夾中上傳多個資產時，Internet Browser 11 和 Edge 出現轉譯問題。NPR-20062

### 整合 {#integration-11}

* 透過匿名使用者存取時，自訂 at.js 檔案不會發佈。NPR-19542：CQ-4219592 的 Hotfix
* 將 Analytics 現有的憑證移轉到 WSSE Authentication。NPR-19962

### 品牌入口網站 {#brand-portal}

* 啟用透過標記管理員/標記控制台將標記從 AEM 發佈至 Brand Portal 的功能。NPR-20271

## 表單 {#forms-11}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

### Forms 附加元件套件 {#forms-add-on-package-11}

#### 通信管理 {#correspondence-management-4}

* 啟用可在預覽信函時搜尋文件片段中實際文字的功能。NPR-19712

#### 調適型表單 {#adaptive-forms-8}

* 增強調適型表單，可在 Safari 中附加 PDF 作為附件。為支援現有表格的相同功能，我們需要變更附件小工具和「支援的檔案類型」中的設定，以更新值 application/pdf 而非 .pdf。NPR-19623

#### Forms管理員{#forms-manager-1}

* 如果沒有在調適型表單欄位上定義 validationState，且發生了 elementFocusChanged 事件，則會傳回錯誤事件 (errorState) 至 Adobe Analytics 伺服器。NPR-19513

### Forms JEE 安裝程式 {#forms-jee-installer-11}

#### 核心 {#core-3}

* 關機期間無法使用連線管理器。Jboss 會在取消部署作者 EAR 之前切斷 JDBC 相依性，進而導致損毀問題。NPR-19703

## 包含的 Feature Pack {#feature-packs-included-1}

* Dynamic Media 中的縮圖修正和透明度改善。NPR-15207

## CFP9 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-cfp-5}

AEM 6.2SP1-CFP9 中更新的內容套件清單

[取得檔案](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

AEM 6.2SP1-CFP9 中更新的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 在 Adobe 電子郵件範本服務中，為自訂使用者範本引入標記。
* 增強桌面應用程式的觸控式 UI 按鈕。
* 按一下即停用提交按鈕，以防止翻譯頁面上出現多個表單提交。
* 在對話方塊中設定了多個 RTE 元件。
* 增強 Live Copy 中的 ReferenceUpdates。
* 針對文件片段內容啟用區分大小寫搜尋功能。
* 將 Linux 程式庫清單新增至 AEM Forms 安裝說明文件中。

### 資產 {#assets-11}

* 在 Safari 瀏覽器上對智慧型集合套用 Omnisearch 篩選器時出現問題。NPR-19511
* 當一個 PDF 資產有多個相關的關鍵字時，系統無法妥善擷取和正確修改 PDF 關鍵字中繼資料。為了解決問題，已移除 PDF 資產的「主旨」欄位中繼資料屬性。但是您可編輯中繼資料結構來為「主旨」欄位新增一個多值文字欄位。NPR-19126
* 工作流程通知服務不會對電子郵件中的連結進行編碼，這會導致使用者按一下連結後無法載入。NPR-19490：CQ-4218055 的 Hotfix
* 無法使用 Chrome 在欄檢視中載入頁面/資產的完整清單。NPR-19458：CQ-4214248 的 Hotfix
* 啟用「請求啟用」工作流程時，AEM 收件匣中會顯示錯誤的「關閉時間」圖示。NPR-19365：CQ-4216174
* 清單檢視出現排序問題。NPR-19217：CQ-95602
* 變更「資產資料夾」設定中的標題或縮圖圖片時，原始群組和資料夾的權限遭覆寫。NPR-19283：CQ-4216080 的 Hotfix
* Windows 10 工作站會自動切換到觸控模式，停用部分按鈕的功能。NPR-19183

### 網站 {#sites-11}

* 對話方塊中有多個 RTE 元件會發生問題。NPR-19311：NPR-19587
* VersionManagerImpl 初始化後，Vanilla AEM 6.2 中的自動版本清除作業只能運作一次。NPR-19315：CQ-4217175 的 Hotfix
* 工作流程例項卡在「Salesforce.com 匯出」工作流程步驟。NPR-19222：CQ-4212976 的 Hotfix
* 從 Live Copy 建立的語言副本頁面無法編輯。NPR-18967
* ReferencesUpdateAction 無法在階層變更的情況下將連結更新至巢狀 LiveCopy。NPR-18715：CQ-4214105 的 Hotfix

### 平台 {#platform-9}

* Adobe 電子郵件範本服務為自訂使用者範本新增了標記。NPR-19190：CQ-4217113 的 Hotfix

### 專案 {#projects-2}

* 專案編輯器無法將資產複製/貼上至專案資產資料夾中。NPR-19619
* 安裝 6.2 SP1-CFP1 後，無法為翻譯專案產生預覽。NPR-16481：CQ-4204655

### 整合 {#integration-12}

* 傳統 UI 上 Adobe Digital Publishing Solution 中文章的存取屬性設定錯誤。NPR-19366
* 由於 AEM Article 控制台中的完整尺寸文章，縮圖轉譯程序變得緩慢。NPR-19086：CQ-4217148
* 如果使用者擁有多個區域的存取權，透過 Campaign 對優惠方案進行個人化設定時，自動折疊功能會出現錯誤行為。NPR-19290：CQ-4218029 的 Hotfix
* 編輯並儲存目標模組超過一次時，不會在目標定位模式中顯示目標定位對話方塊。NPR-19144：CQ-4216708 的 Hotfix

### 工作流程 {#workflow-2}

* 使用者無法在收件匣傳統 UI 中依使用者/群組來篩選收件匣中的通知。NPR-19122：CQ-4215374 的 Hotfix
* 影像映射不會保留 HTL 影像元件中選取的座標。NPR-18911：CQ-4211584

## 表單 {#forms-12}

* 透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-12}

* 將內容從 Microsoft Word 或 Web 瀏覽器複製到通信管理器文字編輯器中時，樣式會遺失。NPR-19530
* 文字編輯器中沒有分行符號的內容不會換行。NPR-19481
* 啟用可在預覽信函時搜尋文件片段中實際文字的功能。NPR-17792：CQ-4214501 的 Hotfix

#### 通信管理 {#correspondence-management-5}

>[!NOTE]
>
>這個文字片段搜尋功能具有一些限制：
>
>* 文件片段內容區分大小寫，標題則不區分大小寫。
>* 搜尋字詞的一部分使用不同的樣式或包含特殊字元 (如 &quot;、&#39; 或\) 時，搜尋結果不會醒目提示。
>* 在文件片段中，無法對動態內容 (例如資料字典元素值或變數值) 進行搜尋。


#### Forms管理員{#forms-manager-2}

* 在 AEM 6.2 上套用 CFP6 後，無法編輯調適型表單的 XML 結構屬性。CQ-4219684 的 Hotfix
* 重新啟動伺服器時，沒有啟動 AEM Forms Manager 核心套件組合的所有服務。CQ-4217014 的 Hotfix

### Forms JEE 安裝程式 {#forms-jee-installer-12}

#### 安裝 LCM {#install-lcm-2}

* 安裝 CFP6 後，Microsoft Windows 上的管理員畫面會顯示版本號碼 6.0。CQ-4217573 的 Hotfix

## 包含的 Feature Pack {#feature-packs-included-2}

* 增強桌面應用程式的觸控式 UI 按鈕。NPR-18676

## CFP8 中包含的 OSGi 套件組合{#osgi-bundles-included-in-cfp}

AEM 6.2SP1-CFP8 中更新的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/updated-bundles-list-cfp8.txt)

AEM 6.2SP1-CFP8 中更新的內容套件清單

[取得檔案](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 針對 dc:title 屬性設為 String [] (多欄位) 的影像，在影像卡片上顯示標題的行為變更。
* Dynamic Media Cloud Services、觸控式 UI 和安全性 UI 介面的效能問題修正。
* Apache Felix Http Bridge 3.0.8 中的修正
* 解決製作與發佈環境之間的無二進位檔複寫 (BLR) 問題。
* 支援目標程式庫檔案 AT.JS，這個實作程式庫專為一般 Web 實作和單頁應用程式而設計，用於整合用戶端與 Adobe Target。
* 針對 Marketing Cloud 解決方案 (Analytics、DTM、Target 和 S&amp;P) 推出使用者可設定的連線逾時期間，以改善 AEM 效能。

### 資產 {#assets-12}

* 透過以 Dynamic Media Cloud Services 設定的 AEM 6.3 測試視訊擷取時，會引發「開啟的檔案太多」例外狀況。NPR-18734；CQ-4211407 的 Hotfix
* 重新啟動 AEM 執行個體後，頁面上資產的虛名 URL 設定無法運作。NPR-18634；Granite-18085 的 Hotfix
* 在觸控式 UI 中，會向沒有發佈資產權限的使用者顯示「發佈」按鈕。NPR-18620；CQ-4214042 的 Hotfix
* 為資產設定授權合約後，資產的下載對話方塊中就不會出現動態轉譯選項。NPR-18607；CQ-4212342 的 Hotfix
* 無法為名稱中包含空格的資產下載動態轉譯。NPR-18571；CQ-4211738 的 Hotfix
* 與 Creative Cloud 共用資產資料夾時，無法儲存超過一名使用者。NPR-18489；CQ-103297 的 Hotfix
* dc:title 和 dc:description 不會變更為 crx /de 中的多欄位值。NPR-18474；CQ-4209086 的 Hotfix
* 移動資產的操作會導致效能降低。NPR-18346
* 以預設的「全部顯示」選項設定開啟時間軸時，時間軸中不會顯示任何項目。NPR-18302；CQ-4211957 的 Hotfix
* 將 ASCII/UTF-8 編碼文字檔上傳至 AEM Assets 時發生錯誤，且產生縮圖失敗。NPR-18006：CQ-4209345 的 CFP
* 就算使用者沒有複寫存取權，也會顯示發佈動作按鈕。NPR-17353；CQ-4209269 的 Hotfix
* 使用 min:gcc;obfuscate=true 啟用縮製時，Siteadmin 和 Miscadmin 都無法運作。NPR-18593；CQ-4209220 的 Hotfix
* 每次重新整理畫面後，才會顯示自訂功能表項目。NPR-18500；CQ-4213581 的 Hotfix
* 將 moment.js 升級至 2.10.6。NPR-18596；Granite-11881 的 Hotfix
* 套用 DM 巨集的權限時會中斷管理員使用者的檢視。NPR-18544；CQ-4211729 的 Hotfix
* 對資產執行「稍後發佈」會擲回不正確的 ArgumentException。CQ-4214532

### 網站 {#sites-12}

* 時間到達內容的「開啟時間」設定時，在具有 MongoDB 的主動-主動作者叢集上，兩個作者都會嘗試針對相同內容觸發複寫。NPR-18708；CQ-4210982 的 Hotfix
* 資源的參考若沒有 jcr:content 節點，移動該資源時會引發 NPE。NPR-18664
* 包含多個 parsys 元件的頁面中沒有顯示預留位置。NPR-18645；CQ-110253 的 Hotfix
* AbstractCopyMoveCommand 中出現並行問題。NPR-18591
* 將文字從另一個 AEM 執行個體複製到 parsys 元件時，會建立 parsys 而不設定任何 resourceType。NPR-18511；CQ-4212306 的 Hotfix

### 平台 {#platform-10}

* 安裝套件後 JCR 安裝程式沒有更新套件組合版本。NPR-18728；NPR-15135 的 Hotfix
* 對製作和發佈環境之間的二進位檔進行無二進位檔複寫 (BLR) 時失敗。NPR-18704
* AEM 環境中的 Apache Felix Http Bridge 解析請求。NPR-18297
* 透過 Sling Content Distribution 同時複寫具有類似結構的多個頁面時，複寫會失敗。NPR-18665；Granite-13712 的 Hotfix
* Sling 散發套件會建置且不會自行清理。NPR-18601；Granite-16183 的 Hotfix

### 整合 {#integration-13}

* 檢視從程式庫資料夾發佈的選件會引發 NPE。NPR-18732；CQ-4214593 的 Hotfix
* 從特定日期變更為「啟用/停用時」時，JCR 和 Target 中活動的開始/結束日期不會更新。NPR-18612；CQ-104831 的 Hotfix
* Analytics 與 AEM 的整合沒有為 httpclient 連線設定連線或通訊端逾時。NPR-18497
* DTM 與 AEM 的整合沒有為 httpclient 連線設定連線或通訊端逾時。NPR-18495
* Target 與 AEM 的整合沒有為 httpclient 連線設定連線或通訊端逾時。NPR-18494
* Search&amp;Promote 與 AEM 的整合沒有為 httpclient 連線設定連線或通訊端逾時。NPR-18493
* 新增額外體驗後，Target 活動會停用。NPR-18227；CQ-4201895 的 Hotfix

### WCM-Foundation 元件 {#wcm-foundation-components-7}

* 影像映射不會保留 HTL 影像元件中選取的座標。NPR-18530；CQ-4211584 的 Hotfix

### 轉換 {#translation-5}

* 翻譯搜尋結果沒有包括翻譯專案的名稱。NPR-18224；CQ-4210658 的 Hotfix

### 品牌入口網站 {#brand-portal-1}

* 啟用透過標記管理員/標記控制台將標記從 AEM 發佈至 Brand Portal 的功能。CQ-4212165

## 表單 {#forms-13}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-13}

#### 通信管理 {#correspondence-management-6}

* 儲存片段之前，編輯面板中不會顯示正確的資料。NPR-19092
* 將文件片段加入信函中需要相當長的時間。NPR-18958
* 如果資料 xml 檔案中存在 XML 聲明，且信函轉譯已透過 POST 請求起始，則對應的信函無法顯示資料。NPR-18870
* 系統不會為對 CM 資產採取的動作產生稽核日誌。NPR-16618

>[!NOTE]
>
>如果您受到以下兩個問題影響，請勿安裝此 CFP 附加套件：
>
>* 從 Word/Web 複製貼上到 CM 文字編輯器時，內容中顯示分行符號。NPR-19530
>* CM 文字編輯器中沒有分行符號的內容不會換行。NPR-19449

>
>
這些問題將在未來的 CFP 中解決。

#### 調適型表單 {#adaptive-forms-9}

* 為可重複面板新增面板時，會刪除上一個面板中下拉式欄位的值。NPR-18772
* 標記為僅接受整數的調適型表單欄位也接受數字鍵盤上的幾個特殊字元。NPR-18680
* 用於在初始化 guideroot 面板事件時變更按鈕標題的指令碼無法運作。NPR-18476
* 右側面板中，在規則編輯器下建立的規則沒有顯示捲軸。NPR-18716

#### AEM Forms 應用程式 {#aem-forms-app}

* 表單處於離線模式或未連線至網路時，表單無法在 AEM Forms App 中正確轉譯。CQ-4218368

### Forms JEE 安裝程式{#forms-jee-installer-13}

#### PDFG 服務 {#pdfg-service-3}

* PDF 產生器無法產生含有指定書籤層級的 PDF 文件。CQ-4211102 的 Hotfix

## CFP7 中包含的 OSGi 套件組合{#osgi-bundles-included-in-cfp-1}

AEM 6.2SP1-CFP7 中更新的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

AEM 6.2SP1-CFP7 中更新的內容套件清單

[取得檔案](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 在平板電腦的版面模式中有效管理隱藏的元件。
* 在混合裝置上推出快速動作。
* 解決 Live Copy 的元件層級同步問題。

### 資產 {#assets-13}

* 不具有必要權限的使用者嘗試移動資產上的作業時，客戶會遭到封鎖。NPR-18330；CQ-4212560 的 Hotfix
* 合併多個智慧內容服務設定會造成可用性問題。NPR-18273；CQ-4201557 的 Hotfix
* 一旦 Assets 資料夾中新增約 80 個片段，就無法從時間軸控制台使用「結帳動作/工作流程」。NPR-18257；CQ-4211214 和 NPR-18251 的 Hotfix；CQ-4211216 的 Hotfix。
* Assets 進行報告期間，系統因記憶體不足和缺少分頁而當機。NPR-17865；CQ-4209759 的 Hotfix
* 發佈的視訊無法在已編碼的視訊資產上播放。NPR-17849；CQ-4210739 的 Hotfix
* 系統不會產生 PDF 的縮圖。NPR-17831、NPR-17750；CQ-4210547 的 Hotfix
* Adobe CQ DAM 到期通知工作停用不會過期的資產。NPR-17666；CQ-107766 的 Hotfix
* 如果資產沒有指派的擁有者，資產到期活動會停止。NPR-17665；CQ-4197946 的 Hotfix
* 當資產資料夾中有超過 150 傳入的參考移動時，會出現 Null 指標例外狀況。CQ-4200981

### 網站 {#sites-13}

* 為 IP 範圍設定分段規則時，個人化只對第一個 IP 有效。NPR-18121；CQ-83767 的 Hotfix
* 啟用 historyShow 屬性時，登入會因 NumberFormatException 而失敗。NPR-18073；CQ-101965 的 Hotfix
* 觸控式 UI 中會顯示已標記的已刪除頁面。NPR-18025；CQ-86694 的 Hotfix
* 載入具有大量 (2000+) 受眾的頁面時出現效能問題。NPR-17884；CQ-4209567 的 Hotfix
* 移除頁面上的其他影像後，無法選取影像。NPR-17711；CQ-4201323 的 Hotfix

### 平台 {#platform-11}

* 沒有向不具有必要權限的使用者隱藏觸控式 UI 控制項。NPR-17945；CQ-4211231 的 Hotfix
* TagPicker 欄位上遺漏日文標記。NPR-17768；CQ-4210456 的 Hotfix
* FastQuerySize 已啟用時，getsize() 查詢會傳回不正確的結果。NPR-18018
* 無法存取待命執行個體上的 Web 控制台。NPR-17861；Granite-14582 的 Hotfix

### 商務 {#commerce-2}

* 目錄 Blueprint 沒有為區段定義任何條件時，會發生查詢周遊情況。NPR-18229；CQ-4211924 的 Hotfix

### 社群 {#communities-2}

* PollingImporterImpl導致 AEM 延遲關閉。NPR-18298；CQ-96133 的 Hotfix

### Integrations {#integrations}

* 解決 AEM Day HTTP Client 3.1 OSGI 設定的 Proxy 要求進行摘要式驗證時可能出現的 AEM 搜尋元件錯誤。18128 盧比
* 遺漏還原繼承的核取方塊。NPR-17753；CQ-4210139 的 Hotfix 請求
* 以多個活動定位一個元件時，使用者無法設定優先順序。NPR-18658；CQ-4210727 的 Hotfix
* 使用者無法瀏覽 /etc/segmentation 資料夾以選取在 /etc/segmentation/group1 資料夾底下建立的受眾。NPR-18522

### 安全性 {#security-1}

* 如果使用者沒有目標資料夾的寫入權限，移動資產精靈便會中止。NPR-18300
* 請求在 Apache Sling API 中使用 org.apache.sling.servlets.post servlet 的升級版本 (2.3.22) 以搶先遏止 XSS 漏洞。NPR-18963

### 轉換 {#translation-6}

* 專案完成之前，不應允許將資產頁面重新提交至翻譯專案。NPR-18249；CQ-4209908 的 Hotfix

### WCM-Foundation 元件 {#wcm-foundation-components-8}

* 無法在可編輯的範本中使用 WCM foundation iparsys 元件。NPR-18223；CQ-4210384 的 Hotfix
* 影像映射不會保留 HTL 影像元件中選取的座標。NPR-18032；CQ-4211584 的 Hotfix
* HTL 影像元件轉譯時，URL 中的檔案名稱會重新命名而造成 URL 損毀。NPR-17908；CQ-4211587 的 Hotfix
* 進行變更後無法退出「頁面屬性」。NPR-17832；CQ-96110 的 Hotfix

## 表單 {#forms-14}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-14}

**通信管理**

* 信函轉譯期間會重複讀取資料字典。NPR-18482、CQ-4210805 的 Hotfix
* 為 com.adobe.livecycle.content 類別新增 JavaDocs。NPR-18467
* 建立信函時沒有儲存信函說明。NPR-18039
* 文字模組已儲存，且文字模組中的運算式不包含開頭或結尾運算式標記時，系統沒有顯示錯誤訊息。文字模組顯示錯誤訊息且無法在信函中轉譯。NPR-17798
* 安裝附加套件時記錄中出現未預期的錯誤。NPR-18295

**Forms Manager**

* AEM Forms UI 從最舊到最新列出所有資產。使用者無法從最新到最舊重新排序資產。NPR-18451

### Forms JEE 安裝程式{#forms-jee-installer-14}

**輸出服務**

* 改善 AEM Forms 6.2 的輸出服務效能問題。NPR-18033

**簽名服務**

* 無法使用遠端硬體安全性模組簽署 PDF 檔案。NPR-18017

## CFP6 中包含的 OSGi 套件組合{#osgi-bundles-included-in-cfp-2}

AEM 6.2SP1-CFP6 中更新的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

AEM 6.2SP1-CFP6 中更新的內容套件清單

[取得檔案](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 解決共用、移動、發佈及下載資產的數個 UI 問題。
* 增加「移動」對話方塊顯示參考資產的容量。
* 解決 WCM 元件和工作流程的數個問題，例如「解除發佈」和「版本清除」。
* 改善動作列在顯示工具列動作和 Coral 元件方面的回應能力。

### 資產 {#assets-14}

* 改善發佈至 Brand Portal 功能的效能。NPR-17189；CQ-4204150 的 Hotfix
* 使用「共用連結」選項共用資產時，不會建立具有單層資料夾結構的 zip 檔案以供下載。NPR-17513；CQ-4209381 的 Hotfix
* 在 DAM 中選取資產並按一下「發佈」時，不會在「資產詳細資料」頁面中顯示「發佈至 Brand Portal」選項。NPR-17351；CQ-94905 的 Hotfix
* 在 DAM 工作流程步驟中，必須在最終區塊中封閉從工作階段或 ResourceResolver 取得的二進位資料流，以確保不會發生資源洩漏情形。NPR-17385；CQ-4209452 的 Hotfix
* 在 DAM 中上傳 Word 檔案會導致 Null 指標例外狀況，而工作流程例項維持卡在「執行中」狀態。NPR-17160；CQ-4207358 的 Hotfix
* 針對過期的資產，非管理員使用者可在「中繼資料編輯器」頁面上看到「共用」、「移動」、「發佈」和「下載」按鈕。NPR-16903；CQ-101440/CQ-104535 的 Hotfix
* Assets 控制台中的管理使用者應可看到「共用」、「移動」、「發佈」和「複製」等動作。NPR-16902；CQ-4207111 的 Hotfix

### 網站 {#sites-14}

* 使用傳統和觸控式 UI 來移動頁面時，「移動」對話方塊不會顯示超過 150 個參考，導致使用者無法更新這些參考和重新發佈頁面。此問題已藉由為傳統 UI 引入「maxRefNo」屬性而解決，這個屬性可在網站管理員節點「/libs/wcm/core/content/siteadmin」上設定。此屬性指定了進行大量移動作業之前顯示的最大參考數 (預設值 150)，而如果頁面的參考數較多，則不會顯示在 movePage 對話方塊中。此設定也適用於 damadmin 和 miscadmin，方法是分別在以下節點上套用設定：`'/libs/wcm/core/content/damadmin'` 和 `'/libs/wcm/core/content/miscadmin'`。NPR-17222；CQ-85878 的 Hotfix

* 使用 WCM 元件時，觸控式 UI RTF 編輯器會移除含有空格的超連結。NPR-17698、NPR-17570；CQ-4206768 的 Hotfix
* 從頁面屬性觸發「取消發佈請求」工作流程時，無複寫權限的使用者會出現 JavaScript 錯誤。NPR-17294；CQ-102064 的 Hotfix
* 轉譯或匯出 HTL 影像元件時，會將 URL 變更為數字並重新命名檔案名稱，進而造成連結損毀。NPR-17245；CQ-59616 的 Hotfix
* 刪除巢狀啟動中的啟動會造成子啟動變為孤立狀態。NPR-17228；CQ-4202639 的 Hotfix
* 在套用 Oak 1.4.13 的 AEM 6.2 中執行「版本清除」會造成記錄中出現不斷重複的警告。NPR-17391；CQ-4206870 的 Hotfix
* 安裝 ContextHub 元件的 Hotfix 或升級後，內容套件會覆寫 /etc/segmentation/contexthub 中的所有區段，導致所有自訂 ContextHub 區段都遺失。NPR-17250；CQ-79958 的 Hotfix
* 以工作流程使用者身分執行含巢狀群組的工作流程時，WorkflowStatusProvider (pageinfo.json) 會造成工作流程例項鎖定。NPR-17555；CQ-4202056 的 Hotfix
* 使用 WCM-頁面編輯器元件時，在製作執行個體的觸控式 UI 編輯模式下，頁面末端存在大量空格。NPR-17510；CQ-4205441 的 Hotfix
* 轉譯或匯出 HTL 影像元件時，會將 URL 變更為數字，進而造成連結損毀。NPR-17245；CQ-59616 的 Hotfix

### UI {#ui}

* 選取資產並按一下「開發人員工具」時，不一定會以緩慢的連線顯示動作列中的工具列動作，而且必須重新載入頁面。NPR-17568；CQ-108365 的 Hotfix
* 動作列應更新為使用兩個容器：coral-actionbar-primary 和 coral-actionbar-secondary，而非 coral-actionbar-container。NPR-17591；GRANITE-15225 的 Hotfix

### Mobile-on-demand {#mobile-on-demand-2}

* 擁有 AEM Mobile 應用程式「唯讀」權限的使用者，無法從 AEM Mobile 的「內容管理」頁面預覽內容。NPR-17390；CQ-4209690 的 Hotfix

### 安全性 {#security-2}

* HTMLRendererServlet 產生的輸出中有 XSS 漏洞。NPR-17136
* 請求防止 AEM Web 新聞訂閱摘要頁面中的 AEM 發行版本洩漏。NPR-16219

### 表單 {#forms-15}

#### Forms 附加元件套件 {#forms-add-on-package-15}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

**調適型表單**

* 針對具有附件的調適型表單，在第二次提交表單時，會在提交的 XML 中建立 afSubmissionInfo 標記的重複項目。NPR-17364
* 使用 Google Chrome 瀏覽器時，從表單中移除附件後，嘗試重新附加相同的附件會擲回錯誤。NPR-17297
* 如果 XSD 式或無表單模型式調適型表單中有可重複的巢狀延遲載入面板，則表單中填入的值不會保留在記錄文件 (DOR) 中。NPR-17176
* 錯誤記錄中顯示的規則編輯器的錯誤記錄，應新增至 try/catch 區塊 JavaScript 程式碼的 catch 區塊中。NPR-16757
* 按一下表單中的檔案附件時會擲回瀏覽器控制台錯誤，而不會顯示附件預覽。NPR-17174

**通信管理**

* 如果在 UI 中新增內嵌文字或空白行，「建立通信 UI」功能會失效。NPR-17748
* 開啟信函以進行編輯時，瀏覽器畫面會閃爍。NPR-17576
* 在計算資料字典元素中新增遠端函數時，如果函數的數量超過顯示遠端函數的索引標籤長度，則卷軸不會出現在索引標籤中。NPR-17359
* API 方法，匯入 com.adobe.icc.services.api.LetterInstanceService 無法運作。NPR-17922、NPR-16008
* 編輯信函時，在文字模組中新增的變數不會顯示在「資料繫結」面板中。NPR-17940
* HTML 提交動作使用 POST 方法時，通信管理 UI 不會啟動。NPR-17595

**Forms經理**

* 在針對 AB 測試設定的調適型表單中，按一下「開始 AB 測試」時不會開始測試，且會擲回瀏覽器控制台錯誤。NPR-17838

**表單服務**

* 應修正 OSGI 表單靜態程式碼分析中報告的問題。NPR-13951

#### Forms JEE 安裝程式 {#forms-jee-installer-15}

**輸出服務**

* 使用 AEM Forms 6.2 輸出服務來合併特定表單與資料 XML 所需的時間，是 LiveCycle ES4 SP1 伺服器執行相同作業所花費的 20 倍。此問題已在 Windows 和 Linux 環境中修正。NPR-17501

**安裝 LCM**

* 安裝 AEM Forms 6.2 GM 組建並套用 AEM 6.2 CFP 後，執行 LiveCycle Configuration Manager 時，「版本資訊」中會顯示不必要的分號，而且 Hotfix 安裝日期不會更新。NPR-14322

**處理程序管理**

* 沒有為 AEM Forms 處理程序填入 TaskContext 變數。CQ-4211857

#### AEM Forms JEE 套件組合套件 {#aem-forms-jee-bundles-package}

* 無論是使用 JEE 管理員 UI 控制台還是 OSGi 控制台，表單使用者可使用的功能應相同。NPR-17670

### CFP5 包含的 Feature Pack {#feature-packs-included-in-cfp}

**Forms JEE 套件**

處理程序管理 - HTML 工作區

* 指派工作區步驟時，如果存在多個附件或附註，工作區附件索引標籤應顯示附件或附註的計數器。NPR-17771
* 請求在 AEM JEE Forms 中支援 Office 365，以取得表單工作流程中的電子郵件功能。NPR-13866

**Forms 附加套件**

通信管理

* 信函預覽期間在文字編輯器中編輯片段時，應顯示處理過的文字以供編輯，而非片段中使用的內嵌條件。NPR-15748、NPR-17504

### CFP5 中包含的 OSGi 套件組合{#osgi-bundles-included-in-cfp-3}

AEM6.2 SP1-CFP5 之間更新的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/cfp5_osgi_bundles.txt)

AEM6.2 SP1-CFP5 之間更新的內容套件清單

[取得檔案](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 為重要更新，包含自 AEM 6.2 SP1 正式發行以來累積的重要客戶修正。

此 Cumulative Fix Pack 的關鍵重點為：

* 針對 Camera Raw 檔案轉譯、時間軸檢視和影像方向的資產修正
* 改善以下功能

   * 網站的 WCM 啟動
   * 專案工作流程
   * ContextHub 元件

* 促銷活動、Mobile On-Demand 和翻譯的修正
* 調適型表單規則編輯器中的可用性改善
* 增強用於 Forms 中通信管理的內嵌條件編輯器
* JEE 版 AEM Forms 的處理程序管理與輸出服務的修正
* 指令碼編輯器的 Forms Designer 相關修正

### 平台 {#platform-12}

* Search&amp;Promote 搜尋表單會在設定雲端服務時忽略 `environment` 設定，導致其無法用於製作執行個體。NPR-16594：CQ-4206076 的 Hotfix
* 無法藉由在 /apps 中覆蓋來將欄新增或自訂至 **Assets OmniSearch** 結果。NPR-16737：CQ-4206785 的 Hotfix
* 從 AEM 6.1 SP2 就地升級至 AEM 6.2 SP1 後，**診斷工具**頁面無法運作。NPR-17121；CQ-4196786 的 Hotfix
* HTL：選取論壇、建立主題和貼文時，`Sightly SightlyCompiledScript` 將不正確的 `addSelectors` 屬性新增到 `RequestDispatcherOption` 中。NPR-17008：GRANITE-16384 的 Hotfix

* 新增對 `ReportImporter` 在 `ManagedPollConfigs` 中所使用 `CRON expressions` 的支援。NPR-16608：CQ-4206066 的 Hotfix 請求

* 上傳 LDAP 使用者的顯示圖片影像失敗。NPR-16561；Granite-17013 的 Hotfix
* 「使用者管理」畫面中顯示的結果數量在「卡片」和「清單」檢視中不同。NPR-16241；GRANITE-16914 的 Hotfix
* 在 Google Chrome 瀏覽器中以全螢幕模式檢視時，工作流程通知無法延遲載入。NPR-17013：CQ-4207567 的 Hotfix

### 資產 {#assets-15}

* 匯入具有已定義方向的影像時，無法正確套用影像方向。NPR-16750：CQ-4204356 的 Hotfix
* 即使預設設定了「全部顯示」，「資產時間軸」檢視仍不會顯示任何資產。NPR-16957：CQ-98780 的 Hotfix
* 將 Camera Raw 檔案 (包括 ARW、CR2、NEF、DNG 和 EPS) 新增為資產中的轉譯時，無法選取或刪除檔案。使用者按一下這些檔案時，就會自動下載這些檔案。NPR-16949：CQ-4206846 的 Hotfix
* 在 Assets UI 中建立另一個 PDF 時，不會在 DAM UI 中顯示已建立的 PDF，不過這些 PDF 會顯示在 crx 存放庫中。NPR-16833：CQ-4206501 的 Hotfix
* 使用觸控式 UI 上傳資產以作為其本身的直接子節點會導致一個問題。資產會上傳為前一個所選資產的直接子節點。NPR-16534：CQ-4204287 的 Hotfix
* 在 DAM UI 中，在註解中對資產加上註解和標記使用者時不會產生郵件通知。NPR-16589：CQ-102318 的 Hotfix

### 專案 {#projects-3}

清除工作流程時，專案工作流程控制台在頁面上顯示 NullPointerException。NPR-17017：CQ-4194269 的 Hotfix

### 網站 {#sites-15}

* `ContextHub` 中的檔案不會在製作執行個體上最小化。NPR-17022：CQ-79456 的 Hotfix
* WCM-Launches 啟動促銷活動需花很長時間才能提升由大型樹狀結構頁面組成的啟動。NPR-16480：CQ-82731 的 Hotfix
* 使用非運作中或未完成的規則建立區段 (或受眾) 時，`ClientContext` 區段條件轉譯程式當機。NPR-16759：CQ-4205104 的 Hotfix
* 在 WCM Launches 中，從觸控式 UI 的頁面屬性中起始動作時，與啟動相關聯的頁面不會解除發佈。NPR-16560：CQ-4204681 的 Hotfix
* 連結重寫器假設冒號「:」定義了 JCR 命名空間，因而錯誤重寫包含冒號的 href 值。NPR-16753：CQ-4203762 的 Hotfix
* 在 WCM-Design Importer 中，開啟測試匯入程式頁面並嘗試上傳 zip 檔案時，如果檔案先前已上傳並刪除，則會引發問題。NPR-16486：CQ-90962 的 Hotfix
* 使用 Firefox、Safari 和 Google Chrome 瀏覽器導覽至&#x200B;**[!UICONTROL 「全域導覽」]**&#x200B;窗格時，會提供不同的使用者體驗。Firefox 瀏覽器會顯示&#x200B;**[!UICONTROL 「工具」]**&#x200B;功能表，Google Chrome 瀏覽器則會顯示&#x200B;**[!UICONTROL 「導覽」]**&#x200B;功能表。NPR-16770；CQ-4200456 的 Hotfix

### 行銷活動 {#campaign}

* 測試 AEM 促銷活動範本和修改種子位址以包含「其他資料」時，Adobe Campaign下拉式清單會在觸控式 UI ContextHub 中消失。NPR-16771：CQ-105748 的 Hotfix

### Mobile On-Demand {#mobile-on-demand-3}

* 從 AEM 製作環境預檢發佈內容時，若「預檢」動作耗時超過 5 秒，會導致「AEMM - AEM PECS 整合」Splunk 控制面板上出現異常尖峰，且每秒都會出現大量狀態請求。NPR-16908：CQ-4207055 的 Hotfix
* 安裝 AEM-6.2-SP1-CFP1-1.0 更新後，AEM Mobile 設定管理會失敗。NPR-16909：CQ-4204892 的 Hotfix

### 轉換 {#translation-7}

* 安裝 6.2 SP1 - CFP1 後，預覽翻譯工作無法運作。NPR-16481；CQ-4204655 的 Hotfix
* 使用「翻譯」建立的語言副本會指向「根主版」，而不是指向當地國家/地區的 LiveCopy。NPR-17257；CQ-4208287 的 Hotfix

### 安全性 {#security-3}

* 將檔案的二進位檔上傳至 AEM 時，不會執行 MIME 類型驗證。NPR-16617
* 上傳 LDAP 使用者的顯示圖片影像時發生問題。NPR-16561

### 表單 {#forms-16}

#### Forms 附加元件套件 {#forms-add-on-package-16}

**調適型表單**

* 在調適型表單編輯器中，head.jsp 中的「Target 設定」註解應以新的 ContextHub 陳述式取代。NPR-17173
* 在調適型表單規則編輯器中，**[!UICONTROL 「選擇項目」]**&#x200B;會將事件顯示為「null」。NPR-17139
* 使用下一頁箭頭 (>) 往下一頁導覽時，已提交的表單會重新提交。NPR-17080
* 透過 AJAX 提交調適型表單時，絕不會在發生錯誤時叫用「error」回呼函數。NPR-17034
* 在執行時間按一下規則編輯器中的&#x200B;**[!UICONTROL 「儲存表單」]**&#x200B;按鈕時，不會儲存表單。NPR-16905
* 靜態文字應排除在調適型表單的 Tab 鍵瀏覽順序之外。NPR-16749
* 不正確顯示小數欄位的計算值。NPR-16596
* 顯示「說明」內容的圖示應包含在調適型表單的 Tab 鍵瀏覽順序中。NPR-16484
* 針對預填調適型表單的資料，支援在「**[!UICONTROL 預設預填服務設定]**」中使用 `dataRef=C:/Users/` 類型的規則運算式。NPR-16425

* 如果有巢狀延遲載入情況，就無法對所有面板正確觸發驗證。NPR-15821

**通信管理**

* 如果信函中包含空白文字模組 (其中不含文字)，則信函轉譯會失敗。NPR-17054
* 在文字編輯器中貼上內容後，會移除內容中的分行符號和 Tab 空格。NPR-17039
* 如果在許多信函中參考文字模組，則顯示文字模組的參考時需花很長的時間。NPR-17035
* 編輯、儲存、刪除和設定文件片段的參考需花很長的時間。NPR-17033
* 預覽信函時，對齊的文字會以不同的字型轉譯。NPR-16976
* 如果搜尋的文字出現多次，搜尋功能就無法正常運作。NPR-16920
* 文字編輯器工具列在瀏覽器中間歇性顯示。NPR-16919
* 規則編輯器的&#x200B;**[!UICONTROL 「儲存表單」]**&#x200B;結構無法運作。NPR-16905
* 使用 Internet Explorer 根據資料字典建立文字模組時，「字型」下拉式清單不會填入字型系列。NPR-16944
* 建立文字片段後，信函字型會在預覽信函時變更。NPR-16830
* 文件片段中，運算式開頭或之間有 Tab 空格的信函無法轉譯或預覽。NPR-16769

**行動表單**

* 「行動表單」預覽會顯示重疊的內容，不過表單會正確顯示以供 PDF 轉譯。NPR-17105

**表單入口網站**

* 按一下已提交表單的&#x200B;**[!UICONTROL 「下載」]**&#x200B;連結時，會開啟 HTML 頁面而非 PDF 表單。NPR-17082

* 針對已提交的例項，儘管檔案附件的 `Upload Comments` 位於儲存在 crx 存放庫中的 XML 中，卻不會顯示在 UI 中。NPR-17075

**Reader 延伸模組服務**

* AEM Forms OSGI 安裝中的特定檔案不是 Reader Extended。NPR-16625

#### Forms JEE 安裝程式{#forms-jee-installer-16}

**核心**

* 進行升級期間，Configuration Manager 會因逾時而失敗。NPR-16774 (請參閱[為元件層級的作業設定逾時](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr))。

**處理程序管理 - HTML 工作區**

* 「啟動任務」的起始點不是從提交起始點時提交的資料開始。NPR- 16917
* 在 HTML 工作區中按一下表單的&#x200B;**[!UICONTROL 「傳回」]**&#x200B;按鈕時不會關閉表單，而是將其傳回至其「群組佇列」。\
   NPR-16352

**處理程序管理**

* 允許使用者將先前任務的顯示名稱設定為程序執行個體中的任何後續任務。NPR-15382

**輸出服務**

* 輸出服務無法處理已修改為在 `date-time format` 中繼資料中包含額外「毫秒」欄位的 PDF。NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer 指令碼編輯器不會遵循 `Calculate Event` 和 `Validate Event` 的「表單屬性」預設值。NPR-15921

### CFP4 包含的 Feature Pack {#feature-packs-included-in-cfp-1}

**Forms 附加套件**

* 增強用於通信管理的內嵌條件編輯器。NPR-10981

### CFP4 中包含的 OSGi 套件組合{#osgi-bundles-included-in-cfp-4}

AEM 6.2 SP1 和 CFP4 之間更新的 OSGi 套件組合清單

CFP3 的關鍵重點為：

* 針對傳統 UI 和使用 Proxy 搭配摘要式驗證的 AEM Search 元件，提高搜尋功能的效率
* 修正上傳資產和顯示資產中繼資料時的問題
* 修正標題中有特殊字元的情況下建立資料夾和移動頁面時的問題。
* 修正使用目標同步受眾、發佈促銷活動，以及在觸控式 UI 中選取目標量度時的問題
* 解決翻譯工作的同步問題
* 為 Forms 預填服務提供增強的安全性
* 改善條碼式表單服務中的表單入口網站草稿和提交元件
* 包含檔案附件小工具或延遲載入片段的調適型表單可用性改善。
* 通信管理中的可用性改善，包括增強的搜尋功能、記錄已刪除的資產以及匯入資料字典。

### 平台 {#platform-13}

* **ModelAdapterFactory** 中的競爭情形 (可能發生在兩個執行緒嘗試插入同一欄位時) 會導致無法構建模型。NPR-16443：SLING-6584 的 Hotfix
* 套件管理器中的驗證選項，可偵測 /apps 底下覆蓋的檔案 (JSP 或 JavaScript 檔案) 與 /libs 底下 Hotfix 中所包含的檔案之間的任何衝突。接著受影響的覆蓋便可重訂基底以包含 /libs 底下檔案的變更。NPR-16216：CQ-81729 的 Hotfix
* 在 error.log 中記錄時有時會在啟動發佈工具後數秒內停止，而且需要清除才能再次執行。請求更新記錄架構和提供 Sling 記錄。NPR-15913：Granite-15452 的 Hotfix
* 請求更新 JavaScript &quot;`use"` API 以避免 HTL JavaScript Use API 實作失敗。NPR-16461：SLING-6780 的 Hotfix

### 網站 {#sites-16}

* 從 AEM 6.0 升級至 AEM 6.2 後，傳統 UI 會因為大量查詢而在搜尋標記時出現效能緩慢情形。若要解決此問題，可以依照[在標記控制台 (傳統 UI) 中停用複寫狀態](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr)底下提及的步驟操作。NPR-15842：CQ-4201748 的 Hotfix。

* 在觸控式 UI 中建立頁面時，對「名稱」欄位進行的輸入檢查不會檢查特殊字元縮寫符號 (與傳統 UI 中相同)，因此無法移動頁面。NPR-16404：CQ-4205321 的 Hotfix。
* 在 RTF 編輯器中對兩列套用不同的樣式，然後再合併這兩列時，會移除對第二列套用的樣式。NPR-16389：CQ-4203835 的 Hotfix。
* 在「觸控式 UI 網站」畫面中，嘗試將頁面貼入沒有子頁面的頁面中時，會因為「貼上」按鈕沒有出現而無法運作。NPR-15894：CQ-4201696 的 Hotfix。
* 在「內容尋找器」面板中捲動「頁面」索引標籤時，幾組頁面會在傳統 UI 中無限顯示，而觸控式 UI 只會顯示有限幾組不重複的頁面。NPR-16271：CQ-4202371 的 Hotfix
* 在觸控式 UI 中開啟 LiveCopy 的「頁面屬性」，然後不做任何變更便按一下「儲存」時，系統會記下任何 LiveCopy 索引標籤並建立 LiveSync 設定節點。NPR-16327：CQ-108562 的 Hotfix
* 表單限制無法讀取 `ConstraintMessage` 屬性。NPR-16388：CQ-101330 的 Hotfix
* `wcm/foundation/components/parsys` 元件沒有顯示&#x200B;**[!UICONTROL 「將元件拖曳到這裡」]**&#x200B;預留位置。NPR：16748：CQ-4205187 的 Hotfix

### 資產 {#assets-16}

* 安裝 6.2 SP1 或 Hotfix12430 後，PDF 模擬轉譯器會停止運作，並造成記憶體不足問題。NPR-15991
* 字串屬性 `documentNumber` 的中繼資料顯示為日期，但實為數字。NPR-16134：GRANITE-16916 的 Hotfix
* 時間軸事件球形文字說明中截斷文字。NPR-16226：CQ-85226 的 Hotfix
* 在標題含有特殊字元的的內容階層底下建立資料夾時，會顯示該特殊字元的編碼形式。NPR-15935：CQ-4202987 的 Hotfix
* 使用者瀏覽資產時無法上傳資產或建立資料夾，因為使用「建立」按鈕時顯示的行為不一致。NPR-16410：CQ-4204793 的 Hotfix
* 從 AEM Authoring 的文章檢視上傳共用 HTML 資源時，會發生非預期的錯誤。NPR-16133：AEMM-4155970 的 Hotfix

### 整合 {#integration-14}

* 啟用搭配摘要式驗證的 Proxy 驗證時，AEM Search 元件會擲回 ConcurrentModificationException。NPR-15309：CQ-4199191 的 Hotfix
* 在 AEM 中建立 Target A/B 測試活動時，受眾不會同步至 Target 且會顯示「無受眾」。NPR-16229：CQ-4204210 的 Hotfix
* 安裝 SP1+NPR-11577 v1.2 後，在觸控式 UI 中進行目標定位期間，為目標量度選擇「使用 Analytics 量度」時，量度的下拉式清單不會載入。NPR-16129：CQ-4204316 的 Hotfix
* 使用目標定位時，發佈促銷活動不會自動發佈整個樹狀結構，包括品牌和主版。NPR-15855：CQ-94630 的 Hotfix

### 轉換 {#translation-8}

* 系統不會自動觸發同步翻譯工作，且若沒有探查翻譯專案 AEM 輪詢就不會發生。NPR-15163：CQ-90856 的 Hotfix

### 表單 {#forms-17}

#### Forms 附加元件套件 {#forms-add-on-package-17}

**調適型表單**

* 儲存含有附件的調適型表單時，附件的完整路徑會新增到所產生 XML 的 `fileAttachment` 標記中，而不是附件的名稱中。NPR-16529
* 在 XDP 型調適型表單中，即使預填 XML 沒有 `afData/afBoundData` 包裝函式，`afData/afBoundData` 包裝函式也會出現在提交的 XML 中。NPR-16118

* 數字欄位中的指數表示法：使用調適型表單時，如果所輸入帶有十進位小數的數字總共超過 10 個字元，則在提交的 XML 中該數字會轉變為指數表示法。NPR-16106
* 針對同時包含檔案附件元件和延遲載入片段的表單，提交的資料 xml 不包含檔案附件元件的資訊。NPR-16022
* 針對沒有可重複上階的延遲載入可重複面板，面板的第二個執行個體中可重複的子項無法重複。NPR-15944
* 嘗試在表單編輯器中儲存片段時，片段模型根不會填入子片段的值。NPR-15943
* 在建立僅包含一個項目的核取方塊，並嘗試顯示保持項目標題隱藏的核取方塊標題時，如果項目文字空白，則建立字典動作會擲回 `ArrayIndexOutOfBoundException`。系統不會建立字典，且不會在畫面中產生錯誤回應。NPR-15816
* 針對具有檔案附件小工具的調適型表單，預覽附加檔案後，表單的某些部分會被停用。\
   NPR：16611

* 針對允許多個附件的檔案附件小工具，如果在具有先前附件的小工具上提交帶有附件的新表單例項，則開啟新增的附件時，會顯示錯誤代碼而不是實際內容。NPR-16258
* 保護表單預填服務不會因 `file://`、`http://` 和 `ftp://` 等通訊協定而遭到未經授權的存取。請參閱「[使用 Configuration Manager 設定預填服務](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)」。NPR-15414

* 請求在驗證步驟中以 PDF 格式 (而非 HTML) 來轉譯調適型表單，並將所有附件附加至 PDF，以便讓列印成品顯示完整的表單。NPR-9011

**通信管理**

* 在「預覽/編輯」模式下處理信函中的文字片段時，如果將文字轉換為清單，便會中斷整個信函功能，並產生 JavaScript 錯誤。NPR-16460
* 每次上傳 XSD 並選取根節點時，瀏覽器會停止回應，導致匯入 XSD 檔案以在通信管理節點中建立資料字典失敗。此問題與瀏覽器無關，不會出現在伺服器記錄中。NPR-16452
* 使用 Internet Explorer 瀏覽器預覽信函並嘗試編輯內容的字型大小時，字型大小下拉式清單中會顯示 8 到 72 的重複值。NPR-16387
* 如果浮動欄位顯示為來自 XDP 片段的輸入欄位，則使用 Internet Explorer 瀏覽器時，欄位不會在信函預覽中展開。NPR-16367
* 嘗試從預覽直接提交信函時，由於信函名稱的快顯畫面隱藏，因此無法正常顯示。NPR-16353
* 編輯信函時新增的行距不會反映在「預覽」視窗中。針對文字片段中的清單，PDF 輸出不會顯示正確的間距。NPR-16267
* 使用 Internet Explorer 瀏覽器處理文字文件片段時，由於游標不允許文字縮排，因此嘗試為文字提供縮排失敗。NPR-16128
* 將資料字典新增或修改至現有文字文件片段需花很長時間，而且使用者不一定會收到通知。NPR-16102
* 使用 Internet Explorer 瀏覽器預覽具有可捲動內容的信函時，瀏覽器捲軸與信函的捲軸重疊，而且無法檢視右側片段的完整內容。NPR-16068
* 使用 Google Chrome 瀏覽器建立或編輯文字文件片段時，顏色選取下拉式清單會自動彈出，而且無法移除。使用者需要選取清單作為資料項目類型才能編輯片段。NPR-16067
* 使用 Letterinstance API 時，`import com.adobe.icc.services.api.LetterInstanceService` 方法無法運作。NPR-16008
* 在「資產撰寫器設定」中將日期顯示格式變更為 `locale=en_US; dateFormat=MMM dd,yyyy;` 時無法如預期運作，且日期格式會顯示為無用字元。NPR-16007
* 即使先前設定的類型不同，重新製作時「資料連結」類型仍會顯示為「使用者」。NPR-16619

**表單入口網站**

* 草稿和提交元件的升級情況不適用於資料庫範例實作。NPR：16752

**條碼式表單服務 (BCF)**

* 條碼式表單服務 (BCF) 的靜態程式碼分析報告了問題。NPR-13855

#### Forms JEE 安裝程式{#forms-jee-installer-17}

**處理程序管理 - HTML 工作區**

* 保護表單預填服務不會因「file://」、「http://」和「ftp://」等通訊協定而遭到未經授權的存取。如需詳細資訊[「使用 Configuration Manager 設定預填服務」](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)。NPR-15434

**使用者管理 **

* AEM 6.2 伺服器上的 SAML 登入畫面會顯示不適用的版本 (6.1.0)。NPR-13825
* 在 AEM Forms 設定為「單一登入」(Kerberos) 驗證時，如果使用者在嘗試登入時驗證失敗，則會傳回錯誤代碼「404」。只有重新整理頁面後才會將使用者重新導向至登入網站。NPR-15015

#### Forms Designer {#forms-designer-1}

* 在 AEM Forms Designer 中無法將「字典拼字檢查」的「表單地區設定」變更為「法文 (加拿大)」。\
   NPR-15896

### CFP3 包含的 Feature Pack {#feature-packs-included-in-cfp-2}

**Forms 附加套件**

* 在通信管理中刪除任何資產時，都應將警告訊息記錄在 error.log 檔案中。NPR-13225
* 增強在通信管理中預覽信函時的搜尋功能，以啟用搜尋文字片段內容中的文字，而不是只搜尋信函標題或標籤。NPR-16103

### CFP3 中包含的 OSGi 套件組合{#osgi-bundles-included-in-cfp-5}

AEM 6.2 SP1 和 CFP3 之間更新的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
Cumulative Fix Pack 2 的關鍵重點為：

* AEM 平台的穩定性修正和效能改善，包括 Sling 架構和作業在內
* 透過針對資產存取、移動、搜尋、上傳和發佈的多項修正改善資產管理
* 透過內容片段、錨點外掛程式、投影片放映和 Context 元件的修正，改善 Sites 的製作和管理功能
* 觸控式 UI 中的多項修正，包括文字編輯器、Omnisearch 和變量建立程序
* 改善翻譯工作流程；增強 Microsoft 連接器，可針對 Azure 入口網站使用新的翻譯 API
* 針對專案和促銷活動的修正
* 透過針對調適型表單、通信管理和表單入口網站功能的修正，改善製作和管理功能
* 針對 Forms JEE 核心、XTG 和 HTML 工作區元件的修正

### 平台 {#platform-14}

* 如果編輯了直接參考 Sling 架構的頁面，便會觸發 `SlingPostProcessor`。NPR-15754：CQ-104153 的 Hotfix

* 導覽至頁面元件時，如果值的標記具有 `tagBasePath` 屬性，傳統 UI 對話方塊中就不會擷取該值。NPR-15543：CQ-4199950 的 Hotfix

* 執行 Sling 作業時，如果有名為「chunk_n_n-1」的區塊，`SlingFileUpload handler.getLastChunk` 便會進入包含空區塊的無限迴圈中。NPR-15455：SLING-5701 的 Hotfix

* 有一個介面延伸另一介面時，超級介面上的可插入方法無法正確插入。NPR-15202：SLING- 5710 的 Hotfix
* 使用 `com.adobe.granite.infocollector.impl.FilesTraversal` 函數呼叫時，無法防止潛在的 Null 指標例外狀況。NPR-15169 CQ-4197640 的 Hotfix
* 某些次要節點的工作流狀態不一致，且在為該節點發送觀察事件時會顯示錯誤。NPR-15701：GRANITE-13786 的 Hotfix
* 當使用者在 CRXDE 中選取節點 (例如 /content/dam/)，然後選取「存取控制」索引標籤以確定「存取控制清單」存在時，若拖放某些元素，會移動所選元素以外的元素。NPR-15696 GRANITE-16300 的 Hotfix
* 嘗試進行模擬時若從下拉式清單中選取使用者，會導致整個使用者快顯視窗消失。NPR-15774：CQ-4201738/GRANITE-11895 的 Hotfix
* 在 Omnisearch 中，無法使用自動填入建議的標記來搜尋。NPR-15088：GRANITE-14426 的 Hotfix。\
   注意：此修正需要 Oak CFP 1.4.11 或更新版本。

### Mobile AEM Author {#mobile-aem-author}

* 將 AEM Mobile 和 ContentSync 套件與混合應用程式搭配使用時，AEM 會以最舊套件 (而非應用程式所請求的套件) 回應應用程式所提出的擷取請求 (含時間戳記)。NPR-15749：CQ-104153 的 Hotfix

### 網站 {#sites-17}

* 如果使用者在啟動工作流後修改頁面，WCM 核心中「工作流收件匣」的修改狀態不會變更。NPR-15684：CQ-4196974 的 Hotfix
* 使用者按一下錨點圖示並新增名稱時，觸控式 UI 的 RTF 編輯器中，錨點外掛程式會產生不相容的 HTML5。它應在錨點元素的 HTML5 標記中新增「id」屬性，而非「name」屬性。NPR-15650：CQ-89782 的 Hotfix
* 建立具有多個欄位的中繼資料結構並套用至內容片段中繼資料時，不會在內容片段中繼資料畫面中建立捲軸，導致無法編輯這些欄位。NPR-15478：CQ-4202622 的 Hotfix
* 編輯 `TagInput` 欄位元件不會針對對話方塊欄位顯示先前設定的值。NPR-15464：CQ-4200360 的 Hotfix

* 在內容片段編輯器 UI 中，建立許多內容片段變化時，側邊面板不會顯示用於導覽所有變化的捲軸。NPR-15445：CQ-4199444 的 Hotfix
* 將使用者從直接群組中移除時，會將其新增至繼承的群組。NPR-15400：CQ-98758 的 Hotfix
* WCM 製作：觸控式 UI 作者不允許編輯名稱中含有逗號的頁面。NPR-15396：CQ-4199723 的 Hotfix
* 使用觸控式 UI 進行製作時，函數 `Granite.author.editableHelper.doSelectParent` 會以錯誤的順序傳遞引數，引發 JavaScript 錯誤。NPR-15349：CQ-4198594 的 Hotfix
* 即使存在選擇退出 Cookie，ContextHub 區段仍會顯示體驗。NPR-15293：CQ-4198024 的 Hotfix
* 傳統 UI 中的投影片放映元件無法建立投影片，或透過拖放影像來建立新投影片。NPR-15281：CQ-4194164 的 Hotfix
* 不論使用者的權限為何，都會在「網站管理員」控制台中顯示「建立」選項，例如「建立頁面」、「建立網站」、「建立 Live Copy」、「建立啟動」和「建立目錄」功能表項目。NPR-15278：CQ-94436 的 Hotfix
* 安裝 AEM 6.2 Service Pack 1 後，「包含子頁面」滑桿就不能用於頁面啟動。NPR-15230：CQ-4198449 的 Hotfix
* 請求增強版本清除功能，以擷取和處理區塊中的版本，以及在 XPath 查詢中使用指定路徑的功能。NPR-15186：CQ-109205 的 Hotfix
* Sites 元件的「頁面屬性」縮圖索引標籤上缺少「清除」按鈕。NPR-15143 CQ-4196997 的 Hotfix
* 針對使用 Live Copy 的網站，在網站管理員控制台的「欄」窗格中選取「Live Copy」核取方塊時，無法正確顯示 Live Copy 狀態，只會顯示 HTML 標記。NPR-15108：CQ-97086 的 Hotfix
* 編輯內容片段時，如果使用者在收到貼文回應之前按下完成編輯 (「√」)，編輯過的內容便無法正確儲存。NPR-15014：CQ-4194095 的 Hotfix
* 處於「時間扭曲」模式期間，關閉「編輯」頁面並嘗試從網站管理員重新開啟該頁面時，會產生狀態「500」的錯誤，而非重新開啟頁面。NPR-14965：CQ-109647 的 Hotfix：
* 在數位資產管理器 (DAM) UI 中，「使用者選擇器尋找可授權項目」搜尋會造成「記憶體不足」例外情況。NPR：15307：CQ-98542 的 Hotfix

### 資產 {#assets-17}

* 在 Omnisearch 中搜尋資產後，選取資產並按一下「檢視屬性」以嘗試編輯屬性，然後按「儲存」按鈕時，會將使用者重新導向至空白頁面。NPR-15900：CQ-4202372 的 Hotfix
* Assets 使用者介面不會回應事件。選取資產並按一下「發佈」或「轉譯」時不會產生任何活動。NPR-15828：CQ-4202247 的 Hotfix
* 從卡片檢視發佈資產時，除非重新整理頁面，否則不會更新卡片以反映已發佈狀態。NPR-15826：CQ-102732 的 Hotfix
* 包含 Assets Hotfix 的累積 Hotfix。NPR-15225
* 如果資產資料夾的名稱包含 &amp; 字元，則導覽至資產時，資料夾名稱無法正確顯示。NPR-15775：CQ-4201735 的 Hotfix
* 在資產檔案名稱中使用 &amp; 字元會在存取其屬性時造成問題。NPR-15770：CQ-4201737 的 Hotfix
* 導覽 Assets 並使用「欄檢視」顯示模式時，如果使用者在選取並按一下資產後重新整理頁面，則會顯示資產詳細資訊，而非重新整理的內容。NPR-15768：CQ-4201727 的 Hotfix
* 由於 PDF 服務的程式庫堆積，PDS 擷取作業的 CPU 使用率高達 100%。NPR-15606：GRANITE-12929 的 Hotfix
* 使用 Firefox 瀏覽器存取「我的連結共用」UI 時，不會顯示共用項目或使用者，而且畫面無法使用。NPR-15539：CQ-4200992 的 Hotfix
* 使用數位資產管理器時，如果頁面與一組影像相關聯，將影像移至新資料夾時會中斷頁面關聯，而關聯的頁面會遺失部分影像。NPR-15538：CQ-111479 的 Hotfix
* 在 Dam Viewer 元件中，使用「nosamplecontent」執行模式時，會導致動態媒體發生錯誤。NPR-15449：CQ-4195425 的 Hotfix
* 建立視訊設定檔時，如果同時選擇高畫質和中畫質的視訊編碼預設集，就不會儲存所做的變更。NPR-15447：CQ-4195482 的 Hotfix
* 即使將資產上傳至 Brand Portal 已因伺服器錯誤回應而失敗，Brand Portal UI 上的狀態仍會更新為「已發佈」，因此難以追蹤遺漏的檔案。NPR-15442：CQ-4197968 的 Hotfix
* 若將資產資料夾發佈至 Brand Portal 時所費時間超過一小時，有些檔案會無法發佈。NPR-15441：CQ-4199493 的 Hotfix
* 在欄檢視中使用資產尋找器控制台時，嘗試建立資料夾會失敗一次，但重試時會成功。NPR-15370：CQ-4199448 的 Hotfix
* 如果 DAM UI 中選取的資產或資料夾名稱中有逗號，「參考」索引標籤就無法使用，且會顯示訊息「參考清單不適用於多個選取項目」。NPR-15362：CQ-4199721 的 Hotfix
* 將資料夾發佈至 Brand Portal 不會變更資料夾的已發佈狀態，即使資料夾下的資產已成功發佈亦然。NPR-15292：CQ-4197667 的 Hotfix
* 在觸控式 UI 中導覽至「資產」控制台時，啟用特定資產時會出現例外情況。NPR-15217：CQ-108779 的 Hotfix
* 透過 Proxy 伺服器連線時，視訊會發佈至 Youtube。NPR-15109：CQ-110332 的 Hotfix
* 使用 data-sly-resource 名稱包含點或句號 (.) 的資產時，不會解析為相同資產，而輸出路徑會在該點終止。NPR-15069：CQ-4195914 的 Hotfix
* AEM 6.2 升級至 Service Pack1 後，將資產同步至 Scene7 失敗。即使是已發佈的資產，dam:Scene7FileStatus 屬性也會顯示「`UploadFailed`」狀態。NPR-15269：CQ-4197708 的 Hotfix

### 使用者介面{#user-interface-5}

* 在&#x200B;**[!UICONTROL 觸控式 UI]** 中，使用 Internet Chrome 瀏覽器 56.0.2924.87 版時，針對沒有 type=&#39;datetime’ 的日期欄位，不會顯示儲存的日期。NPR-15383：Granite-16481 的 Hotfix
* 在&#x200B;**[!UICONTROL 觸控式 UI]** 中，RTF 編輯器會在轉譯 HTML 表格時，從 HTML 表格中移除執行緒和註解元素。NPR-15267：CRTE-41 的 Hotfix
* `FileUpload Validator` 不會處理 autostart 為 true 或手動呼叫了 `uploadFile()` 的情況，且會在這些情況下產生無效驗證報表。NPR-15295：GRANITE-13499 的 Hotfix

* Omnisearch 不允許使用 /apps 的客戶新增欄資料來源，因為它假設位置設定列在 */libs/granite/omnisearch/content/metadata/* 底下。NPR-13188 GRANITE-16479 的 Hotfix
* 使用&#x200B;**[!UICONTROL 觸控式 UI]** 時，不會在與產品相同的層級建立產品變體。系統不會通知使用者變體建立程序的狀態。NPR-15345：CQ-4198948 的 Hotfix

**Scene7**

* 執行 Scene7 工作流程會導致開啟的檔案無法關閉。請求改善 AEM-S7 服務，以維護和重複使用具有共用集區設定的單一 HttpClient 執行個體。NPR-15357：CQ-109958 的 Hotfix

### 轉換 {#translation-9}

* 使用翻譯專案時，從英文主版更新語言副本時，會產生 11 個獨立的啟動，所有啟動都具有相同的名稱和來源根，但如果頁面名稱遵循已設定的模式，啟動根會稍有不同。NPR-15605：CQ-4200699 的 Hotfix
* 語言根的名稱中包含連字號和破折號時，系統不會為頁面建立翻譯專案。NPR-15171：CQ-96286 的 Hotfix
* 請求更新 Microsoft 連接器，以便使用 Microsoft 在 Azure 入口網站中提供的 Microsoft Translator API。NPR-15320：CQ-101010 的 Hotfix

### 專案 {#projects-4}

* 「專案畫面」中只會顯示 20 個非作用中項目，但存放庫中有超過 20 個非作用中項目。NPR-15656：CQ-4200903 的 Hotfix

### 行銷活動 {#campaign-1}

* 使用「Campaign - 目標定位」和「MAC - 測試和 Target 整合」元件時，取消發佈活動時不會更新主 UI 中的活動狀態。NPR-15401：CQ-4199839 的 Hotfix
* 在 AEM Commerce 中移動產品時，產品移動精靈會遺漏產品名稱、標題、參考頁面、建立作者和建立日期的預填值。NPR-15228：CQ-98617 的 Hotfix

### 安全性 {#security-4}

* 使用 GET 方法將 CSRF 代號參數新增至表單。NPR-15229

### 表單 {#forms-18}

#### Forms 附加元件套件 {#forms-add-on-package-18}

`**Adaptive Forms**`

* 使用輸入 XML 預先填入調適型表單時，預設值會被 XML 中的空值覆寫。NPR-15721
* 即使預填 XML 的 XML 結構型調適型表單中沒有 `afData/afBoundData` 包裝函式，`afData/afBoundData` 包裝函式仍存在於已提交的 XML 中。NPR-15541

* 摺疊式功能表列中的標題應為可編輯的 HTML「h2」標題，而非「a」標記。NPR-15475
* 螢幕助讀程式使用者無法存取表單面板的摺疊式功能表版面。使用者若使用螢幕助讀程式軟體 (例如 JAWS 或 NVDA)，無法單獨透過鍵盤導覽至摺疊式功能表索引標籤。NPR-15474

`**Correspondence Management**`

* 儲存、刪除和設定文件片段的參考需花很長的時間。NPR-15939
* 「管理資產」中針對包含多個標頭的文字設定的索引標籤對齊方式，在 CCR UI 裡中斷。NPR-15818
* 雖然文字包含使用 Google Chrome 中的分頁建立的對齊內容，但文字模組的縮圖沒有顯示對齊內容。NPR-15819

`**Forms Portal**`

* 預填服務無法用於 XDP 表單。NPR-15466
* 將調適型表單草稿和提交項目儲存到資料庫時，資料庫連線若因任何原因 (例如長時間閒置) 而失敗，調適型表單的狀態會損毀。NPR-15297

#### Forms JEE 安裝程式{#forms-jee-installer-18}

`**Core**`

* 升級至最新版 Java 1.8.0_121-b13 後，無法在 AEM Forms 中存取管理員使用者介面。NPR-15330

`**XTG**`

* 使用輸出服務來合併特定表單與資料 XML 所需的回應時間，是 ES4 SP1 伺服器執行相同作業所花費的 20 倍。NPR-15283

#### AEM Forms 應用程式 {#aem-forms-app-1}

* 恢復未儲存的任務時，所顯示恢復未儲存任務的訊息需要更加清楚，以減少使用者錯誤。NPR-15377
* AEM Forms 應用程式不會轉譯從自訂範本建立的表單。NPR-15892
* 使用者無法登入 AEM Forms 應用程式。NPR-15891

AEM 6.2 SP2-CFP1 的關鍵重點為：

* 簡化 Sites 中的複寫功能：

   * 修正各種轉出、LiveCopy 和錯誤寫入問題

* 增強進行下列程序期間觸控式 UI 的回應能力：

   * 資產搜尋
   * 依大小排序

* 增強智慧型集合中的 Tag management
* 對資料夾執行 CRUD 作業期間進行更嚴格的存取控制

### 平台 {#previous}

* 請求在複寫代理啟動期間移除 `ReplicationQueue#forceRetry` API 呼叫，因為這類呼叫會顯著減慢執行個體的速度，尤其是執行個體具有多個複寫代理時。NPR-14032：GRANITE-13095 的 Hotfix
* 請求 `DurboImportConfigurationProviderService` OSGi 設定以支援可儲存陣列值的欄位。NPR-14570：CQ-108684 的 Hotfix
* 移轉至 AEM 6.2 後，在頁面中使用 Sightly 元件會導致頁面的「屬性」對話方塊停止運作。NPR-14328：CQ-108355 的 Hotfix
* 取消排程先前排程的工作時，不會刪除 */var/eventing/scheduled-jobs* 底下的對應節點。NPR-14253：SLING-5666 的 Hotfix
* 管理員嘗試模擬已刪除的使用者時，使用者介面無法重新整理。NPR-14247：CQ-107446 的 Hotfix
* XSS 防護檢查造成 Sightly 元件中的編碼錯誤。NPR-14004：CQ-93821 的 Hotfix
* 請求將 Jackrabbit Filevault 升級至 3.1.30 以解決多個問題。NPR-13454
* Sling 散發將散發套件從製作同步至發佈時，會發生快取錯誤。NPR-13034：GRANITE-13970 的 Hotfix

### 網站 {#sites-18}

* VersionManagerImpl 從版本歷史記錄中清除錯誤版本時發生問題。NPR-14372
* WCM Sightly Foundation parsys 元件會忽略元件聲明標記名稱 `cq:htmlTag / cq:tagName`。NPR-14225
* 在觸控式 UI 中使用 Sightly Parsys 來轉換透過 JavaScript 插入的元件時，重新整理頁面後會忽略自訂裝飾。NPR-14122
* 建立多個 RTF 欄位 (例如連結) 時，Target 下拉式清單無法在觸控式 UI 對話方塊中運作。NPR-13911
* 在對話方塊 (觸控式 UI) 中使用多個 RTF 編輯器 (RTE) 屬性編輯文字欄位時，焦點會隨機切換到特定的 RTE 屬性。NPR-13703
* 預設的現成視訊元件不會轉譯視訊縮圖。NPR-14976
* 在範本編輯器的「即時使用情況」索引標籤中，資訊載入速度緩慢。NPR-14880：CQ-83417 的 Hotfix
* 在 AEM 6.2 執行個體上安裝 Hotfix-10936 會停用 iparsys 元件。NPR-14330：CQ-106982 的 Hotfix
* 移轉至 AEM 6.1 SP1 後，出現多個轉出元件問題和一個 Live Copy 問題。NPR-15256
* 「頁面轉出」動作無法針對多個轉出設定建立超出第一層的子項。NPR-15055
* 從編輯器提交 PageProperties 對話方塊時，會重寫 LiveCopy 索引標籤中未變更的資料。NPR-14693
* 從編輯器提交 PageProperties 對話方塊時，MSM 後處理器會寫入請求中的一些參數，而不是 `msm:writeLiveCopyConfig` 參數。NPR-14434
* 與轉出元件、Live Copy 和 MSM 其他方面相關的多個問題。NPR-12235

### 資產 {#assets-18}

* 解除封裝工作流程無法處理影像檔案名稱中具有特殊字元的影像。NPR-15227：CQ-103887 的 Hotfix
* 無法正確顯示具有「條件式重複」運算式的資產。使用者預覽 `*CDN3835RLCEN*` 信函範本時，沒有顯示位於內文目標區域中的資產。若取消選取預先選取的選用資產 `*VIPReassement*`，那麼預先選取的其他資產會顯示在信函中。NPR-14844

* 建立智慧型集合期間，儲存智慧型集合時不會保留樣式標記。NPR-15081：CQ-4195494 的 Hotfix
* 多個使用者同時進行搜尋期間，觸控式 UI 中的資產搜尋查詢程序執行速度緩慢。NPR-15019：CQ-4195405 的 Hotifx
* 將原始資產重新上傳至不同位置時，為 `Long[]` 類型的屬性擷取的中繼資料會轉換為 `String[]` 類型。NPR-15016：CQ-4195005 的 Hotfix

* 使用者無法刪除已儲存的搜尋或智慧型集合。NPR-14924：CQ-108494 的 Hotfix
* 在基礎中繼資料結構的下拉式欄位中，為 TypeHint 使用布林值時，若大量編輯資產的中繼資料 (附加模式)，便會產生錯誤。NPR-14529：CQ-106876 的 Hotfix
* 沒有複寫權限的使用者無法刪除資產資料夾。NPR-14321：CQ-88271 的 Hotfix
* 嘗試在管道編輯器中編輯視訊的視訊設定檔時，設計對話方塊不會開啟，且會在錯誤記錄中記下「Null 指標例外狀況」。NPR-14144：CQ-81101 的 Hotfix
* 資產的屬性頁面中，所顯示系統產生的「已建立」時間戳記屬性不正確。NPR-13992：CQ-95029 的 Hotfix
* 請求在 AEM Assets NPR-13851 中為沒有讀取存取權的使用者啟用偵測重複資產的功能：CQ-102281 的 Hotfix
* 使用者無法從屬性頁面大量編輯資產的中繼資料。NPR-13721：CQ-100703 的 Hotfix
* 上傳重複資產時，傳統 UI 中出現不正確的錯誤訊息。錯誤訊息未指出上傳失敗的原因。NPR-13691：CQ-99272 的 Hotfix
* 資料夾中包含大量資產時，AEM Assets 無法在清單檢視中一次依大小排序超過 50 個資產。CQ-100588
* 如果資產/資料夾 URI 太長，選取多個資產會導致出現回應代碼 - 414 (請求-URI 過長) 錯誤。NPR-13516：CQ-76076 的 Hotfix
* 使用者在「設定欄」對話方塊中選取所有選項時，「Assets 報表」頁面會停止回應。NPR-13187：CQ-95589 的 Hotfix
* Safari 和 Internet Explorer 中的標記選取器出現非預期的行為。NPR-13134
* 從「Assets 管理員搜尋」邊欄編輯儲存的搜尋時，會將搜尋儲存為巢狀智慧型選取項目，這會造成環境穩定性問題。NPR-13119：CQ-99460 的 Hotfix
* 移動檔案 (或資料夾) 並重新命名後，「cq:name」中繼資料不會反映新的檔案名稱 (資料夾名稱)。NPR-13036：CQ-99141 的 Hotfix
* 無法從透過電子郵件共用的下載連結下載名稱包含特殊字元的資產。NPR-12872：CQ-95795 的 Hotfix
* 具有大量資產時產生的現成 Asset 報表，會造成嚴重的周遊情況，使搜尋不會比對到任何索引，且 CPU 使用量會達到尖峰。NPR-12811：CQ-84409 的 Hotfix
* AMS AEM Assets 製作執行個體上，從不同網路進行存取的使用者若沒有資料夾刪除權限，便無法使用區塊上傳功能來上傳資產。NPR-12768：CQ-82715 的 Hotfix
* 使用「資產搜尋」邊欄的標記式資產搜尋功能時，「預先輸入」功能不會限制為根路徑，且會顯示來自所有命名空間的標記。NPR-12666
* StaticRenditions 元件引發 Null 指標例外狀況。NPR-12665
* 請求停用 MissingMetadataNotificationJob，因為它會導致徽章通知 UI 出現執行階段例外狀況「無法掃描輸入」而中斷頁面。NPR-12500：CQ-93573 的 Hotfix
* 標記欄位的「停用編輯」選項無法在觸控式 UI 的資產屬性頁面中運作。NPR-12429：CQ-88835 的 Hotfix
* AEM Assets 6.2 中適用於 Companion App SMB 實作的 API 修正。NPR-11099
* 自從 Jquery 更新以來，使用者無法選取資產集合，以及在內容片段的「為內容建立關聯」面板中確認選取項目。NPR-14847：CQ-4194209 的反向移植
* 即使在用戶端叫用了無限排序，目前 UI 中仍只會顯示文章/橫幅/集合。NPR-14493：CQ-109926 的 Hotfix
* 請求為 AEM Mobile-on-demand 服務實作 Omnisearch 功能。對任何文章、集合或橫幅進行關鍵字搜尋都不會傳回任何相符項目。NPR-14093：CQ-101394 的 Hotfix
* 在對話方塊中使用 Coral-select 元件 (*granite/ui/components/coral/foundation/form/select*)時，若選取的值包含單一項目，Internet Explorer (IE11 或 Edge 瀏覽器) 中的值初始化作業無法正常運作。NPR-13395：CQ-101013 的 Hotfix

### 專案 {#projects-5}

* 將使用翻譯方法建立的翻譯專案匯出為「human」，並將翻譯提供者匯出為「none」時，因為缺少 GUID 對應檔案，故不會產生 translation_export_summary.xml 檔案。NPR-13137：CQ-91976 的 Hotfix
* 在 AEM 專案中，建立設有到期日屬性的專案時，由於伺服器和用戶端之間的時區差異，日期轉換會錯誤設定時間。NPR-13003：CQ-98288 的 Hotfix
* 更新翻譯專案時，翻譯工作中的「在網站中顯示」選項會不見。NPR-12966：CQ-93740 的 Hotfix
* 為匯出的網站頁面建立翻譯專案時，無法在預覽中正確轉譯。NPR-12964：CQ-84627 的 Hotfix

### 工作流程 {#workflow-3}

* 在工作流控制台的「封存」索引標籤中，按一下裝載連結時，會傳回一個回應代碼為「404」的錯誤。NPR-14993：CQ-4194977 的 Hotfix
* 使用 AEM 預設工作流程時，CQ Mailer 無法傳送電子郵件通知給遺漏單一成員電子郵件地址的群組。NPR-14804：CQ-91499 的 Hotfix 請求
* 改善觸控式 UI 中收件匣和通知徽章的效能。NPR-14145：CQ-101125 的 Hotfix
* 起始工作流程時，使用者無法從工作流程收件匣控制台預覽裝載。NPR-13226：CQ-100275 的 Hotfix
* 使用 SAML 驗證處理常式設定的「saml_request_path」Cookie 會顯示以額外「?」字元設定的 Cookie。此外，將 SAML 回應發佈回 AEM 時，AEM「saml_request_path」Cookie 會因為字元已編碼而傳回無效值。NPR-13517：GRANITE-11722 和 GRANITE-14414 的主動式 Hotfix

### 解決方案整合{#solution-integration}

* 將 AEM 6.2 與 Search&amp;Promote 整合後，如果使用者搜尋傳回橫幅的詞彙，搜尋功能就會停止回應。NPR-14549：CQ-109631 的 CFP

### 動態媒體 {#dynamic-media}

* 在 AEM 啟動的過程中建立和取消的許多 AEM-Scene7 Sling 工作，在進行複寫期間會記錄為封存工作。NPR-12835：CQ-86115 的 Hotfix

### 安全性 {#security-5}

* 請求解決 WCMDebug 篩選器中的輸入驗證問題。NPR-12444：CQ-94890 的 Hotfix 請求
* 主動請求更正使用建立啟動精靈時的 XSS 行為。\
   NPR-13062：CQ-99577 的 Hotfix 請求

#### Forms 附加元件套件 {#forms-add-on-package-19}

`Adaptive Forms`

* 使用調適型表單建立可重複的面板時，無法在執行時更新面板標題。NPR-15325
* 若已設定選項按鈕的預設值，在儲存或提交時選取預設值以外的值時，預填時不會顯示該值。NPR-15304
* 使用選項事件來以動態方式填入下拉式清單，以及提交所選項目的值時，Google Chrome 會顯示錯誤的行為。NPR-15198
* 使用調適型表單建立可重複的面板時，無法在執行時更新面板標題。NPR-15181
* 針對調適型表單使用編輯模式時，會發生 JavaScript 錯誤，例如「元件的處理常式無效」和「guidelib 未定義」。NPR-15112
* 重複面板中的延遲載入片段無法如預期運作。NPR-13916、NPR-14785

`Correspondence Management`

* 無法正確顯示設有 `'Repeat with condition'` 運算式的通信管理資產。NPR-14844
* 搜尋通信管理資產 (例如信函、文件片段或任何其他類型) 時，工具列中的「下載佇列」圖示會消失。NPR-14745
* 建立清單模組時，無法切換特定於資產的屬性 (例如可編輯、強制項目)。NPR-14689
* 若建立條件模組時沒有選取資料字典，運算式產生器公用程式中的「資料元素」面板會持續載入。NPR-14688
* 預覽信函時，使用者無法使用 Tab 空格來以表格格式對齊內容。NPR-14481
* 從使用者介面大量匯出通信管理資產時，AEM Forms 伺服器會產生不必要的記錄。NPR-15226
* 預覽信函時，對齊文字會以不同的字型顯示。NPR-15468

`**Forms Portal**`

* 提交來自入口網站提交的新草稿時，已提交表單的附件不會顯示在 Forms 入口網站中。NPR-13515

`**Forms Manager**`

* 在 *FormsandDocuments* 目錄中導覽期間，使用者複製任何資產然後導覽至其他資料夾時，不會顯示「貼上」按鈕。CQ-111327

#### Forms JEE 安裝程式 {#forms-jee-installer-19}

`Rights Management`

* 系統以無效的時間記錄使用者登入相關稽核事件。稽核事件的正確時間無法追蹤。NPR-13107
* Adobe Acrobat Reader 和 Microsoft Office 無法開啟受到延伸驗證保護的檔案。NPR-14482

`Process Management`

* 將 HTML 工作區中轉送的草稿任務傳回給初始使用者時，該任務不會顯示在初始使用者的佇列中。NPR-15178

`Assembler Service`

* AEM Forms 無法使用兩個以上的簽名來驗證 PDF/A-2b。NPR-14101

`XTG`

* 使用列表機手送紙匣來列印文件時，`GeneratePrintedOutput` 函數未啟用從右方手送紙匣取紙。NPR-14079

#### Forms Designer {#forms-designer-2}

* 使用者執行「表單地區設定」選為「法文 (加拿大)」的「拼字檢查」公用程式時，Forms Designer 會當機。NPR-13740
* 使用者為表單欄位選取計算事件或驗證事件，並將語言變更為 JavaScript，再於&#x200B;**[!UICONTROL 指令碼編輯器]**&#x200B;視窗中輸入 `this.` 時，Forms Designer 會當機。NPR-12974

### CFP1 包含的 Feature Pack {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms 附加套件)：

* 若調適型表單是從 XDP 檔案建立，協助工具的 Tab 鍵瀏覽順序不會遵循設定模式。NPR-12562

`Adaptive forms` (Forms 附加套件)：

* 調適型表單的規則產生器不提供角色型存取功能。無法追蹤作者所做的變更。NPR-12840

`Core` (Forms JEE 安裝程式)：

* 沒有為 Jboss+ 啟用核心跨來源資源共用 (CORS) 功能作為 servlet 篩選器。NPR-13050

## 透過 Software Distribution 下載 CFP 的指示 {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>針對 AEM Forms 客戶，必須先安裝任何 AEM Service Pack、Cumulative Service Pack 或 Feature Pack，才能安裝 AEM Forms 附加套件。

您可以直接從 Software Distribution 下載 CFP 套件或執行以下步驟：

1. 開啟 [Software Distribution](https://experience.adobe.com/downloads)。您需要 Adobe ID 才能登入 Software Distribution。
1. 點一下頁首功能表中的 **[!UICONTROL Adobe Experience Manager]**。
1. 點一下套件名稱，選取&#x200B;**[!UICONTROL 「接受 EULA 條款」]**，然後點一下&#x200B;**[!UICONTROL 「下載」]**。

## CFP 的安裝指示 {#installation-instructions-for-cfp}

本節逐一說明安裝 CFP 的要求和步驟。

### 安裝之前 {#before-you-install}

>[!NOTE]
>
>Adobe 提供的選用 Feature Pack 依存於發行版本和 Cumulative Fix Pack。若您已安裝任何 Feature Pack，請聯絡 [AEM 客戶服務團隊](https://helpx.adobe.com/marketing-cloud/contact-support.html)以驗證與這個適用 AEM 6.2 的 Cumulative Fix Pack 之間的相容性。

>[!NOTE]
>
>建議您在嘗試安裝之前，先對每個新安裝套件都執行驗證。安裝之前預先驗證程序會分析並報告所有發現的錯誤，並主動警告使用者出現這些錯誤、覆蓋、權限。
>
>如需驗證選項的說明文件，請前往 [https://docs.adobe.com/content/docs/zh-Hant/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/zh-Hant/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 是 CFP 的必備條件。如需安裝指示，請參閱 [AEM 6.2 Service Pack 1 發行說明](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。

* Cumulative Fix Pack 下載項目可於 [Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) (可直接從 AEM 執行個體存取) 取得。
* 針對使用 (RDBMK 或 MongoDB) 的叢集部署，CFP 套件可安裝在使用套件管理器的任何製作執行個體上。

* 安裝 Cumulative Fix Pack 之前，請務必拍攝快照或備份您的 AEM 執行個體。
* 不支援解除安裝 CFP。

### 透過 Software Distribution 安裝 CFP {#install-the-cfp-via-package-share}

執行以下步驟來在現有 AEM 6.2 SP1 執行個體上安裝 Cumulative Fix Pack：

1. 按一下 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) 連結即可下載套件。

1. 開啟[套件管理器](http://localhost:4502/crx/packmgr/index.jsp)，然後按一下&#x200B;**[!UICONTROL 「上傳套件」]**&#x200B;即可上傳套件。

1. 選取套件名稱並按一下&#x200B;**[!UICONTROL 「安裝」]**。

### 自動安裝 {#automatic-installation}

可藉由以下方式將 CFP 自動安裝至執行中的執行個體：

* 伺服器執行期間將套件置於 ../crx-quickstart/install 中。套件便會自動安裝。
* [從套件管理器使用 HTTP API](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) (請務必使用 `cmd=install&recursive=true`) 以安裝巢狀套件。

### 驗證安裝 {#validate-installation}

1. 產品資訊頁面 (/system/console/ productinfo) 現在應在「已安裝產品」下方顯示更新的版本字串「Adobe Experience Manager，6.2.0.SP1-CFP20 版」。
1. 在 OSGI 控制台 (使用 Web 控制台：/system/console/bundles) 中，所有 OSGI 套件組合均為「作用中」或「片段」。

>[!NOTE]
>
>成功安裝套件時，會顯示提供資訊的訊息，指出已成功安裝內容套件，例如「內容套件 AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 已成功安裝」。

>[!NOTE]
>
>自 AEM 6.2 SP1-CFP1 起，Jackrabbit FileVault 中大部分訊息的記錄層級已從「資訊」變更為「除錯」。若要取得 AEM 6.2 SP1-CFP1 或以上版本所安裝內容套件的安裝記錄，請為 `org.apache.jackrabbit.vault.packaging.impl` 啟用「除錯」記錄層級。

### 安裝 AEM Forms {#install-forms}

>[!NOTE]
>
>如果您沒有使用 AEM Forms，請略過本節。

#### 安裝 AEM Forms 附加元件 {#install-aem-forms-add-on}

>[!NOTE]
>
>(**JEE 版 AEM Forms**) 如需瞭解在 JEE 版 AEM Forms 上安裝 CFP 的程序，請參閱[在 AEM Forms JEE 上安裝 CFP](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee)。

1. 確認您已安裝 AEM 6.2 SP1 CFP 套件。
1. 下載適用於您作業系統的 [AEM Forms 發行版本](aem-forms-releases.md)所列出的對應 Forms 附加套件。
1. 依照[安裝 AEM Forms 附加元件套件](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html)中的說明安裝 Forms 附加元件套件。

#### 安裝 AEM Forms JEE 套件組合套件{#install-aem-forms-jee-bundles-package}

AEM Forms JEE 中的修正是透過單獨的安裝程式提供。如需更多有關在 JEE 版 AEM Forms 上安裝 CFP 的資訊，請參閱[在 AEM Forms JEE 上安裝 CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer 安裝程式 {#designer-installer}

1. 若要安裝更新，請執行 Designer6.2.0_&lt;語言>_Cumulative_QF.msp 檔案。
1. 在歡迎畫面中按一下&#x200B;**「更新」**。安裝程序隨即會開始。
1. 安裝完成後，請按一下&#x200B;**「完成」**。

## DTM、Analytics、Target、Search&amp;Promote 連線的使用者可設定逾時參數{#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

在 AEM Cumulative Fix Pack 6.2 SP1-CFP7 及更新版本中，已可針對上述所有連線設定連線逾時期間，詳細資訊如下：

| **連線** | **連線逾時*** | **通訊端逾時**** |
|---|---|---|
| DTM | 30000ms | 30000ms |
| 分析 | 30000ms | 30000ms |
| 目標 | 60000ms | 30000ms |
| Search&amp;Promote | 30000ms | 30000ms |

* **連線逾時*** - 建立連線前的逾時 (毫秒)。逾時值零會解譯為無限逾時。
* **通訊端逾時**** - 等待資料或兩個連續資料封包之間最長閒置時間的逾時 (毫秒)。

>[!NOTE]
>
>若使用 AEM Cumulative Fix Pack 6.2 SP1-CFP6 和更新版本，用於 Search&amp;Promote 整合的 OSGi 設定為 Apache HTTP 元件 Proxy 設定。不再使用 Day Commons HTTP Client 3.1 的 Proxy 設定。

## 在標記控制台中停用複寫狀態 (傳統 UI) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

如果您是使用 CFP3 或更新版本，請依照下列指示，在傳統 UI 的「標記」控制台中停用「複寫狀態」：

* 覆蓋 */apps* 中的&#x200B;*「/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js」*

* 在第 416 行後面新增 `replicationStateRequired`: &quot;false&quot;。

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## 最新的 Java 8 Update 131 擲回一個例外狀況 (NPR-21355){#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>這些組態設定供使用文件安全性的 AEM Forms 客戶專用。

CFP12.1 中包含 NPR-21355。若要安裝 CFP12.1 或更新版本，請執行下列程序，在 JBoss 應用程式伺服器上設定 NPR-21355。若您是在 Oracle WebLogic 或 IBM WebSpehere 應用程式伺服器上所執行的 AEM Forms 伺服器上安裝 CFP12.1，則無需進行額外設定。

1. 備份、刪除和建立新的 module.xml 檔案。檔案的預設位置為 [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. 開啟新建立的 module.xml 檔案以進行編輯。將下列程式碼新增至檔案中：

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. 為位於 [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ 的 jsafeFIPS.jar、jsafeJCEFIPS.jar 和 certjFIPS.jar 檔案建立備份，並從上述目錄中刪除檔案。

   請聯絡 [Adobe 支援](https://helpx.adobe.com/marketing-cloud/contact-support.html)以取得新的 JAR 檔案。將向 [Adobe 支援](https://helpx.adobe.com/marketing-cloud/contact-support.html)取得的 JAR 檔案放置於 [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (僅限 Windows) 修改 `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` 或 `domain.conf.bat` 設定檔：

   * 針對使用獨立設定的 JBoss 伺服器，請開啟 standalone.conf.bat 進行編輯。
   * 針對使用叢集設定的 JBoss 伺服器，請開啟 domain.conf.bat 進行編輯。

   在結尾處新增以下幾行並儲存檔案：

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. (僅限 Linux 作業系統) 修改 [AEM_Forms_Installation_directory]/jboss/standalone.conf 或 domain.conf 設定檔：

   * 針對使用獨立設定的 JBoss 伺服器，請開啟 standalone.conf 進行編輯。
   * 針對使用叢集設定的 JBoss 伺服器，請開啟 domain.conf 進行編輯。

   在結尾處新增以下幾行並儲存檔案：

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## NPR-19778 所需的配置設定 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778 屬於 CFP14 的一部分。

預設情況下，使用者認領任務時，不會重新整理其他使用者的共用佇列計數。為此，我們引入了一項新屬性。請依照下列步驟操作，在您的 AEM 執行個體上設定此屬性：

1. 前往「管理員 UI -> 服務 -> 工作區 -> 全域管理」。
1. 匯出全域設定。
1. 在下載的 XML 檔案中新增 `<client_tasksPollingInterval>10</client_tasksPollingInterval>` 標記。其中的 10 是以秒為單位的範例值。您可以視情況修改此值。
1. 儲存檔案。
1. 返回「管理員 UI -> 服務 -> 工作區 -> 全域管理」。
1. 在「匯入全域設定」區段中匯入該 xml 檔案。
1. 這時您可以登出系統並重新登入。
1. 系統會為工作區中的其他使用者開始重新整理共用佇列的計數。
1. 若要關閉輪詢，請將值變更為 0，然後再次匯入 XML 檔案。

## UI 變更 {#ui-changes}

* 針對 dc:title 屬性設為 String [] (多欄位) 的影像，在影像卡片上顯示標題的行為變更：在 UI 中，影像卡片上只會顯示最後變更的標題，不過所有標題都會儲存在 CRX 中。CQ-4217165 的 Hotfix

## 已知問題 {#known-issues}

* 從 CFP18 更新至 AEM 6.2SP1-CFP19 和 AEM 6.2SP1-CFP20 時，會將根重新導向變更為傳統 UI 歡迎頁面，而非 /sites.html/content。您可能必須使用 CRX Explorer 將 sling:target 屬性從 /welcome.html 修正為 /index.html。從 CFP17 或舊版更新時，沒有發現此問題。

安裝 AEM 6.2 SP1-CFPx 時，可能會發生下列暫時性錯誤。不過，不需要對這些錯誤採取解決措施，因為它們不會影響您的 AEM 執行個體，且安裝 CFP 後就會消失：

* 將 AEM 6.2SP1-CFP20 執行個體升級至 AEM 6.5 時，有些虛名 URL 可能無法運作，例如：

   * */projects.html*
   * */sites.html*

不過因應措施是在升級後重新啟動 AEM 執行個體。

* 開啟 Webconsole 元件詳細資訊頁面時，會收到 HTTP 500 內部伺服器錯誤。
* 由於存放庫重新啟動，而發生&#x200B;**建立元件例項**&#x200B;和&#x200B;**服務工廠傳回 null** 這類錯誤：

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] 由於無法繫結參考 profileManager，故無法建立元件例項
   * org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException：服務工廠傳回 null。(元件：com.day.cq.tagging.impl.TagGarbageCollector (1687)))

* 在 Mongo 和 DB2 中 CFP 安裝中發現的錯誤：**org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry：例外狀況：java.lang.NullPointerException**。安裝 CFP8 以上的 CFP 後，就不會發生此錯誤。
* (Adobe Granite 維護排程器更新任務)com.adobe.granite.maintenance.impl.TaskScheduler：針對 window granite:weekly 找不到名為 WorkflowPurgeTask 的維護任務
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* 在 AEM 6.2 SP1 (包含智慧標記功能套件) 上安裝 CFPx 時，先前新增的智慧標記資產的工作流程步驟會從 DAM 更新資產工作流程中刪除。

請參閱 ]AEM 6.2 SP1 中的已知問題[清單 (https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known Issues)。

## Uber Jar {#uber-jar}

適用於 6.2 SP1-CFP20 的 Uber Jar 可於 [Adobe Public Maven 存放庫](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/)取得。

若要在 Maven 專案中使用 Uber Jar，請在專案 POM 中納入以下相依性：

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-5}

下列文字記錄 CFP 中包含的 OSGI 套件組合和內容套件清單。

* [AEM 6.2 SP1-CFP20 中包含的 OSGi 套件組合清單](assets/do-not-localize/updated.txt)
* [AEM 6.2SP1-CFP20 中包含的內容套件清單](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 Hotfix 頁面](https://helpx.adobe.com/experience-manager/kb/aem62-available-hotfixes.html)
>* [AEM 6.2 SP1 發行說明](https://docs.adobe.com/content/docs/zh-Hant/aem/6-2/release-notes/sp1.html)
>* [AEM 6.2 發行說明](https://docs.adobe.com/docs/en/aem/6-2/release-notes.html)
>* [AEM 產品頁面](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.2 檔案](https://docs.adobe.com/content/docs/zh-Hant/aem/6-2.html)
>* [訂](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe)閱 [Adobe 優先產品更新](https://docs.adobe.com/content/help/zh-Hant/release-notes/experience-cloud/current.html)

