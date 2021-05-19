---
title: 2021 年 4 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 2021 年 4 月所發行 Project Operations 精簡部署中提供之品質更新的資訊。
author: sigitac
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd6fbe8d75fbe9157a97d2edd38d40a97395c924
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868065"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>2021 年 4 月新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

  - Dataverse 環境的 Project Operations 版本 4.9.0.221 

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- 專案的非庫存材料。 主要功能包括：
  - 對專案銷售週期期間的非庫存材料進行估計和定價。 如需詳細資訊，請參閱[設定產品類別目錄產品的成本及銷售費率 - 精簡](../pricing-costing/set-up-cost-sales-rates-catalog-products.md)。
  - 追蹤專案交付期間的非庫存材料使用。 如需詳細資訊，請參閱[記錄專案和專案工作的材料使用方式](../../material/material-usage-log.md)。
  - 開立已使用非庫存材料成本的發票。 如需詳細資訊，請參閱[管理帳務積存 - 精簡](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog)。
  - Dynamics 365 Dataverse 中的新 API 允許對 **排程實體** 執行建立、更新和刪除作業。 如需詳細資訊，請參閱 [使用排程 API 對排程實體執行作業](../../project-management/schedule-api-preview.md)。

## <a name="quality-updates"></a>品質更新

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2224568 | 新增邏輯，以啟用涉及叫用發票確認外掛程式的自訂。 |
| 帳單和定價 | 2101098 | 改善預估發票預設欄位的邏輯：**帳單地址**、**帳單姓名** 和 **付款條件** 現在會根據對應的專案合約客戶記錄設定預設值。 |
| 帳單和定價 | 2021413 | 更新 **工作** 實體的 **實際成本** 與 **銷售** 欄位，以包含工作上未開單及已開單費用中的銷售值。 |
| 帳單和定價 | 2182110 | 複製專案合約時，目的地專案合約中會重新產生合約服務內容，以確保其唯一性。 |
| 商機管理 | 2186741 | 新增驗證，以確保無法更新現有報價明細詳細資料上的 **來源** 欄位和 **交易類型**。 |
| 商機管理 | 2191353 | 不可在時間和材料合約服務內容上建立里程碑。 |
| 商機管理 | 2216956 | 修正 **更新價格** 的問題。 |
| 規劃和追蹤 | 2182979 | 專案複製功能已改善，可確保費用估計明細是從原始專案複製而來。 |
| 規劃和追蹤 | 2184144 | 專案複製功能已改善，可確保資源職位名稱是從原始專案複製而來。 |
| 規劃和追蹤 | 2184799 | 專案複製：加強控制，以確保正在進行複製時無法變更估計開始日期。 |
| 規劃和追蹤 | 2185134 | 專案複製：目的地專案估計開始日期已設定為今天的日期。 |
| 規劃和追蹤 | 2196373 | 專案複製：確保專案經理和團隊成員記錄在專案團隊中不會重複。 |
| 規劃和追蹤 | 2211833 | 專案複製：資源指派會從源專案工作複製到目的地專案。 |
| 規劃和追蹤 | 2186541 | 修正 **估計值** 網格依資源分組時發生的問題。 |
| 規劃和追蹤 | 2166906 | 工作中的交易類別必須是複製到 **資源指派** 實體。 |
| 資源管理 | 2125362 | 修正使用根據工作時數配置方法建立一般團隊成員的問題。 |
| 時間和費用 | 2113603 | 修正從 **時間項目** 頁面中移除屬性的自訂相關問題。 系統現在會先檢查頁面上是否有該屬性，再使用指令碼來存取屬性。 |
| 時間和費用 | 2204377 | 在輸入時間期間選取 **複製週次** 時，必須自動顯示已複製的工時表。 |
| 時間和費用 | 2209059 | Dynamics 365 Field Service 時間項目的 **狀態** 欄位可以進行編輯。 |