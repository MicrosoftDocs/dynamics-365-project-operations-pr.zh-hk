---
title: 重要概念 - 專案合約
description: 本主題提供有關 Project Operations 中專案合約重要概念的資訊。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4ab43a9de6b27f0f0e9b8cbe6ea8b613ce81e08d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087436"
---
# <a name="key-concepts---project-contracts"></a><span data-ttu-id="41513-103">重要概念 - 專案合約</span><span class="sxs-lookup"><span data-stu-id="41513-103">Key concepts - Project contracts</span></span>

<span data-ttu-id="41513-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="41513-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="41513-105">本主題提供開始使用 Dynamics 365 Project Operations 中的專案合約前，需要了解的重要概念：</span><span class="sxs-lookup"><span data-stu-id="41513-105">This topic provides the key concepts to be aware of before you begin using Project contracts in Dynamics 365 Project Operations:</span></span>

## <a name="owning-company"></a><span data-ttu-id="41513-106">負責公司</span><span class="sxs-lookup"><span data-stu-id="41513-106">Owning Company</span></span>

<span data-ttu-id="41513-107">負責公司是 Dynamics 365 Finance 所提供之 Project Operations **專案管理與會計** 模組中的法律實體。</span><span class="sxs-lookup"><span data-stu-id="41513-107">The owning company is the legal entity from the **Project management and accounting** module for Project Operations from Dynamics 365 Finance.</span></span> <span data-ttu-id="41513-108">負責公司代表對交易所產生之成本與營收負有責任的法律實體。</span><span class="sxs-lookup"><span data-stu-id="41513-108">The owning company represents the legal entity that will account for the cost and revenue that accrues from a deal.</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="41513-109">合約單位</span><span class="sxs-lookup"><span data-stu-id="41513-109">Contracting Unit</span></span>

<span data-ttu-id="41513-110">合約單位代表負責交付專案的部門或業務單位。</span><span class="sxs-lookup"><span data-stu-id="41513-110">The contracting unit represents the division or practice that owns the delivery of the project.</span></span> <span data-ttu-id="41513-111">您可以設定每個合約單位的資源成本。</span><span class="sxs-lookup"><span data-stu-id="41513-111">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="41513-112">指定資源的資源成本時，您也可以為資源設定不同的成本費率。</span><span class="sxs-lookup"><span data-stu-id="41513-112">When you specify the resource cost for a resource, you will also be able to set up different cost rates for resources.</span></span> <span data-ttu-id="41513-113">此合約單位會向企業中的其他部門或業務單位借用這些資源。</span><span class="sxs-lookup"><span data-stu-id="41513-113">This contracting unit borrows these resources from other division or practices within the enterprise.</span></span> <span data-ttu-id="41513-114">資源的成本費率即稱為轉撥價格、資源借用或借調價格。</span><span class="sxs-lookup"><span data-stu-id="41513-114">The cost rates for the resources are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="41513-115">設定從其他部門借用資源的成本費率時，請使用出借部門的貨幣。</span><span class="sxs-lookup"><span data-stu-id="41513-115">When you set up the cost rates to borrow resources from other divisions, use the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="41513-116">成本貨幣</span><span class="sxs-lookup"><span data-stu-id="41513-116">Cost Currency</span></span>

<span data-ttu-id="41513-117">成本貨幣是在畫面上用來報告成本的貨幣。</span><span class="sxs-lookup"><span data-stu-id="41513-117">Cost currency is the currency in which costs are reported on screen.</span></span> <span data-ttu-id="41513-118">此貨幣是取自合約及專案上附加至 **合約單位** 欄位的貨幣。</span><span class="sxs-lookup"><span data-stu-id="41513-118">This currency is derived from the currency attached to the **Contracting Unit** field on the contract and the project.</span></span> <span data-ttu-id="41513-119">您可以在專案上使用任何貨幣來記錄成本。</span><span class="sxs-lookup"><span data-stu-id="41513-119">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="41513-120">不過，顯示在畫面上時，會發生從記錄成本所用貨幣到專案成本貨幣之間的貨幣轉換。</span><span class="sxs-lookup"><span data-stu-id="41513-120">However, there is currency conversion from the currency the costs were recorded in, to the cost currency of the project when shown on the screen.</span></span>

