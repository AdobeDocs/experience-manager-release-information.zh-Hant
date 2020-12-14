---
title: 舊版AEM、CQ和CRX
description: 舊版 Adobe Experience Manager、CQ 和 CRX 的文件套件。
translation-type: tm+mt
source-git-commit: 47b391ed659264b611f08d2fa9e45a923be5c445
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 2%

---


# 舊版[!DNL Adobe Experience Manager]、CQ和CRX {#older-versions-aem-cq-crx}

## 舊版[!DNL Experience Manager]檔案{#older-version-aem-documentation}

本頁所列的[!DNL Experience Manager]、CQ和CRX版本為生命週期結束，Adobe不再正式銷售。 我們針對這些舊版的官方檔案的最新版本，可供您自助使用。 我們建議您升級至最新版本（目前為[[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html)）。

>[!NOTE]
>
>要瞭解[!DNL Experience Manager]版本何時將到達核心支援的結束，請參閱[產品和技術支援期](https://helpx.adobe.com/support/programs/eol-matrix.html)並搜索`AEM`。

### 安裝{#before-installation}之前

在您下載套件之前，請先決定要使用內容的對象。 此決定將決定其部署方式：

* 開發人員可在本機安裝，以便快速參考。
* 如需更廣泛的組織檔案需求，建議將套件部署在內部可存取、非生產的AEM Author例項上。

>[!NOTE]
>
>使用者必須登入[!DNL Experience Manager]例項才能存取[!DNL Experience Manager]作者上的此內容。 AEM Publish預設無法存取此內容（因為它存在於/libs下）。

## 軟體分發位置{#software-distribution-locations}

您需要有效的Adobe ID:

* 如果您沒有Adobe ID，可以在www.adobe.com建立Adobe ID
如果您需要建立或管理Adobe ID的協助，請參閱本指南[](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] 版本 | 軟體分發連結 |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.1 | [從軟體散發下載AEM-DOCS-6.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-1.zip) |
| [!DNL Experience Manager] 6.0 | [從軟體散發下載AEM-DOCS-6.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [從軟體散發下載AEM-DOCS-5.6.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5.6 | [從軟體散發下載AEM-DOCS-5.6](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [從軟體散發下載CQ-DOCS-5.5](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [從軟體散發下載CQ-DOCS-5.4](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [從軟體散發下載CQ-DOCS-5.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [從軟體散發下載CRX-DOCS-2.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [從軟體散發下載CRX-DOCS-2.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [從軟體散發下載CRX-DOCS-2.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [從軟體散發下載CRX-DOCS-2.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## 如何安裝文檔軟體包{#how-to-install-documentation-package}

要安裝舊版文檔包，您必須在本地驅動器或網路驅動器上安裝並運行[!DNL Experience Manager]。

### 下載文檔軟體包{#download-documentation-package}

1. 從上表中，選擇要下載的[!DNL Experience Manager]文檔版本的連結。 例如AEM 5.6.1。

1. 使用您的Adobe ID登入。 如果您沒有ID，請建立一個。

1. 選擇&#x200B;**[!UICONTROL 下載]**&#x200B;按鈕。

1. 以下是您將看到的範例：

![軟體分發示例](assets/screen_shot_2020-07-10at161922.jpg)

### 在您的本地實例{#install-package-local-instance}上安裝軟體包

1. 開啟[!DNL Experience Manager]用戶介面。 在網頁瀏覽器中輸入：`http://localhost:4502/`。 以管理員身分登入。

1. 選擇&#x200B;**[!UICONTROL 工具]** > **[!UICONTROL 部署]** > **[!UICONTROL 軟體包]**。

1. 在「包管理器」UI中，選擇&#x200B;**[!UICONTROL 上載包]**。

1. 瀏覽至您下載AEM 5.6.1套件的位置(aem-docs-5-6-1.zip)。

1. 選擇包並按一下&#x200B;**[!UICONTROL 確定]**。

1. 在上傳套件後，您就需要安裝它。

1. 在Package Manager UI中，找到該軟體包並選擇&#x200B;**[!UICONTROL Install]**。

1. 在確認對話框上，再次選擇&#x200B;**[!UICONTROL Install]**。 注意：安裝過程需要幾分鐘的時間。

1. 在網頁瀏覽器中，啟動檔案頁面。 使用AEM 5.6.1範例，URL會是：http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html。

## 取得[!DNL Experience Manager]社群{#get-help-from-aem-community}的協助

如果您對使用Experience Manager有任何疑問，建議您[在 [!DNL Experience Manager] 論壇](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community)中與我們經驗豐富的社群專家聯絡。
