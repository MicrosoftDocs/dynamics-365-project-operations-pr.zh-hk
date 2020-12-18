---
title: 管理預估發票
description: 此主題提供有關如何管理和使用預估發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f3aab57f159dbb522ebe5d24dc3693034f6f81f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181479"
---
# <a name="manage-a-proforma-invoice"></a>管理預估發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

在 Dynamics 365 Project Operations 中，預估發票是建立為 Dynamics 365 Sales 中的發票延伸。 但是，在開立發票時，Sales 與 Project Operations 之間的開立發票程序有許多不同的差別。 例如，無法從 Project Operations 的 **發票清單** 頁面建立新的發票，但是可以在 Sales 中進行此作業。 這些差異和擴充功能已到位，可支援與銷售訂單之一般發票不同的專案的開立發票程序。

> [!IMPORTANT]
> 因為這些差異，請勿在 Sales 與 Project Operations 間交替使用發票。

## <a name="invoice-header"></a>發票標題

您可以在 Project Operations 的預估發票標題上使用下列資訊。

| 欄位 | 地點 | 描述 | 下游影響 |
| --- | --- | --- | --- |
| **發票識別碼** | **摘要** 索引標籤 | 識別碼會在預估發票建立時自動產生。 鎖定無法編輯的唯讀欄位。 | 此欄位是做為每個預估發票的參考。 |
| **名稱** | **摘要** 索引標籤 | 預設設定為專案合約的名稱。 使用者可以編輯此欄位。 | &nbsp;  |
| **貨幣** | **摘要** 索引標籤 | 預設設定為專案合約的貨幣。 鎖定無法編輯的唯讀欄位。 |&nbsp; |
| **價目表** | **摘要** 索引標籤 | 預設設定為專案合約的價目表。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **商機** | **摘要** 索引標籤 | 連結商機的參考。 鎖定無法編輯的唯讀欄位。 | &nbsp;  |
| **合約** | **摘要** 索引標籤 | 連結專案合約的參考。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **客戶** | **摘要** 索引標籤 | 連結專案合約的參考。 鎖定無法編輯的唯讀欄位。 |&nbsp;  |
| **描述** | **摘要** 索引標籤 | 描述發票的文字欄位。 使用者可以編輯此欄位。 | &nbsp; |
| **帳單地址** 與相關欄位 | **摘要索引標籤** | 預設值是從專案合約客戶處進行設定。 使用者可以編輯此欄位。  | &nbsp; |
| **狀態** | **摘要** 索引標籤 | 設定下列選項：**使用中**、**已關閉**、**已支付** 和 **已取消**，且可由使用者編輯。 | Project Operations 不支援的狀態包括 **已關閉** 和 **已取消**。 </br> 在建立發票時，狀態會設定為 **使用中**。 </br>只有在確認發票後，才會將狀態設定為 **已付費**。 |
| **專案發票狀態** | **摘要** 索引標籤 | 設定下列選項：**草稿**、**檢閱中** 和 **已確認**，且可由使用者編輯。 | 在 **草稿** 和 **檢閱中** 狀態，可以編輯發票。 發票確認後就無法再編輯。 |
| **明細總金額** | **摘要** 索引標籤 | 預付金和扣除額後所有發票明細上的金額總和。 鎖定無法編輯的唯讀欄位。 | 此欄位是用來計算最終金額。 |
| **折扣 (%)** | **摘要** 索引標籤 | 您可以編輯此欄位，以輸入折扣百分比。 Project Operations 功能不支援此欄位。 | 這是不受支援的欄位。 |
| **折扣金額** | **摘要** 索引標籤 | 您可以編輯此欄位，以輸入折扣金額。 Project Operations 功能不支援此欄位。 | 這是不受支援的欄位。 |
| **折扣後金額** | **摘要索引標籤** | 套用折扣後的發票總金額。 鎖定無法編輯的唯讀欄位。 | 此欄位是用來計算最終金額。 |
| **運費金額** | **摘要** 索引標籤 | 您可以編輯此欄位，以輸入運費金額。 Project Operations 功能不支援此欄位。 | 這是不受支援的欄位。 |
| **稅金總計** | **摘要** 索引標籤 | 發票上所有發票明細的稅金總計。 鎖定無法編輯的唯讀欄位。 | 無。 |
| **總計金額** | **摘要** 索引標籤 | 折扣和稅金後的金額總和。 | 總和是指客戶需要支付的金額。 |