<span data-ttu-id="41513-121">因為 Common Data Service (CDS) 平台中的匯率無法即日生效，如果您更新貨幣匯率，畫面上的總計成本可能會隨時間改變。</span><span class="sxs-lookup"><span data-stu-id="41513-121">Because the exchange rates in the Common Data Service (CDS) platform can't be date effective, the on-screen totals for cost may change over time if you update the currency exchange rates.</span></span> <span data-ttu-id="41513-122">不過，記錄於資料庫中的成本仍會保持不變，因為金額是以其開支所用的貨幣來儲存。</span><span class="sxs-lookup"><span data-stu-id="41513-122">However, costs as recorded in the database remain unchanged because the amounts are stored in the currency that were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="41513-123">銷售貨幣</span><span class="sxs-lookup"><span data-stu-id="41513-123">Sales Currency</span></span>

<span data-ttu-id="41513-124">Project Operations 中的銷售貨幣是記錄和顯示估計及實際銷售金額所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="41513-124">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="41513-125">銷售貨幣也是開立交易發票給客戶所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="41513-125">Sales currency is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="41513-126">在專案合約上，預設會使用客戶或客戶記錄的銷售貨幣，而且可以在建立合約時變更。</span><span class="sxs-lookup"><span data-stu-id="41513-126">On a project contract, the sales currency defaults from the customer or account record and can be changed during when the contract is created.</span></span> <span data-ttu-id="41513-127">當合約是以成交關閉報價的方式建立時，合約的貨幣會預設為報價的貨幣。</span><span class="sxs-lookup"><span data-stu-id="41513-127">When a contract is created by closing a quote as won, the currency on the contract is defaulted from the currency on the quote.</span></span>

<span data-ttu-id="41513-128">從頭開始建立專案合約時，無法編輯 **銷售貨幣** 欄位。</span><span class="sxs-lookup"><span data-stu-id="41513-128">When you create a project contract from scratch, the **Sales Currency** field can't be edited.</span></span> <span data-ttu-id="41513-129">產品及專案價目表會根據合約上的這個貨幣來設定預設值。</span><span class="sxs-lookup"><span data-stu-id="41513-129">Product and project price lists default based on this currency on the contract.</span></span>

<span data-ttu-id="41513-130">與成本不同，銷售值只能以銷售貨幣來記錄。</span><span class="sxs-lookup"><span data-stu-id="41513-130">Unlike costs, sales values can only be recorded in the sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="41513-131">計費方式</span><span class="sxs-lookup"><span data-stu-id="41513-131">Billing Method</span></span>

<span data-ttu-id="41513-132">專案通常有兩種類型的合約模型，固定費用型和耗用量型。</span><span class="sxs-lookup"><span data-stu-id="41513-132">There are typically two types of contracting models for projects, fixed fee and consumption-based.</span></span> <span data-ttu-id="41513-133">這些模型代表 Project Operations 中的帳務方式，其中有兩個可能的值：</span><span class="sxs-lookup"><span data-stu-id="41513-133">These models are represented in Project Operations as billing methods with two possible values:</span></span>

