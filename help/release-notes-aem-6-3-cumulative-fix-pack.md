---
title: AEM 6.3 Cumulative Fix Pack
description: AEM 6.3 Cumulative Fix Pack發行說明
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '15916'
ht-degree: 1%

---


# AEM 6.3 Cumulative Fix Pack發行說明{#release-notes-aem-cumulative-fix-pack}

## 發行資訊{#release-information}

| **產品** | Adobe Experience Manager |
|---|---|
| **版本** | 6.3 |
| **發行** | [PackageShare](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8)、[軟體散發（測試版）](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip)上的累積修補程式套件6.3.3.8 |
| **先決條件** | [AEM 6.3 Service Pack 3(6.3.3.0)](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **全面上市** | 2020年3月05日 |

### 累積修補程式套件{#cumulative-fix-pack}

Adobe推出單一傳送模型來發佈修正。 Adobe現在不會針對個別問題發佈Hotfix，而是每個月發行Cumulative Fix Pack(CFP)（必須經過品質檢查）。 CFP是整合式內容套件，可用於多項修正。 CFP主要包含錯誤修正，但也可能包含功能套件。 相較於個別的修補程式版本，它們有下列優點：

* 累積性（例如，CFP包含透過舊版CFP提供的修正）
* 提高品質保證
* 簡化安裝（使用者將CFP安裝為單一套件，除最新的Service Pack外，沒有相依性）

如需有關CFP和其他類型發行的詳細資訊，請參閱[維護髮行工具定義。](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html)

## 關於版本{#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8是自2018年9月AEM 6.3 Service Pack 3(6.3.0)全面推出以來，包含數項內部和客戶修正的重要更新。

AEM Cumulative Fix Pack 6.3.3.8取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.20版。

>[!CAUTION]
>
>在不驗證已安裝功能套件之間相容性的情況下套用CFP，可能會導致系統故障或遺失自訂組態，而這可能需要從備份還原才能解決。

>[!NOTE]
>
>對於版本低於6.3.3.0的AEM例項，Adobe建議透過安裝資料夾為在AEM例項上有大量使用者的客戶部署SP/CFP。

>[!NOTE]
>
>從AEM 6.3.3.1版開始，支援MongoDB Enterprise 3.6。

## 問題清單{#changes}

本節列出目前CFP中包含的所有問題和修補程式。

此外，此CFP還包含在[先前累積修補程式套件](#previous)中提供的修補程式。

### 資產 {#assets}

* 新增資產至系列時，「新增至系列」頁面不會在「卡片檢視」中顯示所有可用的系列(NPR-32537)。

### 網站 {#sites}

* 當您選取parsys和其中的元件，並使用鍵盤快速鍵刪除選取的項目時，動作會同時刪除元件及其父項parsys(NPR-32071)。
* 保存頁面屬性時，會建立不正確的節點(NPR-31774)。

### 整合{#integrations}

* ReportSuitesServlet易受SSRF的攻擊(NPR-32162)。

### 促銷活動定位{#campaign-targeting}

* 在「作者」例項中變更後再啟動的元件內容，在「發佈」例項中無法顯示，直到元件重新啟動&#x200B;**com.day.cq.personalization.impl.TargetedContentManagerImpl**（NPR-32489和NPR-32232）。
* Contexthub在出版時的效能當機(NPR-31170)。

### 品牌入口網站 {#brand-portal}

* Adobe I/O未與Adobe Experience Manager 6.3 for Brand Portal整合(NPR-32056)。

### 表單 {#forms}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

#### Forms add-on package {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms附加套件有助於將表單功能與AEM Service Pack和Cumulative Fix Pack對齊。 因此，在安裝任何AEM Service Pack、Cumulative Fix Pack或Feature Pack後，必須安裝AEM Forms附加套件。

* 設計人員：如果啟用標籤選項，子表單邊框會消失在產生的PDF輸出中（NPR-32324和NPR-32545）。
* 設計人員：如果表格中有合併的儲存格，則無障礙環境支援測試會失敗，無法針對使用輸出服務從XDP表單轉換的輸出PDF檔案(NPR-32068)。
* 檔案安全性：受保護的PDF檔案無法離線開啟，`DisableGlobalOfflineSynchronizationData`選項設為`True`(NPR-32080)。

## 舊版累積修補程式套件包含的修補程式和功能套件{#previous}

### 累積修補程式套件6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7是重要的更新，自2018年9月AEM 6.3 Service Pack 3(6.3.3.0)全面推出以來，已包含數項內部和客戶修正。

AEM Cumulative Fix Pack 6.3.3.7取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

### 資產 {#assets-1}

* 在從「僅內容」下拉式清單中選取篩選選項，然後選取移動選項之前，選取的資產（在觸控UI的「欄檢視」中）也會移動(NPR-30693)。
* `${extension}`變數不會在工作流程處理的作者實例中呈現(NPR-31694)。
* 為「動態媒體混合」模式配置的過期（用戶端快取至上線時間）值不會複製至動態媒體傳送環境(NPR-31114)。
* 即使在使用預設篩選器(NPR-30856)後，資產也會從在Dynamic Media - Scene7部署上執行的「作者」例項複製至「發佈」例項。

### 網站 {#sites-1}

* 載入主版頁面的頁面屬性失敗，並傳回NullPointerException。 新增cq:blueprint屬性(NPR-30901)時，問題已解決。
* 轉出配置無法從根節點上的blueprintConfig中正確檢索。 藍圖和即時副本都會觸發停用。 請僅針對Blueprint觸發停用(NPR-30866)。
* 當使用者卷出頁面時，卷出設定對話方塊會顯示重複的即時複製路徑(NPR-30438)。
* 立即可用的腳手架Rich Text Editor(RTE)。 意外地將內嵌字型大小套用至元素(NPR-31283、NPR-30922)。
* 無法同步包含現成可用設計匯入工具元件的Adobe促銷活動(NPR-30890)。
* 富格文本編輯器(RTE)。 不允許將嵌入表作為清單項插入(NPR-30878)。
* 當使用者專注在左側欄位並使用鍵盤快速鍵貼上內容時，會貼上頁面編輯器剪貼簿的內容，而非從左側欄位複製的內容(NPR-31173)。
* 當用戶編輯內容片段時，恢復內容片段的已刪除的變化(NPR-31272)。
* AEM網站沒有建立語言副本的選項(NPR-30690)。
* 頁面編輯器的動作沒有控制項來發佈即時副本(NPR-30613)。

### 社群 {#communities}

* 活動和通知標題不一致(NPR-30940)。
* Analytics報表未填入AEM作者環境，空白頁面會出現(NPR-30905)。
* 在社群部落格中編頁無法正常運作(NPR-30827)。

### 基礎{#foundation}

* 不會儲存Jetty型HTTP服務緩衝區大小設定的更新(NPR-30925)。

### 表單 {#forms-1}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms附加套件有助於將表單功能與AEM Service Pack和Cumulative Fix Pack對齊。 因此，在安裝任何AEM Service Pack、Cumulative Fix Pack或Feature Pack後，必須安裝AEM Forms附加套件。

#### 適用性表單 {#adaptive-forms}

* 使用指令碼計算的浮動值無法正確顯示為表單集的一部分的表單(NPR-30802)。

#### HTML5 Forms {#html-forms}

* 產生XDP表單的HTML5預覽會在新增子表單例項時顯示閃爍(NPR-30908)。

### Forms JEE安裝程式{#forms-jee-installer}

#### 文件服務 {#document-services}

* 在套用修補程式將HTML修正為PDF問題後，OutputService會顯示不正確的回應(NPR-31504)。

#### PDFG服務{#pdfg-service}

* JMX主控台的最大重複使用計數不會針對HTML2PDF服務顯示(NPR-30305)。

#### Foundation JEE {#foundation-jee}

* JMX主控台的最大重複使用計數不會針對HTML2PDF服務顯示(NPR-30136)。

### 累積修補程式套件6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6是自2018年9月AEM 6.3 Service Pack 3(6.3.0)全面推出以來，包含數項內部和客戶修正的重要更新。

AEM Cumulative Fix Pack 6.3.3.6取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

### 資產 {#assets-2}

* 「動態視訊」的視訊匯總只會傳回結果集中前100個項目。 NPR-30441;CQ-4213561的修補程式
* 透過Datapower的Adobe Smart Tag連線問題。 NPR-30026:CQ-4269457的修補程式
* 無法使用「資產」介面開啟具有名稱中含百分比符號(%)的檔案夾解壓縮。 NPR-29989:CQ-4270467的修補程式
* 處理大型PDF檔案的子資產會造成OutOfMemoryError(OOME)例外。 NPR-29851:CQ-4269574的修補程式

### 網站 {#sites-2}

* AEM和促銷活動整合期間發生ContextHub錯誤。 NPR-30624:CQ-4250790的修補程式
* 如果AEM伺服器重新啟動，不會回調儲存在資產上的&#39;onTime&#39;或&#39;offTime&#39;中繼資料屬性。 NPR-30412:CQ-4272784的修補程式
* 產生CSV匯出時，新增清單檢視的自訂欄會中斷報表。 NPR-30208:CQ-4273344的修補程式
* /etc/reports/中的OOTB報表無法正常運作，歷史資料圖表也無法顯示。 NPR-30016:CQ-4220180的修補程式
* resourceType請求參數的值被複製到HTML標籤屬性的值中，該屬性被封裝為雙引號。 NPR-29832:CQ-4255365的修補程式

### 社群 {#communities-1}

* AEM Communities協調主控台的內容問題重複。 NPR-30667:CQ-4276829的修補程式

### 轉換 {#translation}

* 翻譯問題——使用「機器翻譯」翻譯的元件只有幾個。 NPR-30079:CQ-4273764的修補程式
* 使用翻譯框架時，將頁面添加到多個翻譯作業會觸發錯誤。 NPR-29746:CQ-4270953的修補程式

### 表單 {#forms-2}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms附加套件有助於將表單功能與AEM Service Pack和Cumulative Fix Pack對齊。 因此，在安裝任何AEM Service Pack、Cumulative Fix Pack或Feature Pack後，必須安裝AEM Forms附加套件。

#### HTML5 Forms {#html-forms-1}

* 當在瀏覽模式中使用非視覺案頭存取來讀取HTML5表格時，Chrome瀏覽器會在表單設計中的每個可縮放向量圖形(SVG)之前讀取「圖形」。 NPR-30451:CQ-4274732的修補程式

#### 表單——後端整合{#forms-backend-integration}

* 在建立表單資料模型(FDM)時，無法查看資料庫連接的服務／資料源。 NPR-30108:CQ-4273359的修補程式

### Forms JEE安裝程式{#forms-jee-installer-1}

#### 表單——文檔服務{#forms-document-services}

* 當對HTML至PDF服務執行載入測試時，它會失敗，並出現錯誤，而且檔案類型設定會從AEM表單伺服器移除。 NPR-30111、NPR-30086:CQ-4271495的修補程式

### 累積修補程式套件6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5是自2018年9月AEM 6.3 Service Pack 3(6.3.0)全面推出以來，包含數項內部和客戶修正的重要更新。

AEM Cumulative Fix Pack 6.3.3.5取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.17版。

### 資產 {#assets-3}

* 更新DAM DMGateway介面，以支援S3多部份。 NPR-29740:Q-4226303的修補程式
* 無法從資產詳細資料頁面刪除視訊資產上的影像轉譯。 NPR-29417:CQ-4268675的修補程式
* 擁有者無法在私人資料夾內建立私人資料夾。 NPR-29397:CQ-4229830的修補程式
* 上傳超過2 GB的Adobe Illustrator圖稿檔案會產生Java堆積空間錯誤。 NPR-29265:CQ-4226217的修補程式
* 在DAM CQ Mime Type Service套用m3u8文字後，資產就變得無法使用。 NPR-29259:CQ-4264052的修補程式
* 嘗試在Edge中建立系列時，建立選項無法運作。 NPR-29248:CQ-4265699和CQ-4265438的修補程式
* 資產連結共用會針對資料夾中的某些資產顯示空白的灰色卡片。 NPR-29831:CQ-4270187的修補程式
* 新增至資產的新標籤無法儲存並從屬性中消失。 CQ-4271931、CQ-4270476的修補程式

### 網站 {#sites-3}

* CoralUI搭配Multifield使用時，會將fileReferenceParameter儲存在元件層級，而非多欄位層級。 NPR-29535:CQ-4266129的修補程式
* 嘗試比較AEM 6.3.3.3的最新和目前頁面版本時發生問題。NPR-29532:CQ-4269639的修補程式
* 路徑欄位會在根路徑開啟，而不考慮指定的搜尋路徑。 NPR-29398:CQ-4268897的修補程式
* （體驗片段）FacebookApplication#setUpApp使用已過時的API，但已無法運作。 NPR-29213:CQ-4266630的修補程式
* 在實例上啟用微型化時，將元件添加到WCM頁時，將生成錯誤警報。 NPR-29476:CQ-4266197的修補程式
* 在轉出期間，空屬性和多個屬性不會從Blueprint傳播。 使用Blueprint重設即時副本無法用於元件。NPR-29252:CQ-4264928、CQ-4264926、CQ-4267722的修補程式
* 在原始碼編輯模式中，從全螢幕將Rich Text Editor最小化會導致內容遺失。 NPR-28838:CQ-4260584的修補程式

### 社群 {#communities-2}

* 沒有協調者權限的訪客和成員可以透過貼上URL來查看未核准和待審貼文。 NPR-29726:CQ-4271124的修補程式
* 使用者登入社群時，可觀察到高達40-50秒的高回應時間。 NPR-29679:CQ-4269444的修補程式
* 使用不同的使用者名稱登入時無法重設密碼，而且由於密鑰似乎是以交換的使用者名稱和電子郵件產生。 NPR-29281:CQ-4268694的修補程式

### 體驗片段 {#experience-fragments}

* 當使用智慧型影像時，無法將體驗片段匯出至目標。 CQ-4269606的修補程式

### 複寫 {#replication}

* Replication Agent元件容易受到向未授權用戶洩漏敏感資訊的漏洞的攻擊。 NPR-29613:Granite-25070的修補程式
* 在`cq/replication/components/agent`元件的輸出中，不會逸出使用者提供的資料，造成儲存的跨網站指令碼(XSS)弱點。 NPR-29452:CQ-4266263的修補程式

### 表單 {#forms-3}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

### Forms add-on package {#forms-add-on-package-3}

* Forms附加元件套件中沒有新的AEM Forms修正。

### Forms JEE安裝程式{#forms-jee-installer-2}

* Forms JEE安裝程式中沒有新的AEM Forms修正。

### 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}隨附的OSGI組合和內容封裝

AEM 6.3.3.5隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6_5-bundle-list.txt)

AEM 6.3.3.5內容套件清單

[取得檔案](assets/do-not-localize/content_packages6335.txt)

### 累積修補程式套件6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4是自2018年9月AEM 6.3 Service Pack 3(6.3.0)全面推出以來，包含數項內部和客戶修正的重要更新。

AEM Cumulative Fix Pack 6.3.3.4取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.16版。
* 已在品牌入口網站複製代理中新增通訊端逾時和連線逾時。

### 資產 {#assets-4}

* 如果重新上傳同名的封存，則不會為新處理的資產產生轉譯。 NPR-28643:CQ-4262286的修補程式
* Workflow CommandLineProcess失敗，檔案名稱只有單引號。 NPR-28805:CQ-4262287的修補程式
* 使用篩選器的系列頁面和系列頁面的值不同。 NPR-28642:CQ-4261405的修補程式
* CommitFailedException觸發器，可上傳大型郵遞區號封存資產。 NPR-28528:CQ-4260903的修補程式
* 編輯包含特殊字元的資料夾時，資料夾中繼資料無法儲存。 NPR-28211:CQ-4260401的修補程式
* 無法從「資產詳細資料」頁面刪除視訊資產的影像轉譯。 NPR-29149:CQ-4266073的修補程式
* 使用DMComponent的DMS7案頭視訊傳送使用漸進式下載來在發佈模式中播放視訊，而不會串流。 NPR-28754:CQ-4263732的修補程式
* 無法建立／編輯影像預設集，因為限制存取/etc/dam/video/dynamicmedia會停用影像管理員的功能。 NPR-28662:CQ-4263022的修補程式
* 與DMS7編碼視訊檔案的連結共用會產生空白的資料夾。 NPR-28851:CQ-4206743的修補程式
* 從AEM複製至品牌入口網站的時間會很長。 NPR-28913:CQ-4254932的修補程式

### 社群 {#communities-3}

* 無法開啟在Outlook發送和收件箱資料夾中包含附件的郵件。 NPR-28559:CQ-4217072的修補程式

### 網站 {#sites-4}

* 6.3版SeckuingHandler中的跨網站指令碼(XSS)。NPR-28692:CQ-4253821的修補程式
* 深入的展示結束，而不會包含個別LiveCopy中的所有分支。 NPR-29175:CQ-4239472的修補程式
* (MSM)使用oak-index建置LiveCopyIndex。 NPR-29198:CQ-4222472的修補程式
* 檔案&#39;coral.js&#39;包含有弱點的程式庫&#39;handlebars.js&#39;版本。 NPR-26973:CQ-4255377的修補程式
* 使用含巢狀版面容器和文字元件的Target元件時，在編輯文字或按一下容器時會引發JavaScript錯誤「無法讀取屬性currentPos of null」。 NPR-29077:CQ-4246594的修補程式
* (Touch UI)無法將標籤大量更新至已由不同標籤標籤的頁面。 NPR-28729:CQ-4262922的修補程式
* 在卡片檢視中開啟變數會造成500錯誤。 NPR-28611:CQ-4263571的修補程式
* 在主版中移動的結構的轉出會導致錯誤cq:moveTarget。 NPR-28968:CQ-4265280的修補程式

### 整合{#integration}

* （雲端服務設定）應移除根層級顯示的「繼承自」核取方塊。 NPR-28771:CQ-4259676的修補程式
* com.day.cq.personalization.impl.TeaserResourceEventHandler會進入無限循環，並導致發佈例項上的節點更新。 NPR-28561:CQ-4263096的修補程式
* 使用Brightedge憑證失敗，出現連線錯誤。 NPR-29167:CQ-4265872的修補程式
* 由於「資源」類別的匯入陳述式遺失，OfferproxyTandtProvider.java中的編譯問題：缺少import語句：import org.apache.sling.api.resource.Resource. NPR-28772

### 商務 {#commerce}

* 「排序」選項無法用於「商務」系列內的資產。 NPR-28755:CQ-4213622的修補程式

### Jetty {#jetty}

* 在6.3.3之上安裝CFP2後，每302次重新導向的error.log中會有空白例外。NPR-28606:CQ-4262844的支援埠

### UI - Foundation {#ui-foundation}

* 按一下標籤會移除全域滑鼠設定事件，而對話方塊會凍結在「可拖曳模式」中。 NPR-28641:CUI-7294的修補程式

### WCM - MSM {#wcm-msm}

* PushOnModify推出PageManager時，會從兩個作業階段中多次移動提交，造成競爭條件。 NPR-28880:CQ-4266191的修補程式

### 弱點{#vulnerability}

* CSRF保護架構無法與AEM基礎表單搭配使用。 NPR-28612:GRANITE-22231的修補程式

### 表單 {#forms-4}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

AEM Forms的主要亮點是：

* 啟用選項，可在「策略集」視圖頁上選擇每頁的項目。
* 新增所有瀏覽器的「共用佇列」功能。

### Forms add-on package {#forms-add-on-package-4}

#### 表單——工作流{#forms-workflow}

* 共用佇列回應工作會在HTML5工作區中開啟flash元素。 NPR-29161:CQ-4266498的修補程式
* 如果按鈕包含變母字元，則無法從工作區提交。 NPR-29014:CQ-4263172的修補程式

#### Forms - Document Security {#forms-document-security}

* 啟用選項，以在「原則集檢視」頁面上選取每頁的項目。 NPR-29243:CQ-4268567和CQ-4265132的修補程式

#### 表單——文檔服務{#forms-document-services-1}

* OSGi Forms Assembler無法處理Acrobat檔案。 NPR-29049:CQ-4254426的修補程式

#### HTML5 Forms {#html-forms-2}

* 在Designer中將XDP預覽為PDF時，會體驗到與HTML相同的XDP行為。 NPR-28602:CQ-4260239的修補程式

### Forms JEE安裝程式{#forms-jee-installer-3}

* Forms JEE安裝程式中沒有新的AEM Forms修正。

### 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}隨附的OSGI組合和內容封裝

AEM 6.3.3.4隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

AEM 6.3.3.4內容套件清單

[取得檔案](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### 累積修補程式套件6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3是自2018年9月AEM 6.3 Service Pack 3(6.3.0)全面推出以來，包含數項內部和客戶修正的重要更新。

AEM Cumulative Fix Pack 6.3.3.3取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.16版。
* 原則設定清單分頁變更，以限制每頁50個記錄。
* 新增代表：在發佈例項上，快取至AEM Communities User Sync Listener的可忽略節點。
* 已新增清單和卡片檢視按鈕的標籤。
* 執行任何搜尋時，包含逗號的逸出字元。
* 已啟用內容原則的合成資源支援。

#### 資產 {#assets-5}

* 無法下載。jp2、.max、.oft、.msg類型的多個檔案。 NPR-28002:CQ-4210856的修補程式
* ImageServer發佈設定不會複製至混合傳送。 NPR-28329:CQ-4253030的修補程式

#### 社群 {#communities-4}

* 在「發佈」上為「AEM Communities啟用元件」啟用鍵盤導覽。 NPR-27739:CQ-4253856的修補程式
* 啟用鍵盤導覽以觸發內容播放。 NPR-27738:CQ-4254026的修補程式
* 已新增清單和卡片檢視按鈕的標籤。 NPR-27736:CQ-4254027的修補程式
* （支援）新增代表：在發佈例項上，快取至AEM Communities User Sync Listener的可忽略節點。 NPR-27841:CQ-4247234的修補程式
* 在UI層級的搜尋方塊中，特殊字元會加上轉義字元(\)的前置詞。 NPR-27839:CQ-4259757的修補程式
* 搜尋字元(, +,?)時發生錯誤 快速搜尋。 NPR-28212:CQ-4260969的修補程式
* 無法使用API刪除使用者產生的內容中的注釋。 NPR-28075:CQ-4260534的修補程式
* 張貼新留言時，張貼至下一頁的留言會以黃色反白顯示。 NPR-28148:CQ-4259681的修補程式
* 無法開啟在Outlook發送和收件箱資料夾中包含附件的郵件。 NPR-28559:CQ-4217072的修補程式

#### 網站 {#sites-5}

* 在AEM 6.3中執行「清除版本」會在記錄檔中持續重複警告。 NPR-27750;CQ-4206870的修補程式
* Rich Text Editor全螢幕模式不支援樣式外掛程式。 NPR-27622:CQ-4258674的修補程式
* 將內容影格載入editor.js NPR-27768後，清單&#39;loaderCompories&#39;不會被清除：CQ-4205337的修補程式
* 在未設定父元件的情況下，無法在嵌套的parsys上設定模板策略。 NPR-27987:CQ-4246095的修補程式
* 元件瀏覽器無法淨化使用者輸入，因此可能會擲回javascript錯誤。 NPR-27986:CQ-4247590的修補程式
* 當使用者嘗試編輯內容片段時，頁面會顯示空白。 NPR-27669
* 當使用者按一下註解時，註解反白顯示就會消失。 BPR-27196:CQ-4254423的修補程式

#### 整合{#integration-1}

* ResourceResolver不解析Target元件的多個域。 NPR-28265:CQ-107847的修補程式
* LiveCopy繼承取消無法在目標容器上正常運作，因為不會顯示任何動作。 NPR-28129:CQ-4259813的修補程式

#### 複寫 {#replication-1}

* DispatcherFlushRules在6.3.3.1 NPR-28150中中斷複製：CQ-4261401的修補程式

#### 促銷活動——定位{#campaign-targeting-1}

* TargetedContentManager中的NullPointerException。 CQ-4263485的修補程式

#### Social - SCORM {#social-scorm}

* 移除播放器中可分享內容物件參考模型(SCORM)雲端的參考。 CQ-4260779的修補程式

#### DAM —— 常規{#dam-general}

* 透過連結共用電子郵件下載會傳回空白／損毀的zip。 CQ-4259686的修補程式

#### MAC - Test&amp;Target整合{#mac-test-target-integration}

* 除了「預設對象」以外，對象無法使用「設定目標元件」選項。 CQ-4261370的修補程式

#### 轉換 {#translation-1}

* 將MS Translator升級至API v3.0後，在AEM 6.3中啟用MS Translator服務支援。NPR-28365:CQ-4259096的修補程式

### 表單 {#forms-5}

### Forms add-on package {#forms-add-on-package-5}

#### 表單——工作流{#forms-workflow-1}

* 無法在HTML5工作區上轉換PDF表格。 NPR-28059:CQ-4260373的修補程式

#### 表單——文檔服務{#forms-document-services-2}

* 在管理控制台的「原則集」檢視中，看不到前1000個以外的任何原則集。 NPR-28060、NPR-26047:CQ-4249865的修補程式
* 以java.lang.IllegalArgumentException訊息：No enum常數com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE引發例外，使短暫的程式無法完成。 NPR-28652

#### 表單——最適化表單{#forms-adaptive-forms}

* 在勾選核取方塊項目時，下拉式清單中的新增／移除項目不會更新。 NPR-28224:CQ-4252834的修補程式

### Forms - JEE安裝程式{#forms-jee-installer-4}

* Forms JEE安裝程式中沒有新的AEM Forms修正。

### 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}隨附的OSGI組合和內容封裝

AEM 6.3.3.3隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6333_bundle_list.txt)

AEM 6.3.3.3內容套件清單

[取得檔案](assets/do-not-localize/content_package_list_6333.txt)

### 累積修補程式套件6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2是重要的更新，自2018年9月AEM 6.3 Service Pack 3(6.3.3.0)全面推出以來，已包含數項內部和客戶修正。

AEM Cumulative Fix Pack 6.3.3.2取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱AEM 6.3 Service Pack 3版本注意事項。

AEM Cumulative Fix Pack的主要亮點為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.15版。
* 新增對「規則」標籤的支援，以及對「資產資料夾」中「資料夾中繼資料結構」的強制執行。
* 已啟用分頁支援，可在發佈時將清單頁面分組。
* 啟用通知ureaddCount，以配置任何數字。 預設值設為20。
* 外部連結檢查器中的修正。

#### 資產 {#assets-6}

* 動態下拉式清單不支援階層式下拉式清單。 NPR-27044;CQ-4252564的修補程式
* 改進查詢以使用ExpiryNotification功能。 NPR-26999:CQ-4251188的修補程式
* 規則從中繼資料結構移轉至資料夾中繼資料結構。 NPR-27771:CQ-4257737、CQ-4257735、CQ-4259822的支援
* 資產參考調整無法更新屬於Sling ResourceCollections一部分之資產的參考。 NPR-26759:CQ-4252605的修補程式
* 透過連結共用電子郵件下載會傳回空白／損毀的zip檔案。 NPR-27997:CQ-4259686的修補程式
* 混合視訊編碼尚未完成，而且未建立縮圖。 NPR-27122:CQ-4255080的修補程式

#### 網站 {#sites-6}

* 暫停父頁面會移除cq :來自遺失頁面的LiveRelationship混合類型。 NPR-26996:CQ-4254113的修補程式
* （外部連結檢查器）內部連結在個別頁面上顯示為已中斷，但外部連結無法使用相同的連結。 NPR-27481:CQ-4257780的修補程式
* 在編輯其他頁面屬性時，雲端服務設定繼承正在中斷。 NPR-27311:CQ-4256785的修補程式
* 使用核心元件表單和基礎表單同時使用核心元件表單時的Null指針異常。 NPR-27333:CQ-4249176的修補程式
* Rich Text Editor會移除空的alt標籤。 NPR-26938:CQ-4253267的修補程式
* （傳統UI）效能問題   選擇變更   偵聽器，以備多次下拉。 NPR-27115:CQ-4237215的修補程式
* 當富格文本編輯器與多個欄位組合時，Uncated TypeError:fieldAPI.getName不是發生foundation.js錯誤時的函式。 NPR-27146:CQ-4253155、CQ-4259967的修補程式
* 即使在Safari瀏覽器中按一下選項按鈕，焦點／游標仍會保留在Rich Text Editor中。 NPR-27144:CQ-4249635的修補程式
* 當使用者嘗試編輯內容片段時，頁面會顯示為空白。 NPR-27669
* 無法建立體驗片段的版本。 NPR-27689:CQ-4259009的修補程式

#### 整合{#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever會在整棵樹上走動，以收集可用的品牌。 NPR-27060:CQ-4255790的修補程式
* The   cq:不會針對目標元件考慮動作。 NPR-27616:CQ-4257497的修補程式

#### Sling {#sling}

* 當與名稱相同的類一起使用資料漏洞時，將生成不可編譯的代碼。 NPR-27282:Sling-7581的修補程式

#### 商務 {#commerce-1}

* 更新至Apache Felix Http Jetty 4.0.6。NPR-26472:Granite-22916的修補程式

#### DAM - DM客戶端{#dam-dm-client}

* 在動態媒體元件中指定中斷點後，不會顯示影像。 CQ-4256168的修補程式

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet與相關視訊無法正確同步。 CQ-4251650的修補程式
* 在混合媒體集的檢視器預設集編輯器中，視訊無法播放。 CQ-4251442的修補程式

#### DAM —— 常規{#dam-general-1}

* 套用SP3修補程式後，內容片段模型的連結遺失。 CQ-4259029的修補程式

#### DAM - UI {#dam-ui}

* 安裝SP3後，資料夾中繼資料結構UI會中斷。 CQ-4257737的修補程式

#### 社群 {#communities-5}

* 新增發佈時群組清單的編頁支援。 NPR-26953:CQ-4246525的修補程式
* 未讀計數通知無法設定超過21。 NPR-27496:CQ-4252829的修補程式
* 使用者訂閱限制為1000。 NPR-27615:CQ-4254689的修補程式
* 在論壇中上傳影像以外的附件（例如。pdf）時發生錯誤。 NPR-27375:CQ-4257753的修補程式
* 回覆的連結無法在列按一下時運作。 NPR-24556:CQ-4256138的修補程式
* 刪除UGC時，不會刪除與UGC的關係。 NPR-27631:CQ-4258706的修補程式
* 如果社區已與資料庫儲存資源提供程式(DSRP)一起設定，則無法按關鍵字搜索中的地址值進行搜索。 NPR-27652:CQ-4253261的修補程式
* 刪除確認後，按一下影像上的垃圾桶圖示會永久移除附件。 NPR-27340:CQ-4255150的修補程式
* 論壇貼文和回覆會新增至第二頁上方，當重新整理後，貼文會移至第一頁上方的正確位置。 NPR-27341:CQ-4247338的修補程式
* 啟用Scorm資源完成狀態標籤在UI中顯示為空。 NPR-27152:CQ-4249994的修補程式
* 在啟用「允許特權」時，特權成員只能為社區成員的用戶進行合成。 NPR-27901:CQ-4251235的修補程式

#### 維護{#sustenance}

* 應將包管理器活動日誌提取到單獨的日誌檔案中。 NPR-27323:Granite-14866的修補程式

#### 轉換 {#translation-2}

* 翻譯預覽無法與we.retail範例內容搭配使用。 NPR-27170:CQ-4241179的修補程式

* 主動式平台。login修正。 NPR-26961
* 在AEM WAR with Tomcat中，頁面屬性上的「儲存並關閉」無法返回正確的頁面。 NPR-27567:Granite-23671的修補程式

* 儲存後，輸入的文字會透過sourceEdit功能遺失。 CQ-4259273的修補程式

### 表單 {#forms-6}

### Forms add-on package {#forms-add-on-package-6}

#### Forms - Document Security {#forms-document-security-1}

* JEE用戶端SDK的並行問題。 NPR-27572:CQ-4247156的修補程式

#### 表單——文檔服務{#forms-document-services-3}

* 在WebSphere上，基於SOAP建立表單資料模型失敗。 NPR-27692:CQ-4253702的修補程式

#### 表單——最適化表單{#forms-adaptive-forms-1}

* AEM表單的XML插入弱點。 NPR-27863:CQ-4257315的修補程式
* 一旦在網站頁面中設定錯誤的表單，且選取「表單涵蓋頁面的整個寬度」核取方塊，AEM Forms Container元件就會不可見。 NPR-25972:CQ-4239287、CQ-4249133的修補程式

### Forms JEE安裝程式{#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* 在WebSphere上，基於SOAP建立表單資料模型失敗。 NPR-27692:CQ-4253702的修補程式

#### 包含{#osgi-bundles-and-content-packages-included}的OSGI組合和內容封裝

AEM 6.3.3.2隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/63332bundle_list.txt)

