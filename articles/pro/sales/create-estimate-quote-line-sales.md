---
title: 估計專案型報價明細
description: 本主題提供有關如何在專案型報價明細上建立估計值的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966895"
---
# <a name="estimating-a-project-based-quote-line"></a><span data-ttu-id="ab62f-103">估計專案型報價明細</span><span class="sxs-lookup"><span data-stu-id="ab62f-103">Estimating a project-based quote line</span></span>

<span data-ttu-id="ab62f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="ab62f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ab62f-105">專案型報價明細的詳細資料可協助您估計提供報價明細所需工作的成本和可能營收。</span><span class="sxs-lookup"><span data-stu-id="ab62f-105">A project-based quote line has details that help with estimating the cost and potential revenue of the work involved to deliver the quote line.</span></span>

<span data-ttu-id="ab62f-106">若要估計專案型報價明細，請選取專案型報價明細上**報價明細詳細資料**索引標籤。有兩種方法可以在專案型報價明細上建立估計值：</span><span class="sxs-lookup"><span data-stu-id="ab62f-106">To estimate a project-based quote line, on the project-based quote line, select the **Quote Line Detail** tab. There are two ways to create an estimate on a project-based quote line:</span></span>

- <span data-ttu-id="ab62f-107">使用報價明細詳細資料，直接在報價明細上手動建立估計值</span><span class="sxs-lookup"><span data-stu-id="ab62f-107">Manually create the estimate directly on the quote line using quote line details</span></span> 
- <span data-ttu-id="ab62f-108">建立專案和專案計劃，然後將專案以及專案上的工作關聯至報價明細。</span><span class="sxs-lookup"><span data-stu-id="ab62f-108">Create a project and a project plan, and then associate the project and tasks on the project to the quote line.</span></span> <span data-ttu-id="ab62f-109">將會啟用根據您所提供資訊將專案計劃中估計值匯入至報價明細的程序。</span><span class="sxs-lookup"><span data-stu-id="ab62f-109">The process to import the estimates on the project plan into the quote line based on the information you provided will be enabled.</span></span>

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a><span data-ttu-id="ab62f-110">直接在專案型報價明細上建立估計值</span><span class="sxs-lookup"><span data-stu-id="ab62f-110">Create estimates directly on a project-based quote line</span></span>

<span data-ttu-id="ab62f-111">若要在專案型報價明細建立估計值，請選取**報價明細詳細資料**索引標籤。您在此索引標籤上建立的明細項目將會摘要列出此報價明細的報價值。</span><span class="sxs-lookup"><span data-stu-id="ab62f-111">To create an estimate on a project-based quote line, select the **Quote Line Detail** tab. The line item that you create on this tab will summarize the quoted value for this quote line.</span></span> 

<span data-ttu-id="ab62f-112">若要建立報價明細詳細資料，請選取**報價明細詳細資料**子格中的 **+ 新增報價明細詳細資料**。</span><span class="sxs-lookup"><span data-stu-id="ab62f-112">To create quote line details, select **+ New quote line detail** on the **Quote Line Details** sub-grid.</span></span> <span data-ttu-id="ab62f-113">將會開啟快速建立滑桿。</span><span class="sxs-lookup"><span data-stu-id="ab62f-113">A quick create slider will open.</span></span> <span data-ttu-id="ab62f-114">**報價明細**表單包含下列欄位：</span><span class="sxs-lookup"><span data-stu-id="ab62f-114">The following fields on the **Quote Line** form:</span></span>