- <span data-ttu-id="41513-134">時間和材料：基於耗用量的合約模型，其中每項產生的成本都是以對應的營收為背景來源。</span><span class="sxs-lookup"><span data-stu-id="41513-134">Time and Material: A consumption-based contracting model where each incurred cost is backed by corresponding revenue.</span></span> <span data-ttu-id="41513-135">隨著您估計或產生更多成本時，對應的估計和實際銷售也會增加。</span><span class="sxs-lookup"><span data-stu-id="41513-135">As you estimate or incur more costs, the corresponding estimated and actual sales also increase.</span></span> <span data-ttu-id="41513-136">在使用此帳務方式的合約服務內容上指定不得超過的限制，這會設定實際營收的上限。</span><span class="sxs-lookup"><span data-stu-id="41513-136">Specify not-to-exceed limits on contract lines that have this billing method, which caps off the actual revenue.</span></span> <span data-ttu-id="41513-137">估計營收不受不得超過的限制所影響。</span><span class="sxs-lookup"><span data-stu-id="41513-137">Estimated revenue isn't impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="41513-138">固定價格：固定費用合約模型，表示銷售值將與產生的成本無關。</span><span class="sxs-lookup"><span data-stu-id="41513-138">Fixed Price: A fixed fee contracting model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="41513-139">銷售值已固定，不會因為您估計或產生更多成本而改變。</span><span class="sxs-lookup"><span data-stu-id="41513-139">The sales value is fixed and doesn't change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="41513-140">專案價目表</span><span class="sxs-lookup"><span data-stu-id="41513-140">Project Price lists</span></span>

<span data-ttu-id="41513-141">專案價目表是用來設定時間、費用及其他專案相關元件預設價格 (不是預設成本費率) 的價目表。</span><span class="sxs-lookup"><span data-stu-id="41513-141">Project price lists are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="41513-142">可以有多個價目表。</span><span class="sxs-lookup"><span data-stu-id="41513-142">There can be multiple prices lists.</span></span> <span data-ttu-id="41513-143">每個價目表都有其本身對於各自專案合約的日期時效性。</span><span class="sxs-lookup"><span data-stu-id="41513-143">Each price list has its own date effectivity for each project contract.</span></span> <span data-ttu-id="41513-144">Project Operations 不支援專案價目表的有效日期範圍重疊。</span><span class="sxs-lookup"><span data-stu-id="41513-144">Overlapping date-effectivity on project price lists isn't supported in Project Operations.</span></span>

<span data-ttu-id="41513-145">因專案報價成交而建立專案合約時，會將專案價目表連同合約名稱及日期一起複製。</span><span class="sxs-lookup"><span data-stu-id="41513-145">When a project contract is created by winning a project quote, project price lists are copied with the contract name and date included.</span></span> <span data-ttu-id="41513-146">複製此資訊會建立此專案合約中專案元件的自訂定價。</span><span class="sxs-lookup"><span data-stu-id="41513-146">Copying this information constitutes custom pricing for project components on this project contract.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="41513-147">交易分類</span><span class="sxs-lookup"><span data-stu-id="41513-147">Transaction Classes</span></span>

<span data-ttu-id="41513-148">Project Operations 支援四種類型的交易分類：</span><span class="sxs-lookup"><span data-stu-id="41513-148">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="41513-149">時間</span><span class="sxs-lookup"><span data-stu-id="41513-149">Time</span></span>
- <span data-ttu-id="41513-150">費用</span><span class="sxs-lookup"><span data-stu-id="41513-150">Expense</span></span>
- <span data-ttu-id="41513-151">資料</span><span class="sxs-lookup"><span data-stu-id="41513-151">Material</span></span>
- <span data-ttu-id="41513-152">費用</span><span class="sxs-lookup"><span data-stu-id="41513-152">Fee</span></span>

<span data-ttu-id="41513-153">成本值和銷售值可以在 [時間]、[費用] 和 [材料] 交易分類上進行估計和列計。</span><span class="sxs-lookup"><span data-stu-id="41513-153">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="41513-154">服務費是營收專屬交易分類。</span><span class="sxs-lookup"><span data-stu-id="41513-154">Fee is a revenue-only transaction class.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="41513-155">工作實體和帳單實體</span><span class="sxs-lookup"><span data-stu-id="41513-155">Work entities and Billing entities</span></span>

<span data-ttu-id="41513-156">代表工作的實體是 [專案] 和 [工作]。</span><span class="sxs-lookup"><span data-stu-id="41513-156">Entities that represent work are projects and tasks.</span></span> <span data-ttu-id="41513-157">代表帳單相關事項的實體是 [合約服務內容]。</span><span class="sxs-lookup"><span data-stu-id="41513-157">Entities that represent billing aspects are contract lines.</span></span> <span data-ttu-id="41513-158">您可以將不同工作實體繫結至合約服務內容，藉此將這些實體繫結至帳單選項。</span><span class="sxs-lookup"><span data-stu-id="41513-158">You can tie different work entities to billing options by tying them to contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="41513-159">多客戶交易</span><span class="sxs-lookup"><span data-stu-id="41513-159">Multi-customer deals</span></span>