AEM 6.3.3.2內容套件清單

[取得檔案](assets/do-not-localize/6332content_package.txt)

### 累積修補程式套件6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1是重要的更新，包含自2018年9月AEM 6.3 Service Pack 3(6.3.3.0)全面上市以來的數項內部和客戶修正。

AEM Cumulative Fix Pack 6.3.3.1取決於AEM 6.3 Service Pack 3。 因此，在安裝AEM 6.3 Service Pack 3後，您必須安裝AEM Cumulative Fix Pack 6.3.3.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 3發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.14版。
* 謂語和搜尋的效能改進。
* 修正FormData處理預設值的問題。
* 將FormBuilder升級至最新的Handlebar版本。
* 已為RTE的編輯配置添加在對話框模式下的配置Servlet。
* 新增對複合欄位的支援。
* 富格文本編輯器的啟用／禁用工具欄項，其中包含編輯對話框的內容策略。

#### 資產 {#assets-7}

* 啟用IDS去耦後，DAM更新資產工作流程將不再連結參照。 NPR-26135:CQ-4250933的修補程式
* 不會開啟解壓縮由未存檔程式步驟建立的存檔，其名稱中包含%的資料夾。 NPR-26275:CQ-4251482的修補程式
* 單引號字元可防止中繼資料更新。 NPR-26808:CQ-4254305的修補程式
* (Omnisearch)在系列中搜尋時的效能問題。 NPR-26714:CQ-4253408的修補程式
* 對於在文本中包含&quot;OR&quot;字母的全文搜索，使用GQLConverter會被錯誤處理。 NPR-26564:CQ-4247362的修補程式
* 從多租用戶預先共用資產連結，以產生無效的URL。 NPR-26482:CQ-4253540的修補程式
* 在Dynamic Media Cloud設定UI中停用「公司根資料夾路徑」。 NPR-26361:CQ-4249505的修補程式
* 擷取。mos RAW檔案的時間會延長。 NPR-26296:CQ-4250661的修補程式
* 「資產連結共用」不允許新增超過一個具有數值使用者ID的內部使用者。 NPR-26206:CQ-4251466的修補程式
* 使用deflate64演算法壓縮的Zip檔案損毀。 NPR-26793:CQ-4253995的修補程式
* 縮圖產生程式無法正確處理複雜的PDF檔案，造成縮圖，而影像部分遺失。 NPR-26057:CQ-4250944的修補程式
* 產生縮圖時的堆積記憶體使用率問題。 NPR-25545:CQ-4246960的修補程式
* 在資產上建立大量關係會導致錯誤。 NPR-26309:CQ-4250708的修補程式
* 「刪除轉譯」選項無法運作，並會擲回「無需刪除」錯誤。 NPR-26007:CQ-4213414的修補程式
* 無法刪除多值欄位的預設值。 NPR-25116:CQ-4247856的修補程式
* (DM Hybrid)AEM 6.3.2與Dynamic Media的目錄複製中斷。 NPR-26406:CQ-4251306的修補程式

