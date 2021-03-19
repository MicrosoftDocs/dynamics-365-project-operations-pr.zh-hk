---
title: 實際值概觀
description: 本主題提供有關專案實際值的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285645"
---
# <a name="actuals-overview"></a><span data-ttu-id="a67a5-103">實際值概觀</span><span class="sxs-lookup"><span data-stu-id="a67a5-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a67a5-104">實際值是專案中已完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="a67a5-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a67a5-105">專案實際值可以追溯至其原始憑證。</span><span class="sxs-lookup"><span data-stu-id="a67a5-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a67a5-106">這些原始憑證包括時間項目、費用項目與帳目分錄以及發票。</span><span class="sxs-lookup"><span data-stu-id="a67a5-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![如何將專案實際值追蹤至原始憑證](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a67a5-108">送出時間項目</span><span class="sxs-lookup"><span data-stu-id="a67a5-108">Submitting a time entry</span></span>

<span data-ttu-id="a67a5-109">在 PSA 中，將對應至時間及材料合約服務內容之專案的時間項目送出時，會建立兩個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a67a5-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a67a5-110">一項明細用於成本，而另一項用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="a67a5-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a67a5-111">將對應至固定價格合約服務內容之專案的時間項目送出時，只會建立成本的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a67a5-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a67a5-112">輸入預設價格的邏輯會存在於帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a67a5-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a67a5-113">時間項目中的所有欄位值都會複製到帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a67a5-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a67a5-114">這些欄位包括交易的日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。</span><span class="sxs-lookup"><span data-stu-id="a67a5-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a67a5-115">影響預設價格的欄位 (例如 **角色** 和 **組織單位**) 會產生要在帳目明細上依預設輸入的適當價格。</span><span class="sxs-lookup"><span data-stu-id="a67a5-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a67a5-116">如果在時間項目上新增自訂欄位，而且您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。</span><span class="sxs-lookup"><span data-stu-id="a67a5-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a67a5-117">送出費用項目</span><span class="sxs-lookup"><span data-stu-id="a67a5-117">Submitting an expense entry</span></span>

<span data-ttu-id="a67a5-118">在 PSA 中，將對應至時間及材料合約服務內容之專案的費用項目送出時，會建立兩個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a67a5-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a67a5-119">一項明細用於成本，而另一項用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="a67a5-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a67a5-120">將對應至固定價格合約服務內容之專案的費用項目送出時，只會建立成本的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a67a5-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a67a5-121">輸入費用預設價格的邏輯是根據您在 **費用項目** 頁面上選取的費用類別。</span><span class="sxs-lookup"><span data-stu-id="a67a5-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a67a5-122">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="a67a5-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a67a5-123">不過，就價格本身而言，使用者輸入的金額預設會直接設定在成本和銷售的相關費用帳目明細上。</span><span class="sxs-lookup"><span data-stu-id="a67a5-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a67a5-124">在目前的 PSA 版本中，依類別輸入的每單位預設價格無法在費用項目上使用。</span><span class="sxs-lookup"><span data-stu-id="a67a5-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="a67a5-125">使用分錄帳目來記錄成本</span><span class="sxs-lookup"><span data-stu-id="a67a5-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="a67a5-126">在 PSA 中，您可以使用分錄帳目來記錄材料、費用、時間、支出或稅務交易分類中的成本或營收。</span><span class="sxs-lookup"><span data-stu-id="a67a5-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a67a5-127">帳目有標題、明細和 **確認** 動作。</span><span class="sxs-lookup"><span data-stu-id="a67a5-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a67a5-128">以下是一些您可能會使用帳目的情況：</span><span class="sxs-lookup"><span data-stu-id="a67a5-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a67a5-129">您必須在專案上記錄材料實際成本和銷售。</span><span class="sxs-lookup"><span data-stu-id="a67a5-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a67a5-130">您必須將交易實際值從其他系統移至 PSA。</span><span class="sxs-lookup"><span data-stu-id="a67a5-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a67a5-131">您必須記錄其他系統中發生的成本 (例如採購或轉承包成本)。</span><span class="sxs-lookup"><span data-stu-id="a67a5-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a67a5-132">使用分錄帳目建立實際值的工作，只能由完全了解實際值對專案所產生之會計影響的使用者來完成。</span><span class="sxs-lookup"><span data-stu-id="a67a5-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="a67a5-133">這是因為應用程式不會驗證帳目明細類型，或帳目明細上所輸入的相關價格。</span><span class="sxs-lookup"><span data-stu-id="a67a5-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="a67a5-134">由於會有這種帳目類型的影響，請在授與何人建立分錄帳目的存取權限時，特別小心。</span><span class="sxs-lookup"><span data-stu-id="a67a5-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a67a5-135">根據專案事件記錄實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-135">Recording actuals based on project events</span></span>

