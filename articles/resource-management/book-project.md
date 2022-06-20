---
title: 預約給專案
description: 本文提供有關預約資源給專案的資訊。
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928551"
---
# <a name="book-to-a-project"></a>預約給專案

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

專案經理或資源管理員有時需要將資源配置給沒有一般團隊成員所定義之特定需求的專案。 這可以透過三種方式之一來達成。

- 從團隊成員網格預約
- 從排程面板預約
- 從 **專案** 表單預約

## <a name="book-from-the-team-member-grid"></a>從團隊成員網格預約

如果您的組織是在混合資源配置模式下運作，則專案經理可以完成下列步驟，直接將資源預約給專案。

1. 從專案中移至團隊成員網格，然後選取 **新增**。
2. 定義資源的職位名稱和角色。
3. 從可用的查詢中選取可預約資源。
4. 選取資源之後，定義下列欄位資訊以預約資源：

    - 開始日期
    - 完成日期
    - 配置方法
    - 時數 (如果適用)
    - 專案核准者

6. 選取 **儲存後關閉**

## <a name="book-from-the-schedule-board"></a>從排程面板預約

資源管理員需要直接將資源預約給專案時，他們可以使用排程面板和專案需求。 專案需求是隨時可供預約的資源需求。 若要直接從排程面板預約給專案，請完成下列步驟。

1. 瀏覽至排程面板，然後在左側頁面上，篩選您考慮要用於需求的資源。
2. 在下方窗格中，選取 **專案** 索引標籤，以檢視專案需求清單。
3. 將需求拖曳到資源，並定義下列資訊：

    - 開始日期
    - 完成日期
    - 預約狀態
    - 預約方式
    - Duration
   
   > [!NOTE]
   > Dynamics 365 Project Operations 目前不支援排程面板。   

## <a name="book-from-the-project-form"></a>從專案表單中預約

身為專案經理，您可能需要將資源預約給專案，但是只知道準則，而不知資源的名稱。 請完成下列步驟，使用排程小幫手根據資源的任何可用屬性來尋找資源。 

1. 瀏覽至專案，並選取 **預約** 以開啟排程小幫手。
2. 使用排程小幫手左側的篩選，縮小準則的範圍並選取 **搜尋**。
3. 您可以根據結果中傳回的資源來預約資源。

> [!NOTE]
> 此方法不會為資源建立任何預約。 反而是將資源新增至團隊。 將團隊成員新增至專案之後，專案經理就可以使用維護預約或延長預約，將必要的預約新增至資源。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
