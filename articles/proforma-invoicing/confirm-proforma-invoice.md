---
title: 確認專案型預估發票
description: 本主題提供有關確認專案型預估發票的資訊。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012163"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="ccfa4-103">確認專案型預估發票</span><span class="sxs-lookup"><span data-stu-id="ccfa4-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="ccfa4-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ccfa4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ccfa4-105">確認預估發票之後，專案發票的狀態會更新為 **已確認**。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="ccfa4-106">確認發票時，它會變成唯讀。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="ccfa4-107">接下來，只有在任何客戶主動提出更正或貸記時，才能修正此發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="ccfa4-108">下表列出系統所建立的實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="ccfa4-109">這些實際值是在確認草稿專案發票前對其執行特定作業時所建立。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ccfa4-110">
                    <strong>案例</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccfa4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ccfa4-111">
                    <strong>確認時建立的實際值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccfa4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-112">開立預付金 (或定額保留後隨用即扣型付款) 的發票</span><span class="sxs-lookup"><span data-stu-id="ccfa4-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-113">類型為<strong>保留款</strong>的已開單銷售實際值是針對預付金 (或定額保留後隨用即扣型付款) 的金額所建立。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-114">要用於協調對帳差異之保留款或預付金金額為負數的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-115">在發票上將保留款或預付金的差異完全協調之後。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-116">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ccfa4-117">此金額為正值，因為這是要用來抵消開立保留款或預付金發票時所建立的負值金額。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-118">此發票金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ccfa4-119">在發票上將保留款或預付金的差異部分協調之後。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-120">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ccfa4-121">此金額為正值，因為這是要用來抵消開立保留款或預付金發票時所建立的負值金額。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-122">此發票金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-123">要在未來發票上用於協調對帳差異之保留款或預付金剩餘金額的負數未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-124">不對草稿發票進行任何編輯，即開立時間交易發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-125">原始時間核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-126">原始時間核准上的時數及金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ccfa4-127">開立減少數量時所編輯之時間交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-128">原始時間核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-129">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-130">對已編輯發票明細詳細資料、銷售實際值沖銷和等額已開單銷售實際值扣減更正數字之後剩餘時數和金額不應收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-131">開立增加數量時所編輯之時間交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-132">原始時間核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-133">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-134">不對草稿發票進行任何編輯，即開立費用交易發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-135">原始費用核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-136">原始費用核准上的數量及金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ccfa4-137">開立減少數量時所編輯之費用交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-138">原始費用核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-139">應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-140">不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-141">開立增加數量時所編輯之費用交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-142">原始費用核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-143">應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-144">在未對草稿發票進行任何編輯的情況下，開立材料交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-145">原始材料使用核准上數量和金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-146">原始材料使用核准上數量和金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ccfa4-147">開立為減少數量所編輯之材料交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-148">原始時間核准上數量和金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-149">應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-150">不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-151">開立為增加數量所編輯之材料交易的發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-152">原始材料使用核准上數量和金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-153">應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccfa4-154">開立服務費發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-155">原始帳目明細上的服務費金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-156">原始費用帳目明細上的數量及金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ccfa4-157">開立里程碑發票。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ccfa4-158">原始里程碑在專案合約服務內容上的里程碑金額已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="ccfa4-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
