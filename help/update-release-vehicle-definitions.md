---
title: 更新發行工具定義
description: 本文詳細說明各種類型的 [!DNL Experience Manager] 版本，包括完整版本、功能套件和服務套件。
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 4%

---


# [!DNL Experience Manager] 更新版本車輛定義  {#update-release-vehicle-definitions}

本檔案包含各種[!DNL Adobe Experience Manager]版本的詳細資訊，包括[!DNL Adobe]提供給客戶的完整版本、功能套件和服務套件。

>[!NOTE]
>
>有關[!DNL Experience Manager]更新版本的發行計畫，請參閱[[!DNL Experience Manager] 更新版本路線圖](update-releases-roadmap.md)

## 完整版{#full-release}

| 項目 | 說明 |
|-------|------|
| 定義 | <ul> <li> 排程發行 </li> <li> 支援特定版本的升級途徑，這些途徑在版本注意事項中定義 </li> </ul> |
| 命名 | <ul> <li> 主要版本的版本號碼會依公式X+1.Y.Z而增加。 </li> <li> 次要版本的版本號碼會根據公式X.Y+1.Z而增加 </li> </ul> 其中X是主要版本號，Y是次要版本號，Z是補丁程式號。 |
| 包含項目 | <ul> <li> 新功能 </li> <li>  改進 </li> <li>  錯誤修正 </li> </ul> |
| 文件 | <ul> <li> 檔案入口網站提供發行說明 </li> <li> 說明檔案入口網站提供功能、改進和錯誤修正的檔案 </li> </ul> |
| Cadence | 每年 |
| 可用性和安裝 | <ul> <li> 以獨立版產品安裝程式形式提供 </li> <li>  可從授權網站和受管理服務取得 </li> <li> 授權網站可能需要轉換內容存放庫 </li> </ul> |
| 測試等級 | 由QA完全驗證 |

## Service Pack {#service-pack}

| 項目 | 說明 |
|-----|-----|
| 定義 | <ul> <li> 排程發行 </li> <li> 目前，無法回滾 </li> </ul> |
| 命名 | <ul> <li> 修補程式版本號是單位數字 </li> <li> 安裝後，將根據公式X.Y.Z.SPx增加已安裝的發行版本號修補程式數 </li> </ul> 其中X是主要版本號，Y是次要版本號，Z是補丁程式號。 x是服務包號。 |
| 包含項目 | <ul> <li> 新功能</li> <li>  改進 </li> <li> 錯誤修正 </li> <li> Common Interest功能套件（如果有） </li> </ul> |
| 文件 | <ul> <li> 說明檔案入口網站上的發行說明 </li> <li> 說明檔案入口網站功能、改進和錯誤修正的檔案 </li> </ul> |
| Cadence | 每季 |
| 可用性和安裝 | <ul> <li> 以套件形式傳送 </li> <li> 適用於軟體散發</li> <li>  需要現有的功能安裝 </li> </ul> |
| 測試等級 | <ul> <li> 已驗證所有修正QA </li> <li>  使用自動執行功能，讓整個套件的健全運作 </li> </ul> |

## 累積修補程式套件{#cumulative-fix-pack-aem}

| 項目 | 說明 |
|-----|-----|
| 定義 | <ul> <li> 釋放修正的單一傳送模型 </li> <li> 包含個別元件之內容封裝的匯整器內容封裝 </li> <li>  CFP是Hotfix的轉換功能，但並未提供任何改進。  </li> </ul> |
| 命名 | X.Y.Z.CFPx <br>其中X是主要版本號，Y是次要版本號，Z是補丁程式號。 x是累積的Service Pack編號。 |
| 包含項目 | CFP是包含所有元件在指定日期之前修正的累積修補程式套件。 例如，如果客戶套用CFP3，則CFP3 = CFP1 + CFP2。 |
| 文件 | 說明檔案入口網站上的發行說明 |
| Cadence | 每季 |
| 可用性和安裝 | <ul> <li> 以套件形式傳送 </li> <li>  適用於軟體散發 </li> <li>  取決於最新發佈的Service Pack </li> <li>  CFP是自我依賴的。 客戶無需擔心尋找／解決相依性。 CFP應安裝在最新發行的Service Pack。 </li> <li>  CFP可以安裝為單一套件，以改善客戶體驗。  </li> </ul> |
| 測試等級 | QA已在整合層級和回歸測試中驗證 |

## 覆蓋 {#overlay}

| 項目 | 詳細資料 |
|-------|--------|
| 命名 | overlay-&lt;票證ID> |
| 包含項目 | JS或JSP檔案的錯誤修正 |
| 文件 | 無 |
| Cadence | 視需要 |
| 可用性和安裝 | <ul> <li> 由[!DNL Experience Manager]客戶服務以包裹形式提供  </li> <li> Service Pack或完整版不一定包含在內 </li> </ul> |
| 測試等級 | 經客戶服務驗證 |

## 功能套件{#feature-pack}

| 項目 | 詳細資料 |
|--------|-----|
| 定義 | <ul> <li>功能包是附加功能，並通過Service Pack提供。 如果[!DNL Experience Manager]版本已發行其最後一個Service Pack,Adobe將來不會提供任何功能套件。 </li> <li> FP包含產品增強功能，已排定在後續產品發行時提供，但是會根據[!DNL Adobe's]產品管理的決定提前提供。</li> <li>  功能總是與下一個主要版本合併，然後移植到客戶所需的[!DNL Experience Manager]版本 </li> <li>  Common Interest和GA功能包合併到下一個Service Pack中  </li> </ul> |
| 命名 | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| 包含項目 | <ul> <li> 新功能 </li> <li> 改進 </li> <li> 錯誤修正（增量產品更新） </li> </ul> |
| 文件 | 檔案可在adobe.com上取得。 |
| Cadence | 視產品區域而定 |
| 可用性和安裝 | <ul> <li>通過Service Pack提供 </li> <li> 可在軟體散發中取得。 客戶接受[!DNL Adobe's]「軟體散發條款」。 </li> </ul> |
| 測試等級 | 「一般可用性」功能包已通過QA驗證。 |

* 1:OAK修正不會以個別Hotfix的形式提供。 不過，這些修補程式會包含在後續的Cumulative Oak Hotfix中。 如有必要，可以在最新COFP之上提供診斷版本。 前提是客戶擁有最新的COFP運行。 診斷構建版本僅提供與Hot Fix相同的級別品質保證。 因此，它們無法提供與累積修補程式套件、服務套件或產品發行相同等級的品質保證。 最終修正方案將隨下一個CFP提供。