#### 網站 {#sites-7}

* 主動式網站支援修正。 NPR-26963
* 當「標題」和「名稱」的大小寫類型有差異時，會建立兩次標籤。 NPR-26877:CQ-4254134的修補程式
* 編輯對話框中的富格文本編輯器功能不受策略控制。 NPR-27059、NPR-26750:CQ-4241130的修補程式
* 用戶端內容segment.js快取與非快取問題。 NPR-26622:CQ-4253486的修補程式
* 針對傳統規則的區段規則(/etc/segmentation)啟動會導致發佈關閉。 NPR-26601:CQ-4253588的修補程式
* 新增「特殊字元」會將「豐富型文字編輯器」對話方塊捲動至頂端。 NPR-26435:CQ-4249869的修補程式
* (Touch UI)當從全螢幕切換為浮動對話方塊時，工具列就無法與多個Rich Text Editor搭配使用。 NPR-25652:CQ-4206008的修補程式
* 促銷多頁啟動會為每個頁面建立多個版本。 NPR-26810:CQ-4254663的修補程式
* 標籤移動操作不會被結構化內容片段模型標籤欄位所反映。 NPR-26801:CQ-4251805的修補程式
* (Touch UI)從頁面編輯器取消發佈子頁面在重新命名Blueprint中的頁面後無法運作。 NPR-26774:CQ-4254175的修補程式
* 未發佈的頁面無法與參考搭配使用。 NPR-26749:CQ-4254372的修補程式
* 將變數建立為即時副本時，使用者必須重新整理頁面以反映。 NPR-26663:CQ-4254328的修補程式
* （傳統UI）回到頁面屬性時，縮圖影像不再使用繼承，並從網站管理員和側腳消失，影像會顯示為空白。 NPR-26562:CQ-4252346的修補程式
* 當建立頁面版本並觸發比較時，來自/content/versionshistory的節點會列在Blueprint的即時副本清單中。 NPR-26506:CQ-4243957的修補程式
* 「體驗片段管理員編輯器」中的URL不允許覆蓋。 NPR-26318:CQ-4252156的修補程式

#### 平台 {#platform}

* ReplicationEventListener中的會話洩漏與測試事件。 NPR-25937:CQ-4251090的修補程式
* 複製使用過期的OAuth Token，造成多個錯誤。 NPR-25894:GRANITE-22388的修補程式

#### 整合{#integration-3}

* TSDK內嵌於AEM，由於使用不相容的範本，升級至Handlebar 4會中斷。 NPR-26699:CQ-4248974的修補程式
* 使用新資產發佈頁面會停用發佈例項中的子頁面，而不需通知。 NPR-24869:CQ-4247832的修補程式
* 複製使用過期的Token來驗證。 NPR-25984:Granite-22388的修補程式

#### 複寫 {#replication-2}

* Http傳輸可能會洩露開放會話。 Granite-17434的修補程式
* 多個複製代理同時訪問訪問令牌節點時日誌中的異常。 NPR-26964:GRANITE-23276、Granite-23155的修補程式

#### ContextHub {#contexthub}

* 檔案&#39;coral.js&#39;包含有弱點的程式庫&#39;handlebars.js&#39;版本。 CQ-4255377的修補程式

#### DAM - DM客戶端{#dam-dm-client-1}

* 刪除影像資產的復本會使原始影像資產無法使用。 CQ-4251648的修補程式
* 從S7伺服器備援下載額外影像內容。 CQ-4248770的修補程式

#### 花崗岩{#granite}

* AEM OAuth提供者不執行不區分大小寫的搜尋。 NPR-26133:GRANITE-22650的修補程式
* Package Validator不會驗證CFP/SP中包含的封裝。 NPR-26775:Granite-22825的修補程式

#### 社群 {#communities-6}

* 搜尋結果的分隔字元問題。 NPR-27051:CQ-4248939的修補程式
* 在Adobe儲存資源提供者中，將下拉式清單值從Dallas變更為Virginia。 NPR-26936:CQ-4254434的修補程式
* 在SocialTagManager中啟用本地化標題搜尋的支援。 NPR-26932:CQ-4250276的修補程式
* 建立論壇貼文時，附件影像不會顯示縮圖。 NPR-26380:CQ-4253105的修補程式
* 從Word外掛程式貼上無法載入多個影像。 NPR-26728:CQ-4253638的修補程式
* 無法篩選協調頁面中的內容。 NPR-26697:CQ-4213766的修補程式
* （安全漏洞）由於JWT配置錯誤而接管帳戶。 NPR-26440:CQ-4253314的修補程式
* 從Adobe儲存資源提供者擷取資料的速度緩慢。 NPR-26237:NPR-24152的修補程式
* 私人訊息合成頁面的行為不穩定。 NPR-26120:CQ-4250923的修補程式
* 「將所有已讀取標籤」通知只會將前10個顯示為未讀取，而不需重新整理頁面。 NPR-27036:CQ-4254058的修補程式
* 社群注釋區段分頁點按和頁面載入行為。 NPR-27030:CQ-4251228的修補程式
* （論壇搜尋）「上一步」按鈕會跳過頁面，並傳回至forum.html。 NPR-26949:CQ-4254804的修補程式
* 未讀取通知的數量不會超過21個。 NPR-26947:CQ-4251251的修補程式
* （SearchScheduledPosts工作）在ConfigMgr中新增啟用／停用切換。 NPR-26924:CQ-4250463的修補程式
* 在「工作總攬」頁面上捲動時，Tomcat上下文(/aempublish)路徑會掉落。 NPR-26919:CQ-4254345的修補程式
* 建立組和成員時的NullPointerException。 NPR-26778:CQ-4248095的修補程式
* 協調者未定義和未加入功能的內容無法與MySQL單一責任原則(SRP)搭配使用。 NPR-26767:CQ-4251520的修補程式
* 某些字元的搜尋功能問題。 NPR-26726:CQ-4247744的修補程式
* 啟用協調UI與啟用資源的深層連結。 NPR-26705:CQ-4251381的修補程式
* 論壇元件上的搜索問題。 NPR-26577:CQ-4251303的修補程式
* 在社群訊息中同時搜尋名字和姓氏並不會傳回預期結果。 NPR-26377:CQ-4253150的修補程式
* 移除回覆時，分頁不會更新。 NPR-26327
* 刪除貼文會運作，但在主控台上會顯示錯誤，而貼文仍會顯示在UI上。 NPR-26292:CQ-4252803的修補程式
* 分頁不會動態更新，回覆清單也會持續增加。 NPR-26145:CQ-4251586的修補程式
* 群組設定不會載入包含50K~100K使用者的群組。 NPR-25642:CQ-4238426的修補程式
* 目錄資源播放器無法獲取上下文路徑。 NPR-25640:CQ-4238426的修補程式
* （論壇搜尋）-具有大量貼文之主題的已編頁連結無法用於通知。 CQ-4254202的修補程式
* 協調控制台只會顯示5個Firefox項目。 CQ-4254128的修補程式
* 建立網站時，不會顯示群組。 NPR-27148:CQ-4251788的修補程式
* 將組和成員添加到角色設定並允許部落格函式中的特權成員時出現空指針異常。 NPR-21732、NPR-27176:CQ-4255909的修補程式
* 編輯站點並在角色設定中添加成員會引發空指針異常。 NPR-27132:CQ-4255909的修補程式

#### 使用者介面{#user-interface}

* 主動式平台登入修正。 NPR-26961
* （多欄位）允許複合項目具有自訂名稱。 NPR-26493:Granite-20568的修補程式
* 貼上頁面後，欄檢視在重新整理後才會更新。 NPR-26030:CQ-4236346的修補程式
* 主動granite.ui.commons修正。 NPR-26960
* 主動granite.ui.co內容修正。 NPR-26959
* 主動式CQ/體驗記錄修正。 NPR-26943
* 主動式Foundation UI後台。 NPR-26942
* (IE11)在輸入負值時，數字欄位中會顯示「NaN」。 NPR-26701:CQ-100826的修補程式
* (珊瑚色。 多欄位)巢狀多欄位使用錯誤的範本來建立項目。 NPR-25649:CUI-6743的修補程式
* 更新花崗岩coralui2和coralui3 clientlibs，從建置移除Handlebar。 NPR-25606:Granite-22116的修補程式

### 表單 {#forms-7}

### Forms add-on package {#forms-add-on-package-7}

#### Forms - Document Security {#forms-document-security-2}

* 主密鑰變換在活動密鑰的伺服器日誌中出現異常。 NPR-26748:CQ-4253705的修補程式
* 無法建立或修改Document Security的浮水印設定。 NPR-26267、NPR-26129:CQ-4250234的修補程式

#### 表單——文檔服務{#forms-document-services-4}

* PDF/A驗證無法以「驗證PDF/A」顯示有效。NPR-25934:CQ-4248558的修補程式

#### 表單——互動式通訊{#forms-interactive-communication}

* 當編輯、儲存可編輯的模組，然後開啟／關閉PDF預覽時，「字母」的PDF和HTML預覽會在同一視窗中顯示並運作。 NPR-26770:CQ-4253217的修補程式

#### 表單——工作流{#forms-workflow-2}

