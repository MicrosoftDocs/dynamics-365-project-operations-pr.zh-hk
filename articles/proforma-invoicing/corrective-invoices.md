---
title: 已更正的發票
description: 本主題提供有關已更正發票的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087668"
---
# <a name="corrected-invoices"></a>已更正的發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

您可以編輯已確認的發票。 編輯已確認的發票時，會建立已更正發票的草稿。 因為假設您要從原始發票中沖回所有交易和數量，已更正的發票會包含原始發票中所有的交易，而其中所有的數量皆為零 (0)。

交易不需要更正時，您可以從草稿更正發票移除這些交易。 若只是要沖回或回復部分數量，則可以編輯明細詳細資料上的 [數量] 欄位。 如果開啟發票明細詳細資料，您可以查看原始發票數量。 然後就可以編輯目前發票數量，使其小於或等於原始發票數量。

確認更正發票時，會沖回原始已開單銷售實際值，並建立新的已開單銷售實際值。 如果數量已減少，則差額也會導致建立新的未開單銷售實際值。 例如，如果原始已開單銷售是八小時，且已更正的發票明細詳細資料的數量已減少為六小時，則會沖回原始已開單銷售明細，並建立兩個新的實際值：

- 六小時的已開單銷售實際。
- 剩餘兩個小時的未開單銷售實際值。 依據與客戶的協商，此交易可以稍後再開帳單，或標示為不應收費。
