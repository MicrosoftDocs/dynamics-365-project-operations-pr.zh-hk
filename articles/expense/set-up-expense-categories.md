---
title: 設定費用類別
description: 本主題提供有關如何為費用報表設定費用類別和共用類別的資訊。
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d66df1ffd2be2ff884561010c46cda255a2d2189
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001843"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="f3427-103">設定費用類別</span><span class="sxs-lookup"><span data-stu-id="f3427-103">Set up expense categories</span></span>

<span data-ttu-id="f3427-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f3427-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f3427-105">員工建立費用報表時，他們記錄的每項費用都必須與費用類別有關聯。</span><span class="sxs-lookup"><span data-stu-id="f3427-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="f3427-106">費用類別是從可在您組織中所有法律實體之間共用的共用類別衍生而來。</span><span class="sxs-lookup"><span data-stu-id="f3427-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="f3427-107">視組織如何定義而定，這些費用類別也可以在其他區域中共用。</span><span class="sxs-lookup"><span data-stu-id="f3427-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="f3427-108">您必須根據組織的定義和實作團隊的指引，判斷費用管理中使用的類別是僅限在費用管理中使用，還是應在其他區域中共用。</span><span class="sxs-lookup"><span data-stu-id="f3427-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="f3427-109">這些類別可以在 [專案管理與會計] 與 [費用管理] 之間共用，或是在 [專案管理與會計] 與 [生產] 之間共用。</span><span class="sxs-lookup"><span data-stu-id="f3427-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="f3427-110">不過，無法在 [費用管理] 與 [生產] 之間共用。</span><span class="sxs-lookup"><span data-stu-id="f3427-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="f3427-111">開始設定程序之前，您必須對每一個費用類別做出下列決定：</span><span class="sxs-lookup"><span data-stu-id="f3427-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="f3427-112">什麼是費用類別？</span><span class="sxs-lookup"><span data-stu-id="f3427-112">What is the expense category?</span></span> <span data-ttu-id="f3427-113">範例包括航班、住宿或里程等類別。</span><span class="sxs-lookup"><span data-stu-id="f3427-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="f3427-114">費用類別也可以用於 [專案管理與會計] 嗎？</span><span class="sxs-lookup"><span data-stu-id="f3427-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="f3427-115">如果可以，您還必須做出下列決定：</span><span class="sxs-lookup"><span data-stu-id="f3427-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="f3427-116">下列費用會使用哪個成本科目？</span><span class="sxs-lookup"><span data-stu-id="f3427-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="f3427-117">成本</span><span class="sxs-lookup"><span data-stu-id="f3427-117">Cost</span></span>
        - <span data-ttu-id="f3427-118">薪資分攤</span><span class="sxs-lookup"><span data-stu-id="f3427-118">Payroll allocation</span></span>
        - <span data-ttu-id="f3427-119">WIP 成本值</span><span class="sxs-lookup"><span data-stu-id="f3427-119">WIP-cost value</span></span>
        - <span data-ttu-id="f3427-120">成本項目</span><span class="sxs-lookup"><span data-stu-id="f3427-120">Cost-item</span></span>
        - <span data-ttu-id="f3427-121">WIP 成本值項目</span><span class="sxs-lookup"><span data-stu-id="f3427-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="f3427-122">應計損失</span><span class="sxs-lookup"><span data-stu-id="f3427-122">Accrued loss</span></span>
        - <span data-ttu-id="f3427-123">WIP 應計損失</span><span class="sxs-lookup"><span data-stu-id="f3427-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="f3427-124">下列營收來源會使用哪個收入科目？</span><span class="sxs-lookup"><span data-stu-id="f3427-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="f3427-125">已開發票營收</span><span class="sxs-lookup"><span data-stu-id="f3427-125">Invoiced revenue</span></span>
        - <span data-ttu-id="f3427-126">應計收入 - 銷售值</span><span class="sxs-lookup"><span data-stu-id="f3427-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="f3427-127">WIP - 銷售值</span><span class="sxs-lookup"><span data-stu-id="f3427-127">WIP-sales value</span></span>
        - <span data-ttu-id="f3427-128">應計收入 - 生產</span><span class="sxs-lookup"><span data-stu-id="f3427-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="f3427-129">WIP - 生產</span><span class="sxs-lookup"><span data-stu-id="f3427-129">WIP-production</span></span>
        - <span data-ttu-id="f3427-130">應計收入 - 利潤</span><span class="sxs-lookup"><span data-stu-id="f3427-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="f3427-131">WIP - 利潤</span><span class="sxs-lookup"><span data-stu-id="f3427-131">WIP-profit</span></span>
        - <span data-ttu-id="f3427-132">應計收入 - 訂閱</span><span class="sxs-lookup"><span data-stu-id="f3427-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="f3427-133">WIP - 訂閱</span><span class="sxs-lookup"><span data-stu-id="f3427-133">WIP-subscription</span></span>

- <span data-ttu-id="f3427-134">什麼是費用類型？</span><span class="sxs-lookup"><span data-stu-id="f3427-134">What is the expense type?</span></span>
- <span data-ttu-id="f3427-135">什麼是費用類別的預設付款方式？</span><span class="sxs-lookup"><span data-stu-id="f3427-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="f3427-136">費用類別中的費用是否必須逐條列舉？</span><span class="sxs-lookup"><span data-stu-id="f3427-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="f3427-137">什麼是費用類別的主要預設科目？</span><span class="sxs-lookup"><span data-stu-id="f3427-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="f3427-138">什麼是費用類別的預設項目銷售課稅群組？</span><span class="sxs-lookup"><span data-stu-id="f3427-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="f3427-139">費用類別是否允許其他付款方式？</span><span class="sxs-lookup"><span data-stu-id="f3427-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="f3427-140">如果是，有哪些？</span><span class="sxs-lookup"><span data-stu-id="f3427-140">If so, what are they?</span></span>
- <span data-ttu-id="f3427-141">此費用類別中是否有子類別？</span><span class="sxs-lookup"><span data-stu-id="f3427-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="f3427-142">如果有子類別，您還必須做出下列決定：</span><span class="sxs-lookup"><span data-stu-id="f3427-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="f3427-143">是否有任何子類別不在稅金退還之列？</span><span class="sxs-lookup"><span data-stu-id="f3427-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="f3427-144">什麼是子類別的項目銷售課稅群組？</span><span class="sxs-lookup"><span data-stu-id="f3427-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]