<span data-ttu-id="41513-160">多客戶交易會有多個需要開立交易發票的客戶。</span><span class="sxs-lookup"><span data-stu-id="41513-160">Multi- customer deals have more than one customer to invoice on a deal.</span></span> <span data-ttu-id="41513-161">常見的範例包括：</span><span class="sxs-lookup"><span data-stu-id="41513-161">Common examples of this include:</span></span>

- <span data-ttu-id="41513-162">OEM 企業及其合作夥伴：合作夥伴和轉銷商會搭配一些加值服務 (通常涉及與客戶的特定交易) 來銷售產品。</span><span class="sxs-lookup"><span data-stu-id="41513-162">OEM Enterprises and their partners: Partners and resellers sell a product with some value-added services, typically involving a particular deal with a customer.</span></span> <span data-ttu-id="41513-163">OEM 願意為一部分專案提供融資。</span><span class="sxs-lookup"><span data-stu-id="41513-163">The OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="41513-164">公共事業專案：多個當地政府部門同意資助專案，並依據先前議定的分攤額度來開立發票。</span><span class="sxs-lookup"><span data-stu-id="41513-164">Public sector projects: Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="41513-165">例如，學區或當地政府部門同意資助興建游泳池。</span><span class="sxs-lookup"><span data-stu-id="41513-165">For example, s school district and the local government agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="41513-166">發票排程</span><span class="sxs-lookup"><span data-stu-id="41513-166">Invoice Schedules</span></span>

<span data-ttu-id="41513-167">發票排程是每個特定合約服務內容專屬的排程，而且自動發票開立功能必須有此排程才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="41513-167">Invoice schedules are specific to each contract line and are required for automatic invoicing to work.</span></span> <span data-ttu-id="41513-168">發票排程是根據特定開始和完成日期以及發票週期所建立。</span><span class="sxs-lookup"><span data-stu-id="41513-168">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="41513-169">此排程用於設定自動發票建立程序時的合約階段中。</span><span class="sxs-lookup"><span data-stu-id="41513-169">The schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="41513-170">從報價建立專案合約時，發票排程會從報價複製到專案合約。</span><span class="sxs-lookup"><span data-stu-id="41513-170">When a project contract is created from a quote, the invoice schedule is copied to the project contract from the quote.</span></span>

## <a name="changes-from-dynamics-365-sales-orders"></a><span data-ttu-id="41513-171">Dynamics 365 Sales 訂單發生的變更</span><span class="sxs-lookup"><span data-stu-id="41513-171">Changes from Dynamics 365 Sales Orders</span></span>

<span data-ttu-id="41513-172">Project Operations 中的合約是以 Dynamics 365 Sales 中的訂單為基礎所建置。</span><span class="sxs-lookup"><span data-stu-id="41513-172">Contracts in Project Operations are built on Orders in Dynamics 365 Sales.</span></span> <span data-ttu-id="41513-173">不過，在功能上有重要的偏差與變化。</span><span class="sxs-lookup"><span data-stu-id="41513-173">However, there are important deviations and differences in functionality.</span></span> <span data-ttu-id="41513-174">合約有其本身的表單以及 UI 元素、商務規則、外掛程式中的商務規則，以及使其與訂單有所不同的用戶端指令碼。</span><span class="sxs-lookup"><span data-stu-id="41513-174">Contracts have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Orders.</span></span> <span data-ttu-id="41513-175">因此，不要交替使用 Sales 訂單與 Project Operations 合約。</span><span class="sxs-lookup"><span data-stu-id="41513-175">For these reasons, don't use a Sales order and Project Operations contract interchangeably.</span></span>
