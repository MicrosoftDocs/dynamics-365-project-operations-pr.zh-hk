---
title: 在可預約資源擔任專案的多個角色時，估計專案銷售和成本
description: 本主題提供相關資訊，說明如何使用定價維度支援專案中擔任多個角色之資源的定價和成本計算。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291016"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="3be0f-103">在可預約資源擔任專案的多個角色時，估計專案銷售和成本</span><span class="sxs-lookup"><span data-stu-id="3be0f-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3be0f-104">專案型公司通常需要一個資源在專案上扮演多個角色。</span><span class="sxs-lookup"><span data-stu-id="3be0f-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="3be0f-105">其中每一個角色都可以用不同方式進行定價和成本計算，這表示視每個角色的帳單及成本費率而定，專案上同一個資源的工時會得出不同的財務估計值。</span><span class="sxs-lookup"><span data-stu-id="3be0f-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="3be0f-106">Project Service Automation 允許對具名資源的團隊成員記錄進行值設定，並允許每個指派至團隊成員的工作有不同的覆寫值。</span><span class="sxs-lookup"><span data-stu-id="3be0f-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="3be0f-107">下列範例說明簡單覆寫這個值，如何能讓資源在專案上擁有多個使用不同成本及帳單費率的角色。</span><span class="sxs-lookup"><span data-stu-id="3be0f-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="3be0f-108">建立工作</span><span class="sxs-lookup"><span data-stu-id="3be0f-108">Create tasks</span></span>
<span data-ttu-id="3be0f-109">建立兩個各有時數為 40 小時的專案工作：工作 A 和工作 B。選取工作 A 做為工作 B 的前置任務。</span><span class="sxs-lookup"><span data-stu-id="3be0f-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="3be0f-110">設定一般專案團隊成員的角色與組織單位</span><span class="sxs-lookup"><span data-stu-id="3be0f-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="3be0f-111">在 **排程** 頁面上，選取工作 A 的 **工作** 列。</span><span class="sxs-lookup"><span data-stu-id="3be0f-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="3be0f-112">在 **資源** 欄位中，選取下拉式清單中的 **建立**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="3be0f-113">在 **團隊成員快速建立** 頁面上，指定可執行此工作之一般團隊成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="3be0f-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="3be0f-114">選取適當的角色與組織單位，然後選取 **儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="3be0f-115">隨即會建立一般團隊成員，並將其指派至此工作。</span><span class="sxs-lookup"><span data-stu-id="3be0f-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="3be0f-116">對工作 B 重複這些步驟，並確定工作 B 與工作 A 所建立的一般團隊成員，其角色及組織單位各不相同。</span><span class="sxs-lookup"><span data-stu-id="3be0f-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="3be0f-117">設定一般專案的角色及組織單位</span><span class="sxs-lookup"><span data-stu-id="3be0f-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="3be0f-118">建立工作 A 之後，選取該工作，然後選取 **編輯工作**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="3be0f-119">在 **工作詳細資料** 頁面上，尋找 **角色** 和 **組織單位** 欄位，並新增執行此工作之資源所需的值。</span><span class="sxs-lookup"><span data-stu-id="3be0f-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="3be0f-120">如果您要使用 Project Service Automation 示範資料來完成此案例，請為角色選取 **諮詢主管**，並選取 **Fabrikam US** 做為組織單位。</span><span class="sxs-lookup"><span data-stu-id="3be0f-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="3be0f-121">選取工作 B，然後選取 **編輯工作**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="3be0f-122">在 **工作詳細資料** 頁面上，尋找 **角色** 和 **組織單位** 欄位，並新增執行此工作之資源所需的值。</span><span class="sxs-lookup"><span data-stu-id="3be0f-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="3be0f-123">請確定工作 B 與工作 A 在 **角色** 及 **組織單位** 欄位中的值不相同。</span><span class="sxs-lookup"><span data-stu-id="3be0f-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="3be0f-124">如果您要使用 Project Service Automation 示範資料來完成此案例，請為角色選取 **網路技術人員**，並選取 **Fabrikam US** 做為組織單位。</span><span class="sxs-lookup"><span data-stu-id="3be0f-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="3be0f-125">儲存並關閉 **工作詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="3be0f-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="3be0f-126">團隊成員和估計行為</span><span class="sxs-lookup"><span data-stu-id="3be0f-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="3be0f-127">在 **工作詳細資料** 頁面的 **團隊成員** 上，選取兩個一般團隊成員，然後選取 **產生需求**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="3be0f-128">選取 **諮詢主管** 的團隊成員列 ，然後選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="3be0f-129">排程面板會開啟，並將資源預約給該需求。</span><span class="sxs-lookup"><span data-stu-id="3be0f-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="3be0f-130">選取 **網路技術人員** 的團隊成員列 ，然後選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="3be0f-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="3be0f-131">排程面板會開啟，並預約該需求上的相同資源。</span><span class="sxs-lookup"><span data-stu-id="3be0f-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="3be0f-132">團隊成員網格</span><span class="sxs-lookup"><span data-stu-id="3be0f-132">Team Member grid</span></span> 
<span data-ttu-id="3be0f-133">在 **團隊成員** 網格上，您會發現已刪除這兩個一般團隊成員記錄，而且已取代其中一個資源。</span><span class="sxs-lookup"><span data-stu-id="3be0f-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="3be0f-134">該資源有一組值，會顯示一組預設的 **角色** 及 **組織單位** 值。</span><span class="sxs-lookup"><span data-stu-id="3be0f-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="3be0f-135">展開該團隊成員記錄的列時，您可以在這兩個工作的團隊成員記錄中看到不同的指派。</span><span class="sxs-lookup"><span data-stu-id="3be0f-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="3be0f-136">每個指派列在 **角色** 和 **組織單位** 中都會有工作特定的值。</span><span class="sxs-lookup"><span data-stu-id="3be0f-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="3be0f-137">估計值網格</span><span class="sxs-lookup"><span data-stu-id="3be0f-137">Estimates grid</span></span> 
<span data-ttu-id="3be0f-138">瀏覽至 **估計值** 網格時，您會發現同一個資源的這兩個指派各以不同的方式進行定價。</span><span class="sxs-lookup"><span data-stu-id="3be0f-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="3be0f-139">工作 A 的資源指派是使用 **諮詢主管** 的 **角色** 屬性值來定價。</span><span class="sxs-lookup"><span data-stu-id="3be0f-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="3be0f-140">同一個資源在工作 B 上的指派是使用 **網路技術人員** 的 **角色** 屬性值來定價。</span><span class="sxs-lookup"><span data-stu-id="3be0f-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]