* 工作區間歇性掛起，並反複顯示起點。 NPR-26461:CQ-4253439的修補程式
* 在任務名稱中使用大括弧時，日誌中會拋出ESAPI異常。 CQ-4256627的修補程式
* 開啟非預填充的自適應表單／表單集關聯起始點時拋出空指針異常。 CQ-4256124的修補程式
* 無法使用全域設定傳送電子郵件。 NPR-26163:CQ-111110的修補程式
* 應用axis.jar檔案後無法開啟工作區。 NPR-26131:CQ-4251126的修補程式
* 刷新按鈕無法將伺服器的最新資料同步到Adaptive表單。 CQ-4255670的修補程式
* 從管理員UI設定搜尋範本，然後使用相同範本在AEM Forms工作區中搜尋工作，會引發例外。 CQ-4255649的修補程式
* HTML工作區中不會顯示在名稱中帶有括弧符號之應用程式下方的追蹤程式詳細資料。 CQ-4242101的修補程式
* 在HTML工作區的偏好設定畫面中儲存變更會引發例外。 CQ-4241485的修補程式
* 在最新的JEE設定中，批量核准會中斷。 CQ-4241486的修補程式
* 在最新6.4 JEE伺服器上，任務／起始點的草稿失敗。 CQ-4241484的修補程式
* 設定Date()。getTime()。toString參數以初始化作業，而非Date.toString()。 CQ-4241483的修補程式
* 在開啟/lc/ws時，HTML參數中會出現有弱點的字元例外。 CQ-4241481的修補程式

#### 弱點{#vulnerability-1}

* Forms Manager的「附註」標籤中儲存的跨網站指令碼(XSS)弱點。 NPR-27157:CQ-4255556的修補程式

### Forms JEE安裝程式{#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Enterprise Security API的程式碼審核。 CQ-4255638的修補程式
* 在WAS9中無法將esapi.properties載入為類載入器資源。 CQ-4255631的修補程式
* 按一下「網域設定期間新增驗證」會引發錯誤。 CQ-4255634的修補程式
* Forms JEE支援PKCS#11相互驗證。 NPR-21372
* 已修正核心靜態程式碼分析中報告的問題。 CQ-104446的修補程式
* 執行LCM時，部署adobe.livecycle.weblogic.ear和adobe.livecycle.websphere.ear失敗。 CQ-4255629、CQ-4255630的修補程式
* 應用程式管理中的錯誤消息無效。 NPR-23289:CQ-4233163、CQ-4255636的修補程式
* 在域配置期間按一下添加驗證會導致錯誤。 CQ-4255634的修補程式

#### 表單- JEE連接器{#forms-jee-connector}

* 修正連接器靜態程式碼分析中報告的問題。 NPR-22260

#### PDFG服務{#pdfg-service-1}

* 從LiveCycle升級至AEM 6.2表單後，記錄檔中出現org.jgroups.Message錯誤。 NPR-26795:CQ-4220415的修補程式
* AEM表格——轉換樣式時發生錯誤。 CQ-4251969的修補程式
* 修正PDFG靜態程式碼分析報告中所報告的問題。 NPR-23251:CQ-4213930的修補程式

#### 6.3.3.1 {#osgi-bundles-and-content-packages-included-in-3}隨附的OSGI組合和內容封裝

AEM 6.3.3.1隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/63sp3cfp1bundlelist.txt)

AEM 6.3.3.1內容套件清單

### 累積修補程式套件6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2是自2018年4月AEM 6.3 Service Pack 2(6.3.2.0)全面推出以來，包含數項內部和客戶修正的重要更新。

AEM Cumulative Fix Pack 6.3.2.2取決於AEM 6.3 Service Pack 2。 因此，在安裝AEM 6.3 Service Pack 2後，您必須安裝AEM Cumulative Fix Pack 6.3.2.x套件。 如需安裝指示，請參閱[AEM 6.3 Service Pack 2發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html)。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.11版。
* 在品牌入口網站上啟用子資產和多頁資產檢視器。
* 將欄位類型的長度更改為255，以支援不同附件類型的所有可能的MIME類型。
* 當影像違反上傳准則時，伺服器會傳送已設定的錯誤訊息。
* 已在Day CQ Mail Service中新增STARTTLS支援。
* 更新至最新版cq-wcm-content和com.adobe.cq.launches.it.serverside。
* 將com.adobe.granite.ui.coralui3-rte更新至最新發行的版本。
* 如果expressionResolver為null，則確保渲染條件返回正常結果。
* Coral.ColumnView:新增對shift+click的支援。

### 資產 {#assets-8}

* 「資產資料夾已關閉使用者群組」(CUG)欄位不會傳回「每個人」群組。 NPR-23163:CQ-4239377的修補程式
* 搜尋智慧型系列儲存的搜尋並不會傳回所有結果。 NPR-23243:CQ-4240355的修補程式
* (ExpiryNotificationJobImpl)現有查詢的最佳化。 NPR-23330:CQ-4205249的修補程式
* （中繼資料設定檔）在建立時設定的標準標籤值在儲存後無法使用。 NPR-23370:CQ-4235458的修補程式
* (Touch UI)由於JS錯誤，無法移動多個資產。 NPR-23395:CQ-4241279的修補程式
* 下載大小與顯示的資訊不相符，會造成使用者混淆。 NPR- 23418:CQ-4242774的修補程式
* 提取的檔案副檔名LSR和SKETCH的mimetype不正確，導致檔案下載無效。 NPR-23644:CQ-4243260的修補程式
* (Firefox/Chrome)無法在「資產共用」頁面中下載資產。 NPR-23963:CQ-4244391的修補程式
* 資產管理員搜尋Facet在預覽後會在搜尋面板中消失。 NPR-23964:CQ-4244410的修補程式
* 取消發佈搜尋表單會完全移除預設的搜尋表單。 NPR-23291:CQ-4241382的修補程式
* (Brand Portal)複製時，應篩選掉目錄謂語中的搜尋。 NPR-23292:CQ-4241385的修補程式
* 無法發佈至品牌入口網站UI動作。 NPR-23293:CQ-4241161的修補程式
* 「發佈／取消發佈至品牌入口網站」按鈕不適用於內容片段。 NPR-23318:CQ-4245086的修補程式
* （品牌入口網站）啟用在發佈資產時建立子資產。 NPR-23331:CQ-4242018的修補程式
* 動態媒體請求不使用proxy/HTTP公用用戶端。 NPR-10727:CQ-45695、CQ-88800的修補程式
* 無法在Dynamic Media S7(DMS7)中註解單一轉譯MP4視訊資產。 NPR-22046:CQ-4215912的修補程式
* 在Ptiff產生程式中，EmbedXMP資料一律設為「作用中」。 NPR-22903:CQ-4234498的修補程式
* 「動態轉譯」顯示／選取問題，影像預設集計數偏大。 NPR-23151:CQ-4217511的修補程式
* 動態媒體編碼視訊——修改／重新上傳啟動程式的問題。 NPR-23237:CQ-4240260的修補程式
* Dynamic Media S7中HTTP轉發程式的Proxy處理修正。 NPR-24001:CQ-244140的修補程式

### 網站 {#sites-8}

* 查詢產生器的差異導致6.2和6.3之間的xPath轉換不同。NPR-23245:CQ-4240396的修補程式
* 頁面屬性中的縮表徵圖簽無法用於延伸對話方塊。 NPR-22844:CQ-4241474的修補程式
* Parsys會中斷模擬器裝置影格寬度，並裁切加入其中的任何元件。 NPR-22926:CQ-4238224的修補程式
* 當執行多次啟動時，啟動會在Author中提升，但是由於缺乏複製權限，這些變更不會複製到Publish伺服器上。 NPR-22934:CQ-4234746的修補程式
* 由用戶在第一會話中鎖定的頁面可由另一個用戶在另一個會話中修改。 NPR-23057;CQ-4199017的修補程式
* 修正清單檢視中可重新排序的選項。 NPR-23065:CQ-4239321的修補程式
* （頁面編輯器）再次開啟對話方塊時，影像元件上的影像會消失。 NPR-23156:CQ-4239978的修補程式
* 範本編輯器只顯示20個範本／檔案夾，當捲動至頁面底部時不會載入其他範本／檔案夾。 NPR-23185:CQ-4238483的修補程式
* (Classic UI)移動或重新命名頁面時會產生錯誤。 NPR-23213:CQ-4240971的修補程式
* 無法編輯／建立ContextHub區段。 NPR-23218:CQ-4226948的修補程式
* （富格文本編輯器）-替換操作會更改單字的格式。 NPR-23271:CQ-4239677的修補程式
* XF變數的Blueprint標籤中遺失轉出按鈕。 NPR-23320:CQ-4240404的修補程式
* 由於不再使用，傳統UI無法編輯CUG。 NPR-24122:4241823的修補程式
* 主動修正，以防止不想要的內容促銷活動。 NPR-24387:4244993的修補程式
* 約一次 80個片段會新增至「資產」的資料夾中，這是從時間軸主控台觸發工作流程時遇到的錯誤。 NPR-23393;CQ-4211216的修補程式
* 無法從內容搜尋器將影像拖放至「豐富型文字編輯器」對話方塊。 NPR-23403:CQ-4242094的修補程式
* 將元件從AEM 6.0移轉至AEM 6.2時，發生「無效的遞回選擇器值」錯誤。NPR-23532:CQ-4241258的修補程式
* (Rich Text Editor)工具提示會顯示外掛程式的變數名稱，而非可讀的外掛程式名稱。 NPR-23550:CQ-4243269的修補程式
* 無法在行動／平板電腦版本中儲存對話方塊及必要的選擇下拉式清單。 NPR-23904:CQ-4243096的修補程式
* 在安裝6.3.2.1後的所有頁面上都會顯示樣式系統選項。 NPR-23972:CQ-4244394的修補程式
* 由於不再使用，傳統UI無法編輯CUG。 NPR-24122:4241823的修補程式
* 主動修正，以防止不想要的內容促銷活動。 NPR-24387:4244993的修補程式
* 資產移動時不會更新資產參考。 NPR-23208:CQ-4239879的修補程式

### 平台 {#platform-1}

* 如果在搜尋Facet中使用標籤述詞，則Smart Collection在儲存後不會顯示結果。 NPR-23401:Granite-21278的修補程式
* 從clientlib修補jQuery 1.12.4以包含安全性修正。 NPR-24128:Granite-20058的修補程式
* 除非重新啟動捆綁包，否則不會更新國際化翻譯。 NPR-23193:Sling-7190的修補程式
* ReplicationEventListener中未關閉的資源解析器。 NPR-23240:CQ-4241350的修補程式
* 在「Day CQ Mail Service」中支援STARTTLS。 NPR-23941:CQ-4240397的修補程式
* JCR抱怨標籤名稱應根據「標籤標題」自動填入。 NPR-24173:CQ-4199411的修補程式

### 整合{#integration-4}

* (Target)當將API類型使用為XML時，不會啟用促銷活動。 NPR-23199:CQ-4240936的修補程式****
* 配置引用複製失敗，中間資料夾結構。 NPR-23485:CQ-4242751的修補程式

### 弱點{#vulnerability-2}

* Salesforce整合容易受到伺服器端偽造要求(SSRF)的影響。 NPR-24289:CQ-424527的修補程式
* 管理UI專案連結中的跨網站指令碼(XSS)。 NPR-23272:CQ-4241795的修補程式

### WCM —— 基礎元件{#wcm-foundation-components}

* Foundation表易受儲存的跨站點指令碼攻擊。 NPR-23214:CQ-4240760的修補程式

### 轉換 {#translation-3}

* 建立語言副本時不會刪除即時副本屬性。 NPR-23123:CQ-4230641的修補程式

### 使用者介面{#user-interface-1}

* DatePicker不支援手動設定由隱藏欄位設定的外部類型提示。 變更文字提示會產生轉換錯誤。 NPR-23371:Granite-21194的修補程式
* Coral.ColumnView:新增shift+click支援。 NPR-23404:Granite-13338的修補程式
* 選取空值項目時，選取「RT不會驗證」。 NPR-23405:Granite-21283的修補程式
* (OMEGA)僅以英文報告「功能」。 NPR-23990:Granite-21231的修補程式
* Coral.Autocomplete API的修正。 NPR- 23516

### 花崗岩{#granite-1}

* Apache Http用戶端追蹤連線和高堆積使用率會造成AEM伺服器當機。 NPR-23906:Granite-21056的修補程式

### 商務 {#commerce-2}

* 促銷活動json輸出不包含servlet上下文根。 NPR-23733:CQ-4243827的修補程式

### 社群 {#communities-7}

* 在社群上搜索很少用詞。 NPR-23256:CQ-4240717的修補程式
* 無法為社區管理員角色問題分配組。 NPR-23317:CQ-4241233的修補程式：CQ-4221399
* 使用類似資產名稱建立資源時的問題。 NPR-23319:CQ-4240700的修補程式
* (ContextPath)在社群群組成員清單中搜尋群組成員時，中斷Jetty組態的訊息功能會中斷，並出現錯誤。 NPR-23336:CQ-4241519、CQ-4242080的修補程式
* 上傳影像至社群論壇不會顯示在Adobe儲存資源提供者(ASRP)中。 NPR-23397:CQ-4242497的修補程式
* 刪除的構想會在「活動」中顯示為作用中的連結。 NPR-23406
* imsmanifest.xml無法載入使用內容根目錄執行的AEM。 NPR-23483:CQ-4242193的修補程式
* 舊版Handlebar中的安全性弱點。 NPR-23518:CQ-4243055的修補程式
* 通道服務無法正常工作。 NPR-23543:CQ-4242217的修補程式
* 透過Dispatcher和sling dynamic include存取社群元件時的問題已啟用。 NPR-23586:CQ-4242360、CQ-4241522的修補程式
* 當搜尋透過搜尋產生許多結果的搜尋詞，然後輸入新搜尋詞時，不會重設分頁。 NPR-23739:CQ-4222593的修補程式
* 在論壇元件上執行搜索時出現的問題。 NPR-23838:CQ-4243770的修補程式
* （社群協調標幟）標籤訊息的大量允許無法運作。 NPR-23845:CQ-4243962的修補程式
* 排序按鈕文字不會顯示預設的選取值   的子菜單。 NPR-23881:CQ-4243375的修補程式
* 由於群組的訊息失敗，網頁和郵件通知不會觸發。 NPR-23934:CQ-4242880的修補程式
* 使用DSRP配置時，不會顯示標籤用戶和原因的詳細資訊。 NPR-23973:CQ-4243205的修補程式
* 未標幟的使用者的標幟原因仍然可見/ NPR-23974:CQ-4243822的修補程式
* 將兩個同名檔案連接兩次至表單貼文會導致伺服器錯誤。 NPR-24166:CQ-4244367的修補程式
* 無法使用資料庫儲存資源開發人員(DSRP)儲存MIME類型超過15個字元的附件。 NPR-24174
* 當違反上傳准則的影像拖放至貼文文字時，會擲回伺服器錯誤，並向使用者顯示一般錯誤訊息。 NPR-24243
* 修正數個AEM Communities伺服器端問題。 NPR-23971:CQ-4243144、CQ-4242145、CQ-4243365、CQ-4244098的修補程式
* 修正數個Adobe Social問題。 NPR-24242:CQ-4245054、CQ-4245120、CQ-4245296的修補程式

### 行銷活動 {#campaign}

* 促銷活動json輸出不包含servlet上下文根。 NPR-23733:CQ-4243827的修補程式

### MSM {#msm}

* 在滾出頁面時，livecopy不會顯示繼承自主版的開／關時間屬性。 NPR-23873:CQ-4243431的修補程式
* LiveCopy操作不會忽略已刪除元件的子節點。 NPR-23058:CQ-4211662的修補程式

### 卸載{#offloading}

* 要求機制在處理後或定期清除員工實例中的資產。 NPR-23638:Granite-21337的修補程式

## 表單 {#forms-8}

### Forms add-on package {#forms-add-on-package-8}

