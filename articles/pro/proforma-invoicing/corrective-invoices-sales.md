---
title: 更正過的發票 - 精簡
description: 本主題提供有關 Project Operations 中已更正發票的資訊
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176458"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="0c8ce-103">更正過的發票 - 精簡</span><span class="sxs-lookup"><span data-stu-id="0c8ce-103">Corrected invoices - lite</span></span>

<span data-ttu-id="0c8ce-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="0c8ce-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0c8ce-105">確認過的專案發票可進行更正以處理與客戶及專案經理議定的變更或貸記。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="0c8ce-106">若要對已確認的發票進行編輯，請開啟已確認的發票，然後選取 **更正此發票**。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0c8ce-107">除非專案發票已確認，否則不提供此選取項目。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="0c8ce-108">新的草稿發票會從已確認的發票中建立。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="0c8ce-109">所有來自先前已確認發票的發票明細詳細資料都會複製到新的草稿中。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="0c8ce-110">以下是了解新更正發票中明細詳細資訊的一些要點：</span><span class="sxs-lookup"><span data-stu-id="0c8ce-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="0c8ce-111">所有數量都會更新為零。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-111">All quantities are updated to zero.</span></span> <span data-ttu-id="0c8ce-112">應用程式假設所有已開發票的項目都已完全貸記。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="0c8ce-113">如有需要，您可以手動更新這些數量以反映要開立發票的數量，而不是貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="0c8ce-114">應用程式會根據您輸入的數量，計算貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="0c8ce-115">此金額會反映在確認更正後發票時所建立的實際值中。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="0c8ce-116">如果您要對稅金金額進行變更，就必須輸入正確的稅額，而不是貸記的稅額。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="0c8ce-117">不會複製先前已確認的產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="0c8ce-118">不支援處理對產品型專案發票的更正。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="0c8ce-119">里程碑更正一律以完全貸記的方式處理。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="0c8ce-120">如果開立了金額不正確的發票給客戶，則可以更正保留款或預付金的金額。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="0c8ce-121">如果使用了不正確的金額對先前已確認發票上的收費進行協調，則可以更正保留款及預付金的對帳單。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c8ce-122">對其他已開發行票的收費做更正的發票明細詳細資料，其 **更正** 欄位會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="0c8ce-123">已更正發票明細詳細資料的發票具有名為 **有更正** 的欄位，此欄位也會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="0c8ce-124">在確認更正發票時所建立的實際值：</span><span class="sxs-lookup"><span data-stu-id="0c8ce-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="0c8ce-125">以下是應用程式在確認前根據已對草稿更正發票執行之作業進行更正確認時所建立的實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0c8ce-126">
                    <strong>案例</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c8ce-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0c8ce-127">
                    <strong>確認時建立的實際值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c8ce-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0c8ce-128">確認已開發票預付金或保留款的更正。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c8ce-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-129">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0c8ce-130">此金額為正數，因為這是要用來抵消開立保留款或預付金發票時所建立的負數金額。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-131">已開單銷售沖銷是針對保留款或預付金的金額建立來沖銷原始已開單銷售。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-132">新的已開單銷售實際值是針對根據保留款或預付金更正之發票明細的更正金額所建立。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-133">根據保留款或預付金更正之發票明細金額為負數的未開單銷售實際值，用於協調對帳差異。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0c8ce-134">對先前已協調保留款或預付金的更正確認。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-135">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0c8ce-136">此金額為正數，要用來抵消先前進行對帳差異協調時所建立的負數金額。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-137">先前發票金額的已開單銷售沖銷實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-138">套用於更正後發票之已更正保留款金額的新開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-139">更正後剩餘保留款或預付金為負數金額的未開單銷售實際值，這會用來對後來的發票進行對帳差異協調。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c8ce-140">對先前已開發票的時間交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-141">原始時間發票明細詳細資料上時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-142">原始時間發票明細詳細資料上時數及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0c8ce-143">對時間交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-144">原始時間發票明細詳細資料上已開發票時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-145">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-146">應按照扣減發票明細詳細資料上已更正數字後剩餘時數及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c8ce-147">對先前已開發票的費用交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-148">原始費用發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-149">原始費用發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0c8ce-150">對先前已開發票的費用交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-151">原始費用發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-152">應按照更正後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-153">應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c8ce-154">對先前已開發票的服務費交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-155">原始服務費發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-156">原始服務費發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c8ce-157">對先前已開發票的服務費交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-158">原始服務費發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-159">應按照編輯後更正發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0c8ce-160">對先前已開發票的里程碑交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-161">原始里程碑發票明細詳細資料上金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="0c8ce-162">專案合約服務內容的里程碑發票或帳單狀態已更新為 **已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0c8ce-163">對先前已開發票的里程碑交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-164">不支援</span><span class="sxs-lookup"><span data-stu-id="0c8ce-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0c8ce-165">先前已開發票產品型合約服務內容的貸記和更正。</span><span class="sxs-lookup"><span data-stu-id="0c8ce-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0c8ce-166">不支援</span><span class="sxs-lookup"><span data-stu-id="0c8ce-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
