---
title: 透過分工結構圖排程專案
description: 如何使用 Project Service 中的分工結構圖排程專案 (Project Service Automation)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757314"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="db868-103">使用分工結構圖排程專案 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="db868-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="db868-104">專案排程會溝通哪些工作需要執行，哪些資源將執行這些工作，以及需要完成工作的時間。</span><span class="sxs-lookup"><span data-stu-id="db868-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="db868-105">專案排程會反映所有與按時交付專案相關的所有工作。</span><span class="sxs-lookup"><span data-stu-id="db868-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="db868-106">在專案初期的前幾個步驟之一，是擬訂專案排程。</span><span class="sxs-lookup"><span data-stu-id="db868-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="db868-107">若要建立專案排程，您需要建立分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="db868-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="db868-108">使用分工結構圖建立專案結構，有助於：</span><span class="sxs-lookup"><span data-stu-id="db868-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="db868-109">將工作細分成可管理的工作</span><span class="sxs-lookup"><span data-stu-id="db868-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="db868-110">評估完成工作所需的時間</span><span class="sxs-lookup"><span data-stu-id="db868-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="db868-111">設定工作相依性及工作期間</span><span class="sxs-lookup"><span data-stu-id="db868-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="db868-112">決定完成每項工作所需的角色</span><span class="sxs-lookup"><span data-stu-id="db868-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="db868-113">分工結構圖中的專案排程有熟悉的外觀與操作方式，連同互動式甘特圖表。</span><span class="sxs-lookup"><span data-stu-id="db868-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="db868-114">建立專案的分工結構圖</span><span class="sxs-lookup"><span data-stu-id="db868-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="db868-115">建立分工結構圖來呈現專案中工作的順序。</span><span class="sxs-lookup"><span data-stu-id="db868-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="db868-116">分工結構圖包括工作、每項工作的要求，以及營收和成本資訊。</span><span class="sxs-lookup"><span data-stu-id="db868-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="db868-117">在您的分工結構圖中，可以新增：</span><span class="sxs-lookup"><span data-stu-id="db868-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="db868-118">階層式工作順序</span><span class="sxs-lookup"><span data-stu-id="db868-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="db868-119">其他工作 (如果有的話)，必須先完成這些工作，才能開始某一項工作。</span><span class="sxs-lookup"><span data-stu-id="db868-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="db868-120">工作開始日期、結束日期和工作期間</span><span class="sxs-lookup"><span data-stu-id="db868-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="db868-121">工作所需時數</span><span class="sxs-lookup"><span data-stu-id="db868-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="db868-122">任何必要的工作者技能和教育</span><span class="sxs-lookup"><span data-stu-id="db868-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="db868-123">指派至工作的工作者</span><span class="sxs-lookup"><span data-stu-id="db868-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="db868-124">預估營收和成本</span><span class="sxs-lookup"><span data-stu-id="db868-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="db868-125">工作類型</span><span class="sxs-lookup"><span data-stu-id="db868-125">Task types</span></span>  
<span data-ttu-id="db868-126">在建立分工結構圖時，您將使用下列類型的工作：</span><span class="sxs-lookup"><span data-stu-id="db868-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="db868-127">**專案根節點**</span><span class="sxs-lookup"><span data-stu-id="db868-127">**Project root node**</span></span> | <span data-ttu-id="db868-128">專案的最上層摘要工作。</span><span class="sxs-lookup"><span data-stu-id="db868-128">The top-level summary task for the project.</span></span> <span data-ttu-id="db868-129">所有其他專案工作都會在它底下建立。</span><span class="sxs-lookup"><span data-stu-id="db868-129">All other project tasks are created under it.</span></span> <span data-ttu-id="db868-130">根工作的名稱是專案名稱。</span><span class="sxs-lookup"><span data-stu-id="db868-130">The name of the root task is the project name.</span></span> <span data-ttu-id="db868-131">根節點的投入程度、日期和期間是根據其底下階層的值而定。</span><span class="sxs-lookup"><span data-stu-id="db868-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="db868-132">您無法編輯根節點屬性或刪除根節點。</span><span class="sxs-lookup"><span data-stu-id="db868-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="db868-133">**摘要或容器工作**</span><span class="sxs-lookup"><span data-stu-id="db868-133">**Summary or container tasks**</span></span> | <span data-ttu-id="db868-134">摘要工作是底下擁有子工作的工作。</span><span class="sxs-lookup"><span data-stu-id="db868-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="db868-135">摘要工作沒有自己的工作量或成本。</span><span class="sxs-lookup"><span data-stu-id="db868-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="db868-136">其工作量與成本是其子工作的彙總。</span><span class="sxs-lookup"><span data-stu-id="db868-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="db868-137">您可以變更摘要工作的名稱，但是無法變更投入程度、日期或期間，因為這些是自動計算出。</span><span class="sxs-lookup"><span data-stu-id="db868-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="db868-138">刪除摘要工作也會刪除工作和所有其子工作。</span><span class="sxs-lookup"><span data-stu-id="db868-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="db868-139">**分葉節點工作**</span><span class="sxs-lookup"><span data-stu-id="db868-139">**Leaf node tasks**</span></span> | <span data-ttu-id="db868-140">分葉節點工作代表專案中最詳細的工作。</span><span class="sxs-lookup"><span data-stu-id="db868-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="db868-141">它擁有預估的工作量、規劃的資源數、規劃的開始和結束日期，以及期間。</span><span class="sxs-lookup"><span data-stu-id="db868-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="db868-142">工作階層</span><span class="sxs-lookup"><span data-stu-id="db868-142">Task hierarchy</span></span>  
 <span data-ttu-id="db868-143">建立工作階層時，有下列選項：</span><span class="sxs-lookup"><span data-stu-id="db868-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="db868-144">**新增工作**。</span><span class="sxs-lookup"><span data-stu-id="db868-144">**Add task**.</span></span>   <span data-ttu-id="db868-145">您可以在工作階層中選擇的位置新增工作。</span><span class="sxs-lookup"><span data-stu-id="db868-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="db868-146">如果您未選取位置，新工作會顯示在結尾。</span><span class="sxs-lookup"><span data-stu-id="db868-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="db868-147">**縮排工作**。</span><span class="sxs-lookup"><span data-stu-id="db868-147">**Indent task**.</span></span>   <span data-ttu-id="db868-148">縮排工作，讓它成為其正上方工作的子項。</span><span class="sxs-lookup"><span data-stu-id="db868-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="db868-149">**凸排工作**。</span><span class="sxs-lookup"><span data-stu-id="db868-149">**Outdent task**.</span></span>   <span data-ttu-id="db868-150">凸排工作，讓它不再是其原始上層工作的子工作。</span><span class="sxs-lookup"><span data-stu-id="db868-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="db868-151">**上移和下移**。</span><span class="sxs-lookup"><span data-stu-id="db868-151">**Move up and Move down**.</span></span>   <span data-ttu-id="db868-152">在工作的上層工作的階層中上移和下移。</span><span class="sxs-lookup"><span data-stu-id="db868-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="db868-153">將工作上下移動不會影響其投入程度、成本、日期或期間。</span><span class="sxs-lookup"><span data-stu-id="db868-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="db868-154">工作屬性</span><span class="sxs-lookup"><span data-stu-id="db868-154">Task attributes</span></span>  
 <span data-ttu-id="db868-155">工作的名稱說明需要完成的工作。</span><span class="sxs-lookup"><span data-stu-id="db868-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="db868-156">您使用不同的工作屬性描述工作的排程和人員配置需求。</span><span class="sxs-lookup"><span data-stu-id="db868-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="db868-157">排程屬性</span><span class="sxs-lookup"><span data-stu-id="db868-157">Schedule attributes</span></span>

 - <span data-ttu-id="db868-158">將值指派至**努力時數**、**資源數目**、**開始日期**、**結束日期**及**期間**，以決定工作的排程。</span><span class="sxs-lookup"><span data-stu-id="db868-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="db868-159">**努力**是完成工作的預估時數。</span><span class="sxs-lookup"><span data-stu-id="db868-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="db868-160">**資源數目**是專案經理投入工作的預估值，以協助擬訂最佳排程。</span><span class="sxs-lookup"><span data-stu-id="db868-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="db868-161">**期間** (天數) 表示完成工作所需的工作天數。</span><span class="sxs-lookup"><span data-stu-id="db868-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="db868-162">人員配置屬性</span><span class="sxs-lookup"><span data-stu-id="db868-162">Staffing attributes</span></span>

 - <span data-ttu-id="db868-163">**角色**、**資源組織單位**、**資源數目**及**資源**描述工作的人員配置需求。</span><span class="sxs-lookup"><span data-stu-id="db868-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="db868-164">**角色**描述執行工作所需的資源類型。</span><span class="sxs-lookup"><span data-stu-id="db868-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="db868-165">**資源組織單位**表示為該工作配置的人員資源所屬的組織單位；這也會影響工作的成本和銷售估計值，因為這會在決定資源的銷售單價時納入考量。</span><span class="sxs-lookup"><span data-stu-id="db868-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="db868-166">**資源**保存一班資源或具名資源 (如果有的話)。</span><span class="sxs-lookup"><span data-stu-id="db868-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="db868-167">工作相依性</span><span class="sxs-lookup"><span data-stu-id="db868-167">Task dependencies</span></span>  
 <span data-ttu-id="db868-168">您可以在分工結構圖中的一個或多個工作之間建立前置任務關係。</span><span class="sxs-lookup"><span data-stu-id="db868-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="db868-169">您可以在工作的前置任務欄位中設定一個或多個值，表示將與該工作相依的工作。</span><span class="sxs-lookup"><span data-stu-id="db868-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="db868-170">當您指派前置任務值至工作時，該工作只有在所有前置任務工作完成時才能開始。</span><span class="sxs-lookup"><span data-stu-id="db868-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="db868-171">在工作上設定此相依性會重新計算工作規劃的開始日期，以所有其前置任務的最後結束日期為準。</span><span class="sxs-lookup"><span data-stu-id="db868-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="db868-172">對排程的前置任務相關影響，不受工作上所定義的工作模式的限制。</span><span class="sxs-lookup"><span data-stu-id="db868-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="db868-173">工作模式</span><span class="sxs-lookup"><span data-stu-id="db868-173">Task mode</span></span>  
 <span data-ttu-id="db868-174">工作模式是決定排程分葉節點工作的其中一個重要因素。</span><span class="sxs-lookup"><span data-stu-id="db868-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="db868-175">每一項工作有兩種工作模式：自動排程模式和手動排程模式。</span><span class="sxs-lookup"><span data-stu-id="db868-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="db868-176">**自動排程**。</span><span class="sxs-lookup"><span data-stu-id="db868-176">**Auto scheduling**.</span></span>   <span data-ttu-id="db868-177">當您將工作模式設定為 [自動排程] 時，工作排程引擎會對下列工作屬性使用工作排程規則以決定工作的排程：</span><span class="sxs-lookup"><span data-stu-id="db868-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="db868-178">前置任務</span><span class="sxs-lookup"><span data-stu-id="db868-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="db868-179">努力</span><span class="sxs-lookup"><span data-stu-id="db868-179">Effort</span></span>  
  
    -   <span data-ttu-id="db868-180">資源數目</span><span class="sxs-lookup"><span data-stu-id="db868-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="db868-181">開始和結束日期</span><span class="sxs-lookup"><span data-stu-id="db868-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="db868-182">**排程規則**。</span><span class="sxs-lookup"><span data-stu-id="db868-182">**Scheduling rules**.</span></span>   <span data-ttu-id="db868-183">沒有前置任務的分葉節點工作的開始日期會預設為專案的排程開始日期。</span><span class="sxs-lookup"><span data-stu-id="db868-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="db868-184">分葉節點工作的期間一律計算為開始和結束日期之間的工作天數。</span><span class="sxs-lookup"><span data-stu-id="db868-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="db868-185">自動排程工作時，排程引擎會依照下列規則：</span><span class="sxs-lookup"><span data-stu-id="db868-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="db868-186">工作的開始與結束日期必須一律為工作天數，根據專案的排程行事曆</span><span class="sxs-lookup"><span data-stu-id="db868-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="db868-187">有前置任務的工作的開始日期預設為其前置任務的最後結束日期</span><span class="sxs-lookup"><span data-stu-id="db868-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="db868-188">努力 = 人數 \* 期間 \* 專案行事曆的標準工作日中的時數</span><span class="sxs-lookup"><span data-stu-id="db868-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="db868-189">**手動排程**。</span><span class="sxs-lookup"><span data-stu-id="db868-189">**Manual scheduling**.</span></span>   <span data-ttu-id="db868-190">在某些情況下，您可能想要偏離這些規則。</span><span class="sxs-lookup"><span data-stu-id="db868-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="db868-191">在這些情況下，您可以設定手動排程工作的工作模式。</span><span class="sxs-lookup"><span data-stu-id="db868-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="db868-192">這樣就會停止排程引擎計算其他排程屬性的值。</span><span class="sxs-lookup"><span data-stu-id="db868-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="db868-193">設定工作的前置任務一律會影響相依工作的開始日期。</span><span class="sxs-lookup"><span data-stu-id="db868-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="db868-194">建立分工結構圖</span><span class="sxs-lookup"><span data-stu-id="db868-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="db868-195">移至 **Project Service > 專案**。</span><span class="sxs-lookup"><span data-stu-id="db868-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="db868-196">按一下您要處理的專案。</span><span class="sxs-lookup"><span data-stu-id="db868-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="db868-197">在橫跨畫面頂端的列中，選取專案名稱旁的向下箭頭，然後按一下 [分工結構圖]。</span><span class="sxs-lookup"><span data-stu-id="db868-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="db868-198">若要新增工作，按一下**新增工作**。</span><span class="sxs-lookup"><span data-stu-id="db868-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="db868-199">填入工作的欄位，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="db868-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="db868-200">繼續新增工作，直到分工結構圖完成。</span><span class="sxs-lookup"><span data-stu-id="db868-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="db868-201">建立分工結構圖時，您可以執行下列動作來組織工作：</span><span class="sxs-lookup"><span data-stu-id="db868-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="db868-202">選取工作並按一下**縮排**，將工作移到另一項工作底下，或按一下 [凸排] 將它移出一層。</span><span class="sxs-lookup"><span data-stu-id="db868-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="db868-203">選取工作並按一下**上移**或**下移**，在青單中上下移動。</span><span class="sxs-lookup"><span data-stu-id="db868-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="db868-204">按一下**隱藏甘特圖**隱藏甘特圖表，按一下**顯示甘特圖**即可再次顯示。</span><span class="sxs-lookup"><span data-stu-id="db868-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="db868-205">在**時幅**中為甘特圖選取不同的時段。</span><span class="sxs-lookup"><span data-stu-id="db868-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="db868-206">若要將您在分工結構圖中指定的角色新增至專案的團隊成員，按一下**產生專案團隊**。</span><span class="sxs-lookup"><span data-stu-id="db868-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="db868-207">當您完成變更時，按一下畫面右下角的**儲存**。</span><span class="sxs-lookup"><span data-stu-id="db868-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="db868-208">請參閱</span><span class="sxs-lookup"><span data-stu-id="db868-208">See Also</span></span>  
 [<span data-ttu-id="db868-209">專案經理指南</span><span class="sxs-lookup"><span data-stu-id="db868-209">Project manager guide</span></span>](../project-service/project-manager-guide.md)
