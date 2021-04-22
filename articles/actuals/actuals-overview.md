---
title: 實際值
description: 本主題提供有關如何在 Microsoft Dynamics 365 Project Operations 中處理實際值的資訊。
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852571"
---
# <a name="actuals"></a><span data-ttu-id="33dad-103">實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-103">Actuals</span></span> 

<span data-ttu-id="33dad-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="33dad-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33dad-105">實際值表示專案上已審查且核准的財務及排程進度。</span><span class="sxs-lookup"><span data-stu-id="33dad-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="33dad-106">這些值是因為核准時間、費用、材料使用項目以及帳目分錄和發票而產生。</span><span class="sxs-lookup"><span data-stu-id="33dad-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="33dad-107">帳目明細和時間提交</span><span class="sxs-lookup"><span data-stu-id="33dad-107">Journal lines and time submission</span></span>

<span data-ttu-id="33dad-108">如需時間項目的詳細資訊，請參閱 [時間項目概觀 ](../time/time-entry-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="33dad-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="33dad-109">時間及材料</span><span class="sxs-lookup"><span data-stu-id="33dad-109">Time and materials</span></span>

<span data-ttu-id="33dad-110">將提交的時間項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="33dad-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="33dad-111">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-111">Fixed price</span></span>

<span data-ttu-id="33dad-112">將提交的時間項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="33dad-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="33dad-113">預設定價</span><span class="sxs-lookup"><span data-stu-id="33dad-113">Default pricing</span></span>

<span data-ttu-id="33dad-114">建立預設價格的邏輯會存在於帳目明細。</span><span class="sxs-lookup"><span data-stu-id="33dad-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="33dad-115">時間項目中的欄位值都會複製到帳目明細。</span><span class="sxs-lookup"><span data-stu-id="33dad-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="33dad-116">這些值包含交易日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。</span><span class="sxs-lookup"><span data-stu-id="33dad-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="33dad-117">影響預設定價的欄位 (例如 **角色** 和 **資源分配單位**) 會用來決定帳目明細上的適當價格。</span><span class="sxs-lookup"><span data-stu-id="33dad-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="33dad-118">您可以在時間項目上新增自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="33dad-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="33dad-119">如果您希望欄位值傳播至實際值，請在 **實際值** 和 **帳目明細** 資料表中建立欄位。</span><span class="sxs-lookup"><span data-stu-id="33dad-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="33dad-120">利用自訂程式碼，使用交易來源透過帳目明細將選取的欄位值從時間項目傳播至實際值。</span><span class="sxs-lookup"><span data-stu-id="33dad-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="33dad-121">如需交易來源及人脈的詳細資訊，請參閱[將實際值連結至原始記錄](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。</span><span class="sxs-lookup"><span data-stu-id="33dad-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="33dad-122">帳目明細和基本費用提交</span><span class="sxs-lookup"><span data-stu-id="33dad-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="33dad-123">如需費用項目的詳細資訊，請參閱 [費用概觀 ](../expense/expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="33dad-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="33dad-124">時間及材料</span><span class="sxs-lookup"><span data-stu-id="33dad-124">Time and materials</span></span>

<span data-ttu-id="33dad-125">將提交的基本費用項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="33dad-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="33dad-126">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-126">Fixed price</span></span>

<span data-ttu-id="33dad-127">當送出的基本費用項目已與對應至固定價格合約服務內容的專案連結時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="33dad-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="33dad-128">預設定價</span><span class="sxs-lookup"><span data-stu-id="33dad-128">Default pricing</span></span>

<span data-ttu-id="33dad-129">輸入費用的預設價格的邏輯是根據費用類別而定。</span><span class="sxs-lookup"><span data-stu-id="33dad-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="33dad-130">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="33dad-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="33dad-131">影響預設定價的欄位 (例如 **角色** 和 **交易類別**) 會用來決定帳目明細上的適當價格。</span><span class="sxs-lookup"><span data-stu-id="33dad-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="33dad-132">不過，這只有在價目表的定價方式是 **單價** 時才適用。</span><span class="sxs-lookup"><span data-stu-id="33dad-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="33dad-133">如果定價方式是 **依照成本** 或 **成本加成**，則成本會使用建立費用項目時所輸入的價格，而銷售帳目明細的價格則是根據定價方式進行計算。</span><span class="sxs-lookup"><span data-stu-id="33dad-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="33dad-134">您可以在費用項目上新增自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="33dad-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="33dad-135">如果您希望欄位值傳播至實際值，請在 **實際值** 和 **帳目明細** 資料表中建立欄位。</span><span class="sxs-lookup"><span data-stu-id="33dad-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="33dad-136">利用自訂程式碼，使用交易來源透過帳目明細將選取的欄位值從時間項目傳播至實際值。</span><span class="sxs-lookup"><span data-stu-id="33dad-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="33dad-137">如需交易來源及人脈的詳細資訊，請參閱[將實際值連結至原始記錄](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。</span><span class="sxs-lookup"><span data-stu-id="33dad-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="33dad-138">帳目明細及材料使用記錄送出</span><span class="sxs-lookup"><span data-stu-id="33dad-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="33dad-139">如需費用項目的詳細資訊，請參閱[材料使用記錄](../material/material-usage-log.md)。</span><span class="sxs-lookup"><span data-stu-id="33dad-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="33dad-140">時間及材料</span><span class="sxs-lookup"><span data-stu-id="33dad-140">Time and materials</span></span>

<span data-ttu-id="33dad-141">將送出的材料使用記錄項目與對應至時間及材料合約服務內容的專案連結時，系統會建立兩個帳目明細，一個用於成本，一個用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="33dad-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="33dad-142">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-142">Fixed price</span></span>

<span data-ttu-id="33dad-143">當送出的材料使用記錄項目已與對應至固定價格合約服務內容的專案連結時，系統會為成本建立一個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="33dad-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="33dad-144">預設定價</span><span class="sxs-lookup"><span data-stu-id="33dad-144">Default pricing</span></span>

<span data-ttu-id="33dad-145">輸入材料預設價格的邏輯是根據產品與單位組合而定。</span><span class="sxs-lookup"><span data-stu-id="33dad-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="33dad-146">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="33dad-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="33dad-147">影響預設定價的欄位 (例如 **角色** 和 **產品識別碼**) 會用來決定帳目明細上的適當價格。</span><span class="sxs-lookup"><span data-stu-id="33dad-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="33dad-148">不過，這只適用於目錄產品。</span><span class="sxs-lookup"><span data-stu-id="33dad-148">However, this only works for catalog products.</span></span> <span data-ttu-id="33dad-149">如果是目錄外產品，則將建立材料使用記錄項目時所輸入的價格用於帳目明細上的成本和售價。</span><span class="sxs-lookup"><span data-stu-id="33dad-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="33dad-150">您可以在 **材料使用記錄** 項目上新增自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="33dad-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="33dad-151">如果您希望欄位值傳播至實際值，請在 **實際值** 和 **帳目明細** 資料表中建立欄位。</span><span class="sxs-lookup"><span data-stu-id="33dad-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="33dad-152">利用自訂程式碼，使用交易來源透過帳目明細將選取的欄位值從時間項目傳播至實際值。</span><span class="sxs-lookup"><span data-stu-id="33dad-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="33dad-153">如需交易來源及人脈的詳細資訊，請參閱[將實際值連結至原始記錄](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。</span><span class="sxs-lookup"><span data-stu-id="33dad-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="33dad-154">使用分錄帳目來記錄成本</span><span class="sxs-lookup"><span data-stu-id="33dad-154">Use entry journals to record costs</span></span>

<span data-ttu-id="33dad-155">您可以使用分錄帳目來記錄材料、服務費、時間、費用或稅務交易分類中的成本或營收。</span><span class="sxs-lookup"><span data-stu-id="33dad-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="33dad-156">帳目可用於下列用途：</span><span class="sxs-lookup"><span data-stu-id="33dad-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="33dad-157">將交易實際值從其他系統移到 Microsoft Dynamics 365 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="33dad-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="33dad-158">記錄其他系統中發生的成本。</span><span class="sxs-lookup"><span data-stu-id="33dad-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="33dad-159">這些成本可以包含採購或轉承包成本。</span><span class="sxs-lookup"><span data-stu-id="33dad-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33dad-160">應用程式不會驗證帳目明細類型或是帳目明細上所輸入的相關定價。</span><span class="sxs-lookup"><span data-stu-id="33dad-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="33dad-161">因此，只有完全了解實際值對專案所產生之會計影響的使用者，才應使用帳目來建立實際值。</span><span class="sxs-lookup"><span data-stu-id="33dad-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="33dad-162">由於會有這種帳目類型的影響，您必須小心選擇有存取權限可建立分錄帳目的人員。</span><span class="sxs-lookup"><span data-stu-id="33dad-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="33dad-163">根據專案事件記錄實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-163">Record actuals based on project events</span></span>

<span data-ttu-id="33dad-164">Project Operations 會記錄專案期間發生的財務交易。</span><span class="sxs-lookup"><span data-stu-id="33dad-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="33dad-165">這些交易記錄會以實際值來記錄。</span><span class="sxs-lookup"><span data-stu-id="33dad-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="33dad-166">下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。</span><span class="sxs-lookup"><span data-stu-id="33dad-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="33dad-167">資源隸屬於與專案承包單位相同的組織單位</span><span class="sxs-lookup"><span data-stu-id="33dad-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="33dad-168">Event</span><span class="sxs-lookup"><span data-stu-id="33dad-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="33dad-169">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="33dad-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="33dad-170">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="33dad-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="33dad-171">內部專案</span><span class="sxs-lookup"><span data-stu-id="33dad-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="33dad-172">時間及材料</span><span class="sxs-lookup"><span data-stu-id="33dad-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="33dad-173">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33dad-174">實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-174">Actuals</span></span></th>
<th><span data-ttu-id="33dad-175">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-175">Transaction currency</span></span></th>
<th><span data-ttu-id="33dad-176">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-176">Fixed price</span></span></th>
<th><span data-ttu-id="33dad-177">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33dad-178">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="33dad-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="33dad-179">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="33dad-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-180">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="33dad-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="33dad-181">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="33dad-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33dad-182">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="33dad-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33dad-183">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-183">Cost actual</span></span></td>
<td><span data-ttu-id="33dad-184">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-185">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-186">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="33dad-187">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-188">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-189">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="33dad-190">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33dad-191">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="33dad-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33dad-192">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-192">Cost actual</span></span></td>
<td><span data-ttu-id="33dad-193">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-194">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-195">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-196">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-197">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-198">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33dad-199">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-200">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33dad-201">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33dad-202">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="33dad-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33dad-203">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33dad-204">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-205">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-206">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-207">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-208">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-209">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-209">Billed sales</span></span></td>
<td><span data-ttu-id="33dad-210">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33dad-211">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="33dad-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33dad-212">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33dad-213">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-214">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-215">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-216">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-217">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-218">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33dad-219">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-220">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33dad-221">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33dad-222">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="33dad-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33dad-223">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33dad-224">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="33dad-225">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="33dad-226">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="33dad-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="33dad-227">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-228">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-229">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-230">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-230">Billed sales</span></span></td>
<td><span data-ttu-id="33dad-231">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33dad-232">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="33dad-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33dad-233">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33dad-234">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-235">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="33dad-236">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-237">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="33dad-238">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="33dad-239">資源隸屬於與專案承包單位不同的組織單位</span><span class="sxs-lookup"><span data-stu-id="33dad-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="33dad-240">Event</span><span class="sxs-lookup"><span data-stu-id="33dad-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="33dad-241">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="33dad-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="33dad-242">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="33dad-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="33dad-243">內部專案</span><span class="sxs-lookup"><span data-stu-id="33dad-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="33dad-244">時間及材料</span><span class="sxs-lookup"><span data-stu-id="33dad-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="33dad-245">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33dad-246">實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-246">Actuals</span></span></th>
<th><span data-ttu-id="33dad-247">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-247">Transaction currency</span></span></th>
<th><span data-ttu-id="33dad-248">固定價格</span><span class="sxs-lookup"><span data-stu-id="33dad-248">Fixed price</span></span></th>
<th><span data-ttu-id="33dad-249">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33dad-250">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="33dad-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="33dad-251">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="33dad-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-252">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="33dad-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="33dad-253">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="33dad-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="33dad-254">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="33dad-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33dad-255">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-255">Cost actual</span></span></td>
<td><span data-ttu-id="33dad-256">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="33dad-257">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="33dad-258">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="33dad-259">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="33dad-260">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-261">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="33dad-262">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-263">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="33dad-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="33dad-264">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-265">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="33dad-266">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="33dad-267">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="33dad-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33dad-268">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-268">Cost actual</span></span></td>
<td><span data-ttu-id="33dad-269">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-270">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-271">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-272">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-273">成本實際值</span><span class="sxs-lookup"><span data-stu-id="33dad-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-274">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="33dad-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="33dad-275">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-276">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="33dad-277">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-278">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33dad-279">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-280">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33dad-281">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33dad-282">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="33dad-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33dad-283">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33dad-284">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-285">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-286">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-287">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="33dad-288">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-289">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-289">Billed sales</span></span></td>
<td><span data-ttu-id="33dad-290">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33dad-291">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="33dad-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33dad-292">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33dad-293">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-294">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-295">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-296">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33dad-297">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-298">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33dad-299">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-300">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33dad-301">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33dad-302">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="33dad-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33dad-303">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33dad-304">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="33dad-305">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="33dad-306">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="33dad-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="33dad-307">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-308">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="33dad-309">不適用</span><span class="sxs-lookup"><span data-stu-id="33dad-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-310">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-310">Billed sales</span></span></td>
<td><span data-ttu-id="33dad-311">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33dad-312">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="33dad-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33dad-313">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="33dad-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33dad-314">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-315">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="33dad-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="33dad-316">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33dad-317">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="33dad-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="33dad-318">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="33dad-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
