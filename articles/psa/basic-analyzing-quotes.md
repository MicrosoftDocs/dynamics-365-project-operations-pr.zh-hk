---
title: 專案報價分析
description: 此主題提供專案報價分析的相關資訊。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012478"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="c3909-103">專案報價分析</span><span class="sxs-lookup"><span data-stu-id="c3909-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c3909-104">Dynamics 365 Project Service Automation 會分析專案報價，以估計獲利能力。</span><span class="sxs-lookup"><span data-stu-id="c3909-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="c3909-105">它也會分析報價與客戶對交付日期或完成日期以及預算的期望相符程度。</span><span class="sxs-lookup"><span data-stu-id="c3909-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="c3909-106">獲利率分析</span><span class="sxs-lookup"><span data-stu-id="c3909-106">Profitability analysis</span></span>

<span data-ttu-id="c3909-107">Project Service Automation 使用毛利率和調整後毛利率來分析獲利率。</span><span class="sxs-lookup"><span data-stu-id="c3909-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="c3909-108">毛利率使用下列公式計算：</span><span class="sxs-lookup"><span data-stu-id="c3909-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="c3909-109">調整後毛利率使用下列公式計算：</span><span class="sxs-lookup"><span data-stu-id="c3909-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="c3909-110">如果毛利率和調整後毛利率的值相差幅度很大，表示報價中有一大部分的工作是歸類為非應收費。</span><span class="sxs-lookup"><span data-stu-id="c3909-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="c3909-111">分析客戶期望</span><span class="sxs-lookup"><span data-stu-id="c3909-111">Analysis of customer expectations</span></span>

<span data-ttu-id="c3909-112">如果您輸入下列欄位的值，就可以分析報價並產生客戶對排程和預算的期望圖表：</span><span class="sxs-lookup"><span data-stu-id="c3909-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="c3909-113">報價標頭上的 **要求的交貨日期** 欄位。</span><span class="sxs-lookup"><span data-stu-id="c3909-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="c3909-114">每個報價明細的 **客戶預算** 欄位 (適用於專案型明細和產品型明細)。</span><span class="sxs-lookup"><span data-stu-id="c3909-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="c3909-115">分析客戶對排程的期望的作法是，在報價的所有報價明細中，將報價明細詳細資料的最後結束日期與要求的交貨日期進行比較。</span><span class="sxs-lookup"><span data-stu-id="c3909-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="c3909-116">分析客戶對排程的預算的作法是，在所有報價明細中，將客戶預算總計的總和與報價金額進行比較</span><span class="sxs-lookup"><span data-stu-id="c3909-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]