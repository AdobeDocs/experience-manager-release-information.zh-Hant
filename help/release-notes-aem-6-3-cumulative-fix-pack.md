---
title: AEM 6.3 Cumulative Fix Pack
description: AEM 6.3 Cumulative Fix Pack 發行說明。
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
source-git-commit: e9031f819352f34248c6a458ef5a9101a660fbea
workflow-type: tm+mt
source-wordcount: '15909'
ht-degree: 99%

---

# AEM 6.3 Cumulative Fix Pack 發行說明 {#release-notes-aem-cumulative-fix-pack}

## 發行資訊 {#release-information}

| **產品** | Adobe Experience Manager |
|---|---|
| **版本** | 6.3 |
| **發行** | [軟體發佈](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) 上的 Cumulative Fix Pack 6.3.3.8 |
| **必備條件** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **正式發行** | 2020 年 3 月 5 日 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe 針對發行修正推出單一交付模式。Adobe 現在改採每個月發行一個 Cumulative Fix Pack (CFP) 的方式 (可能因通過品質檢查的情況而異)，而非針對個別問題發行 Hotfix。CFP 是多個修正的彙總式內容套件。CFP 主要包含錯誤修正，但也可能包含 Feature Pack。比起發行個別 Hotfix，這種方式的優點如下：

* 本質上為累積性質 (例如 CFP 包含透過先前版本 CFP 提供的修正)
* 提高品質保證
* 簡化安裝程序 (使用者以無相依性的單一套件安裝 CFP 即可，但最新版 Service Pack 除外)

如需更多有關 CFP 和其他發行版本的相關資訊，請參閱[維護版本工具定義](https://docs.adobe.com/content/docs/zh-Hant/aem/6-3/deploy/maintenance-release-vehicle-definitions.html)。

## 關於發行版本 {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.8 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.20 版。

>[!CAUTION]
>
>如果未確認與已安裝的 Feature Pack 之間的相容性就套用 CFP，可能會導致系統失敗或遺失自訂設定，上述情況可能需要從備份復原才能解決。

>[!NOTE]
>
>若使用版本低於 6.3.3.0 的 AEM 執行個體，Adobe 建議針對 AEM 執行個體上有大量使用者的客戶，透過安裝資料夾來部署 SP/CFP。

>[!NOTE]
>
>AEM 6.3.3.1 版開始支援 MongoDB Enterprise 3.6。

## 問題清單 {#changes}

本節列出此版 CFP 中所包含的所有問題和 Hotfix。

此外，此版 CFP 也包含[先前版本 Cumulative Fix Pack](#previous) 提供的 Hotfix。

### 資產 {#assets}

* 將資產新增至集合時，「新增至集合」頁面沒有在「卡片檢視」中顯示所有可用的集合 (NPR-32537)。

### 網站 {#sites}

* 選取 parsys 和其中的元件，並使用鍵盤快速鍵來刪除所選項目時，此操作會同時刪除元件和其上層 parsys (NPR-32071)。
* 儲存頁面屬性時建立了錯誤的節點 (NPR-31774)。

### Integrations {#integrations}

* ReportSuitesServlet 容易遭受 SSRF 攻擊 (NPR-32162)。

### Campaign 目標定位 {#campaign-targeting}

* 在製作執行個體中變更元件的內容然後啟用，但在元件重新啟動前不會顯示在發佈執行個體中&#x200B;**com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 和 NPR-32232)。
* 發佈時 Contexthub 效能當機 (NPR-31170)。

### Brand Portal {#brand-portal}

* Adobe I/O 沒有針對 Brand Portal 與 Adobe Experience Manager 6.3 整合 (NPR-32056)。

### Forms {#forms}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

#### Forms 附加元件套件 {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms 附加元件套件用於協助讓表單功能與 AEM Service Pack 和 Cumulative Fix Pack 一致。因此，必須先安裝任何 AEM Service Pack、Cumulative Fix Pack 或 Feature Pack，才能安裝 AEM Forms 附加套件。

* Designer：如果已啟用標記選項，所產生 PDF 輸出中的子表單邊界會消失 (NPR-32324 和 NPR-32545)。
* Designer：如果表格中有合併的儲存格，協助工具測試就無法輸出透過輸出服務從 XDP 表單轉換而來的 PDF 檔案 (NPR-32068)。
* 文件安全性：`DisableGlobalOfflineSynchronizationData` 選項若設為 `True`，受保護的 PDF 檔案就無法離線開啟 (NPR-32080)。

**在 6.3.0-0047 中修正的問題**

* (僅限 JEE) 針對 Apache Log4j2 回報的重大安全漏洞 (CVE-2021-44228 和 CVE-2021-45046)。

## 先前版本 Cumulative Fix Pack 中包含的 Hotfix 和 Feature Pack {#previous}

### Cumulative Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.7 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

### 資產 {#assets-1}

* 從「僅限內容」下拉式功能表中選取篩選器選項之前就已選取資產 (在觸控式 UI 裡的欄檢視中)，然後選取移動選項也遭移動 (NPR-30693)。
* 處理工作流程時沒有在製作執行個體中轉譯 `${extension}` 變數 (NPR-31694)。
* 針對 Dynamic Media 混合模式設定的到期 (用戶端快取的存留時間) 值沒有複製到 Dynamic Media 交付環境中 (NPR-31114)。
* 即便使用預設篩選器後，資產仍從在 Dynamic Media - Scene7 部署中執行的製作執行個體複製到發佈執行個體 (NPR-30856)。

### 網站 {#sites-1}

* 主版頁面的頁面屬性無法載入，並傳回 NullPointerException。新增 cq:blueprint 屬性解決了此問題 (NPR-30901)。
* 未從根節點上的 blueprintConfig 正確擷取轉出設定。同時對 Blueprint 和 Live Copy 觸發了停用。應該只對 Blueprint 觸發停用 (NPR-30866)。
* 使用者轉出頁面時，轉出設定對話方塊顯示重複的 Live Copy 路徑 (NPR-30438)。
* 現成的支架 RTF 編輯器 (RTE)。未預期地對元素套用內嵌字型大小 (NPR-31283、NPR-30922)。
* 無法在包含現成設計匯入工具元件的 Adobe 促銷活動中的同步處理促銷活動 (NPR-30890)。
* RTF 編輯器 (RTE)。不允許將內嵌表格插入為清單項目 (NPR-30878)。
* 當使用者聚焦於左方邊欄的欄位，並使用鍵盤快速鍵貼上內容時，貼上了頁面編輯器剪貼簿的內容，而非左方邊欄的欄位內容 (NPR-31173)。
* 使用者編輯內容片段時，系統復原了已刪除的內容片段變化 (NPR-31272)。
* AEM Site 不提供建立語言副本的選項 (NPR-30690)。
* 頁面編輯器的動作無法控制轉出 Live Copy (NPR-30613)。

### 社群 {#communities}

* 活動與通知標題不一致 (NPR-30940)。
* Analytics 報表沒有填入 AEM 製作環境中，出現空白頁面 (NPR-30905)。
* Communities 部落格中的分頁沒有正常運作 (NPR-30827)。

### Foundation {#foundation}

* 未儲存 Jetty 型 HTTP 服務的緩衝區大小設定更新 (NPR-30925)。

### Forms {#forms-1}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms 附加元件套件用於協助讓表單功能與 AEM Service Pack 和 Cumulative Fix Pack 一致。因此，必須先安裝任何 AEM Service Pack、Cumulative Fix Pack 或 Feature Pack，才能安裝 AEM Forms 附加套件。

#### 調適型表單 {#adaptive-forms}

* 使用指令碼計算的浮動值沒有正確以屬於表單集的形式顯示 (NPR-30802)。

#### HTML5 Forms {#html-forms}

* 新增子表單的例項時，產生 XDP 表單的 HTML5 預覽後出現閃爍畫面 (NPR-30908)。

### Forms - JEE 安裝程式 {#forms-jee-installer}

#### 文件服務 {#document-services}

* 套用修補程式以修正 HTML 轉 PDF 問題後，OutputService 顯示錯誤的回應 (NPR-31504)。

#### PDFG 服務 {#pdfg-service}

* 沒有針對 HTML2PDF 服務顯示 JMX 控制台的重複使用次數上限 (NPR-30305)。

#### Foundation JEE {#foundation-jee}

* 沒有針對 HTML2PDF 服務顯示 JMX 控制台的重複使用次數上限 (NPR-30136)。

### Cumulative Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.6 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

### 資產 {#assets-2}

* Dynamic Video 執行的視訊彙總只傳回結果集中的前 100 個項目。NPR-30441；CQ-4213561 的 Hotfix
* Adobe 智慧標記透過 Datapower 連線的問題。NPR-30026：CQ-4269457 的 Hotfix
* 封存檔中的資料夾檔名若具有百分比符號 (%)，解壓縮後無法使用 Assets 介面開啟。NPR-29989：CQ-4270467 的 Hotfix
* 處理大型 PDF 檔案的子資產會造成 OutOfMemoryError (OOME) 例外狀況。NPR-29851：CQ-4269574 的 Hotfix

### 網站 {#sites-2}

* AEM 和 Campaign 整合期間出現 ContextHub 錯誤。NPR-30624：CQ-4250790 的 Hotfix
* 如果 AEM 伺服器重新啟動，系統不會重新叫用資產上儲存的「onTime」或「offTime」中繼資料屬性。NPR-30412：CQ-4272784 的 Hotfix
* 產生 CSV 匯出期間，為清單檢視新增自訂欄會中斷報表。NPR-30208：CQ-4273344 的 Hotfix
* /etc/reports/ 中的 OOTB 報表無法正常運作，且歷史資料圖表沒有顯示。NPR-30016：CQ-4220180 的 Hotfix
* 系統將 resourceType 請求參數的值複製到 HTML 標記屬性 (以雙引號包圍) 的值中。NPR-29832：CQ-4255365 的 Hotfix

### 社群 {#communities-1}

* AEM Communities 審核控制台出現重複內容問題。NPR-30667：CQ-4276829 的 Hotfix

### 轉換 {#translation}

* 翻譯問題 - 使用機器翻譯時只翻譯了幾個元件。NPR-30079：CQ-4273764 的 Hotfix
* 使用翻譯架構時，對多個翻譯工作新增頁面會觸發錯誤。NPR-29746：CQ-4270953 的 Hotfix

### Forms {#forms-2}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms 附加元件套件用於協助讓表單功能與 AEM Service Pack 和 Cumulative Fix Pack 一致。因此，必須先安裝任何 AEM Service Pack、Cumulative Fix Pack 或 Feature Pack，才能安裝 AEM Forms 附加套件。

#### HTML5 Forms {#html-forms-1}

* 以瀏覽模式使用 NonVisual Desktop Access 來讀取 HTML5 Forms時，Chrome 瀏覽器在表單設計中的每個可縮放向量圖形 (SVG) 之前讀到「graphic」。NPR-30451：CQ-4274732 的 Hotfix

#### Forms - 後端整合 {#forms-backend-integration}

* 建立表單資料模型 (FDM) 時無法查看資料庫連線的服務/資料來源。NPR-30108：CQ-4273359 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-1}

#### Forms - 文件服務 {#forms-document-services}

* 對 HTML 轉 PDF 服務執行負載測試時，發生錯誤而失敗，且檔案類型設定從 AEM 表單伺服器中移除。NPR-30111、NPR-30086：CQ-4271495 的 Hotfix

### Cumulative Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.5 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.17 版。

### 資產 {#assets-3}

* 更新 DAM DMGateway 介面以提供 S3 多部分支援。NPR-29740：Q-4226303 的 Hotfix
* 無法從資產詳細資訊頁面中刪除視訊資產的影像轉譯。NPR-29417：CQ-4268675 的 Hotfix
* 擁有者無法在私人資料夾中建立私人資料夾。NPR-29397：CQ-4229830 的 Hotfix
* 上傳超過 2 GB 的 Adobe Illustrator Artwork 檔案會產生 Java 堆積空間錯誤。NPR-29265：CQ-4226217 的 Hotfix
* DAM CQ Mime Type Service 為 m3u8 套用文字後，資產變得無法使用。NPR-29259：CQ-4264052 的 Hotfix
* 嘗試在 Edge 中建立集合時，建立選項無作用。NPR-29248：CQ-4265699 和 CQ-4265438 的 Hotfix
* 資產連結分享針對資料夾中某些資產顯示空白灰色卡片。NPR-29831：CQ-4270187 的 Hotfix
* 新增至資產的新標記無法儲存，且從屬性中消失。CQ-4271931、CQ-4270476

### 網站 {#sites-3}

* 搭配多欄位使用時，CoralUI 在元件層級儲存 fileReferenceParameter 而非多欄位層級。NPR-29535：CQ-4266129 的 Hotfix
* 在 AEM 6.3.3.3 上嘗試比較最新和目前頁面版本時發生問題。NPR-29532：CQ-4269639 的 Hotfix
* 系統無視指定的搜尋路徑，在根路徑開啟路徑欄位。NPR-29398：CQ-4268897 的 Hotfix
* (體驗片段) FacebookApplication#setUpApp 使用已棄用的 API，而該 API 已失效。NPR-29213：CQ-4266630 的 Hotfix
* 已在執行個體上啟用縮製的情況下，將元件新增至 WCM 頁面時會產生錯誤警報。NPR-29476：CQ-4266197 的 Hotfix
* 轉出時沒有從 Blueprint 傳播空白屬性和多個屬性。透過 Blueprint 重設 Live Copy 對元件無效。NPR-29252：CQ-4264928、CQ-4264926、CQ-4267722 的 Hotfix
* 處於來源編輯模式時若從全螢幕最小化 RTF 編輯器，會導致內容遺失。NPR-28838：CQ-4260584 的 Hotfix

### 社群 {#communities-2}

* 無版主權限的訪客和成員可以藉由貼上 URL 看到未核准和待核准的貼文。NPR-29726：CQ-4271124 的 Hotfix
* 觀察到使用者登入 Community 時出現 40-50 秒的長回應時間。NPR-29679：CQ-4269444 的 Hotfix
* 以不同使用者名稱登入時無法重設密碼，且作為密碼的電子郵件似乎是因使用者名稱和電子郵件交換所產生。NPR-29281：CQ-4268694 的 Hotfix

### 體驗片段 {#experience-fragments}

* 使用智慧影像時，無法將體驗片段匯出至目標。CQ-4269606 的 Hotfix

### 複寫 {#replication}

* 複寫代理元件疑似為漏洞，向未獲授權的使用者洩漏了敏感資訊。NPR-29613：Granite-25070 的 Hotfix
* `cq/replication/components/agent` 元件中，使用者提供的資料沒有在輸出上逸出，導致儲存型跨網站指令碼 (XSS) 漏洞。NPR-29452：CQ-4266263 的 Hotfix

### Forms {#forms-3}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

### Forms 附加元件套件 {#forms-add-on-package-3}

* Forms 附加套件中沒有新的 AEM Forms 修正。

### Forms - JEE 安裝程式 {#forms-jee-installer-2}

* Forms JEE 安裝程式中沒有新的 AEM Forms 修正。

### 6.3.3.5 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in}

AEM 6.3.3.5 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6_5-bundle-list.txt)

AEM 6.3.3.5 中包含的內容套件清單

[取得檔案](assets/do-not-localize/content_packages6335.txt)

### Cumulative Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.4 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.16 版。
* 在 Brand Portal 複寫代理中新增通訊端逾時和連線逾時。

### 資產 {#assets-4}

