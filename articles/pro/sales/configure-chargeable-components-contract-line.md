---
title: 設定專案型合約服務內容的應收費元件
description: 本主題提供有關如何在 Project Operations 中新增應收費元件至合約服務內容的資訊。
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003748"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="437c8-103">設定專案型合約服務內容的應收費元件</span><span class="sxs-lookup"><span data-stu-id="437c8-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="437c8-104">_**適用於：** 精簡部署 - 交易至開立預估發票、資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="437c8-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="437c8-105">專案型合約服務內容有 *包含* 元件和 *應收費* 元件。</span><span class="sxs-lookup"><span data-stu-id="437c8-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="437c8-106">內含元件是受限於下列各項的元件：</span><span class="sxs-lookup"><span data-stu-id="437c8-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="437c8-107">帳務方式和客戶分割</span><span class="sxs-lookup"><span data-stu-id="437c8-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="437c8-108">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="437c8-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="437c8-109">專案型合約服務內容上定義的發票週期設定</span><span class="sxs-lookup"><span data-stu-id="437c8-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="437c8-110">您可以使用 **帳單類型** 欄位將一部分內含元件標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="437c8-111">**帳單類型** 欄位是選項組，允許在合約服務內容的情境下使用下列值：</span><span class="sxs-lookup"><span data-stu-id="437c8-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="437c8-112">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-112">Chargeable</span></span>
  - <span data-ttu-id="437c8-113">不應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-113">Non-chargeable</span></span>

<span data-ttu-id="437c8-114">您可以在工作、角色和交易類別上定義應收費元件。</span><span class="sxs-lookup"><span data-stu-id="437c8-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="437c8-115">可收費率是在專案合約服務內容的工作上所定義，並套用至服務內容所包含的所有交易分類。</span><span class="sxs-lookup"><span data-stu-id="437c8-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="437c8-116">如果合約服務內容上的 **包含工作** 欄位為空白或已設定為 **整個專案**，則沒有提供 **應收費工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="437c8-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="437c8-117">專案合約服務內容的角色上所定義的可收費率只能套用至 **時間** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="437c8-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="437c8-118">如果合約服務內容上的 **包含時間** 欄位為空白或已設定為 **否**，則沒有提供 **應收費角色** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="437c8-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="437c8-119">專案合約服務內容的交易類別上所定義的可收費率只能套用至 **費用** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="437c8-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="437c8-120">如果 **包含費用** 欄位已設定為 **否**，則沒有提供 **應收費類別** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="437c8-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="437c8-121">將專案工作更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="437c8-122">專案工作在能使下列設定變成可行的特定合約服務內容上可以是應收費，也可以是不應收費：</span><span class="sxs-lookup"><span data-stu-id="437c8-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="437c8-123">如果專案型合約服務內容包含 **時間**，且特定工作 **T1** 與其建立為應收費關聯。</span><span class="sxs-lookup"><span data-stu-id="437c8-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="437c8-124">如果有第二個合約服務內容，其中包含 **費用** 時，您可以將合約服務內容的 T1 工作關聯為不應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="437c8-125">結果是，工作中所記錄的所有時間都是應收費的，而所有費用都是不應收費的。</span><span class="sxs-lookup"><span data-stu-id="437c8-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="437c8-126">工作的帳單類型可以在合約服務內容的 **應收費工作** 索引標籤上，透過更新合約服務內容工作子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="437c8-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="437c8-127">或者，也可以在顯示與工作相關之合約服務內容的專案工作帳單設定子格中更新 **帳單類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="437c8-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="437c8-128">將角色更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="437c8-129">角色在特定合約服務內容上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="437c8-130">您可以在合約服務內容的 **應收費角色** 索引標籤上設定角色的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="437c8-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="437c8-131">若要這樣，請更新 **應收費角色** 子格上的 **帳單類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="437c8-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="437c8-132">將交易類別更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="437c8-133">交易類別在特定合約服務內容上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="437c8-134">您可以在專案型合約服務內容的 **應收費類別** 索引標籤上設定交易的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="437c8-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="437c8-135">若要這樣，請更新 **應收費類別** 子格上的 **帳單類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="437c8-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="437c8-136">解析可收費率</span><span class="sxs-lookup"><span data-stu-id="437c8-136">Resolve chargeability</span></span>

