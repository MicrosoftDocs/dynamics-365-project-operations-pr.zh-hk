---
title: 管理專案報價上的專案價目表
description: 本主題提供有關在報價上使用專案價目表的資訊。
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912d2fad33ac02c3ba980da7eeb88eef5c331230
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858635"
---
# <a name="manage-project-price-lists-on-project-quotes"></a><span data-ttu-id="e9b5e-103">管理專案報價上的專案價目表</span><span class="sxs-lookup"><span data-stu-id="e9b5e-103">Manage project price lists on project quotes</span></span> 

<span data-ttu-id="e9b5e-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e9b5e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e9b5e-105">專案報價是為了支援多個有效日期銷售價目表而設計。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-105">Project quotes are designed to support multiple date effective sales price lists.</span></span> <span data-ttu-id="e9b5e-106">在 Dynamics 365 Project Operations 中，加入了新的名為 **專案價目表** 的相關實體。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-106">With Dynamics 365 Project Operations, a new associated entity called **Project price lists** is added.</span></span> <span data-ttu-id="e9b5e-107">此實體與專案報價之間有 1 對多的關聯。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-107">This entity has a 1-to-many relationship to a project quote.</span></span>

<span data-ttu-id="e9b5e-108">專案價目表可用於訂定專案中時間、材料及費用交易的價格。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="e9b5e-109">當報價有一份或多份專案價目表時，這些價目表會在透過報價明細與報價產生關聯的專案上，用於訂定時間、材料、費用估計值及實際值的價格。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-109">When a quote has one or more project price lists, these price lists are used to price time, material, expense estimates, and actuals on projects that are associated to the quote through the quote line.</span></span>

<span data-ttu-id="e9b5e-110">專案報價上沒有專案價目表時，您會收到警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-110">When there are no project price lists on a project quote, you will receive a warning message.</span></span> <span data-ttu-id="e9b5e-111">訊息表示因為沒有專案價目表，無法設定估計和實際的專案工作與費用的價格。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-111">The message states that because there are no project price lists, your estimated and actual project work and expenses will not be priced.</span></span> <span data-ttu-id="e9b5e-112">而是有價格為零 (0) 的銷售值。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-112">Instead, they will have zero (0) price for sales values.</span></span>

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a><span data-ttu-id="e9b5e-113">在專案報價上建立專案價目表的關聯或將其解除關聯</span><span class="sxs-lookup"><span data-stu-id="e9b5e-113">Associate or disassociate a project price list on a project quote</span></span>

<span data-ttu-id="e9b5e-114">若要建立或選取用於估計專案型工作及費用的特定價目表，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-114">To create or select a specific price list for estimating project-based work and expenses, complete the following steps.</span></span>

1. <span data-ttu-id="e9b5e-115">在報價上，選取 **專案價格** 索引標籤，並在子格中，選取 **+ 新增專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-115">On the quote, select the **Project Price** tab and in the subgrid, select **+ Add New Project Price List**.</span></span>
2. <span data-ttu-id="e9b5e-116">在 [快速建立] 頁面上，選取價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-116">On the Quick Create page, select a price list.</span></span> <span data-ttu-id="e9b5e-117">下拉式清單會顯示內容設定為 **銷售** 且貨幣與報價貨幣相符的所有價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-117">The drop-down list shows all price lists that have the context set to **Sales** and the currency matches the currency on the quote.</span></span>
4. <span data-ttu-id="e9b5e-118">輸入專案價目表關聯的描述，並選取 **儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-118">Enter a description for the project price list association and select **Save and Close**.</span></span>

<span data-ttu-id="e9b5e-119">專案價目表關聯已建立。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-119">A project price list association is created.</span></span>

<span data-ttu-id="e9b5e-120">如果需要將多個專案價目表與專案報價建立關聯，您可以重複此程序。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-120">You can repeat this process if you need to associate more than one project price list to the project quote.</span></span> <span data-ttu-id="e9b5e-121">只有在每個相關聯專案價目表的生效日期都不同時，才要建立多個專案價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-121">Only create multiple project price lists if you have different effective dates on each of the associated project price lists.</span></span>

> [!NOTE]
> <span data-ttu-id="e9b5e-122">Project Operations 不支援專案價目表的有效日期範圍重疊。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-122">Project Operations does't support overlapping date effectivity of the project price lists.</span></span> <span data-ttu-id="e9b5e-123">如果指定日期的交易有多個專案價目表，則該交易的價格會預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-123">If there are multiple project prices lists for a transaction with given date, the price on that transaction will be defaulted to zero (0).</span></span>
<span data-ttu-id="e9b5e-124">若要移除專案價目表關聯，請選取專案價目表，然後選取 **刪除報價專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-124">To remove a project price list association, select the project price list and then select **Delete Quote Project Price List**.</span></span> <span data-ttu-id="e9b5e-125">價目表會從報價的專案價目表中移除，但是不會將價目表本身刪除。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-125">The price list is removed from the project price lists of the quote, but the price list itself is not deleted.</span></span> <span data-ttu-id="e9b5e-126">刪除的只是與報價的關聯。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-126">Only the association to the quote is deleted.</span></span>