#### 適用性表單 {#adaptive-forms-1}

* 將ReCaptchaConfigService移至內部套件。 CQ-4217459的修補程式
* 數值欄位不符合最小值。 NPR-23967:CQ-4244830的修補程式
* 在與AdobeSign整合的Adaptive Forms中支援多分享。 NPR-23383

#### 後端整合{#backend-integration}

* (FDM)(WebService)支援WSDL剖析器中的WSDL擴充架構。 NPR-23640,NPR:23236:4205821的修補程式
* 在Forms Add-on Client SDK中包含SDLInvokerParams。 NPR-23157

### Forms JEE安裝程式{#forms-jee-installer-7}

#### 流程管理{#process-management}

* 套用新的axis.jar檔案後，無法開啟工作區。 NPR-23316
* LiveCycle在PMAdmin上容易受到XSS的攻擊。 NPR-23267
* 升級至AEM 6.1 Forms後，HTML工作區在存取特定使用者的工作清單時會停止。 NPR-23943

#### 核心 {#core}

* Forms JEE支援PKCS#11相互驗證。 NPR-21372

#### PDFG服務{#pdfg-service-2}

* 同時處理TIFF檔案（大小約為50 KB）時，Paper capture服務會當機。 NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server輸出——註解的替代說明遺失。 NPR-22207
* 將PDF/UA支援新增至透過Designer和Output Service產生的XML表格。 NPR-23132

### 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}隨附的OSGI組合和內容封裝

AEM 6.3.2.2隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6_3_2_2_bundle-list.txt)

AEM 6.3.2.2內容套件清單

[取得檔案](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### 累積修補程式套件6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1是重要的更新，自2018年4月AEM 6.3 Service Pack 2(6.3.2.0)全面推出以來，已包含數項內部和客戶修正。

**AEM Cumulative Fix Pack**&#x200B;的主要亮部為：

* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.10版。
* 已改善Classic UI中Parsys元件的轉換。
* 已更新sling模型組合以包含字元集修正。
* 針對所有資產類型，將其非同步發佈至品牌入口網站。
* 將coralui-component-richtexteditor.git從0.1.15更新至0.1.16
* 下拉式元件的show/hide功能中的修正。
* 已啟用核心影像元件的影像翻轉功能。
* 更新的felix   http bundles以啟用作業屬性。

* 由於記憶體耗用問題，Sling Models已移除cache=true。

### 資產 {#assets-9}

* 在「資產檔案夾」設定中變更標題或縮圖圖片時，會覆寫檔案夾的原始群組和權限。 NPR-22171:CQ-4216080的修補程式
* UI會擲回錯誤「發佈至品牌入口網站失敗」，而工作會新增至複製佇列，資產會發佈至品牌入口網站。 NPR-22179:CQ-4205273的修補程式
* （觸控UI）欄檢視中資產的預設上傳位置。 NPR-22465:CQ-4237057的修補程式
* AEM嘗試將資產結構描述從/conf/global複製到/conf/ mytenant時，會引發StackOverflow錯誤。 NPR-22489:CQ-4235875的修補程式
* 嘗試解壓縮ZIP檔案失敗，因為檔案夾名稱結尾有尾隨空格。 NPR-22522:CQ-4238036的修補程式
* 使用資產標題欄排序無法用於搜尋結果。 NPR-22908:CQ-4239076的修補程式
* Youtube影片會以完整路徑來標籤，而非標籤名稱本身。 NPR-22976:CQ-4238669的修補程式
* 不會持續重新排序可重新排序資料夾下的資料夾。 NPR-23125:CQ-4231761的修補程式
* HTTP 504:嘗試使用共用連結共用系列時發生閘道逾時錯誤。 NPR-21928:CQ-4234507的修補程式
* 當有多個關鍵字與PDF資產相關聯時，PDF關鍵字中繼資料無法正確擷取和修改。 為瞭解決此問題，PDF資產的「主旨」欄位中繼資料屬性已移除。 不過，您可以編輯中繼資料結構，為「主旨」欄位新增多值文字欄位。 NPR-21972:4215741的修補程式****
* 如果在顯示2個快顯視窗之間變更了選取的資料夾，則會刪除錯誤的資產。 NPR-21980:CQ-4233675的修補程式
* (DAM)新增至收集精靈時，有多項跨網站指令碼(XSS)弱點。 NPR-22432:CQ-4327086的修補程式
* 在Safari的Assets中使用Digital Rights Management時，資產下載失敗。 使用者無法下載包含免責聲明和長檔案名稱的資產。 NPR-22747:CQ-4236460和CQ-4235274的修補程式
* 在將資產發佈至品牌入口網站時，將公開分享設為預設選項。 NPR-21931:CQ-4218816的修補程式

### 網站 {#sites-9}

* 「工作流」收件箱中的新項目顯示頁面路徑，而非頁面標題。 NPR-21634:CQ-4230672的修補程式
* 可編輯的結構元件會在編輯時遺失回應式格線所需的CSS類別名稱。 NPR-21741:CQ-4232374的修補程式
* (TouchUI)HTL元件的多個跨網站指令碼(XSS)弱點。 NPR-21899:CQ-4232511的修補程式
* 無法更改內容片段混合媒體映像資源類型。 NPR-21907:CQ-4233401的修補程式
* RTE Fullscreen For the Touch UI Dialog is Hiding the RTE plugins. NPR-22034:CQ-4235457的修補程式
* (Touch UI)Rich Text Editor會從&lt;a>標籤中移除除id以外的所有屬性。 NPR-22044:CQ-4234133的修補程式
* 由於長時間執行的查詢（超過6個），多個堆疊Parsys會使AEM變得呆滯。 NPR-22134:CQ-4233904的修補程式
* 無法更改名稱中包含冒號的節點的權限。 NPR-22136:CQ-4236221的修補程式
* (Classic UI)Rich text editor output html adds &#39;list-position-style:inside;&#39;，作為&lt;ul>標籤的內嵌樣式。 NPR-22145:CRTE-114的修補程式
* 當文字空白時，讓TreeNode回退至name屬性。 NPR-22146:CQ-4234724/CQ-4236300的修補程式
* RSS饋送問題，埠-1到AEM 6.3。NPR-22176:CQ-4233339的修補程式
* （傳統UI）貼上文字快速鍵(Ctrl+V)不適用於OOTB文字(Rich Text)元件。 NPR-22224:CQ-4236224的修補程式
* Tagfield的篩選無法如預期般在輸入文字時運作。 NPR-22236:CQ-4236655的修補程式
* （頁面編輯器）在影像地圖元件中貼上文字資料時，在影像地圖元件中貼上文字資料時，也會貼上文字元件。 NPR-22264:CQ-4236230的修補程式
* 「對話方塊檔案上傳」欄位必填，會導致對話方塊提交中發生問題。 NPR-22464:CQ-4222192的修補程式
* 如果移動的頁面或其反向連結無法啟動，則移動複製權限會啟動啟動工作流程的要求。 NPR-22467:CQ-4211765的修補程式
* 載入具有大（2000個以上）觀眾的頁面時，效能問題。 NPR-22478;CQ-4209567的修補程式
* ContextHub在初始化期間儲存會覆寫預設永續性層時的永續性問題。 NPR-22479:CQ-4218399的修補程式
* 如果未在第一個內容根目錄上勾選「包含子頁面」，則使用多個頁面啟動不會將子頁面發佈至發佈伺服器。 NPR-22482:CQ-4237818的修補程式
* (Touch UI)透過Classic UI主控台刪除啟動，會讓所有頁面都無法編輯。 NPR-22491:CQ-4225074的修補程式
* 由於對話方塊中有額外空間，造成影像元件問題。 NPR-22528:CQ-4238183的修補程式
* 使用內部模式開啟元件時，先前載入的外掛程式在第二次時無法顯示。 NPR-22591:CQ-4236850的修補程式
* 在巢狀啟動中刪除啟動會導致子啟動變成孤立。 NPR-22621;CQ-4202639的修補程式
* （傳統UI側點）當頁面處於工作流程鎖定階段時，會停用「工作流程」標籤。 NPR-22722:CQ-4237557的修補程式
* 翻轉頁面上影像元件中新增的影像後，不會儲存變更，而原始影像會顯示在頁面上。 已透過[https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141)新增演算支援至影像核心元件。 NPR-22801:CQ-4221539的修補程式
* 當使用者嘗試從錨點選單刪除現有錨點時，Rich text editor元件視窗會關閉，而變更仍未儲存。 NPR-22802:CQ-4238167的修補程式
* Omnisearch篩選器不會顯示Sites主控台中的所有動作。 NPR-22804:CQ-4239007的修補程式
* 「在Touch UI中複製／貼上作業系統剪貼簿」和內部AEM剪貼簿的問題。 NPR-22807:CQ-4220383的修補程式
* Lucene Search傳回的摘錄反白顯示不一致。 NPR-22879:CQ-4238513的修補程式
* 啟動具有發佈例項的頁面會導致呈綠色狀態，而非變成琥珀色。 NPR-22927:CQ-4236310的修補程式
* (StyleSystem)從彈出式視窗選取樣式時，畫面位置會跳轉。 NPR-23183:CQ-4238867的修補程式
* （管理出版物）移至下個月的日曆需要按幾下。 NPR-23508:CQ-4242732的修補程式

### 平台 {#platform-2}

* Sling Exporter servlet無法正確匯出日文字元。 NPR-22153:CQ-4228920的修補程式
* 啟動期間調度程式死鎖。 NPR-22440:Sling-7004的修補程式
* 無法在兩個發佈實例之間同步組。 NPR-21943:Granite-19564的修補程式
* org.apache.sling.i18n共用作業階段／資源解析程式的效能問題。 NPR-23390:Sling-7543的修補程式

### 整合{#integration-5}

* com.day.cq.analytics.sitecatalyst中未關閉的資源解析程式。 NPR-22323:CQ-4236515的修補程式
* TargetContentImpl會在長時間執行的查詢期間，讓AEM變得呆滯。 NPR-22361:CQ-4236907的修補程式
* 目標引擎(mbox.js, at.js)不使用損毀的URL，並使用包含冒號的URL，因為某些部署可能會失敗。 NPR-22366:CQ-4237854的修補程式
* 提供自訂at.js或mbox.js時，包含指令碼會以文字而非HTML標籤寫入頁面。 NPR-22441:CQ-4203691的修補程式
* 在「目標」模式中，作者可以修改從Blueprint繼承的元件，而不取消繼承。 NPR-22751:CQ-4237907的修補程式
* PersonalizationDataSource會因遺失jcr而引發Null指標異常：內容節點。 NPR-22850:CQ-4222122的修補程式
* 使用非英文語言時，AEM定位失敗。 NPR-22917:CQ-4218213的修補程式
* 發佈含有目標內容的頁面會遺失相關資源。 NPR-23064:CQ-4227119的修補程式
* 使用者無法在mbox呼叫中看到測試靜態參數值，當以AT.js作為雲端設定的用戶端程式庫進行測試時，就會看到這些值。 NPR-21930:CQ-4234520的修補程式

### WCM-Foundation元件{#wcm-foundation-components-1}

* iParsys在取消選中取消／禁用繼承複選框後建立位置偏移。 NPR-21905:CQ-4230951的修補程式
* 表單下拉式元件的顯示／隱藏功能無法如預期般運作。 NPR-22327:CQ-4222853的修補程式
* CAPTCHA元件已停用以提高安全性，如果您使用CAPTCHA元件，則會傳送訊息「Captcha元件已停用，不應再使用」。 將在安裝6.3.2.1或更新版本後顯示。 AEM元件可自訂為包含reCAPTCHA，以提高安全性NPR-22151:CQ-4220052的修補程式

### WCM —— 頁面編輯器{#wcm-page-editor}

* 使用無效選擇器時的反映式跨網站指令碼(XSS)。 CQ-4270397的修補程式

### 轉換 {#translation-4}

* 調查「預覽」功能的問題。 NPR-22114:CQ-4223753的修補程式

### 使用者介面{#user-interface-2}

* 設定「最小」和「最大」日期範圍時，「珊瑚日曆」月份選擇器的問題。 NPR-22716:CUI-7187的修補程式
* (Classic UI)元件會顯示預設值，即使關聯的表單資料模型服務設為空白欄位亦然。 NPR-22272:GRANITE-19744的修補程式

### 花崗岩{#granite-2}

* Asset Share AEM Publisher例項的穩定性問題，是由記憶體洩漏造成的。 NPR-22205、NPR-23178:Hotfix for Sling-5668、Sling-7292和Sling-7470。
* 不穩定的服務ID不應用於會話屬性名。 NPR-22821:Granite-21059的修補程式
* 當http   電子白板管理的會話被失效，如果該會話沒有其它會話屬性，則容器會話也被失效。 NPR-23059:FELIX-5819的修補程式
* 啟動時，LogbackManager可能會漏掉某些OSGi配置。 NPR-23060:Granite-19791修補程式

### 商務 {#commerce-3}

* 在「體驗片段」功能表中啟用建立工作流程。 NPR-22347:CQ-4221661的修補程式
* WeRetail上可重複的體驗片段錯誤。 NPR-21958:CQ-4220061的修補程式
* 啟動包含已刪除體驗片段的頁面會引發NullPointerException。 NPR-23179:CQ-4239939的修補程式

### 專案 {#projects}

* （多語言項目）項目不列出19種以上語言的翻譯作業。 NPR-22498:CQ-4229978的修補程式

### 工作流程 {#workflow}

* （傳統UI）啟用或停用工作流程啟動程式會導致不良行為。 NPR-22907:CQ-4239153的修補程式

## 表單 {#forms-9}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

AEM Forms的主要亮點是：

* 新增對HTML5輸入類型的支援。
* 修正基本SOAP標題驗證。
* 新增超連結的標題屬性支援。
* 在Forms Designer的協助工具樹中啟用PDF/UA識別碼。
* 為Workbench使用者啟用憑證驗證。
* 新增支援製作符合PDF/A-2a或PDF/A-3a規範的PDF檔案。

### Forms add-on package {#forms-add-on-package-9}

#### 表單管理UI {#forms-admin-ui}

* 在「ECM連接器配置」頁的「檢查密碼」欄位中，密碼顯示在純文字檔案中。 NPR-22508:CQ-4236065的修補程式

#### Forms服務{#forms-service}

* 啟用SSL時，「提交」和「放棄」事件無法與「表單分析」搭配運作。 NPR-22637;CQ-4237973的修補程式

#### 使用者管理 {#user-management}

* 由於cglib-nodep版本不正確，無法同步LDAP。 NPR-22493:CQ-4234099的修補程式

#### 適用性表單 {#adaptive-forms-2}

* 規則編輯器的自訂功能正在增加額外的功能；在函式呼叫後，即使自訂函式傳回true，驗證仍失敗。 NPR-22481:CQ-4235499的修補程式
* 不論選取的日期模式為何，當顯示最小和最大驗證訊息時，日期選擇器元件不會遵循模式。 NPR-22444:CQ-4236269的修補程式
* 提交請求中傳送的日期格式應與日期選擇器元件中提供的模式對齊。 NPR-22384
* 在Android 6.0 Samsung裝置上，不會執行最適化表單文字方塊的指定字元數上限。 NPR-22363、NPR-22364:CQ-4235205的修補程式
* (Microsoft Edge)(IE11)具有多行欄位的自適應表單文本欄位元件將「Null」顯示為預設值，而非空白。 NPR-22284:CQ-69107的修補程式
* 最適化表單中的SOAP UTF-8輸入編碼會傳回亂碼頁面的錯誤。 NPR-20105:CQ-4222669的修補程式
* 在網站頁面中設定錯誤的表單後，AEM Forms容器元件便無法供編輯。 CQ-4237456的修補程式
* 在JEE伺服器上執行開發測試時失敗。 CQ-4222082的修補程式
* AF測試因Calvin Framework中的微型化問題而在JEE伺服器上失敗。 CQ-4217220的修補程式

#### Forms Manager {#forms-manager}

* (Firefox)無法更新Adaptive Forms的XML架構屬性，因為記錄檔案(DOR)中的選項不會像屬性頁面中的預先選取一樣出現。 NPR-22298:CQ-4237402的修補程式
* 發佈頁面後修改的表單不會在發佈網站時再次發佈。 NPR-23013:CQ-4236566的修補程式

#### 後端整合{#backend-integration-1}

* OOTB SOAP服務的基本驗證不適用於FDM整合中的基本驗證。 NPR-23238:CQ-4241308的修補程式

#### 通信管理{#correspondence-management}

* OOTB XDP在字母內使用並預覽時，會顯示與頁尾重疊的內容。 CQ-4212414的修補程式

#### 匯編器服務{#assembler-service}

* Acrobat DC和AEM報告中有關PDF/A-1b相容性檢查錯誤的差異。 NPR-22051、NPR-22050:CQ-4226128、CQ-4227671的修補程式

### Forms JEE安裝程式{#forms-jee-installer-8}

#### 工作台{#workbench}

* 為Workbench使用者啟用憑證驗證。 NPR-20644:CQ-4214486的修補程式
* 使用Workbench下載伺服器記錄檔僅適用於一台伺服器，而對於另一台伺服器則無法運作。 NPR-21079:CQ-4229842的修補程式

#### 流程管理{#process-management-1}

* （HTML工作區）捲軸的螢幕大小問題。 NPR-23288
* （HTML工作區）「處理起點」不會以英數字元順序排序。 NPR-22841 CQ-4238944的修補程式
* （HTML工作區）在工作區中關閉表單時，會觸發準備資料。 NPR-21127:CQ-4224574的修補程式
* （HTML工作區）在叫用需要附註且描述較長的程式時，「附註」展開按鈕無法運作。 CQ-4241488的修補程式

#### 核心 {#core-1}

* 啟動調度程式時遇到錯誤。 NPR-22990
* 防止瀏覽器儲存輸入HTML表單的認證。 NPR-21762:CQ-4206543的修補程式
* Core靜態代碼分析中所報告的問題應予以修正。 CQ-104446的修補程式

#### PDFG服務{#pdfg-service-3}

* PDF產生器無法產生具有指定書籤層級的PDF檔案。 NPR-22921、NPR-22285:CQ-4230562的修補程式
* 新增支援製作符合PDF/A-2a或PDF/A-3a規範的PDF檔案。 NPR-23021:CQ-4214172的修補程式

#### Forms Designer {#forms-designer-1}

* 當從設計人員儲存為PDF時，會遺失PDF/UA識別碼。 NPR-23137
* 路徑物件，例如：當從Designer儲存為PDF時，不會標籤邊框、底線和超連結。 NPR-23136
* 當從設計人員儲存為PDF時，影像物件沒有邊界方框。 NPR-23134
* 當從Designer儲存為PDF時，Designer中定義的內嵌超連結不會加上標籤，也不會有替代文字。 NPR-23133
* 使用AEM 6.3 Forms Designer開啟XML資料套件會從XML來源移除XHTML格式。 NPR-21178:LC-3917046修補程式

#### 安裝LCM {#install-lcm}

* 在安裝程式和LCM中將Jsafe Jar更新至Cryptoj 6.1.3.1。 NPR-21370

#### 簽名服務{#signatures-service}

* 嘗試透過HSM數位簽署／認證PDF檔案時發生例外。 NPR-21154:CQ-4226978的修補程式

### 6.3.2.1 {#osgi-bundles-and-content-packages-included-in-5}隨附的OSGI組合和內容封裝

AEM 6.3.2.1隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/bundle-list_002_.txt)

