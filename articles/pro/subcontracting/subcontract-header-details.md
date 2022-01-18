---
title: 轉包合約的標題詳細資料
description: 本主題說明 Project Operations 中轉包合約標題上所提供的功能。
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501353"
---
# <a name="header-details-for-subcontracts"></a>轉包合約的標題詳細資料

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

本主題說明 Dynamics 365 Project Operations 中轉包合約標題上所提供的功能。

當專案經理規畫並執行專案時，他們可能會利用轉包商，並向廠商購買產品和服務。 當專案經理需要購買產品或服務時，他們可以在 Project Operations 中建立轉包合約。

若要建立轉包合約，請完成下列步驟。

1. 在導覽窗格中，選取 **轉包合約**，並在 **轉包合約** 頁面上選取 **新增**。
2. 輸入必要資訊，然後選取 **儲存**。

    下表提供有關 **轉包合約標題** 頁面中欄位的資訊。

    | 欄位 | 描述 |功能影響 |
    |---|------|---| 
    | 名稱 | 轉包合約名稱。 | 在所有轉包合約下拉式清單中，轉包合約的名稱都會列在第一欄，以協助您識別轉包合約。 | 
    | 描述 | 轉包合約上所要採購之服務與產品的簡短描述。 | 無​​ |
    | 廠商 | 要從中購買產品與服務之公司的名稱。 此客戶記錄的關聯類型為 **廠商** 或 **供應商**。 | 根據選取的廠商而定，下列欄位會自動輸入預設值：<br/> **• 貨幣** </br> **• 價目表** </br> **• 付款條件**</br> **• 付款地址**</br> **• 帳單地址**</br> **• 帳單姓名** </br>**• 廠商客戶經理**|
    | 轉包合約日期 | 建立轉包合約的日期。 | 轉包合約日期會用於從附加至相關廠商的價目表或從專案參數中選取正確的採購價目表。 |
    | 狀態原因 | 轉包合約的狀態。 | 此狀態會判斷轉包合約在商務程序中所在的階段，以及是否可加以編輯。 <br/>其值包括：<br>• **草稿**：可以編輯轉包合約。 您只能編輯狀態為 **草稿** 的轉包合約。<br/>• **已確認**：與廠商的交涉完成，並已核准轉包合約進行交貨。 <br/>• **已關閉**：轉包合約的交貨完成。<br/>• **已取消**：轉包合約已取消，且未安排任何交貨。  | 
    | 貨幣 | 購買產品和服務時所用的貨幣。 預設值是自動根據供應商客戶輸入，但您可以進行變更。 | 轉包合約的貨幣會用於從附加至相關廠商的價目表或從專案參數中選取採購價目表。 使用其他貨幣的價目表無法與轉包合約產生關聯。 廠商資源根據此轉包合約所交付之時間、費用及材料的成本會以此貨幣記錄於專案中。 儲存轉包合約記錄之後，就無法變更轉包合約上的貨幣。|
    | 合約單位 | 與廠商簽訂採購合約或轉包合約的公司部門。 | 無​​ |
    | 付款條款 | 此轉包合約所簽發之廠商發票的付款條件。 預設值是自動根據供應商客戶記錄輸入。 | 轉包合約的付款條件會複製到所有與此轉包合約相關的廠商發票。 如果轉包合約的狀態是 **草稿**，則可以更新付款條件。 | 
    | 付款地址 | 付款必須發送到的廠商地址。 預設值是自動根據供應商客戶記錄輸入。 | 轉包合約的付款地址會做為付款地址複製到所有為此轉包合約建立的廠商發票。 如果轉包合約的狀態是 **草稿**，則可以更新付款地址。|
    | 帳單姓名 | 廠商公司中負責傳送發票之人員或部門的名稱。 預設值是自動根據供應商客戶記錄輸入。 | 轉包合約的 **付款姓名** 值會複製到所有與此轉包合約相關的廠商發票。 如果轉包合約的狀態是 **草稿**，則可以更新此欄位。|
    | 帳單地址 | 廠商發票上所使用的地址。 預設值是自動根據供應商客戶記錄輸入。 | 此地址是針對此轉包合約所建立之廠商發票上的「發票開票人」地址。 |
    | 小計 | 如果轉包合約沒有服務內容，請在稅金前輸入訂單小計。 如果轉包合約有服務內容，則此欄位是唯讀欄位。 顯示的金額是轉包合約中所有服務內容的小計金額。 | 無​​ |
    | 總稅金 | 如果轉包合約沒有服務內容，請輸入此轉包合約上的總計稅金。 如果轉包合約有服務內容，則此欄位是唯讀欄位。 顯示的金額是轉包合約中所有服務內容的稅金加總。 | 無​​ |
    | 總金額 | 此導出欄位會顯示含稅後的轉包合約服務內容總金額。 | 無​​ |
    | 確認日期 | 確認轉包合約的日期。 | 無​​ |
    | 要求者 | 此欄位預設會設定為建立轉包合約的使用者名稱。 不過，轉包合約的建立者可以變更此值，指出委託他們代為建立轉包合約的人。 | 無​​ |
    | 廠商客戶經理 | 廠商帳戶主要連絡人的名稱。 預設值是自動根據供應商客戶記錄輸入。 您可以選取不同的連絡人做為轉包合約的廠商客戶經理。 | 您可以設定電子郵件警示，以便在轉包合約因價格交涉而有所變更時通知連絡人。 |