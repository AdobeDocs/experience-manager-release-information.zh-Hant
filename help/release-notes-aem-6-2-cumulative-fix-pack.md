---
title: AEM 6.2 Cumulative Fix Pack
description: 'null'
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '19954'
ht-degree: 1%

---


# AEM 6.2 Cumulative Fix Pack發行說明{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## 發行資訊{#release-information}

| **產品** | Adobe Experience Manager |
|---|---|
| **版本** | 6.2 |
| **發行** | [累積修補程式套件6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **先決條件** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **全面上市** | 2019年6月6日 |

### 累積修補程式套件{#cumulative-fix-pack}

Adobe推出單一傳送模型來發佈修正。 Adobe現在不會針對個別問題發佈Hotfix，而是每個月發行Cumulative Fix Pack(CFP)（必須經過品質檢查）。 CFP是整合式內容套件，可用於多項修正。 CFP主要包含錯誤修正，但也可能包含功能套件。 相較於個別的修補程式版本，它們有下列優點：

* 累積性（例如，CFP包含透過舊版CFP提供的修正）
* 提高品質保證
* 簡化安裝（使用者將CFP安裝為單一套件，除最新的Service Pack外，沒有相依性）

如需有關CFP和其他類型發行版本的詳細資訊，請參閱[維護髮行工具](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html)。

## 關於版本{#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20是AEM 6.2的最後一個Cumulative Fix Pack，是重要的更新，其中包含自[ AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)全面推出以來的重要客戶修正。

>[!CAUTION]
>
>在不驗證已安裝功能套件之間相容性的情況下套用CFP，可能會導致系統故障或遺失自訂組態，而這可能需要從備份還原才能解決。

>[!NOTE]
>
>* AEM Cumulative Fix Pack 6.2 SP1-CFP10隨附新的Sling `discovery-  api` bundle Johnzon 1.0.0。 此外，服務用戶sling-discovery在CRX儲存庫中為節點&#x200B;*/var/discovery*&#x200B;添加了「讀取」和「寫入」權限。
   >
   >
* 已新增apache commons **org.apache.commons/commons-email/1.5**&#x200B;的電子郵件套裝，取代&#x200B;**com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**。
   >
   >
* Adobe建議透過安裝資料夾為在AEM執行個體上擁有大量使用者的客戶部署CFP。

>



## 問題包括{#issues-included}

本節列出目前CFP中包含的所有問題和修補程式。

此外，此CFP還包含在[先前累積修補程式套件](#previous)中提供的修補程式。

### 整合{#integration}

* 支援多個促銷活動定位個人化改進。 NPR-29163:CQ-4264126的修補程式
* com.day.cq.personalization.impl.TeaserResourceEventHandler會進入無限循環，並導致發佈例項上的節點更新。 NPR-28561:CQ-4263096的修補程式

### DAM —— 常規{#dam-general}

* 無法在特定dam資料夾中顯示／隱藏非管理員使用者的複製按鈕。 NPR-29026:CQ-4265361的修補程式

### 弱點{#vulnerability}

* CSRF保護架構無法與AEM基礎表單搭配使用。 NPR-28612:GRANITE-22231的修補程式

### 表單 {#forms}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package}

>[!NOTE]
>
>對於AEM Forms客戶，在安裝任何AEM Service Pack、Cumulative Fix Pack或Feature Pack後，必須安裝AEM Forms附加套件。

>[!NOTE]
>
>AEM Forms附加套件有助於將表單功能與AEM Service Pack和Cumulative Fix Pack對齊。 因此，在安裝任何AEM Service Pack、Cumulative Fix Pack或Feature Pack後，必須安裝AEM Forms附加套件。

#### 適用性表單 {#adaptive-forms}

* iOS 12.1裝置的塗鴉元件可用性問題。 NPR- 29082:CQ-4261765的修補程式

#### Forms - Document Security {#forms-document-security}

* 使用PDF進階電子簽名(PAdES)驗證PDF中的所有簽名會引發InvalidOperationException。 NPR-27848:CQ-4244837的修補程式

#### 表單——通信{#forms-correspondence}

* 在將字母預覽為PDF時，位於主版頁面的文字欄位不會遵循從資料標籤或依指定資料連結所輸入的值。 NPR-29239:CQ-4266856的修補程式。

#### 表單——互動式通訊{#forms-interactive-communication}

* 新增撇號字元時，字母中預先填入的欄位會顯示為ASCII字元，而非一般字母。 NPR-28863:CQ-4262900的修補程式

### Forms JEE安裝程式{#forms-jee-installer}

* Forms JEE安裝程式中沒有新的AEM Forms修正。

## 舊版累積修補程式套件包含的修補程式和功能套件{#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### 累積修補程式套件19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19是重要的更新，其中包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已啟用對AEM 6.2的MS Translator API v3.0支援
* 成功安裝所有SP、CFP和HF的套件後，新增記錄訊息。

### 資產 {#assets}

* 如果缺少「編輯ACL」權限，則無法更名DAM資料夾。 NPR-27555:CQ-104652的修補程式
* 6.2.1 CFP 17及更新版本中的影像預設集編輯器工具不回應。 NPR-28147:CQ-4261041的修補程式

### 網站 {#sites}

* 「連結檢查程式」無法完成工作，而且會因沒有回應的連結而卡住。 NPR-27373:CQ-4256030的修補程式
* 區段檔案無法正確載入，因為有額外的根路徑會中斷區段的路徑。 NPR-28014:CQ-4260332的修補程式

### 整合{#integration-1}

* LiveCopy繼承取消無法在目標容器上正常運作。 NPR-28129:CQ-4259813的修補程式
* cq :actions不會考慮目標元件。 NPR-27616:CQ-4257497的修補程式

* 用於中斷繼承的表徵圖的顯示不連貫。 NPR-27671:CQ-4257779的修補程式

### Felix {#felix}

* 在AEM 6.2 SP1執行個體上安裝CFP 18後，Web主控台元件詳細資訊會因500而失敗。 NPR-28350:CQ-4261095的修補程式

### 轉換 {#translation}

* 將MS Translator升級至API v3.0後，在AEM 6.3中啟用MS Translator服務支援。NPR-28123:CQ-4259096的修補程式

### UI - Foundation {#ui-foundation}

* OOTB網站日曆顯示不正確的日期。 NPR-28392

### 花崗岩{#granite}

* 使用sling :basename的資源組合不會使字典失效。 NPR-27624

### 維護{#sustenance}

* 應將包管理器活動日誌提取到單獨的日誌檔案中。 NPR-27323:Granite-14866的修補程式
* 安裝完成時，將在error.log中顯示的標準化片語／措詞/log-line。 NPR-27835
* Granite套件外掛程式是挑選org.apache.sling.i18n較低版本的相依性。 CQ-4263245的修補程式
* 在安裝6.2SP1-CFP15之後的最新CFP時，會刪除com.adobe.cq.com.adobe.cq.ui.commons套裝。 CQ-4258808的修補程式

### 表單 {#forms-1}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-1}

#### 適用性表單 {#adaptive-forms-1}

* AEM表單的XML插入弱點。 NPR-27843:CQ-4257315的修補程式

### Forms JEE安裝程式{#forms-jee-installer-1}

* Forms JEE安裝程式中沒有新的AEM Forms修正。

### 包含{#osgi-bundles-and-content-packages-included}的OSGI組合和內容封裝

以下文字記錄CFP中OSGI組合和內容套件的清單。

AEM 6.2 SP1-CFP19隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/cfp19_osgi_bundles.txt)

AEM 6.2SP1-CFP19內容套件清單

[取得檔案](assets/do-not-localize/cfp19_content_packages.txt)

### 累積修補程式套件18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18是重要的更新，其中包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已新增DAM CommandLineProcess支援，以終止長期執行的程式。
* 修正ReplicationEventListener中的會話洩漏。
* 新增對核心頁面元件的重新導向支援。

### 資產 {#assets-1}

* Camera RAW程式在大量擷取期間會卡住，最終封鎖所有工作流程處理。 NPR-26990:NPR-23860的修補程式
* 下載功能透過資產下載servlet運用AEM Assets，讓匿名使用者下載所有資產。 NPR-27054, CQ-4254732的修補程式
* 特殊字元會在AEM的電子郵件範本主旨行中斷。 NPR-26470:CQ-4252368的修補程式

### 網站 {#sites-1}

* 由於ConfigPostProcessor類的行為不正確，暫停父映像會刪除cq :來自子頁面的LiveRelationship混合類型。 NPR-26745:CQ-4254163的修補程式
* 新增重新導向支援至核心頁面元件。 NPR-26576:CQ-110529的修補程式
* 將上下文中心移轉至jquery 3。 NPR-26956:CQ-4255472的修補程式
* 錨點輸入欄位會出現在對話方塊上的瀏覽器可見區段中，直到最大化為止。 NPR-26852:CQ-4255019的修補程式
* 複製在內容片段中插入不需要的&lt;br>文字的貼上。 NPR-26660:CRTE-151的修補程式
* 傳統網站管理員不會針對某些頁面在右窗格中呈現清單。 NPR-27247:CQ-4251621的修補程式
* （傳統UI）嘗試移動／重新命名頁面時，會產生「移動頁面時發生錯誤」錯誤。 NPR-27179:CQ-4235907的修補程式

### 整合{#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever會在整棵樹上走動，以收集可用的品牌。 NPR-27060:CQ-4255790的修補程式

### WCM —— 基礎元件{#wcm-foundation-components}

* Foundation清單元件的搜尋功能問題。 NPR-26817:CQ-4250324的修補程式

### 平台 {#platform}

* 由於特殊字元em dash,Publisher在清除快取時發生問題。 NPR-27199:CQ-4242790的修補程式

### 花崗岩{#granite-1}

* Package Validator不會驗證CFP/SP中包含的封裝。 NPR-26775:Granite-22825的修補程式

### 複寫 {#replication}

* ReplicationListener中的JCR會話洩漏。 NPR-27063:CQ-4232088的修補程式

### 表單 {#forms-2}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-2}

* Forms附加元件套件中沒有新的AEM Forms修正。

### Forms JEE安裝程式{#forms-jee-installer-2}

* Forms JEE安裝程式中沒有新的AEM Forms修正。

#### 包含{#osgi-bundles-and-content-packages-included-1}的OSGI組合和內容封裝

AEM 6.2 SP1-CFP18隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/62cfp18updated_bundles.txt)

AEM 6.2 SP1-CFP18內容套件清單

[取得檔案](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### 累積修補程式套件17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17是重要的更新，其中包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 新增對at-integration.js中無延伸功能網站URL的支援
* 已從S7雲端服務設定移除S7輪詢匯入工具。
* 變更觀眾檢視，以支援多租用戶實作的資料夾結構。
* 更新至jqueryui   clientlib v1.12.1。

### 資產 {#assets-2}

* 從資產UI啟動工作流程時，使用者必須擁有寫入／刪除／修改權限。 NPR-25688:CQ-4250140的修補程式
* 即使對於沒有「複製」權限的使用者，發佈和取消發佈按鈕仍然可見。 NPR-25094
* （工作流程）智慧型標籤資產工作流程不會透過AEM Proxy設定處理。 NPR-25915:CQ-4248202的修補程式
* 從S7雲端服務設定移除S7輪詢匯入工具。 NPR-25239:CQ-95236的修補程式

### 網站 {#sites-2}

* 從「編輯器」->「頁面資訊」開始的工作流程會在裝載中包含內容路徑。 NPR-26389:CQ-76804的修補程式
* （外部連結檢查器）無效的https連結會顯示為有效的連結。 NPR-25541:CQ-4201333的修補程式
* (Classic UI)在即時副本下建立獨立頁面時，頁面會建立為即時副本。 NPR-25610:CQ-4249801的修補程式
* 啟動頁面時，與Design Importer元件關聯的發佈資源問題。 NPR-25638:CQ-102532的修補程式
* RTE富格文本工具欄覆蓋選擇清單。 NPR-25165:CQ-4248948的修補程式
* 將contexthub移轉至jquery 3。 NPR-25059:Granite-19902的修補程式
* 對於嵌套的parsys元件，始終從多個可用元件中應用滿足設計的第一個（具有最少的嵌套路徑）。 如需詳細資訊，請參閱[設計路徑解析度](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html)。 NPR-25250:CQ-4246276的修補程式

### 整合{#integration-3}

* 使用OOTB定位整合，定位元件會轉譯整個頁面，而非空的定位元件。 NPR-25273:CQ-4248003的修補程式
* 在定位模式中中斷繼承仍會顯示元件為定位，而在編輯模式中繼承未中斷。 NPR-25324:CQ-4248162的修補程式
* 當在頁面上定義個人化並解決對象時，對應的體驗會以編輯模式顯示。 NPR-25731:CQ-4249465的修補程式
* 使用AEM搭配非預設的上下文路徑時，會出現錯誤的摘要URL。 NPR-25971:CQ-4250953的修補程式
* 使用Optout時產生空白。 NPR-25295:CQ-4246792的修補程式
* 在啟動頁面時，從作者環境刪除的體驗不會從發佈網站移除。 NPR-24869:CQ-4247832的修補程式

### DAM - DM客戶端{#dam-dm-client}

* (Chrome、Firefox)VideoPlayer會忽略啟用觸控功能的裝置上的滑鼠點按。 CQ-4247370的修補程式

### 平台 {#platform-1}

* 允許配置獲取／釋放包時的最大重試次數。 NPR-25328:Granite-22376的修補程式
* 發生複製錯誤時記錄錯誤。 NPR-25308:CQ-4249402的修補程式
* 將Forms AEM 6.2 Forms CFP8安裝至CFP14會導致Apache POI失敗。 NPR-25053:Granite-21771的修補程式

### 花崗岩{#granite-2}

* 使用者同步程式失敗，但出現OakConstraint0022例外。 NPR-25729:Oak-7428的修補程式

### 社群 {#communities}

* cq -social-as-provider套件不以mongo驅動程式3.x版開頭。 NPR-26271:CQ-4252710的修補程式

### UI - Foundation {#ui-foundation-1}

* 更新至jqueryui   clientlib v1.12.1。NPR-25090:Granite-21981、CQ-4248897的修補程式

* (Omnisearch):&#39;Title&#39;屬性易受站點中跨站點(XSS)指令碼攻擊。 NPR-24994:Granite-19933的修補程式

### 表單 {#forms-3}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-3}

#### 最適化表單{#adaptive-forms-2}

* 從最適化表單提交資料時，編碼錯誤。 NPR-25539

#### 表單——管理{#forms-management}

* 發佈頁面時，不相關的表單資產會報告為參考。 NPR-26167:CQ-4251004的修補程式

### Forms - JEE安裝程式{#forms-jee-installer-3}

#### Document Security {#document-security}

* 變數會填入為資料類型清單，子類型為字串，但我們會收到「無法強制物件」錯誤。 NPR-26194:CQ-4252287的修補程式
* 安裝6.2-SP1-CFP15後，無法存取浮水印組態。 NPR-26130:CQ-4250984的修補程式

### 包含{#osgi-bundles-and-content-packages-included-2}的OSGI組合和內容封裝

AEM 6.2 SP1-CFP17隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/62cfp17updated_bundles.txt)

AEM 6.2SP1-CFP17內容套件清單

