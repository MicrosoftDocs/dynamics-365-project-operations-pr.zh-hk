---
title: 估計專案型合約服務內容
description: 本主題提供有關專案型合約服務內容估計值的資訊。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180489"
---
# <a name="estimate-a-projectbased-contract-line"></a>估計專案型合約服務內容

_**適用於：** 資源/非庫存型案例適用的 Project Operations_ 

在 Dynamics 365 Project Operations 中，專案型合約服務內容會有可協助估計交付合約服務內容所需工作之成本及可能營收的詳細資訊。

若要估計專案型合約服務內容，請移至專案型 **合約服務內容** 上的 **合約服務內容詳細資料** 索引標籤。  有兩種可在專案型合約服務內容中建立估計值的方式：

   - 手動新增合約服務內容詳細資料，以直接在合約服務內容上建立估計值。
   - 建立專案及專案計劃，然後將專案及工作關聯至專案的合約服務內容。 這樣會啟用可藉以根據合約服務內容所含元件將專案計劃估計值匯入至合約服務內容的程序。

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>直接在專案型合約服務內容中建立估計值

1. 移至合約服務內容，並選取 **合約服務內容詳細資料** 索引標籤。您在此索引標籤上建立的明細將會合計起來，並顯示為此 **合約服務內容** 的 **合約值**。 
2. 在 **合約服務內容詳細資料** 子格中，選取 **+ 新增合約服務內容詳細資料**。 快速建立滑桿隨即開啟。 **合約服務內容詳細資料** 表單中會有下列欄位：

| 欄位 | 地點 | 描述 | 下游影響 |
| --- | --- | --- | --- |
| **描述** | **快速建立** | 特定估計值的描述。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **交易類別** | **快速建立** | 此下拉式清單是專案型合約服務內容的 **一般** 索引標籤中所包含的交易分類清單。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **角色** | **快速建立** | 執行此工作或產生此費用之人員的角色。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **類別** | **快速建立** | 工作或費用的類別。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **開始日期** | **快速建立** | 工作的開始日期。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **結束日期** | **快速建立** | 工作的結束日期。 | 此欄位會預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **資源供應公司** | **快速建立** | 要承擔此成本並提供資源進行處理的資源供應公司或法律實體。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 此欄位也會用於成本價擷取。 |
| **資源分配單位** | **快速建立** | 承擔此成本並提供資源進行處理的資源分配單位。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 此欄位也會用於成本價擷取。 |
| **單位排程** | **快速建立** | 工作或費用的單位群組。 屬於單位排程或單位群組的單位。 例如，*英里* 和 *公里 (Km)* 是屬於描述距離之單位群組的單位。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **單位** | **快速建立** | 工作或費用的單位。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **數量** | **快速建立** | 工作或費用的數量。 | 此欄位預設為自動建立之成本的相關合約服務內容詳細資料。 |
| **單價** | **快速建立** | 執行工作之角色的帳單費率或費用類別的銷售價。 此欄位的預設值是以開始日期生效之專案價目表中角色與資源分配單位組合為根據的 **時間**。 對於費用，此欄位的預設值來自從開始日期生效之專案價目表中交易類別的價格設定。 如果交易類別的定價方式不是 **單價**，就沒有預設值，且此欄位保留空白。 | 執行工作之角色的成本費率或費用類別的單位成本。 已附加至合約單位且從開始日期生效之成本價目表的角色價格明細上的 **以角色為根據的時間** 與資源分配單位組合預設會使用此欄位。 對於費用，此欄位的預設值是根據已附加至合約單位且從開始日期生效之成本價目表的類別價格明細而定。 如果交易類別的定價方式不是單價，就沒有預設值，且此欄位保留空白。 |
| **估計稅額** | **快速建立** | 使用者所輸入此工作或費用的估計稅金。 | 使用者所輸入此工作或費用的估計稅金。 |
| **金額** | **快速建立** | 如果讓 **數量** 和 **價格** 欄位保留空白，則可由使用者在此欄位中新增此值。 如果已填入 **數量** 和 **價格**，則 **金額** 欄位為唯讀，並以 **(數量 \* 單價) + 稅金** 來計算。 | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>更新合約服務內容詳細資料上的價格

如果您在附加至合約的專案價目表或合約單位的成本價目表上變更價格，則可以重新整理個別合約服務內容詳細資料的價格，以反映此變更。 在 **合約** 頁面上，選取 **重新計算**。 警告會開啟，通知您此合約上所有合約服務內容的價格都會重設。 選取 **是** 以重新整理銷售及成本合約服務內容詳細資料的價格。

## <a name="access-contract-line-details-for-cost"></a>存取成本的合約服務內容詳細資料

在 **合約服務內容詳細資料** 索引標籤上，選取網格中的一列，以顯示子格工具列中的動作。 子格工具列上的第一個動作會是 **開啟成本詳細資料**。 若要查看此合約服務內容詳細資料的相關成本費率及金額，請選取 **開啟成本詳細資料**。 

> [!NOTE]
> 在 **成本** 的合約服務內容詳細資料上變更資源供應公司、資源分配單位、數量、日期、角色或類別值，也會在 **銷售** 的合約服務內容詳細資料上變更對應的值。

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>成本及銷售合約服務內容詳細資料上的貨幣

**銷售** 合約服務內容詳細資料會透過從合約服務內容詳細資料之開始日期生效的專案價目表來設定預設貨幣。

**成本** 合約服務內容詳細資料會透過從 **成本** 合約服務內容詳細資料開始日期生效之合約的合約單位價目表來設定預設貨幣。

獲利率計算會將 **成本** 及 **銷售** 的合約服務內容詳細資料金額轉換為環境的基準貨幣，以便報告合約上的總實際利潤和估計利潤。

> [!NOTE]
> 貨幣捨入錯誤和變動利潤可能會因為缺少即日有效的匯率而發生。 使用這些計算僅做為專案合約上的近似值，而不要將其用於實際法定報告或其他需要更高捨入精確度及匯率日期時效性感知的報告。