---
title: Installing Cumulative Fix Packs on AEM Forms JEE
description: 在 AEM Forms JEE 上安裝和設定 Cumulative Fix Pack (CFP) 步驟摘要
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 5a549a95acf4d1b78b9040411c9e1720911afeb9
workflow-type: ht
source-wordcount: '910'
ht-degree: 100%

---

# 在 AEM[!DNL  Forms] JEE 上安裝 Cumulative Fix Pack{#installing-cumulative-fix-packs-on-aem-forms-jee}

## 在 AEM 6.3 [!DNL Forms JEE] 上安裝 CFP  {#install-cfp-forms-6-3}

若要在 AEM 6.3 [!DNL Forms JEE] 上安裝 Cumulative Fix Pack，以下列順序執行步驟。

1. 若要取得 AEM 6.3 [!DNL Forms JEE] 安裝程式以安裝 CFP，請聯絡 [Adobe 支援](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support)。
1. 執行 CFP 安裝程式，依照[安裝和設定 AEM  [!DNL Forms JEE]](#install-and-configure-aem-forms-jee) 中所述設定 AEM [!DNL Forms JEE]。
1. 安裝最新的 AEM CFP 6.3.3.x
1. 安裝適用於 AEM CFP [6.3.3.x](aem-forms-releases.md) 的 [!DNL Forms] 附加元件套件

### 安裝 AEM [!DNL Forms JEE] 套件組合套件 {#install-aem-forms-jee-bundles-package}

AEM[!DNL  Forms JEE] 套件 (aemfd-jee-bundles-package-6.3CFP1；1.0.2 版) 為 AEM [!DNL Forms] 的 [!DNL Forms JEE] 使用者，提供與 AEM [!DNL Forms OSGi] 上相同的權限和功能。在 Package Manager 中查看已安裝的套件，且若尚未安裝該套件，請加以安裝。

### CQ-4208044 的其他說明 {#additional-instructions-for-cq}

如果您搭配 Oracle 資料庫使用 AEM 6.3 [!DNL Forms JEE] 伺服器，請在部署 CFP1 後 (即在執行 Configuration Manager 後) 設定下列設定。在執行企業網域同步時，必須使用此設定來同步使用者、群組和群組成員。

1. 登入 **管理員** UI。
1. 導覽至 **[!UICONTROL 設定]** > **[!UICONTROL 使用者管理]** > **[!UICONTROL 設定]** > **[!UICONTROL 匯入與匯出設定檔]**
1. 匯出 config.xml 檔案。
1. 在 *config.xml* 修改網域設定中的「`groupMemberDBQueryBatchSize`」項目。範例項目：

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. 再次匯入修改的檔案，然後重新執行同步。

## 在 AEM 6.2 [!DNL  Forms JEE] 上安裝 CFP  {#install-cfp-on-aem-62-forms-jee}

若要在 AEM 6.2 [!DNL Forms JEE] 上安裝 Cumulative Fix Pack，以下列順序執行步驟。

1. 若要取得 AEM 6.2 [!DNL Forms JEE] 安裝程式以安裝 CFP，請聯絡 [Adobe 支援](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support)。
1. 執行 CFP 安裝程式，依照[安裝和設定 AEM  [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee) 中所述設定 AEM [!DNL Forms JEE]。
1. 安裝 AEM Hotfix 12785 7.0 版。
1. 安裝 AEM 6.2 Service Pack 1。
1. 安裝最新的 release-notes-aem-6-2-cumulative-fix-pack.md。
1. 安裝適用於 AEM 6.2 Service Pack 1 CFP 的 [!DNL Forms] 附加元件套件。

### 安裝 AEM [!DNL Forms JEE] 套件組合套件 {#install-aem-forms-jee-bundles-package-1}

AEM Forms JEE 套件 (aemfd-jee-bundles-package-6.2CFP5；1.0.2 版) 會為 AEM [!DNL Forms] 的 [!DNL Forms JEE] 使用者提供在與 AEM [!DNL Forms OSGi] 上相同的權限和功能。在 Package Manager 中查看已安裝的套件，且若尚未安裝該套件，請加以安裝。

### 為元件層級操作設定逾時 (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>在安裝 AEM 6.2 CFP4 後，您可透過下列說明為 DSC 操作設定逾時，以防在升級程序中因逾時遇到問題。

DSC 部署因可能失敗，所花時間不一定。若要變更 DSC 操作 (如安裝、載入、啟動和停止) 的逾時，必須使用具「-D」選項的 JVM 引數設定 `adobe.component.registry.timeout`。

以秒為單位指定機碼的值。例如：`-Dadobe.component.registry.timeout=300`

您也可以使用下列三個屬性，在元件層級變更逾時：

1. `adobe.all-component.timeout`：覆寫產品所有服務的逾時。
1. `adobe.<serviceName>.timeout`：僅覆寫機碼中提及之服務 (&lt;serviceName>) 的逾時。如果已設定服務層級的值，則使用此命令只會覆寫指定服務的逾時值 (如果在應用程式層級設定)。
1. `adobe.<serviceName>.<operationName>.timeout`：僅覆寫機碼中提及之特定服務操作 (&lt;serviceName>.&lt;operationName>) 的逾時。如果在操作層級設定值，則使用此命令只會覆寫指定服務的逾時值 (如果在應用程式層級或服務層級設定)。

**範例：**

使用下列命令在元件層級設定逾時：

1. 若要將所有服務操作的逾時設定為 600 秒：

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. 若要將 `DesigntimeService` 操作值逾時設定為 500 秒，請使用：

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. 若要將 `DesigntimeService's previewLCA` 操作值逾時設定為 700 秒，請使用：

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. 若要將 `DSC operations` (例如載入和安裝) 設定為 600 秒，請使用：

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## 安裝與設定 AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. 備份 /deploy 檔案夾。如果決定解除安裝快速修正，則此為必要操作。
1. 停止應用程式伺服器。
1. 將修補程式安裝程式封存檔案解壓縮至硬碟。
1. 在根據您使用的作業系統命名的目錄中：

   **Windows**

   在您複製安裝程式的硬碟上，導覽至安裝媒體或檔案夾的相關目錄：

   * (Windows 32 位元)：Disk1\InstData\Windows\VM
   * (Windows 64 位元)：Disk1\InstData\Windows_64bit\VM

   接著，按兩下以下名稱的檔案：

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®、Solaris™、AIX®**

   導覽至相關目錄：

   * (Linux®)：Disk1/InstData/Linux/ NoVM
   * (Solaris™)：Disk1/InstData/Solaris/ NoVM
   * (AIX®)：Disk1/InstData/AIX/VM

   在命令提示字元輸入：

   * 。/aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * 。/aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * 。/aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   系統會啟動安裝精靈，引導您完成安裝。

1. 在 Introduction 面板上，按一下 **[!UICONTROL Next]**。
1. 在 Choose Install Folder 畫面中，確認針對現有安裝顯示的預設位置是否正確，或按一下 **[!UICONTROL Browse]** 以選取安裝 AEM [!DNL Forms] 的替代檔案夾，然後按一下 **[!UICONTROL Next]**。
1. 閱讀 Quick Fix Patch Summary 資訊，然後按一下 **[!UICONTROL Next]**。
1. 閱讀 Pre-Installation Summary 資訊，然後按一下 **[!UICONTROL Install]**。
1. 安裝後，按一下 **[!UICONTROL Next]**，將快速修正更新套用至已安裝的檔案。
1. 預設會選取 Start Configuration Manager 核取方塊。按一下 **[!UICONTROL Done]**，執行 Configuration Manager。

   若要稍後執行 Configuration Manager，請取消選取 **[!UICONTROL Start Configuration Manager]** 選項，再按一下 **[!UICONTROL Done]**。您稍後可以使用 *`[AEM_forms_root]`/configurationManager/bin* 目錄中的適當指令碼，啟動 Configuration Manager。

1. 視您的應用程式伺服器而定，選擇下列其中一份文件，然後依照&#x200B;*設定和部署 AEM[!DNL Forms]* 一節中的說明操作。

   若為 AEM [!DNL Forms] 6.3，請參閱：

   * 安裝和部署 AEM [!DNL Forms] for JBoss®
   * 安裝和部署 AEM [!DNL Forms] for WebSphere®
   * 安裝和部署 AEM [!DNL Forms] for WebLogic

1. 重新啟動 AEM [!DNL Forms] JEE 伺服器。