## <a name="project-based-invoice-lines"></a>專案型發票明細

在 Project Operations 中，每個專案合約服務內容一律有一個發票明細。 即使沒有實際值，也會建立發票明細。 您可以在預估發票明細上使用下列資訊。

| 欄位 | 地點 | 描述 | 下游影響 |
| --- | --- | --- | --- |
| **發票識別碼** | **一般** 索引標籤 | 發票識別碼的參考。 鎖定無法編輯的唯讀欄位。 | 發票識別碼連結可以用來瀏覽回發票標題。 |
| **名稱** | **一般** 索引標籤 | 預設從合約服務內容名稱設定的發票明細名稱。 使用者可以編輯此欄位。 | &nbsp; |
| **Project** | **一般** 索引標籤 | 相關專案合約服務內容上的專案。 鎖定無法編輯的唯讀欄位。 | 專案連結可以用來瀏覽至專案。 |
| **計費方式** | **一般** 索引標籤 | 相關專案合約服務內容上的計費方式。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **合約服務內容金額** | **一般** 索引標籤 | 相關專案合約服務內容上的合約金額。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **至當日為止已開立發票** | **一般** 索引標籤 | 此發票的所有發票明細詳細資料上的金額總和。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **金額** | **一般** 索引標籤 | 此發票的所有應收費發票明細詳細資料上的金額總和。 鎖定無法編輯的唯讀欄位。 | 此欄位是用來計算發票標題上的最終金額。 |
| **稅金** | **一般** 索引標籤 | 此發票明細的所有發票明細詳細資料上的稅額總和。 鎖定無法編輯的唯讀欄位。 | 此欄位是用來計算發票標題上的最終稅額。 |
| **應收金額** | **一般** 索引標籤 | 此發票明細的所有應收費發票明細詳細資料上的總金額 (**稅金 + 金額**)。 鎖定無法編輯的唯讀欄位。 | 此欄位是用來計算發票標題上的最終金額。 |

## <a name="invoice-line-details"></a>發票明細詳細資料

專案發票中的每個發票明細均包含發票明細詳細資料。 這些明細詳細資料與發票明細所參考之合約服務內容相關的未開單銷售實際值與里程碑有關。 所有這些交易都會標示 **已準備好開立發票**。

對於 **時間和資料發票** 明細，發票明細詳細資料會在 **發票明細** 頁面上分組為 **應收費**、**不應收費** 和 **附贈**。 **應收費發票明細** 詳細資料會加總至發票明細總計。 **附贈** 和 **不應收費實際值** 不會加總到發票明細總計。

在 **固定價格發票** 明細中，發票明細詳細資料是由在相關合約服務內容上標示為 **已準備好開立發票** 的里程碑所建立。 從里程碑建立發票明細詳細資料後，里程碑的帳單狀態會更新為 **客戶發票已建立**。

### <a name="edit-invoice-line-details"></a>編輯發票明細詳細資料

下欄欄位可用於根據未開單銷售實際值所產生的發票明細詳細資料。