<span data-ttu-id="437c8-137">只有在下列情況下，才能將針對時間建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="437c8-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="437c8-138">**時間** 已包含在合約服務內容中。</span><span class="sxs-lookup"><span data-stu-id="437c8-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="437c8-139">**角色** 已在合約服務內容中設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="437c8-140">**包含的工作** 已在合約服務內容上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="437c8-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="437c8-141">如果這三種情況成立，工作就會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="437c8-142">只有在下列情況下，才能將針對費用建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="437c8-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="437c8-143">**費用** 已包含在合約服務內容中</span><span class="sxs-lookup"><span data-stu-id="437c8-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="437c8-144">**交易類別** 已在合約服務內容中設定為應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="437c8-145">**包含的工作** 已在合約服務內容上設定為 **選取的工作**</span><span class="sxs-lookup"><span data-stu-id="437c8-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="437c8-146">如果這三種情況成立，**工作** 就會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="437c8-147">只有在下列情況下，才能將針對材料建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="437c8-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="437c8-148">**材料** 已包含在合約服務內容中</span><span class="sxs-lookup"><span data-stu-id="437c8-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="437c8-149">**包含的工作** 已在合約服務內容上設定為 **選取的工作**</span><span class="sxs-lookup"><span data-stu-id="437c8-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="437c8-150">如果這兩種情況成立，**工作** 就會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="437c8-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-151">
                    <strong>包含時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="437c8-152">
                    <strong>包含費用</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="437c8-153">
                    <strong>包含材料</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="437c8-154">
                    <strong>包含的工作</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-155">
                    <strong>角色</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-156">
                    <strong>類別</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-157">
                    <strong>工作​​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="437c8-158">
                    <strong>可收費率影響</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-159">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-160">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-161">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-162">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-163">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-164">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-165">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-166">時間實際值的帳單：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-167">費用實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-168">材料實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-169">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-170">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-171">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-172">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="437c8-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-173">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-174">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-175">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-176">時間實際值的帳單：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-177">費用實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-178">材料實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-179">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-180">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-181">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-182">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="437c8-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-183">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-184">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-185">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-186">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-187">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="437c8-188">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-189">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-190">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-191">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-192">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="437c8-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-193">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-194">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-195">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-196">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-197">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-198">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-199">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-200">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-201">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-202">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="437c8-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-203">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-204">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-205">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-206">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-207">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-208">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-209">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-210">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-211">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-212">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="437c8-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-213">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-214">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-215">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-216">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-217">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-218">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-219">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-220">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-221">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-222">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-223">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-224">
                    <strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-225">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-226">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-227">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="437c8-228">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-229">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-230">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-231">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-232">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-233">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-234">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-235">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-236">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-237">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-238">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-239">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="437c8-240">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-241">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-242">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-243">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-244">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-245">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-246">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="437c8-247">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-248">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-249">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="437c8-250">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="437c8-251">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-252">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-253">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-254">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-255">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-256">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-257">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-258">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-259">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-260">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="437c8-261">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-262">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-263">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-264">應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-265">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-266">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="437c8-267">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="437c8-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="437c8-268">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="437c8-269">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="437c8-270">.是</span><span class="sxs-lookup"><span data-stu-id="437c8-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="437c8-271">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="437c8-272">整個專案</span><span class="sxs-lookup"><span data-stu-id="437c8-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="437c8-273">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="437c8-274">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="437c8-275">無法設定</span><span class="sxs-lookup"><span data-stu-id="437c8-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="437c8-276">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-277">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="437c8-278">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="437c8-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
