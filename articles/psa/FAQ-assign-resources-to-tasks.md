---
title: 將資源指派給工作
description: 本主題提供有關如何將資源指派給工作的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a348130ee5760196b2f008ea811e7a81758dd73e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993263"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="27338-103">將資源指派給工作</span><span class="sxs-lookup"><span data-stu-id="27338-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="27338-104">有三種方法可以在 Microsoft Dynamics 365 Project Service Automation 中指派資源給工作。</span><span class="sxs-lookup"><span data-stu-id="27338-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="27338-105">預約資源做為團隊成員，再將該資源指派給工作</span><span class="sxs-lookup"><span data-stu-id="27338-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="27338-106">您可以將資源新增至專案團隊，然後再將該資源指派給專案排程中的工作。</span><span class="sxs-lookup"><span data-stu-id="27338-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="27338-107">在 **團隊成員** 索引標籤中，選取 **新增** 以將新的團隊成員加入。</span><span class="sxs-lookup"><span data-stu-id="27338-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="27338-108">**團隊成員快速建立面板** 會開啟，您可以在其中選取可預約資源名稱並設定角色。</span><span class="sxs-lookup"><span data-stu-id="27338-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="27338-109">選取下列其中一個配置方法以進行資源預約：</span><span class="sxs-lookup"><span data-stu-id="27338-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="27338-110">**完整產能** 會預約資源在指定之開始和結束日期的完整產能。</span><span class="sxs-lookup"><span data-stu-id="27338-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="27338-111">**產能百分比** 會預約資源在指定之開始和結束日期一定百分比資源的產能。</span><span class="sxs-lookup"><span data-stu-id="27338-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="27338-112">**依時數平均分配** 會預約指定時數的資源，並在指定之開始到結束日期內平均分配每日的時數。</span><span class="sxs-lookup"><span data-stu-id="27338-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="27338-113">**依時數前重後輕** 會預約指定時數的資源，並在指定之開始和結束日期內以前重後輕的方式分配每日的時數。</span><span class="sxs-lookup"><span data-stu-id="27338-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="27338-114">**無** 會將資源新增至團隊，但不建立任何會吸收其產能的預約。</span><span class="sxs-lookup"><span data-stu-id="27338-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="27338-115">在工作的 **排程** 網格中，選取資源儲存格中的 **資源** 圖示，然後在 **團隊成員** 下方選取您剛新增的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="27338-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="27338-116">在 **團隊成員** 和 **協調** 索引標籤上，此資源都會顯示預約時數和指派時數。</span><span class="sxs-lookup"><span data-stu-id="27338-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="27338-117">這些時數應該相同，但不是必要的，因為預約與指派並非緊密聯繫。</span><span class="sxs-lookup"><span data-stu-id="27338-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="27338-118">**協調** 索引標籤會在兩者有差異時提供詳細資料，例如當您指派比您所預約還要多的時數給資源時。</span><span class="sxs-lookup"><span data-stu-id="27338-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="27338-119">如有需要，您可以藉由延長資源預約或變更指派來更正資訊。</span><span class="sxs-lookup"><span data-stu-id="27338-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="27338-120">透過工作指派建立一般團隊成員</span><span class="sxs-lookup"><span data-stu-id="27338-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="27338-121">透過工作指派建立一般團隊成員時，您會建立描述最終要在工作上使用之具名資源特性的預留位置或一般資源。</span><span class="sxs-lookup"><span data-stu-id="27338-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="27338-122">然後您會產生用來搜尋並預約具名資源的需求 (或使用需求送出要求)。</span><span class="sxs-lookup"><span data-stu-id="27338-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="27338-123">在工作的 **排程** 網格中，選取資源儲存格中的 **資源** 圖示。</span><span class="sxs-lookup"><span data-stu-id="27338-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="27338-124">輸入要做為預留位置資源名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="27338-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="27338-125">例如，「方案經理」。</span><span class="sxs-lookup"><span data-stu-id="27338-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="27338-126">選取 **建立**，並在右側的 **快速建立專案團隊成員** 欄位中，設定一般資源的角色。</span><span class="sxs-lookup"><span data-stu-id="27338-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="27338-127">您可以在工作的 **資源選取器** 上選取資源，繼續將工作指派給此預留位置資源。</span><span class="sxs-lookup"><span data-stu-id="27338-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="27338-128">這些資源會在 **團隊成員** 下方列出。</span><span class="sxs-lookup"><span data-stu-id="27338-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="27338-129">完成指派一般資源時，選取 **團隊** 索引標籤上的一般資源，然後選取 **產生需求** 以建立一般資源的資源需求。</span><span class="sxs-lookup"><span data-stu-id="27338-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="27338-130">針對該一般資源選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="27338-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="27338-131">您可以接著使用排程面板來尋找並預約實際的資源。</span><span class="sxs-lookup"><span data-stu-id="27338-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="27338-132">您也可以送出要求資源管理員履行的需求。</span><span class="sxs-lookup"><span data-stu-id="27338-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="27338-133">使用具名資源履行一般資源時，一般資源將會從團隊中移除，而且一般資源的工作指派會指派給履行一般資源之資源需求的具名資源。</span><span class="sxs-lookup"><span data-stu-id="27338-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="27338-134">從所有可預約資源清單中指派具名預約</span><span class="sxs-lookup"><span data-stu-id="27338-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="27338-135">您可以使用 **資源選取器** 中的搜尋方塊，搜尋所有的可預約資源，並將這些資源指派給工作。</span><span class="sxs-lookup"><span data-stu-id="27338-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="27338-136">以此方式指派的資源會新增至沒有任何預約的團隊。</span><span class="sxs-lookup"><span data-stu-id="27338-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="27338-137">這類似於新增團隊成員後，再選取 [無] 做為配置方法。</span><span class="sxs-lookup"><span data-stu-id="27338-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="27338-138">資源會在 **團隊** 和 **協調** 索引標籤中顯示為只有指派而預約短缺的資源。</span><span class="sxs-lookup"><span data-stu-id="27338-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="27338-139">如果您想要使用其可用產能，請加以預約。</span><span class="sxs-lookup"><span data-stu-id="27338-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="27338-140">在工作的 **排程** 網格中，選取資源儲存格中的 **資源** 圖示。</span><span class="sxs-lookup"><span data-stu-id="27338-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="27338-141">開始輸入一個名稱。</span><span class="sxs-lookup"><span data-stu-id="27338-141">Start typing a name.</span></span> <span data-ttu-id="27338-142">該名稱的搜尋結果會顯示在 **資源選取器** 的 **其他資源** 下方。</span><span class="sxs-lookup"><span data-stu-id="27338-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="27338-143">選取您要指派給工作的資源。</span><span class="sxs-lookup"><span data-stu-id="27338-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]