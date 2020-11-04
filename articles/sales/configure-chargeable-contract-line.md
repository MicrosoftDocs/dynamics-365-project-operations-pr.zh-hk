---
title: 設定專案型合約服務內容的應收費元件
description: 本主題提供有關合約服務內容中內含、應收費和不應收費元件的資訊。
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087437"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="4e9e5-103">設定專案型合約服務內容的應收費元件</span><span class="sxs-lookup"><span data-stu-id="4e9e5-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="4e9e5-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="4e9e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4e9e5-105">專案型合約服務內容有內含、應收費和不應收費的概念。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-105">A project-based contract line has the concept of included, chargeable, and non-chargeable components.</span></span>

<span data-ttu-id="4e9e5-106">內含元件受限於帳務方式、客戶分割、不得超過限制以及在專案型合約服務內容所定義的發票週期設定。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-106">Included components are subject to the billing method, customer splits, not-to-exceed limits, and invoice frequency settings defined on the project-based contract line.</span></span>

<span data-ttu-id="4e9e5-107">您可以更新 **帳單類型** 欄位，將一部分內含元件標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-107">A subset of the included components can be marked as chargeable by updating the **Billing Type** field.</span></span>

<span data-ttu-id="4e9e5-108">您可以在角色和交易類別上定義應收費元件。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-108">Chargeable components can be defined on roles, and transaction categories.</span></span>

<span data-ttu-id="4e9e5-109">就專案合約服務內容而言，角色上所定義的可收費率只能套用至 **時間** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-109">For a project contract line, the chargeability defined on a role only applies to the **Time** transaction class.</span></span> <span data-ttu-id="4e9e5-110">如果 **包含時間** 在專案合約服務內容上設定為 **否** ，則沒有提供 **應收費角色** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-110">If **Include Time** is set to **No** on a project contract line, the **Chargeable roles** tab isn't available.</span></span>

<span data-ttu-id="4e9e5-111">專案合約服務內容的交易類別上所定義的可收費率只能套用至 **費用** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-111">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="4e9e5-112">如果 **包含費用** 在專案合約服務內容上設定為 **否** ，則沒有提供 **應收費類別** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-112">If **Include Expenses** is set to **No** on a project contract line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4e9e5-113">將角色更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-113">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4e9e5-114">角色在特定專案型合約服務內容上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-114">A role can be chargeable or non-chargeable on specific project-based contract line.</span></span>

<span data-ttu-id="4e9e5-115">在專案型合約服務內容的 **應收費角色** 索引標籤上的 **應收費類別** 子格的 **帳單類型** 欄位中，更新角色的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-115">On the **Chargeable roles** tab of a projec-based contract line, on the **Chargeable Categories** sub-grid, in the **Billing Type** field, update the billing type for a role.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4e9e5-116">將交易類別更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-116">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4e9e5-117">交易類別在特定專案型合約服務內容上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-117">A transaction category can be chargeable or non-chargeable on a specific project-based contract line.</span></span>

<span data-ttu-id="4e9e5-118">在專案型合約服務內容的 **應收費類別** 索引標籤上的 **應收費類別** 子格的 **帳單類型** 欄位中，更新交易的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-118">On the **Chargeable Categories** tab of a project-based contract line, on the **Chargeable Categories** sub-grid, in the **Billing Type** field, update the billing type for a transaction.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="4e9e5-119">解析可收費率</span><span class="sxs-lookup"><span data-stu-id="4e9e5-119">Resolve chargeability</span></span>

<span data-ttu-id="4e9e5-120">針對時間所建立的估計值或實際值，只有在時間已包含在合約服務內容中時，以及在角色已在合約服務內容上設定為應收費時，才會視為應收費。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-120">An estimate or actual created for time will only be considered chargeable if time is included on the contract line, and if the role is configured as chargeable on the contract line.</span></span>

<span data-ttu-id="4e9e5-121">針對費用所建立的估計值或實際值，只有在費用已包含在合約服務內容中時，以及在交易類別已在合約服務內容上設定為應收費時，才會視為應收費。</span><span class="sxs-lookup"><span data-stu-id="4e9e5-121">An estimate or actual created for expense will only be considered chargeable if expense is included on the contract line, and if the transaction category is configured as chargeable on the contract line.</span></span>