<span data-ttu-id="a67a5-136">PSA 會記錄專案期間發生的財務交易。</span><span class="sxs-lookup"><span data-stu-id="a67a5-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a67a5-137">這些交易記錄會以 **實際值** 來記錄。</span><span class="sxs-lookup"><span data-stu-id="a67a5-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a67a5-138">下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。</span><span class="sxs-lookup"><span data-stu-id="a67a5-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a67a5-139">**資源隸屬於與專案承包單位相同的組織單位**</span><span class="sxs-lookup"><span data-stu-id="a67a5-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a67a5-140">Event</span><span class="sxs-lookup"><span data-stu-id="a67a5-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a67a5-141">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="a67a5-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a67a5-142">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="a67a5-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a67a5-143">內部專案</span><span class="sxs-lookup"><span data-stu-id="a67a5-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a67a5-144">時間及材料</span><span class="sxs-lookup"><span data-stu-id="a67a5-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a67a5-145">固定價格</span><span class="sxs-lookup"><span data-stu-id="a67a5-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a67a5-146">實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-146">Actuals</span></span></th>
<th><span data-ttu-id="a67a5-147">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-147">Transaction currency</span></span></th>
<th><span data-ttu-id="a67a5-148">固定價格</span><span class="sxs-lookup"><span data-stu-id="a67a5-148">Fixed price</span></span></th>
<th><span data-ttu-id="a67a5-149">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a67a5-150">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="a67a5-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a67a5-151">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="a67a5-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-152">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="a67a5-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a67a5-153">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="a67a5-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a67a5-154">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="a67a5-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a67a5-155">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-155">Cost actual</span></span></td>
<td><span data-ttu-id="a67a5-156">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-157">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-158">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a67a5-159">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-160">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-161">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a67a5-162">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a67a5-163">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="a67a5-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a67a5-164">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-164">Cost actual</span></span></td>
<td><span data-ttu-id="a67a5-165">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-166">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-167">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-168">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-169">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-170">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a67a5-171">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-172">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a67a5-173">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a67a5-174">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="a67a5-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a67a5-175">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a67a5-176">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-177">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-178">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-179">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-180">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-181">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-181">Billed sales</span></span></td>
<td><span data-ttu-id="a67a5-182">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a67a5-183">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="a67a5-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a67a5-184">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a67a5-185">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-186">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-187">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-188">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-189">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-190">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a67a5-191">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-192">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a67a5-193">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a67a5-194">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="a67a5-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a67a5-195">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a67a5-196">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a67a5-197">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a67a5-198">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="a67a5-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a67a5-199">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-200">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-201">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-202">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-202">Billed sales</span></span></td>
<td><span data-ttu-id="a67a5-203">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a67a5-204">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="a67a5-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a67a5-205">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a67a5-206">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-207">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a67a5-208">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-209">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a67a5-210">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a67a5-211">**資源隸屬於與專案承包單位不同的組織單位**</span><span class="sxs-lookup"><span data-stu-id="a67a5-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a67a5-212">Event</span><span class="sxs-lookup"><span data-stu-id="a67a5-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a67a5-213">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="a67a5-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a67a5-214">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="a67a5-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a67a5-215">內部專案</span><span class="sxs-lookup"><span data-stu-id="a67a5-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a67a5-216">時間及材料</span><span class="sxs-lookup"><span data-stu-id="a67a5-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a67a5-217">固定價格</span><span class="sxs-lookup"><span data-stu-id="a67a5-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a67a5-218">實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-218">Actuals</span></span></th>
<th><span data-ttu-id="a67a5-219">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-219">Transaction currency</span></span></th>
<th><span data-ttu-id="a67a5-220">固定價格</span><span class="sxs-lookup"><span data-stu-id="a67a5-220">Fixed price</span></span></th>
<th><span data-ttu-id="a67a5-221">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a67a5-222">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="a67a5-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a67a5-223">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="a67a5-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-224">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="a67a5-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a67a5-225">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="a67a5-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a67a5-226">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="a67a5-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a67a5-227">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-227">Cost actual</span></span></td>
<td><span data-ttu-id="a67a5-228">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a67a5-229">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a67a5-230">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a67a5-231">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a67a5-232">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-233">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a67a5-234">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-235">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="a67a5-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a67a5-236">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-237">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a67a5-238">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a67a5-239">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="a67a5-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a67a5-240">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-240">Cost actual</span></span></td>
<td><span data-ttu-id="a67a5-241">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-242">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-243">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-244">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-245">成本實際值</span><span class="sxs-lookup"><span data-stu-id="a67a5-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-246">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="a67a5-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a67a5-247">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-248">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a67a5-249">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-250">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a67a5-251">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-252">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a67a5-253">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a67a5-254">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="a67a5-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a67a5-255">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a67a5-256">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-257">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-258">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-259">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a67a5-260">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-261">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-261">Billed sales</span></span></td>
<td><span data-ttu-id="a67a5-262">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a67a5-263">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="a67a5-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a67a5-264">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a67a5-265">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-266">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-267">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-268">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a67a5-269">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-270">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a67a5-271">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-272">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a67a5-273">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a67a5-274">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="a67a5-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a67a5-275">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a67a5-276">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a67a5-277">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a67a5-278">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="a67a5-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a67a5-279">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-280">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a67a5-281">不適用</span><span class="sxs-lookup"><span data-stu-id="a67a5-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-282">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-282">Billed sales</span></span></td>
<td><span data-ttu-id="a67a5-283">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a67a5-284">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="a67a5-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a67a5-285">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="a67a5-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a67a5-286">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-287">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="a67a5-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a67a5-288">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a67a5-289">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="a67a5-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a67a5-290">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="a67a5-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]