| <span data-ttu-id="ab62f-115">**欄位**</span><span class="sxs-lookup"><span data-stu-id="ab62f-115">**Field**</span></span> | <span data-ttu-id="ab62f-116">**位置**</span><span class="sxs-lookup"><span data-stu-id="ab62f-116">**Location**</span></span> | <span data-ttu-id="ab62f-117">**關聯性、目的和指引**</span><span class="sxs-lookup"><span data-stu-id="ab62f-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="ab62f-118">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="ab62f-118">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="ab62f-119">描述</span><span class="sxs-lookup"><span data-stu-id="ab62f-119">Description</span></span> | <span data-ttu-id="ab62f-120">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-120">Quick create</span></span> | <span data-ttu-id="ab62f-121">特定估計值的描述。</span><span class="sxs-lookup"><span data-stu-id="ab62f-121">A description of the specific estimate.</span></span> | <span data-ttu-id="ab62f-122">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-122">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-123">交易類別</span><span class="sxs-lookup"><span data-stu-id="ab62f-123">Transaction Class</span></span> | <span data-ttu-id="ab62f-124">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-124">Quick create</span></span> | <span data-ttu-id="ab62f-125">此下拉式清單提供專案型報價明細的**一般**索引標籤中所包含的交易類別。</span><span class="sxs-lookup"><span data-stu-id="ab62f-125">This drop-down list provides the transaction classes that are included on the **General** tab of project-based quote line.</span></span>  | <span data-ttu-id="ab62f-126">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-126">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-127">角色</span><span class="sxs-lookup"><span data-stu-id="ab62f-127">Role</span></span> | <span data-ttu-id="ab62f-128">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-128">Quick create</span></span> | <span data-ttu-id="ab62f-129">將執行此工作或產生此費用的人員。</span><span class="sxs-lookup"><span data-stu-id="ab62f-129">The person that will perform this work or incur this expense.</span></span> | <span data-ttu-id="ab62f-130">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-130">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-131">Category</span><span class="sxs-lookup"><span data-stu-id="ab62f-131">Category</span></span> | <span data-ttu-id="ab62f-132">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-132">Quick create</span></span> | <span data-ttu-id="ab62f-133">工作或費用的類別。</span><span class="sxs-lookup"><span data-stu-id="ab62f-133">Category of the work or expense.</span></span> | <span data-ttu-id="ab62f-134">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-134">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-135">開始日期</span><span class="sxs-lookup"><span data-stu-id="ab62f-135">Start Date</span></span> | <span data-ttu-id="ab62f-136">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-136">Quick create</span></span> | <span data-ttu-id="ab62f-137">工作開始日期。</span><span class="sxs-lookup"><span data-stu-id="ab62f-137">Start date of the work.</span></span> | <span data-ttu-id="ab62f-138">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-138">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-139">結束日期</span><span class="sxs-lookup"><span data-stu-id="ab62f-139">End Date</span></span> | <span data-ttu-id="ab62f-140">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-140">Quick create</span></span> | <span data-ttu-id="ab62f-141">工作結束日期。</span><span class="sxs-lookup"><span data-stu-id="ab62f-141">End date of the work.</span></span> | <span data-ttu-id="ab62f-142">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-142">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-143">資源分配單位</span><span class="sxs-lookup"><span data-stu-id="ab62f-143">Resourcing Unit</span></span> | <span data-ttu-id="ab62f-144">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-144">Quick create</span></span> | <span data-ttu-id="ab62f-145">將會產生此成本及提供資源加以處理的資源分配單位。</span><span class="sxs-lookup"><span data-stu-id="ab62f-145">Resourcing unit that will incur this cost and provide the resource to work on it.</span></span> | <span data-ttu-id="ab62f-146">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-146">This field defaults to the related quote line detail for cost that is automatically created.</span></span> <span data-ttu-id="ab62f-147">此欄位也會用於成本價擷取。</span><span class="sxs-lookup"><span data-stu-id="ab62f-147">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="ab62f-148">單位排程</span><span class="sxs-lookup"><span data-stu-id="ab62f-148">Unit schedule</span></span> | <span data-ttu-id="ab62f-149">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-149">Quick create</span></span> | <span data-ttu-id="ab62f-150">工作或費用的單位群組。</span><span class="sxs-lookup"><span data-stu-id="ab62f-150">Unit group of the work or expense.</span></span> <span data-ttu-id="ab62f-151">屬於單位排程或單位群組的單位。</span><span class="sxs-lookup"><span data-stu-id="ab62f-151">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="ab62f-152">例如，英哩和公里屬於描述距離之單位群組的單位。</span><span class="sxs-lookup"><span data-stu-id="ab62f-152">For example, Miles and KMs are units that belong to a group of units that describes distance.</span></span> | <span data-ttu-id="ab62f-153">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-153">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-154">單位</span><span class="sxs-lookup"><span data-stu-id="ab62f-154">Unit</span></span> | <span data-ttu-id="ab62f-155">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-155">Quick create</span></span> | <span data-ttu-id="ab62f-156">工作或費用的單位。</span><span class="sxs-lookup"><span data-stu-id="ab62f-156">Unit of the work or expense.</span></span> | <span data-ttu-id="ab62f-157">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-157">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-158">數量</span><span class="sxs-lookup"><span data-stu-id="ab62f-158">Quantity</span></span> | <span data-ttu-id="ab62f-159">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-159">Quick create</span></span> | <span data-ttu-id="ab62f-160">工作或費用的數量</span><span class="sxs-lookup"><span data-stu-id="ab62f-160">Quantity of work or expense</span></span> | <span data-ttu-id="ab62f-161">此欄位預設為自動建立的成本相關報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab62f-161">This field defaults to the related quote line detail for cost that is automatically created.</span></span> |
| <span data-ttu-id="ab62f-162">單價</span><span class="sxs-lookup"><span data-stu-id="ab62f-162">Unit price</span></span> | <span data-ttu-id="ab62f-163">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-163">Quick create</span></span> | <span data-ttu-id="ab62f-164">執行工作之角色的帳單費率或費用類別的售價。</span><span class="sxs-lookup"><span data-stu-id="ab62f-164">Bill rate of the role that is performing the work or the Sales price of the expense category.</span></span> <span data-ttu-id="ab62f-165">此欄位的預設值是以開始日期生效之專案價目表中角色與資源分配單位組合為根據的時間。</span><span class="sxs-lookup"><span data-stu-id="ab62f-165">This field defaults for Time based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="ab62f-166">對於費用，此欄位預設值是開始日期生效之專案價目表中交易類別的價格設定。</span><span class="sxs-lookup"><span data-stu-id="ab62f-166">For expenses, this field defaults from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="ab62f-167">如果交易類別的定價方式不是單價，就沒有預設值，且此欄位保留空白。</span><span class="sxs-lookup"><span data-stu-id="ab62f-167">If the pricing method for the transaction category is not price-per-unit, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="ab62f-168">執行工作之角色的成本費率或費用類別的單位成本。</span><span class="sxs-lookup"><span data-stu-id="ab62f-168">Cost rate of the role that is performing the work or the cost-per-unit of the expense category.</span></span> <span data-ttu-id="ab62f-169">此欄位的預設值是以開始日期生效之報價價目表合約單位價格中角色與資源分配單位組合為根據的時間。</span><span class="sxs-lookup"><span data-stu-id="ab62f-169">This field defaults for Time based on the role and resourcing unit combination on the price of the Contracting unit of the Quote price list that is effective for the start date.</span></span> <span data-ttu-id="ab62f-170">對於費用，此欄位預設值是開始日期生效之合約單位成本價目表中交易類別的價格設定。</span><span class="sxs-lookup"><span data-stu-id="ab62f-170">For expenses, this field defaults from the price setup for the transaction category in the cost price list of Contracting unit that is effective for the start date.</span></span> <span data-ttu-id="ab62f-171">如果交易類別的定價方式不是單價，就沒有預設值，且此欄位保留空白。</span><span class="sxs-lookup"><span data-stu-id="ab62f-171">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="ab62f-172">估計稅額</span><span class="sxs-lookup"><span data-stu-id="ab62f-172">Estimated Tax</span></span> | <span data-ttu-id="ab62f-173">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-173">Quick create</span></span> | <span data-ttu-id="ab62f-174">您可以手動輸入此工作或費用的估計稅金。</span><span class="sxs-lookup"><span data-stu-id="ab62f-174">You can manually enter the estimated tax for this work or expense.</span></span> | <span data-ttu-id="ab62f-175">此欄位沒有任何下游影響。</span><span class="sxs-lookup"><span data-stu-id="ab62f-175">There is no downstream impact of this field.</span></span> |
| <span data-ttu-id="ab62f-176">總數</span><span class="sxs-lookup"><span data-stu-id="ab62f-176">Amount</span></span> | <span data-ttu-id="ab62f-177">快速建立</span><span class="sxs-lookup"><span data-stu-id="ab62f-177">Quick create</span></span> | <span data-ttu-id="ab62f-178">如果**數量**和**價格**欄位保留空白，您可以在此欄位中手動輸入資訊。</span><span class="sxs-lookup"><span data-stu-id="ab62f-178">You can manually input information into this field if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="ab62f-179">如果這些欄位不是空白，則此欄位會變成唯讀，並且會依 (數量 \* 單價) + 稅金的方式進行計算。</span><span class="sxs-lookup"><span data-stu-id="ab62f-179">If these fields are not blank, this field becomes read-only and is calculated as (Quantity \* Unit price) + Tax.</span></span> | <span data-ttu-id="ab62f-180">此欄位沒有任何下游影響。</span><span class="sxs-lookup"><span data-stu-id="ab62f-180">There is no downstream impact of this field.</span></span> |

