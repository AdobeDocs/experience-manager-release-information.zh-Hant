---
title: 在AEM Forms JEE上安裝Cumulative Fix Pack
description: 在AEM Forms JEE上安裝及設定Cumulative Fix Pack(CFP)的步驟摘要
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%

---


# 在AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}上安裝累積修補程式套件

## 在AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}上安裝CFP

請依照指定順序執行下列步驟，在AEM 6.3 [!DNL Forms JEE]上安裝累積修補程式套件。

1. 請聯絡[Adobe支援](https://www.adobe.com/account/sign-in.supportportal.html)以取得CFP的AEM 6.3 [!DNL Forms JEE]安裝程式。
1. 執行CFP安裝程式並依照[安裝與設定AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee)中的說明設定AEM [!DNL Forms JEE]。
1. 安裝最新的AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. 安裝AEM CFP [ 6.3.3.x](aem-forms-releases.md)的[!DNL Forms]附加套件

### 安裝AEM [!DNL Forms JEE] bundles package {#install-aem-forms-jee-bundles-package}

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1;1.0.2版)為AEM的使 [!DNL Forms] 用者提供 [!DNL Forms JEE] 與AEM相同的權限和功能 [!DNL Forms OSGi]。在「軟體包管理器」中檢查已安裝的軟體包，如果尚未安裝該軟體包，請安裝該軟體包。

### CQ-4208044 {#additional-instructions-for-cq}的其他說明

如果您正在將AEM 6.3 [!DNL Forms JEE]伺服器與Oracle資料庫搭配使用，請在部署CFP1後（即在Configuration Manager執行後）設定下列設定。 在執行企業網域同步時，必須使用此設定來同步使用者、群組和群組成員。 請參閱[AEM 6.3發行說明中的CQ-4208044期](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205)。

1. 登入&#x200B;**Admin** UI。
1. 導覽至「**[!UICONTROL 設定]** > **[!UICONTROL 使用者管理]** > **[!UICONTROL 設定]** > **[!UICONTROL 匯入與匯出設定檔]**
1. 匯出config.xml檔案。
1. 在&#x200B;*config.xml*&#x200B;中修改域配置下的&quot; `groupMemberDBQueryBatchSize`&quot;條目。 範例項目：

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. 再次匯入已修改的檔案，然後重新執行同步。

## 在AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}上安裝CFP

請依照指定順序執行下列步驟，在AEM 6.2 [!DNL Forms JEE]上安裝累積修補程式套件。

>[!NOTE]
>
>如果您使用AEM 6.2 [!DNL Forms OSGi]，請依照[AEM 6.2 CFP版本注意事項中的安裝指示進行。](release-notes-aem-6-2-cumulative-fix-pack.md)