* 如果以相同名稱重新上傳封存檔，系統不會為新處理的資產產生轉譯。NPR-28643：CQ-4262286 的 Hotfix
* 工作流程 CommandLineProcess 因檔名中有單引號而失敗。NPR-28805：CQ-4262287 的 Hotfix
* 集合頁面和使用了篩選器的集合頁面之間值不相同。NPR-28642：CQ-4261405 的 Hotfix
* 上傳大型 zip 封存資產會觸發 CommitFailedException。NPR-28528：CQ-4260903 的 Hotfix
* 編輯包含特殊字元的資料夾時，無法儲存資料夾中繼資料。NPR-28211：CQ-4260401 的 Hotfix
* 無法從資產詳細資訊頁面中刪除視訊資產的影像轉譯。NPR-29149：CQ-4266073 的 Hotfix
* 使用 DMComponent 的 DMS7 桌面視訊傳送採用漸進式下載方式，以在發佈模式下播放視訊且不會串流。NPR-28754：CQ-4263732 的 Hotfix
* 無法建立/編輯影像預設集，因為限制存取 /etc/dam/video/dynamicmedia 停用了影像管理員的功能。NPR-28662：CQ-4263022 的 Hotfix
* 含有以 DMS7 編碼的視訊檔案之連結分享導致空白資料夾。NPR-28851：CQ-4206743 的 Hotfix
* 從 AEM 複寫至 Brand Portal 時長時間卡住。NPR-28913：CQ-4254932 的 Hotfix

### 社群 {#communities-3}

* 無法開啟 Outlook 寄件匣和收件匣資料夾中含有附件的訊息。NPR-28559：CQ-4217072 的 Hotfix

### 網站 {#sites-4}

* 適用於 6.3 的 SuggestionHandler 中出現跨網站指令碼 (XSS)。NPR-28692：CQ-4253821 的 Hotfix
* 深度轉出結束卻沒有包含個別 LiveCopy 中的所有分支。NPR-29175：CQ-4239472 的 Hotfix
* (MSM) 使用 oak-index 實作 LiveCopyIndex。NPR-29198：CQ-4222472 的 Hotfix
* 「coral.js」檔案包含有漏洞的「handlebars.js」程式庫版本。NPR-26973：CQ-4255377 的 Hotfix
* 使用含有巢狀配置容器和文字元件的 Target 元件，會導致在編輯文字或按一下容器時擲回 JavaScript 錯誤「無法讀取 null 的 currentPos 屬性」。NPR-29077：CQ-4246594 的 Hotfix
* (觸控式 UI) 無法將大量標記更新至已經使用不同標記加以標記的頁面。NPR-28729：CQ-4262922 的 Hotfix
* 在卡片檢視中開啟變化造成了 500 錯誤。NPR-28611：CQ-4263571 的 Hotfix
* 轉出主版中已移動的結構會導致錯誤的 cq:moveTarget。NPR-28968：CQ-4265280 的 Hotfix

### 整合 {#integration}

* (雲端服務設定) 根層級顯示的「繼承自」核取方塊應移除。NPR-28771：CQ-4259676 的 Hotfix
* com.day.cq.personalization.impl.TeaserResourceEventHandler 進入無限迴圈，並造成發佈執行個體上的節點更新。NPR-28561：CQ-4263096 的 Hotfix
* 使用 Brightedge 憑證時出現連線錯誤而失敗。NPR-29167：CQ-4265872 的 Hotfix
* OfferproxyTandtProvider.java 中出現編譯問題，因為遺失「Resource」類別的匯入陳述式：missing import statement: import org.apache.sling.api.resource.Resource。NPR-28772

### 商務 {#commerce}

* 排序選項無法用於商務集合內的資產。NPR-28755：CQ-4213622 的 Hotfix

### Jetty {#jetty}

* 在 6.3.3 上安裝 CFP2 後，每 302 次重新導向 error.log 中就會出現 Jetty 例外狀況。NPR-28606：CQ-4262844 的反向移植

### UI - Foundation {#ui-foundation}

* 按一下標記會移除全域 mouseup 事件，且對話方塊會凍結在「可拖移模式」下。NPR-28641：CUI-7294 的 Hotfix

### WCM - MSM {#wcm-msm}

* PageManager 移動的 PushOnModify 轉出從兩個工作階段認可多次，造成了競爭情形。NPR-28880：CQ-4266191 的 Hotfix

### 漏洞 {#vulnerability}

* CSRF 保護架構對 AEM Foundation 表單無效。NPR-28612：GRANITE-22231 的 Hotfix

### Forms {#forms-4}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

AEM Forms 的關鍵重點為：

* 啟用原則集檢視頁面上選取每頁項目的選項。
* 對所有瀏覽器新增共用佇列功能。

### Forms 附加元件套件 {#forms-add-on-package-4}

#### Forms - 工作流程 {#forms-workflow}

* 共用的佇列回應任務會在 HTML5 工作區中開啟一個 Flash 元素。NPR-29161：CQ-4266498 的 Hotfix
* 如果按鈕包含 Umlaut 字元，就無法從工作區提交。NPR-29014：CQ-4263172 的 Hotfix

#### Forms - 文件安全性 {#forms-document-security}

* 啟用原則集檢視頁面上選取每頁項目的選項。NPR-29243：CQ-4268567 和 CQ-4265132 的 Hotfix

#### Forms - 文件服務 {#forms-document-services-1}

* OSGi Forms 組合器無法用於 Acrobat 檔案。NPR-29049：CQ-4254426 的 Hotfix

#### HTML5 Forms {#html-forms-2}

* 在 Designer 中以 PDF 預覽 XDP 和以 HTML 預覽相同 XDP 時出現不同的行為。NPR-28602：CQ-4260239 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-3}

* Forms JEE 安裝程式中沒有新的 AEM Forms 修正。

### 6.3.3.4 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-1}

AEM 6.3.3.4 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

AEM 6.3.3.4 中包含的內容套件清單

[取得檔案](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulative Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.3 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.16 版。
* 原則設定清單分頁變更為每頁限制 50 筆記錄。
* 在發佈執行個體上將 rep:cache 新增至 AEM Communities 使用者同步接聽程式的可忽略節點中。
* 為清單和卡片檢視按鈕新增 Aria 標籤。
* 執行任何搜尋時都為逗號包含一個逸出字元。
* 為內容原則的綜合資源啟用支援。

#### 資產 {#assets-5}

* 無法下載多個 .jp2、.max、.oft、.msg 類型的檔案。NPR-28002：CQ-4210856 的 Hotfix
* ImageServer 發佈設定沒有複寫至混合式傳送。NPR-28329：CQ-4253030 的 Hotfix

#### 社群 {#communities-4}

* 在 Publish 上為 AEM Communities Enablement 元件啟用鍵盤導覽。NPR-27739：CQ-4253856 的 Hotfix
* 啟用鍵盤導覽以觸發內容播放。NPR-27738：CQ-4254026 的 Hotfix
* 為清單和卡片檢視按鈕新增 Aria 標籤。NPR-27736：CQ-4254027 的 Hotfix
* (反向移植) 在發佈執行個體上將 rep:cache 新增至 AEM Communities 使用者同步接聽程式的可忽略節點中。NPR-27841：CQ-4247234 的 Hotfix
* 在 UI 層級的搜尋方塊中，特殊字元帶有逸出字元 (\) 首碼。NPR-27839：CQ-4259757 的 Hotfix
* 在快速搜尋中，搜尋 (、+、? 這類字元時出現錯誤。NPR-28212：CQ-4260969 的 Hotfix
* 無法使用 API 刪除使用者產生的內容中的評論。NPR-28075：CQ-4260534 的 Hotfix
* 有新評論發佈時，發佈在下一頁的評論以黃色醒目提示。NPR-28148：CQ-4259681 的 Hotfix
* 無法開啟 Outlook 寄件匣和收件匣資料夾中含有附件的訊息。NPR-28559：CQ-4217072 的 Hotfix

#### 網站 {#sites-5}

* 在 AEM 6.3 中執行「版本清除」會造成記錄中出現不斷重複的警告。NPR-27750；CQ-4206870 的 Hotfix
* RTF 編輯器全螢幕模式不支援樣式外掛程式。NPR-27622：CQ-4258674 的 Hotfix
* 內容框架在 editor.js 中載入後沒有清除「loaderPromises」清單 NPR-27768：CQ-4205337 的 Hotfix
* 無法在未設定上層元件的情況下於巢狀 parsys 上設定範本原則。NPR-27987：CQ-4246095 的 Hotfix
* 元件瀏覽器沒有清除使用者輸入，因此可能擲回 javascript 錯誤。NPR-27986：CQ-4247590 的 Hotfix
* 使用者嘗試編輯內容片段時頁面顯示為空白。NPR-27669
* 使用者按一下附註的當下，附註醒目提示隨即消失。BPR-27196：CQ-4254423 的 Hotfix

#### 整合 {#integration-1}

* ResourceResolver 沒有解析 Target 元件的多個網域。NPR-28265：CQ-107847 的 Hotfix
* 因為沒有顯示任何動作，LiveCopy 繼承取消無法在目標容器上正常運作。NPR-28129：CQ-4259813 的 Hotfix

#### 複寫 {#replication-1}

* DispatcherFlushRules 中斷 6.3.3.1 中的複寫 NPR-28150：CQ-4261401 的 Hotfix

#### Campaign - 目標定位 {#campaign-targeting-1}

* TargetedContentManager 中的 NullPointerException。CQ-4263485 的 Hotfix

#### 社交 - SCORM {#social-scorm}

* 移除播放器中共享內容物件參考模型 (SCORM) 雲端的參考。CQ-4260779 的 Hotfix

#### DAM - 一般 {#dam-general}

* 透過連結分享電子郵件下載傳回空白/損毀的 zip。CQ-4259686 的 Hotfix

#### MAC - Test&amp;Target 整合 {#mac-test-target-integration}

* 預設受眾以外的受眾無法使用設定 Target 元件選項。CQ-4261370 的 Hotfix

#### 轉換 {#translation-1}

* MS Translator 升級為 API v3.0 後，AEM 6.3 啟用了對 MS Translator 服務的支援。NPR-28365：CQ-4259096 的 Hotfix

### Forms {#forms-5}

### Forms 附加元件套件 {#forms-add-on-package-5}

#### Forms - 工作流程 {#forms-workflow-1}

* 無法在 HTML5 工作區上轉譯 PDF 表單。NPR-28059：CQ-4260373 的 Hotfix

#### Forms - 文件服務 {#forms-document-services-2}

* 無法在在 Admin Console 中查看原則集檢視中前 1000 個以外的任何原則集。NPR-28060、NPR-26047：CQ-4249865 的 Hotfix
* 系統擲回例外狀況並出現名稱 java.lang.IllegalArgumentException 訊息：無列舉常數 com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE 導致短期處理程序無法完成。NPR-28652

#### Forms - 調適型表單 {#forms-adaptive-forms}

* 勾選核取方塊項目時，新增/移除下拉式清單中的項目沒有更新。NPR-28224：CQ-4252834 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-4}

* Forms JEE 安裝程式中沒有新的 AEM Forms 修正。

### 6.3.3.3 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-2}

AEM 6.3.3.3 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6333_bundle_list.txt)

AEM 6.3.3.3 中包含的內容套件清單

[取得檔案](assets/do-not-localize/content_package_list_6333.txt)

### Cumulative Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.2 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 AEM 6.3 Service Pack 3 發行說明。

AEM Cumulative Fix Pack 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.15 版。
* 在「資料夾中繼資料結構」中新增對「規則索引標籤」和其在「資產資料夾」上強制執行的支援。
* 啟用分頁支援以分組發佈時列出的頁面。
* 啟用可設為任何數字的 unreadCount 通知。預設值設為 20。
* 針對外部連結檢查器的修正。

#### 資產 {#assets-6}

* 動態下拉式清單不支援階層式下拉式清單。NPR-27044；CQ-4252564 的 Hotfix
* 改善查詢，現可使用 ExpiryNotification 功能。NPR-26999：CQ-4251188 的 Hotfix
* 規則從中繼資料結構移轉至資料夾中繼資料結構。NPR-27771：CQ-4257737、CQ-4257735、CQ-4259822 的反向移植
* 資產參考調整無法更新 Sling ResourceCollections 所屬資產的參考。NPR-26759：CQ-4252605 的 Hotfix
* 透過連結分享電子郵件下載傳回空白/損毀的 zip 檔案。NPR-27997：CQ-4259686 的 Hotfix
* 混合視訊編碼不完整且沒有建立縮圖。NPR-27122：CQ-4255080 的 Hotfix

#### 網站 {#sites-6}

* 暫止的上層頁面從遺失的頁面中移除了 cq:LiveRelationship mixin 類型。NPR-26996：CQ-4254113 的 Hotfix
* (外部連結檢查器) 內部連結在個別頁面上顯示為已損毀，但對外部連結沒有相同作用。NPR-27481：CQ-4257780 的 Hotfix
* 編輯其他頁面屬性時，雲端服務設定繼承關係中斷。NPR-27311：CQ-4256785 的 Hotfix
* 搭配 Foundation 表單使用核心元件時出現 Null 指標例外狀況。NPR-27333：CQ-4249176 的 Hotfix
* RTF 編輯器移除了空白的 alt 標記。NPR-26938：CQ-4253267 的 Hotfix
* (傳統 UI) 如果有多個下拉式清單，selectionchanged 接聽程式會出現效能問題。NPR-27115：CQ-4237215 的 Hotfix
* RTF 編輯器與多個欄位結合時，出現「Uncaught TypeError: fieldAPI.getName 不是 foundation.js 的函數」錯誤。NPR-27146：CQ-4253155、CQ-4259967 的 Hotfix
* 即使按一下 Safari 瀏覽器中的選項按鈕，焦點/游標仍停留在 RTF 編輯器上。NPR-27144：CQ-4249635 的 Hotfix
* 使用者嘗試編輯內容片段時頁面顯示為空白。NPR-27669
* 無法為體驗片段建立版本。NPR-27689：CQ-4259009 的 Hotfix

#### 整合 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever 遊走整個樹狀結構以收集可用的品牌。NPR-27060：CQ-4255790 的 Hotfix
* 系統沒有針對目標元件考慮 cq:actions。NPR-27616：CQ-4257497 的 Hotfix

#### Sling {#sling}

* 搭配名稱相同的類別使用 data-sly-use 時，產生了不相容的程式碼。NPR-27282：Sling-7581 的 Hotfix

#### 商務 {#commerce-1}

* 適用於 Apache Felix Http Jetty 4.0.6 的更新。NPR-26472：Granite-22916 的 Hotfix

#### DAM - DM 用戶端 {#dam-dm-client}

* 指定動態媒體元件中的中斷點後，影像沒有顯示。CQ-4256168 的 Hotfix

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet 與相關視訊沒有正常同步。CQ-4251650 的 Hotfix
* 沒有針對混合媒體集在檢視器預設集編輯器中播放視訊。CQ-4251442 的 Hotfix

#### DAM - 一般 {#dam-general-1}

* 套用 SP3 修補程式後遺失內容片段模型的連結。CQ-4259029 的 Hotfix

#### DAM - UI {#dam-ui}

* 安裝 SP3 後資料夾中繼資料結構 UI 毀損。CQ-4257737 的 Hotfix

#### 社群 {#communities-5}

* 新增分頁支援以分組發佈時列出的頁面。NPR-26953：CQ-4246525 的 Hotfix
* 未讀通知數不能設為超過 21。NPR-27496：CQ-4252829 的 Hotfix
* 使用者訂閱限制上限為 1000。NPR-27615：CQ-4254689 的 Hotfix
* 在論壇中上傳影像以外的附件 (例如 .pdf) 時發現錯誤。NPR-27375：CQ-4257753 的 Hotfix
* 用於回覆的連結對列點擊無效。NPR-24556：CQ-4256138 的 Hotfix
* 刪除 UGC 時沒有刪除與 UGC 相連的關係。NPR-27631：CQ-4258706 的 Hotfix
* 如果社群是透過資料庫儲存資源提供者 (DSRP) 設定，就無法依照關鍵字搜尋中的位址值進行搜尋。NPR-27652：CQ-4253261 的 Hotfix
* 確認刪除後若按一下影像上的垃圾桶圖示，會將附件永久移除。NPR-27340：CQ-4255150 的 Hotfix
* 論壇貼文和回覆會新增到第二頁頂端，而重新整理後貼文就會移至第一頁頂端的正確位置。NPR-27341：CQ-4247338 的 Hotfix
* 啟用 Scorm 資源完成狀態在 UI 中顯示為空白。NPR-27152：CQ-4249994 的 Hotfix
* 啟用「允許有特殊權限者」時，有特殊權限的成員應只能為具有社群成員身分的使用者撰寫內容。NPR-27901：CQ-4251235 的 Hotfix

