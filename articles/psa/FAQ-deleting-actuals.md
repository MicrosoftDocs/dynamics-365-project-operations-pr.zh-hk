---
title: 為什麼我無法從實際值實體刪除記錄？
description: 本主題提供有關為何您無法從實際值實體刪除記錄的資訊。
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993128"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="659e7-103">為什麼我無法從實際值實體刪除記錄？</span><span class="sxs-lookup"><span data-stu-id="659e7-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="659e7-104">Project Service Automation (PSA) 不允許您刪除實際值，因為這些值可以做為對下游系統 (例如總帳) 有財務影響的交易事實原始資料。</span><span class="sxs-lookup"><span data-stu-id="659e7-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="659e7-105">如果可以刪除實際值，可能就會引發對財務報表交易完整性的質疑。</span><span class="sxs-lookup"><span data-stu-id="659e7-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="659e7-106">若要建立稽核線索，客戶必須使用帳目來建立補償交易。</span><span class="sxs-lookup"><span data-stu-id="659e7-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]