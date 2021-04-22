---
title: 設定專案型合約服務內容的應收費元件
description: 本主題提供有關如何在 Project Operations 中新增應收費元件至合約服務內容的資訊。
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858500"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="41f93-103">設定專案型合約服務內容的應收費元件</span><span class="sxs-lookup"><span data-stu-id="41f93-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="41f93-104">_**適用於：** 精簡部署 - 交易至開立預估發票、資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="41f93-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="41f93-105">專案型合約服務內容有 *包含* 元件和 *應收費* 元件。</span><span class="sxs-lookup"><span data-stu-id="41f93-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="41f93-106">內含元件是受限於下列各項的元件：</span><span class="sxs-lookup"><span data-stu-id="41f93-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="41f93-107">帳務方式和客戶分割</span><span class="sxs-lookup"><span data-stu-id="41f93-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="41f93-108">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="41f93-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="41f93-109">專案型合約服務內容上定義的發票週期設定</span><span class="sxs-lookup"><span data-stu-id="41f93-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="41f93-110">您可以使用 **帳單類型** 欄位將一部分內含元件標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="41f93-111">**帳單類型** 欄位是選項組，允許在合約服務內容的情境下使用下列值：</span><span class="sxs-lookup"><span data-stu-id="41f93-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="41f93-112">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-112">Chargeable</span></span>
  - <span data-ttu-id="41f93-113">不應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-113">Non-chargeable</span></span>

<span data-ttu-id="41f93-114">您可以在工作、角色和交易類別上定義應收費元件。</span><span class="sxs-lookup"><span data-stu-id="41f93-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="41f93-115">可收費率是在專案合約服務內容的工作上所定義，並套用至服務內容所包含的所有交易分類。</span><span class="sxs-lookup"><span data-stu-id="41f93-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="41f93-116">如果合約服務內容上的 **包含工作** 欄位為空白或已設定為 **整個專案**，則沒有提供 **應收費工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="41f93-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="41f93-117">專案合約服務內容的角色上所定義的可收費率只能套用至 **時間** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="41f93-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="41f93-118">如果合約服務內容上的 **包含時間** 欄位為空白或已設定為 **否**，則沒有提供 **應收費角色** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="41f93-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="41f93-119">專案合約服務內容的交易類別上所定義的可收費率只能套用至 **費用** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="41f93-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="41f93-120">如果 **包含費用** 欄位已設定為 **否**，則沒有提供 **應收費類別** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="41f93-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="41f93-121">將專案工作更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="41f93-122">專案工作在能使下列設定變成可行的特定合約服務內容上可以是應收費，也可以是不應收費：</span><span class="sxs-lookup"><span data-stu-id="41f93-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="41f93-123">如果專案型合約服務內容包含 **時間**，且特定工作 **T1** 與其建立為應收費關聯。</span><span class="sxs-lookup"><span data-stu-id="41f93-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="41f93-124">如果有第二個合約服務內容，其中包含 **費用** 時，您可以將合約服務內容的 T1 工作關聯為不應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="41f93-125">結果是，工作中所記錄的所有時間都是應收費的，而所有費用都是不應收費的。</span><span class="sxs-lookup"><span data-stu-id="41f93-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="41f93-126">工作的帳單類型可以在合約服務內容的 **應收費工作** 索引標籤上，透過更新合約服務內容工作子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="41f93-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="41f93-127">或者，也可以在顯示與工作相關之合約服務內容的專案工作帳單設定子格中更新 **帳單類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="41f93-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="41f93-128">將角色更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="41f93-129">角色在特定合約服務內容上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="41f93-130">您可以在合約服務內容的 **應收費角色** 索引標籤上設定角色的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="41f93-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="41f93-131">若要這樣，請更新 **應收費角色** 子格上的 **帳單類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="41f93-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="41f93-132">將交易類別更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="41f93-133">交易類別在特定合約服務內容上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="41f93-134">您可以在專案型合約服務內容的 **應收費類別** 索引標籤上設定交易的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="41f93-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="41f93-135">若要這樣，請更新 **應收費類別** 子格上的 **帳單類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="41f93-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="41f93-136">解析可收費率</span><span class="sxs-lookup"><span data-stu-id="41f93-136">Resolve chargeability</span></span>