#### 維持 {#sustenance}

* 套件管理器活動記錄應擷取至獨立的記錄檔中。NPR-27323：Granite-14866 的 Hotfix

#### 轉換 {#translation-2}

* we.retail 範例內容無法使用翻譯預覽。NPR-27170：CQ-4241179 的 Hotfix

* 主動式 platform.login 修正。NPR-26961
* 在使用 Tomcat 的 AEM WAR 中，「儲存並關閉」頁面屬性沒有傳回正確頁面。NPR-27567：Granite-23671 的 Hotfix

* 經由 sourceEdit 功能輸入的文字儲存後會遺失。CQ-4259273 的 Hotfix

### Forms {#forms-6}

### Forms 附加元件套件 {#forms-add-on-package-6}

#### Forms - 文件安全性 {#forms-document-security-1}

* JEE 用戶端 SDK 出現並行問題。NPR-27572：CQ-4247156 的 Hotfix

#### Forms - 文件服務 {#forms-document-services-3}

* 在 WebSphere 上根據 SOAP 建立表單資料模型時失敗。NPR-27692：CQ-4253702 的 Hotfix

#### Forms - 調適型表單 {#forms-adaptive-forms-1}

* AEM 表單出現 XML 插入漏洞。NPR-27863：CQ-4257315 的 Hotfix
* 在網站頁面上設定了錯誤的表單時，AEM Forms 容器元件會隱藏，且會選取「表單涵蓋整個頁面寬度」核取方塊。NPR-25972：CQ-4239287、CQ-4249133 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* 在 WebSphere 上根據 SOAP 建立表單資料模型時失敗。NPR-27692：CQ-4253702 的 Hotfix

#### 包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included}

AEM 6.3.3.2 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/63332bundle_list.txt)

AEM 6.3.3.2 中包含的內容套件清單

[取得檔案](assets/do-not-localize/6332content_package.txt)

### Cumulative Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 為重要更新，包含自 2018 年 9 月正式發行 AEM 6.3 Service Pack 3 (6.3.3.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.3.1 依存於 AEM 6.3 Service Pack 3。因此，您必須先安裝 AEM 6.3 Service Pack 3，再安裝 AEM Cumulative Fix Pack 6.3.3.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 3 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.14 版。
* 述詞和搜尋的效能改善。
* 修正預設值的 FormData 處理問題。
* FormBuilder 升級為最新 Handlebars 版本。
* 新增設定 Servlet，用於在對話方塊模式中編輯 RTE 設定。
* 新增對複合欄位的支援。
* 透過編輯對話方塊的內容原則啟用/停用 RTF 編輯器的工具列項目。

#### 資產 {#assets-7}

* 啟用 IDS 分離後，DAM 更新資產工作流程不再連結參考。NPR-26135：CQ-4250933 的 Hotfix
* 透過解封存器步驟建立的封存檔中若包含檔名有 % 的資料夾，則解壓縮該封存檔後無法開啟。NPR-26275：CQ-4251482 的 Hotfix
* 單引號字元導致中繼資料無法更新。NPR-26808：CQ-4254305 的 Hotfix
* (Omnisearch) 在一個集合內搜尋時出現效能問題。NPR-26714：CQ-4253408 的 Hotfix
* 使用 GQLConverter 進行全文檢索搜尋時若文字中包含「OR」字母，則系統會不當處理。NPR-26564：CQ-4247362 的 Hotfix
* 來自多租用戶的共用資產連結會在租用戶 ID 前加上文字，形成無效的 URL。NPR-26482：CQ-4253540 的 Hotfix
* 停用 Dynamic Media 雲端設定 UI 中的「公司根資料夾路徑」。NPR-26361：CQ-4249505 的 Hotfix
* .mos RAW 檔案的擷取時間延長。NPR-26296：CQ-4250661 的 Hotfix
* 資產連結共用不允許新增超過一名使用數值使用者 ID 的內部使用者。NPR-26206：CQ-4251466 的 Hotfix
* 以 deflate64 演算法壓縮的 zip 檔案損毀。NPR-26793：CQ-4253995 的 Hotfix
* 複雜 PDF 檔案的縮圖產生程序無法正常運作，導致屬於影像一部分的縮圖遺失。NPR-26057：CQ-4250944 的 Hotfix
* 產生縮圖時出現堆積記憶體利用問題。NPR-25545：CQ-4246960 的 Hotfix
* 對資產建立大量關聯造成錯誤。NPR-26309：CQ-4250708 的 Hotfix
* 「刪除轉譯」選項無法運作，且擲回「無項目可刪除」錯誤。NPR-26007：CQ-4213414 的 Hotfix
* 無法刪除多值欄位的預設。NPR-25116：CQ-4247856 的 Hotfix
* (DM Hybrid) 使用 Dynamic Media 的 AEM 6.3.2 出現目錄複寫中斷情形。NPR-26406：CQ-4251306 的 Hotfix

#### 網站 {#sites-7}

* Sites 修正的主動式反向移植。NPR-26963
* 標題和名稱案例類型不同時會建立兩次標記。NPR-26877：CQ-4254134 的 Hotfix
* 編輯對話方塊中的 RTF 編輯器功能不受原則控制。NPR-27059、NPR-26750：CQ-4241130 的 Hotfix
* 用戶端內容 segment.js 快取與非快取問題。NPR-26622：CQ-4253486 的 Hotfix
* 傳統子規則的區段規則 (/etc/segmentation) 啟用造成發佈失效。NPR-26601：CQ-4253588 的 Hotfix
* 新增「特殊字元」會將 RTF 編輯器對話方塊捲動至頂端。NPR-26435：CQ-4249869 的 Hotfix
* (觸控式 UI) 從全螢幕切換至浮動式對話方塊時，多個 RTF 編輯器的工具列變得無法使用。NPR-25652：CQ-4206008 的 Hotfix
* 促進多頁面啟動會為每個頁面建立多個版本。NPR-26810：CQ-4254663 的 Hotfix
* 標記移動操作沒有反映在結構化的內容片段模型標記欄位。NPR-26801：CQ-4251805 的 Hotfix
* (觸控式 UI) 重新命名 Blueprint 中的頁面後，從頁面編輯器取消發佈子頁面的功能無法運作。NPR-26774：CQ-4254175 的 Hotfix
* 取消發佈的頁面無法搭配參考使用。NPR-26749：CQ-4254372 的 Hotfix
* 將變化建立為 Live Copy 需要使用者重新更新頁面才會反映。NPR-26663：CQ-4254328 的 Hotfix
* (傳統 UI) 返回頁面屬性，縮圖影像不再使用繼承項目，並從網站管理員和 Sidekick 中消失，而影像顯示為空白。NPR-26562：CQ-4252346 的 Hotfix
* 當頁面版本建立並觸發比較時，/content/versionshistory 中的節點會列在 Blueprint 的 Live Copy 清單中。NPR-26506：CQ-4243957 的 Hotfix
* 體驗片段管理員編輯器中的 URL 不允許覆蓋。NPR-26318：CQ-4252156 的 Hotfix

#### 平台 {#platform}

* ReplicationEventListener 中透過測試事件發生工作階段洩漏情形。NPR-25937：CQ-4251090 的 Hotfix
* 複寫使用過期的 OAuth 代號，造成多個錯誤。NPR-25894：GRANITE-22388 的 Hotfix

#### 整合 {#integration-3}

* 升級為 Handlebars 4 後，由於使用不相容的範本，造成透過 AEM 內嵌的 TSDK 中斷。NPR-26699：CQ-4248974 的 Hotfix
* 發佈含有新資產的頁面時，未經通知便停用了來自發佈執行個體的子頁面。NPR-24869：CQ-4247832 的 Hotfix
* 複寫使用過期的 OAuth 代號。NPR-25984：Granite-22388 的 Hotfix

#### 複寫 {#replication-2}

* Http 傳輸可能洩漏開放工作階段。Granite-17434 的 Hotfix
* 多個複寫代理同時存取了存取代號節點時，記錄中出現例外狀況。NPR-26964：GRANITE-23276、Granite-23155 的 Hotfix

#### ContextHub {#contexthub}

* 「coral.js」檔案包含有漏洞的「handlebars.js」程式庫版本。CQ-4255377 的 Hotfix

#### DAM - DM 用戶端 {#dam-dm-client-1}

* 刪除影像資產的副本會造成原始影像資產無法使用。CQ-4251648 的 Hotfix
* 從 S7 伺服器備援下載額外的影像內容。CQ-4248770 的 Hotfix

#### Granite {#granite}

* AEM OAuth 提供者沒有執行區分大小寫的搜尋。NPR-26133：GRANITE-22650 的 Hotfix
* 套件驗證器沒有驗證 CFP/SP 中包含的套件。NPR-26775：Granite-22825 的 Hotfix

#### 社群 {#communities-6}

* 搜尋結果出現分隔符號問題。NPR-27051：CQ-4248939 的 Hotfix
* Adobe 儲存資源提供者中下拉式清單的值從 Dallas 變更為 Virginia。NPR-26936：CQ-4254434 的 Hotfix
* 啟用 SocialTagManager 中對當地語系化標題搜尋的支援。NPR-26932：CQ-4250276 的 Hotfix
* 建立論壇貼文時附件影像沒有顯示縮圖。NPR-26380：CQ-4253105 的 Hotfix
* 從 Word 外掛程式貼上的操作無法載入超過一個影像。NPR-26728：CQ-4253638 的 Hotfix
* 無法篩選審核頁面中的內容。NPR-26697：CQ-4213766 的 Hotfix
* (安全漏洞) 由於 JWT 錯誤設定，帳戶遭接管。NPR-26440：CQ-4253314 的 Hotfix
* 從 Adobe 儲存資源提供者擷取資料的速度緩慢。NPR-26237：NPR-24152 的 Hotfix
* 私人訊息撰寫頁面執行情況不穩定且緩慢。NPR-26120：CQ-4250923 的 Hotfix
* 「全部標記為已讀」通知只將前 10 個訊息變為已讀而沒有重新整理頁面。NPR-27036：CQ-4254058 的 Hotfix
* Communities 評論區段分頁點擊和頁面載入行為。NPR-27030：CQ-4251228 的 Hotfix
* (論壇搜尋) 「返回」按鈕略過頁面並傳回 forum.html。NPR-26949：CQ-4254804 的 Hotfix
* 未讀通知數增加時不會超過 21。NPR-26947：CQ-4251251 的 Hotfix
* (SearchScheduledPosts job) 新增 ConfigMgr 中的啟用/停用切換項目。NPR-26924：CQ-4250463 的 Hotfix
* 在「指定任務」頁面上捲動時出現 Tomcat Context (/aempublish) 路徑。NPR-26919：CQ-4254345 的 Hotfix
* 建立群組和成員時出現 NullPointerException。NPR-26778：CQ-4248095 的 Hotfix
* 使用 MySQL 單一職責原則 (SRP) 時，版主無法取消釘選和取消精選內容。NPR-26767：CQ-4251520 的 Hotfix
* 使用某些字元時出現搜尋功能問題。NPR-26726：CQ-4247744 的 Hotfix
* 啟用審核 UI 和啟用資源的深層連結。NPR-26705：CQ-4251381 的 Hotfix
* 論壇元件出現搜尋問題。NPR-26577：CQ-4251303 的 Hotfix
* 在 Communities 訊息中同時搜尋名字和姓氏時沒有傳回預期的結果。NPR-26377：CQ-4253150 的 Hotfix
* 移除回覆時分頁沒有更新。NPR-26327
* 刪除貼文會生效，但控制台會出現錯誤，且貼文仍可在 UI 上看到。NPR-26292：CQ-4252803 的 Hotfix
* 分頁沒有以動態方式更新，且回覆清單持續變長。NPR-26145：CQ-4251586 的 Hotfix
* 若群組包含 5-10 萬名使用者，則該群組的設定不會載入。NPR-25642：CQ-4238426 的 Hotfix
* 目錄資源播放器的內容路徑失敗。NPR-25640：CQ-4238426 的 Hotfix
* (論壇搜尋) - 含有大量貼文的討論串之編頁連結在通知中無法運作。CQ-4254202 的 Hotfix
* 使用 Firefox 時審核控制台只顯示 5 個項目。CQ-4254128 的 Hotfix
* 建立網站時群組沒有顯示。NPR-27148：CQ-4251788 的 Hotfix
* 將群組和成員新增至「角色」設定，以及允許有特殊權限的成員使用部落格功能時，出現 Null 指標例外狀況。NPR-21732、NPR-27176：CQ-4255909 的 Hotfix
* 編輯網站和在角色設定中新增成員時，系統擲回 Null 指標例外狀況。NPR-27132：CQ-4255909 的 Hotfix

#### 使用者介面 {#user-interface}

* 主動式平台登入修正。NPR-26961
* (多欄位) 允許複合項目有自訂名稱。NPR-26493：Granite-20568 的 Hotfix
* 貼上頁面後欄檢視沒有更新，直到重新整理後才更新。NPR-26030：CQ-4236346 的 Hotfix
* 主動式 granite.ui.commons 修正。NPR-26960
* 主動式 granite.ui.content 修正。NPR-26959
* 主動式 CQ/體驗記錄修正。NPR-26943
* 主動式 Foundation UI 反向移植。NPR-26942
* (IE11) 輸入負值時數字欄位中顯示「NaN」。NPR-26701：CQ-100826 的 Hotfix
* (Coral。多欄位) 巢狀多欄位使用錯誤的範本來建立項目。NPR-25649：CUI-6743 的 Hotfix
* 更新 granite coralui2 和 coralui3 clientlibs 以從組建中移除 Handlebars。NPR-25606：Granite-22116 的 Hotfix

### Forms {#forms-7}

### Forms 附加元件套件 {#forms-add-on-package-7}

#### Forms - 文件安全性 {#forms-document-security-2}

* 非作用中金鑰的伺服器記錄中出現主要金鑰變換例外情況。NPR-26748：CQ-4253705 的 Hotfix
* 無法建立或修改文件安全性的浮水印設定。NPR-26267、NPR-26129：CQ-4250234 的 Hotfix

#### Forms - 文件服務 {#forms-document-services-4}

* PDF/A 驗證沒有以「驗證 PDF/A」顯示有效。NPR-25934：CQ-4248558 的 Hotfix

#### Forms -互動式通訊 {#forms-interactive-communication}

* 編輯、儲存可編輯的模組然後開啟/關閉 PDF 預覽時，PDF 和信函 HTML 預覽可在相同視窗中顯示和運作。NPR-26770：CQ-4253217 的 Hotfix

#### Forms - 工作流程 {#forms-workflow-2}

* 工作區間歇性中止並重複顯示起始點。NPR-26461：CQ-4253439 的 Hotfix
* 任務名稱中使用大括號時，系統在記錄中擲回 ESAPI 例外狀況。CQ-4256627 的 Hotfix
* 與起始點相關聯的非預填適用性表單/表單集開啟時，系統會擲回 Null 指標例外狀況。CQ-4256124 的 Hotfix
* 無法使用全域設定傳送電子郵件。NPR-26163：CQ-111110 的 Hotfix
* 套用 axis.jar 檔案後無法開啟工作區。NPR-26131：CQ-4251126 的 Hotfix
* 重新整理按鈕無法將最新資料從伺服器同步至適用性表單。CQ-4255670 的 Hotfix
* 從管理員 UI 設定搜尋範本，然後使用相同 UI 搜尋 AEM Forms 工作區中的任務，系統便會擲回例外狀況。CQ-4255649 的 Hotfix
* 應用程式名稱中若帶有括號，其底下的程序追蹤詳細資訊不會顯示在 HTML 工作區中。CQ-4242101 的 Hotfix
* 在 HTML 工作區的偏好設定畫面中儲存變更時，系統會擲回例外狀況。CQ-4241485 的 Hotfix
* 最新 JEE 設定的大量核准功能失效。CQ-4241486 的 Hotfix
* 最新 6.4 JEE 伺服器上的任務/起始點草稿失敗。CQ-4241484 的 Hotfix
* 設定 Date().getTime().toString 參數以初始化工作階段而非設定 Date.toString()。CQ-4241483 的 Hotfix
* 開啟 /lc/ws 時，在 HTML 參數中發現有漏洞的字元例外狀況。CQ-4241481 的 Hotfix