| 欄位 | 描述 | 下游影響 |
| --- | --- | --- |
| **發票明細** | **發票明細識別碼** 的參考。 唯讀欄位，鎖定無法編輯。 | 此連結可用來瀏覽回發票標題。 |
| **描述** | 發票明細詳細資料的描述。 預設從 **時間項目** 的 **內部留言** 欄位以及從 **費用項目** 的 **描述** 欄位進行設定。 使用者可以編輯此欄位。| &nbsp; |
| **外部描述** | 發票明細詳細資料的描述。 預設從 **時間項目** 的 **外部留言** 欄位以及 **費用項目** 的 **描述** 欄位進行設定。 使用者可以編輯此欄位。 | 此描述可用於判斷要傳送給客戶之列印發票上的內容。 在 Project Operations 中，預估發票不具備設定發票列印設定的所有必要功能。 |
| **開始日期** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 |
| **Project** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 預設設定為相關合約服務內容上的專案。 |
| **工作** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 下拉式清單會顯示與相關專案合約服務內容相關聯的所有工作。  |
| **交易類別** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由實際來源所產生的新發票明細詳細資料中編輯此欄位。 |
| **角色** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 |
| **可預約資源** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由實際來源所產生的新發票明細詳細資料中編輯此欄位。 |
| **資源供應公司** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 |
| **資源分配單位** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 |
| **數量** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 |
| **單位排程** | 對於時間的發票明細詳細資料，這通常是設定為時間而且不可以編輯。 如果是費用，則預設根據來源費用實際值設定。 鎖定無法編輯的唯讀欄位。 | 在不是由實際值所產生的新發票明細詳細資料上，預設設定為 **時間**。 |
| **單位** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位 |
| **價格** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 您可以在不是由來源實際值所產生的新發票明細詳細資料中編輯此欄位。 如果未輸入任何值，則預設會在 **儲存** 後設定。 |
| **貨幣** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 在沒有實際支援下建立新的發票詳細資料時，預設會從發票標題設定。  鎖定無法編輯的唯讀欄位。 |
| **金額** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 在沒有實際支援下建立新的發票詳細資料時，會計算為 **數量\*價格**。 會在 **儲存** 後計算。 鎖定無法編輯的唯讀欄位。 |
| **稅金** | 預設會根據來源實際值設定。 使用者可以編輯此欄位 | 在沒有實際支援下建立新的發票詳細資料時，使用者可以編輯此欄位。 |
| **應收金額** | 計算為 **金額 + 稅金** 的導出欄位。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **帳單類型** | 預設會根據來源實際值設定。 使用者可以編輯此欄位。 | 選取 **應收費** 會將明細加總至發票明細總計。 **附贈** 和 **不應收費** 將從發票明細總計中排除它。 |
| **交易類型** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 在沒有實際支援下建立新的 **發票明細詳細資料** 時，預設會設定為 **開單銷售** 並鎖定。  |
| **交易類別** | 預設會根據來源實際值設定。 鎖定無法編輯的唯讀欄位。 | 根據使用者是選擇建立 **時間**、**費用** 還是 **服務費** 發票明細詳細資料，以及同時在沒有實際支援下建立新的 **發票明細詳細資料** 時，預設設定。 鎖定無法編輯。 |

下欄欄位可用於根據里程碑所產生的發票明細詳細資料：

| 欄位 | 描述 | 下游影響 |
| --- | --- | --- |
| **發票明細** | **發票明細識別碼** 的參考。 鎖定無法編輯的唯讀欄位。 | 連結可用來瀏覽回發票標題。 |
| **描述** | 發票明細詳細資料的描述。 預設根據來源里程碑的描述設定。 | &nbsp; |
|**外部描述** | 預設會從來源里程碑的描述中設定的發票明細詳細資料描述。 | 此欄位可用於判斷要傳送給客戶之列印發票上的內容。 Project Operations 中的預估發票不具備設定發票列印設定的所有必要功能。 |
| **開始日期** | 預設根據來源里程碑上的 **里程碑** 日期設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **Project** | 預設會根據來源里程碑設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **工作** | 預設會根據來源里程碑設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **交易類別** | 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **角色** | 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **可預約資源** | 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **資源分配單位** | 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **單位排程** | 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **單位** | 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **價格** | 預設根據來源里程碑的金額設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **貨幣** | 預設會根據來源里程碑設定。 鎖定無法編輯的唯讀欄位。 |&nbsp; |
| **金額** | 預設根據來源里程碑的金額設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **稅金** | 預設根據來源里程碑的稅額設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **應收金額** | 預設根據來源里程碑的應收金額設定。 使用者可以編輯此欄位 | &nbsp; |
| **帳單類型** | 預設一律設定為 **應收費**。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **交易類型** | 預設會根據來源里程碑設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |
| **交易類別** | 預設會根據來源里程碑設定。 鎖定無法編輯的唯讀欄位。 | &nbsp; |

## <a name="refresh-invoice-transactions"></a>重新整理發票交易

如果在建立發票後有實際值，則可以在發票上包括這些實際值。

1. 在 **帳務積存檢視** 中，將資料標記為 **已準備好開立發票**。   
2. 開啟草稿預估發票，並在功能區 **動作** 上，按一下 **重新整理發票明細交易**。

  這會為任何已過期並標示為 **已準備好開立發票** 的實際值建立發票明細詳細資料，但不會包括在發票中。