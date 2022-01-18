---
title: 轉包合約服務內容里程碑
description: 本主題說明如何為廠商的轉包合約建立和維護按里程碑請款的發票排程。
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558529"
---
# <a name="subcontract-line-milestones"></a>轉包合約服務內容里程碑

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

在 Dynamics 365 Project Operations 中，採用固定價格計費方式的轉包合約服務內容可以指定廠商按里程碑請款的發票排程。

您可以讓系統使用已設定的頻率自動產生廠商開立發票的里程碑，也可以手動建立這些里程碑。

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>自動為轉包合約服務內容建立按里程碑請款的發票排程

完成下列步驟，讓系統自動為固定一組平均分佈的里程碑產生按里程碑請款的發票排程。

1. 移至 **設定** > **發票週期**，然後設定轉包合約服務內容的發票週期。
2. 開啟 **轉包合約** 頁面、開啟您要使用的轉包合約，然後開啟要為其建立里程碑排程的固定價格轉包合約服務內容。
3. 在 **轉包合約服務內容里程碑** 索引標籤上，選取 **產生定期里程碑**。
4. 在對話方塊中，輸入或選取日期範圍、里程碑數目和發票週期。 您可以選取開始日期、選取里程碑數目以及發票週期或開始日期，也可以選取結束日期和發票週期。 您無法選取里程碑的結束日期和數目。
系統會使用此資訊來產生顯示在 **里程碑** 網格中的里程碑和記錄。

   - **里程碑名稱** - 里程碑的名稱會根據發票週期設定為里程碑的日期。
   - **里程碑日期** - 根據發票週期而定的日期。
   - **里程碑金額** - 計算方式為轉包合約服務內容的小計金額除以里程碑數目。

如果轉包合約服務內容的 **估計稅額** 欄位中有值，則此值會在產生定期里程碑時，均等增加到每個里程碑上。

轉包合約服務內容里程碑金額的總和必須等於轉包合約服務內容的值。 如果不相等，就會發生錯誤。 您可以修正此錯誤，並確認里程碑總計是否等於轉包合約服務內容值，方法是建立、編輯或刪除里程碑和稅額。 進行變更之後，儲存並重新整理頁面，以確保不再發生其他錯誤。

## <a name="manually-create-subcontract-line-milestones"></a>手動建立轉包合約服務內容里程碑

轉包合約服務內容上的固定價格里程碑未經定期分割時，您可以手動產生這些里程碑。 若要手動建立轉包合約服務內容里程碑，請完成下列步驟。

1. 在導覽窗格上，選取 **轉包合約**，並開啟您要使用的轉包合約。
2. 開啟要為其建立里程碑的固定價格轉包合約服務內容。
3. 在 **轉包合約服務內容里程碑** 索引標籤的子格上，選取 **+ 新增轉包合約服務內容里程碑**。
4. 在 **新增轉包合約服務內容里程碑** 頁面上，根據下表輸入必要的資訊。

    | 欄位 | 描述 |功能影響|
    | --- | --- |----------------------|
    | 里程碑名稱 | 里程碑的名稱。 |這會在所有根據轉包合約服務內容里程碑進行的查詢中顯示為第一欄。 根據此里程碑建立的廠商發票明細，也會使用轉包合約服務內容里程碑的名稱做為廠商發票明細的預設名稱。|
    | 描述 | 里程碑的描述。 |根據此里程碑建立的廠商發票明細，也會使用轉包合約服務內容里程碑的描述做為廠商發票明細的預設描述。|
    | 里程碑日期 | 自動發票建立程序屆時應尋找此里程碑要納入開立發票考量之狀態的日期。| 開立此轉包合約服務內容的發票時，此值會做為廠商發票明細的預設日期。 |
    | 總額 | 要向客戶開立發票的里程碑金額或值。 |開立此轉包合約服務內容的發票時，此值會做為廠商發票明細的預設金額。 |
    | 稅額 | 套用在里程碑上的稅額。| 開立此轉包合約服務內容的發票時，此值會做為廠商發票明細的預設稅金。 |
    | 稅後金額 | 此唯讀欄位是以「金額 + 稅金」的方式來計算。|開立此轉包合約服務內容的發票時，此值會做為廠商發票明細的預設值。 |
    | 發票狀態 | 建立里程碑時，此狀態一律設定為 **尚未準備好開立發票**。|  狀態為 **已準備好開立發票** 時，廠商發票建立作業會將此里程碑包含在廠商發票中。 |

5. 選取 **儲存後關閉**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]