#### 漏洞 {#vulnerability-1}

* Forms Manager 的附註索引標籤中出現儲存型跨網站指令碼 (XSS) 漏洞。NPR-27157：CQ-4255556 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Enterprise Security API 的程式碼審查。CQ-4255638 的 Hotfix
* 無法將 esapi.properties 載入為 WAS9 中的類別載入器資源。CQ-4255631 的 Hotfix
* 進行網域設定期間若按下「新增驗證」，系統會擲回錯誤。CQ-4255634 的 Hotfix
* Forms JEE 支援 PKCS#11 相互驗證。NPR-21372
* 修正 Core 靜態程式碼分析中報告的問題。CQ-104446 的 Hotfix
* 執行 LCM 期間部署 adobe.livecycle.weblogic.ear 和 adobe.livecycle.websphere.ear 失敗。CQ-4255629、CQ-4255630
* 應用程式管理中出現無效的錯誤訊息。NPR-23289：CQ-4233163、CQ-4255636 的 Hotfix
* 進行網域設定期間若按下「新增驗證」會導致錯誤。CQ-4255634 的 Hotfix

#### Forms - JEE Connector {#forms-jee-connector}

* 修正 Connector 靜態程式碼分析中報告的問題。NPR-22260

#### PDFG 服務 {#pdfg-service-1}

* 從 LiveCycle 升級為 AEM 6.2 表單時，記錄中出現 org.jgroups.Message 錯誤。NPR-26795：CQ-4220415 的 Hotfix
* AEM Forms - 移轉樣式時出現錯誤。CQ-4251969 的 Hotfix
* 修正 PDFG 靜態程式碼分析報表中報告的問題。NPR-23251：CQ-4213930 的 Hotfix

#### 6.3.3.1 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-3}

AEM 6.3.3.1 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/63sp3cfp1bundlelist.txt)

AEM 6.3.3.1 中包含的內容套件清單

### Cumulative Fix Pack 6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2 為重要更新，包含自 2018 年 4 月正式發行 AEM 6.3 Service Pack 2 (6.3.2.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 6.3.2.2 依存於 AEM 6.3 Service Pack 2。因此，您必須先安裝 AEM 6.3 Service Pack 2，再安裝 AEM Cumulative Fix Pack 6.3.2.x 套件。如需安裝指示，請參閱 [AEM 6.3 Service Pack 2 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp2-release-notes.html)。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.11 版。
* 啟用 Brand Portal 上的子資產多頁面資產檢視器。
* 欄位類型長度變更為 255 以支援不同附件類型的所有可能 mime 類型。
* 設定了影像違反上傳準則時從伺服器傳出的錯誤訊息。
* Day CQ Mail Service 新增 STARTTLS 支援。
* 更新為 cq-wcm-content 和 com.adobe.cq.launches.it.serverside 的最新版本。
* 將 com.adobe.granite.ui.coralui3-rte 更新已發行的最新版本。
* 確認如果 expressionResolver 為 null，轉譯條件會傳回合理的結果。
* Coral.ColumnView：新增對 Shift + 按一下操作的支援。

### 資產 {#assets-8}

* 資產資料夾封閉使用者群組 (CUG) 欄位沒有傳回「所有人」群組。NPR-23163：CQ-4239377 的 Hotfix
* 搜尋智慧型集合儲存的搜尋不會傳回所有結果。NPR-23243：CQ-4240355 的 Hotfix
* (ExpiryNotificationJobImpl) 最佳化現有查詢。NPR-23330：CQ-4205249 的 Hotfix
* (中繼資料設定檔) 建立時設定的標準標記值儲存後無法使用。NPR-23370：CQ-4235458 的 Hotfix
* (觸控式 UI) 由於 JS 錯誤而無法移動多個資產。NPR-23395：CQ-4241279 的 Hotfix
* 下載大小與顯示的資訊不相符錯誤導致使用者混淆。NPR- 23418：CQ-4242774 的 Hotfix
* 針對 LSR 和 SKETCH 副檔名擷取的 mimetype 錯誤，並導致檔案下載無效。NPR-23644：CQ-4243260 的 Hotfix
* (Firefox/Chrome) 無法下載「資產共用」頁面中的資產。NPR-23963：CQ-4244391 的 Hotfix
* 預覽後搜尋面板中的資產管理員搜尋面向消失。NPR-23964：CQ-4244410 的 Hotfix
* 取消發佈搜尋表單會完全移除預設的搜尋表單。NPR-23291：CQ-4241382 的 Hotfix
* (Brand Portal) 複寫時應篩選掉目錄述詞中的搜尋。NPR-23292：CQ-4241385 的 Hotfix
* 無法使用發佈至 Brand Portal UI 的動作。NPR-23293：CQ-4241161 的 Hotfix
* 發佈/取消發佈至 Brand Portal 按鈕不應適用於內容片段。NPR-23318：CQ-4245086 的 Hotfix
* (Brand Portal) 啟用發佈資產時建立子資產的功能。NPR-23331：CQ-4242018 的 Hotfix
* Dynamic Media 請求不使用 Proxy/HTTP 常見用戶端。NPR-10727：CQ-45695、CQ-88800 的 Hotfix
* 無法在 Dynamic Media S7 (DMS7) 中為單一轉譯 MP4 視訊資產留下附註。NPR-22046：CQ-4215912 的 Hotfix
* EmbedXMP 資料一律對 Ptiff 產生程序設為「作用中」。NPR-22903：CQ-4234498 的 Hotfix
* 大量影像預設集出現動態轉譯顯示/選取問題。NPR-23151：CQ-4217511 的 Hotfix
* Dynamic Media 編碼視訊 - 修改/重新上傳啟動器出現問題。NPR-23237：CQ-4240260 的 Hotfix
* Dynamic Media S7 中 HTTP 轉寄站的 Proxy 處理修正。NPR-24001：CQ-244140 的 Hotfix

### 網站 {#sites-8}

* 查詢產生器差異導致 6.2 和 6.3 之間出現不同的 xPath 轉譯。NPR-23245：CQ-4240396 的 Hotfix
* 頁面屬性中的縮圖索引標籤在延伸對話方塊時無法運作。NPR-22844：CQ-4241474 的 Hotfix
* Parsys 中斷了模擬器裝置框架寬度，並裁切掉其中新增的任何元件。NPR-22926：CQ-4238224 的 Hotfix
* 執行多次啟動時，會在 Author 中提升該啟動，但是但是由於缺少複寫權限，因此不會在 Publish 伺服器上複寫變更。NPR-22934：CQ-4234746 的 Hotfix
* 使用者在第一個工作階段中鎖定的頁面，可以由另一個使用者在另一個工作階段中修改。NPR-23057；CQ-4199017 的 Hotfix
* 修正清單檢視中的可重新排序選項。NPR-23065：CQ-4239321 的 Hotfix
* (頁面編輯器) 重新開啟對話方塊時，影像元件上的影像會消失。NPR-23156：CQ-4239978 的 Hotfix
* 範本編輯器只顯示 20 個範本/資料夾，且捲動至頁面底部時沒有載入其他範本/資料夾。NPR-23185：CQ-4238483 的 Hotfix
* (傳統 UI) 移動或重新命名頁面時產生錯誤。NPR-23213：CQ-4240971 的 Hotfix
* 無法編輯/建立 ContextHub 區段。NPR-23218：CQ-4226948 的 Hotfix
* (RTF 編輯器) - 取代操作會變更文字的格式。NPR-23271：CQ-4239677 的 Hotfix
* 「XF 變化」的「Blueprint」索引標籤缺少「轉出」按鈕。NPR-23320：CQ-4240404 的 Hotfix
* 由於功能遭淘汰，傳統 UI 無法用於編輯 CUG。NPR-24122：4241823 的 Hotfix
* 用於防止提升不需要的內容之主動式修正。NPR-24387：4244993 的 Hotfix
* 一旦將大約 80 個片段新增至 Assets 中的資料夾，從時間表控制台觸發工作流程時就會發生錯誤。NPR-23393；CQ-4211216 的 Hotfix
* 無法將影像從內容尋找器拖放至 RTF 編輯器對話方塊中。NPR-23403：CQ-4242094 的 Hotfix
* 將元件從 AEM 6.0 移轉到 AEM 6.2 時，出現「無效的遞迴選擇器值」錯誤。NPR-23532：CQ-4241258 的 Hotfix
* (RTF 編輯器) 工具提示顯示外掛程式的變數名稱而非可讀的外掛程式名稱。NPR-23550：CQ-4243269 的 Hotfix
* 無法透過行動裝置/平板電腦版本中要求的選取下拉式清單儲存對話。NPR-23904：CQ-4243096 的 Hotfix
* 樣式系統選項在發佈 6.3.2.1 安裝的所有頁面上顯示。NPR-23972：CQ-4244394 的 Hotfix
* 由於功能遭淘汰，傳統 UI 無法用於編輯 CUG。NPR-24122：4241823 的 Hotfix
* 用於防止提升不需要的內容之主動式修正。NPR-24387：4244993 的 Hotfix
* 資產移動時沒有更新資產參考。NPR-23208：CQ-4239879 的 Hotfix

### 平台 {#platform-1}

* 如果在搜尋面向中使用標記述詞，儲存後智慧型集合不會顯示結果。NPR-23401：Granite-21278 的 Hotfix
* 修補 clientlib 中 jQuery 1.12.4 以包含安全性修正。NPR-24128：Granite-20058 的 Hotfix
* 除非重新啟動套件組合，否則國際化翻譯不會更新。NPR-23193：Sling-7190 的 Hotfix
* ReplicationEventListener 中無結尾標記的資源解析器。NPR-23240：CQ-4241350 的 Hotfix
* 「Day CQ Mail Service」支援 STARTTLS。NPR-23941：CQ-4240397 的 Hotfix
* JCR 申訴標記應根據標記標題自動填入。NPR-24173：CQ-4199411 的 Hotfix

### 整合 {#integration-4}

* (Target) 使用 API 類型作為 XML 時促銷活動沒有啟用。NPR-23199：CQ-4240936 的 Hotfix****
* 中繼資料夾結構出現設定參考複寫失敗。NPR-23485：CQ-4242751 的 Hotfix

### 漏洞 {#vulnerability-2}

* Salesforce 整合容易遭受伺服器端請求偽造 (SSRF) 攻擊。NPR-24289：CQ-424527 的 Hotfix
* 管理員 UI 專案連結中有跨網站指令碼 (XSS)。NPR-23272：CQ-4241795 的 Hotfix

### WCM - Foundation 元件 {#wcm-foundation-components}

* Foundation 表格容易受到儲存型跨網站指令碼攻擊。NPR-23214：CQ-4240760 的 Hotfix

### 轉換 {#translation-3}

* 建立語言副本時沒有刪除 Live Copy 屬性。NPR-23123：CQ-4230641 的 Hotfix

### 使用者介面 {#user-interface-1}

* 日期挑選器不支援手動設定隱藏欄位所設定的外部類型提示。變更類型提示會出現對話錯誤。NPR-23371：Granite-21194 的 Hotfix
* Coral.ColumnView：新增對 Shift + 按一下操作的支援。NPR-23404：Granite-13338 的 Hotfix
* 選取了含有空值的項目時，選取 RT 不會進行驗證。NPR-23405：Granite-21283 的 Hotfix
* (OMEGA) 只以英文報告「功能」。NPR-23990：Granite-21231 的 Hotfix
* Coral.Autocomplete API 的修正。NPR- 23516

### Granite {#granite-1}

* Apache HTTP 用戶端追蹤連線和高堆積利用率導致 AEM 伺服器當機。NPR-23906：Granite-21056 的 Hotfix

### 商務 {#commerce-2}

* 促銷活動 json 輸出不包含 servlet 內容根。NPR-23733：CQ-4243827 的 Hotfix

### 社群 {#communities-7}

* 對社群進行搜尋因幾個字而失敗。NPR-23256：CQ-4240717 的 Hotfix
* 無法為群組管理員角色指派群組的問題。NPR-23317：CQ-4241233、CQ-4221399 的 Hotfix
* 以類似的資產名稱建立資源時出現問題。NPR-23319：CQ-4240700 的 Hotfix
* (ContextPath) 中斷訊息功能因 Jetty 設定而中斷，且在社群群組成員清單中搜尋群組成員時出現錯誤。NPR-23336：CQ-4241519、CQ-4242080 的 Hotfix
* 上傳至 Communities 論壇的影像沒有顯示在 Adobe 儲存資源提供者 (ASRP) 中。NPR-23397：CQ-4242497 的 Hotfix
* 已刪除的創意在「活動」中顯示為作用中連結。NPR-23406
* 無法透過以內容根執行的 AEM 載入 imsmanifest.xml。NPR-23483：CQ-4242193 的 Hotfix
* 舊版 Handlebars 中有安全漏洞。NPR-23518：CQ-4243055 的 Hotfix
* 通道服務無法運作。NPR-23543：CQ-4242217 的 Hotfix
* 透過 Dispatcher 存取且對其啟用 Sling Dynamic Include 時，Communities 元件出現問題。NPR-23586：CQ-4242360、CQ-4241522 的 Hotfix
* 當搜尋會透過搜尋產生許多結果的搜尋詞彙，然後再輸入新搜尋詞彙時，系統沒有重設分頁。NPR-23739：CQ-4222593 的 Hotfix
* 對論壇元件執行搜尋時發生問題。NPR-23838：CQ-4243770 的 Hotfix
* (Communities 審核標幟) 大量允許已標幟訊息的功能無法運作。NPR-23845：CQ-4243962 的 Hotfix
* 儘管選取了預設排列順序，排序按鈕文字仍沒有顯示預設的選取值。NPR-23881：CQ-4243375 的 Hotfix
* 由於向群組傳送訊息失敗，系統沒有觸發 Web 和郵件通知。NPR-23934：CQ-4242880 的 Hotfix
* 使用 DSRP 設定時標幟使用者和理由沒有詳細資訊。NPR-23973：CQ-4243205 的 Hotfix
* 已取消標幟的使用者之標幟理由仍然顯示/ NPR-23974：CQ-4243822 的 Hotfix
* 將相同名稱的兩個檔案附加至一個表單貼文兩次，會導致伺服器錯誤。NPR-24166：CQ-4244367 的 Hotfix
* 使用資料庫儲存資源開發工具 (DSRP) 時無法儲存 mime 類型超過 15 個字元的附件。NPR-24174
* 將違反上傳準則的影像拖放至貼文的文字中時，系統會擲回伺服器錯誤，且會向使用者顯示一般錯誤訊息。NPR-24243
* 多個 AEM Communities 伺服器端問題的修正。NPR-23971：CQ-4243144、CQ-4242145、CQ-4243365、CQ-4244098 的 Hotfix
* 多個 Adobe Social 問題的修正。NPR-24242：CQ-4245054、CQ-4245120、CQ-4245296 的 Hotfix

### 行銷活動 {#campaign}

* 促銷活動 json 輸出不包含 servlet 內容根。NPR-23733：CQ-4243827 的 Hotfix

### MSM {#msm}

* 轉出頁面時，Live Copy 沒有顯示繼承自主版的開啟/關閉時間屬性。NPR-23873：CQ-4243431 的 Hotfix
* LiveCopy 作業沒有忽略已刪除元件的子節點。NPR-23058：CQ-4211662 的 Hotfix

### 卸載 {#offloading}

* 請求進行處理後或定期從背景工作執行個體清除資產的機制。NPR-23638：Granite-21337 的 Hotfix

## Forms {#forms-8}

### Forms 附加元件套件 {#forms-add-on-package-8}

#### 調適型表單 {#adaptive-forms-1}

* 將 ReCaptchaConfigService 移至內部套件。CQ-4217459 的 Hotfix
* 數值欄位無視最小值。NPR-23967：CQ-4244830 的 Hotfix
* 透過 AdobeSign 支援適用性表單整合中的多重分區。NPR-23383

