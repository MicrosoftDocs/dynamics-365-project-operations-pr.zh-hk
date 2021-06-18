---
title: 為什麼費用成本實際值上的價格會預設為零？
description: 排解費用成本實際值上的價格為何預設為 0 的問題。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992813"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="ddaa2-103">為什麼費用成本實際值上的價格會預設為零</span><span class="sxs-lookup"><span data-stu-id="ddaa2-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ddaa2-104">本常見問題集適用於交易類別設為 [費用] 且交易類型為 [成本] 的費用實際值。</span><span class="sxs-lookup"><span data-stu-id="ddaa2-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="ddaa2-105">排解有關費用成本實際值的成本費率問題</span><span class="sxs-lookup"><span data-stu-id="ddaa2-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="ddaa2-106">移至相關的費用項目，並確定費用項目欄位中有金額。</span><span class="sxs-lookup"><span data-stu-id="ddaa2-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="ddaa2-107">如果原始費用項目沒有填入金額欄位，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="ddaa2-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="ddaa2-108">若要解決此問題，請重新建立包含有效金額的費用項目，並予以核准。</span><span class="sxs-lookup"><span data-stu-id="ddaa2-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]