1. 請聯絡[Adobe支援](https://www.adobe.com/account/sign-in.supportportal.html)以取得CFP的AEM 6.2 [!DNL Forms JEE]安裝程式。
1. 執行CFP安裝程式並依照[安裝與設定AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee)中的說明設定AEM [!DNL Forms JEE]。
1. 安裝[AEM Hotfix 12785 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785)版本。
1. 安裝[AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。
1. 安裝最新版[ AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md)。
1. 安裝[!DNL Forms] Add-on套件，以取得[ AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md)。

### 安裝AEM [!DNL Forms JEE] bundles package {#install-aem-forms-jee-bundles-package-1}

[AEM Forms JEE套件](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24) (aemfd-jee-bundles-package-6.2CFP5;1.0.2版)為AEM的使 [!DNL Forms] 用者提供 [!DNL Forms JEE] 與AEM相同的權限和功能 [!DNL Forms OSGi]。在「軟體包管理器」中檢查已安裝的軟體包，如果尚未安裝該軟體包，請安裝該軟體包。

### 在元件級別配置操作超時(NPR-16774){#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>在AEM 6.2 CFP4之後，您可使用下列指示來設定DSC作業的逾時，以防您在升級程式中因逾時而遇到問題。 （請參閱[AEM 6.2 CFP4發行說明](release-notes-aem-6-2-cumulative-fix-pack.md)中的NPR-16774）。

DSC部署需要變化的時間，因此可能失敗。 要更改DSC操作（如安裝、載入、啟動和停止）的超時，需要使用帶-D選項的JVM參數設定`adobe.component.registry.timeout`。

指定索引鍵的值（以秒為單位）。 例如：`-Dadobe.component.registry.timeout=300`

您也可以使用下列三個屬性，在元件層級變更逾時：

1. `adobe.all-component.timeout`:覆寫產品所有服務的逾時。
1. `adobe.<serviceName>.timeout`:覆寫僅用於索引鍵中提&lt;servicename>及之服務的逾時。如果設定了服務級別的值，則使用此命令只覆蓋指定服務的超時值（如果在應用程式級別設定）。
1. `adobe.<serviceName>.<operationName>.timeout`:它僅覆蓋特定服務操作的超時(&lt;servicename>.&lt;operationname>)。如果值設定在操作級別，則使用此命令只覆蓋指定服務的超時值（如果它設定在應用程式級別或服務級別）。

**範例：**

使用以下命令在元件級別設定超時：

1. 要將所有服務操作的超時設定為600秒：

   設定&quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. 要將`DesigntimeService`操作值超時設定為500秒，請使用：

   設定&quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. 要將`DesigntimeService's previewLCA`操作值超時設定為700秒，請使用：

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. 要將`DSC operations`（如load、install等）設定為600秒，請使用：

   設定&quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## 安裝並設定AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. 備份/deploy資料夾。 如果您決定解除安裝快速修正，則此為必要項目。
1. 停止應用程式伺服器。
1. 將修補程式安裝程式封存檔案解壓縮至硬碟。
1. 在根據您使用的作業系統命名的目錄中：

   **Windows**

   導覽至硬碟上安裝媒體或資料夾上您複製安裝程式的適當目錄：

   * （Windows 32位元）:Disk1\InstData\Windows\VM
   * （Windows 64位元）:Disk1\InstData\Windows_64bit\VM

   然後，連按兩下名為：

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe(**AEM [!DNL Forms] 6.1**)

   **Linux、Solaris、AIX**

   導覽至適當的目錄：

   * (Linux):Disk1/InstData/Linux/NoVM
   * (Solaris):Disk1/InstData/Solaris/NoVM
   * (AIX):Disk1/InstData/AIX/VM

   在命令提示符下，鍵入：

   * 。/aemforms63_cfp_install.bin(**AEM [!DNL Forms] 6.3**)
   * 。/aemforms62_cfp_install.bin(**AEM [!DNL Forms] 6.2**)
   * 。/aemforms61_cfp_install.bin(**AEM [!DNL Forms] 6.1**)

   這會啟動安裝精靈，引導您完成安裝。

1. 在「簡介」面板上，按一下「下一步」。****
1. 在「選擇安裝資料夾」畫面上，確認顯示的預設位置是否正確，或按一下「瀏覽」以選取目前安裝AEM **[!UICONTROL 的替代資料夾，然後按一下「下一步」。]**[!DNL Forms]****
1. 閱讀「快速修復補丁程式摘要」資訊，然後按一下&#x200B;**[!UICONTROL Next]**。
1. 閱讀「預安裝摘要」資訊，然後按一下&#x200B;**[!UICONTROL Install]**。
1. 安裝完成後，按一下&#x200B;**[!UICONTROL Next]**&#x200B;將快速修復更新應用於已安裝的檔案。
1. 預設情況下，「啟動配置管理器」(Start Configuration Manager)複選框處於選中狀態。 按一下&#x200B;**[!UICONTROL Done]**&#x200B;運行配置管理器。

   要稍後運行Configuration Manager，請取消選擇&#x200B;**[!UICONTROL 啟動Configuration Manager]**&#x200B;選項，然後按一下&#x200B;**[!UICONTROL Done]**。 您稍後可以使用&#x200B;*`[AEM_forms_root]`/configurationManager/bin*&#x200B;目錄中的相應指令碼啟動Configuration Manager。

1. 視您的應用程式伺服器而定，選擇下列其中一份檔案，然後依照&#x200B;*設定和部署AEM[!DNL Forms]*&#x200B;一節中的指示進行。

   如需AEM [!DNL Forms] 6.3，請參閱：

   * [安裝和部署 [!DNL Forms] AEMfor JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [安裝和部署 [!DNL Forms] AEMfor WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [安裝和部署 [!DNL Forms] AEMfor WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   如需AEM [!DNL Forms] 6.2，請參閱：

   * [安裝和部署 [!DNL Forms] AEMfor JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [安裝和部署 [!DNL Forms] AEMfor WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [安裝和部署 [!DNL Forms] AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   如需AEM Forms 6.1，請參閱：

   * [安裝和部署 [!DNL Forms] AEMfor JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [安裝和部署 [!DNL Forms] AEMfor WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [安裝和部署 [!DNL Forms] AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. 重新啟動AEM [!DNL Forms] JEE伺服器。