#### 後端整合 {#backend-integration}

* (FDM) (WebService) 支援 WSDL 解析程式中的 WSDL 延伸模組結構。 NPR-23640、NPR:23236: 4205821 的 Hotfix
* 在 Forms 附加用戶端 SDK 中包含 SDLInvokerParams。NPR-23157

### Forms JEE 安裝程式 {#forms-jee-installer-7}

#### 處理程序管理 {#process-management}

* 套用新 axis.jar 檔案後無法開啟工作區。NPR-23316
* LiveCycle 容易在 PMAdmin 上遭受 XSS 攻擊。NPR-23267
* 升級至 AEM 6.1 Forms 後，存取特定使用者的任務清單時 HTML 工作區會凍結。NPR-23943

#### 核心 {#core}

* Forms JEE 支援 PKCS#11 相互驗證。NPR-21372

#### PDFG 服務 {#pdfg-service-2}

* 同時處理 TIFF 檔案 (大小約 50 KB) 時紙張擷取服務當機。NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server Output Service - 遺漏附註的替代說明。NPR-22207
* 為透過 Designer 和 Output Service 產生的 XML 表單新增 PDF/UA 支援。NPR-23132

### 6.3.2.2 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-4}

AEM 6.3.2.2 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6_3_2_2_bundle-list.txt)

AEM 6.3.2.2 中包含的內容套件清單

[取得檔案](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulative Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 為重要更新，包含自 2018 年 4 月正式發行 AEM 6.3 Service Pack 2 (6.3.2.0) 以來累積的多項內部及客戶修正。

**AEM Cumulative Fix Pack** 的關鍵重點為：

* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.10 版。
* 改善傳統 UI 中轉譯 Parsys 元件的功能。
* 更新 Sling 模型套件組合以加入字元集修正。
* 針對所有資產類型非同步處理發佈至 Brand Portal。
* 將 coralui-component-richtexteditor.git 從 0.1.15 更新至 0.1.16
* 下拉式元件會顯示/隱藏功能的修正。
* 為核心影像元件啟用影像翻轉功能。
* 更新 felix http 套件組合以啟用工作階段屬性。

* 移除 Sling 模型上因為記憶體損毀問題造成的 cache=true。

### 資產 {#assets-9}

* 變更「資產資料夾」設定中的標題或縮圖圖片時，原始群組和資料夾的權限遭覆寫。NPR-22171：CQ-4216080 的 Hotfix
* UI 擲回假錯誤「發佈至 Brand Portal 失敗」，其實工作已新增至複寫佇列且資產已發佈至 Brand Portal。NPR-22179：CQ-4205273 的 Hotfix
* (觸控式 UI) 欄檢視中資產的預設上傳位置。NPR-22465：CQ-4237057 的 Hotfix
* 嘗試將資產結構從 /conf/global 複製到 /conf/mytenant 時，AEM 擲回 StackOverflow 錯誤。NPR-22489：CQ-4235875 的 Hotfix
* 由於資料夾名稱結尾帶有空格，因此嘗試解壓縮 ZIP 封存檔失敗。NPR-22522：CQ-4238036 的 Hotfix
* 使用資產標題欄進行排序無法用於搜尋結果。NPR-22908：CQ-4239076 的 Hotfix
* Youtube 影片以完整路徑標記，而非標記名稱本身。NPR-22976：CQ-4238669 的 Hotfix
* 在可重新排列的資料夾底下重新排列資料夾無法持續。NPR-23125：CQ-4231761 的 Hotfix
* 嘗試使用共用連結來共用集合時，出現「HTTP 504：閘道逾時」錯誤。NPR-21928：CQ-4234507 的 Hotfix
* 當一個 PDF 資產有多個相關的關鍵字時，系統無法妥善擷取和正確修改 PDF 關鍵字中繼資料。為了解決問題，已移除 PDF 資產的「主旨」欄位中繼資料屬性。但是您可編輯中繼資料結構來為「主旨」欄位新增一個多值文字欄位。NPR-21972：4215741 的 Hotfix****
* 如果 2 個快顯視窗顯示之間變更了選取的資料夾，系統會刪除錯誤的資產。NPR-21980：CQ-4233675 的 Hotfix
* (DAM) 新增至集合精靈時出現多個跨網站指令碼 (XSS) 漏洞。NPR-22432：CQ-4327086 的 Hotfix
* 透過 Safari 在 Assets 中使用 Digital Rights Management 時，資產下載失敗。使用者無法下載含有免責聲明和檔名很長的資產。NPR-22747：CQ-4236460 和 CQ-4235274 的 Hotfix
* 將公開共用設為將資產發佈至 Brand Portal 時的預設選項。NPR-21931：CQ-4218816 的 Hotfix

### 網站 {#sites-9}

* 工作流程收件匣中的新項目顯示頁面路徑而非頁面標題。NPR-21634：CQ-4230672 的 Hotfix
* 可編輯的結構元件遺失編輯時回應式格線所需的 CSS 類別名稱。NPR-21741：CQ-4232374 的 Hotfix
* (觸控式 UI) HTL 元件有多個跨網站指令碼 (XSS) 漏洞。NPR-21899：CQ-4232511 的 Hotfix
* 無法變更內容片段混合媒體影像資源類型。NPR-21907：CQ-4233401 的 Hotfix
* 觸控式 UI 對話方塊的 RTE 全螢幕隱藏了 RTE 外掛程式。NPR-22034：CQ-4235457 的 Hotfix
* (觸控式 UI) RTF 編輯器從 &lt;a> 標記中移除了 ID 以外的所有屬性。NPR-22044：CQ-4234133 的 Hotfix
* 因為執行時間長的查詢 (超過 6 個) 出現多個堆疊，導致 AEM 變得緩慢。NPR-22134：CQ-4233904 的 Hotfix
* 無法為名稱中有冒號的節點變更權限。NPR-22136：CQ-4236221 的 Hotfix
* (傳統 UI) RTF 編輯器輸出 html 將「list-position-style: inside;」作為內嵌樣式新增 &lt;ul> 標記中。NPR-22145：CRTE-114 的 Hotfix
* 文字空白時讓 TreeNode 後援以便為屬性命名。NPR-22146：CQ-4234724/CQ-4236300 的 Hotfix
* RSS 摘要問題，AEM 6.3 的連接埠 -1。NPR-22176：CQ-4233339 的 Hotfix
* (傳統 UI) 貼上文字的快速鍵 (Ctrl+V) 無法用於 OOTB 文字 (RTF) 元件。NPR-22224：CQ-4236224 的 Hotfix
* 輸入文字時 Tagfield 的篩選功能未如預期運作。NPR-22236：CQ-4236655 的 Hotfix
* (頁面編輯器) 在影像地圖元件中貼上文字資料時，文字元件也會貼上。NPR-22264：CQ-4236230 的 Hotfix
* 必填的對話方塊 FileUpload 欄位造成提交對話方塊時出現問題。NPR-22464：CQ-4222192 的 Hotfix
* 如果移動的頁面或其反向連結無法啟用，移動 w/o 複寫權限會起始啟用工作流程請求。NPR-22467：CQ-4211765 的 Hotfix
* 載入具有大量 (2000+) 受眾的頁面時出現效能問題。NPR-22478；CQ-4209567 的 Hotfix
* 初始化期間 ContextHub 儲存覆寫預設持久層時，出現持續性問題。NPR-22479：CQ-4218399 的 Hotfix
* 如果沒有在第一個內容根勾選「包含子頁面」，含有多個頁面的啟動就不會將子頁面發佈至發佈伺服器。NPR-22482：CQ-4237818 的 Hotfix
* (觸控式 UI) 透過傳統 UI 控制台刪除啟動會導致所有頁面都無法編輯。NPR-22491：CQ-4225074 的 Hotfix
* 對話方塊中的額外空格導致影像元件出現問題。NPR-22528：CQ-4238183 的 Hotfix
* 使用 inlide 模式開啟元件時，先前載入的外掛程式第二次會無法顯示。NPR-22591：CQ-4236850 的 Hotfix
* 刪除巢狀啟動中的啟動會造成子啟動變為孤立狀態。NPR-22621；CQ-4202639 的 Hotfix
* (傳統 UI Sidekick) 頁面處於工作流程鎖定階段時，工作流程索引標籤會停用。NPR-22722：CQ-4237557 的 Hotfix
* 將新增至頁面上影像元件中的影像翻轉後，變更沒有儲存且在頁面上儲存原始影像。透過 [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141) 為影像核心元件新增轉譯支援。NPR-22801：CQ-4221539 的 Hotfix
* 使用者嘗試將現有的錨點從錨點功能表中刪除時，RTF 編輯器元件視窗會關閉，且變更保持未儲存狀態。NPR-22802：CQ-4238167 的 Hotfix
* Omnisearch 篩選器沒有顯示 Sites 控制台中的所有動作。NPR-22804：CQ-4239007 的 Hotfix
* 觸控式 UI 中 OS 剪貼簿和內部 AEM 剪貼簿出現複製/貼上問題。NPR-22807：CQ-4220383 的 Hotfix
* Lucene 搜尋傳回的摘要醒目提示不一致。NPR-22879：CQ-4238513 的 Hotfix
* 在發佈執行個體關閉的情況下啟用頁面會導致進入綠色狀態而非變為琥珀色。NPR-22927：CQ-4236310 的 Hotfix
* (StyleSystem) 從快顯視窗選擇樣式時螢幕位置跳躍。NPR-23183：CQ-4238867 的 Hotfix
* (管理發佈) 需點按多次才能移至下個月的月曆。NPR-23508：CQ-4242732 的 Hotfix

### 平台 {#platform-2}

* Sling Exporter servlet 無法正確匯出日文字元。NPR-22153：CQ-4228920 的 Hotfix
* 啟動期間排程器鎖死。NPR-22440：Sling-7004 的 Hotfix
* 無法同步兩個發佈執行個體之間的群組。NPR-21943：Granite-19564 的 Hotfix
* org.apache.sling.i18n 共用工作階段/資源解析器出現效能問題。NPR-23390：Sling-7543 的 Hotfix

### 整合 {#integration-5}

* com.day.cq.analytics.sitecatalyst 中無結尾標記的資源解析器。NPR-22323：CQ-4236515 的 Hotfix
* 長時間執行查詢期間 TargetContentImpl 導致 AEM 變得緩慢。NPR-22361：CQ-4236907 的 Hotfix
* 目標引擎 (mbox.js、at.js) 沒有使用損害 URL 而使用包含冒號的 URL，這可能因為某些部署而失敗。NPR-22366：CQ-4237854 的 Hotfix
* 提供自訂 at.js 或 mbox.js 時，系統將 include 指令碼作為文字寫入頁面，而非作為 HTML 標記。NPR-22441：CQ-4203691 的 Hotfix
* 在「目標」模式中，作者不需要取消繼承即可修改從 Blueprint 繼承的元件。NPR-22751：CQ-4237907 的 Hotfix
* 由於遺失 jcr:content 節點，PersonalizationDataSource 擲回 Null 指標例外狀況。NPR-22850：CQ-4222122 的 Hotfix
* 使用英文以外的語言時，AEM 目標定位會失敗。NPR-22917：CQ-4218213 的 Hotfix
* 含有目標內容的發佈頁面遺失相關資源。NPR-23064：CQ-4227119 的 Hotfix
* 使用者無法查看 mbox 呼叫中的測試「靜態參數」值，而透過雲端設定中作為用戶端程式庫的 AT.js 進行測試時可看到這些值。NPR-21930：CQ-4234520 的 Hotfix

### WCM-Foundation 元件 {#wcm-foundation-components-1}

* 取消勾選取消/停用繼承核取方塊後，iParsys 會建立位置移位。NPR-21905：CQ-4230951 的 Hotfix
* 表單下拉式元件的顯示/隱藏功能未如預期運作。NPR-22327：CQ-4222853 的 Hotfix
* 為提高安全性，已棄用 CAPTCHA 元件，若您正使用 CAPTCHA 元件，則安裝 6.3.2.1 或更新版本後，會顯示「Captcha 元件已棄用且不應再使用。」訊息。為提高安全性，AEM 元件可供自訂以包含 reCAPTCHA NPR-22151：CQ-4220052 的 Hotfix

### WCM - 頁面編輯器 {#wcm-page-editor}

* 使用無效的選擇器時出現反射型跨網站指令碼 (XSS)。CQ-4270397 的 Hotfix

### 轉換 {#translation-4}

* 發現預覽功能出現問題。NPR-22114：CQ-4223753 的 Hotfix

### 使用者介面 {#user-interface-2}

* 設定了日期範圍的「下限」和「上限」時，Coral Calendar 月份選取器出現問題。NPR-22716：CUI-7187 的 Hotfix
* (傳統 UI) 如果相關的表單資料模型服務設為空白欄位，元件會顯示預設值。NPR-22272：GRANITE-19744 的 Hotfix

### Granite {#granite-2}

* 因記憶體洩漏造成資產共用 AEM 發佈器執行個體出現穩定性問題。NPR-22205、NPR-23178：Sling-5668、Sling-7292 和 Sling-7470 的 Hotfix。
* 不穩定的服務 ID 不應用於工作階段屬性名稱。NPR-22821：Granite-21059 的 Hotfix
* 當 HTTP Whiteboard 受管工作階段失效時，如果工作階段沒有其他工作階段屬性，則容器工作階段也會失效。NPR-23059：FELIX-5819 的 Hotfix
* 啟動時 LogbackManager 遺漏了部分 OSGi 設定。NPR-23060：Granite-19791 的 Hotfix

### 商務 {#commerce-3}

* 起用在體驗片段功能表中建立工作流程的功能。NPR-22347：CQ-4221661 的 Hotfix
* 體驗片段錯誤可在 WeRetail 上重現。NPR-21958：CQ-4220061 的 Hotfix
* 啟用包含已刪除體驗片段的頁面會擲回 NullPointerException。NPR-23179：CQ-4239939 的 Hotfix

### 專案 {#projects}

* (多語專案) 專案沒有列出超過 19 種語言的翻譯工作。NPR-22498：CQ-4229978 的 Hotfix

### 工作流程 {#workflow}

* (傳統 UI) 啟用或停用工作流程啟動器會導致行為異常。NPR-22907：CQ-4239153 的 Hotfix

## Forms {#forms-9}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

AEM Forms 的關鍵重點為：

* 新增對 HTML5 輸入類型的支援。
* 修正基本 SOAP 標頭驗證。
* 新增對超連結標題屬性的支援。
* 啟用 Forms Designer 協助工具樹狀結構中的 PDF/UA 識別碼。
* 啟用 Workbench 使用者的憑證驗證功能。
* 新增對產生 PDF/A-2a 或 PDF/A-3a 相容 PDF 檔案的支援。

### Forms 附加元件套件 {#forms-add-on-package-9}

#### Forms - 管理員 UI {#forms-admin-ui}

* 檢查 ECM 連接器設定頁面的密碼欄位時會以純文字顯示密碼。NPR-22508：CQ-4236065 的 Hotfix

#### Forms 服務 {#forms-service}

* SSL 啟用時，無法搭配 Form Analytics 使用提交和放棄事件。NPR-22637；CQ-4237973 的 Hotfix

#### 使用者管理 {#user-management}

* 由於 cglib-nodep 版本錯誤而無法同步 LDAP。NPR-22493：CQ-4234099 的 Hotfix

#### 調適型表單 {#adaptive-forms-2}

* 規則編輯器的自訂函數在函數後面新增了一個額外的「;」，因此即使自訂函數傳回 true，仍無法驗證。NPR-22481：CQ-4235499 的 Hotfix
* 顯示驗證訊息下限和上限時，無論選取的日期模式為何，日期選取器元件都不會依循該模式。NPR-22444：CQ-4236269 的 Hotfix
* 提交請求中傳送的日期格式應與日期選取器元件中提供的模式一致。NPR-22384
* Android 6.0 Samsung 裝置不遵循為適用性表單文字方塊指定的字元數上限。NPR-22363、NPR-22364：CQ-4235205 的 Hotfix
* (Microsoft Edge) (IE11) 適用性表單文字欄位元件讓多行欄位的預設值顯示為「Null」而非空白。NPR-22284：CQ-69107 的 Hotfix
* 適用性表單中的 SOAP UTF-8 輸入編碼傳回錯誤並出現亂碼頁面。NPR-20105：CQ-4222669 的 Hotfix
* 一旦在網站頁面中設定了錯誤的表單，AEM Forms 容器元件就無法用於編輯。CQ-4237456 的 Hotfix
* 在 JEE 伺服器上執行開發測試時失敗。CQ-4222082 的 Hotfix
* 由於 Calvin 框架中的縮製問題，JEE 伺服器上的 AF 測試失敗。CQ-4217220 的 Hotfix

#### Forms Manager {#forms-manager}

* (Firefox) 因為文件記錄 (DOR) 中的選項不是屬性頁面中的預先選取項目，因此無法更新適用性表單的 XML 結構屬性。NPR-22298：CQ-4237402 的 Hotfix
* 發佈網站時，發佈頁面之後修改的表單不會再發佈一次。NPR-23013：CQ-4236566 的 Hotfix

#### 後端整合 {#backend-integration-1}

* SOAP 服務的 OOTB 基本驗證無法用於 FDM 整合中的基本驗證。NPR-23238：CQ-4241308 的 Hotfix

#### 通信管理 {#correspondence-management}

* 在信函中使用 OOTB XDP 並預覽時，會顯示內容與頁尾重疊。CQ-4212414 的 Hotfix

#### 組合器服務 {#assembler-service}

* 有關 PDF/A-1b 合規性檢查錯誤的 Acrobat DC 和 AEM 報表之間出現不一致。NPR-22051、NPR-22050：CQ-4226128、CQ-4227671 的 Hotfix

### Forms - JEE 安裝程式 {#forms-jee-installer-8}

#### Workbench {#workbench}

* 啟用 Workbench 使用者的憑證驗證功能。NPR-20644：CQ-4214486 的 Hotfix
* 使用 Workbench 下載伺服器記錄只能用於一部伺服器，不能用於另一部伺服器。NPR-21079：CQ-4229842 的 Hotfix

#### 處理程序管理 {#process-management-1}

* (HTML 工作區) 因捲軸而出現螢幕大小問題。NPR-23288
* (HTML 工作區) 程序起始點沒有依照字母順序排列。NPR-22841 CQ-4238944 的 Hotfix
* (HTML 工作區) 在工作區關閉表單時會觸發準備資料。NPR-21127：CQ-4224574 的 Hotfix
* (HTML 工作區) 叫用需要含有長說明的附註之程序時，附註展開按鈕無法運作。CQ-4241488 的 Hotfix

#### 核心 {#core-1}

* 啟動排程器期間在啟始時發生錯誤。NPR-22990
* 阻止瀏覽器儲存輸入 HTML 表單中的憑證。NPR-21762：CQ-4206543 的 Hotfix
* 應修正 Core 靜態程式碼分析中報告的問題。CQ-104446 的 Hotfix

#### PDFG 服務 {#pdfg-service-3}

* PDF 產生器無法產生含有指定書籤層級的 PDF 文件。NPR-22921、NPR-22285：CQ-4230562 的 Hotfix
* 新增對產生 PDF/A-2a 或 PDF/A-3a 相容 PDF 檔案的支援。NPR-23021：CQ-4214172 的 Hotfix

#### Forms Designer {#forms-designer-1}

* 從 Designer 另存為 PDF 時遺失 PDF/UA 識別碼。NPR-23137
* 從 Designer 另存為 PDF 時沒有標記路徑物件 (例如邊框、底線、和超連結)。NPR-23136
* 從 Designer 另存為 PDF 時影像物件沒有邊界方框。NPR-23134
* 從 Designer 另存為 PDF 時，在 Designer 中定義的內嵌超連結沒有受到標記，且沒有替代文字。NPR-23133
* 透過 AEM 6.3 Forms Designer 開啟 XML Data Package 時，會移除 XML 來源中的 XHTML 格式設定。NPR-21178：LC-3917046 的 Hotfix

#### 安裝 LCM {#install-lcm}

* 在安裝程式和 LCM 中將 Jsafe Jar 更新至 Cryptoj 6.1.3.1。NPR-21370

#### 簽名服務 {#signatures-service}

* 嘗試透過 HSM 以數位方式簽署/認證 PDF 文件時，發生例外狀況。NPR-21154：CQ-4226978 的 Hotfix

### 6.3.2.1 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-5}

AEM 6.3.2.1 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/bundle-list_002_.txt)