<span data-ttu-id="41f93-137">只有在下列情況下，才能將針對時間建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="41f93-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="41f93-138">**時間** 已包含在合約服務內容中。</span><span class="sxs-lookup"><span data-stu-id="41f93-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="41f93-139">**角色** 已在合約服務內容中設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="41f93-140">**包含的工作** 已在合約服務內容上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="41f93-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="41f93-141">如果這三種情況成立，工作就會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="41f93-142">只有在下列情況下，才能將針對費用建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="41f93-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="41f93-143">**費用** 已包含在合約服務內容中</span><span class="sxs-lookup"><span data-stu-id="41f93-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="41f93-144">**交易類別** 已在合約服務內容中設定為應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="41f93-145">**包含的工作** 已在合約服務內容上設定為 **選取的工作**</span><span class="sxs-lookup"><span data-stu-id="41f93-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="41f93-146">如果這三種情況成立，**工作** 就會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="41f93-147">只有在下列情況下，才能將針對材料建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="41f93-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="41f93-148">**材料** 已包含在合約服務內容中</span><span class="sxs-lookup"><span data-stu-id="41f93-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="41f93-149">**包含的工作** 已在合約服務內容上設定為 **選取的工作**</span><span class="sxs-lookup"><span data-stu-id="41f93-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="41f93-150">如果這兩種情況成立，**工作** 就會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="41f93-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-151">
                    <strong>包含時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="41f93-152">
                    <strong>包含費用</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="41f93-153">
                    <strong>包含材料</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="41f93-154">
                    <strong>包含的工作</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-155">
                    <strong>角色</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-156">
                    <strong>類別</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-157">
                    <strong>工作​​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="41f93-158">
                    <strong>可收費率影響</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-159">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-160">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-161">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-162">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-163">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-164">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-165">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-166">時間實際值的帳單：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-167">費用實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-168">材料實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-169">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-170">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-171">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-172">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="41f93-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-173">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-174">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-175">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-176">時間實際值的帳單：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-177">費用實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-178">材料實際值的帳單類型：<strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-179">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-180">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-181">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-182">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="41f93-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-183">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-184">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-185">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-186">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-187">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="41f93-188">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-189">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-190">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-191">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-192">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="41f93-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-193">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-194">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-195">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-196">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-197">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-198">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-199">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-200">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-201">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-202">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="41f93-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-203">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-204">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-205">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-206">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-207">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-208">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-209">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-210">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-211">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-212">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="41f93-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-213">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-214">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-215">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-216">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-217">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-218">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-219">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-220">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-221">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-222">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-223">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-224">
                    <strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-225">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-226">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-227">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="41f93-228">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-229">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-230">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-231">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-232">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-233">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-234">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-235">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-236">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-237">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-238">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-239">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="41f93-240">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-241">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-242">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-243">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-244">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-245">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-246">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="41f93-247">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-248">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-249">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="41f93-250">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="41f93-251">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-252">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-253">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-254">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-255">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-256">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-257">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-258">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-259">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-260">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="41f93-261">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-262">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-263">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-264">應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-265">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-266">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="41f93-267">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="41f93-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="41f93-268">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="41f93-269">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="41f93-270">.是</span><span class="sxs-lookup"><span data-stu-id="41f93-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="41f93-271">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="41f93-272">整個專案</span><span class="sxs-lookup"><span data-stu-id="41f93-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="41f93-273">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="41f93-274">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="41f93-275">無法設定</span><span class="sxs-lookup"><span data-stu-id="41f93-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="41f93-276">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-277">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="41f93-278">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="41f93-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
