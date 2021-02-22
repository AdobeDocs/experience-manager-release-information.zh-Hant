---
title: AEM、CQ 和 CRX 的較舊版本
description: 舊版 Adobe Experience Manager、CQ 和 CRX 的文件套件。
translation-type: ht
source-git-commit: c8e7f79be233c94d33b7605c73e586dce022412c
workflow-type: ht
source-wordcount: '773'
ht-degree: 100%

---


# 舊版 [!DNL Adobe Experience Manager]、CQ 和 CRX {#older-versions-aem-cq-crx}

## 舊版 [!DNL Experience Manager] 說明文件 {#older-version-aem-documentation}

本頁所列的 [!DNL Experience Manager]、CQ 和 CRX 版本已終止服務，Adobe 不再正式販售。您可自助使用這些較舊版本的最新版本官方說明文件。建議您升級至最新版本 (目前為 [[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html))。

>[!NOTE]
>
>若要了解 [!DNL Experience Manager] 版本何時結束核心支援，請參閱[產品和技術支援期間](https://helpx.adobe.com/support/programs/eol-matrix.html)並搜尋 `AEM`。

### 安裝之前 {#before-installation}

下載套件前，請先決定要使用內容的受眾。此決定會決定其部署方式：

* 開發人員可在本機安裝，以供快速參考。
* 若為更廣泛的組織說明文件需求，建議將此套件部署在內部可存取、非生產的 AEM Author 執行個體上。

>[!NOTE]
>
>使用者必須登入 [!DNL Experience Manager] 執行個體才能在 [!DNL Experience Manager] Author 上存取此內容。預設無法在 AEM Publish 上存取此內容 (因位於 /libs 下)。

## Software Distribution 位置 {#software-distribution-locations}

您需有有效 Adobe ID：

* 如果您沒有 Adobe ID，可在 www.adobe.com 建立 Adobe ID
如果您需要建立或管理 Adobe ID 的協助，[請參閱這份指南](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] 版本 | Software Distribution 連結 |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.2 | [從 Software Distribution 下載 AEM-DOCS-6.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-2.zip) |
| [!DNL Experience Manager] 6.1 | [從 Software Distribution 下載 AEM-DOCS-6.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-6-1.zip) |
| [!DNL Experience Manager] 6.0 | [從 Software Distribution 下載 AEM-DOCS-6.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [從 Software Distribution 下載 AEM-DOCS-5.6.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5.6 | [從 Software Distribution 下載 AEM-DOCS-5.6](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [從 Software Distribution 下載 CQ-DOCS-5.5](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [從 Software Distribution 下載 CQ-DOCS-5.4](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [從 Software Distribution 下載 CQ-DOCS-5.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [從 Software Distribution 下載 CRX-DOCS-2.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [從 Software Distribution 下載 CRX-DOCS-2.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [從 Software Distribution 下載 CRX-DOCS-2.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [從 Software Distribution 下載 CRX-DOCS-2.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## 如何安裝說明文件套件 {#how-to-install-documentation-package}

若要安裝舊版說明文件套件，您必須安裝 [!DNL Experience Manager]，並在本機硬碟或網路硬碟上執行。

### 下載說明文件套件 {#download-documentation-package}

1. 從上表選取要下載的 [!DNL Experience Manager] 說明文件版本連結。例如 AEM 5.6.1。

1. 使用 Adobe ID 登入。如果您沒有 ID，請建立 ID。

1. 選取&#x200B;**[!UICONTROL 下載]**&#x200B;按鈕。

1. 以下是您會看到的範例：

![Software Distribution 範例](assets/screen_shot_2020-07-10at161922.jpg)

### 在本機執行個體上安裝套件 {#install-package-local-instance}

1. 開啟 [!DNL Experience Manager] 使用者介面。在網頁瀏覽器中輸入：`http://localhost:4502/`。以管理員身分登入。

1. 選取&#x200B;**[!UICONTROL 工具]** > **[!UICONTROL 部署]** > **[!UICONTROL 套件]**。

1. 在套件管理程式 UI 中，選取&#x200B;**[!UICONTROL 上傳套件]**。

1. 瀏覽至下載 AEM 5.6.1 套件 (aem-docs-5-6-1.zip) 的位置。

1. 選取該套件，然後按一下&#x200B;**[!UICONTROL 確定]**。

1. 上傳套件後，您必須加以安裝。

1. 在套件管理程式 UI 中，找到該套件並選取&#x200B;**[!UICONTROL 安裝]**。

1. 在確認對話方塊中，再次選取&#x200B;**[!UICONTROL 安裝]**。注意：安裝需要幾分鐘時間。

1. 在網頁瀏覽器中，啟動說明文件頁面。以 AEM 5.6.1 當作範例，URL 會是：http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html。

## 取得 [!DNL Experience Manager] 社群的協助 {#get-help-from-aem-community}

如果您對使用 Experience Manager 有任何疑問，建議[在 [!DNL Experience Manager] 論壇中聯絡經驗豐富的社群專家](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community)。
