---
title: 時間和材料業務開發中的實際值影響
description: 本主題提供有關業務開發在 Microsoft Dynamics 365 Project Operations 中處於時間和材料業務開發生命週期時各種事件中對實際值資料表所產生影響的資訊。
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
ms.openlocfilehash: a4ea3f9cf74d8a67447571001b75065b8cde5c00
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580851"
---
# <a name="actuals-impact-in-a-time-and-materials-engagement"></a>時間和材料業務開發中的實際值影響

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

下表列出時間和材料業務開發中各種事件發生時所建立之不同交易類型的實際值。

| 事件 | 成本實際值 | 未開單銷售實際值 | 已開單銷售實際值 | 範例 |
|---|---|---|---|---|
| 時間已建立。 | 不適用 | 不適用 | 不適用 | <p>Bob Kozack 來自成本費率為每小時 100 美元 (USD 100) 的 Fabrikam US 組織單位，他正在從事一個名為「在 Adatum 進行機械臂安裝」的專案。 在此專案中，他的合約帳單費率是每小時 200 美元。 以下是 Bob Kozak 的範例時間項目：</p><p>Bob Kozack，8 小時</p> |
| 時間已提交。 | 不適用 | 不適用 | 不適用 | 建立時間項目的成本帳目明細和未開單銷售帳目。 帳目分錄中已輸入預設價格和成本費率。 |
| 此時間項目會在核准之前回收。 | 不適用 | 不適用 | 不適用 | |
| 時間已核准：已提交的時數等於計費時數。 | 成本實際值已建立。 | 未開單銷售實際值已建立。 | 不適用 | <p>建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600</li></ul> |
| 時間已核准：計費時數減少到提交的時數以下。 | 成本實際值已建立。 | <p>建立兩個未開單銷售實際值：</p><ul><li>計費時數的應收費未開單銷售實際值</li><li>剩餘數量的不應收費未開單銷售實際值</li></ul> | 不適用 | <p>建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，6 小時，美元 1,200，*應收費*</li><li>**未開單銷售實際值：** Bob Kozack，2 小時，美元 400，*不應收費*</li></ul> |
| 時間已核准：計費時數減少到提交的時數以上。 | 成本實際值已建立。 | 未開單銷售實際值已建立。 | 不適用 | <p>建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，10 小時，美元 2,000</li></ul> |
| 時間核准已取消。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | <p>原始未開單銷售實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回未開單銷售實際值。</p> | 不適用 | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul> |
| 此時間項目會在核准之後回收。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | <p>原始未開單銷售實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回未開單銷售實際值。</p> | 不適用 | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul> |
| 合約已確認。 | <p>舊成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p><p>重新評估合約規則之後，建立新的成本實際值。</p> | <p>舊未開單銷售實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回未開單銷售實際值。</p><p>重新評估合約規則之後，建立新的未開單銷售實際值。</p> | 不適用 | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul><p>針對已重新評估的財務影響所建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600</li></ul> |
| 發票已建立。 | 不適用 | 不適用 | 不適用 | |
| 發票已確認。 未開單銷售實際值的數量對發票明細詳細資料上的數量沒有產生變更。 | 不適用 | <p>舊的未開單銷售實際值的發票狀態已更新。</p><p>建立調整狀態為 **不可調整** 的沖回未開單銷售實際值。 | 已開單銷售實際值已建立。 | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul><p>已更新的現有實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*客戶發票已過帳*</li></ul>為了沖回先前財務在製品 (WIP) 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)</li></ul><p>為了記錄已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，8 小時，美元 1,600</li></ul> |
| 未開單銷售實際值的數量減少到發票明細詳細資料上的數量之後，發票獲確認。 | 不適用 | <p>原始未開單銷售實際值的調整狀態已更新為 **已調整**。</p><p>建立原始未開單銷售實際值的沖回未開單銷售實際值。 其調整狀態為 **不可調整**。</p><p>建立兩個新的未開單銷售實際值：</p><ul><li>計費時數的應收費未開單銷售實際值</li><li>剩餘數量的不應收費未開單銷售實際值</li></ul><p>建立這兩個新的未開單銷售實際值的沖回未開單銷售實際值。</p> | <p>建立兩個已開單銷售實際值：</p><ul><li>計費時數的應收費已開單銷售實際值</li><li>剩餘數量的不應收費已開單銷售實際值</li></ul> | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul><p>已更新的現有實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*已調整*</li></ul><p>為了沖回先前財務 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul><p>為了記錄更新後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，6 小時，美元 1,200，*應收費*</li><li>**未開單銷售實際值：** Bob Kozack，2 小時，美元 400，*不應收費*</li></ul><p>為了沖回更新後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(6 小時)，(美元 1,200)，*應收費*</li><li>**未開單銷售實際值：** Bob Kozack，(2 小時)，(美元 400)，*不應收費*</li></ul><p>為了記錄已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，6 小時，美元 1,200，*應收費*</li><li>**已開單銷售實際值：** Bob Kozack，2 小時，美元 400，*不應收費*</li></ul> |
| 未開單銷售實際值的數量增加到發票明細詳細資料上的數量之後，發票獲確認。 | 不適用 | <p>原始未開單銷售實際值的調整狀態已更新為 **已調整**。</p><p>建立原始未開單銷售實際值的沖回未開單銷售實際值。 其調整狀態為 **不可調整**。</p><p>新數量建立新的未開單銷售實際值。</p><p>建立新的未開單銷售實際值的沖回未開單銷售實際值。</p> | 新數量建立已開單銷售實際值。 | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul><p>已更新的現有實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*已調整*</li></ul><p>為了沖回先前財務 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul><p>為了記錄更新後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，10 小時，美元 2,000，*應收費*</li></ul><p>為了沖回更新後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(10 小時)，(美元 2,000)，*應收費*，*不可調整*</li></ul><p>為了記錄已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，10 小時，美元 2,000，*應收費*</li></ul> |
| 已更正發票以減少應收費數量或價格。 | 不適用 | <p>建立兩個未開單銷售實際值：</p><ul><li>更正發票中數量的應收費未開單銷售實際值</li><li>剩餘數量的應收費未開單銷售實際值</li></ul><p>建立這兩個新的未開單銷售實際值的沖回未開單銷售實際值。</p> | <p>沖回已開單銷售實際值已建立。</p><p>新數量建立新的已開單銷售實際值。 | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*客戶發票已過帳*</li><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)</li></ul><p>已更新的現有實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*已調整*</li></ul><p>為了沖回先前已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul><p>為了記錄更正後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，6 小時，美元 1,200，*應收費*，*客戶發票已過帳*</li><li>**未開單銷售實際值：** Bob Kozack，2 小時，美元 400，*應收費*</li></ul><p>為了沖回更正後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(6 小時)，(美元 1,200)，*應收費*，*不可調整*</li></ul><p>為了記錄更正後已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，6 小時，美元 1,200，*應收費*</li></ul> |
| 已更正發票以增加應收費數量或價格。 | 不適用 | <p>新數量建立新的未開單銷售實際值。</p> <p>建立新的未開單銷售實際值的沖回未開單銷售實際值。</p> | <p>沖回已開單銷售實際值已建立。</p>新數量建立新的已開單銷售實際值。</p> | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600，*客戶發票已過帳*</li><li>**未開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)</li></ul><p>已更新的現有實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*已調整*</li></ul><p>為了沖回先前已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，(8 小時)，(美元 1,600)，*不可調整*</li></ul><p>為了記錄更正後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，10 小時，美元 2,000，*應收費*，*客戶發票已過帳*</li></ul><p>為了沖回更正後銷售 WIP 而建立的新實際值：</p><ul><li>**未開單銷售實際值：** Bob Kozack，(10 小時)，(美元 2,000)，*應收費*</li></ul><p>為了記錄更正後已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** Bob Kozack，10 小時，美元 2,000，*應收費*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]