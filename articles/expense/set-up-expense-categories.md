---
title: 設定費用類別
description: 本主題提供有關如何為費用報表設定費用類別和共用類別的資訊。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123810"
---
# <a name="set-up-expense-categories"></a>設定費用類別

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

員工建立費用報表時，他們記錄的每項費用都必須與費用類別有關聯。 費用類別是從可在您組織中所有法律實體之間共用的共用類別衍生而來。 視組織如何定義而定，這些費用類別也可以在其他區域中共用。 您必須根據組織的定義和實作團隊的指引，判斷費用管理中使用的類別是僅限在費用管理中使用，還是應在其他區域中共用。

> [!NOTE]
> 這些類別可以在 [專案管理與會計] 與 [費用管理] 之間共用，或是在 [專案管理與會計] 與 [生產] 之間共用。 不過，無法在 [費用管理] 與 [生產] 之間共用。

開始設定程序之前，您必須對每一個費用類別做出下列決定：

- 什麼是費用類別？ 範例包括航班、住宿或里程等類別。
- 費用類別也可以用於 [專案管理與會計] 嗎？ 如果可以，您還必須做出下列決定：

    - 下列費用會使用哪個成本科目？

        - 成本
        - 薪資分攤
        - WIP 成本值
        - 成本項目
        - WIP 成本值項目
        - 應計損失
        - WIP 應計損失

    - 下列營收來源會使用哪個收入科目？

        - 已開發票營收
        - 應計收入 - 銷售值
        - WIP - 銷售值
        - 應計收入 - 生產
        - WIP - 生產
        - 應計收入 - 利潤
        - WIP - 利潤
        - 應計收入 - 訂閱
        - WIP - 訂閱

- 什麼是費用類型？
- 什麼是費用類別的預設付款方式？
- 費用類別中的費用是否必須逐條列舉？
- 什麼是費用類別的主要預設科目？
- 什麼是費用類別的預設項目銷售課稅群組？
- 費用類別是否允許其他付款方式？ 如果是，有哪些？
- 此費用類別中是否有子類別？ 如果有子類別，您還必須做出下列決定：

    - 是否有任何子類別不在稅金退還之列？
    - 什麼是子類別的項目銷售課稅群組？


[!INCLUDE[footer-include](../includes/footer-banner.md)]