[取得檔案](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### 累積修補程式套件16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16是重要的更新，其中包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已在Day CQ Mail Service中新增STARTTLS支援。
* 修正描述檔快顯中的ContextHub圖示對齊方式。
* 下拉式元件的show/hide功能中的修正。
* 升級至最新的Jackson 2.8.11版

### 資產 {#assets-3}

* 無法從清單視圖啟動工作流。 NPR-24393:CQ-4245788的修補程式
* (Firefox/Chrome)無法在「資產共用」頁面中下載資產。 NPR-24523:CQ-4224408的修補程式
* 已提高AEM中視訊預覽的預設品質。 NPR-24148:CQ-4244310的修補程式

### 整合{#integration-4}

* 當元件定位在發佈例項上時，在定位之前會出現閃爍的預設體驗。 NPR-23992:CQ-4242038的修補程式
* 在啟動頁面時，從作者環境刪除的體驗不會從發佈網站移除。 NPR-24869:CQ-4247832的修補程式

### 平台 {#platform-2}

* 從clientlib修補jQuery 1.12.4以包含安全性修正。 NPR-24129:Granite-20058的修補程式
* 已在Day CQ Mail Service中新增STARTTLS支援。 NPR-23941:CQ-4240397的修補程式
* 刪除預設的MERGE_PRESERVE aclHandling。 NPR-24593:Granite-21889的修補程式
* 當請求包含無效的查詢參數時，LineChecker無法將連結外部化。 NPR-24127:CQ-4241893的修補程式

### MSM {#msm}

* 針對跨網站指令碼攻擊(XSS)的主動式修補程式。 NPR-21893:CQ-4223385的修補程式
* MSM LiveRelationship:如果BlueprintConfig位於root，則有效RolovetConfig會出錯。 NPR-23999:CQ-4243000的修補程式

### 網站 {#sites-3}

* 在即時副本區域中建立新體驗時，必須中斷繼承才能進行設定。 NPR-24995, CQ-4248209的修補程式
* （觸控UI）在鎖定或解除鎖定頁面時，頂端工具列上的數個圖示會消失。 NPR-23954:CQ-4243345的修補程式
* 上下文中的欄位未正確對齊。 NPR-23958
* 在撰寫鎖定的分頁符時發佈動作。 NPR-23970:CQ-4243203的修補程式
* /etc/reports/中的OOTB報表無法正常運作，且無歷史資料圖表顯示。 NPR-20035:CQ-4220180的修補程式
* 在專案上啟動「請求啟動」工作流程時，啟動建立失敗。 NPR-24255:CQ-4245030的修補程式
* 在CFP10安裝後，電子郵件會忽略HTML標籤和屬性。 NPR-24287:CQ-4240028的修補程式
* TagPicker:標籤中繼資料結構標籤欄位中的標籤建議會查詢可標籤的節點，因此需要很長時間的載入。 NPR-24347:CQ-4244291的修補程式
* Salesforce整合無法與Proxy設定整合。 NPR-24418:CQ-4245300的修補程式
* (WCM)PageManager在建立修訂期間將「頁面」保留在「異常」上。 NPR-24565:CQ-4246203的修補程式
* 在套用CFP14後，「裝置模擬器」按鈕會從編輯和預覽模式消失。 NPR-24566:CQ-4247060的修補程式
* (Classic UI)在對話方塊中撰寫完整的標籤後，會顯示為空白。 NPR-24688, CQ-4246407的修補程式
* 無法在第一次嘗試時建立版本。 NPR-24774:CQ-4232176的修補程式
* /etc/reports/中的OOTB報表無法正常運作，且無歷史資料圖表顯示。 NPR-24138:CQ-4220180的修補程式

### 弱點{#vulnerability-1}

* Salesforce整合容易受到伺服器端偽造要求(SSRF)的影響。 NPR-24289:CQ-4245277的修補程式
* ReportingServicesProxyServlet中的伺服器端偽造要求(SSRF)弱點。 NPR-24657:CQ-4246880的修補程式

### 花崗岩{#granite-3}

* 中繼資料讀取作業不會終止。 NPR-24240:Granite-19866修補程式
* 將Jetty更新為9.4.11.v20180605以修正弱點。 NPR-25033:Granite-22120的修補程式

### WCM —— 基礎元件{#wcm-foundation-components-1}

* PageComparator在排序頁時拋出ClassCastException。 NPR-24123:CQ-4244048的修補程式
* 表單下拉式元件的顯示／隱藏功能無法如預期般運作。 NPR-24562:CQ-4222853的修補程式

### 使用者介面{#user-interface}

* 由於「管理搜尋」功能中有許多要求，所以會發現CPU使用率較高。 NPR-23588:Granite-21286的修補程式
* (Classic UI)元件會顯示預設值，即使關聯的表單資料模型服務設為空白欄位亦然。 NPR-21903:GRANITE-19744的修補程式
* 當沒有FormData可供請求時，會擲出多欄位NPE。 NPR-24513:Granite-21055的修補程式

## 表單 {#forms-4}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-4}

#### 核心 {#core}

* (OSGI)受Jackson資料系結安全性警報影響的AEM Forms OSGI。 NPR-24274:CQ-4230245的修補程式

#### Rights Management {#rights-management}

* 在安裝AEM 6.2 SP1-CFP14後，Apache POI失敗。 NPR-25054、NPR-25052:CQ-4245898、CQ-4244778的修補程式

#### HTML5 Forms {#html-forms}

* 資料不會在HTML預覽中預先填入多行欄位。 NPR-23357:CQ-4244212的修補程式
* 透過預設預覽預覽字母時，版面片段對應不會顯示，而在點按預覽按鈕時，版面片段對應會正確顯示。 NPR-22993:CQ-4237745的修補程式
* 套用「社交保全號碼」模式至範本時，文字欄位的HTML預覽問題。 NPR-23205

#### 適用性表單 {#adaptive-forms-3}

* 將AEM表單新增至parsys元件時發生「Guidelib is not defined」錯誤。 NPR-24269:CQ-4244546的修補程式

### Forms JEE安裝程式{#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Shell指令碼檔案中的窗口行尾導致LCM無法在UNIX中運行。 NPR-22958

### 包含{#osgi-bundles-and-content-packages-included-3}的OSGI組合和內容封裝

AEM 6.2 SP1-CFP16隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

AEM 6.2SP1-CFP16內容套件清單

[取得檔案](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### 累積修補程式套件15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15是重要的更新，其中包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* Foundation表中的主動式安全性修復，以維護設計一致性。
* 新增對typeHint的支援，可將值儲存為字串。
* 為表單預填服務提供增強的安全性
* 更新至最新的adobe-reader-extensions-dsc.jar檔案，以取得Reader Extension中的修正。
* 已調整驗證掛接，以考慮「:invalid」項目，以用於提升編號輸入。

### 資產 {#assets-4}

* 在Ptiff產生程式中，EmbedXMP資料一律設為「作用中」。 NPR-22776:CQ-4234498的修補程式
* 無法在「多值」欄位中設定多個預設值。 NPR-22900:CQ-4239000的修補程式
* （動態媒體）在選取「動態轉譯」核取方塊時，下載的zip檔案會產生原始TIFF影像，而零位元組檔案。 NPR-22410:CQ-4198471的修補程式
* （觸控UI）欄檢視中資產的預設上傳位置。 NPR-23475:CQ-4237057的修補程式

### 整合{#integration-5}

* 在「目標」模式中，作者可以修改從Blueprint繼承的元件，而不取消繼承。 NPR-22751:CQ-4237907的修補程式
* 路徑變數未正確編碼，導致非永久性跨網站指令碼(XSS)。 NPR-22851

### MSM {#msm-1}

* 在使用多個展開配置的LiveCopy的推出期間，如果根目錄下出現ResourceNameConflict，則展開流將終止，而不包括所有分支。 NPR-22842:CQ-4236188的修補程式

### 平台 {#platform-3}

* 在反向應用程式的一個請求中實施輪詢限制。 NPR-23351:Granite-21135的修補程式****
* 自訂記錄程式不會反映訊息模式變更。 NPR-23486:CQ-4241974的修補程式

### 網站 {#sites-4}

* 在富格文本編輯器的文本中建立帶有空格或其他特殊字元的文檔的連結不起作用。 NPR-22289:CQ-4224321的修補程式
* 以巨大值(10000000000)儲存區段，將提升值設為0，造成錯誤訊息。 NPR-22524:CQ-4237006的修補程式
* 無法在多欄位元件中按一下「新增項目」。 NPR-22552:CQ-4237404的修補程式
* 當區段有長標題時，水準捲軸不可見。 NPR-22615:CQ-4237001的修補程式
* 載入空對象會產生錯誤的JavaScript程式碼。 NPR-22974:CQ-4238734的修補程式
* 排程啟動或停用工作流程時，工作流程標題是強制性的，因此，自訂工作流程標題不會在時間軸中轉譯。 NPR-23121:CQ-4237552的修補程式
* 要求修正網站中Target區段的相關問題。 NPR-23128
* (Firefox)選定角色的複選框不正確。 NPR-23345
* 不同模式的標籤和表徵圖一起顯示。 NPR-23275
* 將元件從AEM 6.0移轉至AEM 6.2時，發生「無效的遞回選擇器值」錯誤。NPR-23503:CQ-4241258的修補程式

### 社群 {#communities-1}

* 由於群組的訊息失敗，網頁和郵件通知不會觸發。 NPR-23447:CQ-4242880的修補程式

### 轉換 {#translation-1}

* 在翻譯配置上設定「不翻譯」資產時，將建立資產語言副本。 NPR-22540:CQ-4237962的修補程式

### 使用者介面{#user-interface-1}

* 使用Omnisearch搭配連字型大小查詢會傳回伺服器錯誤。 NPR-22999:Granite-19674的修補程式
* DatePicker不支援手動設定由隱藏欄位設定的外部類型提示。 變更文字提示會產生轉換錯誤。 NPR-23333:Granite-21194的修補程式

### WCM —— 基礎元件{#wcm-foundation-components-2}

* CAPTCHA元件已停用以提高安全性，如果您使用CAPTCHA元件，則會傳送訊息「Captcha元件已停用，不應再使用」。 將在安裝6.2 SP2-CFP15或更新版本後顯示。 AEM元件可自訂為包含reCAPTCHA，以提高安全性NPR-22151:CQ-4220052的修補程式
* WCM Foundation元件「表」易受儲存跨站點指令碼的攻擊。 NPR-23206:CQ-4240760的修補程式

### 弱點{#vulnerability-2}

* 管理UI專案連結中的跨網站指令碼(XSS)。 NPR-23272:CQ-4241795的修補程式

## 表單 {#forms-5}

### Forms add-on package {#forms-add-on-package-5}

#### 通信管理{#correspondence-management}

* 透過預設預覽預覽字母時，版面片段對應不會顯示，而在點按預覽按鈕時，版面片段對應會正確顯示。 NPR-23335:CQ-4237745的修補程式
* 與XDP中定義的系結對應的字母中的資料，不會在使用直接字母URL時填入。 NPR-24145:CQ-4244290的修補程式

#### 行動表單{#mobile-forms}

* （對應管理）使用目標XML載入信函時，資料未對齊。 NPR-22993:CQ-4237663的修補程式

#### Reader Extensions Service {#reader-extensions-service}

* 無法在Adobe PDF上套用Reader擴充功能。 NPR-23067

#### Forms Manager {#forms-manager}

* 重新發佈網站頁面時，不會發佈內嵌在網站中的表單。 NPR-23014:CQ-4236566的修補程式

#### 弱點{#vulnerability-3}

* 跨網站指令碼的主動式修補程式。 NPR-20624:CQ-4206055的修補程式
* Forms Manager的「附註」標籤中儲存的跨網站指令碼(XSS)弱點。 NPR-27157:CQ-4255556的修補程式

#### 加密服務{#encryption-service}

* (OSGI)[JEE]使用「驗證PDF程式」驗證附件時，PDF的簽名狀態不正確。 NPR-23269、NPR-23737

### Forms JEE安裝程式{#forms-jee-installer-5}

#### 核心 {#core-1}

* 核心分機靜態代碼分析中所報告的問題應該修正。 NPR-13947

#### PDFG服務{#pdfg-service}

* HTML至PDF轉換器無法運作。 NPR-21545

### 包含{#osgi-bundles-and-content-packages-included-4}的OSGI組合和內容封裝

以下文字記錄CFP中OSGI組合和內容套件的清單。

AEM 6.2 SP1-CFP15隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6_2cfp15updated_bundles.txt)

AEM 6.2SP1-CFP15內容套件清單

[取得檔案](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### 累積修補程式套件14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已改善資產中繼資料屬性的可編輯性。
* 已重新設定已處於過期狀態的資產的密碼過期通知工作。
* 自訂的Touch UI主控台，以擴充其他地區設定。
* 更新cq-msm-core，以有效同步Livecopyindex。
* 簡化了各種推廣的複製功能。

### 資產 {#assets-5}

* 使用者無法下載包含免責聲明和長檔案名稱的資產。 NPR-22163:CQ-4235274的修補程式
* 當您使用快速工具列動作開啟資產的屬性時，單引號字元可防止在Bulkview中更新中繼資料，而且UI會完全中斷。 NPR-22317、NPR-22353:CQ-4236990、CQ-4236469的修補程式
* 「資產到期通知」工作不會停用過期的資產。 NPR-22346:CQ-4237188的修補程式
* 在Safari的Assets中使用Digital Rights Management時，資產下載失敗。 NPR-22378:CQ-4236460的修補程式
* 適用於小型影像的網頁轉譯，像素大小不正確。 NPR-22435:CQ-4236742的修補程式

### 網站 {#sites-5}

* (Touch UI)移動的標籤會顯示在頁面屬性的新舊位置。 NPR-21921, CQ-4238598的修補程式
* (Touch UI)Rich Text Editor會從&lt;a>標籤中移除除id以外的所有屬性。 NPR-22045:CQ-4234133的修補程式
* 使用CTRL+V直接在Rich Text Editor中貼上內容會跳過分行符號。 NPR-22117:CUI-5881的修補程式
* (Touch UI)無法在namespace下顯示超過40個標籤。 NPR-22290:CQ-99114的修補程式
* RSS Feed期刊，埠-1到AEM 6.2 NPR-22158:CQ-4233339的修補程式
* (IE)首次在「豐富文字」欄位中編寫任何字元時，會新增尾隨空格至字元。 NPR-22443:CQ-4235343的修補程式
* 嘗試比對套件名稱時，Java Use物件會因為套件宣告中的尾隨空格字元而凍結SightlyJavaCompilerService。 NPR-22557:Granite-20836的修補程式
* Touch UI主控台不會取得新的標籤語言。 NPR-22250:CQ-4239194的修補程式

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite)「出版物日期」和「封面日期」都是對開本上傳至DPS之前，必須先為對開本設定欄位。 NPR-22484

### 商務 {#commerce}

* 商務建立型錄精靈中有多項跨網站指令碼(XSS)弱點。 NPR-22344:CQ-4237017的修補程式

### MSM {#msm-2}

* LiveCopyIndex同步會導致長索引更新期間線程擁塞。 NPR-22214:CQ-90667的修補程式
* cq:cugEnabled屬性會在編輯livecopy中的其他欄位時停用，因此會使頁面不受保護。 NPR-22246:CQ-4236050的修補程式
* 當頁面暫停時，「頁面展開」動作無法更新子系。 NPR-22483:CQ-4236956的修補程式
* 在主版中移動的結構的轉出會導致錯誤cq:moveTarget。 NPR-22373:CQ-4232536的修補程式

### 整合{#integration-6}

* 嘗試排序選件選擇器程式庫中的選件，會導致行為不穩定。 NPR-22208:CQ-4235439的修補程式
* TargetContentImpl會在長時間執行的查詢期間，讓AEM變得呆滯。 NPR-22361:CQ-4236907的修補程式
* 目標引擎(mbox.js, at.js)不使用損毀的URL，並使用包含冒號的URL，因為某些部署可能會失敗。 NPR-22366:CQ-4237854的修補程式
* 頁面個人化需要直接在品牌節點上發佈。 NPR-22370:CQ-4236895的修補程式

### 基礎{#foundation}

* Apache Sling Scripting Sightly Models使用Provider bundle **org.apache.sling.scripting.sightly.models.provider/1.0.18**。 NPR-22614:Hotfix for Sling-5944、Sling-6866

### 專案 {#projects}

* Workflow Starter無法接受String的TypeHint值。 NPR-22436:CQ-4237855的修補程式

### 轉換 {#translation-2}

* 調查「預覽」功能的問題。 NPR-22201:CQ-4223753的修補程式

### 使用者介面{#user-interface-2}

* (Classic UI)元件會顯示預設值，即使關聯的表單資料模型服務設為空白欄位亦然。 NPR-21903:GRANITE-19744的修補程式

### WCM —— 基礎元件{#wcm-foundation-components-3}

* 發佈指向Adobe促銷活動中匯入工具頁面的即時副本頁面時發生錯誤。 NPR-22470:CQ-4237164的修補程式
* 開啟「體驗片段編輯器」時發生JavaScript錯誤。 NPR-22598:CQ-4238415的修補程式

### 工作流程 {#workflow}

* Day CQ Workflow Email Notification Service會針對WorkflowCompleted和WorkflowAborted通知，在每個Mongo節點觸發一封電子郵件。 NPR-22486:CQ-4238172的修補程式

## 表單 {#forms-6}

### Forms add-on package {#forms-add-on-package-6}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

#### 適用性表單 {#adaptive-forms-4}

* IE11和Chrome中「最適化表單」中下拉式預留位置值的不一致。 NPR-22405:CQ-4227096的修補程式

### Forms JEE安裝程式{#forms-jee-installer-6}

#### 安裝LCM {#install-lcm}

* 在安裝程式和LCM中將Jsafe Jar更新至Cryptoj 6.1.3.1。 NPR-22744

### 包含的功能套件{#feature-packs-included}

#### 流程管理{#process-management}

* （HTML工作區）當使用者要求工作時，會重新整理該特定使用者的佇列計數，但不會重新整理頁面給其他使用者。 NPR-19778:CQ-4233665的修補程式

### CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}隨附的OSGI組合和內容封裝

AEM 6.2 SP1-CFP14隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6_2cfp14updated_bundles.txt)

AEM 6.2SP1-CFP14內容套件清單

[取得](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
FileAEM Cumulative Fix Pack 6.2 SP1-CFP13是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 使用AT.js做為用戶端程式庫時，在「目標元件設定」內啟用「靜態參數」欄位設定。
* 下拉式元件的show/hide功能中的修正。
* 使用目標同步對象的修正。
* 增加「對應管理」的多功能性，以容納特殊字元。

### 資產 {#assets-6}

* 「版本清除」無法移除舊版資產。 NPR-21682:CQ-4212996的修補程式
* 不會持續重新排序可重新排序資料夾下的資料夾。 NPR-21964:CQ-4231761的修補程式

### 網站 {#sites-6}

* (TouchUI)(ClassicUI)HTL和核心元件中的多個跨網站指令碼(XSS)弱點。 NPR-21532:CQ-4232305和CQ-4232511的修補程式
* 在Internet Explorer 11中，在選取的文字上建立／格式化內容（例如指派／移除新的清單樣式）無法正常運作。 NPR-21533:CQ-4230689的修補程式
* (Safari)使用者無法在資產搜尋器面板中檢視所有資產。 NPR-21981:CQ-4213720的修補程式
* 時間彎曲會傳回「RecursionTooDeepException」錯誤，並且頁面亂碼，即使變更日期，也不會建立新版本。 NPR-21707:CQ-4199536的修補程式
* 在編輯器中載入頁面時，WorkflowStatusprovider(pageinfo.json)會被載入三次，導致AEM例項執行緩慢。 NPR-21778:CQ-59232的修補程式

### 整合{#integration-7}

* 在「製作Target」模式中建立「行動類型與瀏覽器」的觀眾無法在AEM中運作。 NPR-21676、NPR-21681:CQ-4232100的修補程式
* 在重新整理目標元件時的延遲較高時，可在元件完全重新整理之前新增另一個選件。 NPR-21744:CQ-4233158/CQ-4234293的修補程式
* 使用者無法在mbox呼叫中看到測試靜態參數值，當以AT.js作為雲端設定的用戶端程式庫進行測試時，就會看到這些值。 NPR-21930:CQ-4234520的修補程式

### 平台 {#platform-4}

* 當使用者或群組數目較多時，使用者同步的效能問題。 NPR-20431:CQ-4223282的修補程式
* 使用者未與使用Sling Distribution的使用者同步同步。 NPR-21911:Granite-20404的修補程式
* 防止搜尋節選中反白顯示停止字詞（在Geometrixx頁面上）。 NPR-21835:Granite-21067的修補程式\
   注意：此修正需要Oak CFP 1.4.20或更新版本。

### 轉換 {#translation-3}

* 在建立翻譯項目時，Initiator用戶ID缺少jcr屬性。 NPR-21715:CQ-4230713的修補程式

### WCM —— 基礎元件{#wcm-foundation-components-4}

* 表單下拉式元件的顯示／隱藏功能無法如預期般運作。 NPR-22164:CQ-4235288的修補程式

## 表單 {#forms-7}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

### Forms add-on package {#forms-add-on-package-7}

#### 適用性表單 {#adaptive-forms-5}

* 自適應表單中的XML外部實體插入(XXE)。 NPR-21982:CQ-109878的修補程式
* (iOS11)按一下檔案附件元件時，檔案附件會開啟相機，而非裝置檔案瀏覽器。 NPR-21926:CQ-4214348的修補程式
* 主題建立UI中遺失標題會導致對話方塊發生異常，而且無法轉譯。 CQ-4236143的修補程式

#### 通信管理{#correspondence-management-1}

* 使用包含特殊字元的xml資料演算問題。 NPR-21712:CQ-4229137的修補程式

### Forms JEE安裝程式{#forms-jee-installer-7}

#### 匯編器服務{#assembler-service}

* 使用6.2.0-ASM-1017-003生成的PDF檔案已中斷。 NPR-21427:CQ-4228046的修補程式

#### PDFG服務{#pdfg-service-1}

* PNG、JPEG和TIFF檔案的OCR失敗，因為頁面大小(PDF)未預期。 NPR-19489:CQ-4209079的修補程式

## CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}隨附的OSGI組合和內容封裝

AEM 6.2 SP1-CFP13隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/cfp13_bundlecompare-list.txt)

