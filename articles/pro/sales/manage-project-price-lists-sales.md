---
title: 管理專案報價上的專案價目表
description: 本主題提供有關在報價上使用專案價目表的資訊。 (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966892"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a><span data-ttu-id="5550b-104">管理專案報價上的專案價目表 (銷售)</span><span class="sxs-lookup"><span data-stu-id="5550b-104">Manage project price lists on project quotes (Sales)</span></span>

<span data-ttu-id="5550b-105">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5550b-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5550b-106">專案報價是為了支援多個有效日期銷售價目表而設計。</span><span class="sxs-lookup"><span data-stu-id="5550b-106">Project quotes are designed to support multiple date effective sales price lists.</span></span> <span data-ttu-id="5550b-107">隨著 Dynamics 365 Project Operations 的推出，新增了名為**專案價目表**的新相關實體。</span><span class="sxs-lookup"><span data-stu-id="5550b-107">With Dynamics 365 Project Operations, a new associated entity called **Project price lists** is added.</span></span> <span data-ttu-id="5550b-108">此實體與專案報價之間有 1 對多的關聯。</span><span class="sxs-lookup"><span data-stu-id="5550b-108">This entity has a 1-to-many relationship to a project quote.</span></span>

<span data-ttu-id="5550b-109">專案價目表會在專案上用來設定時間和費用交易的價格。</span><span class="sxs-lookup"><span data-stu-id="5550b-109">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="5550b-110">當報價有一個或多個專案價目表時，這些價目表會在透過報價明細關聯至報價的專案上用來設定時間和費用估計值及實際值的價格。</span><span class="sxs-lookup"><span data-stu-id="5550b-110">When a quote has one or more project price lists, these price lists are used to price time and expense estimates and actuals on projects that are associated to the quote through the quote line.</span></span>

<span data-ttu-id="5550b-111">專案報價上沒有專案價目表時，您會收到警告訊息。</span><span class="sxs-lookup"><span data-stu-id="5550b-111">When there are no project price lists on a project quote, you will receive a warning message.</span></span> <span data-ttu-id="5550b-112">訊息表示因為沒有專案價目表，無法設定估計和實際的專案工作與費用的價格。</span><span class="sxs-lookup"><span data-stu-id="5550b-112">The message states that because there are no project price lists, your estimated and actual project work and expenses will not be priced.</span></span> <span data-ttu-id="5550b-113">而是有價格為零 (0) 的銷售值。</span><span class="sxs-lookup"><span data-stu-id="5550b-113">Instead, they will have zero (0) price for sales values.</span></span>

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a><span data-ttu-id="5550b-114">在專案報價上建立專案價目表的關聯或將其解除關聯</span><span class="sxs-lookup"><span data-stu-id="5550b-114">Associate or disassociate a project price list on a project quote</span></span>

<span data-ttu-id="5550b-115">若要建立或選取用於估計專案型工作及費用的特定價目表，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="5550b-115">To create or select a specific price list for estimating project-based work and expenses, complete the following steps.</span></span>

1. <span data-ttu-id="5550b-116">在報價上，選取**專案價格**索引標籤，並在子格中，選取 **+ 新增專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="5550b-116">On the quote, select the **Project Price** tab and in the subgrid, select **+ Add New Project Price List**.</span></span>
2. <span data-ttu-id="5550b-117">在 [快速建立] 頁面上，選取價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-117">On the Quick Create page, select a price list.</span></span> <span data-ttu-id="5550b-118">下拉式清單會顯示內容設定為**銷售**且貨幣與報價貨幣相符的所有價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-118">The drop-down list shows all price lists that have the context set to **Sales** and the currency matches the currency on the quote.</span></span>
4. <span data-ttu-id="5550b-119">輸入專案價目表關聯的描述，並選取**儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="5550b-119">Enter a description for the project price list association and select **Save and Close**.</span></span>

<span data-ttu-id="5550b-120">專案價目表關聯已建立。</span><span class="sxs-lookup"><span data-stu-id="5550b-120">A project price list association is created.</span></span>

<span data-ttu-id="5550b-121">如果需要將多個專案價目表與專案報價建立關聯，您可以重複此程序。</span><span class="sxs-lookup"><span data-stu-id="5550b-121">You can repeat this process if you need to associate more than one project price list to the project quote.</span></span> <span data-ttu-id="5550b-122">只有在每個相關聯專案價目表的生效日期都不同時，才要建立多個專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-122">Only create multiple project price lists if you have different effective dates on each of the associated project price lists.</span></span>

> [!NOTE]
> <span data-ttu-id="5550b-123">Project Operations 不支援專案價目表的有效日期範圍重疊。</span><span class="sxs-lookup"><span data-stu-id="5550b-123">Project Operations does't support overlapping date effectivity of the project price lists.</span></span> <span data-ttu-id="5550b-124">如果指定日期的交易有多個專案價目表，則該交易的價格會預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="5550b-124">If there are multiple project prices lists for a transaction with given date, the price on that transaction will be defaulted to zero (0).</span></span>
<span data-ttu-id="5550b-125">若要移除專案價目表關聯，請選取專案價目表，然後選取**刪除報價專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="5550b-125">To remove a project price list association, select the project price list and then select **Delete Quote Project Price List**.</span></span> <span data-ttu-id="5550b-126">價目表會從報價的專案價目表中移除，但是不會將價目表本身刪除。</span><span class="sxs-lookup"><span data-stu-id="5550b-126">The price list is removed from the project price lists of the quote, but the price list itself is not deleted.</span></span> <span data-ttu-id="5550b-127">刪除的只是與報價的關聯。</span><span class="sxs-lookup"><span data-stu-id="5550b-127">Only the association to the quote is deleted.</span></span>

## <a name="set-up-default-project-price-lists-on-a-quote"></a><span data-ttu-id="5550b-128">設定報價上的預設專案價目表</span><span class="sxs-lookup"><span data-stu-id="5550b-128">Set up default project price lists on a quote</span></span>

<span data-ttu-id="5550b-129">您可以將專案價目表設定為專案報價的預設值。</span><span class="sxs-lookup"><span data-stu-id="5550b-129">Project price lists can be set up to default on a project quote.</span></span> <span data-ttu-id="5550b-130">此設定可確保組織中的所有報價一開始都會先使用該價格期間的標準價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-130">This setup ensures that all quotes in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-organizational-default-for-project-price-lists"></a><span data-ttu-id="5550b-131">設定專案價目表的組織預設值</span><span class="sxs-lookup"><span data-stu-id="5550b-131">Set up organizational default for project price lists</span></span>

1. <span data-ttu-id="5550b-132">移至**設定** > **一般** > **參數**。</span><span class="sxs-lookup"><span data-stu-id="5550b-132">Go to **Settings** > **General** > **Parameters**.</span></span>
2. <span data-ttu-id="5550b-133">在**使用中參數**清單頁面上，找出記錄，然後按兩下將其開啟。</span><span class="sxs-lookup"><span data-stu-id="5550b-133">On the **Active Parameters** list page, locate the record and double-click to open it.</span></span> 
3. <span data-ttu-id="5550b-134">在**參數**頁面上，選取**價目表**索引標籤。您可以看到顯示預設價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-134">On the **Parameters** page, select the **Price List** tab. You can see the list of default price lists is shown.</span></span> <span data-ttu-id="5550b-135">這是標準成本清單和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-135">This is a list standard cost and sales price lists.</span></span> <span data-ttu-id="5550b-136">您銷售所用的每一種貨幣在這裡都有相關聯的銷售價目表時，將可確保您為採用此貨幣進行交易的客戶所建立的任何報價都預設會使用此銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-136">Having a sales price list associated here for every currency that you sell in, will ensure that this sales price list is defaulted on any quote that you create for customers that transact in this currency.</span></span>

### <a name="set-up-customer-specific-project-price-lists"></a><span data-ttu-id="5550b-137">設定客戶特定的專案價目表</span><span class="sxs-lookup"><span data-stu-id="5550b-137">Set up customer-specific project price lists</span></span>

<span data-ttu-id="5550b-138">您與客戶議定了主要定價合約時，還可以設定客戶特定的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-138">Customer-specific project price lists can also be set up when you have negotiated a master pricing agreement with your customers.</span></span>

<span data-ttu-id="5550b-139">若要設定客戶特定的專案價目表，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="5550b-139">To set up a customer-specific project price list, complete the following steps.</span></span>

1. <span data-ttu-id="5550b-140">在**銷售**區域中，選取**客戶**。</span><span class="sxs-lookup"><span data-stu-id="5550b-140">In the **Sales** area, select **Customers**.</span></span>
2. <span data-ttu-id="5550b-141">在使用中客戶清單中，選取並開啟您要設定特殊價目表的客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="5550b-141">In the list of your active accounts, select and open the customer record that you have special price list for.</span></span>
3. <span data-ttu-id="5550b-142">在**專案價目表**索引標籤上，您可以建立新的價目表關聯來產生專屬於此客戶的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5550b-142">On the **Project Price Lists** tab, you can create a new price list association to have the project price list that is specific to this customer.</span></span>

## <a name="create-custom-pricing-on-a-project-quote"></a><span data-ttu-id="5550b-143">在專案報價上建立自訂定價</span><span class="sxs-lookup"><span data-stu-id="5550b-143">Create custom pricing on a project quote</span></span>

<span data-ttu-id="5550b-144">有了組織和客戶特定預設專案價目表之後，就會自動使用這些專案價目表關聯來建立您的專案報價。</span><span class="sxs-lookup"><span data-stu-id="5550b-144">After you have organizational and customer-specific default project price lists, your project quotes will automatically be created with these project price list associations.</span></span> <span data-ttu-id="5550b-145">不過，在某些情況下，您可能需要為特定專案報價建立自訂定價。</span><span class="sxs-lookup"><span data-stu-id="5550b-145">However, in certain cases, you may need to create custom pricing for a specific project quote.</span></span> 

1. <span data-ttu-id="5550b-146">在**專案報價**的**專案價目表**索引標籤上，確認子格中沒有選取任何特定價目表記錄。</span><span class="sxs-lookup"><span data-stu-id="5550b-146">On the **Project Quote**, on the **Project Price List** tab, verify in the subgrid that no specific price list record is selected.</span></span>
2. <span data-ttu-id="5550b-147">選取**建立自訂定價**。</span><span class="sxs-lookup"><span data-stu-id="5550b-147">Select **Create Custom Pricing**.</span></span> <span data-ttu-id="5550b-148">這會建立所有目前與報價相關聯標準價目表的複本，並將這些複本與報價建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5550b-148">This will make copies of all the standard price lists currently associated to the quote and associate these copies to the quote.</span></span> <span data-ttu-id="5550b-149">將會移除與標準價目表的現有關聯。</span><span class="sxs-lookup"><span data-stu-id="5550b-149">The existing associations to standard price lists will be removed.</span></span> <span data-ttu-id="5550b-150">銷售人員可以接著開始對這些複本上的價格進行編輯。</span><span class="sxs-lookup"><span data-stu-id="5550b-150">The salesperson can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="5550b-151">這些變更過的價格僅適用於此專案報價。</span><span class="sxs-lookup"><span data-stu-id="5550b-151">These changed prices will be applicable to this project quote only.</span></span>