| <span data-ttu-id="4e9e5-122">包含時間</span><span class="sxs-lookup"><span data-stu-id="4e9e5-122">Includes time</span></span> | <span data-ttu-id="4e9e5-123">包含費用</span><span class="sxs-lookup"><span data-stu-id="4e9e5-123">Includes expense</span></span> | <span data-ttu-id="4e9e5-124">角色</span><span class="sxs-lookup"><span data-stu-id="4e9e5-124">Role</span></span> | <span data-ttu-id="4e9e5-125">Category</span><span class="sxs-lookup"><span data-stu-id="4e9e5-125">Category</span></span> | <span data-ttu-id="4e9e5-126">工作​​</span><span class="sxs-lookup"><span data-stu-id="4e9e5-126">Task</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="4e9e5-127">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-127">Yes</span></span> | <span data-ttu-id="4e9e5-128">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-128">Yes</span></span> | <span data-ttu-id="4e9e5-129">應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-129">Chargeable</span></span> | <span data-ttu-id="4e9e5-130">應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-130">Chargeable</span></span> | <span data-ttu-id="4e9e5-131">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-131">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="4e9e5-132">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-132">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="4e9e5-133">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-133">Yes</span></span> | <span data-ttu-id="4e9e5-134">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-134">Yes</span></span> | <span data-ttu-id="4e9e5-135">不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-135">Non - Chargeable</span></span> | <span data-ttu-id="4e9e5-136">應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-136">Chargeable</span></span> | <span data-ttu-id="4e9e5-137">時間實際值的帳單：不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-137">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="4e9e5-138">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-138">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="4e9e5-139">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-139">Yes</span></span> | <span data-ttu-id="4e9e5-140">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-140">Yes</span></span> | <span data-ttu-id="4e9e5-141">不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-141">Non-Chargeable</span></span> | <span data-ttu-id="4e9e5-142">不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-142">Non-Chargeable</span></span> | <span data-ttu-id="4e9e5-143">時間實際值的帳單：不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-143">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="4e9e5-144">費用實際值的帳單類型：不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-144">Billing type on an expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="4e9e5-145">無</span><span class="sxs-lookup"><span data-stu-id="4e9e5-145">No</span></span> | <span data-ttu-id="4e9e5-146">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-146">Yes</span></span> | <span data-ttu-id="4e9e5-147">無法設定</span><span class="sxs-lookup"><span data-stu-id="4e9e5-147">Can't be set</span></span> | <span data-ttu-id="4e9e5-148">應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-148">Chargeable</span></span> | <span data-ttu-id="4e9e5-149">時間實際值的帳單：無法使用</span><span class="sxs-lookup"><span data-stu-id="4e9e5-149">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="4e9e5-150">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-150">Billing type on an expense actual:Chargeable</span></span> |
| <span data-ttu-id="4e9e5-151">無</span><span class="sxs-lookup"><span data-stu-id="4e9e5-151">No</span></span> | <span data-ttu-id="4e9e5-152">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-152">Yes</span></span> | <span data-ttu-id="4e9e5-153">無法設定</span><span class="sxs-lookup"><span data-stu-id="4e9e5-153">Can't be set</span></span> | <span data-ttu-id="4e9e5-154">不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-154">Non-Chargeable</span></span> | <span data-ttu-id="4e9e5-155">時間實際值的帳單：無法使用</span><span class="sxs-lookup"><span data-stu-id="4e9e5-155">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="4e9e5-156">費用實際值的帳單類型：不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-156">Billing type on an expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="4e9e5-157">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-157">Yes</span></span> | <span data-ttu-id="4e9e5-158">無</span><span class="sxs-lookup"><span data-stu-id="4e9e5-158">No</span></span> | <span data-ttu-id="4e9e5-159">應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-159">Chargeable</span></span> | <span data-ttu-id="4e9e5-160">無法設定</span><span class="sxs-lookup"><span data-stu-id="4e9e5-160">Can't be set</span></span> | <span data-ttu-id="4e9e5-161">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-161">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="4e9e5-162">費用實際值的帳單類型：無法使用</span><span class="sxs-lookup"><span data-stu-id="4e9e5-162">Billing type on an expense actual: Not available</span></span> |
| <span data-ttu-id="4e9e5-163">.是</span><span class="sxs-lookup"><span data-stu-id="4e9e5-163">Yes</span></span> | <span data-ttu-id="4e9e5-164">無</span><span class="sxs-lookup"><span data-stu-id="4e9e5-164">No</span></span> | <span data-ttu-id="4e9e5-165">不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-165">Non-Chargeable</span></span> | <span data-ttu-id="4e9e5-166">無法設定</span><span class="sxs-lookup"><span data-stu-id="4e9e5-166">Can't be set</span></span> | <span data-ttu-id="4e9e5-167">時間實際值的帳單：不應收費</span><span class="sxs-lookup"><span data-stu-id="4e9e5-167">Billing on a time actual: Non-chargeable</span></span> </br> <span data-ttu-id="4e9e5-168">費用實際值的帳單類型：無法使用</span><span class="sxs-lookup"><span data-stu-id="4e9e5-168">Billing type on an expense actual: Not available</span></span> |