AEM 6.3.2.1內容套件清單

[取得檔案](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2是重要的更新，自2017年10月AEM 6.3 Service Pack 1(6.3.1.0)全面推出以來，已包含數項內部和客戶修正。

AEM Cumulative Fix Pack的主要亮點為：

* 已修改UI，以支援在AEM Assets中實作CUG功能。
* 已修正授權檢查頁面上的UI問題，以獲得更佳的體驗。
* 在AEM Forms App中啟用OSGi工作流程任務支援。

### 資產 {#assets-10}

* 已修改UI，以支援在AEM Assets中實作CUG功能。 NPR-19485
* 使用Touch UI將資產上傳為本身的直接子節點會造成問題。 資產會上傳為先前選取資產的直接子系。 NPR-19736
* 載入已儲存的搜尋／智慧型系列時，「日期範圍」述詞和「範圍」述詞無法運作。 NPR-19844:CQ-4220808的修補程式
* 當多個資產（超過4個）發佈至品牌入口網站時，AEM例項會變得無法運作。 NPR-20009:CQ-4213426的修補程式
* 無法從授權檢查頁面下載含空格的資產。 NPR-20067:CQ-4216557的修補程式
* 上傳具有多個alpha圖層的PSB檔案時的處理問題。 NPR-20250:CQ-4220869的修補程式
* 使用者無法下載已定義長檔名和免責聲明的資產。 NPR-20254
* ProductAssetsUploader會將JAVA快取的暫存檔案保留在Java TEMP檔案夾中。 NPR-20256:CQ-4221801的修補程式
* 由於授權問題，將版本比較程式碼取代為Adobe專屬程式碼。 NPR-20272:CQ-4223758的修補程式
* 字串屬性documentNumber的中繼資料會顯示為日期，但應是數字。 NPR-20291:CQ-4223991的修補程式
* 文字擷取會因為損毀的PDF而卡住。 NPR-20416:CTG-4150375的修補程式
* 包含具有非UTF-8相容名稱的資產的壓縮檔案無法正確下載。 NPR-20420:CQ-4219961的修補程式
* OmniSearch中的字元過多會導致AEM伺服器當機。 NPR-20434:CQ-4223602的修補程式
* DAM Asset API中繼資料瑕疵會中斷xmp回寫API。 NPR-20607:CQ-4220455的修補程式
* 新增使用者至系列時的效能問題。 NPR-20699:CQ-4225733的修補程式
* 動態媒體集不應允許從AEM發佈至品牌入口網站。 NPR-20320:CQ-4221147的修補程式
* 含空格和重音的視訊不會產生「轉譯」頁面的視訊。 NPR-19961:CQ-4221014的修補程式
* 已解決資產API的多個資料夾處理問題。 NPR-20569
* 當雲端服務設定中的目標路徑指向根路徑中的子資料夾時，AEM Dynamic Media Classic（前Scene7）無法從AEM伺服器同步資產。 CQ-4228265
* 已新增apache共用`{org.apache.commons/commons-email/1.5}`的電子郵件套裝，取代`{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`。

### 網站 {#sites-10}

* 管理員權限問題：無法從頁面屬性中移除已關閉的使用者群組成員。 NPR-20631
* 透過「管理出版物」發佈頁面時，「通知」方塊中應提供輸入的工作流程名稱。 NPR-20046:CQ-4221586的修補程式
* 在Rich Text Editor的兩列上套用樣式化文字，然後將它們合併為一個段落，會移除樣式化的範圍。 NPR-20110:CQ-4223051的修補程式
* 在「屬性編輯」對話方塊中對多個標籤中的欄位屬性所做的變更，有時不會儲存。 NPR-20286
* 「內容」片段中貼上內容結尾處的標籤非預期。 NPR-20413:CQ-4224014的修補程式
* 在Adobe Campaign中實作機制，從外部定位資源擷取內容資源的原則。 NPR-20667
* 在多欄位Touch UI中，Richtext增效模組無法同時用於內嵌和全螢幕列。 NPR-20973

### 行銷活動 {#campaign-1}

* 在包含多個parsys元件的頁面中，不會顯示佔位符。 NPR-20436;CQ-4215000的修補程式

### 商務 {#commerce-4}

* Internet Explorer 11無法正確顯示體驗片段。 NPR-20161:CQ-4223319的修補程式
* 在商務工作流程中，當根據包含多張影像的主要產品建立變型時，會自動插入空白影像。 NPR-20068:CQ-4222048的修補程式
* 在產品主控台的系列頁面上依標籤篩選無法運作。 NPR-20292:CQ-4224023的修補程式

### 社群 {#communities-8}

* 搜尋結果與搜尋結果元件不一致。 NPR-20070:CQ-4220913的修補程式
* 不會針對發佈元件上的任何協調者相關活動觸發電子郵件通知。 NPR-20122
* 匿名社群使用者會顯示空白分頁，但無結果。 NPR-20136:CQ-4220738的修補程式
* 設定當UGC偵測為垃圾訊息或使用者在預先協調的網站上張貼時的警報觸發。 NPR-20274:CQ-96850的修補程式
* 已解決AEM Communities網站頁面中的多個問題，包括不正確的重新導向和頁面重新整理問題。 NPR-20344
* CommunityUserOperationExtension會執行至類別轉換例外。 NPR-20532:CQ-4224385的修補程式
* 建立社群網站後，使用者無法從網站地圖開啟網站，因為上下文路徑不會優先於URL。 NPR-20730

### 整合{#integration-6}

* 將Analytics現有認證移轉至WSSE驗證。 NPR-19962:CQ-4218071的修補程式
* 在任何修改失敗並擲回錯誤後重新啟用區段。 NPR-20054:CQ-4218401的修補程式
* Search&amp;Promote雲端服務設定會忽略表單擷取方法，使其無法用於作者實例。 NPR-20447:CQ-4206076的修補程式
* 內容套件中模糊的篩選定義會導致在安裝Search&amp;Promote功能時覆寫路徑。 NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* 每次顯示TXT類型的資產的中繼資料屬性時，其屬性會顯示在不同的中繼資料編輯器中。 NPR-20239

### 平台 {#platform-3}

* 解決未關閉的資源解析程式異常。 NPR-19749:Granite的修補程式- 19143
* 要求自訂卡片與作業控制面板中的預設健康檢查一起顯示。 NPR-20145
* 頁面編輯器的註解層在Internet Explorer 11中無法正常運作。 NPR-20222:CQ-4222818的修補程式
* 在複製代理中將用戶代理設定為管理員時，會話洩漏。 NPR-20578
* 對於其他資料密集資源語句，請求屬性未取消設定。 NPR-20639:4226206的修補程式
* 已修正AEM中OOTB資產的捲動標頭請求問題。 NPR-20781:CQ-4221520的修補程式

### 專案 {#projects-1}

* 從「專案」主控台存取不同專案需要較長的載入時間。 NPR-20314
* 安裝AEM 6.3.0.1會移除dam-update-service使用者的金鑰庫。 NPR-20018
* 在某些自訂部署中，嘗試在addTask模組中選取受託人的使用者在使用者選擇器中填入清單需要更長的時間。 NPR-20283:CQ-4224193的修補程式

### 使用者介面{#user-interface-3}

* 儘管對話框中有屬性，Colorfield仍設定為「始終為必需」。 NPR-19702
* Internet Explorer 11的全螢幕多欄位元件不會顯示捲軸。 NPR-20261:CQ-4219782的修補程式
* 如果連續查詢被觸發而導致錯誤結果，則先前的查詢不會中止。 NPR-20398:GRANITE-19306的修補程式

### 工作流程 {#workflow-1}

* 使用者不會收到其收件匣中所接收工作流程工作的通知。 NPR-20213:CQ-4221639的修補程式
* 當在工作流模型的「對話」參與者步驟中按一下下拉式清單時，OOTB花崗岩使用者選擇器不會載入任何使用者。 NPR-20236

## 表單 {#forms-10}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

### Forms add-on package {#forms-add-on-package-10}

#### 適用性表單 {#adaptive-forms-3}

* 缺少對重複面板的聚集運算式的支援。 NPR-20861
* 下拉式清單會顯示最後儲存的值，即使相關聯的表單資料模型服務未傳回值亦然。 NPR-20710
* 無法在規則編輯器中編輯具有布林約束的現有規則。 NPR-21128

#### 表單入口{#form-portal}

* 即使HTML描述檔的資產類型不是XDP，也會針對最適化表單顯示HTML描述檔。 NPR-20079

#### 後端整合{#backend-integration-2}

* 無法在true/false之間設定交換機元件的值。 NPR-21111

#### OSGI Workflow {#osgi-workflow}

* 僅管理工作流程提交清單10個應用程式。 CQ-4230193

#### HTML5 Forms {#html-forms-3}

* 當XDP表單物件（如子表單）的名稱未在協助工具設定中定義時，會顯示為其工具提示。 NPR-20523

### Forms JEE安裝程式{#forms-jee-installer-9}

#### 流程管理{#process-management-2}

* FormSetPrefillApp起點不會在AEM Forms應用程式中預先填寫表單集欄位。 NPR-20950

#### Forms - AEM(LiveCycle){#forms-aem-livecycle}

* 安裝最新的CTJPEG2K程式庫，以解決重大的安全性弱點。 這會影響XMLFM（AEM和IfBA）、RM、PDFG模組。 NPR-20625:NPR-21337。

### 包含的功能套件{#feature-packs-included}

#### AEM Forms App {#aem-forms-app}

* 在AEM Forms App中啟用OSGi工作流程任務支援。 CQ-4222638

### 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}隨附的OSGI組合和內容封裝

AEM 6.3.1.2隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/6_3_1_2-bundle-list.txt)

AEM 6.3.1.2內容套件清單

[取得](assets/do-not-localize/6_3_1_2-content-package-list.txt)
FileAEM Cumulative Fix Pack 6.3.1.1是重要的更新，其中包含自2017年10月AEM 6.3 Service Pack 1(6.3.1.0)全面推出以來的數項內部和客戶修正。

AEM Cumulative Fix Pack的主要亮點為：

* 針對預設中繼資料結構表單啟用發佈至品牌入口網站動作。
* 在具有dc的影像的影像卡上顯示標題的行為變更：title屬性設為字串[](multifield)。
* 以建立時間元件取代伺服器端的時間轉換。
* 已啟用從AEM發佈標籤至品牌入口網站的標籤／標籤控制台。
* 已發佈的JSON API可使用內容片段。
* 內建儲存庫(Apache Jackrabbit Oak)已更新至1.6.5版。

### 資產 {#assets-11}

* 將兩個具有相同屬性的欄位對應為不同類型的屬性欄位，會引發內部錯誤。 NPR-19462:CQ-4216828的HF
* dc:標題和dc:crx /de中的描述不會變更為多欄位值。 NPR-19570:CQ-4209086的HF
* Dynamic Viewer會載入最低品質的視訊轉譯，以測試作者模式的視訊播放體驗。 NPR-19004
* 無法針對名稱中包含空格的資產下載動態轉譯。 NPR-19433:CQ-4211738的修補程式
* 無法使用Chrome在「欄」檢視中載入頁面／資產的完整清單。 NPR-19566:CQ-4214248的修補程式
* 在選取任何結構、搜尋Facet或預設集時，無法使用「發佈至品牌入口網站」選項。 NPR-19550
* 在欄檢視中選取資產並按一下編輯時，頁面會傳回錯誤。 NPR-20301:CQ-4220052的修補程式
* 跨越正時區和負時區時，資產到期顯示關閉。 NPR-20329:CQ-4219333的修補程式

