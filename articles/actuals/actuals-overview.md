---
title: 實際值
description: 本主題提供有關如何在 Microsoft Dynamics 365 Project Operations 中處理實際值的資訊。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087490"
---
# <a name="actuals"></a><span data-ttu-id="bfd64-103">實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-103">Actuals</span></span> 

<span data-ttu-id="bfd64-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="bfd64-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bfd64-105">實際值是專案中已完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="bfd64-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="bfd64-106">這些實際值是因時間和費用項目以及帳目分錄和發票而建立的。</span><span class="sxs-lookup"><span data-stu-id="bfd64-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="bfd64-107">帳目明細和時間提交</span><span class="sxs-lookup"><span data-stu-id="bfd64-107">Journal lines and time submission</span></span>

<span data-ttu-id="bfd64-108">如需時間項目的詳細資訊，請參閱 [時間項目概觀 ](../time/time-entry-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="bfd64-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="bfd64-109">時間及材料</span><span class="sxs-lookup"><span data-stu-id="bfd64-109">Time and materials</span></span>

<span data-ttu-id="bfd64-110">將提交的時間項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="bfd64-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="bfd64-111">固定價格</span><span class="sxs-lookup"><span data-stu-id="bfd64-111">Fixed price</span></span>

<span data-ttu-id="bfd64-112">將提交的時間項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="bfd64-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="bfd64-113">預設定價</span><span class="sxs-lookup"><span data-stu-id="bfd64-113">Default pricing</span></span>

<span data-ttu-id="bfd64-114">建立預設價格的邏輯會存在於帳目明細。</span><span class="sxs-lookup"><span data-stu-id="bfd64-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="bfd64-115">時間項目中的欄位值都會複製到帳目明細。</span><span class="sxs-lookup"><span data-stu-id="bfd64-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="bfd64-116">這些值包含交易日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。</span><span class="sxs-lookup"><span data-stu-id="bfd64-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="bfd64-117">影響預設定價的欄位 (例如 **角色** 和 **組織單位** ) 會在帳目明細上用來決定適當價格。</span><span class="sxs-lookup"><span data-stu-id="bfd64-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="bfd64-118">您可以在時間項目上新增自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="bfd64-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="bfd64-119">如果您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。</span><span class="sxs-lookup"><span data-stu-id="bfd64-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="bfd64-120">帳目明細和基本費用提交</span><span class="sxs-lookup"><span data-stu-id="bfd64-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="bfd64-121">如需費用項目的詳細資訊，請參閱 [費用概觀 ](../expense/expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="bfd64-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="bfd64-122">時間及材料</span><span class="sxs-lookup"><span data-stu-id="bfd64-122">Time and materials</span></span>

<span data-ttu-id="bfd64-123">將提交的基本費用項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="bfd64-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="bfd64-124">固定價格</span><span class="sxs-lookup"><span data-stu-id="bfd64-124">Fixed price</span></span>

<span data-ttu-id="bfd64-125">將提交的基本費用項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="bfd64-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="bfd64-126">預設定價</span><span class="sxs-lookup"><span data-stu-id="bfd64-126">Default pricing</span></span>

<span data-ttu-id="bfd64-127">輸入費用的預設價格的邏輯是根據費用類別而定。</span><span class="sxs-lookup"><span data-stu-id="bfd64-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="bfd64-128">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="bfd64-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="bfd64-129">不過，使用者就價格本身所輸入的金額預設會直接在成本和銷售的相關費用帳目明細上設定。</span><span class="sxs-lookup"><span data-stu-id="bfd64-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="bfd64-130">依類別輸入的每單位預設價格無法在費用項目上使用。</span><span class="sxs-lookup"><span data-stu-id="bfd64-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="bfd64-131">使用分錄帳目來記錄成本</span><span class="sxs-lookup"><span data-stu-id="bfd64-131">Use entry journals to record costs</span></span>

<span data-ttu-id="bfd64-132">您可以使用分錄帳目來記錄材料、服務費、時間、費用或稅務交易分類中的成本或營收。</span><span class="sxs-lookup"><span data-stu-id="bfd64-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="bfd64-133">帳目可用於下列用途：</span><span class="sxs-lookup"><span data-stu-id="bfd64-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="bfd64-134">記錄專案上的材料及銷售實際成本。</span><span class="sxs-lookup"><span data-stu-id="bfd64-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="bfd64-135">將交易實際值從系統移至 Microsoft Dynamics 365 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="bfd64-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="bfd64-136">記錄其他系統中發生的成本。</span><span class="sxs-lookup"><span data-stu-id="bfd64-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="bfd64-137">這些成本可以包含採購或轉承包成本。</span><span class="sxs-lookup"><span data-stu-id="bfd64-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfd64-138">應用程式不會驗證帳目明細類型或是帳目明細上所輸入的相關定價。</span><span class="sxs-lookup"><span data-stu-id="bfd64-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="bfd64-139">因此，只有完全了解實際值對專案所產生之會計影響的使用者，才應使用帳目來建立實際值。</span><span class="sxs-lookup"><span data-stu-id="bfd64-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="bfd64-140">由於會有這種帳目類型的影響，您必須小心選擇有存取權限可建立分錄帳目的人員。</span><span class="sxs-lookup"><span data-stu-id="bfd64-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="bfd64-141">根據專案事件記錄實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-141">Record actuals based on project events</span></span>

<span data-ttu-id="bfd64-142">Project Operations 會記錄專案期間發生的財務交易。</span><span class="sxs-lookup"><span data-stu-id="bfd64-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="bfd64-143">這些交易記錄會以實際值來記錄。</span><span class="sxs-lookup"><span data-stu-id="bfd64-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="bfd64-144">下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。</span><span class="sxs-lookup"><span data-stu-id="bfd64-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="bfd64-145">資源隸屬於與專案承包單位相同的組織單位</span><span class="sxs-lookup"><span data-stu-id="bfd64-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bfd64-146">Event</span><span class="sxs-lookup"><span data-stu-id="bfd64-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bfd64-147">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="bfd64-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bfd64-148">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="bfd64-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bfd64-149">內部專案</span><span class="sxs-lookup"><span data-stu-id="bfd64-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bfd64-150">時間及材料</span><span class="sxs-lookup"><span data-stu-id="bfd64-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bfd64-151">固定價格</span><span class="sxs-lookup"><span data-stu-id="bfd64-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bfd64-152">實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-152">Actuals</span></span></th>
<th><span data-ttu-id="bfd64-153">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-153">Transaction currency</span></span></th>
<th><span data-ttu-id="bfd64-154">固定價格</span><span class="sxs-lookup"><span data-stu-id="bfd64-154">Fixed price</span></span></th>
<th><span data-ttu-id="bfd64-155">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bfd64-156">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="bfd64-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bfd64-157">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="bfd64-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-158">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="bfd64-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bfd64-159">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="bfd64-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfd64-160">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="bfd64-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfd64-161">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-161">Cost actual</span></span></td>
<td><span data-ttu-id="bfd64-162">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-163">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-164">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="bfd64-165">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-166">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-167">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bfd64-168">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfd64-169">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="bfd64-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfd64-170">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-170">Cost actual</span></span></td>
<td><span data-ttu-id="bfd64-171">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-172">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-173">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-174">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-175">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-176">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfd64-177">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-178">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfd64-179">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfd64-180">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="bfd64-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfd64-181">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfd64-182">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-183">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-184">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-185">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-186">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-187">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-187">Billed sales</span></span></td>
<td><span data-ttu-id="bfd64-188">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfd64-189">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="bfd64-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfd64-190">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfd64-191">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-192">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-193">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-194">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-195">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-196">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfd64-197">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-198">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfd64-199">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfd64-200">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="bfd64-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfd64-201">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfd64-202">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bfd64-203">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bfd64-204">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="bfd64-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bfd64-205">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-206">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-207">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-208">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-208">Billed sales</span></span></td>
<td><span data-ttu-id="bfd64-209">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfd64-210">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="bfd64-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfd64-211">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfd64-212">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-213">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bfd64-214">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-215">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfd64-216">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="bfd64-217">資源隸屬於與專案承包單位不同的組織單位</span><span class="sxs-lookup"><span data-stu-id="bfd64-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bfd64-218">Event</span><span class="sxs-lookup"><span data-stu-id="bfd64-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bfd64-219">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="bfd64-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bfd64-220">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="bfd64-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bfd64-221">內部專案</span><span class="sxs-lookup"><span data-stu-id="bfd64-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bfd64-222">時間及材料</span><span class="sxs-lookup"><span data-stu-id="bfd64-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bfd64-223">固定價格</span><span class="sxs-lookup"><span data-stu-id="bfd64-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bfd64-224">實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-224">Actuals</span></span></th>
<th><span data-ttu-id="bfd64-225">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-225">Transaction currency</span></span></th>
<th><span data-ttu-id="bfd64-226">固定價格</span><span class="sxs-lookup"><span data-stu-id="bfd64-226">Fixed price</span></span></th>
<th><span data-ttu-id="bfd64-227">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bfd64-228">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="bfd64-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bfd64-229">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="bfd64-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-230">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="bfd64-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bfd64-231">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="bfd64-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="bfd64-232">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="bfd64-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfd64-233">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-233">Cost actual</span></span></td>
<td><span data-ttu-id="bfd64-234">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bfd64-235">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bfd64-236">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bfd64-237">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bfd64-238">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-239">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bfd64-240">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-241">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="bfd64-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bfd64-242">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-243">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bfd64-244">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="bfd64-245">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="bfd64-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfd64-246">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-246">Cost actual</span></span></td>
<td><span data-ttu-id="bfd64-247">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-248">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-249">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-250">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-251">成本實際值</span><span class="sxs-lookup"><span data-stu-id="bfd64-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-252">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="bfd64-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bfd64-253">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-254">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bfd64-255">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-256">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfd64-257">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-258">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfd64-259">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfd64-260">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="bfd64-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfd64-261">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfd64-262">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-263">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-264">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-265">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bfd64-266">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-267">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-267">Billed sales</span></span></td>
<td><span data-ttu-id="bfd64-268">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfd64-269">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="bfd64-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfd64-270">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfd64-271">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-272">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-273">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-274">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfd64-275">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-276">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfd64-277">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-278">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfd64-279">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfd64-280">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="bfd64-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfd64-281">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfd64-282">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bfd64-283">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bfd64-284">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="bfd64-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bfd64-285">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-286">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bfd64-287">不適用</span><span class="sxs-lookup"><span data-stu-id="bfd64-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-288">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-288">Billed sales</span></span></td>
<td><span data-ttu-id="bfd64-289">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfd64-290">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="bfd64-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfd64-291">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="bfd64-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfd64-292">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-293">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="bfd64-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bfd64-294">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfd64-295">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="bfd64-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfd64-296">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="bfd64-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
