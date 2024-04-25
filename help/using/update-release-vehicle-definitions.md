---
title: 更新發行工具定義
description: 本文章詳細說明各種類型的 [!DNL Experience Manager] 版本，包括完整版本、功能套件和服務套件。
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 125bfbeb881fb86097a609d198098585f6212570
workflow-type: ht
source-wordcount: '731'
ht-degree: 100%

---

# [!DNL Experience Manager] 更新發行工具定義 {#update-release-vehicle-definitions}

本文件包含各種類型[!DNL Adobe Experience Manager]版本的詳細資訊，包括[!DNL Adobe]提供給客戶的完整版本、功能套件和服務套件。

>[!NOTE]
>
>有關[!DNL Experience Manager]更新版本的發行排程，請參閱[[!DNL Experience Manager] 更新發行藍圖](update-releases-roadmap.md)

## 完整版本 {#full-release}

| 項目 | 說明 |
|-------|------|
| 定義 | <ul> <li> 排程發行 </li> <li> 支援特定版本的升級路徑 (於發行說明定義) </li> </ul> |
| 命名 | <ul> <li> 主要版本的版本編號會依公式 X+1.Y.Z 而增加。 </li> <li> 次要版本的版本號碼會依公式 X.Y+1.Z 而增加 </li> </ul> 其中 X 代表主要版本編號，Y 代表次要版本編號，而 Z 是修補程式編號。 |
| 包含項目 | <ul> <li> 新功能 </li> <li>  改善功能 </li> <li>  錯誤修正 </li> </ul> |
| 文件 | <ul> <li> 說明文件入口網站會提供發行說明 </li> <li> 說明文件入口網站會提供功能、改善功能和錯誤修正的說明文件 </li> </ul> |
| 頻率 | 每年 |
| 可用性與安裝 | <ul> <li> 以獨立產品安裝程式的形式提供 </li> <li>  可由授權網站和託管服務取得 </li> <li> 授權網站可能需要移轉內容存放庫 </li> </ul> |
| 測試等級 | 通過完整 QA 驗證 |

## Service Pack {#service-pack}

| 項目 | 說明 |
|-----|-----|
| 定義 | <ul> <li> 排程發行 </li> <li> 當下，無法恢復 </li> </ul> |
| 命名 | <ul> <li> 修補程式版本編號為單一數字 </li> <li> 安裝完成後，將根據公式 X.Y.Z.SPx 增加已安裝發行版本編號的修補程式數字 </li> </ul> 其中 X 代表主要版本編號，Y 代表次要版本編號，而 Z 是修補程式編號。X 代表 Service Pack 編號。 |
| 包含項目 | <ul> <li> 新功能</li> <li>  改善功能 </li> <li> 錯誤修正 </li> <li> Common Interest 功能套件 (如適用) </li> </ul> |
| 文件 | <ul> <li> 說明文件入口網站提供發行說明 </li> <li> 說明文件入口網站提供功能、改善功能和錯誤修正的說明文件 </li> </ul> |
| 頻率 | 每季 |
| 可用性與安裝 | <ul> <li> 以套件形式提供 </li> <li> 在 Software Distribution 上提供</li> <li>  需要安裝現有功能 </li> </ul> |
| 測試等級 | <ul> <li> 所有修正已通過 QA 驗證 </li> <li>  自動執行以維護整體套件的健全度 </li> </ul> |

## Cumulative Fix Pack  {#cumulative-fix-pack-aem}

| 項目 | 說明 |
|-----|-----|
| 定義 | <ul> <li> 發行修正的單一傳送模型 </li> <li> 包含個別元件之內容套件的聚合器內容套件 </li> <li>  CFP 是 Hotfix 的變換版本，但並未提供任何改善功能。  </li> </ul> |
| 命名 | X.Y.Z.CFPx <br> 其中 X 代表主要版本編號，Y 代表次要版本編號，而 Z 是修補程式編號。X 代表累積 Service pack 編號。 |
| 包含項目 | CFP 是包含指定日期中所有元件修正的 Cumulative Fix Pack。例如，如果客戶套用 CFP3，則 CFP3 = CFP1 + CFP2。 |
| 文件 | 說明文件入口網站提供發行說明 |
| 頻率 | 每季 |
| 可用性與安裝 | <ul> <li> 以套件形式提供 </li> <li>  在 Software Distribution 上提供 </li> <li>  取決於最新發行的 Service Pack </li> <li>  CFP 不具相依性。客戶無需尋找/解決相依性問題。CFP 應安裝在最新發行的 Service Pack。 </li> <li>  CFP 可作為單一套件進行安裝，用於改善客戶體驗。  </li> </ul> |
| 測試等級 | 已在整合層級和回歸測試中通過 QA 驗證 |

## 覆蓋 {#overlay}

| 項目 | 詳細資料 |
|-------|--------|
| 命名 | 覆蓋-&lt;票證 ID> |
| 包含項目 | JS 或 JSP 檔案的錯誤修正 |
| 文件 | 無 |
| 頻率 | 視需求 |
| 可用性與安裝 | <ul> <li> 由[!DNL Experience Manager]客戶服務以套件形式提供  </li> <li> 不一定包含在 Service Pack 或完整版本之中 </li> </ul> |
| 測試等級 | 通過客戶服務驗證 |

## Feature Pack {#feature-pack}

| 項目 | 詳細資料 |
|--------|-----|
| 定義 | <ul> <li>Feature Pack 為附加元件功能，是透過 Service Pack 提供。如果 [!DNL Experience Manager] 版本已發行最後一個 Service Pack，Adobe 將不再提供任何功能套件。 </li> <li> FP 包含產品增強功能，已排定在後續產品發行時提供，但可能根據[!DNL Adobe's]產品管理的決定預先提供。</li> <li>  功能皆會與下一個主要版本合併，然後移植到客戶所需的 [!DNL Experience Manager] 版本 </li> <li>  Common Interest 和 GA 功能套件合併至下一個 Service Pack  </li> </ul> |
| 命名 | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| 包含項目 | <ul> <li> 新功能 </li> <li> 改善功能 </li> <li> 錯誤修正 (增量產品更新) </li> </ul> |
| 文件 | 說明文件可由 adobe.com 取得。 |
| 頻率 | 視產品區域而定 |
| 可用性與安裝 | <ul> <li>透過 Service Pack 提供 </li> <li> 在 Software Distribution 上提供。客戶透過 Software Distribution 接受 [!DNL Adobe's] 條款與條件。 </li> </ul> |
| 測試等級 | 「一般可用性」功能套件已通過 QA 驗證。 |

* 1：OAK 修正不會以單獨 Hotfix 的形式提供。然而，上述修正會包含在後續的累積 Oak Hotfix 中。如有需要，可以在最新的 COFP 之上提供診斷版本，但前提是客戶需運行最新的 COFP。診斷版本僅提供與 Hotfix 相同程度的品質保證，因此無法提供與 Cumulative Fix Pack、Service Pack 或產品發行相同等級的品質保證。最終修正將與下個 CFP 一併提供。