## <a name="update-prices-on-quote-line-details"></a><span data-ttu-id="ab62f-181">更新報價明細詳細資料的價格</span><span class="sxs-lookup"><span data-stu-id="ab62f-181">Update prices on quote line details</span></span>

<span data-ttu-id="ab62f-182">如果您已變更在附加至報價之專案價目表或在合約單位之成本價目表上的價格，則可以選取**報價**頁面上的**重新計算**，重新整理個別報價明細詳細資料上的價格，以反映此變更。</span><span class="sxs-lookup"><span data-stu-id="ab62f-182">If you have changed prices on the project price list that is attached to the quote, or on cost price list of the contracting unit, you can select **Recalculate** on the **Quote** page, to refresh the prices on the individual quote line details to reflect this change.</span></span> <span data-ttu-id="ab62f-183">選取**重新計算**時，警告會出現，通知您此報價上所有報價明細之報價明細詳細資料中的價格都將重設。</span><span class="sxs-lookup"><span data-stu-id="ab62f-183">When you select **Recalculate**, a warning occurs that informs you that prices on quote line details for all quote lines on this quote will be reset.</span></span> <span data-ttu-id="ab62f-184">選取**是**以重新整理銷售及成本報價明細詳細資料的價格。</span><span class="sxs-lookup"><span data-stu-id="ab62f-184">Select **Yes**, to refresh prices for both sales and cost quote line details.</span></span>

