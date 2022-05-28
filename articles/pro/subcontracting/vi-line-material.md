---
title: 產品的廠商發票明細
description: 本主題說明如何記錄產品的廠商發票明細，以及使用不同的欄位來記錄從廠商購買的產品。
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599205"
---
# <a name="vendor-invoice-lines-for-products"></a>產品的廠商發票明細

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

Microsoft Dynamics 365 Project Operations 中的廠商發票可以有產品 (也稱為材料) 的廠商發票明細。 專案經理可以使用產品的廠商發票明細，將所購買產品的成本記錄在專案中。

產品的廠商發票明細可能會，也可能不會參考材料的轉包合約服務內容。 如果產品的廠商發票明細參考轉包合約，則專案經理將可以核對由專案經理所記錄並核准的已購產品用途，比對並驗證將由廠商開具發票明細的產品。

下表提供有關產品廠商發票明細中欄位的資訊。

| 欄位 | 名稱 | 功能影響 |
| --- | --- | --- |
| 姓名 | 廠商發票明細的名稱，可協助進行識別。 | 此名稱會在所有根據廠商發票明細進行的查詢中顯示為第一欄。 |
| 名稱 | 廠商根據廠商發票明細所開具之產品的簡短描述。 | None |
| 轉包合約 | 最初訂購產品所用的轉包合約。 | 選取廠商發票的轉包合約時，廠商發票上的所有明細都會繼承所選取的轉包合約。 廠商發票不能有參考不同轉包合約的廠商發票明細。 |
| 轉包合約服務內容 | 訂購產品所用的轉包合約服務內容。 可選取的轉包合約服務內容清單僅限於所選轉包合約中的明細。 | 在產品的廠商發票明細中選取轉包合約服務內容時，**專案**、**工作** 和 **產品** 欄位的預設值是來自轉包合約服務內容中對應欄位的輸入。 如果選取的轉包合約服務內容在 **專案**、**工作** 和 **產品** 欄位中都有值，則廠商發票明細中對應欄位的值不能與這些值不同。 |
| 交易日期 | 將廠商發票明細的成本實際值記錄於專案時的日期。 | None|
| 交易分類 | 開立產品的發票時，此欄位應設定為 **材料**。 | 值為 **材料**，表示廠商發票明細是用來記錄所購買材料的發票金額。 |
| 專案 | 使用發票已開具產品所在之專案的名稱。 | 這是必要欄位，不可保留空白。 |
| 工作 | 使用發票已開具產品所在之專案工作的名稱。 只有選取專案時，才能使用此欄位。 選取專案工作是選擇性的。 | 如果此欄位保留空白，則專案經理可以將廠商發票明細與專案任何工作中所用已購買的產品進行比對。 如果廠商發票明細沒有參考轉包合約服務內容，且此欄位保留空白，則依據廠商發票明細所建立的成本實際值不會連結至任何未開單銷售實際值。 在這種情況下，如果已設定工作型帳單，則無法將此成本的發票開立給最終客戶。 |
| 選取產品 | 選擇發票正在開立的產品是目錄中現有產品還是目錄外產品。 | 選取轉包合約服務內容時，會輸入轉包合約中的預設值。 |
| 產品 | 從目錄中選取產品。 如果產品是目錄外產品，請輸入產品名稱。 | 此欄位是用來輸入現有產品的預設購買價格。 |
| 數量 | 輸入此發票明細中廠商要開具的材料數量。 | None |
| 單位群組 | 選取要用來表示發票開具數量之單位的單位群組。 | None |
| 單位 | 預設值是所選單位群組的基礎單位。 您可以變更此值，按照所選單位群組的任何單位來付款。 | **產品** 與 **單位** 值的組合將會在廠商發票明細上用來做為 **單價** 欄位的預設值或計算值。 |
| 單價 | 預設單價會使用專案價目表中 **產品** 與 **單位** 值的組合，此專案價目表適用於廠商發票明細的交易日期。 | None |
| 小計 | 此唯讀欄位的計算方式為 *數量* &times; *單價* (如果 **數量** 欄位和 **單價** 欄位中都已輸入值)。 如果其中一個或這兩個欄位為空白，您可以在此欄位中輸入值。 | None |
| 銷售稅 | 輸入銷售稅金額。 | None |
| 總金額 | 廠商發票明細的總計金額 (含稅)。 此欄位的計算方式是 *小計* +  *銷售稅*。 | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]