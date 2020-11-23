---
title: 實際值
description: 本主題提供有關如何在 Microsoft Dynamics 365 Project Operations 中處理實際值的資訊。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126354"
---
# <a name="actuals"></a><span data-ttu-id="87db9-103">實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-103">Actuals</span></span> 

<span data-ttu-id="87db9-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="87db9-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87db9-105">實際值是專案中已完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="87db9-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="87db9-106">這些實際值是因時間和費用項目以及帳目分錄和發票而建立的。</span><span class="sxs-lookup"><span data-stu-id="87db9-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="87db9-107">帳目明細和時間提交</span><span class="sxs-lookup"><span data-stu-id="87db9-107">Journal lines and time submission</span></span>

<span data-ttu-id="87db9-108">如需時間項目的詳細資訊，請參閱 [時間項目概觀 ](../time/time-entry-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="87db9-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="87db9-109">時間及材料</span><span class="sxs-lookup"><span data-stu-id="87db9-109">Time and materials</span></span>

<span data-ttu-id="87db9-110">將提交的時間項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="87db9-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="87db9-111">固定價格</span><span class="sxs-lookup"><span data-stu-id="87db9-111">Fixed price</span></span>

<span data-ttu-id="87db9-112">將提交的時間項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="87db9-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="87db9-113">預設定價</span><span class="sxs-lookup"><span data-stu-id="87db9-113">Default pricing</span></span>

<span data-ttu-id="87db9-114">建立預設價格的邏輯會存在於帳目明細。</span><span class="sxs-lookup"><span data-stu-id="87db9-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="87db9-115">時間項目中的欄位值都會複製到帳目明細。</span><span class="sxs-lookup"><span data-stu-id="87db9-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="87db9-116">這些值包含交易日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。</span><span class="sxs-lookup"><span data-stu-id="87db9-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="87db9-117">影響預設定價的欄位 (例如 **角色** 和 **組織單位**) 會在帳目明細上用來決定適當價格。</span><span class="sxs-lookup"><span data-stu-id="87db9-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="87db9-118">您可以在時間項目上新增自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="87db9-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="87db9-119">如果您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。</span><span class="sxs-lookup"><span data-stu-id="87db9-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="87db9-120">帳目明細和基本費用提交</span><span class="sxs-lookup"><span data-stu-id="87db9-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="87db9-121">如需費用項目的詳細資訊，請參閱 [費用概觀 ](../expense/expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="87db9-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="87db9-122">時間及材料</span><span class="sxs-lookup"><span data-stu-id="87db9-122">Time and materials</span></span>

<span data-ttu-id="87db9-123">將提交的基本費用項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="87db9-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="87db9-124">固定價格</span><span class="sxs-lookup"><span data-stu-id="87db9-124">Fixed price</span></span>

<span data-ttu-id="87db9-125">將提交的基本費用項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="87db9-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="87db9-126">預設定價</span><span class="sxs-lookup"><span data-stu-id="87db9-126">Default pricing</span></span>

<span data-ttu-id="87db9-127">輸入費用的預設價格的邏輯是根據費用類別而定。</span><span class="sxs-lookup"><span data-stu-id="87db9-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="87db9-128">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="87db9-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="87db9-129">不過，使用者就價格本身所輸入的金額預設會直接在成本和銷售的相關費用帳目明細上設定。</span><span class="sxs-lookup"><span data-stu-id="87db9-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="87db9-130">依類別輸入的每單位預設價格無法在費用項目上使用。</span><span class="sxs-lookup"><span data-stu-id="87db9-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="87db9-131">使用分錄帳目來記錄成本</span><span class="sxs-lookup"><span data-stu-id="87db9-131">Use entry journals to record costs</span></span>

<span data-ttu-id="87db9-132">您可以使用分錄帳目來記錄材料、服務費、時間、費用或稅務交易分類中的成本或營收。</span><span class="sxs-lookup"><span data-stu-id="87db9-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="87db9-133">帳目可用於下列用途：</span><span class="sxs-lookup"><span data-stu-id="87db9-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="87db9-134">記錄專案上的材料及銷售實際成本。</span><span class="sxs-lookup"><span data-stu-id="87db9-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="87db9-135">將交易實際值從系統移至 Microsoft Dynamics 365 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="87db9-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="87db9-136">記錄其他系統中發生的成本。</span><span class="sxs-lookup"><span data-stu-id="87db9-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="87db9-137">這些成本可以包含採購或轉承包成本。</span><span class="sxs-lookup"><span data-stu-id="87db9-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87db9-138">應用程式不會驗證帳目明細類型或是帳目明細上所輸入的相關定價。</span><span class="sxs-lookup"><span data-stu-id="87db9-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="87db9-139">因此，只有完全了解實際值對專案所產生之會計影響的使用者，才應使用帳目來建立實際值。</span><span class="sxs-lookup"><span data-stu-id="87db9-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="87db9-140">由於會有這種帳目類型的影響，您必須小心選擇有存取權限可建立分錄帳目的人員。</span><span class="sxs-lookup"><span data-stu-id="87db9-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="87db9-141">根據專案事件記錄實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-141">Record actuals based on project events</span></span>

<span data-ttu-id="87db9-142">Project Operations 會記錄專案期間發生的財務交易。</span><span class="sxs-lookup"><span data-stu-id="87db9-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="87db9-143">這些交易記錄會以實際值來記錄。</span><span class="sxs-lookup"><span data-stu-id="87db9-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="87db9-144">下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。</span><span class="sxs-lookup"><span data-stu-id="87db9-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="87db9-145">資源隸屬於與專案承包單位相同的組織單位</span><span class="sxs-lookup"><span data-stu-id="87db9-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="87db9-146">Event</span><span class="sxs-lookup"><span data-stu-id="87db9-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="87db9-147">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="87db9-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="87db9-148">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="87db9-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="87db9-149">內部專案</span><span class="sxs-lookup"><span data-stu-id="87db9-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="87db9-150">時間及材料</span><span class="sxs-lookup"><span data-stu-id="87db9-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="87db9-151">固定價格</span><span class="sxs-lookup"><span data-stu-id="87db9-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="87db9-152">實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-152">Actuals</span></span></th>
<th><span data-ttu-id="87db9-153">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-153">Transaction currency</span></span></th>
<th><span data-ttu-id="87db9-154">固定價格</span><span class="sxs-lookup"><span data-stu-id="87db9-154">Fixed price</span></span></th>
<th><span data-ttu-id="87db9-155">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="87db9-156">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="87db9-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="87db9-157">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="87db9-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-158">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="87db9-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="87db9-159">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="87db9-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="87db9-160">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="87db9-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="87db9-161">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-161">Cost actual</span></span></td>
<td><span data-ttu-id="87db9-162">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-163">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-164">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="87db9-165">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-166">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-167">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="87db9-168">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="87db9-169">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="87db9-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="87db9-170">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-170">Cost actual</span></span></td>
<td><span data-ttu-id="87db9-171">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-172">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-173">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-174">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-175">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-176">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="87db9-177">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-178">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="87db9-179">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="87db9-180">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="87db9-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="87db9-181">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="87db9-182">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-183">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-184">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-185">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-186">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-187">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-187">Billed sales</span></span></td>
<td><span data-ttu-id="87db9-188">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="87db9-189">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="87db9-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="87db9-190">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="87db9-191">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-192">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-193">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-194">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-195">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-196">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="87db9-197">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-198">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="87db9-199">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="87db9-200">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="87db9-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="87db9-201">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="87db9-202">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="87db9-203">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="87db9-204">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="87db9-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="87db9-205">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-206">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-207">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-208">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-208">Billed sales</span></span></td>
<td><span data-ttu-id="87db9-209">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="87db9-210">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="87db9-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="87db9-211">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="87db9-212">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-213">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="87db9-214">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-215">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="87db9-216">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="87db9-217">資源隸屬於與專案承包單位不同的組織單位</span><span class="sxs-lookup"><span data-stu-id="87db9-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="87db9-218">Event</span><span class="sxs-lookup"><span data-stu-id="87db9-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="87db9-219">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="87db9-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="87db9-220">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="87db9-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="87db9-221">內部專案</span><span class="sxs-lookup"><span data-stu-id="87db9-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="87db9-222">時間及材料</span><span class="sxs-lookup"><span data-stu-id="87db9-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="87db9-223">固定價格</span><span class="sxs-lookup"><span data-stu-id="87db9-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="87db9-224">實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-224">Actuals</span></span></th>
<th><span data-ttu-id="87db9-225">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-225">Transaction currency</span></span></th>
<th><span data-ttu-id="87db9-226">固定價格</span><span class="sxs-lookup"><span data-stu-id="87db9-226">Fixed price</span></span></th>
<th><span data-ttu-id="87db9-227">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="87db9-228">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="87db9-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="87db9-229">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="87db9-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-230">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="87db9-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="87db9-231">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="87db9-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="87db9-232">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="87db9-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="87db9-233">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-233">Cost actual</span></span></td>
<td><span data-ttu-id="87db9-234">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="87db9-235">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="87db9-236">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="87db9-237">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="87db9-238">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-239">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="87db9-240">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-241">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="87db9-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="87db9-242">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-243">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="87db9-244">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="87db9-245">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="87db9-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="87db9-246">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-246">Cost actual</span></span></td>
<td><span data-ttu-id="87db9-247">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-248">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-249">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-250">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-251">成本實際值</span><span class="sxs-lookup"><span data-stu-id="87db9-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-252">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="87db9-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="87db9-253">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-254">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="87db9-255">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-256">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="87db9-257">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-258">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="87db9-259">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="87db9-260">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="87db9-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="87db9-261">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="87db9-262">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-263">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-264">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-265">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="87db9-266">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-267">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-267">Billed sales</span></span></td>
<td><span data-ttu-id="87db9-268">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="87db9-269">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="87db9-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="87db9-270">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="87db9-271">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-272">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-273">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-274">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="87db9-275">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-276">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="87db9-277">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-278">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="87db9-279">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="87db9-280">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="87db9-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="87db9-281">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="87db9-282">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="87db9-283">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="87db9-284">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="87db9-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="87db9-285">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-286">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="87db9-287">不適用</span><span class="sxs-lookup"><span data-stu-id="87db9-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-288">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-288">Billed sales</span></span></td>
<td><span data-ttu-id="87db9-289">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="87db9-290">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="87db9-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="87db9-291">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="87db9-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="87db9-292">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-293">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="87db9-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="87db9-294">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87db9-295">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="87db9-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="87db9-296">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="87db9-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
