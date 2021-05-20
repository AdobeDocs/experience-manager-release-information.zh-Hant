---
title: '[!DNL Experience Manager] 近期說明文件更新'
description: ' [!DNL Experience Manager]  說明文件新內容、更新或變更'
contentOwner: trushton
exl-id: 8c136a03-f961-4854-af38-45457b85d289
source-git-commit: fa68729be0642a7369e2a1bef643fac32a76bc3e
workflow-type: tm+mt
source-wordcount: '3247'
ht-degree: 100%

---

# [!DNL Experience Manager] 說明文件：近期說明文件更新 {#aem-documentation-recent-documentation-updates}

本頁列出 [!DNL Adobe Experience Manager] 的重要文件變更和更新內容。

您也可以檢視[先前說明文件更新](previous-documentation-updates.md)。

## [!DNL Adobe Experience Manager] as a [!DNL Cloud Service] {#aem-as-a-cloud-service}

>[!NOTE]
>
>AEM as a Cloud Service 每月發行說明。
>
>如需了解個別發行版 (目前和先前版本) 的相關文件，請參閱[發行說明](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=zh-Hant)。

| 日期 | 主題 | 變更 |
| --- | --- | --- |
| 2020 年 12 月 2 日 | 批次集預設集 | 了解如何使用 Dynamic Media 中的批次集預設集自動建立影像集和迴轉集。請參閱[批次集預設集](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/batch-set-presets-dm.html?lang=zh-Hant#dynamicmedia)。 |
| 2020 年 12 月 2 日 | Dynamic Media 無障礙內容 | Dynamic Media 和 Dynamic Media 檢視器支援 Authoring 使用者介面的鍵盤控制和輔助技術，例如 JAWS 和 NVDA 螢幕閱讀器。請參閱 [Dynamic Media 無障礙內容](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/accessibility-dm.html?lang=zh-Hant#dynamicmedia)。 |
| 2020 年 10 月 29 日 | 核心元件 | 核心元件 2.12.0 版推出新的 POST 表單處理常式；透過上下文感知組態包含自訂 CSS、JavaScript 和中繼資料標記；以及 **DataLayerBuilderutility** 簡化自訂元件中的資料層整合。此版本提供 [Authoring 說明文件](https://docs.adobe.com/content/help/zh-Hant/experience-manager-core-components/using/introduction.html)和[開發人員詳細資訊，並可透過 GitHub 下載專案。](https://github.com/adobe/aem-core-wcm-components) |
| 2020 年 9 月 24 日 | 新 Dynamic Media 組態的收件匣通知 | 新的 Dynamic Media 組態完成設定時，您會在 [!DNL Experience Manager] 收件匣內收到狀態通知。通知會告知您組態是否成功。如果組態失敗，通知將會提供錯誤碼。請於聯絡 Adobe Care 時使用此錯誤碼。<br>請參閱[新 Dynamic Media 組態疑難排解](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#troubleshoot-dm-config)。 |
| 2020 年 9 月 24 日 | 在 Dynamic Media 組態中重設密碼。 | 在 Dynamic Media 中允許初次使用臨時密碼和後續重設密碼，而非透過 Dynamic Media Classic。請參閱[在  [!DNL Cloud Service]s](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#configuring-dynamic-media-cloud-services)、步驟 6 和步驟 7 建立新的 Dynamic Media 組態，以及[變更 Dynamic Media 的密碼](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#change-dm-password)。 |
| 2020 年 9 月 24 日 | 在 Dynamic Media 中使用選擇性發佈 | 您可以在資料夾層級選擇使用「管理出版物」或「快速發佈」，從 [!DNL Experience Manager] 或 Dynamic Media (或以其為目標) 發佈或取消發佈資產，而非僅能依賴在 Dynamic Media 執行個體使用相同資料夾設定的 Dynamic Media 組態。<br>請參閱[在 Dynamic Media 中使用選擇性發佈](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/dynamicmedia/selective-publishing.html)。 |
| 2020 年 9 月 11 日 | 單頁應用程式 | 單次頁面應用程式 (SPA) 編輯器 JavaScript SDK [現在是開放原始碼。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/headless/spa/reference-materials.html) |
| 2020 年 8 月 27 日 | Dynamic Media 中的 CDN 失效 | 您現在可以從 Dynamic Media 傳送要求，讓 CDN 快取在數分鐘內過期。當您更新資產，並希望這些變更立即在您的網站上生效時，這項功能相當實用。<br>請參閱[透過 Dynamic Media 使 CDN 快取失效。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/dynamicmedia/invalidate-cdn-cache-dynamic-media.html) |
| 2020 年 8 月 11 日 | 發佈頁面的 On Time 和 Off Time | 當您使用 [On Time 和 Off Time](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html#basic) 發佈頁面時，請參閱「頁面屬性」的「Basic」索引標籤，您現在可以[預設自動複製。](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/replication.html?lang=zh-Hant#on-and-off-times-trigger-configuration) |
| 2020 年 7 月 23 日 | 核心元件 | 核心元件 2.11.0 版推出 AMP 支援，並且提供 [Authoring 說明文件](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html)和[開發人員詳細資訊，並可透過 GitHub 下載專案。](https://github.com/adobe/aem-core-wcm-components) |
| 2020 年 7 月 15 日 | Sling 速查表 | [Sling 速查表](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/developing/sling-cheatsheet.html)完成更新以參照 [HTL。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-htl/using/overview.html) |
| 2020 年 6 月 24 日 | 內容片段 | [說明文件已更新，目前為標準模型。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) |
| 2020 年 6 月 19 日 | [!DNL Adobe Experience Manager] | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |
| 2020 年 6 月 19 日 | 核心元件 | 核心元件 2.10.0 版推出 PDF Viewer 元件，並且提供 [Authoring 說明文件](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html)和[開發人員詳細資訊，並可透過 GitHub 下載專案。](https://github.com/adobe/aem-core-wcm-components) |
| 2020 年 6 月 4 日 | 使用 Brand Portal 設定 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] | Adobe I/O 已升級並品牌化為 Adobe Developer Console，具備全新的使用者介面和工作流程。說明文件已根據使用 Brand Portal [設定 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 的最新 Adobe Developer Console 工作流程完成更新。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) |
| 2020 年 6 月 1 日 | RTF 編輯器 (RTE) | 下列 RTF 編輯器 (RTE) 相關文章適用於 [!DNL Experience Manager] as a [!DNL Cloud Service]：<br>- [設定 RTE](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html)<br>- [設定各外掛程式](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html)<br>- [設定 RTE 以建立無障礙頁面](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/configuring-and-extending/rte-accessible-content.html)<br>- [使用 RTE 製作內容](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/sites/authoring/fundamentals/rich-text-editor.html) |
| 2020 年 5 月 29 日 | 核心元件 | 核心元件 2.9.0 版推出 Adobe Client 資料層整合與新的進度欄元件，並且提供 Authoring 說明文件和開發人員詳細資訊，並可透過 GitHub 下載專案。 |
| 2020 年 5 月 19 日 | 協助工具及 WCAG 2.1 指南 | 針對 WCAG 2.1 指南進行更新：<br>- [[!DNL Experience Manager] as a [!DNL Cloud Service] 以及網頁協助工具指南](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/onboarding/accessibility/web-accessibility.html)<br>- [WCAG 2.1 快速指南](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/onboarding/accessibility/quick-guide-wcag.html)<br>- [建立無障礙內容 (WCAG 2.1 一致性](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |
| 2020 年 5 月 4 日 | Dynamic Media 不支援的影像格式 | Dynamic Media 不支援光柵影像檔案格式子類型的相關資訊。<br>請參閱 [Dynamic Media 不支援的光柵影像格式。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/administer/assets-formats.html#unsupported-image-formats-dynamic-media) |
| 2020 年 4 月 20 日 | 內容片段 | [ [!DNL Experience Manager] Assets HTTP API 支援內容片段](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/admin/assets-api-content-fragments.html)、[自訂及擴展內容片段](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/configuring-and-extending/content-fragments-customizing.html)和[轉譯所需內容片段設定元件](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/configuring-and-extending/content-fragments-configuring-components-rendering.html)的相關資訊。 |
| 2020 年 4 月 9 日 | 使用 Brand Portal 設定 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] | [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 現在支援 Brand Portal。您可以透過 Adobe I/O 在 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 設定 Brand Portal 租戶：<br>- [設定 [!DNL Experience Manager Assets] as a [!DNL Cloud Service]  Brand Portal ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)<br>- [將資產發佈至 Brand Portal ](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/brand-portal/publish-to-brand-portal.html) |
| 2020 年 4 月 9 日 | Adobe Asset Link v2.0 已推出 | Adobe Asset Link 2.0 支援在多重[!DNL Experience Manager]環境執行作業，並針對[!DNL Experience Manager]以[!DNL Cloud Service]形式提供支援。當行銷者以 AAL 將資產上傳至資料夾時，[!DNL Experience Manager]能針對其設定自動執行資產處理工作流程的需求提供支援。<br> 請參閱 [Adobe 資產連結。](https://helpx.adobe.com/tw/enterprise/using/adobe-asset-link.html) |
| 2020 年 3 月 24 日 | 設定 Dynamic Media Cloud Service | 設定 Dynamic Media Cloud Service 的新選項：<br>**選擇性發佈** - 當選取此選項時，代表資產會發佈並僅限安全預覽，而且無須發佈至 DMS7 供公共域傳送，即可明確發佈至 [!DNL Experience Manager]。<br>請參閱[設定 Dynamic Media Cloud Service。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#configuring-dynamic-media-cloud-services) |
| 2020 年 3 月 2 日 | Dynamic Media - 智慧型裁切 | 在 Dynamic Media 元件使用智慧型裁切的新選項：<br>**啟用長寬比相符** - 選取此選項，使 Dynamic Media 透過智慧型裁切處理挑選最符合原始影像的長寬比。<br>請參閱[當您使用智慧型裁切時。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/assets/dynamicmedia/adding-dynamic-media-assets-to-pages.html#when-working-with-smart-crop) |
| 2020 年 2 月 25 日 | 角色型權限 | Cloud Manager 已預先設定角色，賦予適當權限。各角色皆擁有各自相關的特定權限、預設任務或權限。[角色權限頁面](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/onboarding/what-is-required/role-based-permissions.html)列出可用功能以及可執行此功能的角色。 |
| 2020 年 2 月 15 日 | 雲端中的 Dispatcher | 已上傳 [Dispatcher 與 CDN](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/dispatcher/overview.html#dispatcher-cdn) 和[明確 Dispatcher 快取無效](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/implementing/dispatcher/overview.html#explicit-invalidation)區段，以釐清可用選項和運作方式。 |

## [!DNL Experience Manager] 6.5 {#aem-65}

| 日期 | 主題 | 變更 |
| --- | --- | --- |
| 2021 年 3 月 11 日 | [!DNL Experience Manager] 6.5 Service Pack 8 | [[!DNL Experience Manager] 6.5 Service Pack 8](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=zh-Hant#service-pack) 可供使用。 |
| 2020 年 11 月 25 日 | Dynamic Media 無障礙內容 | Dynamic Media 和 Dynamic Media 檢視器支援 Authoring 使用者介面的鍵盤控制和輔助技術，例如 JAWS 和 NVDA 螢幕閱讀器。請參閱 [Dynamic Media 無障礙內容](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/accessibility-dm.html?lang=zh-Hant#dynamic)。 |
| 2020 年 11 月 26 日 | [!DNL Experience Manager] 6.5 Service Pack 7 | [[!DNL Experience Manager] 6.5 Service Pack 7](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html#service-pack) 可供使用。 |
| 2020 年 9 月 3 日 | Dynamic Media 中的 CDN 失效 | 您現在可以從 Dynamic Media 傳送要求，讓 CDN 快取在數分鐘內過期。當您更新資產，並希望這些變更立即在您的網站上生效時，這項功能相當實用。<br>請參閱[透過 Dynamic Media 使 CDN 快取失效。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/dynamic/invalidate-cdn-cache-dynamic-media.html) |
| 2020 年 9 月 3 日 | 在 Dynamic Media 中使用選擇性發佈 | 您可以在資料夾層級選擇使用「**管理出版物**」或「**快速發佈**」，從 [!DNL Experience Manager] 或 Dynamic Media (或以其為目標) 發佈或取消發佈資產，而非僅能依賴在 **Dynamic Media** 例項使用相同資料夾設定的 Dynamic Media 組態。<br>請參閱[在 Dynamic Media 中使用選擇性發佈](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/dynamic/selective-publishing.html)。 |
| 2020 年 9 月 3 日 | [!DNL Experience Manager] 6.5 Service Pack 6 | [[!DNL Experience Manager] 6.5 Service Pack 6](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=zh-Hant) 可供使用。 |
| 2020 年 7 月 29 日 | 多站點管理員 | [建立新同步化動作](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/developing/extending-aem/extending-msm.html#creating-a-new-synchronization-action)和[建立新轉出設定](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/developing/extending-aem/extending-msm.html#creating-a-new-rollout-configuration)程序已更新。 |
| 2020 年 7 月 15 日 | Sling 速查表 | [Sling 速查表](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/developing/platform/sling-cheatsheet.html)完成更新以參照 [HTL。](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) |
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |
| 2020 年 6 月 4 日 | 使用 Brand Portal 設定 [!DNL Experience Manager Assets] | Adobe I/O 已升級並品牌化為 Adobe Developer Console，具備全新的使用者介面和工作流程。說明文件已根據使用 Brand Portal 設定 [!DNL Experience Manager Assets] 的最新 Adobe Developer Console 工作流程完成更新：<br>- 使用 Brand Portal [設定 [!DNL Experience Manager Assets] ](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html)<br>- [將舊組態升級為 Adobe Developer Console](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| 2020 年 6 月 4 日 | [!DNL Experience Manager] 6.5 Service Pack 5 | [[!DNL Experience Manager] 6.5 Service Pack 5](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html) 可供使用。 |
| 2020 年 5 月 25 日 | 協助工具及 WCAG 2.1 指南 | 針對 WCAG 2.1 指南進行更新：<br>- [Adobe Experience Manager as a  [!DNL Cloud Service]  以及網頁協助工具指南](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/web-accessibility.html)<br>- [WCAG 2.1 快速指南](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/quick-guide-wcag.html)<br>- [建立無障礙內容 (WCAG 2.1 一致性](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |
| 2020 年 4 月 13 日 | 資產版本設定 | 已更新如何在  [!DNL Experience Manager] [建立、預覽和恢復資產版本的內容和影片。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/managing/managing-assets-touch-ui.html#asset-versioning) |
| 2020 年 4 月 13 日 | 資產處理 | 已新增處理資產相關工作流程的概覽，同時也新增說明如何[自動觸發工作流程以處理資產](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/using/assets-workflow.html)的主題。 |
| 2020 年 3 月 30 日 | Dynamic Media - 智慧型影像處理 | 已將新資訊更新至智慧型影像處理說明主題，內含描述新增的智慧型影像處理最佳化之影像資產範例。<br>請參閱[智慧型影像處理。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/dynamic/imaging-faq.html) |
| 2020 年 3 月 5 日 | [!DNL Experience Manager] 6.5 Service Pack 4 | [[!DNL Experience Manager] 6.5 Service Pack 4](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/release-notes/sp-release-notes.html) 可供使用。 |
| 2020 年 3 月 4 日 | 設定 Dynamic Media - Scene7 模式 | 位於 「工具 > Cloud Service」的 Dynamic Media 設定頁面提供「同步所有內容」的新選項。<br>請參閱[建立 Dynamic Media 組態](https://docs.adobe.com/content/help/zh-Hant/experience-manager-65/assets/dynamic/config-dms7.html#configuring-dynamic-media-cloud-services)。 |

## [!DNL Experience Manager] 6.4 {#aem-64}

| 日期 | 主題 | 變更 |
| --- | --- | --- |
| 2021 年 2 月 25 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 4 | [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 4](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/cfp-release-notes.html?lang=zh-Hant) 可供使用。 |
| 2020 年 11 月 26 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 3 | [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 3](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/cfp-release-notes.html) 可供使用。 |
| 2020 年 9 月 3 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 2 | [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 2](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/release-notes/cfp-release-notes.html) 可供使用。 |
| 2020 年 7 月 29 日 | [多站點管理員] | [建立新同步化動作](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/developing/extending-aem/extending-msm.html#creating-a-new-synchronization-action)和[建立新轉出設定](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/developing/extending-aem/extending-msm.html#creating-a-new-rollout-configuration)程序已更新。 |
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |
| 2020 年 6 月 4 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 1 | [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 1](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/cfp-release-notes.html) 可供使用。 |
| 2020 年 4 月 13 日 | 資產處理 | 已新增處理資產相關工作流程的概覽，同時也新增說明如何[自動觸發工作流程以處理資產](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/assets/using/assets-workflow.html)的主題。 |
| 2020 年 3 月 30 日 | Dynamic Media - 智慧型影像處理 | 已將新資訊更新至智慧型影像處理說明主題，內含描述新增的智慧型影像處理最佳化之影像資產範例。<br>請參閱[智慧型影像處理。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/assets/dynamic/imaging-faq.html) |
| 2020 年 3 月 5 日 | [!DNL Experience Manager] 6.4 Service Pack 8 | [[!DNL Experience Manager] 6.4 Service Pack 8](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/release-notes/sp-release-notes.html) 可供使用。 |

## [!DNL Experience Manager] 6.3 {#aem-2}

| 日期 | 主題 | 變更 |
| --- | --- | --- |
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |
| 2020 年 3 月 30 日 | Dynamic Media - 智慧型影像處理 | 新資訊已更新至智慧型影像處理說明主題。<br>請參閱[智慧型影像處理。](https://helpx.adobe.com/tw/experience-manager/6-3/assets/using/imaging-faq.html) |
| 2020 年 3 月 5 日 | [!DNL Experience Manager] 6.3.3.8 | 適用於 [!DNL Experience Manager] 6.3 的[ Cumulative Fix Pack 6.3.3.8](https://helpx.adobe.com/tw/experience-manager/release-notes--aem-6-3-cumulative-fix-pack.html) 可供使用。 |

## [!DNL Experience Manager] 6.2 {#aem-62}

| 日期 | 主題 | 變更 |
|---|---|---|
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |

## [!DNL Experience Manager] 6.1 {#aem-61}

| 日期 | 主題 | 變更 |
|---|---|---|
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |

## [!DNL Experience Manager] 桌面應用程式 {#aem-desktop-app}

| 日期 | 主題 | 變更 |
|---|---|---|
| 2020 年 8 月 27 日 | [!DNL Experience Manager] 桌面應用程式 2.0.3.2<br>[!DNL Experience Manager] 桌面應用程式支援 [!DNL Experience Manager] as a [!DNL Cloud Service]、[!DNL Experience Manager] 6.5、[!DNL Experience Manager]6.4 和 [!DNL Experience Manager] 6.3 (提供相容性套件)。 | [!DNL Experience Manager] 桌面應用程式 2.0.3.2 已開放供創作者、行銷人員和業務線使用者搭配 [!DNL Experience Manager Assets] 使用。<br>請參閱[發行說明。](https://docs.adobe.com/content/help/zh-Hant/experience-manager-desktop-app/using/release-notes.html) |

## [!DNL Experience Manager Assets Brand Portal] {#aem-assets-brand-portal}

| 日期 | 主題 | 變更 |
| --- | --- | --- |
| 2020 年 10 月 27 日 | 從 [!DNL Experience Manager Assets] Brand Portal 下載資產 | 說明文件包含下列重大更新：<br>- [改善下載體驗](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/download/brand-portal-download-assets.html)，提供簡化並提升下載速度。管理員可設定額外的下載組態，以提供符合使用者和企業需求的體驗。<br>- 現在可以從任何頁面一鍵導覽至檔案、[收藏](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/share/brand-portal-share-collection.html)和共用連結。<br>- 使用者現在可以[選取並下載特定轉譯](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets-from-asset-details-page)。可透過「資產」詳細內容頁面的「轉譯」面板新的轉譯下載選項。<br>為提升所有並行使用者的體驗，訪客使用者工作階段將逾時 15 分鐘。 |
| 2020 年 10 月 27 日 | [!DNL Experience Manager Assets] Brand Portal 2020.10.0 版本 | Brand Portal 2020.10.0 中，增強功能包括改善資產下載工作流程、新增排除轉譯選項、從「轉譯」面板直接下載、設定以供特定使用者群組存取及下載，以及可從所有 Brand Portal 頁面輕鬆導覽至檔案、收藏和共用連結。<br>- [Brand Portal 的新功能](https://docs.adobe.com/content/help/zh-Hant/experience-manager/brand-portal/using/whats-new.html)<br>- [Brand Portal 2020.10.0 發行說明](https://docs.adobe.com/content/help/zh-Hant/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
| 2020 年 9 月 3 日 | 從 [!DNL Experience Manager Assets] Brand Portal 下載資產 | Brand Portal 管理員可設定下載設定，在使用者從 Brand Portal 下載資產時提供簡化的使用者體驗。<br>說明文件包含下列重大更新：<br>- [從 Brand Portal 下載資產](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html)<br>- [加速下載指南](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/download/accelerated-download.html)<br>- [套用影像預設集](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/admin-tools/brand-portal-image-presets.html) |
| 2020 年 8 月 12 日 | [!DNL Experience Manager Assets] Brand Portal 6.4.7 版本 | Brand Portal 6.4.7 推出新功能以提升 Brand Portal 使用者資產下載和 PDF 檢視的體驗。<br>- [Brand Portal 的新功能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>- [Brand Portal 6.4.7 發行說明](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 的目標是在程式碼、說明文件和體驗上使用精準的術語。<br>因此，我們正在針對此說明文件集進行一系列的更新，未來也將持續致力於此。 |
| 2020 年 6 月 4 日 | [!DNL Experience Manager Assets] Brand Portal 6.4.6.2 版本 | Brand Portal 6.4.6.2 說明文件已根據使用 Brand Portal 設定[!DNL Experience Manager Assets]的最新 Adobe Developer Console 工作流程完成更新。此版本同時提供資產來源補充功能修正。<br>請參閱下列文章以取得詳細資訊：<br>- [使用 [!DNL Experience Manager Assets] Brand Portal 設定](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br>- [Brand Portal 6.4.6.2 發行說明](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/introduction/brand-portal-release-notes.html)<br>- [Brand Portal 的新功能](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/introduction/whats-new.html)<br>- [常見問題](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/introduction/brand-portal-faqs.html)<br>- [Brand Portal 資產來源補充](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/asset-sourcing-in-brand-portal/brand-portal-asset-sourcing.html)<br>- [Brand Portal 概觀](https://docs.adobe.com/content/help/zh-Hant/experience-manager-brand-portal/using/introduction/brand-portal.html) |
| 2020 年 4 月 9 日 | 使用 Brand Portal 設定 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] | [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 現在支援 Brand Portal。您可以透過 Adobe I/O 在 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 設定 Brand Portal 租用戶：<br>- [設定 [!DNL Assets] as a [!DNL Cloud Service]  Brand Portal ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)<br>- [將資產發佈至 Brand Portal ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/publish-to-brand-portal.html) |
| 2020 年 3 月 6 日 | 使用 Brand Portal 設定[!DNL Assets] (內部部署和託管服務) | 說明文件說明如何針對不同 Experience Manager 版本[在 Adobe I/O 使用 Brand Portal 設定 Experience Manager 資產](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)。<br>請參閱下列文章以取得詳細資訊：<br>**AEM 6.5**<br>- [使用 [!DNL Assets]  Brand Portal 設定](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br>- [升級 Adobe I/O 舊組態](https://docs.adobe.com/content/help/en/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65)<br>**AEM 6.4**<br>- [使用 [!DNL Assets]  Brand Portal 設定](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br>- [升級 Adobe I/O 舊組態](https://docs.adobe.com/content/help/zh-Hant/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64)<br>**AEM 6.3**<br>- [使用  [!DNL Assets] Brand Portal 設定](https://helpx.adobe.com/tw/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html)<br>- [升級 Adobe I/O 舊組態](https://helpx.adobe.com/tw/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| 2020 年 2 月 27 日 | [!DNL Assets] Brand Portal 6.4.6 版本 | 在 Brand Portal 6.4.6 中，[!DNL Assets] 與 Brand Portal 之間的授權通道已變更為 Adobe I/O。[!DNL Experience Manager Assets] 6.3 更新版本支援使用 Adobe I/O 設定 Brand Portal。<br>- [Brand Portal 的新功能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>- [Brand Portal 發行說明](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