AEM 6.2SP1-CFP13內容套件清單

[取得檔案](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 改善多值欄位的中繼資料處理。
* 支援翻譯工作流程中的多字元（兩個以上）國家代碼。
* 已改善使用多個巢狀元件的頁面演算。
* 已改善AEM和Adobe Digital Publishing Suite之間資產發佈日期的同步化。

### 資產 {#assets-7}

* OmniSearch中的字元過多會導致AEM伺服器當機。 NPR-21083:CQ-4223602的修補程式
* 在中繼資料結構的「多值」欄位中，在第二個選項中指定的值不會附加至CRX-de中先前指定的值。 NPR-21220:CQ-4224526的修補程式
* 在Safari的Assets中使用Digital Rights Management時，資產下載失敗。 NPR-21387:CQ-4230287的修補程式

### 網站 {#sites-7}

* (DAM)(ClassicUI)AEM CQ Author/Publish quickstart中某些SWF檔案中的多個跨網站指令碼(XSS)弱點。 NPR-21073、NPR-21074:NPR-20612的修補程式
* 標籤選擇器不會翻譯多種語言的標籤。NPR-21221:CQ-78855的修補程式
* 使用多個巢狀元件時，AEM文章主控台的轉譯問題會使它變慢。 NPR-21271:CQ-4224158的修補程式

### 整合{#integration-8}

* 新增Target架構時，編輯器的「選取模式」清單中無法使用定位模式。 NPR-21047

### 隨選行動裝置{#mobile-on-demand-1}

* (Digital Publishing Suite)AEM中對開本的出版日期與Folio Producer中顯示的日期不符。 NPR-21145

### MSM {#msm-3}

* 刪除LC中的第一個本地頁後，即時複製重置進程將停止。 NPR-21276:CQ-4229743的修補程式

### 平台 {#platform-5}

* 在升級至AEM 6.3後，找不到參照以指令碼實作之標籤的自訂標籤庫。NPR-20149:Granite-18433的修補程式

### 轉換 {#translation-4}

* 翻譯工作流程失敗，但長度超過2個字元的lang_country代碼。 NPR-21088:CQ-4197439的修補程式
* 在項目完成之前，不應再將資產頁面提交到翻譯項目。 NPR-21219:CQ-4209908的修補程式

### 使用者介面{#user-interface-3}

* 在提交表單期間，選擇元件不會刪除目標屬性。 NPR-21163:GRANITE-14125的修補程式
* HTTP.encodePathOfURI展開時會對加號&#39;+&#39;進行雙重編碼。 NPR-21417:GRANITE-16340的修補程式

### 弱點{#vulnerability-4}

* DAM中繼資料編輯器中的跨網站指令碼(XSS)。 NPR-21434:CQ-83472的修補程式
* 多個SWF檔案容易受到跨網站指令碼(XSS)的攻擊。 NPR-20612:CQ-4213297的修補程式

## 表單 {#forms-8}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

### Forms add-on package {#forms-add-on-package-8}

#### 通信管理{#correspondence-management-2}

* (IE11)HTML內容的初始演算只會在左側進行，而右側會在載入完成UI後間歇性載入。 NPR-21554
* 在安裝AEM 6.2 SP1-CFP9後，會停用字母預覽提交按鈕。 NPR-21547
* 在選擇「資產連結類型」時，「資產選擇器」視窗不會在「編輯字母資料系結」精靈中開啟。 NPR-21164:CQ-4194567的修補程式
* 若要編輯內嵌或可編輯的文字模組，請點選相關的「編輯」圖示，或在字母預覽中連按兩下相關的文字模組。 NPR-21402

#### 適用性表單 {#adaptive-forms-6}

* AEM Forms submit按鈕元件會顯示type=&quot;button&quot;，而非type=&quot;submit&quot;。 NPR-21007
* 為可重複面板新增或刪除新面板時，資料會維持持續性。 NPR-21408

### Forms JEE安裝程式{#forms-jee-installer-8}

#### 核心 {#core-2}

* 升級至最新的Java 8更新131會引發例外：&quot;JsafeJCE提供程式已禁用，FIPS 140要求的自我完整性檢查失敗&quot;。 NPR-21355

   **注意：** 此NPR需要其他設定，如需詳細資訊，請參 [閱最新Java 8更新](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr)。

* 在核心、加密、簽名和檔案安全性中，將jsafe jar更新為cryptoj 6.1.3.1。 NPR-21360、NPR-21361、NPR-21356、NPR-21358

#### 安裝LCM {#install-lcm-1}

* 在安裝程式與LCM中將Jsafe Jar更新至Cryptoj 6.1.3.1。 NPR-21362

#### PDFG服務{#pdfg-service-2}

* 在PDFG中將Jsafe Jar更新為Cryptoj 6.1.3.1。 NPR-21359

#### 流程管理{#process-management-1}

* （HTML工作區）啟用欄調整大小，使名稱類別不會出現截斷。 NPR-19770:CQ-4233668的修補程式

#### Reader Extensions Service {#reader-extensions-service-1}

* 在RE中將jsafe jar更新為cryptoj 6.1.3.1。 NPR-21357

## CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}隨附的OSGI組合和內容封裝

AEM 6.2 SP1-CFP12.1隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

AEM 6.2 SP1-CFP12.1內容套件清單

[取得檔案](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 更新cq-msm-core，以有效同步Livecopyindex。
* 改善內容片段的編輯效率。
* 在包管理器中提供用於檢測ACL權限的驗證選項。
* 引入Campaign的功能，可包含客戶通訊的電子郵件ID。
* 已改善動態媒體檔案的視訊編碼功能。
* Sightly元件和LiveCopys中的修正。

### 資產 {#assets-8}

* 動態媒體視訊編碼無法對名稱中包含空格的檔案進行編碼。 NPR-20818:CQ-102469的修補程式
* 在AEM CQ「作者／發佈快速入門」中的某些SWF檔案中，有多個跨網站指令碼(XSS)弱點。 NPR-21071、NPR-21072
* 使用者無法下載包含免責聲明和長檔案名稱的資產。 NPR-20255:CQ-4222139的修補程式

### 網站 {#sites-8}

* AEM和Campaign整合：在Adobe Campaign中會重寫特殊連結，使客戶無法傳送郵件至：超連結。 NPR-20787:CQ-4225760的修補程式
* (Touch UI)當語言設為法文時，AEM的可用性問題和效能問題。 NPR-20854:CQ-4227628的修補程式
* 在RTE中使用連結外掛程式連結編碼資產檔案會傳回空白連結。 NPR-20626、NPR-21059:CQ-4223011的修補程式
* 內容片段中繼資料編輯器會防止內容作者儲存內容片段的變更。 NPR-20641:CQ-4224755的修補程式
* 頁面屬性別名導致請求發佈／請求取消發佈。 NPR-20731:CQ-4226227的修補程式
* 文本元件與RTE元素中連結的編碼有關。 NPR-20755:CQ-4224321的修補程式

### 平台 {#platform-6}

* ResourceResolverImpl.map()不調用ResourceDecorator。 NPR-20788:GRANITE-19718的修補程式
* org.apache.sling.i18n.DefaultLocaleResolver無法透過org.apache.sling.engine.SlingRequestProcessor處理請求。 NPR-20706:CQ-94880的修補程式
* 請求在包管理器中添加驗證選項，以檢測是否對特定包更改了任何ACL權限。 CQ-4229196的修補程式

### 整合{#integration-9}

* (Search&amp;Promote)內容套件的不明確篩選定義會導致安裝時覆寫路徑。 NPR-20808:CQ-4227615的修補程式

### 工作流程 {#workflow-1}

* AEM生產伺服器部署的穩定性問題。 NPR-20979:Granite-19104的修補程式

### 專案 {#projects-1}

* (Touch UI)無法將團隊成員新增至專案。 NPR-20990:CQ-4205375的修補程式

### WCM-Foundation元件{#wcm-foundation-components-5}

* Sightly Image Component &#39;link to&#39;會因為缺少。html副檔名而產生403錯誤。 NPR-20823:CQ-4195909的修補程式
* 在使用LiveCopy的Blueprint網站上，嘗試刪除Form元件會擲回NullPointerException並新增Form元件，而非將其刪除。 NPR-20855:CQ-4204628的修補程式
* LiveCopyIndex同步會導致長索引更新期間線程擁塞。 NPR-20634:CQ-90667的修補程式

### 安全性 {#security}

* 主動式XSS程式庫更新。 NPR-21174
* 升級至Apache Commons Email 1.5，此為傳送電子郵件提供簡化的API。 NPR-20509:Granite-18240的修補程式
* 套用至Apache Sling XSS Protection API的安全性修補程式，以避免XSS略過的可能。 NPR-21290:GRANITE-19924的修補程式
* XSSAPI#getValidHref函式中的XSS略過。 NPR-21174:Granite-19924的修補程式

### 行動應用程式{#mobile-apps}

* 已修正AEM中OOTB資產的捲動標頭請求問題。 NPR-20511:CQ-4221520和CQ-103024的修補程式

## 表單 {#forms-9}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

AEM Forms的主要亮點是：

* 為Workbench使用者啟用憑證驗證。
* 「對應管理」、「HTML5表單」和「AEM表單」工作區的可用性修正。

### Forms add-on package {#forms-add-on-package-9}

#### HTML5 Forms {#html-forms-1}

* iOS 10和11裝置上塗鴉元件的可用性問題。 NPR- 21092

#### 通信管理{#correspondence-management-3}

* （對應UI）按一下後停用提交按鈕。 NPR-21078

### Forms JEE安裝程式{#forms-jee-installer-9}

#### 匯編器服務{#assembler-service-1}

* docConverter無法產生PDF/A，並出現錯誤&quot;stEvt:action&quot;元素的首碼&quot;stEvt&quot;未系結&quot;。 NPR-21032:CQ-4222540的修補程式
* 呼叫服務OMPFSubmission/PDFA/PDFAtoPDFA時，以java.lang.IllegalArgumentException訊息：No enum com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE引發例外。 這樣，在伺服器重新啟動之前，短期簽名驗證過程無法完成。 NPR-20792

#### 工作台{#workbench}

* 為Workbench使用者啟用憑證驗證。 NPR-17548:CQ-4214486的修補程式

#### 流程管理{#process-management-2}

* 準備資料處理會在使用資料區參數轉譯行動表單時多次叫用。 NPR-19801:CQ-4230427的修補程式：CQ-4230400

## CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}隨附的OSGI組合和內容封裝

AEM 6.2 SP1-CFP11隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

AEM 6.2 SP1-CFP11內容套件清單

[取得檔案](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已新增測試的onDialogLoaded公用程式函式。
* 已將前端單元測試和組態新增至ClientLibraryProxyServlet。
* 多影像就地編輯器元件中的效能修正。
* Apache Sling JCR ResourceBundleProvider中的設定更新。

### 資產 {#assets-9}

* 如果資產更新工作流程停用，資產預覽將無法運作。 NPR-20543:CQ-4204986的修補程式
* 花崗岩中新增類別的演算問題：class屬性(cq-damadmin-admin-assets-upload)。 NPR-20514:CQ-4219238的修補程式
* 標題中有特殊字元的縮圖資產會在NPR-20347的alt屬性中顯示java物件：CQ-4223620的修補程式
* 由於授權問題，將版本比較程式碼取代為Adobe專屬程式碼。 NPR-20273:CQ-4223758的修補程式
* 上傳具有多個Alpha圖層的CMYK PSB檔案時的處理問題。 NPR-20251:CQ-4220869的修補程式
* 除非在org.apache.sling.i18n 2.5.6中重新啟動伺服器，否則國際化字典無法運作。NPR-20525:Granite修補程式- 19490
* 沒有根據具有預設線程轉儲收集器配置（預設AEM啟動）的調度器期間生成線程轉儲。 NPR-20288:GRANITE-19488 / GRANITE-12741 / CQ-90647的修補程式。

### 網站 {#sites-9}

* 如果修改的日期篩選在開啟儲存的搜尋後變更，結果將不受影響，而顯示的結果與修改的日期篩選的先前儲存值相同。 NPR-19739:CQ-4219425的修補程式
* 含有巢狀元件的頁面無法載入。 NPR-20312
* 刪除工作流包時，將觸發刪除工作流請求。 NPR-20266:CQ-4221686的修補程式
* （觸控UI）「複製／貼上作業系統剪貼簿」和內部AEM剪貼簿的問題。 NPR-20228:CQ-4220383的修補程式
* 當載入多個資產（超過100個）時，清單檢視的AEM例項會變得呆滯。 NPR-20034:CQ-4222695的修補程式
* (Touch UI)透過Classic UI主控台刪除啟動，會讓所有頁面都無法編輯。 NPR-20520:CQ-4225074的修補程式
* Target下拉式清單無法在對話方塊中處理多個RTE元件。 NPR-20345:CQ-4220981的修補程式

### 平台 {#platform-7}

* 當使用匿名作業存取時，ClientLibraryProxyServlet不會在發佈例項上對用戶端程式庫提出代理要求，並拋出HTTP 404找不到錯誤。 NPR-20195:Granite-14409的修補程式

### 整合{#integration-10}

* 選取目標引擎作為Adobe Target可防止元件載入，並在伺服器記錄檔中引發錯誤。 NPR-20058:CQ-88071、CQ-109698、CQ-4201600的修補程式

### 商務 {#commerce-1}

* 建立相同頁面的產品時，不會顯示確認或重新導向彈出訊息。 NPR-20257:CQ-4223414的修補程式

### 使用者介面{#user-interface-4}

* 當「日期選擇器」是多欄位中的欄位時，編輯元件時，儲存在日期欄位中的值不會持續存在。 NPR-20077:GRANITE-19147的修補程式
* 如果連續查詢被觸發而導致錯誤結果，則先前的查詢不會中止。 NPR-20397:GRANITE-19306的修補程式

### WCM —— 基礎元件{#wcm-foundation-components-6}

* 即使從「多個就地影像」編輯器元件移除影像後，ImageMap屬性仍然存在。 NPR-20142:CQ-4222982的修補程式

## 表單 {#forms-10}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

### Forms add-on package {#forms-add-on-package-10}

#### 適用性表單 {#adaptive-forms-7}

* 值提交指令碼在通過UI更改時對DropDownList執行兩次。 NPR-19989:CQ-110212的修補程式

### Forms JEE安裝程式{#forms-jee-installer-10}

**流程管理**

* CFP套件包含AEM Forms HTML Workspace 2.2.26版。NPR-20099
* 將行動表單設定為PDF時，預先填入的表單無法運作。 NPR-20566

**Rights Management**

* 「CAC/共同驗證證書選擇」對話框應將具有增強密鑰使用(EKU)的證書顯示為客戶端驗證或智慧卡登錄。 NPR-20708
* Forms JEE支援PKCS#11相互驗證。 NPR-15001

## CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}隨附的OSGI組合和內容封裝

AEM CFP 6.2 SP1-CFP10隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/bundle-list-cfp10.txt)

AEM CFP 6.2 SP1-CFP10內容套件清單

[取得檔案](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已改變Analytics Classic UI設定，以進行機密輸入。
* 修正Contexthub的獨立永續性快取。
* 精確計算資產維度。
* 將資產發佈至品牌入口網站時，AEM效能已最佳化。
* 修正畫布節點中Resourcetype值。
* 針對檔案片段內容啟用區分大小寫和特殊字元搜尋功能。
* 增強的最適化表單，在Safari中附加PDF做為附件。\
   提供新的動態媒體，可連接到新的動態媒體發佈基礎架構，以實現更快速、更可擴展的複製。

### 資產 {#assets-10}

* AEM Assets無法擷取InDesign資產的子資產參考，包括資產的重複連結。 NPR-19006:CQ-4204186的修補程式
* 「排序」選項無法用於「商務」下方的系列內的資產。 NPR-19508:CQ-4213622的修補程式
* 當與現有資產同名的資產移至相同位置時，cq的值為：資產的lastReplicationAction會在它們之間交換，這會導致建立錯誤的元資料。 NPR-19531
* 發佈大量資產時會顯示錯誤訊息，儘管所有資產都已正確發佈。 NPR-19629:CQ-4219611的修補程式
* 「靜態轉譯」會列在固定的維度中，但不會反映實際轉譯的大小。 NPR-20004
* 當多個資產（超過4個）發佈至品牌入口網站時，AEM例項會變得無法運作。 NPR-20009

### 網站 {#sites-10}

* AEM會在使用者嘗試發佈/unpublish/建立其他使用者鎖定之頁面版本時，顯示非預期的行為。 NPR-19249;CQ-4215298和CQ-4203856的修補程式
* 手動提升巢狀啟動時，子頁面會遭到刪除。 NPR-19704
* ContextHub在初始化期間儲存會覆寫預設永續性層時的永續性問題。 NPR-19979:CQ-4218399的修補程式
* 內容片段與其他按鈕重疊。 NPR-19980:CQ-4221519的修補程式
* 在SiteAdmin中使用別名檢視時，不會顯示網站頁面。 NPR-20053:CQ-4221478的修補程式
* 發佈指向Adobe促銷活動中匯入工具頁面的即時副本頁面時發生錯誤。 NPR-20066:CQ-4220846的修補程式

### 平台 {#platform-8}

* 將Apache POI升級至3.16版，以支援將PPT投影片的背景影像包含在轉譯中。 NPR-18286
* 在同一資料夾中上傳多個資產時，Internet Browser 11和Edge的轉譯問題。 NPR-20062

### 整合{#integration-11}

* 自訂at.js檔案在與匿名使用者存取時不會發佈。 NPR-19542:CQ-4219592的修補程式
* 將Analytics現有認證移轉至WSSE驗證。 NPR-19962

### 品牌入口網站 {#brand-portal}

* 啟用從AEM發佈標籤至品牌入口網站的標籤／標籤控制台。 NPR-20271

## 表單 {#forms-11}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

### Forms add-on package {#forms-add-on-package-11}

#### 通信管理{#correspondence-management-4}

* 啟用功能，可在預覽字母時搜尋檔案片段中的實際文字。 NPR-19712

#### 適用性表單 {#adaptive-forms-8}

* 增強的最適化表單，在Safari中附加PDF做為附件。 為支援現有表格的相同功能，我們需要變更附件Widget和「支援的檔案類型」中的設定，以更新值application/pdf，而非。pdf。 NPR-19623

#### Forms Manager {#forms-manager-1}

* 如果在最適化表單欄位上未定義validationState，並發生elementFocusChanged事件，則會傳回錯誤事件(errorState)至Adobe Analytics伺服器。 NPR-19513

### Forms JEE安裝程式{#forms-jee-installer-11}

#### 核心 {#core-3}

* 在關閉期間，連接管理器不可用。 Jboss會在取消部署作者EAR之前切斷JDBC相依性，從而導致損壞問題。 NPR-19703

## 包含的功能套件{#feature-packs-included-1}

* 動態媒體中的縮圖修正和透明度改進。 NPR-15207

## CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}隨附的OSGI組合和內容封裝

AEM 6.2SP1-CFP9中更新的內容套件清單

[取得檔案](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

AEM 6.2SP1-CFP9中更新的OSGi組合清單

[取得檔案](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 在Adobe電子郵件範本服務中，為自訂使用者範本引進標籤。
* 案頭應用程式的TouchUI按鈕增強功能。
* 按一下即停用提交按鈕，以防止翻譯頁面上出現多個表單提交。
* 在對話框中配置了多個RTE元件。
* 增強的參考即時副本中的更新。
* 針對檔案片段內容啟用區分大小寫的搜尋功能。
* 將Linux程式庫清單新增至AEM Forms安裝檔案。

### 資產 {#assets-11}

* 在Safari瀏覽器上智慧型系列上套用Omnisearch篩選器的問題。 NPR-19511
* 當有多個關鍵字與PDF資產相關聯時，PDF關鍵字中繼資料無法正確擷取和修改。 為瞭解決此問題，PDF資產的「主旨」欄位中繼資料屬性已移除。 不過，您可以編輯中繼資料結構，為「主旨」欄位新增多值文字欄位。 NPR-19126
* 工作流程通知服務不會對電子郵件中的連結進行編碼，這樣在使用者點按連結後，就無法載入連結。 NPR-19490:CQ-4218055的修補程式
* 無法使用Chrome在「欄」檢視中載入頁面／資產的完整清單。 NPR-19458:CQ-4214248的修補程式
* 啟用「請求啟動」工作流程時，AEM收件匣中會顯示錯誤的關閉時間圖示。 NPR-19365:CQ-4216174
* 清單檢視中排序的問題。 NPR-19217:CQ-95602
* 在「資產檔案夾」設定中變更標題或縮圖圖片時，會覆寫檔案夾的原始群組和權限。 NPR-19283:CQ-4216080的修補程式
* Windows 10工作站會自動切換到「觸控模式」，禁用部分按鈕的功能。 NPR-19183

### 網站 {#sites-11}

* 在對話框中使用多個RTE元件的問題。 NPR-19311:NPR-19587
* VersionManagerImpl初始化後，Vanilla AEM 6.2中的自動清除版本只能運作一次。 NPR-19315:CQ-4217175的修補程式
* 工作流程例項卡在「Salesforce.com Export」工作流程步驟中。 NPR-19222:CQ-4212976的修補程式
* 無法編輯從即時副本建立的語言副本頁面。 NPR-18967
* ReferencesUpdateAction無法在階層變更的情況下將連結更新至巢狀LiveCopy。 NPR-18715:CQ-4214105的修補程式

### 平台 {#platform-9}

* Adobe電子郵件範本服務會新增標籤至自訂使用者範本。 NPR-19190:CQ-4217113的修補程式

### 專案 {#projects-2}

* 專案編輯人員無法將資產複製／貼入專案資產檔案夾。 NPR-19619
* 在安裝6.2 SP1-CFP1後，無法為翻譯項目生成預覽。 NPR-16481:CQ-4204655

### 整合{#integration-12}

* 在Classic UI的Adobe Digital Publishing Solution中，存取文章設定不正確的屬性。 NPR-19366
* 由於AEM Article主控台中的全尺寸文章，縮圖演算不暢。 NPR-19086:CQ-4217148
* 如果使用者可存取多個區域，在透過促銷活動個人化選件時自動折疊的行為不正確。 NPR-19290:CQ-4218029的修補程式
* 當目標模組被編輯並儲存多次時，定位對話框不會在定位模式中顯示。 NPR-19144:CQ-4216708的修補程式

### 工作流程 {#workflow-2}

* 使用者無法依「收件匣傳統型」UI中的使用者／群組來篩選「收件匣」中的通知。 NPR-19122:CQ-4215374的修補程式
* 「影像地圖」不會保留HTL影像元件中選取的座標。 NPR-18911:CQ-4211584

## 表單 {#forms-12}

* AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-12}

* 當內容從Microsoft Word或Web瀏覽器複製到通信管理器文本編輯器時，樣式將丟失。 NPR-19530
* 沒有換行符號的文字編輯器內容不會換行。 NPR-19481
* 啟用功能，可在預覽字母時搜尋檔案片段中的實際文字。 NPR-17792:CQ-4214501的修補程式

#### 通信管理{#correspondence-management-5}

>[!NOTE]
>
>文字片段的搜尋功能有一些限制：-
>
>* 檔案片段內容區分大小寫，標題不區分大小寫。
>* 當搜尋的字詞的一部分使用不同的樣式或包含特殊字元（如「」或「或\）時，搜尋結果不會反白顯示。
>* 在檔案片段中，搜尋不適用於動態內容（例如資料字典元素值或變數值）。


#### Forms Manager {#forms-manager-2}

* 在AEM 6.2上套用CFP6後，無法編輯Adaptive Forms的XML架構屬性。CQ-4219684的修補程式
* 重新啟動伺服器時，不會啟動AEM Forms Manager核心套件的所有服務。 CQ-4217014的修補程式

### Forms JEE安裝程式{#forms-jee-installer-12}

#### 安裝LCM {#install-lcm-2}

* 在Microsoft Windows上，在安裝CFP6後，管理員畫面會顯示版本號碼6.0。 CQ-4217573的修補程式

## 包含的功能套件{#feature-packs-included-2}

* 案頭應用程式的TouchUI按鈕增強功能。 NPR-18676

## CFP8中包含的OSGi組合{#osgi-bundles-included-in-cfp}

AEM 6.2SP1-CFP8中更新的OSGi組合清單

[取得檔案](assets/do-not-localize/updated-bundles-list-cfp8.txt)

AEM 6.2SP1-CFP8中更新的內容套件清單

[取得檔案](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 在具有dc的影像的影像卡上顯示標題的行為變更：title屬性設為字串[](multifield)。
* Dynamic Media Cloud Services、Touch UI和Security UI介面的效能問題修正。
* Apache Felix Http Bridge 3.0.8中的修正
* 已解決作者與發佈環境之間的無二進位複製(BLR)問題。
* 支援目標程式庫檔案AT.JS，此實作程式庫可用於用戶端與Adobe Target整合，專為一般網頁實作和單頁應用程式而設計。
* 針對Marketing Cloud解決方案（Analytics、DTM、Target和S&amp;P）推出使用者可設定的連線逾時期，以改善AEM效能。

### 資產 {#assets-12}

* 在測試使用AEM 6.3設定Dynamic Media Cloud Services的視訊擷取時，會造成「開啟的檔案太多」例外。 NPR-18734;CQ-4211407的修補程式
* 重新啟動AEM例項後，頁面上資產的虛名URL設定無法運作。 NPR-18634;Granite-18085的修補程式
* 在TouchUI中，「發佈」按鈕會針對未取得發佈資產權限的使用者顯示。 NPR-18620;CQ-4214042的修補程式
* 為資產設定授權合約後，資產的下載對話方塊中就不會出現動態轉譯選項。 NPR-18607;CQ-4212342的修補程式
* 無法針對名稱中包含空格的資產下載動態轉譯。 NPR-18571;CQ-4211738的修補程式
* 與Creative Cloud共用資產資料夾時，無法儲存多個使用者。 NPR-18489;CQ-103297的修補程式
* dc:title &amp; dc:crx/de中的說明不會變更為多欄位值。 NPR-18474;CQ-4209086的修補程式
* 移動資產操作會導致效能降低。 NPR-18346
* 當時間軸在開啟時，預設的「全部顯示」選項設定不會顯示任何項目。 NPR-18302;CQ-4211957的修補程式
* 當ASCII/UTF-8編碼文字檔案上傳至AEM Assets且縮圖產生失敗時，會發生錯誤。 NPR-18006:CQ-4209345的CFP
* 即使使用者沒有複製存取權，發佈動作按鈕也會顯示。 NPR-17353;CQ-4209269的修補程式
* 當使用min:gcc;obfuscate=true啟用微型化時，網站管理員和Miscadmin都無法運作。 NPR-18593;CQ-4209220的修補程式
* 每次重新整理螢幕後，自訂功能表項目才會顯示。 NPR-18500;CQ-4213581的修補程式
* 將moment.js升級至2.10.6。NPR-18596;Granite-11881的修補程式
* 為管理員用戶應用DM宏的權限會中斷視圖。 NPR-18544;CQ-4211729的修補程式
* 資產的Publish Later會引發非法的ArgumentException。 CQ-4214532

### 網站 {#sites-12}

* 在具有MongoDB的活動——活動作者群集上，當時間達到內容的「按時」設定時，兩位作者都會嘗試觸發相同內容的複製。 NPR-18708;CQ-4210982的修補程式
* 在移動具有沒有jcr的參考的資源時，NPE:內容節點。 NPR-18664
* 在包含多個parsys元件的頁面中，不會顯示佔位符。 NPR-18645;CQ-110253的修補程式
* AbstractCopyMoveCommand中的併發問題。 NPR-18591
* 當從另一個AEM實例將文本複製到parsys元件時，將建立parsys而不設定任何resourceType。 NPR-18511;CQ-4212306的修補程式

### 平台 {#platform-10}

* JCR安裝程式不會在安裝套件後更新套件版本。 NPR-18728;NPR-15135的修補程式
* 無二進位檔案複製(BLR)在二進位檔案b/w作者和發佈環境中失敗。 NPR-18704
* AEM環境中的Apache Felix Http Bridge解析要求。 NPR-18297
* 當多個具有類似結構的頁面同時與Sling Content Distribution複製時，複製會失敗。 NPR-18665;Granite-13712的修補程式
* Sling散發套件已建立且未自行清理。 NPR-18601;Granite-16183的修補程式

### 整合{#integration-13}

* 檢視從資料庫資料夾發佈的選件會產生NPE。 NPR-18732;CQ-4214593的修補程式
* 從特定日期變更為「啟用／停用時」時，JCR和Target中活動的開始／結束日期不會更新。 NPR-18612;CQ-104831的修補程式
* Analytics與AEM的整合沒有為httpclient連線設定連線或通訊端逾時。 NPR-18497
* DTM與AEM的整合沒有為httpclient連線設定連線或通訊端逾時。 NPR-18495
* Target與AEM的整合沒有為httpclient連線設定連線或通訊端逾時。 NPR-18494
* 與AEM的Search &amp; Promote整合沒有為httpclient連線設定連線或通訊端逾時。 NPR-18493
* 新增額外體驗後，Target活動會停用。 NPR-18227;CQ-4201895的修補程式

### WCM-Foundation元件{#wcm-foundation-components-7}

* 影像地圖不會保留HTL影像元件中選取的坐標。 NPR-18530;CQ-4211584的修補程式

### 轉換 {#translation-5}

* 翻譯搜索結果不包括翻譯項目的名稱。 NPR-18224;CQ-4210658的修補程式

### 品牌入口網站 {#brand-portal-1}

* 啟用從AEM發佈標籤至品牌入口網站的標籤／標籤控制台。 CQ-4212165

## 表單 {#forms-13}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-13}

#### 通信管理{#correspondence-management-6}

* 在儲存片段之前，編輯面板中不會顯示正確的資料。 NPR-19092
* 將檔案片段加入信件需要相當長的時間。 NPR-18958
* 如果XML聲明存在於資料xml檔案中，並且字母轉譯通過POST請求啟動，則對應的字母無法顯示資料。 NPR-18870
* 不會為對CM資產採取的操作生成審計日誌。 NPR-16618

>[!NOTE]
>
>如果您受到以下兩個問題的影響，請勿安裝此CFP附加套件：
>
>* 「從Word/Web複製貼上到CM」文本編輯器顯示換行內容。 NPR-19530
>* CM文本編輯器中沒有換行符的內容不換行。 NPR-19449

>
>
這些問題將在未來的CFP中解決。

#### 適用性表單 {#adaptive-forms-9}

* 在為可重複面板新增面板時，會刪除上一個面板中下拉式欄位的值。 NPR-18772
* 標籤為僅接受整數的最適化表單欄位，也接受數值面板中的幾個特殊字元。 NPR-18680
* 在引導面板初始化事件時變更按鈕標題的指令碼無法運作。 NPR-18476
* 在規則編輯器下建立的規則的右側面板中看不到捲軸。 NPR-18716

#### AEM Forms App {#aem-forms-app}

* 當表單處於離線模式或未連線至網路時，表單無法在AEM Forms App中正確呈現。 CQ-4218368

### Forms JEE安裝程式{#forms-jee-installer-13}

#### PDFG服務{#pdfg-service-3}

* PDF產生器無法產生具有指定書籤層級的PDF檔案。 CQ-4211102的修補程式

## CFP7 {#osgi-bundles-included-in-cfp-1}隨附的OSGi組合

AEM 6.2SP1-CFP7中更新的OSGi組合清單

[取得檔案](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

AEM 6.2SP1-CFP7中更新的內容套件清單

[取得檔案](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 在平板電腦的版面模式中有效管理隱藏元件。
* 在混合裝置上推出Quickactions。
* 解決即時副本的元件層級同步問題。

### 資產 {#assets-13}

* 當沒有必要權限的使用者嘗試移動資產作業時，客戶會遭到封鎖。 NPR-18330;CQ-4212560的修補程式
* 合併多個智慧型內容服務組態會造成可用性問題。 NPR-18273;CQ-4201557的修補程式
* 「結帳動作／工作流程」約一次無法從時間軸主控台使用。 「資產」檔案夾中新增80個片段。 NPR-18257;CQ-4211214和NPR-18251的修補程式；CQ-4211216的修補程式。
* 系統在「記憶體不足」中當機，在「資產」報表期間無法分頁。 NPR-17865;CQ-4209759的修補程式
* 發佈的視訊無法在編碼的視訊資產上播放。 NPR-17849;CQ-4210739的修補程式
* 不會產生PDF的縮圖。 NPR-17831、NPR-17750;CQ-4210547的修補程式
* 過期的資產不會由Adobe CQ DAM到期通知工作停用。 NPR-17666;CQ-107766的修補程式
* 資產到期活動會在資產沒有指派擁有者時停止。 NPR-17665;CQ-4197946的修補程式
* 當移動包含150個以上傳入參考的資產資料夾時，會出現Null指標例外。 CQ-4200981

### 網站 {#sites-13}

* 個人化只適用於為IP範圍設定分段規則時的第一個IP。 NPR-18121;CQ-83767的修補程式
* 啟用historyShow屬性時，登入會因NumberFormatException而失敗。 NPR-18073;CQ-101965的修補程式
* 已標籤的已刪除頁面可在Touch UI中顯示。 NPR-18025;CQ-86694的修補程式
* 載入具有大（2000個以上）觀眾的頁面時，效能問題。 NPR-17884;CQ-4209567的修補程式
* 在移除頁面上的其他影像後，無法選取影像。 NPR-17711;CQ-4201323的修補程式

### 平台 {#platform-11}

* 沒有必要權限的使用者不會隱藏觸控UI控制項。 NPR-17945;CQ-4211231的修補程式
* 標籤欄位上遺失日文標籤。 NPR-17768;CQ-4210456的修補程式
* 啟用FastQuerySize時，getsize()查詢會傳回不正確的結果。 NPR-18018
* 無法訪問備用實例上的Web控制台。 NPR-17861;Granite-14582的修補程式

### 商務 {#commerce-2}

* 當目錄藍圖沒有為節定義任何條件時，會發生查詢遍歷。 NPR-18229;CQ-4211924的修補程式

### 社群 {#communities-2}

* PollingImporterImpl. 延遲AEM關閉。 NPR-18298;CQ-96133的修補程式

### 整合{#integrations}

* 已解決當AEM Day HTTP Client 3.1 OSGI設定為需要摘要驗證的Proxy時，可能發生的AEM Search元件錯誤。 18128盧比
* 還原繼承缺少複選框。 NPR-17753;CQ-4210139的修補程式要求
* 當使用者定位具有多個活動的一個元件時，無法設定優先順序。 NPR-18658;CQ-4210727的修補程式
* 使用者無法瀏覽資料夾/etc/segmentation，以選取在資料夾/etc/segmentation/group1下建立的對象。 NPR-18522

### 安全性 {#security-1}

* 如果用戶對目標資料夾沒有寫權限，則移動資產嚮導將掛起。 NPR-18300
* 請求在Apache Sling API中使用org.apache.sling.servlets.post servelet(2.3.22)升級版，以預先防範XSS弱點。 NPR-18963

### 轉換 {#translation-6}

* 在項目完成之前，不應再將資產頁面提交到翻譯項目。 NPR-18249;CQ-4209908的修補程式

### WCM-Foundation元件{#wcm-foundation-components-8}

* 無法在可編輯的範本中使用WCM foundation iparsys元件。 NPR-18223;CQ-4210384的修補程式
* 「影像地圖」不會保留HTL影像元件中選取的座標。 NPR-18032;CQ-4211584的修補程式
* 當HTL影像元件轉譯時，URL中的檔案名稱會重新命名，造成URL中斷。 NPR-17908;CQ-4211587的修補程式
* 進行變更後，無法退出「頁面屬性」。 NPR-17832;CQ-96110的修補程式

## 表單 {#forms-14}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-14}

**信件管理**

* 在字母轉換期間，資料字典會重複讀取。 NPR-18482, CQ-4210805的修補程式
* 新增com.adobe.livecycle.content類別的JavaDocs。 NPR-18467
* 建立字母時，不保存該字母的說明。 NPR-18039
* 當文本模組被保存且文本模組中的表達式不包含開啟或關閉表達式標籤時，不會顯示錯誤消息。 文字模組會顯示錯誤訊息，無法在字母中呈現。 NPR-17798
* 在安裝附加軟體包的日誌中出現意外錯誤。 NPR-18295

**Forms Manager**

* AEM Forms UI會以最舊的首次順序列出所有資產。 使用者無法以最新的首次順序重新排序資產。 NPR-18451

### Forms JEE安裝程式{#forms-jee-installer-14}

**輸出服務**

* 已改善AEM表單6.2的Output服務效能問題。NPR-18033

**簽名服務**

* 無法使用遠端硬體安全性模組簽署PDF檔案。 NPR-18017

## CFP6 {#osgi-bundles-included-in-cfp-2}隨附的OSGi組合

AEM 6.2SP1-CFP6中更新的OSGi組合清單

[取得檔案](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

AEM 6.2SP1-CFP6中更新的內容套件清單

[取得檔案](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* 已解決共用、移動、發佈及下載資產的數個UI問題。
* 增加「移動」對話方塊顯示參考資產的能力。
* 已解決WCM元件和工作流程的數個問題，例如「解除發佈」和「版本清除」。
* 已改善動作列在顯示工具列動作和Coral元件方面的回應速度。

### 資產 {#assets-14}

* 發佈至品牌入口網站功能的效能改進。 NPR-17189;CQ-4204150的修補程式
* 使用「共用連結」選項共用資產並不會建立具有平面檔案夾結構的zip檔案以供下載。 NPR-17513;CQ-4209381的修補程式
* 在DAM中選取資產並按一下「發佈」，不會在「資產詳細資料」頁面中顯示「發佈至品牌入口網站」選項。 NPR-17351;CQ-94905的修補程式
* 在DAM工作流步驟中，必須在最終塊中關閉從會話或資源解析器獲取的二進位流，以確保不會發生資源洩漏。 NPR-17385;CQ-4209452的修補程式
* 在DAM中上傳Word檔案會導致Null指標異常，而工作流程例項仍會卡在「執行」狀態。 NPR-17160;CQ-4207358的修補程式
* 對於過期的資產，非管理員使用者可在「中繼資料編輯器」頁面上看到「共用」、「移動」、「發佈」和「下載」按鈕。 NPR-16903;CQ-101440/CQ-104535的修補程式
* 「資產」主控台中的管理使用者可看到「共用」、「移動」、「發佈」和「複製」等動作。 NPR-16902;CQ-4207111的修補程式

### 網站 {#sites-14}

* 使用Classic和Touch UI移動頁面時，「移動」對話方塊不會顯示超過150的參照，使用者無法更新這些參照並重新發佈頁面。 此問題已經修正，因為Classic UI的屬性已經推出：&#39;maxRefNo&#39;，可在siteadmin節點上配置：&#39;/libs/wcm/core/content/siteadmin&#39;。 此屬性指定在大量移動操作之前顯示的最大引用數（預設值150），如果頁面的引用數較多，則不會在movePage對話框中顯示這些引用。 此配置也適用於damdin和miscadmin，方法是在節點上應用配置：`'/libs/wcm/core/content/damadmin'`和`'/libs/wcm/core/content/miscadmin'`。 NPR-17222;CQ-85878的修補程式

* 使用WCM元件時，Touch UI Rich Text Editor會移除含空格的超連結。 NPR-17698、NPR-17570;CQ-4206768的修補程式
* 從頁面屬性觸發「請求取消發佈」工作流程時，無複製權限的使用者會出現JavaScript錯誤。 NPR-17294;CQ-102064的修補程式
* 轉譯或匯出HTL影像元件會將URL變更為數字，並重新命名檔案名稱，這會造成連結中斷。 NPR-17245;CQ-59616的修補程式
* 在巢狀啟動中刪除啟動會導致子啟動變成孤立。 NPR-17228;CQ-4202639的修補程式
* 在已套用Oak 1.4.13的AEM 6.2中執行Version Purge會在記錄檔中持續重複警告。 NPR-17391;CQ-4206870的修補程式
* 在安裝ContextHub元件的修補程式或升級後，內容套件會覆寫/etc/segmentation/contexthub中的所有區段，導致所有自訂ContextHub區段遺失。 NPR-17250;CQ-79958的修補程式
* 當以工作流程使用者身分執行含巢狀群組的工作流程時，WorkflowStatusProvider(pageinfo.json)會鎖定工作流程例項。 NPR-17555;CQ-4202056的修補程式
* 使用WCM-Page編輯器元件時，在作者實例的Touch UI編輯模式下，頁面末尾存在大量空白。 NPR-17510;CQ-4205441的修補程式
* 轉譯或匯出HTL影像元件會將URL變更為數字，而造成連結中斷。 NPR-17245;CQ-59616的修補程式

### UI {#ui}

* 選取資產並按一下「開發人員工具」時，動作列中的工具列動作不一定會以緩慢的連線顯示，而且必須重新載入頁面。 NPR-17568;CQ-108365的修補程式
* 動作列應更新為使用兩個容器：coral-actionbar-primary和coral-actionbar-secondary，而非coral-actionbar-container。 NPR-17591;GRANITE-15225的修補程式

### 隨選行動裝置{#mobile-on-demand-2}

* 擁有AEM Mobile應用程式「唯讀」權限的使用者無法從AEM Mobile內容管理頁面預覽內容。 NPR-17390;CQ-4209690的修補程式

### 安全性 {#security-2}

* HTMLRenderServlet產生的輸出中的XSS弱點。 NPR-17136
* 要求防止AEM Web Syndication Feeds頁面中AEM版本洩漏。 NPR-16219

### 表單 {#forms-15}

#### Forms add-on package {#forms-add-on-package-15}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

**適用性表單**

* 對於具有附件的最適化表單，在第二次提交表單時，afSubmissionInfo標籤的重複項目會在提交的XML中建立。 NPR-17364
* 使用Google Chrome瀏覽器時，從表單移除附件後，嘗試重新附加相同的附件會再次引發錯誤。 NPR-17297
* 如果XSD或No-Form-model型自適應表單中有巢狀的可重複延遲載入面板，則表單中填入的值不會保留在記錄檔案(DOR)中。 NPR-17176
* 規則編輯器的錯誤記錄中顯示的錯誤應新增至try/catch區塊JavaScript程式碼的catch區塊。 NPR-16757
* 在表單中按一下檔案附件會引發瀏覽器主控台錯誤，而不會顯示附件預覽。 NPR-17174

**信件管理**

* 「建立對應UI」功能會中斷，以免在UI中新增內嵌文字或空白行。 NPR-17748
* 當開啟信函供編輯時，瀏覽器會閃爍。 NPR-17576
* 在計算資料字典元素中添加遠程函式時，如果函式數大於顯示遠程函式的頁籤的長度，則捲動條不會出現在頁籤中。 NPR-17359
* API方法匯入com.adobe.icc.services.api.LetterInstanceService無法運作。 NPR-17922、NPR-16008
* 在編輯字母時，在文字模組中新增的變數不會顯示在「資料系結」面板中。 NPR-17940
* 當HTML提交動作使用POST方法時，Corresponce Management UI不會啟動。 NPR-17595

**Forms Manager**

* 在為AB測試設定的最適化表單中，按一下「開始AB測試」不會啟動測試，並會擲回瀏覽器主控台錯誤。 NPR-17838

**表單服務**

* OSGI表單靜態代碼分析中報告的問題應該修正。 NPR-13951

#### Forms JEE安裝程式{#forms-jee-installer-15}

**輸出服務**

* 使用AEM forms 6.2 Output Service將特定表單與資料XML合併所需的時間，是LiveCycle ES4 SP1伺服器執行相同作業所花費的20倍。 它固定在Windows和Linux環境中。 NPR-17501

**安裝LCM**

* 安裝AEM Forms 6.2 GM組建版本並套用AEM 6.2 CFP後，執行LiveCycle Configuration Manager時，「版本資訊」中會顯示不需要的分號，而且修補程式安裝日期不會更新。 NPR-14322

**流程管理**

* AEM Forms進程不會填入TaskContext變數。 CQ-4211857

#### AEM Forms JEE Bundles Package {#aem-forms-jee-bundles-package}

* 表單使用者的功能（不論使用JEE管理UI主控台或OSGi主控台）應相同。 NPR-17670

### CFP5包含的功能套件{#feature-packs-included-in-cfp}

**Forms JEE套件**

流程管理-HTML工作區

* 在指定工作區步驟時，工作區附件頁籤應顯示附件或附註的計數器，以備存在多個附件或附註時使用。 NPR-17771
* 要求在AEM JEE Forms中支援Office 365，以取得表單工作流程中的電子郵件功能。 NPR-13866

**Forms Add-on Package**

信件管理

* 在字母預覽期間在文字編輯器中編輯片段時，應顯示已處理的文字以供編輯，而非片段中使用的內嵌條件。 NPR-15748、NPR-17504

### CFP5 {#osgi-bundles-included-in-cfp-3}隨附的OSGi組合

AEM6.2 SP1-CFP5之間更新的OSGi組合清單

[取得檔案](assets/do-not-localize/cfp5_osgi_bundles.txt)

AEM6.2 SP1-CFP5之間更新的內容套件清單

[取得檔案](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4是重要的更新，其中包含自AEM 6.2 SP1全面推出以來的重要客戶修正。

此Cumulative Fix Pack的主要亮點為：

* Camera Raw檔案轉譯、時間軸檢視和影像方向的資產修正
* 改進功能

   * WCM針對網站的啟動
   * 專案工作流程
   * ContextHub元件

* 促銷活動、行動隨選和翻譯的修正
* 最適化表單規則編輯器中的可用性改進
* 用於表單中對應管理的增強內嵌條件編輯器
* JEE上AEM表單的程式管理與輸出服務修正
* 指令碼編輯器的Forms Designer相關修正

### 平台 {#platform-12}

* Search&amp;Promote搜尋表單會在設定雲端服務時忽略`environment`設定，使其無法用於作者例項。 NPR-16594:CQ-4206076的修補程式
* 在/apps中覆蓋將欄新增或自訂至&#x200B;**Assets OmniSearch**&#x200B;結果時，無法運作。 NPR-16737:CQ-4206785的修補程式
* 從AEM 6.1 SP2就地升級至AEM 6.2 SP1後，**診斷工具**頁面無法運作。 NPR-17121;CQ-4196786的修補程式
* HTL:在選擇論壇、建立主題和帖子時，`Sightly SightlyCompiledScript`將不正確的`addSelectors`屬性添加到`RequestDispatcherOption`。 NPR-17008:GRANITE-16384的修補程式

* 已新增`ReportImporter`在`ManagedPollConfigs`中對`CRON expressions`的支援。 NPR-16608:CQ-4206066的修補程式要求

* 上傳LDAP使用者的頭像影像失敗。 NPR-16561;Granite-17013的修補程式
* 「使用者管理」畫面上顯示的結果數量在「卡片」和「清單」檢視中不同。 NPR-16241;GRANITE-16914的修補程式
* 在Google Chrome瀏覽器中以全螢幕模式檢視時，工作流程通知無法延遲載入。 NPR-17013:CQ-4207567的修補程式

### 資產 {#assets-15}

* 導入具有已定義方向的影像時，無法正確應用影像方向。 NPR-16750:CQ-4204356的修補程式
* 「資產時間軸」檢視不會顯示任何資產，即使預設設定了「全部顯示」亦然。 NPR-16957:CQ-98780的修補程式
* 在資產中新增為轉譯時，無法選取或刪除Camera Raw檔案（包括ARW、CR2、NEF、DNG和EPS）。 當使用者按一下這些檔案時，就會自動下載這些檔案。 NPR-16949:CQ-4206846的修補程式
* 在「資產」UI中建立另一個PDF時，不會在DAM UI中顯示已建立的PDF，不過這些PDF會顯示在crx儲存庫中。 NPR-16833:CQ-4206501的修補程式
* 使用Touch UI將資產上傳為本身的直接子節點會造成問題。 資產會上傳為先前選取資產的直接子系。 NPR-16534:CQ-4204287的修補程式
* 在DAM UI中，在注釋中對資產加上註解和標籤使用者並不會產生郵件通知。 NPR-16589:CQ-102318的修補程式

### 專案 {#projects-3}

在清除工作流時，「項目」工作流控制台在頁上顯示NullPointerException。 NPR-17017:CQ-4194269的修補程式

### 網站 {#sites-15}

* `ContextHub`中的檔案在作者實例上不會最小化。 NPR-17022:CQ-79456的修補程式
* WCM-Launches啟動促銷活動需要很長時間，才能促銷由大樹狀頁面組成的啟動。 NPR-16480:CQ-82731的修補程式
* `ClientContext` 區段條件轉換程式在使用非使用或未完成的規則建立區段（或對象）時當機。NPR-16759:CQ-4205104的修補程式
* 在「WCM啟動」中，當動作從Touch UI的頁面屬性中啟動時，與啟動相關聯的頁面不會解除發佈。 NPR-16560:CQ-4204681的修補程式
* 「連結重寫器」假設冒號&quot;:&quot;定義JCR命名空間，不實地重寫包含冒號的href值。 NPR-16753:CQ-4203762的修補程式
* 在WCM-Design Importer中，開啟測試匯入程式頁面並嘗試上傳zip檔案會造成先前已上傳和刪除的問題。 NPR-16486:CQ-90962的修補程式
* 使用Firefox Safari和Google Chrome瀏覽器導覽至&#x200B;**[!UICONTROL 全域導覽]**&#x200B;窗格，提供不同的使用者體驗。 Firefox瀏覽器會顯示&#x200B;**[!UICONTROL 工具]**&#x200B;功能表，而Google Chrome瀏覽器則會顯示&#x200B;**[!UICONTROL 導覽]**&#x200B;功能表。 NPR-16770;CQ-4200456的修補程式

### 行銷活動 {#campaign}

* 在測試AEM促銷活動範本並修改種子位址以包含「其他資料」時，Adobe Campaign下拉式清單會在Touch UI Context Hub中消失。 NPR-16771:CQ-105748的修補程式

### 行動隨選{#mobile-on-demand-3}

* 當從AEM作者環境預檢出版物時，超過5秒的「預檢」動作會在AEMM - AEM PECS整合顯示面板上產生異常尖峰，每秒會出現大量狀態要求。 NPR-16908:CQ-4207055的修補程式
* 安裝AEM-6.2-SP1-CFP1-1.0更新後，AEM Mobile組態管理會失敗。 NPR-16909:CQ-4204892的修補程式

### 轉換 {#translation-7}

* 在安裝6.2 SP1 - CFP1後，預覽轉譯作業無法運作。 NPR-16481;CQ-4204655的修補程式
* 使用「翻譯」建立的語言副本指向「根主版」，而不是指向本地國家／地區的副本。 NPR-17257;CQ-4208287的修補程式

### 安全性 {#security-3}

* 將檔案的二進位檔上傳至AEM時，不會執行MIME類型驗證。 NPR-16617
* 上傳LDAP使用者頭像的問題。 NPR-16561

### 表單 {#forms-16}

#### Forms add-on package {#forms-add-on-package-16}

**適用性表單**

* 在最適化表單編輯器中，head.jsp中的Target設定注釋應以新的Context Hub陳述式取代。 NPR-17173
* 在最適化表單規則編輯器中，**[!UICONTROL 選擇項目]**&#x200B;會將事件顯示為&#39;null&#39;。 NPR-17139
* 使用前向箭頭(>)在前嚮導覽時，提交的表單會重新送出。 NPR-17080
* 透過AJAX提交最適化表單時，不會在發生錯誤時呼叫&#39;error&#39;回呼函式。 NPR-17034
* 在執行時期按一下規則編輯器中的「儲存表單」按鈕時，不會儲存表單。 **** NPR-16905
* 靜態文字應排除在「最適化」表單的Tabbing順序之外。 NPR-16749
* 小數欄位的計算值顯示不正確。 NPR-16596
* 顯示「說明」內容的圖示應包含在「最適化」表單的標籤順序中。 NPR-16484
* 支援在「**[!UICONTROL 預設預填充服務配置]**」中使用類型`dataRef=C:/Users/`的規則表達式來預填充最適化表單的資料。 NPR-16425

* 如果有巢狀延遲載入的藍本，則無法正確觸發所有面板的驗證。 NPR-15821

**信件管理**

* 如果字母包含空白文字模組（一個不含文字），字母轉譯會失敗。 NPR-17054
* 在「文字編輯器」中貼上後，內容中會移除分行符號和制表符空格。 NPR-17039
* 如果文本模組被引用為多個字母，則文本模組的引用的顯示會花費很多時間。 NPR-17035
* 編輯、儲存、刪除和設定檔案片段參考需要很長的時間。 NPR-17033
* 在預覽字母時，對齊文字會以不同的字型呈現。 NPR-16976
* 如果搜尋的文字有多次發生，搜尋功能無法正常運作。 NPR-16920
* 「文字編輯器」工具列會間歇性地顯示在瀏覽器中。 NPR-16919
* 從規則編輯器中保存表單的&#x200B;**[!UICONTROL 結構無法運作。]** NPR-16905
* 「字型」下拉式清單不會在使用Internet Explorer根據資料字典建立文字模組時填入「字型」系列。 NPR-16944
* 建立文字片段後，字母字型會在預覽字母時變更。 NPR-16830
* 檔案片段中，開頭或之間有制表符空格的字母無法呈現或預覽。 NPR-16769

**行動表單**

* 「行動表單」預覽會顯示重疊的內容，不過表單會正確顯示以供PDF轉譯。 NPR-17105

**表單入口網站**

* 按一下已提交表單的&#x200B;**[!UICONTROL Download]**&#x200B;連結，會開啟HTML頁面，而非PDF表單。 NPR-17082

* `Upload Comments` 對於已提交實例，檔案附件不會顯示在UI中，儘管它們儲存在crx儲存庫中的XML中。NPR-17075

**Reader Extensions服務**

* 在AEM Forms OSGI安裝中，特定檔案不是Reader Extended。 NPR-16625

#### Forms JEE安裝程式{#forms-jee-installer-16}

**核心**

* 在升級過程中，Configuration Manager會因超時而失敗。 NPR-16774（請參閱[在元件級別為操作配置超時](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)）。

**流程管理- HTML工作區**

* 從「開始任務」開始的起始點不會從提交起始點時提交的資料開始。 NPR- 16917
* 在HTML工作區中按一下表格的&#x200B;**[!UICONTROL Return]**&#x200B;按鈕並不會關閉表格，但會將其傳回至其群組佇列。\
   NPR-16352

**流程管理**

* 允許用戶將先前任務的顯示名稱設定為進程實例中的任何後續任務。 NPR-15382

**輸出服務**

* 「輸出服務」無法處理已修改為在`date-time format`中繼資料中包含額外「毫秒」欄位的PDF。 NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer指令碼編輯器不會遵循`Calculate Event`和`Validate Event`的「表單屬性」預設值。 NPR-15921

### CFP4包含的功能套件{#feature-packs-included-in-cfp-1}

**Forms Add-on Package**

* 在內嵌條件編輯器中增強對應管理。 NPR-10981

### CFP4 {#osgi-bundles-included-in-cfp-4}隨附的OSGi組合

AEM 6.2 SP1和CFP4之間更新的OSGi組合清單

CFP3的主要特點為：

* 使用含摘要驗證的Proxy，更有效率地搜尋Classic UI和AEM Search元件
* 修正上傳資產和資產中繼資料顯示時的問題
* 修正建立資料夾和移動頁面時的問題，以防標題有特殊字元。
* 使用定位——同步觀眾、發佈促銷活動，以及在Touch UI中選取目標量度的修正
* 解決轉譯工作的同步問題
* 為表單預填服務提供增強的安全性
* 表單入口網站草稿和提交元件以及Barcoded Forms服務的改進
* 包含檔案附件Widget或延遲載入片段的最適化表單的可用性改進。
* 通信管理中的可用性改進包括增強的搜尋功能、記錄已刪除的資產，以及匯入資料字典。

### 平台 {#platform-13}

* **ModelAdapterFactory**&#x200B;中的競爭條件（當兩個線程嘗試插入同一欄位時）會導致無法構建模型。 NPR-16443:SLING-6584的修補程式
* 套件管理器中的驗證選項，可偵測/apps下重疊的檔案（JSP或JavaScript檔案）與/libs下修補程式中所包含的檔案之間的任何衝突。 然後，受影響的覆蓋可以重新建立為包含/libs下檔案的變更。 NPR-16216:CQ-81729的修補程式
* 登入error.log有時會在啟動發行者後數秒內停止，而且需要清除才能再次執行。 要求更新記錄架構並提供Sling記錄。 NPR-15913:Granite-15452的修補程式
* 請求更新JavaScript &quot; `use"` API以避免HTL JavaScript使用API實作失敗。 NPR-16461:SLING-6780的修補程式

### 網站 {#sites-16}

* 從AEM 6.0升級至AEM 6.2後，Classic UI會因為許多查詢而在搜尋標籤時顯示緩慢的效能。 要解決此問題，可以遵循[在標籤控制台（傳統UI）](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr)中禁用複製狀態下提及的步驟。 NPR-15842:CQ-4201748的修補程式。

* 在Touch UI中建立頁面時，「輸入」檢查&#39;name&#39;欄位不會檢查特殊字元&#39;Apostrophe&#39;（與Classic UI中相同）。 因此，無法移動頁面。 NPR-16404:CQ-4205321的修補程式。
* 在Rich Text Editor中對兩列套用不同的樣式，然後合併這些樣式會移除套用在第二列的樣式。 NPR-16389:CQ-4203835的修補程式。
* 在「Touch UI Sites」（觸控UI網站）畫面中，嘗試將頁面貼入沒有子頁面的頁面時，無法運作，因為「貼上」按鈕不會出現。 NPR-15894:CQ-4201696的修補程式。
* 在「內容搜尋器」面板中捲動「頁面」標籤時，「傳統型」UI中會無限顯示幾組頁面，而「觸控型」UI則只顯示少數不重複的頁面。 NPR-16271:CQ-4202371的修補程式
* 在Touch UI中開啟LiveCopy的「頁面屬性」，然後按一下「儲存」而不做任何變更，會記下任何LiveCopy標籤並建立LiveSync Config節點。 NPR-16327:CQ-108562的修補程式
* 表單約束無法讀取`ConstraintMessage`屬性。 NPR-16388:CQ-101330的修補程式
* `wcm/foundation/components/parsys`元件不會顯示&#x200B;**[!UICONTROL &#39;Drag components here]**&#39;預留位置。 NPR:16748:CQ-4205187的修補程式

### 資產 {#assets-16}

* 在安裝6.2 SP1或修補程式12430後，pdf點陣化器會停止運作並導致記憶體不足問題。 NPR-15991
* 字串屬性`documentNumber`的中繼資料會顯示為日期，但應是數字。 NPR-16134:GRANITE-16916的修補程式
* 時間軸事件球標中的文字截斷。 NPR-16226:CQ-85226的修補程式
* 當在具有具有特殊字元的標題的內容層次下建立資料夾時，顯示該特殊字元的編碼形式。 NPR-15935:CQ-4202987的修補程式
* 使用者在瀏覽資產時無法上傳資產或建立資料夾，因為使用「建立」按鈕時顯示的行為不一致。 NPR-16410:CQ-4204793的修補程式
* 從「AEM編寫」的文章檢視上傳共用的HTML資源時，會遇到非預期的錯誤。 NPR-16133:AEMM-4155970的修補程式

### 整合{#integration-14}

* 啟用Digest驗證的Proxy驗證時，AEM Search元件會拋出ConcurrentModificationException。 NPR-15309:CQ-4199191修補程式
* 在AEM中建立Target A/B測試活動時，對象不會同步至Target並顯示「無對象」。 NPR-16229:CQ-4204210的修補程式
* 在安裝SP1+NPR-11577 v1.2後，當在TouchUI中定位時，為目標量度選擇「使用分析量度」時，量度的下拉式清單不會載入。 NPR-16129:CQ-4204316的修補程式
* 使用定位時，發佈促銷活動不會自動發佈整個樹狀結構，包括品牌和主版。 NPR-15855:CQ-94630的修補程式

### 轉換 {#translation-8}

* 同步轉譯工作不會自動觸發，而且AEM輪詢不會在不戳記轉譯專案的情況下發生。 NPR-15163:CQ-90856的修補程式

### 表單 {#forms-17}

#### Forms add-on package {#forms-add-on-package-17}

**適用性表單**

* 在保存帶有附件的最適化表單時，附件的完整路徑會添加到生成的XML的`fileAttachment`標籤中，而不是附件的名稱中。 NPR-16529
* 在以XDP為基礎的最適化表單中，即使預填充XML沒有`afData/afBoundData`包裝函式，`afData/afBoundData`包裝函式也會出現在提交的XML中。 NPR-16118

* 數字欄位中的指數表示法：在使用自適應表單時，如果輸入的小數分數總數超過10個字元的數字，則該數字在提交的XML中會變成指數符號。 NPR-16106
* 對於同時包含檔案附件元件和延遲載入片段的表單，提交的資料xml不包含檔案附件元件的資訊。 NPR-16022
* 對於沒有可重複祖先的延遲載入的可重複面板，在面板的第二個實例中可重複的子項無法重複。 NPR-15944
* 嘗試在表單編輯器中保存片段時，片段模型根不填充子片段的值。 NPR-15943
* 在建立僅包含一個項的複選框並嘗試顯示保持項目標題隱藏的複選框標題時，如果項目文本為空，則建立字典操作會拋出`ArrayIndexOutOfBoundException`。 不會建立字典，且不會在畫面上產生錯誤回應。 NPR-15816
* 對於具有檔案附件Widget的最適化表單，在預覽附加檔案後，表單的某些部分將被禁用。\
   NPR:郵編：16611

* 對於允許多個附件的檔案附件Widget，如果在具有先前附件的介面工具集上提交具有附件的新表單實例，則在開啟添加的附件而不是實際內容時會顯示錯誤代碼。 NPR-16258
* 保護表單預填服務不會因`file://`、`http://`和`ftp://`等通訊協定而遭到未經授權的存取。 請參閱「使用Configuration Manager[配置預填充服務」。 ](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)NPR-15414

* 請求在「驗證」步驟中以PDF格式（而非HTML）來轉換最適化表單，並將所有附件附加至PDF，如此列印成品就會顯示完整的表單。 NPR-9011

**信件管理**

* 在「預覽／編輯」模式下處理字母文字片段時，如果文字轉換為清單，則會中斷整個字母功能，並產生JavaScript錯誤。 NPR-16460
* 每次上載XSD並選取根節點時，瀏覽器停止回應時，匯入XSD檔案以在「對應管理」節點中建立資料字典會失敗。 此問題與瀏覽器無關，不會出現在伺服器記錄檔中。 NPR-16452
* 使用Internet Explorer瀏覽器預覽字母並嘗試編輯內容的字型大小時，字型大小下拉式清單中會顯示8到72的重複值。 NPR-16387
* 如果浮動欄位顯示為XDP片段的輸入欄位，則使用Internet Explorer瀏覽器時，欄位不會在字母預覽中展開。 NPR-16367
* 嘗試從預覽直接提交信件時，由於信件名稱的彈出畫面已隱藏，因此無法正確顯示。 NPR-16353
* 編輯字母時添加的行空格不會反映在「預覽」窗口中。 對於文字片段中的清單，PDF輸出不會顯示正確的間距。 NPR-16267
* 使用Internet Explorer瀏覽器處理文本文檔片段時，嘗試為文本提供縮進失敗，因為游標不允許文本縮進。 NPR-16128
* 將資料字典新增或修改至現有文字檔案片段需要很長時間，而且使用者不會一律收到通知。 NPR-16102
* 使用Internet Explorer瀏覽器預覽具有可捲動內容的字母時，瀏覽器捲軸與字母的捲軸重疊，而且無法在右側查看整個內容的片段。 NPR-16068
* 使用Google Chrome瀏覽器建立或編輯文字檔案片段時，顏色選擇下拉式清單會自動彈出，而且無法移除。 用戶需要選擇清單作為資料條目類型才能編輯片段。 NPR-16067
* 使用Letterinstance API時，方法`import com.adobe.icc.services.api.LetterInstanceService`無法運作。 NPR-16008
* 在「Asset Composer設定」中將日期顯示格式變更為`locale=en_US; dateFormat=MMM dd,yyyy;`無法如預期般運作，且日期格式會顯示為無用字元。 NPR-16007
* 重新編寫時的「資料連結」類型會顯示為「使用者」，即使設定的不同較早。 NPR-16619

**表單入口網站**

* 草稿和提交元件的升級方案不適用於資料庫示例實施。 NPR:郵編：16752

**Barcoded Forms Service(BCF)**

* Barcoded Forms Service(BCF)報告問題的靜態程式碼分析。 NPR-13855

#### Forms JEE安裝程式{#forms-jee-installer-17}

**流程管理- HTML工作區**

* 保護表單預填服務不會透過「file://」、「http://」和「ftp://」等通訊協定未經授權的存取。 有關詳細資訊，請參閱[使用Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)配置預填充服務。 NPR-15434

**使用者管理 **

* SAML登入畫面會在AEM 6.2伺服器上顯示不當的版本(6.1.0)。 NPR-13825
* 在AEM Forms已設定為「單一登入」(Kerberos)驗證時，如果使用者驗證在嘗試登入時失敗，則會傳回錯誤碼&#39;404&#39;。 只有在重新整理頁面後，使用者才會重新導向至登入網站。 NPR-15015

#### Forms Designer {#forms-designer-1}

* 在「字典拼字檢查」中將「表單區域設定」變更為「法文（加拿大）」在AEM Forms Designer中無法運作。\
   NPR-15896

### CFP3中的功能套件{#feature-packs-included-in-cfp-2}

**Forms Add-on Package**

* 刪除通信管理中的任何資產時，應將警告消息記錄在error.log檔案中。 NPR-13225
* 增強在對應管理中預覽字母時的搜尋功能，以啟用文字片段內容中的搜尋文字，而不是只搜尋字母標題或標籤。 NPR-16103

### CFP3 {#osgi-bundles-included-in-cfp-5}隨附的OSGi組合

AEM 6.2 SP1和CFP3之間更新的OSGi組合清單

[取得](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
檔案Cumulative Fix Pack 2的主要亮點為：

* AEM平台中的穩定性修正和效能改進，包括Sling架構和作業
* 改善資產管理，並修正數項資產存取、移動、搜尋、上傳和發佈
* 使用內容片段、錨點外掛程式、投影片和內容中樞元件的修正，改善網站的製作和管理
* Touch UI中的數項修正，包括文字編輯器、Omnisearch和變型建立程式
* 改善翻譯工作流程；增強的Microsoft連接器，可針對Azure入口網站使用新的翻譯API
* 專案和促銷活動中的修正
* 改善的製作和管理，包括修正最適化表單、通訊管理和表單入口網站功能
* Forms JEE核心、XTG和HTML工作區元件中的修正

### 平台 {#platform-14}

* 如果編輯了直接參照Sling架構的頁面，則會觸發`SlingPostProcessor`。 NPR-15754:CQ-104153的修補程式

* 導覽至頁面元件時，傳統UI對話方塊中不會擷取具有`tagBasePath`屬性之標籤的值。 NPR-15543:CQ-4199950的修補程式

* 執行Sling作業時，當您有名為&#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk`的區塊，會執行包含空區塊的循環。 NPR-15455:SLING-5701的修補程式

* 當介面擴展另一介面時，超介面上的可注射方法不能正確注入。 NPR-15202:SLING- 5710的修補程式
* 使用`com.adobe.granite.infocollector.impl.FilesTraversal`函式調用時，不會防止潛在的空指針異常。 NPR-15169 CQ-4197640的修補程式
* 某些輔助節點的工作流狀態不一致，在為該節點調度觀察事件時顯示錯誤。 NPR-15701:GRANITE-13786的修補程式
* 當用戶在CRXDE中選擇節點（例如/content/dam/），然後選擇「訪問控制」頁籤時，確定存在「訪問控制清單」，拖放某些元素會移動選定元素以外的元素。 NPR-15696 GRANITE-16300修補程式
* 嘗試模擬時從下拉式清單中選取使用者，會使整個使用者快顯視窗消失。 NPR-15774:CQ-4201738/GRANITE-11895的HotFix
* 在Omnisearch中，無法使用自動填入建議的標籤來搜尋。 NPR-15088:GRANITE-14426的修補程式。\
   注意：此修正需要Oak CFP 1.4.11或更新版本。

### 行動AEM作者{#mobile-aem-author}

* 將AEM Mobile和ContentSync封裝與混合應用程式搭配使用時，AEM會回應應用程式以最舊套件（而非應用程式所要求的套件）所提出的擷取要求（含時間戳記）。 NPR-15749:CQ-104153的修補程式

### 網站 {#sites-17}

* 如果用戶在激活工作流後修改頁面，則WCM核心中「工作流收件箱」的修改狀態不會更改。 NPR-15684:CQ-4196974的修補程式
* 當使用者按一下錨點圖示並新增名稱時，Touch UI的Rich Text Editor中的錨點外掛程式會產生不相容的HTML5。 它應在錨點元素的HTML5標籤中新增&#39;id&#39;屬性，而非&#39;name&#39;屬性。 NPR-15650:CQ-89782的修補程式
* 當建立具有多個欄位的中繼資料架構並套用至內容片段中繼資料時，內容片段中繼資料畫面不會建立捲軸，使這些欄位無法編輯。 NPR-15478:CQ-4202622的修補程式
* 編輯`TagInput`欄位元件不會針對對話框欄位顯示先前配置的值。 NPR-15464:CQ-4200360的HotFix

* 在「內容片段編輯器」UI中，當建立許多「內容片段」變數時，側面板不會顯示捲軸來導覽所有變數。 NPR-15445:CQ-4199444的修補程式
* 當使用者從直接群組中移除時，他們會新增至繼承的群組。 NPR-15400:CQ-98758的修補程式
* WCM編寫：Touch UI作者不允許編輯名稱中含有逗號的頁面。 NPR-15396:CQ-4199723的修補程式
* 使用Touch UI進行編寫時，函式`Granite.author.editableHelper.doSelectParent`會以錯誤的順序傳遞引數，導致JavaScript錯誤。 NPR-15349:CQ-4198594的修補程式
* 即使有選擇退出Cookie,ContextHub區段仍會顯示體驗。 NPR-15293:CQ-4198024的修補程式
* Classic UI中的投影片元件無法建立投影片，或拖放影像以建立新投影片。 NPR-15281:CQ-4194164的修補程式
* 不論使用者的權限為何，都會在「網站管理控制台」中顯示「建立」選項，例如「建立頁面」、「建立網站」、「建立即時副本」、「建立啟動」和「建立目錄」功能表項目。 NPR-15278:CQ-94436的修補程式
* 安裝AEM 6.2 Service Pack 1後，「包含子頁面」滑桿就會停止在頁面啟動時運作。 NPR-15230:CQ-4198449的修補程式
* 請求增強版本清除功能，以擷取和處理塊中的版本，並且還可以將指定路徑用於XPath查詢。 NPR-15186:CQ-109205的修補程式
* 「Sites」（網站）元件的「Page Properties」（頁面屬性）縮表徵圖簽上缺少「Clear」（清除）按鈕。 NPR-15143 CQ-4196997的修補程式
* 對於使用即時副本的網站，在網站管理控制台的「欄」窗格中選取「即時副本」核取方塊時，無法正確顯示即時副本狀態，只會顯示HTML標籤。 NPR-15108:CQ-97086的修補程式
* 在編輯內容片段時，如果使用者在收到貼文回應之前按完(「√」)進行編輯，編輯的內容便無法正確儲存。 NPR-15014:CQ-4194095的修補程式
* 在「時間彎曲」模式期間關閉「編輯」頁面並嘗試從網站管理員重新開啟頁面，會導致狀態為「500」的錯誤，而非重新開啟頁面。 NPR-14965:CQ-109647的修補程式：
* 在Digital Asset Manager(DAM)UI中，「使用者選擇器尋找可授權的項目」搜尋會造成「記憶體不足」例外。 NPR:一五三零七年：CQ-98542的修補程式

### 資產 {#assets-17}

* 在Omnisearch中搜尋資產後，選取資產並嘗試按一下「檢視屬性」以編輯屬性，然後「儲存」按鈕會將使用者重新導向至空白頁面。 NPR-15900:CQ-4202372的修補程式
* 資產使用者介面不會回應事件。 選取資產並按一下「發佈」或「轉譯」不會產生任何活動。 NPR-15828:CQ-4202247的修補程式
* 從「卡片」檢視發佈資產時，除非重新整理頁面，否則不會更新卡片以反映已發佈狀態。 NPR-15826:CQ-102732的HotFix
* 包含資產修補程式的累積修補程式。 NPR-15225
* 如果資產檔案夾的名稱包含&amp;符號(&#39;&amp;&#39;)字元，在導覽至資產時，檔案夾名稱無法正確顯示。 NPR-15775:CQ-4201735的修補程式
* 在資產檔案名稱中使用&amp;符號(&#39;&amp;&#39;)字元會在存取其屬性時造成問題。 NPR-15770:CQ-4201737的修補程式
* 在導覽「資產」並使用「欄檢視」顯示模式時，如果使用者在選取並按一下資產後重新整理頁面，則會顯示資產詳細資料，而非重新整理的內容。 NPR-15768:CQ-4201727的修補程式
* PDS擷取功能使用PDF服務的程式庫堆積，CPU使用率高達100%。 NPR-15606適用於GRANITE-12929的HotFix
* 使用Firefox瀏覽器存取「我的連結分享」UI時，不會顯示共用項目或使用者，而且畫面無法使用。 NPR-15539:CQ-4200992的HotFix
* 使用Digital Asset Manager時，如果頁面與一組影像相關聯，將影像移至新資料夾會中斷頁面關聯，而關聯的頁面會遺漏部分影像。 NPR-15538:CQ-111479的修補程式
* 在Dam Viewer元件中，使用「nosamplecontent」執行模式會導致動態媒體發生錯誤。 NPR-15449:CQ-4195425的修補程式
* 在建立視訊描述檔時，如果同時選擇高品質和中品質的視訊編碼預設集，則不儲存所做的變更。 NPR-15447:CQ-4195482的修補程式
* 即使資產上傳至品牌入口網站因伺服器錯誤回應而失敗，品牌入口網站UI上的狀態仍會更新為「已發佈」，因此很難追蹤遺漏的檔案。 NPR-15442:CQ-4197968的修補程式
* 將資產資料夾發佈至品牌入口網站（發佈需時超過一小時）時，有些檔案無法發佈。 NPR-15441:CQ-4199493的修補程式
* 在欄檢視中使用Asset Finder主控台時，嘗試建立資料夾失敗一次，但它在重試時成功。 NPR-15370:CQ-4199448的修補程式
* 如果DAM UI中選取的資產或檔案夾名稱中有逗號，則「參考」索引標籤將不可用，並顯示訊息「參考清單不適用於多個選擇」。 NPR-15362:CQ-4199721的修補程式
* 將資料夾發佈至品牌入口網站並不會變更資料夾的已發佈狀態，即使資料夾下的資產已成功發佈亦然。 NPR-15292:CQ-4197667的修補程式
* 在Touch UI中導覽至「資產」主控台時，啟用特定資產時會出現例外，如所示。 NPR-15217:CQ-108779的修補程式
* 當連線是透過代理伺服器時，將視訊發佈至Youtube。 NPR-15109:CQ-110332的HotFix
* 使用名稱包含點或句點(.)的資產 在資料透明資源中，不會解析為同一資產，而輸出路徑會終止於點。 NPR-15069:CQ-4195914的修補程式
* 將AEM 6.2升級至Service Pack1後，資產同步至Scene7失敗。 dam:Scene7FileStatus屬性會顯示「 `UploadFailed`」狀態，即使是已發佈資產亦然。 NPR-15269:CQ-4197708的修補程式

### 使用者介面{#user-interface-5}

* 在&#x200B;**[!UICONTROL Touch UI]**&#x200B;中，使用Internet Chrome瀏覽器版本56.0.2924.87時，對於沒有type=&#39;datetime&#39;的日期欄位，不會顯示儲存的日期。NPR-15383:GRANITE-16481的修補程式
* 在&#x200B;**[!UICONTROL Touch UI]**&#x200B;中，Rich Text Editor會在轉譯HTML表格時，從HTML表格中移除串流和標題元素。 NPR-15267:CRTE-41的修補程式
* `FileUpload Validator` 不處理自動啟動為真或手動呼叫並 `uploadFile()` 在這些情況下產生無效驗證報告的情況。NPR-15295:GRANITE-13499的修補程式

* Omnisearch不允許使用/apps的客戶新增欄資料來源，因為它假設位置設定列在&#x200B;*/libs/granite/omnisearch/content/metadata/*&#x200B;下。 NPR-13188 GRANITE-16479的修補程式
* 使用&#x200B;**[!UICONTROL Touch UI]**&#x200B;時，不會在產品的相同層級建立產品變數。 用戶未獲知變型建立過程的狀態。 NPR-15345:CQ-4198948的修補程式

**Scene7**

* 執行Scene7工作流程會導致開啟的檔案無法關閉。 要求改善AEM-S7服務，以便維護並重複使用具有共用集區設定的單一HttpClient例項。 NPR-15357:CQ-109958的HotFix

### 轉換 {#translation-9}

* 使用翻譯專案時，從英文主版更新語言副本，會產生11個不同的啟動，所有啟動都使用相同的名稱和來源根目錄，但啟動根目錄稍有不同，以備頁面名稱遵循設定模式時使用。 NPR-15605:CQ-4200699的修補程式
* 當語言根的名稱中包含連字型大小和破折號時，不會為頁面建立翻譯項目。 NPR-15171:CQ-96286的修補程式
* 要求更新Microsoft連接器，以便能夠使用Microsoft Translator API,Microsoft會在Azure入口網站中提供此API。 NPR-15320:CQ-101010的修補程式

### 專案 {#projects-4}

* 「項目螢幕」中只能顯示20個非活動項目，但儲存庫中有20多個非活動項目。 NPR-15656:CQ-4200903的修補程式

### 行銷活動 {#campaign-1}

* 使用「促銷活動——定位」和「MAC —— 測試和定位」整合元件時，取消發佈活動不會更新主UI中的活動狀態。 NPR-15401:CQ-4199839的修補程式
* 在AEM Commerce中移動產品時，「產品移動精靈」會遺漏產品名稱、標題、參考頁面、建立作者和建立日期的預先填入值。 NPR-15228:CQ-98617的修補程式

### 安全性 {#security-4}

* 使用GET方法新增至表單的CSRF Token參數。 NPR-15229

### 表單 {#forms-18}

#### Forms add-on package {#forms-add-on-package-18}

`**Adaptive Forms**`

* 當使用輸入XML預先填入最適化表單時，預設值會以xml中的空值覆寫。 NPR-15721
* `afData/afBoundData`包裝函式存在於已提交的XML中，但即使預填充XML在基於XML架構的自適應表單中也沒有`afData/afBoundData`包裝函式。 NPR-15541

* Accordion列中的標題應是可編輯的HTML &#39;h2&#39;標題，而非&#39;a&#39;標籤。 NPR-15475
* 螢幕閱讀程式使用者無法存取表單面板的accordion版面。 使用者無法使用螢幕閱讀程式軟體（例如JAWS或NVDA），僅透過鍵盤導覽至accordion標籤。 NPR-15474

`**Correspondence Management**`

* 儲存、刪除和設定檔案片段的參考需要相當長的時間。 NPR-15939
* 在CCR UI中，在「管理資產」中設定的標籤對齊方式包含多個標題分頁符。 NPR-15818
* 「文字」模組的縮圖不會顯示對齊的內容，不過文字包含使用Google Chrome中的「標籤」建立的對齊內容。 NPR-15819

`**Forms Portal**`

* 預填服務不適用於XDP表單。 NPR-15466
* 將自適應表單草稿和提交儲存到資料庫時，當資料庫連接因任何原因（例如，長時間不活動後）而失敗時，自適應表單的狀態將損壞。 NPR-15297

#### Forms JEE安裝程式{#forms-jee-installer-18}

`**Core**`

* 升級至最新版Java 1.8.0_121-b13後，AEM Forms將無法存取管理員使用者介面。 NPR-15330

`**XTG**`

* 當使用輸出服務將特定表單與資料軸合併時，響應時間是ES4 SP1伺服器執行相同操作所花費時間的20倍。 NPR-15283

#### AEM Forms App {#aem-forms-app-1}

* 恢復未保存的任務時，需要更清楚地顯示恢復未保存任務時顯示的消息，以減少用戶錯誤。 NPR-15377
* AEM Forms應用程式不會轉譯從自訂範本建立的表單。 NPR-15892
* 使用者無法登入AEM Forms應用程式。 NPR-15891

AEM 6.2 SP2-CFP1的主要亮點為：

* 優化站點中的複製功能：

   * 修正各種Roploat、LiveCopy和寫作問題

* 在下列期間增強Touch UI回應速度：

   * 資產搜尋
   * 大小排序

* 增強智慧型系列中的標籤管理
* 對資料夾執行CRUD操作期間更嚴格的訪問控制

### 平台 {#previous}

* 請求在啟動複製代理期間刪除`ReplicationQueue#forceRetry` API調用，因為此類調用會顯著減慢實例的速度，特別是當實例具有多個複製代理時。 NPR-14032:GRANITE-13095的修補程式
* 請求`DurboImportConfigurationProviderService` OSGi配置以支援可儲存陣列值的欄位。 NPR-14570:CQ-108684的修補程式
* 移轉至AEM 6.2後，在頁面中使用Sightly元件會導致頁面的「屬性」對話方塊停止運作。 NPR-14328:CQ-108355的修補程式
* 取消調度以前調度的作業不會刪除&#x200B;*/var/eventing/scheduled-jobs*&#x200B;下的相應節點。 NPR-14253:SLING-5666的修補程式
* 當管理員嘗試模擬為已刪除的使用者時，使用者介面無法重新整理。 NPR-14247:CQ-107446的修補程式
* XSS保護檢查造成Sightly元件中的編碼錯誤。 NPR-14004:CQ-93821的修補程式
* 請求將Jackrabbit Filevault升級至3.1.30以解決多個問題。 NPR-13454
* 當Sling散發將散發套件從作者同步至發佈時，會發生快取錯誤。 NPR-13034:GRANITE-13970的修補程式

### 網站 {#sites-18}

* VersionManager問題實施從版本歷史記錄中清除錯誤版本。 NPR-14372
* WCM Sightly Foundation parsys元件忽略元件聲明標籤名稱`cq:htmlTag / cq:tagName`。 NPR-14225
* 當使用Sightly Parsys來轉換透過Touch UI中的JavaScript插入的元件時，在重新整理頁面後會忽略自訂裝飾。 NPR-14122
* 當建立多個Richtext欄位（例如連結）時，Target下拉式清單無法在Touch UI對話方塊中運作。 NPR-13911
* 在對話框(Touch UI)中使用多個富格文本編輯器(RTE)屬性編輯文本欄位時，焦點會隨機切換到特定的RTE屬性。 NPR-13703
* 預設的開箱即用視訊元件不會呈現視訊縮圖。 NPR-14976
* 在範本編輯器的「即時使用實例」索引標籤中，資訊會慢慢載入。 NPR-14880:CQ-83417的修補程式
* 在AEM 6.2例項上安裝Hotfix-10936會停用iparsys元件。 NPR-14330:CQ-106982的修補程式
* 移轉至AEM 6.1 SP1後，出現多重轉出元件問題和即時副本問題。 NPR-15256
* 「頁面展開」動作無法建立超過第一層的子系，即使對於多個展開設定亦然。 NPR-15055
* 從編輯器提交PageProperties對話方塊時，LiveCopy標籤中未變更的資料會重寫。 NPR-14693
* 當從編輯器提交「PageProperties」對話框時，MSM後處理器會從請求中寫入一些參數，而不是`msm:writeLiveCopyConfig`參數。 NPR-14434
* 與MSM的Lovolt元件、即時副本和其他方面相關的多個問題。 NPR-12235

### 資產 {#assets-18}

* UnPack Workflow無法處理影像檔案名稱中具有特殊字元的影像。 NPR-15227:CQ-103887的修補程式
* 具有「重複與條件」運算式的資產無法正確顯示。 當使用者預覽`*CDN3835RLCEN*`字母範本時，不會顯示位於Body目標區域中的資產。 當預先選取的資產`*VIPReassement*`為選用資產時，會取消選取該資產，則預先選取的其他資產會顯示在字母中。 NPR-14844

* 建立智慧型系列時，儲存智慧型系列時，不會保留樣式標籤。 NPR-15081:CQ-4195494的修補程式
* 資產搜尋查詢在多個使用者同時搜尋期間在觸控式UI中執行緩慢。 NPR-15019:CQ-4195405的Hotifx
* 為類型`Long[]`的屬性提取的中繼資料會在原始資產重新上傳至不同位置時轉換為類型`String[]`。 NPR-15016:CQ-4195005的修補程式

* 使用者無法刪除儲存的搜尋或智慧型系列。 NPR-14924:CQ-108494的修補程式
* 在基礎中繼資料結構的下拉式欄位中，使用TypeHint的布林值，大量編輯資產的中繼資料（附加模式）時，會產生錯誤。 NPR-14529:CQ-106876的修補程式
* 沒有複製權限的用戶無法刪除資產資料夾。 NPR-14321:CQ-88271的修補程式
* 嘗試在頻道編輯器中編輯視訊的視訊描述檔時，設計對話方塊不會開啟，並會在錯誤記錄中引發「空指標例外」。 NPR-14144:CQ-81101的修補程式
* 資產屬性頁面中顯示的系統產生的「已建立」時間戳記屬性不正確。 NPR-13992:CQ-95029的修補程式
* 請求在AEM Assets NPR-13851中為沒有讀取存取權的使用者啟用重複資產的偵測：CQ-102281的修補程式
* 使用者無法從屬性頁面大量編輯資產的中繼資料。 NPR-13721:CQ-100703的修補程式
* 上傳重複資產時，Classic UI中的錯誤訊息不正確。 錯誤訊息未指出上傳失敗的原因。 NPR-13691:CQ-99272的修補程式
* AEM Assets無法在「清單」檢視中，當資料夾包含許多資產時，依大小一次排序超過50個資產。 CQ-100588
* 如果資產／資料夾URI太長，選取多個資產會導致回應代碼- 414（請求-URI過長）錯誤。 NPR-13516:CQ-76076的修補程式
* 當使用者在「設定欄」對話方塊中選取所有選項時，「資產報表」頁面會停止回應。 NPR-13187:CQ-95589的修補程式
* Safari和Internet Explorer中的標籤選擇器非預期行為。 NPR-13134
* 從「資產管理搜尋」邊欄編輯儲存的搜尋，可將搜尋儲存為巢狀智慧型選取範圍，這會造成環境穩定性問題。 NPR-13119:CQ-99460的修補程式
* 移動檔案（或檔案夾）並重新命名後，「cq:name」中繼資料不會反映新的檔案名稱（檔案夾名稱）。 NPR-13036:CQ-99141的修補程式
* 無法從透過電子郵件共用的下載連結下載名稱包含特殊字元的資產。 NPR-12872:CQ-95795的修補程式
* 當大量資產產生時立即可用的資產報表，會造成大量橫穿，而搜尋未達到任何索引和CPU使用量尖峰。 NPR-12811:CQ-84409的修補程式
* AMS AEM Assets的使用者從不同的網路建立執行個體存取，無法使用區塊上傳來上傳資產，而沒有檔案夾的刪除權限。 NPR-12768:CQ-82715的修補程式
* 在使用「資產搜尋」邊欄的標籤式資產搜尋中，「超前輸入」功能不會限制為根路徑，並會顯示所有名稱空間的標籤。 NPR-12666
* StaticRenditions元件提出空指針異常。 NPR-12665
* 請求停用MissingMetadataNotificationJob，因為這會導致徽章通知UI中斷頁面，但執行階段例外為「無法掃描輸入」。 NPR-12500:CQ-93573的修補程式
* 標籤欄位的「停用編輯」選項無法在TouchUI的資產屬性頁面中運作。 NPR-12429:CQ-88835的修補程式
* AEM Assets 6.2 for Companion App SMB實作中的API修正。 NPR-11099
* 自從Jquery更新後，使用者便無法選取資產系列，並在「關聯內容」面板中確認內容片段的選取。 NPR-14847:CQ-4194209的支援埠
* 雖然在用戶端叫用無限排序，但UI中目前只會顯示文章／橫幅／系列。 NPR-14493:CQ-109926的修補程式
* 要求為AEM Mobile-on-demand服務實作Omnisearch功能。 任何文章、系列或橫幅的關鍵字搜尋不會傳回任何相符項目。 NPR-14093:CQ-101394的修補程式
* 在對話方塊中使用Coral-select元件(*granite/ui/components/coral/foundation/form/select*)時，當選取的值包含單一項目時，Internet Explorer（IE11或Edge瀏覽器）的值初始化無法正常運作。 NPR-13395:CQ-101013的修補程式

### 專案 {#projects-5}

* 將使用翻譯方法建立的翻譯項目導出為&#39;human&#39;，將翻譯提供程式導出為&#39;none&#39;時，不會生成translation_export_summary.xml檔案，因為缺少GUID映射檔案。 NPR-13137:CQ-91976的修補程式
* 在AEM專案中，當建立具有due-date屬性設定的專案時，由於伺服器和用戶端之間的時區差異，日期轉換會不正確地設定時間。 NPR-13003:CQ-98288的修補程式
* 更新翻譯項目時，翻譯作業中會遺漏「在站點中顯示」選項。 NPR-12966:CQ-93740的修補程式
* 為導出的站點頁面建立翻譯項目時，它無法在預覽中正確顯示。 NPR-12964:CQ-84627的修補程式

### 工作流程 {#workflow-3}

* 在「工作流控制台」的「封存」索引標籤中，裝載連結會在按一下時傳回回回應代碼為「404」的錯誤。 NPR-14993:CQ-4194977的修補程式
* 使用AEM預設工作流程時，CQ Mailer無法傳送電子郵件通知給遺漏單一成員電子郵件地址的群組。 NPR-14804:CQ-91499的修補程式要求
* Touch UI中收件匣和通知徽章的效能改進。 NPR-14145:CQ-101125的修補程式
* 啟始工作流程時，使用者無法從工作流程「收件匣」主控台預覽裝載。 NPR-13226:CQ-100275的修補程式
* 使用SAML驗證處理常式設定的&#39;saml_request_path&#39; Cookie會顯示以額外&#39;?&#39;設定的Cookie 字元。 此外，當SAML回應張貼回AEM時，AEM &#39;saml_request_path&#39; Cookie會因為已編碼字元而傳回無效值。 NPR-13517:適用於GRANITE-11722和GRANITE-14414的主動式修補程式

### 解決方案整合{#solution-integration}

* 在將AEM 6.2與Search&amp;Promote整合後，如果使用者搜尋傳回橫幅的詞語，搜尋功能就會停止回應。 NPR-14549:CQ-109631的CFP

### 動態媒體 {#dynamic-media}

* 在AEM啟動期間建立和取消的許多AEM-Scene7 sling作業在複製期間記錄為封存作業。 NPR-12835:CQ-86115的修補程式

### 安全性 {#security-5}

* 要求解決WCMDebug篩選器中的輸入驗證問題。 NPR-12444:CQ-94890的修補程式要求
* 使用「建立啟動精靈」時，主動要求更正XSS行為。\
   NPR-13062:CQ-99577的修補程式要求

#### Forms add-on package {#forms-add-on-package-19}

`Adaptive Forms`

* 使用可調式表單建立可重複的面板時，無法在執行時期更新面板標題。 NPR-15325
* 當設定選項按鈕的預設值，並在儲存或提交時選取預設值以外的值時，預先填寫時不會顯示該值。 NPR-15304
* Google Chrome顯示使用選項事件動態填入下拉式清單及送出選取項目值時的錯誤行為。 NPR-15198
* 使用可調式表單建立可重複的面板時，無法在執行時期更新面板標題。 NPR-15181
* 當針對最適化表單使用編輯模式時，會遇到JavaScript錯誤，例如- &#39;元件的處理常式無效&#39;和&#39;guidelib is undefined&#39;。 NPR-15112
* 重複面板中的延遲載入片段無法如預期般運作。 NPR-13916、NPR-14785

`Correspondence Management`

* 具有`'Repeat with condition'`運算式集的Correponse Management資產無法正確顯示。 NPR-14844
* 在搜尋「對應管理」資產（例如信件、檔案片段或任何其他類型）時，工具列中的「下載佇列」圖示會遺失。 NPR-14745
* 在建立清單模組時，切換資產特定屬性（例如可編輯、強制）無法運作。 NPR-14689
* 運算式產生器公用程式中的「資料元素」面板會持續載入，以防條件模組建立時，不需選取資料字典。 NPR-14688
* 在預覽字母時，使用者無法使用索引標籤空格來對齊表格格式的內容。 NPR-14481
* 從使用者介面大量匯出「對應管理」資產時，AEM Forms伺服器會產生不必要的記錄檔。 NPR-15226
* 當預覽字母時，對齊文字會以不同的字型顯示。 NPR-15468

`**Forms Portal**`

* 提交從入口網站提交的新草稿時，Forms入口網站中已提交表單的附件不可見。 NPR-13515

`**Forms Manager**`

* 在&#x200B;*FormsandDocuments*&#x200B;目錄中導覽時，當使用者複製任何資產然後導覽至其他資料夾時，不會顯示「貼上」按鈕。 CQ-111327

#### Forms JEE安裝程式{#forms-jee-installer-19}

`Rights Management`

* 用戶登錄相關審計事件以無效的時間記錄。 稽核事件的正確時間無法追蹤。 NPR-13107
* Adobe Acrobat Reader和Microsoft Office無法開啟使用延伸驗證保護的檔案。 NPR-14482

`Process Management`

* 當將HTML工作區中轉發的草稿任務返回給初始用戶時，該任務不會出現在初始用戶的隊列中。 NPR-15178

`Assembler Service`

* AEM Forms無法使用兩個以上的簽名來驗證PDF/A-2b。 NPR-14101

`XTG`

* 使用打印機旁路紙盒打印文檔時，`GeneratePrintedOutput`功能不允許從右旁路紙盒取紙。 NPR-14079

#### Forms Designer {#forms-designer-2}

* 當使用者以法文（加拿大）的形式執行具有選定「表單地區設定」的「拼字檢查」公用程式時，Forms Designer會當機。 NPR-13740
* 當使用者為表單欄位選擇計算事件或驗證事件，並將語言變更為JavaScript，並在&#x200B;**[!UICONTROL 指令碼編輯器]**&#x200B;視窗中輸入`this.`時，表單設計器會當機。 NPR-12974

### CFP1包含的功能套件{#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms Add-on Package):

* 當從XDP檔案建立最適化表單時，無障礙環境支援的標籤不會遵循設定模式。 NPR-12562

`Adaptive forms` (Forms Add-on Package):

* 最適化表單的規則產生器不提供角色存取。 作者所做的變更無法追蹤。 NPR-12840

`Core` （Forms JEE安裝程式）:

* Jboss+未啟用核心跨原始資源共用(CORS)作為servlet篩選器的功能。 NPR-13050

## 透過軟體散發下載CFP的指示{#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>對於AEM Forms客戶，在安裝任何AEM Service Pack、Cumulative Service Pack或Feature Pack後，必須安裝AEM Forms附加套件。

您可以直接從「軟體散發」下載CFP套件，或執行下列步驟：

1. 開啟[軟體分發](https://experience.adobe.com/downloads)。 您必須有Adobe ID才能登入「軟體散發」。
1. 點選頁首功能表中的「Adobe Experience Manager **[!UICONTROL 」。]**
1. 點選套件名稱，選取「**[!UICONTROL 接受EULA條款]**」，然後點選「**[!UICONTROL 下載]**」。

## CFP {#installation-instructions-for-cfp}的安裝指示

本節會逐步帶您瞭解安裝CFP的需求和步驟。

### 安裝{#before-you-install}之前

>[!NOTE]
>
>Adobe提供的選購功能套件與發行版本和累積修補程式套件有相依性。 如果您已安裝任何功能套件，請聯絡[AEM客戶服務團隊](https://helpx.adobe.com/tw/marketing-cloud/contact-support.html)以驗證此AEM 6.2版累積修補程式套件的相容性。

>[!NOTE]
>
>建議您在嘗試安裝軟體包之前，先對每個新安裝軟體包運行驗證。 預先驗證會分析並報告在安裝前發現的任何錯誤，並主動警告使用者此類錯誤、覆蓋、權限。
>
>您可以在[https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)存取「驗證」選項的檔案

* AEM 6.2 Service Pack 1是CFP的先決條件。 如需安裝指示，請參閱[AEM 6.2 Service Pack 1發行說明](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。

* Cumulative Fix Pack下載可從[Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20)取得，您可以直接從AEM例項存取。
* 對於使用（RDBMK或MongoDB）的叢集部署，CFP套件可安裝在任何使用Package Manager的Author執行個體上。

* 在安裝累積修補程式套件之前，請確定要建立快照或備份您的AEM實例。
* 不支援解除安裝CFP。

### 透過軟體散發安裝CFP {#install-the-cfp-via-package-share}

請執行下列步驟，在現有的AEM 6.2 SP1執行個體上安裝Cumulative Fix Pack:

1. 按一下[軟體分發](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip)連結下載軟體包。

1. 開啟[包管理器](http://localhost:4502/crx/packmgr/index.jsp) ，然後按一下&#x200B;**[!UICONTROL 上載包]**&#x200B;來上載包。

1. 選擇軟體包名稱，然後按一下&#x200B;**[!UICONTROL Install]**。

### 自動安裝{#automatic-installation}

CFP可透過下列方式自動安裝至執行中的執行個體：

* 在伺服器運行時，將軟體包放入。./crx-quickstart/install中。 軟體包會自動安裝。
* 使用Package Manager的[HTTP API ](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) —— 請確定您使用`cmd=install&recursive=true` —— 如此巢狀套件便已安裝。

### 驗證安裝{#validate-installation}

1. 「產品資訊」頁面(/system/console/ productinfo)現在應在「已安裝產品」下顯示更新版本字串「Adobe Experience Manager, Version 6.2.0.SP1-CFP20」。
1. 所有OSGI組合在OSGI主控台中都是ACTIVE或FRAGMENT(使用Web主控台：/system/console/bundles)。

>[!NOTE]
>
>成功安裝套件時，會出現資訊性訊息，指出內容套件已成功安裝，例如「Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20已成功安裝」。

>[!NOTE]
>
>自從AEM 6.2 SP1-CFP1起，Jackrabbit FileVault中的記錄檔層級已針對大部分訊息從INFO變更為DEBUG。 若要取得安裝在AEM 6.2 SP1-CFP1或更新版本的內容套件的安裝記錄檔，請啟用`org.apache.jackrabbit.vault.packaging.impl`的DEBUG記錄檔層級。

### 安裝AEM Forms {#install-forms}

>[!NOTE]
>
>如果您不使用AEM Forms，請略過本節。

#### 安裝AEM Forms附加元件{#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms on JEE**)在JEE的AEM Forms上安裝CFP的程式，請參閱[在AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee)上安裝CFP。

1. 請確定您已安裝AEM 6.2 SP1 CFP套件。
1. 針對您的作業系統，下載列在[AEM Forms發行版](aem-forms-releases.md)的對應Forms附加元件套件。
1. 如[安裝AEM Forms附加套件](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html)中所述，安裝Forms附加套件。

#### 安裝AEM Forms JEE bundles套件{#install-aem-forms-jee-bundles-package}

AEM Forms JEE中的修正會透過個別安裝程式提供。 如需在JEE的AEM Forms上安裝CFP的詳細資訊，請參閱[在AEM Forms JEE上安裝CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer安裝程式{#designer-installer}

1. 要安裝更新，請運行Designer6.2.0_&lt;Language>_Cumulative_QF.msp檔案。
1. 在歡迎畫面上，按一下&#x200B;**update**。 安裝開始。
1. 安裝完成後，按一下&#x200B;**finish**。

## DTM、Analytics、Target、Search &amp; Promote連線的使用者可設定逾時參數{#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

在AEM Cumulative Fix Pack 6.2 SP1-CFP7及更新版本中，已針對上述所有連線設定連線逾時期，詳細資訊如下：

| **連線** | **連線逾時*** | **通訊端逾時**** |
|---|---|---|
| DTM | 30000ms | 30000ms |
| 分析 | 30000ms | 30000ms |
| 目標 | 60000ms | 30000ms |
| Search&amp;Promote | 30000ms | 30000ms |

* **連線逾時*** —— 連線建立前的逾時（毫秒）。逾時值零會被解讀為無限逾時。
* **通訊端逾時****-等待資料或兩個連續資料封包之間最長閒置時間的逾時（毫秒）。

>[!NOTE]
>
>在AEM Cumulative Fix Pack 6.2 SP1-CFP6及更新版本中，用於「搜尋與提升整合」的OSGi組態是Apache HTTP Components Proxy組態。 不再使用Day Commons HTTP Client 3.1的Proxy設定。

## 在標籤控制台(Classic UI)(NPR-15842){#disable-replication-status-in-tagging-console-classic-ui-npr}中禁用複製狀態

如果您使用CFP3或更新版本，請依照下列指示，在Classic UI的「標籤」主控台中停用複製狀態：

* 覆蓋&#x200B;*/apps*&#x200B;中的&#x200B;*&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;*

* 添加`replicationStateRequired`:第416行後面的&quot;false&quot;。

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## 最新的Java 8更新131引發例外(NPR-21355){#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>這些設定設定是針對使用Document安全性的AEM Forms客戶而設定。

CFP12.1中包含NPR-21355。如果您要安裝CFP12.1或更新版本，請執行下列程式，在JBoss應用程式伺服器上配置NPR-21355。 如果您要在Oracle WebLogic或IBM WebSpehere應用程式伺服器上執行的AEM Forms伺服器上安裝CFP12.1，則不需要額外的設定：

1. 備份、刪除和建立新的module.xml檔案。 檔案的預設位置為[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. 開啟新建立的module.xml檔案以進行編輯。 將下列程式碼新增至檔案：

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

1. 建立位於[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/的jsafeFIPS.jar、jsafeJCEFIPS.jar和certjFIPS.jar檔案的備份，並從前述目錄中刪除檔案。

   請聯絡[Adobe支援](https://helpx.adobe.com/marketing-cloud/contact-support.html)以取得新的JAR檔案。 將從[Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html)取得的JAR檔案置於[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. （僅限Windows）修改`[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat`或`domain.conf.bat`配置檔案：

   * 對於獨立配置中的JBoss伺服器，請開啟standalone.conf.bat進行編輯。
   * 對於群集配置中的JBoss伺服器，請開啟domain.conf.bat進行編輯。

   在結尾處添加以下行並保存檔案：

   設定&quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   設定&quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. （僅限Linux作業系統）修改[AEM_Forms_Installation_directory]/jboss/standalone.conf或domain.conf組態檔案：

   * 對於獨立配置中的JBoss伺服器，請開啟standalone.conf進行編輯。
   * 對於群集配置中的JBoss伺服器，請開啟domain.conf進行編輯。

   在結尾處添加以下行並保存檔案：

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## NPR-19778 {#configuration-settings-required-for-npr}所需的配置設定

>[!NOTE]
>
>NPR-19778是CFP14的一部分。

預設情況下，當用戶聲明任務時，不會刷新其他用戶的共用隊列計數。 為此，我們引入了一種新屬性。 請依照下列步驟，在您的AEM例項上設定此屬性：

1. 前往「管理員UI ->服務->工作區->全域管理」。
1. 匯出全域設定。
1. 在下載的XML檔案中，新增`<client_tasksPollingInterval>10</client_tasksPollingInterval>`標籤。10是以秒為單位的範例值。 您可以相應地修改它。
1. 儲存檔案。
1. 返回「管理員UI ->服務->工作區->全域管理」。
1. 在「匯入全域設定」區段中匯入xml檔案。
1. 您現在可以註銷系統並重新登錄。
1. 共用佇列的計數會開始重新整理工作區中的其他使用者。
1. 若要關閉輪詢，請將值更改為0，然後再次導入XML檔案。

## UI變更{#ui-changes}

* 在具有dc的影像的影像卡上顯示標題的行為變更：title屬性設定為字串[](multifield):在UI中，影像卡上只會顯示最新變更的標題，不過所有標題都會儲存在CRX中。 CQ-4217165的修補程式

## 已知問題 {#known-issues}

* 從CFP18更新AEM 6.2SP1-CFP19和AEM 6.2SP1-CFP20會變更根目錄，將其重新導向至Classic UI歡迎頁面，而非/sites.html/content。 您可能必須修正sling:使用CRX Explorer將target屬性從/welcome.html移至/index.html。 在從CFP17或舊版更新時，未發現此問題。

當您安裝AEM 6.2 SP1-CFPx時，可能會發生下列暫時錯誤。 不過，這些錯誤不需要解決方法，因為它們不會影響您的AEM執行個體，並在安裝CFP後離開：

* 在將AEM 6.2SP1-CFP20執行個體升級至AEM 6.5時，有些虛名URL可能無法運作：

   * */projects.html*
   * */sites.html*

不過，因應措施是在升級後重新啟動AEM例項。

* 開啟Webconsole元件詳細資訊頁時，會收到HTTP 500內部伺服器錯誤。
* **create component instance**&#x200B;和&#x200B;**服務工廠返回的錯誤由於儲存庫重新啟動而發生：**

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)]由於無法綁定引用profileManager，無法建立元件實例
   * org.apache.sling.commons.schedulerFrameworkEvent ERROR(org.osgi.framework.ServiceException:服務工廠返回空值。 (元件：com.day.cq.tating.impl.TagGarbageCollector(1687))

* 在Mongo和DB2中CFP安裝中觀察到的錯誤：**org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry:例外：java.lang.NullPointerException**。 在CFP8上安裝CFP後，不會發生此錯誤。
* (Adobe Granite Maintenance Scheduler Update Task)com.adobe.granite.maintenance.impl.TaskScheduler:找不到名為WorkflowPurgeTask的維護任務（用於窗口granite:weekly）
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
* 當您在AEM 6.2 SP1（包含智慧型標籤功能套件）上安裝CFPx時，先前新增的智慧型標籤資產的工作流程步驟會從DAM更新資產工作流程中刪除。

請參閱AEM 6.2 SP1]中的[已知問題清單(https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known問題)。

## Uber Jar {#uber-jar}

6.2 SP1-CFP20版Uber Jar可在[Adobe Public Maven存放庫](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/)取得。

要在Maven項目中使用Uber Jar，請在項目POM中包括以下相關性：

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## 包含{#osgi-bundles-and-content-packages-included-5}的OSGI組合和內容封裝

以下文字記錄CFP中OSGI組合和內容套件的清單。

* [AEM 6.2 SP1-CFP20隨附的OSGi搭售清單](assets/do-not-localize/updated.txt)
* [AEM 6.2SP1-CFP20內容套件清單](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2修補程式頁面](https://helpx.adobe.com/experience-manager/kb/aem62-available-hotfixes.html)
>* [AEM 6.2 SP1版本注意事項](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [AEM 6.2版本注意事項](https://docs.adobe.com/docs/en/aem/6-2/release-notes.html)
>* [AEM產品頁面](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.2 檔案](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [訂](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) 閱 [Adobe優先產品更新](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

