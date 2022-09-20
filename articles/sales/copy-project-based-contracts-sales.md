---
title: 複製專案型合約
description: 本文提供有關在 Microsoft Dynamics 365 Project Operations 中複製專案合約的資訊。
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410344"
---
# <a name="copy-project-based-contracts"></a>複製專案型合約

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

您可以透過下列兩種方式之一複製現有合約，輕鬆地建立新的專案合約：

- 在 **專案合約** 清單頁面上，選取專案合約，然後選取 **複製**。
- 在 **專案合約** 詳細資料頁面上，選取 **複製**。

這兩種情況下都會出現對話方塊，您可在其中設定所複製合約的參數。 對話方塊包含下列欄位。 視您選取的值而定，複製程序可能會變更。

| 欄位 | 名描述 | 下游影響 |
| --- | --- | --- |
| 主題 | 輸入目標合約的主題。 對話方塊頁面開啟時，系統會將此欄位設定為來源合約的名稱，但在其後附加「複本」一詞。 | 此欄位沒有任何下游影響。 |
| 客戶 | 客戶公司或客戶記錄的參考。 對話方塊開啟時，系統會將此欄位設定為來源合約上的客戶。 | 此欄位是合約上的主要客戶。 |
| 擁有公司 | 負責交付與此交易相關聯之專案的公司。 對話方塊開啟時，系統會將此欄位設定為來源合約的擁有公司。 | 擁有公司是在完成交易後執行專案的法律實體。 擁有公司的貨幣必須與合約單位的貨幣相符。 |
| 合約單位 | 負責交付與此交易相關聯之專案的組織單位。 對話方塊開啟時，系統會將此欄位設定為來源合約的合約單位。 | 合約單位是要在完成交易後執行專案的公司部門。 每個合約單位都有貨幣。 此貨幣會用來報告專案期間所產生的估計和實際成本。 |
| 貨幣 | 進行交易所用的貨幣。 對話方塊開啟時，系統會將此欄位設定為來源合約的貨幣。 您可以變更此貨幣。 如果是這樣，則 **複製定價** 欄位一律設定為 **否**，因為來源合約的價目表已不再相關。 | 預設價目表使用此貨幣以產生合約的財務估計值，以及在交易成交時開立發票給客戶。 |
| 要求的交貨日期 | 客戶要求的交貨日期。 | 此日期會用來做為您按照特定頻率建立發票開立日期時的結束日期。 |
| 複製定價 | 指示合約上的定價是否應從來源合約複製的值。 | 如果欄位已設定為 **是**，則會將專案和產品價目表參考從來源合約複製到目標合約。 如果設定為 **否**，則價目表會根據客戶或專案參數的最新價目表使用預設價目表。 |

選取對話方塊中的 **確定** 時，系統會根據您設定的參數值，建立合約的複本。 接著會開啟新合約。

下列資訊 **不會** 從來源合約複製到目標合約，因為這是個別合約專屬的資訊：

- 發票排程
- 專案與合約服務內容客戶
- 專案型合約服務內容上的專案參考
- 客戶預算資訊

將會複製專案與產品的合約服務內容、合約服務內容詳細資料的估計值，以及合約層級上不得超過的值。 預設價格及成本費率的輸入取決於 **複製參數** 對話方塊中 **複製定價** 欄位的選取項目。

[!INCLUDE[footer-include](../includes/footer-banner.md)]