---
title: 設定報價明細的應收費元件
description: 本主題提供有關設定專案型報價明細中應收費和不應收費元件的資訊。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003793"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="fa273-103">設定報價明細的應收費元件</span><span class="sxs-lookup"><span data-stu-id="fa273-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="fa273-104">_**適用於：** 精簡部署 - 交易至開立預估發票、資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="fa273-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fa273-105">專案型報價明細有 *內含* 元件和 *應收費* 元件的概念。</span><span class="sxs-lookup"><span data-stu-id="fa273-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="fa273-106">內含元件受限於下列各項：</span><span class="sxs-lookup"><span data-stu-id="fa273-106">Included components are subject to:</span></span>

  - <span data-ttu-id="fa273-107">帳務方式和客戶分割</span><span class="sxs-lookup"><span data-stu-id="fa273-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="fa273-108">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="fa273-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="fa273-109">專案型報價明細上定義的發票週期設定</span><span class="sxs-lookup"><span data-stu-id="fa273-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="fa273-110">您可以使用 **帳單類型** 欄位將一部分內含元件標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="fa273-111">**帳單類型** 欄位是選項組，允許在報價明細的情境下使用下列值：</span><span class="sxs-lookup"><span data-stu-id="fa273-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="fa273-112">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-112">Chargeable</span></span>
  - <span data-ttu-id="fa273-113">不應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-113">Non-chargeable</span></span>

<span data-ttu-id="fa273-114">您可以在工作、角色和交易類別上定義應收費元件。</span><span class="sxs-lookup"><span data-stu-id="fa273-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="fa273-115">可收費率是在報價明細的工作上所定義，並套用至該明細所包含的所有交易分類。</span><span class="sxs-lookup"><span data-stu-id="fa273-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="fa273-116">如果 **包含工作** 欄位已設定為 **整個專案** 或保持空白，則沒有提供 **應收費工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="fa273-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="fa273-117">報價明細的角色上所定義的可收費率只能套用至 **時間** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="fa273-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="fa273-118">如果 **包含時間** 欄位在專案報價明細上設定為 **否**，則沒有提供 **應收費角色** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="fa273-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="fa273-119">可收費率是在報價明細的交易類別上所定義，並且只能套用至 **費用** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="fa273-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="fa273-120">如果 **包含費用** 欄位在專案報價明細上設定為 **否**，則沒有提供 **應收費類別** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="fa273-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fa273-121">將專案工作更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fa273-122">專案工作在能使下列設定變成可行的特定專案型報價明細內容中可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="fa273-123">如果專案型報價明細包含 **時間** 和工作 **T1**，則工作會與報價明細建立應收費關聯。</span><span class="sxs-lookup"><span data-stu-id="fa273-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="fa273-124">如果有第二個報價明細，其中包含 **費用** 時，您可以將報價明細的 **T1** 工作關聯為不應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="fa273-125">結果是，工作中所記錄的所有時間都是應收費的，而工作中所記錄的所有費用都是不應收費的。</span><span class="sxs-lookup"><span data-stu-id="fa273-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="fa273-126">工作的帳單類型可以在專案型報價明細的 **應收費工作** 索引標籤上，透過更新 **報價明細工作** 子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="fa273-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="fa273-127">或者，也可以在顯示與工作相關之報價明細的專案工作帳單設定子格的 **帳單類型** 欄位中更新專案工作的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="fa273-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fa273-128">將角色更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fa273-129">角色在特定專案型報價明細的內容中，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="fa273-130">角色的帳單類型可以在報價明細的 **應收費角色** 索引標籤上，透過更新 **應收費角色** 子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="fa273-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fa273-131">將交易類別更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fa273-132">交易類別在特定報價明細上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="fa273-133">交易的帳單類型可以在報價明細的 **應收費類別** 索引標籤上，透過更新 **應收費類別** 子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="fa273-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="fa273-134">解析可收費率</span><span class="sxs-lookup"><span data-stu-id="fa273-134">Resolve chargeability</span></span>
<span data-ttu-id="fa273-135">只有在下列情況下，才能將針對時間建立的估計值或實際值視為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="fa273-136">**時間** 已包含在報價明細中。</span><span class="sxs-lookup"><span data-stu-id="fa273-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="fa273-137">**角色** 已在報價明細中設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="fa273-138">**包含的工作** 已在報價明細上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="fa273-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="fa273-139">如果這三種情況成立，**工作** 也會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="fa273-140">只有在下列情況下，才能將針對費用建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="fa273-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="fa273-141">**費用** 已包含在報價明細中。</span><span class="sxs-lookup"><span data-stu-id="fa273-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="fa273-142">**交易類別** 已在報價明細中設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="fa273-143">**包含的工作** 已在報價明細上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="fa273-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="fa273-144">如果這三種情況成立，**工作** 也會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="fa273-145">只有在下列情況下，才能將針對材料建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="fa273-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="fa273-146">**材料** 已包含在報價明細中。</span><span class="sxs-lookup"><span data-stu-id="fa273-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="fa273-147">**包含的工作** 已在報價明細上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="fa273-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="fa273-148">如果這兩種情況成立，**工作** 也應設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="fa273-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-149">
                    <strong>包含時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa273-150">
                    <strong>包含費用</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa273-151">
                    <strong>包含材料</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="fa273-152">
                    <strong>包含的工作</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-153">
                    <strong>角色</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-154">
                    <strong>類別</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-155">
                    <strong>工作​​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="fa273-156">
                    <strong>可收費率影響</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-157">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-158">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-159">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-160">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-161">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-162">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-163">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-164">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-165">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-166">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-167">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-168">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-169">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-170">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="fa273-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-171">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-172">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-173">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-174">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-175">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-176">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-177">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-178">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-179">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-180">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="fa273-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-181">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-182">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-183">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-184">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-185">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-186">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-187">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-188">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-189">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-190">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="fa273-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-191">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-192">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-193">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-194">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-195">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-196">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-197">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-198">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-199">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-200">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="fa273-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-201">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-202">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-203">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-204">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-205">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-206">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-207">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-208">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-209">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-210">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="fa273-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-211">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-212">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-213">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-214">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-215">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-216">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-217">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-218">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-219">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-220">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-221">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-222">
                    <strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-223">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-224">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-225">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-226">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-227">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-228">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-229">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-230">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-231">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-232">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-233">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-234">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-235">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-236">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-237">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa273-238">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-239">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-240">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-241">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-242">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-243">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-244">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-245">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-246">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-247">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa273-248">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa273-249">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-250">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-251">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-252">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-253">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-254">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-255">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-256">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-257">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-258">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa273-259">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-260">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-261">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-262">應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-263">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-264">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-265">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="fa273-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa273-266">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa273-267">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa273-268">.是</span><span class="sxs-lookup"><span data-stu-id="fa273-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa273-269">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa273-270">整個專案</span><span class="sxs-lookup"><span data-stu-id="fa273-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa273-271">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa273-272">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa273-273">無法設定</span><span class="sxs-lookup"><span data-stu-id="fa273-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa273-274">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-275">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa273-276">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa273-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