### 行銷活動 {#campaign-2}

* 為促銷活動選擇預設體驗時，不會顯示促銷活動滑桿元件。 NPR-19213

### 整合{#integration-7}

* 自訂at.js檔案在與匿名使用者存取時不會發佈。 NPR-19542:CQ-4219592的修補程式
* 設定精靈中的「定位引擎」欄位已設為ContextHub(AEM)，而非Adobe Target。 NPR-19320:CQ-4218465的HF
* 建立體驗時，受眾區段會損毀。 NPR-19110
* 當目標模組被編輯並儲存多次時，定位對話框不會在定位模式中顯示。 NPR-19144:CQ-4216708的修補程式
* 在Classic UI的Adobe Digital Publishing Solution中，存取文章設定不正確的屬性。 NPR-19367
* 如果使用者可存取多個區域，在透過促銷活動個人化選件時自動折疊的行為不正確。 NPR-19290:CQ-4218029的修補程式

### 網站 {#sites-11}

* 由於將執行個體升級至AEM 6.1SP2-CFP3後，Sidekick.js中的程式碼變更，因此無法重新填入多重複合欄位下拉式值。 NPR-19450:HF for CQ-4194771
* WCMMode.EDIT無法在編寫模式下用於目標元件。 NPR-19387
* 已發佈的JSON API可使用內容片段。 NPR-19500
* 粗體、斜體、下划線功能不適用於作者對話框中的富格文本編輯器欄位。 NPR-19670:NPR-19718:CQ-4219088的修補程式

### 行動隨選{#mobile-on-demand-1}

* AEM文章主控台的轉換問題，與使用全尺寸影像相同，會造成影像效果不佳。 NPR-19088

### 轉換 {#translation-5}

* 無法為翻譯項目生成預覽。 NPR-19289

### 安全性 {#security}

* SSL連接錯誤。 無法與伺服器建立安全連接。 NPR-19628

### 社群 {#communities-9}

* 透過預先協調的網站張貼內容時，會觸發郵件。 NPR-20008
* 電子郵件通知不適用於發佈元件上與協調者相關的任何活動。 NPR-19767:CQ-4218060的HF

### 平台 {#platform-4}

* AEM生產伺服器部署的穩定性問題。 NPR-19707
* 在升級至AEM 6.3後，找不到參照以指令碼實作之標籤的自訂標籤庫。NPR-19087
* AEM 6.3.1的HTL錯誤修正。NPR-19161
* 多欄位元件中無法編輯Richtext欄位。 NPR-19604:Granite-16755的修補程式
* Adobe電子郵件範本服務會新增標籤至自訂使用者範本。 NPR-19190
* Oak 1.6.5的修補程式。NPR-19148

### 商務 {#commerce-5}

* 在選擇XF變數編輯器後，「啟動工作流」按鈕無效。 NPR-19642:CQ-4207796的修補程式

### 專案 {#projects-2}

* 專案編輯人員無法將資產複製／貼入專案資產檔案夾。 NPR-19619:CQ-4215321的修補程式

### Web內容管理{#web-content-management}

* 在「轉出」畫面中，無法勾選或取消勾選與livecopy頁面對應的核取方塊。 NPR-19518
* 頁面屬性的大量編輯無法正確使用，因為目前所有標籤和欄位都可用於批量編輯。 NPR-19451
* 在傳統UI中編輯影像時，不會顯示OOTB屬性和影像對齊屬性。 NPR-19488:HF for CQ-4217914

### 用戶介面{#user-interface-4}

* 使用Google Chrome瀏覽器時，使用者無法使用TouchUI中的欄檢視來載入頁面／資產的完整清單。 NPR-19566:CQ-4214248的修補程式

### 品牌入口網站 {#brand-portal-1}

* 無法從AEM發佈資產並加上註解和註解。 NPR-19590:CQ-4218386的修補程式
* 啟用從AEM發佈標籤至品牌入口網站的標籤／標籤控制台。 NPR-20271:CQ-4223948的修補程式
* 修正品牌入口網站雲端服務設定UI上的「已啟用」欄位。 CQ-4211101的修補程式
* 搜索表單複製失敗。 CQ-4220080的修補程式

## 表單 {#forms-11}

AEM Forms修正是透過附加元件套件和隨發行提供的其他修補程式安裝程式來提供。 如需詳細資訊，請參閱「AEM Forms發行」。

### Forms add-on package {#forms-add-on-package-11}

#### 最適化表單{#adaptive-forms-4}

* 提交至JEE工作流程不會將輸出參數從JEE端傳回至AEM，並會擲回「因為值不是基本值而忽略」錯誤。 NPR-20265
* 最適化表單不允許PDF在Safari中做為附件。 NPR-19625
* RestoreGuideState會覆寫customcontextproperty map。 CQ-4222877
* 使用雲端服務設定Google reCaptcha時，在需要為外部連線設定org.apache.http.proxyconfigurator的環境中，POST呼叫似乎不會經過PROXY。 NPR-20454
* 基於XSD架構的最適化表單會針對安裝中具有小數分隔符號&quot;。&quot;以外的地區設定，提交數值欄位的錯誤XML值。 導致錯誤。 NPR-20444
* 對第三方伺服器發出HTTP請求時，不接受為「Apache HTTP Components Proxy Configuration」設定的代理設定。 使用HTTP GET或POST呼叫的連線逾時問題。 NPR-20457、NPR-20456、NPR-20455、NPR-20451

#### 表單資料整合{#forms-data-integration}

* SOAP服務的輸出UTF-8字元無法正確複製到非英文地區設定的最適化表單欄位。 NPR-20238:NPR-20103

#### 通信管理{#correspondence-management-1}

* 從文字檔案複製貼上內容會在文字編輯器中載入其內容色彩和字型。 NPR-19521

#### Assembler Services {#assembler-services}

* 在將檔案驗證為PDFA-1b格式時，Acrobat和AEM的結果不一致。 NPR-19280

#### 工作流程 {#workflow-2}

* 「工作流程簽署」步驟，允許http呼叫透過Proxy連線。 NPR-20529

#### HTML5 Forms {#html-forms-4}

* 新增對preSubmit事件的支援。 NPR-20604

### Forms JEE安裝程式{#forms-jee-installer-10}

#### 流程管理{#process-management-3}

* 當表單最大化／最小化並儲存為草稿或轉送時，工作流程附件、註解和詳細資訊標籤在工作區中無法運作。 NPR-20243
* 在HTML工作區中提交資料後，多行文字欄位(TextArea)不會保留新的行字元或在文字中斷。 NPR-20085

#### 流程報告{#process-reporting}

* 由於指針異常，進程報告無法正確讀取資料。 NPR-19759

>[!NOTE]
>
>安裝列在[AEM Forms Releases](aem-forms-releases.md)文章中的LiveCycle內嵌套件，以修正問題。

#### 標準服務{#standard-services}

* docConverter不支援PDF中的平面化透明度，且無法產生PDF/A。NPR-16228:CQ-4214488的修補程式

#### 核心 {#core-2}

* 在JBoss應用程式的叢集設定中執行的AEM Forms伺服器停止時，應用程式伺服器會與資料庫中斷連線。 這可能導致資料損毀問題。 NPR-19724

### 包含的功能套件{#feature-packs-included-1}

* 下拉式中繼資料結構欄位無法設為強制，因為資產遺失強制欄位驗證。 NPR-17882:FP for CQ-4208373

### 6.3.1.1 {#osgi-bundles-and-content-packages-included-in-7}隨附的OSGI組合和內容封裝

AEM CFP 6.3.1.1隨附的OSGi搭售清單

[取得檔案](assets/do-not-localize/bundle-list.txt)

AEM CFP 6.3.1.1內容套件清單

[取得檔案](assets/do-not-localize/content-package-list.txt)

AEM Cumulative Fix Pack 6.3.0.2是重要的更新，自2017年4月AEM 6.3全面推出以來，已包含數項內部和客戶修正。

AEM Cumulative Fix Pack的主要亮點為：

* 用戶訪問控制的可審計性
* 包含內建儲存庫1.6.2版(Apache Jackrabbit Oak)
* 已解決未關閉的資源解析程式問題
* 智慧型內容服務的簡化配置
* 解決內容片段驗證問題
* 在混合裝置上改善中繼資料結構的可編輯性
* 解決即時副本中的元件層級同步問題
* 改善欄檢視中內容密集頁面的可用性
* 已改善長標題頁面的頁面命名慣例合規性
* 改善Touch UI上的促銷活動個人化體驗
* 修正各種專案覆蓋問題

### 平台 {#platform-5}

* Oak 1.6.2的修補程式。NPR-16993
* 使用篩選器開啟搜尋時，不再設定路徑。 NPR-17398:CQ-4204870的修補程式
* AEM中使用者權限變更的可稽核性需求。 NPR-17061
* 與DM Cloud Services的連線久拖不決，導致「開啟的檔案太多」例外。 CQ-4211407

### 資產 {#assets-12}

* 使用不同選項設定智慧型內容服務時的可用性問題。 NPR-18200:CQ-4201557的修補程式
* 二進位流中的資源洩漏到S3資料儲存。 NPR-18041:CQ-4209506的修補程式
* 當ASCII/UTF-8編碼文字檔案上傳至AEM Assets且縮圖產生失敗時，會發生錯誤。 NPR-18006:CQ-4209345的CFP
* 預設中繼資料結構會造成內容片段驗證失敗。 NPR-17769:CQ-4211111的修補程式
* com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner中的未關閉資源解析程式。 NPR-17598:CQ-4209018適用的CFP
* 請求建立多個複製代理，以便將資產發佈至品牌入口網站。 NPR-17189
* 「日文」檔案夾下的資產檢閱工作無法運作。 CQ-4204782
* 當資產從其屬性頁面移動時，會發生Null指標異常。 CQ-4204251
* 如果AEM多次連結至InDesign檔案，則無法追蹤屬性頁面中資產的後續參照。 CQ-4204186
* 在混合裝置上的Chrome中編輯中繼資料結構表單時，在其中新增標籤的問題。 CQ-4201810
* 上傳重複資產時，（刪除／保留）選項會套用至所有資產，即使在偵測到重複的對話方塊中未選取此選項亦然。 CQ-4201673
* 當移動包含150個以上傳入參考的資產資料夾時，會出現Null指標例外。 CQ-4200981
* 對於下載的資產資料夾，如果擷取ZIP檔案的內容時發生衝突，預設選項會顯示為「建立版本」，而非「同時保留兩者」。 CQ-97800
* 具有應用程式唯讀權限的使用者無法從AEM Mobile內容管理預覽內容。 NPR-17486:CQ-4209690適用的CFP
* 「建立目錄」按鈕在「目錄」控制台的列視圖中無法工作。 CQ-4209952

### 網站 {#sites-12}

* 透過資料智慧資源屬性內嵌影像／視訊元件的問題。 NPR-18182:CQ-4212100的CFP
* 在LiveCopy中重新套用繼承時，已修改的本地化元件不會還原為原始格式。 NPR-18172:CQ-4211379的修補程式
* 在Touch UI的欄檢視中導覽內容繁多的頁面時發生問題。 NPR-17799:CQ-4199611的修補程式
* `com.day.cq.wcm.core.impl.VersionManagerImpl`中未關閉的資源解析器。 NPR-17789:CQ-4211152的CFP
* 長頁標題的頁面名稱不會依慣例產生。 NPR-17633:CQ-4209056的修補程式
* 在部署於Jboss EAP 6.4的AEM 6.3中，在Touch UI上建立頁面的問題。NPR-17589:CQ-4210137的修補程式
* 當巢狀群組存在時，工作流程狀態提供程式會導致例項鎖定。 NPR-17556:CFP要求CQ-4202056
* 以下對象中未關閉的資源解析器：

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497:CQ-4208673的CFP
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495:CQ-4208668的CFP
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494:CQ-4208669的CFP
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493:GRANITE-17404的CFP

### 整合{#integrations-1}

* 已解決當AEM Day HTTP Client 3.1 OSGI設定為需要摘要驗證的Proxy時，可能發生的AEM Search元件錯誤。 18128盧比：NPR-18029的修補程式
* 透過Classic UI個人化促銷活動和相關體驗的問題。 NPR-18127:CQ-4211559的修補程式
* 將品牌／區域設定為網站的根頁面時，子頁面中「區域」的繼承一旦取消，便無法復原。 NPR-17753:CQ-4210139的修補程式

### 工作流程 {#workflow-3}

* 在非暫時性工作流中，不會保存在外部進程步驟之前所做的進程歷史記錄和元資料更改。 NPR-17848:GRANITE-17757的修補程式
* 工作流對話框欄位的值不會保存在工作項目節點中。 NPR-17734:CQ-4210369的修補程式
* 從收件匣編輯工作時，會發生不可分割的日期錯誤。 CQ-4208749

### 專案 {#projects-3}

* 修正各種專案覆蓋問題。 NPR-17733
* 專案模組中的pod重組會降低其可設定性。 CQ-4209859
* 將頁面新增至翻譯工作時，資產路徑會變更至個別本地化網站。 CQ-4206007

### 安全性 {#security-1}

* 上傳LDAP使用者頭像的問題。 NPR-16561
* 請求在Apache Sling API中使用org.apache.sling.servlets.post servlet(2.3.22)的升級版本，以預先防範XSS弱點。 NPR-18963

## 表單 {#forms-12}

AEM Forms修正可透過Forms附加元件套件和隨發行提供的其他修補程式安裝程式傳送。 如需詳細資訊，請參閱[AEM Forms Releases](aem-forms-releases.md)。

AEM Forms的主要亮點是：

* 修正對應管理文字模組、字母預覽，並以程式設計方式啟動建立對應管理UI。
* 修正PDF/A-1b驗證、將大型影像檔案轉換為PDF，以及PDF產生器中的日文PDF檔案。
* 可用性修正，以管理信件、檔案安全性和表單工作流程。
* 新增支援擷取塗鴉簽名欄位的審核事件。

### Forms add-on package {#forms-add-on-package-12}

**信件管理**

* 編輯對應管理片段時，文字編輯器會顯示內嵌條件以及已處理的文字。 CQ-4211930
* 在建立信件管理信函時，不保存信函的說明。 NPR-18089
* 項目清單上方和下方的額外邊界會顯示在文字編輯器中，但HTML和PDF轉譯中則不顯示。 NPR-18126
* 當HTML送出使用POST方法時，建立對應UI無法啟動。 NPR-18202
* 當文本模組被保存且文本模組中的表達式不包含開啟或關閉表達式標籤時，不會顯示錯誤消息。 文字模組會顯示錯誤訊息，無法在字母中呈現。 NPR-18535
* 新增內容或按下Enter鍵時，div標籤會新增至文字模組。 NPR-18240

**匯編器**