## <a name="set-up-default-project-price-lists-on-a-quote"></a><span data-ttu-id="e9b5e-127">設定報價上的預設專案價目表</span><span class="sxs-lookup"><span data-stu-id="e9b5e-127">Set up default project price lists on a quote</span></span>

<span data-ttu-id="e9b5e-128">您可以將專案價目表設定為專案報價的預設值。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-128">Project price lists can be set up to default on a project quote.</span></span> <span data-ttu-id="e9b5e-129">此設定可確保組織中的所有報價一開始都會先使用該價格期間的標準價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-129">This setup ensures that all quotes in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-organizational-default-for-project-price-lists"></a><span data-ttu-id="e9b5e-130">設定專案價目表的組織預設值</span><span class="sxs-lookup"><span data-stu-id="e9b5e-130">Set up organizational default for project price lists</span></span>

1. <span data-ttu-id="e9b5e-131">移至 **設定** > **一般** > **參數**。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-131">Go to **Settings** > **General** > **Parameters**.</span></span>
2. <span data-ttu-id="e9b5e-132">在 **使用中參數** 清單頁面上，找出記錄，然後按兩下將其開啟。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-132">On the **Active Parameters** list page, locate the record and double-click to open it.</span></span> 
3. <span data-ttu-id="e9b5e-133">在 **參數** 頁面上，選取 **價目表** 索引標籤。您可以看到顯示預設價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-133">On the **Parameters** page, select the **Price List** tab. You can see the list of default price lists is shown.</span></span> <span data-ttu-id="e9b5e-134">這是標準成本清單和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-134">This is a list standard cost and sales price lists.</span></span> <span data-ttu-id="e9b5e-135">您銷售所用的每一種貨幣在這裡都有相關聯的銷售價目表時，將可確保您為採用此貨幣進行交易的客戶所建立的任何報價都預設會使用此銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-135">Having a sales price list associated here for every currency that you sell in, will ensure that this sales price list is defaulted on any quote that you create for customers that transact in this currency.</span></span>

### <a name="set-up-customer-specific-project-price-lists"></a><span data-ttu-id="e9b5e-136">設定客戶特定的專案價目表</span><span class="sxs-lookup"><span data-stu-id="e9b5e-136">Set up customer-specific project price lists</span></span>

<span data-ttu-id="e9b5e-137">您與客戶議定了主要定價合約時，還可以設定客戶特定的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-137">Customer-specific project price lists can also be set up when you have negotiated a master pricing agreement with your customers.</span></span>

<span data-ttu-id="e9b5e-138">若要設定客戶特定的專案價目表，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-138">To set up a customer-specific project price list, complete the following steps.</span></span>

1. <span data-ttu-id="e9b5e-139">在 **銷售** 區域中，選取 **客戶**。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-139">In the **Sales** area, select **Customers**.</span></span>
2. <span data-ttu-id="e9b5e-140">在使用中客戶清單中，選取並開啟您要設定特殊價目表的客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-140">In the list of your active accounts, select and open the customer record that you have special price list for.</span></span>
3. <span data-ttu-id="e9b5e-141">在 **專案價目表** 索引標籤上，您可以建立新的價目表關聯來產生專屬於此客戶的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-141">On the **Project Price Lists** tab, you can create a new price list association to have the project price list that is specific to this customer.</span></span>

## <a name="create-custom-pricing-on-a-project-quote"></a><span data-ttu-id="e9b5e-142">在專案報價上建立自訂定價</span><span class="sxs-lookup"><span data-stu-id="e9b5e-142">Create custom pricing on a project quote</span></span>

<span data-ttu-id="e9b5e-143">有了組織和客戶特定預設專案價目表之後，就會自動使用這些專案價目表關聯來建立您的專案報價。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-143">After you have organizational and customer-specific default project price lists, your project quotes will automatically be created with these project price list associations.</span></span> <span data-ttu-id="e9b5e-144">不過，在某些情況下，您可能需要為特定專案報價建立自訂定價。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-144">However, in certain cases, you may need to create custom pricing for a specific project quote.</span></span> 

1. <span data-ttu-id="e9b5e-145">在 **專案報價** 的 **專案價目表** 索引標籤上，確認子格中沒有選取任何特定價目表記錄。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-145">On the **Project Quote**, on the **Project Price List** tab, verify in the subgrid that no specific price list record is selected.</span></span>
2. <span data-ttu-id="e9b5e-146">選取 **建立自訂定價**。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-146">Select **Create Custom Pricing**.</span></span> <span data-ttu-id="e9b5e-147">這會建立所有目前與報價相關聯標準價目表的複本，並將這些複本與報價建立關聯。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-147">This will make copies of all the standard price lists currently associated to the quote and associate these copies to the quote.</span></span> <span data-ttu-id="e9b5e-148">將會移除與標準價目表的現有關聯。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-148">The existing associations to standard price lists will be removed.</span></span> <span data-ttu-id="e9b5e-149">銷售人員可以接著開始對這些複本上的價格進行編輯。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-149">The salesperson can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="e9b5e-150">這些變更過的價格僅適用於此專案報價。</span><span class="sxs-lookup"><span data-stu-id="e9b5e-150">These changed prices will be applicable to this project quote only.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
