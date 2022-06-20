---
title: 內部專案的實際值影響
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 內部專案各種事件中實際值資料表影響的資訊。
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921375"
---
# <a name="actuals-impact-for-an-internal-project"></a>內部專案的實際值影響

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

下表列出內部專案業務開發中各種事件發生時所建立之不同交易類型的實際值。

| 事件 | 成本實際值 | 範例 |
|---|---|---|
| 時間已建立。 | 不適用 | <p>Bob Kozack 來自成本費率為每小時 100 美元 (USD 100) 的 Fabrikam US 組織單位，他正在從事一個名為「在 Adatum 進行機械臂安裝」的專案。 此專案已對應至合約服務內容中的固定價格帳務方式。 以下是 Bob Kozak 的範例時間項目：</p><p>Bob Kozack - 8 小時</p> |
| 時間已提交。 | 不適用 | 時間項目的成本帳目明細已建立。 帳目分錄中已輸入預設成本費率。 |
| 此時間項目會在核准之前回收。 | 不適用 | |
| 時間已核准。 | 成本實際值已建立。 | <p>建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul> |
| 時間核准已取消。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul> |
| 此時間項目會在核准之後回收。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