## <a name="access-quote-line-details-for-cost"></a><span data-ttu-id="ab62f-185">存取成本的報價明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="ab62f-185">Access quote line details for cost</span></span>

<span data-ttu-id="ab62f-186">在**報價明細詳細資料**索引標籤中，選取網格中的一列，以在子格的工具列上啟用某些動作。</span><span class="sxs-lookup"><span data-stu-id="ab62f-186">On the **Quote Line Details** tab, select a row in the grid to enable some actions on the toolbar of the sub-grid.</span></span> <span data-ttu-id="ab62f-187">選取報價明細詳細資料時，子格工具列上的第一個動作會是**開啟成本詳細資料**。</span><span class="sxs-lookup"><span data-stu-id="ab62f-187">The first action on the sub-grid tool bar when a quote line detail is selected is **Open Cost Detail**.</span></span> <span data-ttu-id="ab62f-188">選取**開啟成本詳細資料**，以查看此報價明細的相關成本費率及金額。</span><span class="sxs-lookup"><span data-stu-id="ab62f-188">Select **Open Cost Detail** to see the related cost rate and amount for this quote line.</span></span>

> [!NOTE]
> <span data-ttu-id="ab62f-189">在成本報價明細詳細資料中變更資源分配單位、數量、日期、角色或類別值，將會變更銷售報價明細詳細資料中對應的值。</span><span class="sxs-lookup"><span data-stu-id="ab62f-189">Changing the resourcing unit, quantity, dates, role, or category values on the quote line detail for cost will change the corresponding values on the quote line details for sales.</span></span>
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a><span data-ttu-id="ab62f-190">成本及銷售報價明細詳細資料上的貨幣</span><span class="sxs-lookup"><span data-stu-id="ab62f-190">Currency on quote line details for cost and sales</span></span>

<span data-ttu-id="ab62f-191">銷售報價明細詳細資料上的貨幣會使用報價明細詳細資料開始日期生效之專案價目表中的預設值。</span><span class="sxs-lookup"><span data-stu-id="ab62f-191">Currency on the quote line detail for sales defaults from the project price list that is effective for the start date of the quote line detail.</span></span>

<span data-ttu-id="ab62f-192">成本報價明細詳細資料上的貨幣會使用成本報價明細詳細資料開始日期生效之報價合約單位價目表中的預設值。</span><span class="sxs-lookup"><span data-stu-id="ab62f-192">Currency on the quote line detail for cost defaults from the price list of the contracting unit of the quote that is effective for the start date of the quote line detail for cost.</span></span>

<span data-ttu-id="ab62f-193">獲利率計算會將成本及銷售報價明細詳細資料上的金額轉換成環境的基準貨幣，以報告報價的整體估計利潤。</span><span class="sxs-lookup"><span data-stu-id="ab62f-193">Profitability calculations convert the amount on quote line details for cost and sales into the base currency of the environment to report the overall estimated margin on the quote.</span></span>

<span data-ttu-id="ab62f-194">這可能會因為缺少有效日期匯率而產生貨幣捨入誤差和改變利潤。</span><span class="sxs-lookup"><span data-stu-id="ab62f-194">This could result in currency rounding errors and changing margins because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="ab62f-195">這些對專案報價進行的計算只能用來當做近似值，不可做為實際法定申報值或其他需要使用較高捨入精確度以及了解匯率日期有效性的報告值。</span><span class="sxs-lookup"><span data-stu-id="ab62f-195">Use these calculations on Project quotes only as approximations and not actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>