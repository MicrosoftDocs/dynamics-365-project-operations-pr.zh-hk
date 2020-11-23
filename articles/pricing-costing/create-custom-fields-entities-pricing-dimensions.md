---
title: 將自訂欄位及實體建立為定價維度
description: 本主題提供有關如何建立自訂選項組或實體的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130920"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="e7ce6-103">將自訂欄位及實體建立為定價維度</span><span class="sxs-lookup"><span data-stu-id="e7ce6-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="e7ce6-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e7ce6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7ce6-105">每當您想要建立自訂選項組或實體時，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7ce6-106">建議您在不同的解決方案中進行所有自訂定價維度變更。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="e7ce6-107">這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e7ce6-108">進行所有必要變更之後，將此解決方案匯出為 **受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="e7ce6-109">建立自訂定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="e7ce6-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="e7ce6-110">移至 **設定** > **解決方案**，然後選取 **新增** 建立新的解決方案。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="e7ce6-111">將解決方案命名為 **\<your organization name> 定價維度**、輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="e7ce6-112">在定價維度解決方案中建立自訂欄位及選項組</span><span class="sxs-lookup"><span data-stu-id="e7ce6-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="e7ce6-113">定價維度可以是選項組或實體。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="e7ce6-114">兩者預必須在定價解決方案中建立。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="e7ce6-115">此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="e7ce6-116">以實體為準的維度</span><span class="sxs-lookup"><span data-stu-id="e7ce6-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="e7ce6-117">移至 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="e7ce6-118">在方案總管的左導覽窗格中，選取 **實體**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="e7ce6-119">選取 **新增** 以建立名為 **標準職稱** 的新實體。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="e7ce6-120">輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="e7ce6-121">以選項組為準的維度</span><span class="sxs-lookup"><span data-stu-id="e7ce6-121">Option set-based dimensions</span></span> 
<span data-ttu-id="e7ce6-122">您可以建立兩個以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="e7ce6-123">使用 **資源工作地點** 來追蹤 **住家** 地點工作和 **現場** 工作的價格，以及使用 **資源工作時數** 搭配 **正常工時** 和 **加班工時** 值，在工作完成時套用加成。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="e7ce6-124">移至 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e7ce6-125">在方案總管的左導覽窗格中，選取 **選項組**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="e7ce6-126">選取 **新增** 建立新的選項組、輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="e7ce6-127">建立以實體為準維度的資料</span><span class="sxs-lookup"><span data-stu-id="e7ce6-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="e7ce6-128">您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料</span><span class="sxs-lookup"><span data-stu-id="e7ce6-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="e7ce6-129">使用此程序中的步驟，從以實體為準的維度 **標準職稱** 建立兩個標準職稱 **系統工程師** 和 **資深系統工程師**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="e7ce6-130">如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="e7ce6-131">選取 **進階尋找**、選取 **標準職稱** 實體，然後選取 **結果**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="e7ce6-132">將會顯示 **標準職稱** 實體中所有的列。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="e7ce6-133">選取 **新增**，並在 **名稱** 欄位中輸入「系統工程師」，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="e7ce6-134">關閉此表單。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-134">Close the form.</span></span> 
4. <span data-ttu-id="e7ce6-135">重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="e7ce6-136">將所有必要的體及相關元件新增至定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="e7ce6-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="e7ce6-137">您必須將下列實體新增至您的定價方案。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="e7ce6-138">使用此程序中的步驟，在定價方案中進行一些重要的結構描述變更，讓實體得知新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="e7ce6-139">選取 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e7ce6-140">在方案總管的左導覽窗格中，選取 **新增現有的** >  **實體**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="e7ce6-141">在 **解決方案元件** 對話方塊中，選取下列實體：</span><span class="sxs-lookup"><span data-stu-id="e7ce6-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="e7ce6-142">實際</span><span class="sxs-lookup"><span data-stu-id="e7ce6-142">Actual</span></span>
  - <span data-ttu-id="e7ce6-143">可預約資源</span><span class="sxs-lookup"><span data-stu-id="e7ce6-143">Bookable Resource</span></span>
  - <span data-ttu-id="e7ce6-144">估計明細</span><span class="sxs-lookup"><span data-stu-id="e7ce6-144">Estimate Line</span></span>
  - <span data-ttu-id="e7ce6-145">發票明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="e7ce6-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="e7ce6-146">帳目明細</span><span class="sxs-lookup"><span data-stu-id="e7ce6-146">Journal Line</span></span>
  - <span data-ttu-id="e7ce6-147">專案合約服務內容詳細資料</span><span class="sxs-lookup"><span data-stu-id="e7ce6-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="e7ce6-148">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="e7ce6-148">Project Team Member</span></span>
  - <span data-ttu-id="e7ce6-149">報價明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="e7ce6-149">Quote Line Detail</span></span>
  - <span data-ttu-id="e7ce6-150">角色價格加成</span><span class="sxs-lookup"><span data-stu-id="e7ce6-150">Role Price Markup</span></span>
  - <span data-ttu-id="e7ce6-151">角色價格</span><span class="sxs-lookup"><span data-stu-id="e7ce6-151">Role Price</span></span> 
  - <span data-ttu-id="e7ce6-152">時間項目</span><span class="sxs-lookup"><span data-stu-id="e7ce6-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="e7ce6-153">請務必包含所選每個實體的所有表單和檢視表。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="e7ce6-154">系統提示您包含上述所選實體的任何相依實體時，選取 **否**。</span><span class="sxs-lookup"><span data-stu-id="e7ce6-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

