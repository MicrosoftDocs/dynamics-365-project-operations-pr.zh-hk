---
title: 專案型報價明細的發票排程
description: 本主題提供有關為報價明細建立發票排程和里程碑的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ecaf4d872873473b0e7fe3b08d62c6fe5af9c3d
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908765"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>專案型報價明細的發票排程

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

專案型報價明細提供表示發票排程的功能。 這在報價階段中是選擇性的，因為應用程式繫結至報價明細時，不支援開立專案開票。 只有在報價成交後，才允許開立發票。 在報價階段建立發票排程唯一造成的下游影響是，將此發票排程複製到專案型合約服務內容。 如果您未在報價階段建立發票排程，則可以在專案型合約服務內容上這樣做。

總而言之，發票排程的目的在於允許自動建立專案型合約服務內容的草稿發票。 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>建立專案型報價明細的時間和材料發票排程

專案型報價明細的帳務方式為 [時間和材料] 時，系統會產生基於日期的發票排程。 若要讓系統自動產生基於日期的發票排程，請完成下列步驟。

1. 移至**設定** > **發票週期**，並設定發票週期。
2. 在**報價**頁面上，開啟專案報價，並在**摘要**索引標籤中設定要求的交付日期。
3. 開啟需要建立基於日期的發票排程的時間和材料報價明細。 
4. 在**發票排程**索引標籤上，選取**帳單開始日期**及**發票週期**欄位中的值。 
5. 在子格上，選取**產生發票排程**。
6. 應用程式會產生以下列方式設定**發票執行日期**、**交易截止日期**和**執行狀態**欄位的發票排程：

    - **發票執行日期**會設定為取決於發票週期的日期。
    - **交易截止日期**會設定為**發票執行日期**的前一天。
    - **執行狀態**會自動設為**未執行**。 自動發票建立作業針對特定發票執行日期執行時，此作業會將此欄位更新為**執行成功**或**執行失敗**。

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>建立專案型報價明細的固定價格發票排程

專案型報價明細的帳務方式為**固定價格**時，系統會建立基於里程碑的發票排程。 完成下列步驟，為一組在行事曆期間平均分佈的固定里程碑，自動產生此排程。

1. 移至**設定** > **發票週期**，並設定發票週期。
2. 在**報價**頁面上，開啟專案報價，並在**摘要**索引標籤中設定要求的交付日期。
3. 開啟需要建立里程碑排程的固定價格報價明細。 
4. 在**發票排程**索引標籤上，選取**帳單開始日期**及**發票週期**欄位中的值。 
5. 在子格上，選取**產生定期里程碑**。
6. 應用程式會產生包含里程碑名稱、日期和金額的發票排程。

    - 里程碑名稱會設定為取決於發票週期的日期。
    - 里程碑日期會設定為取決於發票週期的日期。
    - 里程碑金額的計算方式是，將專案型報價明細的報價金額除以根據週期和帳單開始日期以及要求的交付日期所決定的里程碑數目。
    - 如果報價明細還有估計稅額，此值會產生定期里程碑時，均等分攤至每個里程碑。

### <a name="manually-create-milestones"></a>手動建立里程碑

當固定價格里程碑並非定期分割時，您也可以手動產生這些里程碑。 若要手動建立里程碑：

開啟需要建立里程碑的固定價格報價明細。 在**發票排程**索引標籤的子格上，選取 **+ 建立新的報價明細里程碑**，然後根據下表輸入必要的資訊。

| **欄位** | **位置** | **關聯性、目的和指引** | **下游影響** |
| --- | --- | --- | --- |
| 里程碑名稱 | 快速建立 | 里程碑的名稱。 | 這會傳播至專案合約服務內容里程碑和發票 |
| 專案工作 | 快速建立 | 如果里程碑已繫結至專案工作，您可以使用此參考，新增根據工作狀態設定里程碑狀態的自訂邏輯。 | 應用程式不會對工作產生此參考的任何下游影響。 |
| 里程碑日期 | 快速建立 | 設定日期，自動發票建立程序應在此日期尋找此里程碑的這個要考慮開立發票的狀態。 | 這會傳播至專案合約服務內容里程碑和發票。 |
| 發票狀態 | 快速建立 | 建立里程碑時，此狀態一律設定為**尚未準備好開立發票**。 | 這會傳播至專案合約服務內容里程碑和發票。 |
| 明細金額 | 快速建立 | 向客戶開立發票的里程碑金額或值。 | 這會傳播至專案合約服務內容里程碑和發票。 |
| 稅額 | 快速建立 | 將套用至里程碑的稅額。 | 這會傳播至專案合約服務內容里程碑和發票。 |