* 在驗證PDF/A-1b相容的PDF檔案時，AEM Forms會傳回驗證錯誤：PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED。 當使用Adobe Preflight和協力廠商軟體驗證時，PDF檔案不會傳回錯誤。 NPR-18011
* 在驗證PDF檔案以符合PDF/A-1b規範時，AEM Forms會傳回驗證錯誤：表單欄位有多種外觀。 PDF檔案與PDF/A-1b相容。 NPR-18013

**監視資料夾**

* 在選擇使用工作流處理檔案時，在建立監視資料夾時，工作流模型選擇下拉式清單將出現截斷。 NPR-17566

**HTML5 Forms**

* AEM Forms不會擷取塗鴉簽名欄位的稽核事件。 NPR-15286

**表單管理員**

* AEM Forms UI會以最舊的首次順序列出所有資產。 使用者無法以最新的首次順序重新排序資產。 NPR-18450

**Java API參考**

新增com.adobe.livecycle.content類別的JavaDocs。 NPR-18468

### Forms JEE安裝程式{#forms-jee-installer-11}

**PDF產生器**

* PDF Generator服務無法將超過100 MB的影像轉換為PDF檔案。 函號CQ-4208628
* 當PDF產生器服務與日文語言OCR搭配使用時，就會產生反轉的PDF。 NPR-17602

**流程管理**

* AEM Forms進程不會填入TaskContext變數。 NPR-18199

**Document Security**

* Microsoft Excel和Microsoft PowerPoint開啟使用AEM Document Security Extension for Microsoft Office保護的檔案需要更長的時間。 CQ-4212358
* 當建立新原則且與現有原則名稱相同的原則時，會發生內部伺服器錯誤。 NPR-18247

## 包含的功能套件{#feature-packs-included-2}

* AEM中使用者權限變更的可稽核性需求。 NPR-17061

AEM Cumulative Fix Pack 6.3.0.1是重要的更新，自2017年4月AEM 6.3全面推出以來，已包含數項內部和客戶修正。AEM Cumulative Fix Pack的主要重點為：

* 以下方面的改進：

   * 內容片段、網站和Rich Text編輯器、規則編輯器和範本編輯器元件
   * 社交評論和Facebook社交登入
   * 配置和啟動翻譯作業
   * 在社交社群中存取通知的回應時間
   * 在DAM儲存庫中顯示審核任務

* 在Package Manager中提供驗證選項，以偵測覆蓋與CFP之間的衝突

## 透過軟體散發下載CFP的指示{#download-instructions-for-cfp-via-package-share}

您可直接從[Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8)下載CFP套件，或執行下列步驟：

1. 開啟[軟體分發](https://experience.adobe.com/downloads)。 您必須有Adobe ID才能登入「軟體散發」。
1. 點選頁首功能表中的「Adobe Experience Manager ]**」。**[!UICONTROL 
1. 點選套件名稱，選取「**[!UICONTROL 接受EULA條款]**」，然後點選「**[!UICONTROL 下載]**」。

## 安裝指示 {#installation-instructions}

本節會逐步帶您瞭解安裝CFP的需求和步驟。

### 安裝{#before-you-install}之前

>[!NOTE]
>
>Adobe提供的選購功能套件與發行版本和累積修補程式套件有相依性。 如果您已安裝任何功能套件，請聯絡[AEM客戶服務團隊](https://helpx.adobe.com/tw/marketing-cloud/contact-support.html)以驗證此AEM 6.3版累積修補程式套件的相容性。

>[!NOTE]
>
>建議您在嘗試安裝軟體包之前，先對每個新安裝軟體包運行驗證。 預驗證會分析並報告安裝前發現的任何錯誤，並主動向用戶警告此類錯誤。
>
>您可以在[https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator)存取「驗證」選項的檔案

* AEM 6.3.3.0是CFP的先決條件。 請造訪[升級檔案](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html)，以取得有關將AEM安裝升級至AEM 6.3的詳細指示。
* 對於使用RDBMK或MongoDB的叢集部署，CFP套件可安裝在任何使用Package Manager的Author執行個體上。
* 在安裝累積修補程式套件之前，請確定要建立快照或備份您的AEM實例。
* 不支援解除安裝CFP。

### 添加新記錄程式{#adding-new-loggers}

若要在安裝SP/CFP時設定除錯層級記錄並擷取活動記錄檔，請遵循下列步驟：

* 您可以在預設位置[http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog)新增新的記錄器，並包含以下屬性：

   * 記錄層級：除錯
   * 加法：false
   * 日誌檔案：logs/activity.log
   * 記錄器：org.apache.jackrabbit.vault.packaging.impl.ActivityLog

activity.log將建立於   crx -quickstart /logs資料夾。

### 通過軟體分發安裝Cumulative Fix Pack {#install-the-cumulative-fix-pack-via-package-share}

請執行下列步驟，在現有的AEM 6.3執行個體上安裝Cumulative Fix Pack:

1. 按一下[軟體分發](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip)連結下載軟體包。

1. 開啟[包管理器](http://localhost:4502/crx/packmgr/index.jsp) ，然後按一下&#x200B;**[!UICONTROL 上載包]**&#x200B;來上載包。

1. 選擇軟體包名稱，然後按一下&#x200B;**[!UICONTROL Install]**。

### 自動安裝{#automatic-installation}

CFP可透過下列方式自動安裝至執行中的執行個體：

* 在伺服器運行時將軟體包放入`../crx-quickstart/install`中。 軟體包會自動安裝。
* 使用Package Manager的[HTTP API ](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/package-manager.html) —— 請確定您使用`cmd=install&recursive=true` —— 如此巢狀套件便已安裝。

### 驗證安裝{#validate-installation}

1. 「產品資訊」頁面(`/system/console/  productinfo`)現在應在「已安裝產品」下方顯示更新版本字串「Adobe Experience Manager, Version 6.3.3.8」。
1. 所有OSGI組合在OSGI主控台中都是ACTIVE或FRAGMENT(使用Web主控台：`/system/console/bundles`)。

>[!NOTE]
>
>成功安裝套件時，錯誤記錄檔上會顯示資訊性訊息，指出內容套件已成功安裝，例如「Content Package **AEM-6.3.3-Cumulative-Fix-Pack-7**&#x200B;已成功安裝。」

>[!NOTE]
>
>自AEM 6.3.3.1以來，Jackrabbit FileVault中的記錄檔層級已針對大部分訊息從INFO變更為DEBUG。 若要取得安裝在AEM 6.3.3.1或更新版本的內容套件的安裝記錄檔，請啟用org.apache.jackrabbit.vault.packaging.impl的DEBUG記錄檔層級。

### 安裝AEM Forms {#install-aem-forms}

>[!NOTE]
>
>如果您不使用AEM Forms，請略過本節。

#### 安裝AEM Forms附加元件{#install-forms}

1. 請確定您已安裝AEM 6.3.3.x CFP套件。
1. 針對您的作業系統，下載列在[AEM Forms發行版](aem-forms-releases.md)的對應Forms附加元件套件。
1. 如[安裝AEM Forms附加套件](https://helpx.adobe.com/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html)中所述，安裝Forms附加套件。

#### 安裝AEM Forms JEE bundles套件{#install-aem-forms-jee-bundles-package}

AEM Forms JEE中的修正會透過個別安裝程式提供。 如需在JEE的AEM Forms上安裝CFP的詳細資訊，請參閱[在AEM Forms JEE上安裝CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer安裝程式{#designer-installer}

1. 要安裝更新，請運行Designer 6.2.0_&lt;Language>_Cumulative_QF.msp檔案。
1. 在歡迎畫面上，按一下&#x200B;**update**。 安裝開始。
1. 安裝完成後，按一下&#x200B;**finish**。

## AEM Forms JEE(JBoss EAP){#configuration-settings-for-aem-forms-jee-jboss-eap}的組態設定

>[!NOTE]
>
>如果要安裝6.3.3.0或更新版本，請執行以下過程以配置JBoss應用程式伺服器的設定。 如果您要在Oracle WebLogic或IBM WebSpehere應用程式伺服器上執行的AEM Forms伺服器上安裝6.3.3.0，則不需要額外的設定。 如需詳細資訊，請參閱[AEM 6.3.3.0發行說明](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html)。

## Search&amp;Promote整合的組態更新{#configuration-updates-for-search-promote-integration}

在AEM Cumulative Fix Pack 6.3.0.2及更新版本中，用於Search&amp;Promote整合的OSGi組態為&#x200B;**Apache HTTP Components Proxy Configuration**。 不再使用Day Commons HTTP Client 3.1的Proxy設定。

## 已知問題 {#known-issues}

* 在安裝AEM CFP 6.3.3.x時可能會發生下列錯誤和警告，而且可以安全地忽略：

   * *WARN* [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependependendencements.jar-jar-jar-jar-jar-s-jar-jar-bingruntis-blexing runtivexing runtime異常。
   * *ERROR* [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.sosical.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)]等待註冊表更改完成未註冊的超時。 CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver服務遺失，無法要求服務，傳送狀態503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource:無法檢查資源[/bin/receive] ，頁面管理器不可用
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver:呼叫錯誤處理常式會導致錯誤
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver原始錯誤null
   * org.apache.sling.engine.impl.DefaultErrorHandler錯誤處理常式失敗：java.io.IOException
   * *ERROR* [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR(org.osgi.framework.ServiceException:服務工廠返回空值。 (元件：com.day.cq.dam.handler.standard.ps.PostScriptHandler)

**品牌入口網站**

* 自6.3.1.2起，智慧型系列的「發佈至品牌入口網站」按鈕已移除。

**使用者介面**

>[!NOTE]
>
>如果您受到這兩個問題中任何問題的影響，請連絡[ AEM客戶服務](https://helpx.adobe.com/marketing-cloud/contact-support.html)。

* 由於「管理搜尋」功能中有許多要求，所以會發現CPU使用率較高。 NPR-24229
* 重新開啟元件時，pathBrowser中未選取PathField。 NPR-24177

## NPR-27692 {#configuration-settings-required-for-npr}所需的配置設定

>[!NOTE]
>
>此組態設定適用於CFP 6.3.3.2和更新版本。 它指示您更新`sling` .properties檔案中的引導委託屬性。

若要手動更新adobe- livecycle - cq -author.ear/ cq .war中的變更，請遵循下列步驟：

* 停止AEM伺服器。
* 前往adobe-livecycle-cq-author.ear/cq.war
* 開啟adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml進行編輯：

   * 將&#x200B;**sling.bootdelement.ibm** param-name值更新為：

      * com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * 在進行上述變更後，init-param應該如下所示：

      * &lt;init-param>\
         &lt;param-name>sling.bootdesignation.&lt;/param-name> &lt;param-value>ibmcom.ibm.xml。*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* 從websphere應用程式伺服器解除安裝先前的企業封存檔(EAR)檔案，並依照[https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)第10.2節的步驟安裝更新的EAR檔案
* 保存檔案並重新啟動伺服器。 [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## NPR-23208 {#configuration-settings-required-for-npr-1}所需的配置設定

>[!NOTE]
>
>此組態設定適用於6.3.2.2和更新版本。 它指示您通過CRX-DE手動更新訪問控制清單(ACL)策略，因為ACL由於「merge_preserve」acHandling而無法通過CFP安裝進行更新。

**手動添加ACL策略的文檔**

要更新ACL策略，請添加以下通過CRX-DE的訪問控制：

`1)` 在「/content」路徑\
`a)` 主管：參考調整服務\
類型：允許\
權限：jcr:read, jcr:modifyProperties\
限制：rep:glob=&quot;/*/jcr:content&quot;\
`b)` 主管：參考調整服務\
類型：允許\
權限：jcr:read, jcr:modifyProperties\
限制：rep:glob=&quot;/*/jcr:content/*&quot;

`2)` 在「/content/usergenerated」路徑\
`a)` 主管：參考調整服務\
類型：允許\
權限：jcr:write

`3)` 在「/etc」路徑\
`a)` 主管：參考調整服務\
類型：允許\
權限：jcr:read, jcr:modifyProperties\
限制：rep:glob=&quot;/*/jcr:content&quot;\
`b)` 主管：參考調整服務\
類型：允許\
權限：jcr:read, jcr:modifyProperties\
限制：rep:glob=&quot;/*/jcr:content/*&quot;

## NPR-19450 {#configuration-settings-required-for-npr-2}所需的配置設定

>[!NOTE]
>
>此組態設定適用於CFP 6.3.1.1和更新版本。

**配置屬性CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL。**

該屬性控制頁` /  jcr   :content`節點下節點子樹的最大深度，直到儲存庫中顯示的節點用於獲取頁屬性為止。 會忽略此屬性中指定深度下方的任何節點。

預設值為1。 可以覆蓋值，方法是覆蓋檔案constants.js(`/libs/cq/ui/widgets/source/constants.js`)，取消注釋CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL屬性，並為其指定所需值（頁面/jcr:content下的最大深度，直到儲存頁面屬性資料為止）。

**如果用戶需要建立多個頁變型，使頁的/ jcr:content節點下的節點數大於1000，請使用以下步驟進行配置更改：**

* 設定Apache Sling的屬性JSON Max結果
* 使用`/system/console/  configMgr`獲取Servlet
* 將其值設定為>1000（當前預設值），使此數字大於/ jcr:content子樹中的節點總數，直到上述配置深度為止。

這可讓sling GET servlet能夠傳回所有必要的節點。

## Uber Jar {#uber-jar}

6.3.3.8版Uber Jar可在[Adobe Public Maven資料庫](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/)取得。

要在Maven項目中使用Uber Jar，請參閱[如何使用Uber jar](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/ht-projects-maven.html)一文，並在項目POM中包括以下相關性：

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## 已移除／已過時的功能{#deprecated}

本節列出已從AEM 6.3移除或淘汰的功能和功能。

| 區域 | 功能 | 替代方案 | 版本 |
|----|-----|-----|-----|
| 資產與Adobe Creative Cloud整合 | [AEM to Creative Cloud資料夾](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/creative-cloud.html) 共用是在AEM 6.2中引進的，可讓創意使用者存取AEM的資產。Creative Cloud應用程式中發行的新功能Adobe Asset Link提供更佳的使用者體驗，並可直接從Photoshop、InDesign和Illustrator內部，以更強大的方式存取AEM中的資產。<br /> Adobe不會進一步增強資料夾共用功能。雖然AEM中包含此功能，但強烈建議客戶使用此取代。 | Adobe Asset Link或案頭應用程式。 如需詳細資訊，請參閱[AEM Creative Cloud整合](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html)文章。 | AEM 6.3.3.x |

## 包含{#osgi-bundles-and-content-packages-included-1}的OSGi捆綁包和內容包

下列文字檔案列出CFP中包含的OSGi組合和內容封裝。

* [AEM 6.3.3.8隨附的OSGi搭售清單](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [AEM 6.3.3.8內容套件清單](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM發行和更新](https://helpx.adobe.com/experience-manager/aem-releases-updates.html)
>* [AEM 6.3修補程式頁面](https://helpx.adobe.com/experience-manager/kb/aem63-available-hotfixes.html)
>* [AEM 6.3版本注意事項](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM產品頁面](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.3 檔案](https://docs.adobe.com/content/docs/en/aem/6-3.html)
>* 訂閱[Adobe優先產品更新](https://www.adobe.com/subscription/priority-product-update.html)

