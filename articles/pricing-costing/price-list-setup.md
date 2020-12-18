---
title: 設定價目表
description: 本主題提供有關如何設定成本及銷售價目表的資訊。
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 000c22944b187b6250f2e982d73020028093fde6
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180219"
---
# <a name="set-up-price-lists"></a>設定價目表

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 中的價目表代表費率的目錄。 費率表示成本、銷售及帳單費率。 根據價目表所表示的是成本費率還是銷售及帳單費率而定，價目表的內容與 **銷售** 或 **成本** 相關。

下列擴充功能是 Project Operations 的專屬功能，並且套用至 Dynamics 365 Sales 的價目表。

- **內容**：此欄位支援的值有 **成本** 和 **銷售**。 不支援執 **購買** 這個值。 將 [內容] 設定為 **成本** 以建立成本價目表，或是將 [內容] 設定為 **銷售** 以建立銷售價目表。 成本價目表會在估計值和實際值記錄的成本類型上解析價格。 銷售價目表會在未開單和已開單銷售類型的估計及實際記錄上解析價格。
- **時間單位**：這是價目表相關 **角色價格** 表格中所設定價格的預設時間單位。
- **價目表實體**：此隱藏欄位由 Project Operations 用來將報價或合約特定的價目表與標準及全域適用的價目表區分開來。

## <a name="price-list-header"></a>價目表標題

下表包含 Project Operations 在價目表的 **一般** 索引標籤上獨有的欄位，或在行為上有不同於 Sales 價目表之重大變更的欄位。

| 欄位 | 地點 | 描述 | 下游影響 |
| --- | --- | --- | --- |
| 名字 | **一般** 索引標籤和 **快速建立** 表單 | 價目表的識別碼。 | 價目表會在所有清單頁面和下拉式選項與此值一起顯示。|
| 內容 | **一般** 索引標籤和 **快速建立** 表單 | 此欄位可以設定為 **成本** 或 **銷售**。 | 設定為 **成本** 的價目表會用來查詢成本估計值和成本實際值的價格。 設定為 **銷售** 的價目表會用來查詢銷售估計值和銷售實際值的價格。 只有其內容設定為 **銷售** 的價目表，才能附加至客戶、專案報價及專案合約的專案價目表。 |
| 開始日期 | **一般** 索引標籤和 **快速建立** 表單 | 價目表生效期間的開始日期。 | 使用 **結束日期** 欄位時，此欄位是用來判斷哪個價目表適用於特定估計或實際明細。 |
| 結束日期 | **一般** 索引標籤和 **快速建立** 表單 | 價目表生效期間的結束日期。 | 使用 **開始日期** 欄位時，此欄位是用來判斷哪個價目表適用於特定估計或實際明細。 |
| 貨幣 | **一般** 索引標籤和 **快速建立** 表單 | 此欄位會在每個與此價目表相關的角色、類別或價目表項目明細上用來設定預設貨幣。 | 在 **銷售** 價目表上，無法使用者此貨幣以外的任何貨幣來建立角色、類別或價目表項目明細。 在 **成本** 價目表中，您可以使用任何貨幣來建立角色價格明細。 這裡所定義的貨幣會用作預設值。 與角色價格相關的使用者設定可以覆寫此值，以使用任何貨幣來啟用人力成本費率設定。 類別成本費率和價目表項目成本只能使用這裡定義的貨幣來進行設定。 |
| 時間單位 | **一般** 索引標籤和 **快速建立** 表單 | 此欄位會在每個與此價目表相關的角色明細上用來設定預設時間單位。 | 只有在相關的角色價格設定中，才能使用此欄位值。 在 **成本** 和 **銷售** 價目表中，您可以使用任何時間單位來建立角色價格明細。 這裡所定義的時間單位會用作預設值。 使用者設定相關的角色價格可以覆寫此值，以使用任何時間單位來啟用人力成本及帳單費率設定。 |
| 描述 | **一般** 索引標籤和 **快速建立** 表單 | 此文字欄位可讓您提供價目表的多行描述。 | 此欄位會在具有相關價目表的各種實體中顯示於價目表的 **相關** 檢視表。 |