AEM 6.3.2.1 中包含的內容套件清單

[取得檔案](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2 為重要更新，包含自 2017 年 10 月正式發行 AEM 6.3 Service Pack 1 (6.3.1.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 的關鍵重點為：

* 修改 UI 以支援在 AEM Assets 中實作 CUG 功能。
* 修正授權檢查頁面的 UI 問題以改善體驗。
* 啟用 AEM Forms App 中的 OSGi 工作流程任務支援。

### 資產 {#assets-10}

* 修改 UI 以支援在 AEM Assets 中實作 CUG 功能。NPR-19485
* 使用觸控式 UI 上傳資產以作為其本身的直接子節點會導致一個問題。資產會上傳為前一個所選資產的直接子節點。NPR-19736
* 載入已儲存的搜尋/智慧型集合時，日期範圍述詞和範圍述詞無法運作。NPR-19844：CQ-4220808 的 Hotfix
* 將多個資產 (超過 4 個) 發佈至 Brand Portal 時，AEM 執行個體會變得緩慢。NPR-20009：CQ-4213426 的 Hotfix
* 無法從授權檢查頁面下載含有空格的資產。NPR-20067：CQ-4216557 的 Hotfix
* 上傳含有多個 Alpha 層的 PSB 檔案時發生處理問題。NPR-20250：CQ-4220869 的 Hotfix
* 使用者無法下載檔案名稱長和含有已定義免責聲明的資產。NPR-20254
* ProductAssetsUploader 將臨時 JAVA 快取檔案留在 Java TEMP 資料夾中。NPR-20256：CQ-4221801 的 Hotfix
* 由於授權問題，以 Adobe 專屬代碼取代了版本比較代碼。NPR-20272：CQ-4223758 的 Hotfix
* 字串屬性 documentNumber 的中繼資料顯示為日期，但實為數字。NPR-20291：CQ-4223991 的 Hotfix
* 損毀 PDF 的文字擷取程序卡住。NPR-20416：CTG-4150375 的 Hotfix
* 壓縮檔案中若包含名稱與 UTF-8 不相容的資產，則無法正確下載。NPR-20420：CQ-4219961 的 Hotfix
* OmniSearch 中有過多字元會造成 AEM 伺服器當機。NPR-20434：CQ-4223602 的 Hotfix
* DAM 資產 API 中繼資料缺陷破壞了 xmp -write-back API。NPR-20607：CQ-4220455 的 Hotfix
* 將使用者新增至集合時出現效能問題。NPR-20699：CQ-4225733 的 Hotfix
* Dynamic Media 集不應允許從 AEM 發佈至 Brand Portal。NPR-20320：CQ-4221147 的 Hotfix
* 含有空格和重音符號的視訊不會為轉譯頁面產生任何視訊。NPR-19961：CQ-4221014 的 Hotfix
* 解決 Assets API 的多個資料夾處理問題。NPR-20569
* 雲端服務設定中的目的地路徑指向根路徑中的子資料夾時，AEM Dynamic Media Classic (前身為 Scene7) 無法從 AEM 伺服器同步資產。CQ-4228265
* Apache Commons 的電子郵件套件組合 `{org.apache.commons/commons-email/1.5}` 已新增，取代 `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`。

### 網站 {#sites-10}

* 管理員權限問題：無法從頁面屬性中移除「已關閉的使用者群組」成員。NPR-20631
* 透過「管理發佈」發佈頁面時，輸入的工作流程名稱應該可在「通知」方塊中使用。NPR-20046：CQ-4221586 的 Hotfix
* 在 RTF 編輯器中對兩列套用已設定樣式的文字，然後將其合併到一個段落中，會移除已設定樣式的範圍。NPR-20110：CQ-4223051 的 Hotfix
* 在「屬性」編輯對話方塊中，對多個索引標籤中的欄位屬性所做的變更沒有儲存。NPR-20286
* 在內容片段中貼上的內容結尾出現未預期的標記。NPR-20413：CQ-4224014 的 Hotfix
* 在 Adobe Campaign 中實作一套機制，用於從外部目標定位資源擷取內容資源的原則。NPR-20667
* RTF 外掛程式無法用於多欄位觸控式 UI 中的內嵌和全螢幕列。NPR-20973

### 行銷活動 {#campaign-1}

* 包含多個 parsys 元件的頁面中沒有顯示預留位置。NPR-20436；CQ-4215000 的 Hotfix

### 商務 {#commerce-4}

* 體驗片段在 Internet Explorer 11 中無法正常顯示。NPR-20161：CQ-4223319 的 Hotfix
* 在商務工作流程中，根據具有多個影像的主要產品建立變體時，會自動插入空白影像。NPR-20068：CQ-4222048 的 Hotfix
* 在產品控制台的集合頁面上依標記篩選的功能無法運作。NPR-20292：CQ-4224023 的 Hotfix

### 社群 {#communities-8}

* searchresult 元件的搜尋結果不一致。NPR-20070：CQ-4220913 的 Hotfix
* 已發佈元件上與版主相關的任何活動都沒有觸發電子郵件通知。NPR-20122
* 為匿名社群使用者顯示了不含結果的空白分頁。NPR-20136：CQ-4220738 的 Hotfix
* 設定偵測到 UGC 為垃圾訊息時，或是當使用者在經過預先審核的網站上發佈內容時的警報觸發器。NPR-20274：CQ-96850 的 Hotfix
* 解決 AEM Communities 網站頁面中的多個問題，包含錯誤的重新導向和頁面重新整理問題。NPR-20344
* CommunityUserOperationExtension 發生類別轉換例外狀況。NPR-20532：CQ-4224385 的 Hotfix
* 建立 Communities 網站後，使用者無法從網站地圖開啟該網站，因為內容路徑沒有加到 URL 前面。NPR-20730

### 整合 {#integration-6}

* 將 Analytics 現有的憑證移轉到 WSSE Authentication。NPR-19962：CQ-4218071 的 Hotfix
* 進行任何修改後重新啟用區段會失敗並擲回錯誤。NPR-20054：CQ-4218401 的 Hotfix
* Search&amp;Promote 雲端服務設定忽略了表單擷取方法，導致無法在製作執行個體上使用。NPR-20447：CQ-4206076 的 Hotfix
* 安裝 Search&amp;Promote 功能時，內容套件中的模糊篩選條件定義造成路徑遭覆寫。NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* 系統每次顯示 TXT 類型資產的中繼資料屬性時，都顯示在不同的中繼資料編輯器中。NPR-20239

### 平台 {#platform-3}

* 解決無結尾標記的資源解析器例外狀況。NPR-19749：Granite - 19143 的 Hotfix
* 請求在操作控制面板中隨著預設健康狀態檢查顯示自訂卡片。NPR-20145
* 頁面編輯器的附註層在 Internet Explorer 11 中無法正常運作。NPR-20222：CQ-4222818 的 Hotfix
* 在複寫代理中將使用者代理設為管理員時發生工作階段洩漏。NPR-20578
* 沒有為其他 data-sly-resource 陳述句取消設定 requestAttributes。NPR-20639：4226206 的 Hotfix
* 修正 AEM 中針對 OOTB 資產的 curl Head 請求問題。NPR-20781：CQ-4221520 的 Hotfix

### 專案 {#projects-1}

* 從專案控制台存取不同專案時需花較長時間載入。NPR-20314
* 安裝 AEM 6.3.0.1 會移除 dam-update-service 使用者的金鑰存放區。NPR-20018
* 在某些自訂部署中，使用者若嘗試在 addTask 模組中選取受託人，會花較長的時間填入使用者選取器中的清單。NPR-20283：CQ-4224193 的 Hotfix

### 使用者介面 {#user-interface-3}

* 無論對話方塊中的屬性為何，Colorfield 均設為「永遠必要」。NPR-19702
* Internet Explorer 11 中沒有以全螢幕為多欄位元件顯示卷軸。NPR-20261：CQ-4219782 的 Hotfix
* 觸發連續查詢時沒有中止先前的查詢，導致了錯誤的結果。NPR-20398：GRANITE-19306 的 Hotfix

### 工作流程 {#workflow-1}

* 系統沒有通知使用者其收件匣中收到工作流程任務。NPR-20213：CQ-4221639 的 Hotfix
* 在工作流程模型的對話參與者步驟中，按下拉式清單時，OOTB Granite 使用者選取器沒有載入任何使用者。NPR-20236

## Forms {#forms-10}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

### Forms 附加元件套件 {#forms-add-on-package-10}

#### 調適型表單 {#adaptive-forms-3}

* 缺少對重複面板彙總運算式的支援。NPR-20861
* 即使相關的表單資料模型服務沒有傳回值，下拉式清單仍會顯示最後儲存的值。NPR-20710
* 無法在規則編輯器中編輯含有布林值限制的現有規則。NPR-21128

#### 表單入口網站 {#form-portal}

* 即使資產類型不是 XDP，仍會為適用性表單顯示 HTML 設定檔。NPR-20079

#### 後端整合 {#backend-integration-2}

* 無法將切換元件的值設定為 true/false。NPR-21111

#### OSGI 工作流程 {#osgi-workflow}

* 管理工作流程提交只列出十個應用程式。CQ-4230193

#### HTML5 Forms {#html-forms-3}

* 如果沒有在協助工具設定中定義名稱，XDP 表單物件 (例如子表單) 的名稱會顯示為其工作提示。NPR-20523

### Forms - JEE 安裝程式 {#forms-jee-installer-9}

#### 處理程序管理 {#process-management-2}

* FormSetPrefillApp 起始點沒有預先填入 AEM Forms 應用程式中的表單集欄位。NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* 針對重大安全漏洞安裝最新 CTJPEG2K 程式庫。這會影響 XMLFM (AEM 和 IfBA)、RM、PDFG 模組。NPR-20625：NPR-21337。

### 包含 Feature Pack {#feature-packs-included}

#### AEM Forms 應用程式 {#aem-forms-app}

* 啟用 AEM Forms App 中的 OSGi 工作流程任務支援。CQ-4222638

### 6.3.1.2 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-6}

AEM 6.3.1.2 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/6_3_1_2-bundle-list.txt)

AEM 6.3.1.2 中包含的內容套件清單

[Get File](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM Cumulative Fix Pack 6.3.1.1 為重要更新，包含自 2017 年 10 月正式發行 AEM 6.3 Service Pack 1 (6.3.1.0) 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 的關鍵重點為：

* 針對預設中繼資料結構表單啟用發佈至 Brand Portal 動作。
* 針對 dc:title 屬性設為 String [] (多欄位) 的影像，在影像卡片上顯示標題的行為變更。
* 以基礎時間元件取代伺服器端的時間轉譯。
* 啟用透過標記管理員/標記控制台將標記從 AEM 發佈至 Brand Portal 的功能。
* 發佈 JSON API 以使用內容片段。
* 內建存放庫 (Apache Jackrabbit Oak) 更新至 1.6.5 版。

### 資產 {#assets-11}

* 將具有相同屬性的兩個欄位對應到不同屬性欄位類型時，系統擲回內部錯誤。NPR-19462：CQ-4216828 的 HF
* dc:title 和 dc:description 不會變更為 crx /de 中的多欄位值。NPR-19570：CQ-4209086 的 HF
* Dynamic Viewer 載入畫質最低的視訊轉譯，用於以製作模式測試視訊播放體驗。NPR-19004
* 無法為名稱中包含空格的資產下載動態轉譯。NPR-19433：CQ-4211738 的 Hotfix
* 無法使用 Chrome 在欄檢視中載入頁面/資產的完整清單。NPR-19566：CQ-4214248 的 Hotfix
* 選取任何結構、搜尋面向或預設集時，無法使用「發佈至 Brand Portal」選項。NPR-19550
* 在欄檢視中選取資產並按一下編輯時，頁面傳回錯誤。NPR-20301：CQ-4224052 的 Hotfix
* 越過正時區和負時區時會關閉資產期限顯示。NPR-20329：CQ-4219333 的 Hotfix

### 行銷活動 {#campaign-2}

* 為促銷活動選擇預設體驗時，促銷活動滑桿元件沒有顯示。NPR-19213

### 整合 {#integration-7}

* 透過匿名使用者存取時，自訂 at.js 檔案不會發佈。NPR-19542：CQ-4219592 的 Hotfix
* 設定精靈中的目標定位引擎欄位設為 ContextHub (AEM) 而非 Adobe Target。NPR-19320：CQ-4218465 的 HF
* 建立體驗期間受眾區段損毀。NPR-19110
* 編輯並儲存目標模組超過一次時，不會在目標定位模式中顯示目標定位對話方塊。NPR-19144：CQ-4216708 的 Hotfix
* 傳統 UI 上 Adobe Digital Publishing Solution 中文章的存取屬性設定錯誤。NPR-19367
* 如果使用者擁有多個區域的存取權，透過 Campaign 對優惠方案進行個人化設定時，自動折疊功能會出現錯誤行為。NPR-19290：CQ-4218029 的 Hotfix

### 網站 {#sites-11}

* 將執行個體升級為 AEM 6.1SP2-CFP3 後，由於 Sidekick.js 中的程式碼變更，系統沒有重新填入多複合欄位下拉式清單值。NPR-19450：CQ-4194771 的 HF
* 在製作模式下 WCMMode.EDIT 無法用於目標元件。NPR-19387
* 發佈 JSON API 以使用內容片段。NPR-19500
* 在製作對話方塊中，粗體、斜體、底線功能無法用於 RTF 編輯器欄位。NPR-19670：NPR-19718：CQ-4219088 的 Hotfix

### Mobile On-Demand {#mobile-on-demand-1}

* AEM 文章控制台出現轉譯問題，使用完整大小的影像導致其速度變得緩慢。NPR-19088

### 轉換 {#translation-5}

* 無法為翻譯專案產生預覽。NPR-19289

### 安全性 {#security}

* SSL 連線錯誤。無法進行安全的伺服器連線。NPR-19628

### 社群 {#communities-9}

* 透過已預先審核的網站發佈內容時會觸發郵件。NPR-20008
* 已發佈元件上與版主相關的任何活動都無法發出電子郵件通知。NPR-19767：CQ-4218060 的 HF

### 平台 {#platform-4}

* AEM 生產伺服器部署的穩定性問題。NPR-19707
* 升級至 AEM 6.3 後，找不到參考標記實作為指令碼的自訂 taglib。NPR-19087
* AEM 6.3.1 的 HTL 錯誤修正。NPR-19161
* 多欄位元件中的 RTF 欄位無法編輯。NPR-19604：Granite-16755 的 Hotfix
* Adobe 電子郵件範本服務為自訂使用者範本新增了標記。NPR-19190
* Oak 1.6.5 的 Hotfix。NPR-19148

### 商務 {#commerce-5}

* 選取 XF 變化編輯器後「開始工作流程」按鈕失效。NPR-19642：CQ-4207796 的 Hotfix

### 專案 {#projects-2}

* 專案編輯器無法將資產複製/貼上至專案資產資料夾中。NPR-19619：CQ-4215321 的 Hotfix

### Web 內容管理 {#web-content-management}

* 在「轉出」畫面中，對應至 Live Copy 頁面的核取方塊無法勾選或取消勾選。NPR-19518
* 因為目前所有索引標籤和欄位都可進行大量編輯，因此無法正常使用頁面屬性大量編輯功能。NPR-19451
* 在傳統 UI 中編輯影像時，OOTB 屬性和影像對齊方式屬性沒有顯示。NPR-19488：CQ-4217914 的 HF

### 使用者介面 {#user-interface-4}

* 使用 Google Chrome 瀏覽器時，使用者無法在觸控式 UI 中使用欄檢視來載入頁面/資產的完整清單。NPR-19566：CQ-4214248 的 Hotfix

### Brand Portal {#brand-portal-1}

* 無法從 AEM 發佈包含評論和附註的資產。NPR-19590：CQ-4218386 的 Hotfix
* 啟用透過標記管理員/標記控制台將標記從 AEM 發佈至 Brand Portal 的功能。NPR-20271：CQ-4223948 的 Hotfix
* 修正 Brand Portal 雲端服務設定 UI 上的「已啟用」欄位。CQ-4211101 的 Hotfix
* 搜尋表單複寫失敗。CQ-4220080 的 Hotfix

## Forms {#forms-11}

透過附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 AEM Forms 發行版本。

### Forms 附加元件套件 {#forms-add-on-package-11}

#### 調適型表單 {#adaptive-forms-4}

* 提交至 JEE 工作流程沒有從 JEE 端傳回輸出參數至 AEM，並擲回「因為值非原始值而忽略」錯誤。NPR-20265
* 在 Safari 中適用性表單不允許 PDF 作為附件。NPR-19625
* RestoreGuideState 會覆寫 customcontextproperty 對應。CQ-4222877
* 使用雲端服務設定 Google reCaptcha 時，在需要 org.apache.http.proxyconfigurator 設定以進行外部連線的環境中，POST 似乎不會通過 PROXY。NPR-20454
* 安裝時以 XSD 結構為基礎的適用性表單所用的地區設定包含「.」以外的小數分隔符號，而對數值欄位提交了有問題的 XML 值，進而導致出現錯誤。NPR-20444
* 對第三方伺服器發出 HTTP 請求時，系統沒有遵循針對「Apache HTTP 元件 Proxy 設定」所設的 Proxy 設定。使用 HTTP GET 或 POST 呼叫時出現連線逾時問題。NPR-20457、NPR-20456、NPR-20455、NPR-20451

#### Forms 資料整合 {#forms-data-integration}

* 針對非英語地區設定，作為 SOAP 服務輸出的 UTF-8 字元沒有正確複製到適用性表單欄位中。NPR-20238：NPR-20103

#### 通信管理 {#correspondence-management-1}

* 在文字編輯器中從 Word 檔案複製貼上內容會失去其內容顏色和字型。NPR-19521

#### 組合器服務 {#assembler-services}

* 對文件進行 PDFA-1b 格式合規性驗證時，Acrobat 和 AEM 的結果出現不一致。NPR-19280

#### 工作流程 {#workflow-2}

* 允許 HTTP 呼叫透過 Proxy 連線的工作流程簽署步驟。NPR-20529

#### HTML5 Forms {#html-forms-4}

* 新增對 preSubmit 事件的支援。NPR-20604

### Forms - JEE 安裝程式 {#forms-jee-installer-10}

#### 處理程序管理 {#process-management-3}

* 當表單最大化/最小化並儲存為草稿或轉寄時，工作區中的工作流程附件、備註和詳細資訊索引標籤無法運作。NPR-20243
* 在 HTML 工作區中提交資料後，多行文字欄位 (TextArea) 沒有保留文字中的新行字元或分行符號。NPR-20085

#### 程序報告 {#process-reporting}

* 由於出現 Null 指標例外狀況，程序報告功能沒有正確擷取資料。NPR-19759

>[!NOTE]
>
>安裝 [AEM Forms 發行版本](aem-forms-releases.md)文章中列出的 LiveCycle 內嵌套件以修正問題。

#### 標準服務 {#standard-services}

* docConvertor 不支援 PDF 中的透明度平面化，且無法產生 PDF/A。NPR-16228：CQ-4214488 的 Hotfix

#### 核心 {#core-2}

* 當 JBoss 應用程式上以叢集設定執行的 AEM Forms 伺服器停止時，應用程式伺服器會中斷與資料庫的連線。這可能導致資料損毀問題。NPR-19724

### 包含 Feature Pack {#feature-packs-included-1}

* 因為資產缺少必要欄位驗證，因此下拉式中繼資料結構欄位無法設為必要。NPR-17882：CQ-4208373 的 FP

### 6.3.1.1 中包含的 OSGI 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-in-7}

AEM CFP 6.3.1.1 中包含的 OSGi 套件組合清單

[取得檔案](assets/do-not-localize/bundle-list.txt)

AEM CFP 6.3.1.1 中包含的內容套件清單

[取得檔案](assets/do-not-localize/content-package-list.txt)

AEM Cumulative Fix Pack 6.3.0.2 為重要更新，包含自 2017 年 4 月正式發行 AEM 6.3 以來累積的多項內部及客戶修正。

AEM Cumulative Fix Pack 的關鍵重點為：

* 使用者存取控制的可稽核性
* 包含內建存放庫的 1.6.2 版 (Apache Jackrabbit Oak)
* 解決無結尾標記的資源解析器問題。
* 簡化智慧內容服務的設定
* 解決內容片段驗證問題
* 改善混合裝置上中繼資料結構的可編輯性
* 解決 Live Copy 中元件層級的同步問題
* 改善欄檢視中含有大量內容的頁面之可用性
* 改善長標題頁面對頁面命名慣例的合規性
* 改善觸控式 UI 上的促銷活動個人化體驗
* 修正多項專案覆蓋問題

### 平台 {#platform-5}

* Oak 1.6.2 的 Hotfix。NPR-19148
* 使用篩選器開啟 Omnisearch 時不再設定路徑。NPR-17398：CQ-4204870 的 Hotfix
* 要求 AEM 中使用者權限變更具有可稽核性。NPR-17061
* 延遲連線至 DM 雲端服務造成「開啟的檔案過多」例外狀況。CQ-4211407

### 資產 {#assets-12}

* 使用不同選項設定智慧內容服務時出現可用性問題。NPR-18200：CQ-4201557 的 Hotfix
* 二進位資料流中的資源洩漏至 S3 資料存放區。NPR-18041：CQ-4209506 的 Hotfix
* 將 ASCII/UTF-8 編碼文字檔上傳至 AEM Assets 時發生錯誤，且產生縮圖失敗。NPR-18006：CQ-4209345 的 CFP
* 預設中繼資料結構造持內容片段驗證失敗。NPR-17769：CQ-4211111 的 Hotfix
* com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner 中無結尾標記的資源解析器。NPR-17598：CQ-4209018 的 CFP
* 請求建立多個複寫代理以用於將資產發佈至 Brand Portal。NPR-17189
* 日文語言資料夾底下的資產審核任務沒有運作。CQ-4204782
* 將資產移至其屬性頁面時發生 Null 指標例外狀況。CQ-4204251
* 如果連結至 InDesign 文件多次，AEM 就無法追蹤屬性頁面中資產的後續參考。CQ-4204186
* 在混合裝置上使用 Chrome 編輯中繼資料結構表單時，在該表單中新增索引標籤會發生問題。CQ-4201810
* 上傳了重複資產時，如果沒有在偵測到重複項目的對話方塊中選擇選項，則 (刪除/保留) 選項會套用至所有資產。CQ-4201673
* 當資產資料夾中有超過 150 傳入的參考移動時，會出現 Null 指標例外狀況。CQ-4200981
* 針對已下載的資產資料夾，擷取 ZIP 檔案的內容時如果發生衝突，預設選項會顯示為「建立版本」而非「保留兩者」。CQ-97800
* 擁有應用程式唯讀權限的使用者無法從 AEM Mobile 內容管理預覽內容。NPR-17486：CQ-4209690 的 CFP
* 「目錄」控制台中，欄檢視中的「建立目錄」按鈕無法運作。CQ-4209952

### 網站 {#sites-12}

* 透過 data-sly-resource 屬性內嵌影像/視訊元件時發生問題。NPR-18182：CQ-4212100 的 CFP
* 在 LiveCopy 中重新套用繼承時，經過修改的當地語系化元件沒有還原為其原始表單。NPR-18172：CQ-4211379 的 Hotfix
* 在觸控式 UI 中以欄檢視導覽含有大量內容的頁面時發生問題。NPR-17799：CQ-4199611 的 Hotfix
* `com.day.cq.wcm.core.impl.VersionManagerImpl` 中無結尾標記的資源解析器。NPR-17789：CQ-4211152 的 CFP
* 長頁面標題沒有依照慣例產生頁面名稱。NPR-17633：CQ-4209056 的 Hotfix
* 在部署於 Jboss EAP 6.4 上的 AEM 6.3 中，使用觸控式 UI 建立頁面時出現問題。NPR-17589：CQ-4210137 的 Hotfix
* 巢狀群組存在時，工作流程狀態提供者會造成執行個體鎖定。NPR-17556：CQ-4202056 的 CFP 請求
* 下列物件中無結尾標記的資源解析器：

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497：CQ-4208673 的 CFP
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495：CQ-4208668 的 CFP
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494：CQ-4208669 的 CFP
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493：GRANITE-17404 的 CFP

### Integrations {#integrations-1}

* 解決 AEM Day HTTP Client 3.1 OSGI 設定的 Proxy 要求進行摘要式驗證時可能出現的 AEM 搜尋元件錯誤。NPR 18128：NPR-18029 的 Hotfix
* 透過傳統 UI 個人化促銷活動和相關體驗時發生問題。NPR-18127：CQ-4211559 的 Hotfix
* 將品牌/區域設為網站的根頁面時，一旦取消繼承，就無法再為子頁面中的區域還原。NPR-17753：CQ-4210139 的 Hotfix

### 工作流程 {#workflow-3}

* 在非暫時性工作流程中，執行外部處理步驟之前進行的處理程序歷史記錄和中繼資料變更都不會保留。NPR-17848：GRANITE-17757 的 Hotfix
* 工作流程對話方塊欄位的值沒有保留在工作項目節點中。NPR-17734：CQ-4210369 的 Hotfix
* 編輯收件匣中的任務時發生無法剖析的日期錯誤。CQ-4208749

### 專案 {#projects-3}

* 修正多項專案覆蓋問題。NPR-17733
* 重建專案模組中的 Pod 以降低其可設定性。CQ-4209859
* 頁面新增至翻譯工作時，資產路徑會針對個別本地化網站進行路徑變更。CQ-4206007

### 安全性 {#security-1}

* 上傳 LDAP 使用者的顯示圖片影像時發生問題。NPR-16561
* 請求在 Apache Sling API 中使用 org.apache.sling.servlets.post servlet 的升級版本 (2.3.22) 以搶先遏止 XSS 漏洞。NPR-18963

## Forms {#forms-12}

透過 Forms 附加套件和發行版本隨附的其他修補安裝程式來提供 AEM Forms 修正。如需詳細資訊，請參閱 [AEM Forms 發行版本](aem-forms-releases.md)。

AEM Forms 的關鍵重點為：

* 通信管理文字模組、信函預覽和以程式編寫方式啟動建立通信管理 UI 的修正。
* PDF 產生器中對 PDF/A-1b 驗證、大型影像檔案轉換為 PDF，以及日文 PDF 文件的修正。
* 通信管理、文件安全性和表單工作流程的可用性修正。
* 新增支援以擷取手寫簽名欄位的稽核事件。

### Forms 附加元件套件 {#forms-add-on-package-12}

**通信管理**

* 編輯通信管理片段時，文字編輯器顯示內嵌條件以及經處理的文字。CQ-4211930
* 建立通信管理信函時沒有儲存信函說明。NPR-18089
* 項目符號清單上下方的額外邊界可以在文字編輯器中看到，但在 HTML 和 PDF 轉譯中看不到。NPR-18126
* HTML 提交使用 POST 方法時，建立通信 UI 無法啟動。NPR-18202
* 文字模組已儲存，且文字模組中的運算式不包含開頭或結尾運算式標記時，系統沒有顯示錯誤訊息。文字模組顯示錯誤訊息且無法在信函中轉譯。NPR-18535
* 新增了內容或按下 Enter 鍵時，系統將 div 標記新增至文字模組中。NPR-18240

**組合器**

* 驗證 PDF 文件的 PDF/A-1b 合規性時 AEM Forms 傳回驗證錯誤：PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED。透過 Adobe Preflight 和第三方軟體進行驗證時，PDF 文件沒有傳回錯誤。NPR-18011
* 驗證 PDF 文件的 PDF/A-1b 合規性時AEM Forms 傳回驗證錯誤：表單欄位有多種外觀。PDF 文件符合 PDF/A-1b。NPR-18013

**監看資料夾**

* 使用工作流程選擇處理檔案時，在建立監看資料夾期間，顯示的工作流程模型選擇下拉式清單遭截斷。NPR-17566

**HTML5 Forms**

* AEM Forms 沒有擷取手寫簽名欄位的稽核事件。NPR-15286

**Forms Manger**

* AEM Forms UI 從最舊到最新列出所有資產。使用者無法從最新到最舊重新排序資產。NPR-18450

**Java API 參考**

為 com.adobe.livecycle.content 類別新增 JavaDocs。NPR-18468

### Forms - JEE 安裝程式 {#forms-jee-installer-11}

**PDF 產生器**

* PDF 產生器服務無法將大於 100 MB 的影像轉換為 PDF 文件。參考編號 CQ-4208628
* 搭配日文 OCR 使用 PDF 產生器服務時，會產生反轉的 PDF。NPR-17602

**處理程序管理**

* 沒有為 AEM Forms 處理程序填入 TaskContext 變數。NPR-18199

**文件安全性**

* Microsoft Excel 和 Microsoft PowerPoint 花很長的時間開啟受到 Microsoft Office 版 AEM 文件安全性延伸模組保護的文件。CQ-4212358
* 建立新原則且名稱與現有原則相同時，會發生內部伺服器錯誤。NPR-18247

## 包含 Feature Pack {#feature-packs-included-2}

* 要求 AEM 中使用者權限變更具有可稽核性。NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 為重要更新，包含自 2017 年 4 月正式發行 AEM 6.3 以來累積的多項內部及客戶修正。AEM Cumulative Fix Pack 的關鍵重點為：

* 改善下列領域：

   * 內容片段、網站以及 RTF 編輯器、規則編輯器和範本編輯器元件
   * Social Review 和 Facebook Social 登入
   * 設定和開始翻譯工作
   * 存取社交社群中通知的回應時間
   * 顯示 DAM 存放庫中的審核任務

* 套件管理器中提供可偵測覆蓋和 CFP 之間衝突的驗證選項

## 透過 Software Distribution 下載 CFP 的指示 {#download-instructions-for-cfp-via-package-share}

您可以直接從 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) 下載 CFP 套件或執行以下步驟：

1. 開啟 [Software Distribution](https://experience.adobe.com/downloads)。您需要 Adobe ID 才能登入 Software Distribution。
1. 點一下頁首功能表中的 **[!UICONTROL Adobe Experience Manager]**。
1. 點一下套件名稱，選取&#x200B;**[!UICONTROL 「接受 EULA 條款」]**，然後點一下&#x200B;**[!UICONTROL 「下載」]**。

## 安裝指示 {#installation-instructions}

本節逐一說明安裝 CFP 的要求和步驟。

### 安裝之前 {#before-you-install}

>[!NOTE]
>
>Adobe 提供的選用 Feature Pack 依存於發行版本和 Cumulative Fix Pack。若您已安裝任何 Feature Pack，請聯絡 [AEM 客戶服務團隊](https://helpx.adobe.com/tw/marketing-cloud/contact-support.html)以驗證與這個適用 AEM 6.3 的 Cumulative Fix Pack 之間的相容性。

>[!NOTE]
>
>建議您在嘗試安裝之前，先對每個新安裝套件都執行驗證。安裝之前預先驗證程序會分析並報告所有發現的錯誤，並主動警告使用者出現這些錯誤。
>
>如需驗證選項的說明文件，請前往 [https://docs.adobe.com/content/docs/zh-Hant/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/zh-Hant/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 是 CFP 的必備條件。請參閱[升級說明文件](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html)，取得有關將 AEM 安裝升級為 AEM 6.3 的詳細指示。
* 針對使用 RDBMK 或 MongoDB 的叢集部署，CFP 套件可安裝在使用套件管理器的任何製作執行個體上。
* 安裝 Cumulative Fix Pack 之前，請務必拍攝快照或備份您的 AEM 執行個體。
* 不支援解除安裝 CFP。

### 新增記錄器 {#adding-new-loggers}

若要在安裝 SP/CFP 期間設定除錯層級記錄和擷取活動記錄，可以依照以下步驟操作：

* 您可以使用以下屬性來在預設位置新增記錄器 [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog)：

   * 記錄層級：Debug
   * 加總：false
   * 記錄檔：logs/activity.log
   * 記錄器：org.apache.jackrabbit.vault.packaging.impl.ActivityLog

activity.log 會建立在 crx-quickstart/logs 資料夾中

### 透過 Software Distribution 安裝 Cumulative Fix Pack {#install-the-cumulative-fix-pack-via-package-share}

執行以下步驟來在現有 AEM 6.3 執行個體上安裝 Cumulative Fix Pack：

1. 按一下 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) 連結即可下載套件。

1. 開啟[套件管理器](http://localhost:4502/crx/packmgr/index.jsp)，然後按一下&#x200B;**[!UICONTROL 「上傳套件」]**&#x200B;即可上傳套件。

1. 選取套件名稱並按一下&#x200B;**[!UICONTROL 「安裝」]**。

### 自動安裝 {#automatic-installation}

可藉由以下方式將 CFP 自動安裝至執行中的執行個體：

* 伺服器執行期間將套件置於 `../crx-quickstart/install`。套件便會自動安裝。
* [從套件管理器使用 HTTP API](https://helpx.adobe.com/tw/experience-manager/6-3/sites/administering/using/package-manager.html) (請務必使用 `cmd=install&recursive=true`) 以安裝巢狀套件。

### 驗證安裝 {#validate-installation}

1. 產品資訊頁面 (`/system/console/  productinfo`) 現在應在「已安裝產品」下方顯示更新的版本字串「Adobe Experience Manager，6.3.3.8 版」。
1. 在 OSGI 控制台 (使用 Web 控制台：`/system/console/bundles`) 中，所有 OSGI 套件組合均為「作用中」或「片段」。

>[!NOTE]
>
>成功安裝套件時，提供資訊的訊息會顯示在錯誤記錄上，指出已成功安裝內容套件，例如「已成功安裝 **AEM-6.3.3-Cumulative-Fix-Pack-7** 內容套件」。

>[!NOTE]
>
>自 AEM 6.3.3.1 起，Jackrabbit FileVault 中大部分訊息的記錄層級已從「資訊」變更為「除錯」。若要取得 AEM 6.3.3.1 或以上版本所安裝內容套件的安裝記錄，請為 org.apache.jackrabbit.vault.packaging.impl 啟用「除錯」記錄層級。

### 安裝 AEM Forms {#install-aem-forms}

>[!NOTE]
>
>如果您沒有使用 AEM Forms，請略過本節。

#### 安裝 AEM Forms 附加元件 {#install-forms}

1. 確認您已安裝 AEM 6.3.3.x CFP 套件。
1. 下載適用於您作業系統的 [AEM Forms 發行版本](aem-forms-releases.md)所列出的對應 Forms 附加套件。
1. 依照[安裝 AEM Forms 附加元件套件](https://helpx.adobe.com/tw/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html)中的說明安裝 Forms 附加元件套件。

#### 安裝 AEM Forms JEE 套件組合套件 {#install-aem-forms-jee-bundles-package}

AEM Forms JEE 中的修正是透過單獨的安裝程式提供。如需更多有關在 JEE 版 AEM Forms 上安裝 CFP 的資訊，請參閱[在 AEM Forms JEE 上安裝 CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer 安裝程式 {#designer-installer}

1. 若要安裝更新，請執行 Designer 6.2.0_&lt;語言>_Cumulative_QF.msp 檔案。
1. 在歡迎畫面中按一下&#x200B;**「更新」**。安裝程序隨即會開始。
1. 安裝完成後，請按一下&#x200B;**「完成」**。

## 配置 AEM Forms JEE (JBoss EAP) 的設定  {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>若您是安裝 6.3.3.0 或更新版本，請執行以下程序來配置 JBoss 應用程式伺服器的設定。若您是在 Oracle WebLogic 或 IBM WebSpehere 應用程式伺服器上所執行的 AEM Forms 伺服器上安裝 6.3.3.0，則無需進行額外設定。如需更多詳細資訊，請參閱 [AEM 6.3.3.0 發行說明](https://helpx.adobe.com/tw/experience-manager/6-3/release-notes/sp3-release-notes.html)。

## 更新 Search&amp;Promote 整合的設定 {#configuration-updates-for-search-promote-integration}

若使用 AEM Cumulative Fix Pack 6.3.0.2 和更新版本，用於 Search&amp;Promote 整合的 OSGi 設定為 **Apache HTTP 元件 Proxy 設定**。不再使用 Day Commons HTTP Client 3.1 的 Proxy 設定。

## 已知問題 {#known-issues}

* 安裝 AEM CFP 6.3.3.x 期間可能會出現下列錯誤和警告，且可安全地忽略：

   * &#42;警告&#42; [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl掛接/META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar with-dependencies.jar引發運行時異常。
   * &#42;錯誤&#42; [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] 等待註冊表更改完成註銷時超時。 CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver 服務遺失，無法處理請求並傳送狀態 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource：無法檢查資源 [/bin/receive]，頁面管理器無法使用
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver：呼叫錯誤處理常式導致一項錯誤
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver 原始錯誤 null
   * org.apache.sling.engine.impl.DefaultErrorHandler 錯誤處理常式失敗：java.io.IOException
   * &#42;錯誤&#42; [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR(org.osgi.framework.ServiceException:服務工廠返回空值。 (元件：com.day.cq.dam.handler.standard.ps.PostScriptHandler))

**Brand Portal**

* 自 6.3.1.2 開始，移除了智慧型集合的「發佈至 Brand Portal」按鈕。

**使用者介面**

>[!NOTE]
>
>若您受到這兩個問題其中任何一個的影響，請聯絡 [AEM 客戶服務](https://helpx.adobe.com/tw/marketing-cloud/contact-support.html)。

* 由於管理搜尋功能中有大量請求，出現高 CPU 使用量問題。NPR-24229
* 重新開啟元件時沒有選取 pathBrowser 中的 PathField。NPR-24177

## NPR-27692 所需的配置設定 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>此配置設定適用於 CFP 6.3.3.2 和更新版本。它會引導您更新 `sling` .properties 檔案中的開機委派屬性。

若要手動更新 adobe-livecycle-cq-author.ear/cq.war 中的變更，請依照下術步驟操作：

* 停止 AEM 伺服器。
* 前往 adobe-livecycle-cq-author.ear/cq.war
* 開啟 adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml 進行編輯：

   * 用以下內容更新 **sling.bootdelegation.ibm** param-name 值：

      * com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * 進行上述變更後，init-param 看起來應該像這樣：

      * &lt;init-param>\
         &lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* 請依照 [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf) 中 10.2 節提供的步驟操作，從 Websphere 應用程式伺服器解除安裝先前的 Enterprise Archive (EAR) 檔案，並安裝更新版 EAR 檔案。
* 儲存檔案並重新啟動伺服器。[https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## NPR-23208 所需的配置設定 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>此配置設定適用於 6.3.2.2 和更新版本。它會指引您透過 CRX-DE 手動更新存取控制清單 (ACL) 原則，因為受到「merge_preserve」acHandling 影響，ACL 不會透過 CFP 安裝更新。

**手動新增 ACL 原則的說明文件**

若要更新 ACL 原則，請透過 CRX-DE 新增以下存取控制：

`1)` At &quot;/content&quot; path\
`a)` Principal : reference-adjustment-service\
Type : Allow\
Privileges : jcr:read , jcr:modifyProperties\
限制：rep:glob=&quot;/&#42;/jcr：內容&quot;\
`b)` Principal : reference-adjustment-service\
Type : Allow\
Privileges : jcr:read , jcr:modifyProperties\
限制：rep:glob=&quot;/&#42;/jcr：內容/&#42;&quot;

`2)` At &quot;/content/usergenerated&quot; path\
`a)` Principal : reference-adjustment-service\
Type : Allow\
Privileges : jcr:write

`3)` At &quot;/etc&quot; path\
`a)` Principal : reference-adjustment-service\
Type : Allow\
Privileges : jcr:read , jcr:modifyProperties\
限制：rep:glob=&quot;/&#42;/jcr：內容&quot;\
`b)` Principal : reference-adjustment-service\
Type : Allow\
Privileges : jcr:read , jcr:modifyProperties\
限制：rep:glob=&quot;/&#42;/jcr：內容/&#42;&quot;

## NPR-19450 所需的配置設定 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>此配置設定適用於 CFP 6.3.1.1 和更新版本。

**設定 CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL 屬性。**

此屬性會控制頁面 ` /  jcr   :content` 節點底下節點子樹狀結構的深度上限，存放庫中到該深度為止的節點應該用於取得頁面屬性。此屬性中比該指定深度還深的任何節點都會被忽略。

預設值為 1。此值可由覆蓋檔案 constants.js (`/libs/cq/ui/widgets/source/constants.js`) 覆寫，方法是取消註解 CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL 屬性並指派所需的值 (頁面 /jcr:content 底下的深度上限，系統會儲存到該深度為止的頁面屬性資料)。

**如果使用者需建立許多頁面變體，以至於頁面 /jcr:content 節點之下的節點數超過 1000，請使用下列步驟來進行設定變更：**

* 設定 Apache Sling 的 JSON Max 結果屬性
* 使用 `/system/console/  configMgr` 取得 Servlet
* 將其值設為 >1000 (目前的預設值)，讓此數大於 /jcr:content 子樹狀結構中所設定深度之上的總結點數。

如此一來 Sling GET servlet 就可以傳回所有需要的節點。

## Uber Jar {#uber-jar}

適用於 6.3.3.8 的 Uber Jar 可於 [Adobe Public Maven 存放庫](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/)取得。

若要在 Maven 專案中使用 Uber Jar，請參閱[如何使用 Uber jar](https://helpx.adobe.com/tw/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) 一文，並在您的專案 POM 中加入以下相依性：

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## 已移除/已棄用的功能 {#deprecated}

本節列出 AEM 6.3 已移除或棄用的特色和功能。

| 區域 | 功能 | 替代方案 | 版本 |
|----|-----|-----|-----|
| Assets 與 Adobe Creative Cloud 整合 | AEM 6.2 引入了 [AEM 對 Creative Cloud 資料夾共用](https://helpx.adobe.com/tw/experience-manager/6-3/sites/administering/using/creative-cloud.html)功能，作為讓 Creative 使用者存取 AEM 資產的方式。Creative Cloud 應用程式推出的新功能 Adobe Asset Link 提供了更優異的使用者體驗，以及更強大的存取功能，可直接從 Photoshop、InDesign 和 Illustrator 中存取 AEM 的資產。<br /> Adobe 將不會再對資料夾共用功能提供近一步的增強項目。由於此功能包含在 AEM 中，強烈建議使用替代功能。 | Adobe Asset Link 或桌面應用程式。如需更多資訊，請參閱 [AEM Creative Cloud 整合](https://helpx.adobe.com/tw/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html)文章。 | AEM 6.3.3.x |

## 包含的 OSGi 套件組合和內容套件 {#osgi-bundles-and-content-packages-included-1}

下列文字記錄列出 CFP 中包含的 OSGi 套件組合和內容套件清單。

* [AEM 6.3.3.8 中包含的 OSGi 套件組合清單](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [AEM 6.3.3.8 中包含的內容套件清單](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM 發行版本和更新](https://helpx.adobe.com/tw/experience-manager/aem-releases-updates.html)
>* [AEM 6.3 Hotfix 頁面](https://helpx.adobe.com/tw/experience-manager/kb/aem63-available-hotfixes.html)
>* [AEM 6.3 發行說明](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM 產品頁面](http://www.adobe.com/tw/solutions/web-experience-management.html)
>* [AEM 6.3 檔案](https://docs.adobe.com/content/docs/zh-Hant/aem/6-3.html)
>* 訂閱 [Adobe 優先產品更新](https://www.adobe.com/tw/subscription/priority-product-update.html)

