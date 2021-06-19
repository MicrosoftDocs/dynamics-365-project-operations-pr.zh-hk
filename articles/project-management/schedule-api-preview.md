---
title: 使用排程 API 對排程實體執行作業
description: 本主題提供有關使用排程 API 的資訊與範例。
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116824"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="ae457-103">使用排程 API 對排程實體執行作業</span><span class="sxs-lookup"><span data-stu-id="ae457-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="ae457-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="ae457-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="ae457-105">本文中提到的部分或所有功能可做為預覽版本的一部分。</span><span class="sxs-lookup"><span data-stu-id="ae457-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="ae457-106">內容和功能隨時可能變更。</span><span class="sxs-lookup"><span data-stu-id="ae457-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="ae457-107">排程實體</span><span class="sxs-lookup"><span data-stu-id="ae457-107">Scheduling entities</span></span>

<span data-ttu-id="ae457-108">排程 API 提供對 **排程實體** 執行建立、更新和刪除作業的功能。</span><span class="sxs-lookup"><span data-stu-id="ae457-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="ae457-109">這些實體是透過 Project for the Web 中的排程引擎進行管理。</span><span class="sxs-lookup"><span data-stu-id="ae457-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="ae457-110">對 **排程實體** 的建立、更新及刪除作業在先前的 Dynamics 365 Project Operations 版本中受到限制。</span><span class="sxs-lookup"><span data-stu-id="ae457-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="ae457-111">下表提供 **排程實體** 的完整清單。</span><span class="sxs-lookup"><span data-stu-id="ae457-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="ae457-112">實體名稱</span><span class="sxs-lookup"><span data-stu-id="ae457-112">Entity name</span></span>  | <span data-ttu-id="ae457-113">實體邏輯名稱</span><span class="sxs-lookup"><span data-stu-id="ae457-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="ae457-114">Project</span><span class="sxs-lookup"><span data-stu-id="ae457-114">Project</span></span> | <span data-ttu-id="ae457-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ae457-115">msdyn_project</span></span> |
| <span data-ttu-id="ae457-116">專案工作</span><span class="sxs-lookup"><span data-stu-id="ae457-116">Project Task</span></span>  | <span data-ttu-id="ae457-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="ae457-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="ae457-118">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="ae457-118">Project Task Dependency</span></span>  | <span data-ttu-id="ae457-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="ae457-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="ae457-120">資源指派</span><span class="sxs-lookup"><span data-stu-id="ae457-120">Resource Assignment</span></span> | <span data-ttu-id="ae457-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="ae457-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="ae457-122">專案貯體</span><span class="sxs-lookup"><span data-stu-id="ae457-122">Project Bucket</span></span>  | <span data-ttu-id="ae457-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="ae457-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="ae457-124">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="ae457-124">Project Team Member</span></span> | <span data-ttu-id="ae457-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="ae457-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="ae457-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="ae457-126">OperationSet</span></span>

<span data-ttu-id="ae457-127">OperationSet 是工作單位模式，當交易中有數個必須處理的排程影響要求時，可以使用此模式。</span><span class="sxs-lookup"><span data-stu-id="ae457-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="ae457-128">排程 API</span><span class="sxs-lookup"><span data-stu-id="ae457-128">Schedule APIs</span></span>

<span data-ttu-id="ae457-129">以下是最新排程 API 的清單。</span><span class="sxs-lookup"><span data-stu-id="ae457-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="ae457-130">**msdyn_CreateProjectV1**：此 API 可以用來建立專案。</span><span class="sxs-lookup"><span data-stu-id="ae457-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="ae457-131">專案和預設專案貯體會立即建立。</span><span class="sxs-lookup"><span data-stu-id="ae457-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="ae457-132">**msdyn_CreateTeamMemberV1**：此 API 可以用來建立專案團隊成員。</span><span class="sxs-lookup"><span data-stu-id="ae457-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="ae457-133">團隊成員記錄會立即建立。</span><span class="sxs-lookup"><span data-stu-id="ae457-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="ae457-134">**msdyn_CreateOperationSetV1**：此 API 可用來排定數個必須在交易中執行的要求。</span><span class="sxs-lookup"><span data-stu-id="ae457-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="ae457-135">**msdyn_PSSCreateV1**：此 API 可以用來建立實體。</span><span class="sxs-lookup"><span data-stu-id="ae457-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="ae457-136">實體可以是任何支援建立作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="ae457-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="ae457-137">**msdyn_PSSUpdateV1**：此 API 可以用來更新實體。</span><span class="sxs-lookup"><span data-stu-id="ae457-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="ae457-138">實體可以是任何支援更新作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="ae457-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="ae457-139">**msdyn_PSSDeleteV1**：此 API 可以用來刪除實體。</span><span class="sxs-lookup"><span data-stu-id="ae457-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="ae457-140">實體可以是任何支援刪除作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="ae457-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="ae457-141">**msdyn_ExecuteOperationSetV1**：此 API 是用來執行指定作業集中所有的作業。</span><span class="sxs-lookup"><span data-stu-id="ae457-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="ae457-142">將排程 API 與 OperationSet 搭配使用</span><span class="sxs-lookup"><span data-stu-id="ae457-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="ae457-143">因為會立即建立同時包含 **CreateProjectV1** 和 **CreateTeamMemberV1** 的記錄，這些 API 無法直接在 **OperationSet** 中使用。</span><span class="sxs-lookup"><span data-stu-id="ae457-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="ae457-144">不過，您可以使用 API 建立所需的記錄、建立 **OperationSet**，然後在 **OperationSet** 中使用這些預先建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="ae457-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="ae457-145">支援的作業</span><span class="sxs-lookup"><span data-stu-id="ae457-145">Supported operations</span></span>

| <span data-ttu-id="ae457-146">排程實體</span><span class="sxs-lookup"><span data-stu-id="ae457-146">Scheduling entity</span></span> | <span data-ttu-id="ae457-147">建立​​</span><span class="sxs-lookup"><span data-stu-id="ae457-147">Create</span></span> | <span data-ttu-id="ae457-148">更新</span><span class="sxs-lookup"><span data-stu-id="ae457-148">Update</span></span> | <span data-ttu-id="ae457-149">Delete</span><span class="sxs-lookup"><span data-stu-id="ae457-149">Delete</span></span> | <span data-ttu-id="ae457-150">重要考量</span><span class="sxs-lookup"><span data-stu-id="ae457-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="ae457-151">專案工作</span><span class="sxs-lookup"><span data-stu-id="ae457-151">Project task</span></span> | <span data-ttu-id="ae457-152">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-152">Yes</span></span> | <span data-ttu-id="ae457-153">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-153">Yes</span></span> | <span data-ttu-id="ae457-154">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-154">Yes</span></span> | <span data-ttu-id="ae457-155">無​​</span><span class="sxs-lookup"><span data-stu-id="ae457-155">None</span></span> |
| <span data-ttu-id="ae457-156">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="ae457-156">Project task dependency</span></span> | <span data-ttu-id="ae457-157">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-157">Yes</span></span> | <span data-ttu-id="ae457-158">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-158">Yes</span></span> | | <span data-ttu-id="ae457-159">不會更新專案工作相依性記錄。</span><span class="sxs-lookup"><span data-stu-id="ae457-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="ae457-160">相反地，可以刪除舊記錄，也可以建立新記錄。</span><span class="sxs-lookup"><span data-stu-id="ae457-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ae457-161">資源指派</span><span class="sxs-lookup"><span data-stu-id="ae457-161">Resource assignment</span></span> | <span data-ttu-id="ae457-162">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-162">Yes</span></span> | <span data-ttu-id="ae457-163">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-163">Yes</span></span> | | <span data-ttu-id="ae457-164">不支援對下列欄位的作業：**BookableResourceID**、**投入量**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="ae457-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="ae457-165">不會更新資源指派記錄。</span><span class="sxs-lookup"><span data-stu-id="ae457-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="ae457-166">相反地，可以刪除舊記錄，也可以建立新記錄。</span><span class="sxs-lookup"><span data-stu-id="ae457-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ae457-167">專案貯體</span><span class="sxs-lookup"><span data-stu-id="ae457-167">Project bucket</span></span> | <span data-ttu-id="ae457-168">無法使用</span><span class="sxs-lookup"><span data-stu-id="ae457-168">N/A</span></span> | <span data-ttu-id="ae457-169">無法使用</span><span class="sxs-lookup"><span data-stu-id="ae457-169">N/A</span></span> | <span data-ttu-id="ae457-170">無法使用</span><span class="sxs-lookup"><span data-stu-id="ae457-170">N/A</span></span> | <span data-ttu-id="ae457-171">預設貯體是使用 **CreateProjectV1** API 所建立。</span><span class="sxs-lookup"><span data-stu-id="ae457-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="ae457-172">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="ae457-172">Project team member</span></span> | <span data-ttu-id="ae457-173">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-173">Yes</span></span> | <span data-ttu-id="ae457-174">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-174">Yes</span></span> | <span data-ttu-id="ae457-175">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-175">Yes</span></span> | <span data-ttu-id="ae457-176">如果是建立作業，請使用 **CreateTeamMemberV1** API。</span><span class="sxs-lookup"><span data-stu-id="ae457-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="ae457-177">Project</span><span class="sxs-lookup"><span data-stu-id="ae457-177">Project</span></span> | <span data-ttu-id="ae457-178">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-178">Yes</span></span> | <span data-ttu-id="ae457-179">.是</span><span class="sxs-lookup"><span data-stu-id="ae457-179">Yes</span></span> | <span data-ttu-id="ae457-180">無法使用</span><span class="sxs-lookup"><span data-stu-id="ae457-180">N/A</span></span> | <span data-ttu-id="ae457-181">不支援對下列欄位的作業：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**投入量**、**EffortCompleted**、**EffortRemaining**、**進度**、**完成**、**TaskEarliestStart** 和 **期間**。</span><span class="sxs-lookup"><span data-stu-id="ae457-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="ae457-182">可以透過包含自訂欄位的實體物件呼叫這些 API。</span><span class="sxs-lookup"><span data-stu-id="ae457-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="ae457-183">識別碼屬性可選用。</span><span class="sxs-lookup"><span data-stu-id="ae457-183">The ID property is optional.</span></span> <span data-ttu-id="ae457-184">如果已提供，則系統會嘗試使用，並在無法使用時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ae457-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="ae457-185">如果未提供，則系統會產生此屬性。</span><span class="sxs-lookup"><span data-stu-id="ae457-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="ae457-186">受限制的欄位</span><span class="sxs-lookup"><span data-stu-id="ae457-186">Restricted fields</span></span>

<span data-ttu-id="ae457-187">下表定義受限制無法 **建立** 和 **編輯** 的欄位。</span><span class="sxs-lookup"><span data-stu-id="ae457-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="ae457-188">專案工作</span><span class="sxs-lookup"><span data-stu-id="ae457-188">Project task</span></span>

| <span data-ttu-id="ae457-189">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="ae457-189">**Logical name**</span></span>                       | <span data-ttu-id="ae457-190">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="ae457-190">**Can create**</span></span> | <span data-ttu-id="ae457-191">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="ae457-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="ae457-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="ae457-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="ae457-193">否</span><span class="sxs-lookup"><span data-stu-id="ae457-193">no</span></span>             | <span data-ttu-id="ae457-194">否</span><span class="sxs-lookup"><span data-stu-id="ae457-194">no</span></span>               |
| <span data-ttu-id="ae457-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="ae457-196">否</span><span class="sxs-lookup"><span data-stu-id="ae457-196">no</span></span>             | <span data-ttu-id="ae457-197">否</span><span class="sxs-lookup"><span data-stu-id="ae457-197">no</span></span>               |
| <span data-ttu-id="ae457-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="ae457-198">msdyn_actualend</span></span>                        | <span data-ttu-id="ae457-199">否</span><span class="sxs-lookup"><span data-stu-id="ae457-199">no</span></span>             | <span data-ttu-id="ae457-200">否</span><span class="sxs-lookup"><span data-stu-id="ae457-200">no</span></span>               |
| <span data-ttu-id="ae457-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="ae457-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="ae457-202">否</span><span class="sxs-lookup"><span data-stu-id="ae457-202">no</span></span>             | <span data-ttu-id="ae457-203">否</span><span class="sxs-lookup"><span data-stu-id="ae457-203">no</span></span>               |
| <span data-ttu-id="ae457-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="ae457-205">否</span><span class="sxs-lookup"><span data-stu-id="ae457-205">no</span></span>             | <span data-ttu-id="ae457-206">否</span><span class="sxs-lookup"><span data-stu-id="ae457-206">no</span></span>               |
| <span data-ttu-id="ae457-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="ae457-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="ae457-208">否</span><span class="sxs-lookup"><span data-stu-id="ae457-208">no</span></span>             | <span data-ttu-id="ae457-209">否</span><span class="sxs-lookup"><span data-stu-id="ae457-209">no</span></span>               |
| <span data-ttu-id="ae457-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="ae457-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="ae457-211">否</span><span class="sxs-lookup"><span data-stu-id="ae457-211">no</span></span>             | <span data-ttu-id="ae457-212">否</span><span class="sxs-lookup"><span data-stu-id="ae457-212">no</span></span>               |
| <span data-ttu-id="ae457-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="ae457-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="ae457-214">否</span><span class="sxs-lookup"><span data-stu-id="ae457-214">no</span></span>             | <span data-ttu-id="ae457-215">否</span><span class="sxs-lookup"><span data-stu-id="ae457-215">no</span></span>               |
| <span data-ttu-id="ae457-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="ae457-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="ae457-217">否</span><span class="sxs-lookup"><span data-stu-id="ae457-217">no</span></span>             | <span data-ttu-id="ae457-218">否</span><span class="sxs-lookup"><span data-stu-id="ae457-218">no</span></span>               |
| <span data-ttu-id="ae457-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ae457-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="ae457-220">否</span><span class="sxs-lookup"><span data-stu-id="ae457-220">no</span></span>             | <span data-ttu-id="ae457-221">否</span><span class="sxs-lookup"><span data-stu-id="ae457-221">no</span></span>               |
| <span data-ttu-id="ae457-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ae457-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="ae457-223">否</span><span class="sxs-lookup"><span data-stu-id="ae457-223">no</span></span>             | <span data-ttu-id="ae457-224">否</span><span class="sxs-lookup"><span data-stu-id="ae457-224">no</span></span>               |
| <span data-ttu-id="ae457-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="ae457-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="ae457-226">否</span><span class="sxs-lookup"><span data-stu-id="ae457-226">no</span></span>             | <span data-ttu-id="ae457-227">否</span><span class="sxs-lookup"><span data-stu-id="ae457-227">no</span></span>               |
| <span data-ttu-id="ae457-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="ae457-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="ae457-229">否</span><span class="sxs-lookup"><span data-stu-id="ae457-229">no</span></span>             | <span data-ttu-id="ae457-230">否</span><span class="sxs-lookup"><span data-stu-id="ae457-230">no</span></span>               |
| <span data-ttu-id="ae457-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="ae457-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="ae457-232">否</span><span class="sxs-lookup"><span data-stu-id="ae457-232">no</span></span>             | <span data-ttu-id="ae457-233">否</span><span class="sxs-lookup"><span data-stu-id="ae457-233">no</span></span>               |
| <span data-ttu-id="ae457-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="ae457-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="ae457-235">否</span><span class="sxs-lookup"><span data-stu-id="ae457-235">no</span></span>             | <span data-ttu-id="ae457-236">否</span><span class="sxs-lookup"><span data-stu-id="ae457-236">no</span></span>               |
| <span data-ttu-id="ae457-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="ae457-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="ae457-238">否</span><span class="sxs-lookup"><span data-stu-id="ae457-238">no</span></span>             | <span data-ttu-id="ae457-239">否</span><span class="sxs-lookup"><span data-stu-id="ae457-239">no</span></span>               |
| <span data-ttu-id="ae457-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="ae457-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="ae457-241">否</span><span class="sxs-lookup"><span data-stu-id="ae457-241">no</span></span>             | <span data-ttu-id="ae457-242">否</span><span class="sxs-lookup"><span data-stu-id="ae457-242">no</span></span>               |
| <span data-ttu-id="ae457-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="ae457-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="ae457-244">否</span><span class="sxs-lookup"><span data-stu-id="ae457-244">no</span></span>             | <span data-ttu-id="ae457-245">否</span><span class="sxs-lookup"><span data-stu-id="ae457-245">no</span></span>               |
| <span data-ttu-id="ae457-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="ae457-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="ae457-247">否</span><span class="sxs-lookup"><span data-stu-id="ae457-247">no</span></span>             | <span data-ttu-id="ae457-248">否</span><span class="sxs-lookup"><span data-stu-id="ae457-248">no</span></span>               |
| <span data-ttu-id="ae457-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="ae457-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="ae457-250">否</span><span class="sxs-lookup"><span data-stu-id="ae457-250">no</span></span>             | <span data-ttu-id="ae457-251">否</span><span class="sxs-lookup"><span data-stu-id="ae457-251">no</span></span>               |
| <span data-ttu-id="ae457-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ae457-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="ae457-253">否</span><span class="sxs-lookup"><span data-stu-id="ae457-253">no</span></span>             | <span data-ttu-id="ae457-254">否</span><span class="sxs-lookup"><span data-stu-id="ae457-254">no</span></span>               |
| <span data-ttu-id="ae457-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="ae457-256">否</span><span class="sxs-lookup"><span data-stu-id="ae457-256">no</span></span>             | <span data-ttu-id="ae457-257">否</span><span class="sxs-lookup"><span data-stu-id="ae457-257">no</span></span>               |
| <span data-ttu-id="ae457-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ae457-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="ae457-259">否</span><span class="sxs-lookup"><span data-stu-id="ae457-259">no</span></span>             | <span data-ttu-id="ae457-260">否</span><span class="sxs-lookup"><span data-stu-id="ae457-260">no</span></span>               |
| <span data-ttu-id="ae457-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="ae457-262">否</span><span class="sxs-lookup"><span data-stu-id="ae457-262">no</span></span>             | <span data-ttu-id="ae457-263">否</span><span class="sxs-lookup"><span data-stu-id="ae457-263">no</span></span>               |
| <span data-ttu-id="ae457-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="ae457-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="ae457-265">否</span><span class="sxs-lookup"><span data-stu-id="ae457-265">no</span></span>             | <span data-ttu-id="ae457-266">否</span><span class="sxs-lookup"><span data-stu-id="ae457-266">no</span></span>               |
| <span data-ttu-id="ae457-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="ae457-267">msdyn_progress</span></span>                         | <span data-ttu-id="ae457-268">否</span><span class="sxs-lookup"><span data-stu-id="ae457-268">no</span></span>             | <span data-ttu-id="ae457-269">否 (對 P4W 則是)</span><span class="sxs-lookup"><span data-stu-id="ae457-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="ae457-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ae457-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="ae457-271">否</span><span class="sxs-lookup"><span data-stu-id="ae457-271">no</span></span>             | <span data-ttu-id="ae457-272">否</span><span class="sxs-lookup"><span data-stu-id="ae457-272">no</span></span>               |
| <span data-ttu-id="ae457-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="ae457-274">否</span><span class="sxs-lookup"><span data-stu-id="ae457-274">no</span></span>             | <span data-ttu-id="ae457-275">否</span><span class="sxs-lookup"><span data-stu-id="ae457-275">no</span></span>               |
| <span data-ttu-id="ae457-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ae457-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="ae457-277">否</span><span class="sxs-lookup"><span data-stu-id="ae457-277">no</span></span>             | <span data-ttu-id="ae457-278">否</span><span class="sxs-lookup"><span data-stu-id="ae457-278">no</span></span>               |
| <span data-ttu-id="ae457-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="ae457-280">否</span><span class="sxs-lookup"><span data-stu-id="ae457-280">no</span></span>             | <span data-ttu-id="ae457-281">否</span><span class="sxs-lookup"><span data-stu-id="ae457-281">no</span></span>               |
| <span data-ttu-id="ae457-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="ae457-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="ae457-283">否</span><span class="sxs-lookup"><span data-stu-id="ae457-283">no</span></span>             | <span data-ttu-id="ae457-284">否</span><span class="sxs-lookup"><span data-stu-id="ae457-284">no</span></span>               |
| <span data-ttu-id="ae457-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ae457-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="ae457-286">否</span><span class="sxs-lookup"><span data-stu-id="ae457-286">no</span></span>             | <span data-ttu-id="ae457-287">否</span><span class="sxs-lookup"><span data-stu-id="ae457-287">no</span></span>               |
| <span data-ttu-id="ae457-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="ae457-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="ae457-289">否</span><span class="sxs-lookup"><span data-stu-id="ae457-289">no</span></span>             | <span data-ttu-id="ae457-290">否</span><span class="sxs-lookup"><span data-stu-id="ae457-290">no</span></span>               |
| <span data-ttu-id="ae457-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="ae457-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="ae457-292">否</span><span class="sxs-lookup"><span data-stu-id="ae457-292">no</span></span>             | <span data-ttu-id="ae457-293">否</span><span class="sxs-lookup"><span data-stu-id="ae457-293">no</span></span>               |
| <span data-ttu-id="ae457-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="ae457-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="ae457-295">否</span><span class="sxs-lookup"><span data-stu-id="ae457-295">no</span></span>             | <span data-ttu-id="ae457-296">否</span><span class="sxs-lookup"><span data-stu-id="ae457-296">no</span></span>               |
| <span data-ttu-id="ae457-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="ae457-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="ae457-298">否</span><span class="sxs-lookup"><span data-stu-id="ae457-298">no</span></span>             | <span data-ttu-id="ae457-299">否</span><span class="sxs-lookup"><span data-stu-id="ae457-299">no</span></span>               |
| <span data-ttu-id="ae457-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ae457-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="ae457-301">否</span><span class="sxs-lookup"><span data-stu-id="ae457-301">no</span></span>             | <span data-ttu-id="ae457-302">否</span><span class="sxs-lookup"><span data-stu-id="ae457-302">no</span></span>               |
| <span data-ttu-id="ae457-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="ae457-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="ae457-304">否</span><span class="sxs-lookup"><span data-stu-id="ae457-304">no</span></span>             | <span data-ttu-id="ae457-305">否</span><span class="sxs-lookup"><span data-stu-id="ae457-305">no</span></span>               |
| <span data-ttu-id="ae457-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="ae457-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="ae457-307">否</span><span class="sxs-lookup"><span data-stu-id="ae457-307">no</span></span>             | <span data-ttu-id="ae457-308">否</span><span class="sxs-lookup"><span data-stu-id="ae457-308">no</span></span>               |
| <span data-ttu-id="ae457-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="ae457-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="ae457-310">否</span><span class="sxs-lookup"><span data-stu-id="ae457-310">no</span></span>             | <span data-ttu-id="ae457-311">否</span><span class="sxs-lookup"><span data-stu-id="ae457-311">no</span></span>               |
| <span data-ttu-id="ae457-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="ae457-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="ae457-313">否</span><span class="sxs-lookup"><span data-stu-id="ae457-313">no</span></span>             | <span data-ttu-id="ae457-314">否</span><span class="sxs-lookup"><span data-stu-id="ae457-314">no</span></span>               |
| <span data-ttu-id="ae457-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="ae457-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="ae457-316">否</span><span class="sxs-lookup"><span data-stu-id="ae457-316">no</span></span>             | <span data-ttu-id="ae457-317">否</span><span class="sxs-lookup"><span data-stu-id="ae457-317">no</span></span>               |
| <span data-ttu-id="ae457-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="ae457-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="ae457-319">否</span><span class="sxs-lookup"><span data-stu-id="ae457-319">no</span></span>             | <span data-ttu-id="ae457-320">否</span><span class="sxs-lookup"><span data-stu-id="ae457-320">no</span></span>               |
| <span data-ttu-id="ae457-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="ae457-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="ae457-322">否</span><span class="sxs-lookup"><span data-stu-id="ae457-322">no</span></span>             | <span data-ttu-id="ae457-323">否</span><span class="sxs-lookup"><span data-stu-id="ae457-323">no</span></span>               |
| <span data-ttu-id="ae457-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="ae457-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="ae457-325">否</span><span class="sxs-lookup"><span data-stu-id="ae457-325">no</span></span>             | <span data-ttu-id="ae457-326">否</span><span class="sxs-lookup"><span data-stu-id="ae457-326">no</span></span>               |
| <span data-ttu-id="ae457-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="ae457-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="ae457-328">否</span><span class="sxs-lookup"><span data-stu-id="ae457-328">no</span></span>             | <span data-ttu-id="ae457-329">否</span><span class="sxs-lookup"><span data-stu-id="ae457-329">no</span></span>               |
| <span data-ttu-id="ae457-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="ae457-330">msdyn_summary</span></span>                          | <span data-ttu-id="ae457-331">否</span><span class="sxs-lookup"><span data-stu-id="ae457-331">no</span></span>             | <span data-ttu-id="ae457-332">否</span><span class="sxs-lookup"><span data-stu-id="ae457-332">no</span></span>               |
| <span data-ttu-id="ae457-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="ae457-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="ae457-334">否</span><span class="sxs-lookup"><span data-stu-id="ae457-334">no</span></span>             | <span data-ttu-id="ae457-335">否</span><span class="sxs-lookup"><span data-stu-id="ae457-335">no</span></span>               |
| <span data-ttu-id="ae457-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="ae457-337">否</span><span class="sxs-lookup"><span data-stu-id="ae457-337">no</span></span>             | <span data-ttu-id="ae457-338">否</span><span class="sxs-lookup"><span data-stu-id="ae457-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="ae457-339">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="ae457-339">Project task dependency</span></span>

| <span data-ttu-id="ae457-340">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="ae457-340">**Logical name**</span></span>              | <span data-ttu-id="ae457-341">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="ae457-341">**Can create**</span></span> | <span data-ttu-id="ae457-342">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="ae457-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="ae457-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="ae457-343">msdyn_linktype</span></span>                | <span data-ttu-id="ae457-344">否</span><span class="sxs-lookup"><span data-stu-id="ae457-344">no</span></span>             | <span data-ttu-id="ae457-345">否</span><span class="sxs-lookup"><span data-stu-id="ae457-345">no</span></span>           |
| <span data-ttu-id="ae457-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="ae457-346">msdyn_linktypename</span></span>            | <span data-ttu-id="ae457-347">否</span><span class="sxs-lookup"><span data-stu-id="ae457-347">no</span></span>             | <span data-ttu-id="ae457-348">否</span><span class="sxs-lookup"><span data-stu-id="ae457-348">no</span></span>           |
| <span data-ttu-id="ae457-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="ae457-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="ae457-350">是</span><span class="sxs-lookup"><span data-stu-id="ae457-350">yes</span></span>            | <span data-ttu-id="ae457-351">否</span><span class="sxs-lookup"><span data-stu-id="ae457-351">no</span></span>           |
| <span data-ttu-id="ae457-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="ae457-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="ae457-353">是</span><span class="sxs-lookup"><span data-stu-id="ae457-353">yes</span></span>            | <span data-ttu-id="ae457-354">否</span><span class="sxs-lookup"><span data-stu-id="ae457-354">no</span></span>           |
| <span data-ttu-id="ae457-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ae457-355">msdyn_project</span></span>                 | <span data-ttu-id="ae457-356">是</span><span class="sxs-lookup"><span data-stu-id="ae457-356">yes</span></span>            | <span data-ttu-id="ae457-357">否</span><span class="sxs-lookup"><span data-stu-id="ae457-357">no</span></span>           |
| <span data-ttu-id="ae457-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="ae457-358">msdyn_projectname</span></span>             | <span data-ttu-id="ae457-359">是</span><span class="sxs-lookup"><span data-stu-id="ae457-359">yes</span></span>            | <span data-ttu-id="ae457-360">否</span><span class="sxs-lookup"><span data-stu-id="ae457-360">no</span></span>           |
| <span data-ttu-id="ae457-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="ae457-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="ae457-362">是</span><span class="sxs-lookup"><span data-stu-id="ae457-362">yes</span></span>            | <span data-ttu-id="ae457-363">否</span><span class="sxs-lookup"><span data-stu-id="ae457-363">no</span></span>           |
| <span data-ttu-id="ae457-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="ae457-364">msdyn_successortask</span></span>           | <span data-ttu-id="ae457-365">是</span><span class="sxs-lookup"><span data-stu-id="ae457-365">yes</span></span>            | <span data-ttu-id="ae457-366">否</span><span class="sxs-lookup"><span data-stu-id="ae457-366">no</span></span>           |
| <span data-ttu-id="ae457-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="ae457-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="ae457-368">是</span><span class="sxs-lookup"><span data-stu-id="ae457-368">yes</span></span>            | <span data-ttu-id="ae457-369">否</span><span class="sxs-lookup"><span data-stu-id="ae457-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="ae457-370">資源指派</span><span class="sxs-lookup"><span data-stu-id="ae457-370">Resource assignment</span></span>

| <span data-ttu-id="ae457-371">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="ae457-371">**Logical name**</span></span>             | <span data-ttu-id="ae457-372">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="ae457-372">**Can create**</span></span> | <span data-ttu-id="ae457-373">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="ae457-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="ae457-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="ae457-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="ae457-375">是</span><span class="sxs-lookup"><span data-stu-id="ae457-375">yes</span></span>            | <span data-ttu-id="ae457-376">否</span><span class="sxs-lookup"><span data-stu-id="ae457-376">no</span></span>           |
| <span data-ttu-id="ae457-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="ae457-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="ae457-378">是</span><span class="sxs-lookup"><span data-stu-id="ae457-378">yes</span></span>            | <span data-ttu-id="ae457-379">否</span><span class="sxs-lookup"><span data-stu-id="ae457-379">no</span></span>           |
| <span data-ttu-id="ae457-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="ae457-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="ae457-381">否</span><span class="sxs-lookup"><span data-stu-id="ae457-381">no</span></span>             | <span data-ttu-id="ae457-382">否</span><span class="sxs-lookup"><span data-stu-id="ae457-382">no</span></span>           |
| <span data-ttu-id="ae457-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="ae457-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="ae457-384">否</span><span class="sxs-lookup"><span data-stu-id="ae457-384">no</span></span>             | <span data-ttu-id="ae457-385">否</span><span class="sxs-lookup"><span data-stu-id="ae457-385">no</span></span>           |
| <span data-ttu-id="ae457-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="ae457-386">msdyn_committype</span></span>             | <span data-ttu-id="ae457-387">否</span><span class="sxs-lookup"><span data-stu-id="ae457-387">no</span></span>             | <span data-ttu-id="ae457-388">否</span><span class="sxs-lookup"><span data-stu-id="ae457-388">no</span></span>           |
| <span data-ttu-id="ae457-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="ae457-389">msdyn_committypename</span></span>         | <span data-ttu-id="ae457-390">否</span><span class="sxs-lookup"><span data-stu-id="ae457-390">no</span></span>             | <span data-ttu-id="ae457-391">否</span><span class="sxs-lookup"><span data-stu-id="ae457-391">no</span></span>           |
| <span data-ttu-id="ae457-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ae457-392">msdyn_effort</span></span>                 | <span data-ttu-id="ae457-393">否</span><span class="sxs-lookup"><span data-stu-id="ae457-393">no</span></span>             | <span data-ttu-id="ae457-394">否</span><span class="sxs-lookup"><span data-stu-id="ae457-394">no</span></span>           |
| <span data-ttu-id="ae457-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ae457-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="ae457-396">否</span><span class="sxs-lookup"><span data-stu-id="ae457-396">no</span></span>             | <span data-ttu-id="ae457-397">否</span><span class="sxs-lookup"><span data-stu-id="ae457-397">no</span></span>           |
| <span data-ttu-id="ae457-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ae457-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="ae457-399">否</span><span class="sxs-lookup"><span data-stu-id="ae457-399">no</span></span>             | <span data-ttu-id="ae457-400">否</span><span class="sxs-lookup"><span data-stu-id="ae457-400">no</span></span>           |
| <span data-ttu-id="ae457-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ae457-401">msdyn_finish</span></span>                 | <span data-ttu-id="ae457-402">否</span><span class="sxs-lookup"><span data-stu-id="ae457-402">no</span></span>             | <span data-ttu-id="ae457-403">否</span><span class="sxs-lookup"><span data-stu-id="ae457-403">no</span></span>           |
| <span data-ttu-id="ae457-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ae457-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="ae457-405">否</span><span class="sxs-lookup"><span data-stu-id="ae457-405">no</span></span>             | <span data-ttu-id="ae457-406">否</span><span class="sxs-lookup"><span data-stu-id="ae457-406">no</span></span>           |
| <span data-ttu-id="ae457-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="ae457-408">否</span><span class="sxs-lookup"><span data-stu-id="ae457-408">no</span></span>             | <span data-ttu-id="ae457-409">否</span><span class="sxs-lookup"><span data-stu-id="ae457-409">no</span></span>           |
| <span data-ttu-id="ae457-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="ae457-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="ae457-411">否</span><span class="sxs-lookup"><span data-stu-id="ae457-411">no</span></span>             | <span data-ttu-id="ae457-412">否</span><span class="sxs-lookup"><span data-stu-id="ae457-412">no</span></span>           |
| <span data-ttu-id="ae457-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ae457-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="ae457-414">否</span><span class="sxs-lookup"><span data-stu-id="ae457-414">no</span></span>             | <span data-ttu-id="ae457-415">否</span><span class="sxs-lookup"><span data-stu-id="ae457-415">no</span></span>           |
| <span data-ttu-id="ae457-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="ae457-417">否</span><span class="sxs-lookup"><span data-stu-id="ae457-417">no</span></span>             | <span data-ttu-id="ae457-418">否</span><span class="sxs-lookup"><span data-stu-id="ae457-418">no</span></span>           |
| <span data-ttu-id="ae457-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="ae457-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="ae457-420">否</span><span class="sxs-lookup"><span data-stu-id="ae457-420">no</span></span>             | <span data-ttu-id="ae457-421">否</span><span class="sxs-lookup"><span data-stu-id="ae457-421">no</span></span>           |
| <span data-ttu-id="ae457-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="ae457-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="ae457-423">否</span><span class="sxs-lookup"><span data-stu-id="ae457-423">no</span></span>             | <span data-ttu-id="ae457-424">否</span><span class="sxs-lookup"><span data-stu-id="ae457-424">no</span></span>           |
| <span data-ttu-id="ae457-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="ae457-425">msdyn_projectid</span></span>              | <span data-ttu-id="ae457-426">是</span><span class="sxs-lookup"><span data-stu-id="ae457-426">yes</span></span>            | <span data-ttu-id="ae457-427">否</span><span class="sxs-lookup"><span data-stu-id="ae457-427">no</span></span>           |
| <span data-ttu-id="ae457-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="ae457-428">msdyn_projectidname</span></span>          | <span data-ttu-id="ae457-429">否</span><span class="sxs-lookup"><span data-stu-id="ae457-429">no</span></span>             | <span data-ttu-id="ae457-430">否</span><span class="sxs-lookup"><span data-stu-id="ae457-430">no</span></span>           |
| <span data-ttu-id="ae457-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="ae457-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="ae457-432">否</span><span class="sxs-lookup"><span data-stu-id="ae457-432">no</span></span>             | <span data-ttu-id="ae457-433">否</span><span class="sxs-lookup"><span data-stu-id="ae457-433">no</span></span>           |
| <span data-ttu-id="ae457-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="ae457-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="ae457-435">否</span><span class="sxs-lookup"><span data-stu-id="ae457-435">no</span></span>             | <span data-ttu-id="ae457-436">否</span><span class="sxs-lookup"><span data-stu-id="ae457-436">no</span></span>           |
| <span data-ttu-id="ae457-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="ae457-437">msdyn_start</span></span>                  | <span data-ttu-id="ae457-438">否</span><span class="sxs-lookup"><span data-stu-id="ae457-438">no</span></span>             | <span data-ttu-id="ae457-439">否</span><span class="sxs-lookup"><span data-stu-id="ae457-439">no</span></span>           |
| <span data-ttu-id="ae457-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="ae457-440">msdyn_taskid</span></span>                 | <span data-ttu-id="ae457-441">否</span><span class="sxs-lookup"><span data-stu-id="ae457-441">no</span></span>             | <span data-ttu-id="ae457-442">否</span><span class="sxs-lookup"><span data-stu-id="ae457-442">no</span></span>           |
| <span data-ttu-id="ae457-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="ae457-443">msdyn_taskidname</span></span>             | <span data-ttu-id="ae457-444">否</span><span class="sxs-lookup"><span data-stu-id="ae457-444">no</span></span>             | <span data-ttu-id="ae457-445">否</span><span class="sxs-lookup"><span data-stu-id="ae457-445">no</span></span>           |
| <span data-ttu-id="ae457-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="ae457-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="ae457-447">否</span><span class="sxs-lookup"><span data-stu-id="ae457-447">no</span></span>             | <span data-ttu-id="ae457-448">否</span><span class="sxs-lookup"><span data-stu-id="ae457-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="ae457-449">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="ae457-449">Project team member</span></span>

| <span data-ttu-id="ae457-450">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="ae457-450">**Logical name**</span></span>                                 | <span data-ttu-id="ae457-451">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="ae457-451">**Can create**</span></span> | <span data-ttu-id="ae457-452">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="ae457-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="ae457-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="ae457-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="ae457-454">否</span><span class="sxs-lookup"><span data-stu-id="ae457-454">no</span></span>             | <span data-ttu-id="ae457-455">否</span><span class="sxs-lookup"><span data-stu-id="ae457-455">no</span></span>           |
| <span data-ttu-id="ae457-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="ae457-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="ae457-457">否</span><span class="sxs-lookup"><span data-stu-id="ae457-457">no</span></span>             | <span data-ttu-id="ae457-458">否</span><span class="sxs-lookup"><span data-stu-id="ae457-458">no</span></span>           |
| <span data-ttu-id="ae457-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="ae457-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="ae457-460">否</span><span class="sxs-lookup"><span data-stu-id="ae457-460">no</span></span>             | <span data-ttu-id="ae457-461">否</span><span class="sxs-lookup"><span data-stu-id="ae457-461">no</span></span>           |
| <span data-ttu-id="ae457-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="ae457-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="ae457-463">否</span><span class="sxs-lookup"><span data-stu-id="ae457-463">no</span></span>             | <span data-ttu-id="ae457-464">否</span><span class="sxs-lookup"><span data-stu-id="ae457-464">no</span></span>           |
| <span data-ttu-id="ae457-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ae457-465">msdyn_effort</span></span>                                     | <span data-ttu-id="ae457-466">否</span><span class="sxs-lookup"><span data-stu-id="ae457-466">no</span></span>             | <span data-ttu-id="ae457-467">否</span><span class="sxs-lookup"><span data-stu-id="ae457-467">no</span></span>           |
| <span data-ttu-id="ae457-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ae457-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="ae457-469">否</span><span class="sxs-lookup"><span data-stu-id="ae457-469">no</span></span>             | <span data-ttu-id="ae457-470">否</span><span class="sxs-lookup"><span data-stu-id="ae457-470">no</span></span>           |
| <span data-ttu-id="ae457-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ae457-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="ae457-472">否</span><span class="sxs-lookup"><span data-stu-id="ae457-472">no</span></span>             | <span data-ttu-id="ae457-473">否</span><span class="sxs-lookup"><span data-stu-id="ae457-473">no</span></span>           |
| <span data-ttu-id="ae457-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ae457-474">msdyn_finish</span></span>                                     | <span data-ttu-id="ae457-475">否</span><span class="sxs-lookup"><span data-stu-id="ae457-475">no</span></span>             | <span data-ttu-id="ae457-476">否</span><span class="sxs-lookup"><span data-stu-id="ae457-476">no</span></span>           |
| <span data-ttu-id="ae457-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="ae457-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="ae457-478">否</span><span class="sxs-lookup"><span data-stu-id="ae457-478">no</span></span>             | <span data-ttu-id="ae457-479">否</span><span class="sxs-lookup"><span data-stu-id="ae457-479">no</span></span>           |
| <span data-ttu-id="ae457-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="ae457-480">msdyn_hours</span></span>                                      | <span data-ttu-id="ae457-481">否</span><span class="sxs-lookup"><span data-stu-id="ae457-481">no</span></span>             | <span data-ttu-id="ae457-482">否</span><span class="sxs-lookup"><span data-stu-id="ae457-482">no</span></span>           |
| <span data-ttu-id="ae457-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="ae457-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="ae457-484">否</span><span class="sxs-lookup"><span data-stu-id="ae457-484">no</span></span>             | <span data-ttu-id="ae457-485">否</span><span class="sxs-lookup"><span data-stu-id="ae457-485">no</span></span>           |
| <span data-ttu-id="ae457-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="ae457-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="ae457-487">否</span><span class="sxs-lookup"><span data-stu-id="ae457-487">no</span></span>             | <span data-ttu-id="ae457-488">否</span><span class="sxs-lookup"><span data-stu-id="ae457-488">no</span></span>           |
| <span data-ttu-id="ae457-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="ae457-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="ae457-490">否</span><span class="sxs-lookup"><span data-stu-id="ae457-490">no</span></span>             | <span data-ttu-id="ae457-491">否</span><span class="sxs-lookup"><span data-stu-id="ae457-491">no</span></span>           |
| <span data-ttu-id="ae457-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="ae457-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="ae457-493">否</span><span class="sxs-lookup"><span data-stu-id="ae457-493">no</span></span>             | <span data-ttu-id="ae457-494">否</span><span class="sxs-lookup"><span data-stu-id="ae457-494">no</span></span>           |
| <span data-ttu-id="ae457-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="ae457-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="ae457-496">否</span><span class="sxs-lookup"><span data-stu-id="ae457-496">no</span></span>             | <span data-ttu-id="ae457-497">否</span><span class="sxs-lookup"><span data-stu-id="ae457-497">no</span></span>           |
| <span data-ttu-id="ae457-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="ae457-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="ae457-499">否</span><span class="sxs-lookup"><span data-stu-id="ae457-499">no</span></span>             | <span data-ttu-id="ae457-500">否</span><span class="sxs-lookup"><span data-stu-id="ae457-500">no</span></span>           |
| <span data-ttu-id="ae457-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="ae457-501">msdyn_start</span></span>                                      | <span data-ttu-id="ae457-502">否</span><span class="sxs-lookup"><span data-stu-id="ae457-502">no</span></span>             | <span data-ttu-id="ae457-503">否</span><span class="sxs-lookup"><span data-stu-id="ae457-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="ae457-504">Project</span><span class="sxs-lookup"><span data-stu-id="ae457-504">Project</span></span>

| <span data-ttu-id="ae457-505">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="ae457-505">**Logical name**</span></span>                       | <span data-ttu-id="ae457-506">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="ae457-506">**Can create**</span></span> | <span data-ttu-id="ae457-507">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="ae457-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="ae457-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="ae457-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="ae457-509">否</span><span class="sxs-lookup"><span data-stu-id="ae457-509">no</span></span>             | <span data-ttu-id="ae457-510">否</span><span class="sxs-lookup"><span data-stu-id="ae457-510">no</span></span>           |
| <span data-ttu-id="ae457-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="ae457-512">否</span><span class="sxs-lookup"><span data-stu-id="ae457-512">no</span></span>             | <span data-ttu-id="ae457-513">否</span><span class="sxs-lookup"><span data-stu-id="ae457-513">no</span></span>           |
| <span data-ttu-id="ae457-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="ae457-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="ae457-515">否</span><span class="sxs-lookup"><span data-stu-id="ae457-515">no</span></span>             | <span data-ttu-id="ae457-516">否</span><span class="sxs-lookup"><span data-stu-id="ae457-516">no</span></span>           |
| <span data-ttu-id="ae457-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="ae457-518">否</span><span class="sxs-lookup"><span data-stu-id="ae457-518">no</span></span>             | <span data-ttu-id="ae457-519">否</span><span class="sxs-lookup"><span data-stu-id="ae457-519">no</span></span>           |
| <span data-ttu-id="ae457-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="ae457-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="ae457-521">否</span><span class="sxs-lookup"><span data-stu-id="ae457-521">no</span></span>             | <span data-ttu-id="ae457-522">否</span><span class="sxs-lookup"><span data-stu-id="ae457-522">no</span></span>           |
| <span data-ttu-id="ae457-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="ae457-524">否</span><span class="sxs-lookup"><span data-stu-id="ae457-524">no</span></span>             | <span data-ttu-id="ae457-525">否</span><span class="sxs-lookup"><span data-stu-id="ae457-525">no</span></span>           |
| <span data-ttu-id="ae457-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="ae457-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="ae457-527">是</span><span class="sxs-lookup"><span data-stu-id="ae457-527">yes</span></span>            | <span data-ttu-id="ae457-528">否</span><span class="sxs-lookup"><span data-stu-id="ae457-528">no</span></span>           |
| <span data-ttu-id="ae457-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="ae457-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="ae457-530">是</span><span class="sxs-lookup"><span data-stu-id="ae457-530">yes</span></span>            | <span data-ttu-id="ae457-531">否</span><span class="sxs-lookup"><span data-stu-id="ae457-531">no</span></span>           |
| <span data-ttu-id="ae457-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="ae457-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="ae457-533">是</span><span class="sxs-lookup"><span data-stu-id="ae457-533">yes</span></span>            | <span data-ttu-id="ae457-534">否</span><span class="sxs-lookup"><span data-stu-id="ae457-534">no</span></span>           |
| <span data-ttu-id="ae457-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="ae457-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="ae457-536">否</span><span class="sxs-lookup"><span data-stu-id="ae457-536">no</span></span>             | <span data-ttu-id="ae457-537">否</span><span class="sxs-lookup"><span data-stu-id="ae457-537">no</span></span>           |
| <span data-ttu-id="ae457-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ae457-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="ae457-539">否</span><span class="sxs-lookup"><span data-stu-id="ae457-539">no</span></span>             | <span data-ttu-id="ae457-540">否</span><span class="sxs-lookup"><span data-stu-id="ae457-540">no</span></span>           |
| <span data-ttu-id="ae457-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="ae457-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="ae457-542">否</span><span class="sxs-lookup"><span data-stu-id="ae457-542">no</span></span>             | <span data-ttu-id="ae457-543">否</span><span class="sxs-lookup"><span data-stu-id="ae457-543">no</span></span>           |
| <span data-ttu-id="ae457-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="ae457-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="ae457-545">否</span><span class="sxs-lookup"><span data-stu-id="ae457-545">no</span></span>             | <span data-ttu-id="ae457-546">否</span><span class="sxs-lookup"><span data-stu-id="ae457-546">no</span></span>           |
| <span data-ttu-id="ae457-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="ae457-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="ae457-548">否</span><span class="sxs-lookup"><span data-stu-id="ae457-548">no</span></span>             | <span data-ttu-id="ae457-549">否</span><span class="sxs-lookup"><span data-stu-id="ae457-549">no</span></span>           |
| <span data-ttu-id="ae457-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="ae457-550">msdyn_duration</span></span>                         | <span data-ttu-id="ae457-551">否</span><span class="sxs-lookup"><span data-stu-id="ae457-551">no</span></span>             | <span data-ttu-id="ae457-552">否</span><span class="sxs-lookup"><span data-stu-id="ae457-552">no</span></span>           |
| <span data-ttu-id="ae457-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ae457-553">msdyn_effort</span></span>                           | <span data-ttu-id="ae457-554">否</span><span class="sxs-lookup"><span data-stu-id="ae457-554">no</span></span>             | <span data-ttu-id="ae457-555">否</span><span class="sxs-lookup"><span data-stu-id="ae457-555">no</span></span>           |
| <span data-ttu-id="ae457-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ae457-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="ae457-557">否</span><span class="sxs-lookup"><span data-stu-id="ae457-557">no</span></span>             | <span data-ttu-id="ae457-558">否</span><span class="sxs-lookup"><span data-stu-id="ae457-558">no</span></span>           |
| <span data-ttu-id="ae457-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="ae457-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="ae457-560">否</span><span class="sxs-lookup"><span data-stu-id="ae457-560">no</span></span>             | <span data-ttu-id="ae457-561">否</span><span class="sxs-lookup"><span data-stu-id="ae457-561">no</span></span>           |
| <span data-ttu-id="ae457-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ae457-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="ae457-563">否</span><span class="sxs-lookup"><span data-stu-id="ae457-563">no</span></span>             | <span data-ttu-id="ae457-564">否</span><span class="sxs-lookup"><span data-stu-id="ae457-564">no</span></span>           |
| <span data-ttu-id="ae457-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ae457-565">msdyn_finish</span></span>                           | <span data-ttu-id="ae457-566">是</span><span class="sxs-lookup"><span data-stu-id="ae457-566">yes</span></span>            | <span data-ttu-id="ae457-567">是</span><span class="sxs-lookup"><span data-stu-id="ae457-567">yes</span></span>          |
| <span data-ttu-id="ae457-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="ae457-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="ae457-569">否</span><span class="sxs-lookup"><span data-stu-id="ae457-569">no</span></span>             | <span data-ttu-id="ae457-570">否</span><span class="sxs-lookup"><span data-stu-id="ae457-570">no</span></span>           |
| <span data-ttu-id="ae457-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="ae457-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="ae457-572">否</span><span class="sxs-lookup"><span data-stu-id="ae457-572">no</span></span>             | <span data-ttu-id="ae457-573">否</span><span class="sxs-lookup"><span data-stu-id="ae457-573">no</span></span>           |
| <span data-ttu-id="ae457-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="ae457-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="ae457-575">否</span><span class="sxs-lookup"><span data-stu-id="ae457-575">no</span></span>             | <span data-ttu-id="ae457-576">否</span><span class="sxs-lookup"><span data-stu-id="ae457-576">no</span></span>           |
| <span data-ttu-id="ae457-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="ae457-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="ae457-578">否</span><span class="sxs-lookup"><span data-stu-id="ae457-578">no</span></span>             | <span data-ttu-id="ae457-579">否</span><span class="sxs-lookup"><span data-stu-id="ae457-579">no</span></span>           |
| <span data-ttu-id="ae457-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="ae457-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="ae457-581">否</span><span class="sxs-lookup"><span data-stu-id="ae457-581">no</span></span>             | <span data-ttu-id="ae457-582">否</span><span class="sxs-lookup"><span data-stu-id="ae457-582">no</span></span>           |
| <span data-ttu-id="ae457-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="ae457-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="ae457-584">否</span><span class="sxs-lookup"><span data-stu-id="ae457-584">no</span></span>             | <span data-ttu-id="ae457-585">否</span><span class="sxs-lookup"><span data-stu-id="ae457-585">no</span></span>           |
| <span data-ttu-id="ae457-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="ae457-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="ae457-587">否</span><span class="sxs-lookup"><span data-stu-id="ae457-587">no</span></span>             | <span data-ttu-id="ae457-588">否</span><span class="sxs-lookup"><span data-stu-id="ae457-588">no</span></span>           |
| <span data-ttu-id="ae457-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="ae457-590">否</span><span class="sxs-lookup"><span data-stu-id="ae457-590">no</span></span>             | <span data-ttu-id="ae457-591">否</span><span class="sxs-lookup"><span data-stu-id="ae457-591">no</span></span>           |
| <span data-ttu-id="ae457-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="ae457-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="ae457-593">否</span><span class="sxs-lookup"><span data-stu-id="ae457-593">no</span></span>             | <span data-ttu-id="ae457-594">否</span><span class="sxs-lookup"><span data-stu-id="ae457-594">no</span></span>           |
| <span data-ttu-id="ae457-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="ae457-596">否</span><span class="sxs-lookup"><span data-stu-id="ae457-596">no</span></span>             | <span data-ttu-id="ae457-597">否</span><span class="sxs-lookup"><span data-stu-id="ae457-597">no</span></span>           |
| <span data-ttu-id="ae457-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ae457-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="ae457-599">否</span><span class="sxs-lookup"><span data-stu-id="ae457-599">no</span></span>             | <span data-ttu-id="ae457-600">否</span><span class="sxs-lookup"><span data-stu-id="ae457-600">no</span></span>           |
| <span data-ttu-id="ae457-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="ae457-602">否</span><span class="sxs-lookup"><span data-stu-id="ae457-602">no</span></span>             | <span data-ttu-id="ae457-603">否</span><span class="sxs-lookup"><span data-stu-id="ae457-603">no</span></span>           |
| <span data-ttu-id="ae457-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="ae457-604">msdyn_progress</span></span>                         | <span data-ttu-id="ae457-605">否</span><span class="sxs-lookup"><span data-stu-id="ae457-605">no</span></span>             | <span data-ttu-id="ae457-606">否</span><span class="sxs-lookup"><span data-stu-id="ae457-606">no</span></span>           |
| <span data-ttu-id="ae457-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ae457-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="ae457-608">否</span><span class="sxs-lookup"><span data-stu-id="ae457-608">no</span></span>             | <span data-ttu-id="ae457-609">否</span><span class="sxs-lookup"><span data-stu-id="ae457-609">no</span></span>           |
| <span data-ttu-id="ae457-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="ae457-611">否</span><span class="sxs-lookup"><span data-stu-id="ae457-611">no</span></span>             | <span data-ttu-id="ae457-612">否</span><span class="sxs-lookup"><span data-stu-id="ae457-612">no</span></span>           |
| <span data-ttu-id="ae457-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ae457-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="ae457-614">否</span><span class="sxs-lookup"><span data-stu-id="ae457-614">no</span></span>             | <span data-ttu-id="ae457-615">否</span><span class="sxs-lookup"><span data-stu-id="ae457-615">no</span></span>           |
| <span data-ttu-id="ae457-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="ae457-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="ae457-617">否</span><span class="sxs-lookup"><span data-stu-id="ae457-617">no</span></span>             | <span data-ttu-id="ae457-618">否</span><span class="sxs-lookup"><span data-stu-id="ae457-618">no</span></span>           |
| <span data-ttu-id="ae457-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="ae457-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="ae457-620">否</span><span class="sxs-lookup"><span data-stu-id="ae457-620">no</span></span>             | <span data-ttu-id="ae457-621">否</span><span class="sxs-lookup"><span data-stu-id="ae457-621">no</span></span>           |
| <span data-ttu-id="ae457-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="ae457-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="ae457-623">否</span><span class="sxs-lookup"><span data-stu-id="ae457-623">no</span></span>             | <span data-ttu-id="ae457-624">否</span><span class="sxs-lookup"><span data-stu-id="ae457-624">no</span></span>           |
| <span data-ttu-id="ae457-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="ae457-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="ae457-626">否</span><span class="sxs-lookup"><span data-stu-id="ae457-626">no</span></span>             | <span data-ttu-id="ae457-627">否</span><span class="sxs-lookup"><span data-stu-id="ae457-627">no</span></span>           |
| <span data-ttu-id="ae457-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="ae457-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="ae457-629">否</span><span class="sxs-lookup"><span data-stu-id="ae457-629">no</span></span>             | <span data-ttu-id="ae457-630">否</span><span class="sxs-lookup"><span data-stu-id="ae457-630">no</span></span>           |
| <span data-ttu-id="ae457-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="ae457-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="ae457-632">否</span><span class="sxs-lookup"><span data-stu-id="ae457-632">no</span></span>             | <span data-ttu-id="ae457-633">否</span><span class="sxs-lookup"><span data-stu-id="ae457-633">no</span></span>           |
| <span data-ttu-id="ae457-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="ae457-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="ae457-635">否</span><span class="sxs-lookup"><span data-stu-id="ae457-635">no</span></span>             | <span data-ttu-id="ae457-636">否</span><span class="sxs-lookup"><span data-stu-id="ae457-636">no</span></span>           |
| <span data-ttu-id="ae457-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="ae457-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="ae457-638">否</span><span class="sxs-lookup"><span data-stu-id="ae457-638">no</span></span>             | <span data-ttu-id="ae457-639">否</span><span class="sxs-lookup"><span data-stu-id="ae457-639">no</span></span>           |
| <span data-ttu-id="ae457-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="ae457-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="ae457-641">否</span><span class="sxs-lookup"><span data-stu-id="ae457-641">no</span></span>             | <span data-ttu-id="ae457-642">否</span><span class="sxs-lookup"><span data-stu-id="ae457-642">no</span></span>           |
| <span data-ttu-id="ae457-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="ae457-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="ae457-644">否</span><span class="sxs-lookup"><span data-stu-id="ae457-644">no</span></span>             | <span data-ttu-id="ae457-645">否</span><span class="sxs-lookup"><span data-stu-id="ae457-645">no</span></span>           |
| <span data-ttu-id="ae457-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="ae457-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="ae457-647">否</span><span class="sxs-lookup"><span data-stu-id="ae457-647">no</span></span>             | <span data-ttu-id="ae457-648">否</span><span class="sxs-lookup"><span data-stu-id="ae457-648">no</span></span>           |
| <span data-ttu-id="ae457-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="ae457-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="ae457-650">否</span><span class="sxs-lookup"><span data-stu-id="ae457-650">no</span></span>             | <span data-ttu-id="ae457-651">否</span><span class="sxs-lookup"><span data-stu-id="ae457-651">no</span></span>           |
| <span data-ttu-id="ae457-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="ae457-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="ae457-653">否</span><span class="sxs-lookup"><span data-stu-id="ae457-653">no</span></span>             | <span data-ttu-id="ae457-654">否</span><span class="sxs-lookup"><span data-stu-id="ae457-654">no</span></span>           |
| <span data-ttu-id="ae457-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="ae457-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="ae457-656">否</span><span class="sxs-lookup"><span data-stu-id="ae457-656">no</span></span>             | <span data-ttu-id="ae457-657">否</span><span class="sxs-lookup"><span data-stu-id="ae457-657">no</span></span>           |
| <span data-ttu-id="ae457-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="ae457-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="ae457-659">否</span><span class="sxs-lookup"><span data-stu-id="ae457-659">no</span></span>             | <span data-ttu-id="ae457-660">否</span><span class="sxs-lookup"><span data-stu-id="ae457-660">no</span></span>           |
| <span data-ttu-id="ae457-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="ae457-662">否</span><span class="sxs-lookup"><span data-stu-id="ae457-662">no</span></span>             | <span data-ttu-id="ae457-663">否</span><span class="sxs-lookup"><span data-stu-id="ae457-663">no</span></span>           |
| <span data-ttu-id="ae457-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="ae457-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="ae457-665">否</span><span class="sxs-lookup"><span data-stu-id="ae457-665">no</span></span>             | <span data-ttu-id="ae457-666">否</span><span class="sxs-lookup"><span data-stu-id="ae457-666">no</span></span>           |
| <span data-ttu-id="ae457-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ae457-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="ae457-668">否</span><span class="sxs-lookup"><span data-stu-id="ae457-668">no</span></span>             | <span data-ttu-id="ae457-669">否</span><span class="sxs-lookup"><span data-stu-id="ae457-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="ae457-670">限制和已知問題</span><span class="sxs-lookup"><span data-stu-id="ae457-670">Limitations and known issues</span></span>
<span data-ttu-id="ae457-671">以下是限制和已知問題的清單：</span><span class="sxs-lookup"><span data-stu-id="ae457-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="ae457-672">只有 **擁有 Microsoft Project 授權的使用者** 才可以使用排程 API。</span><span class="sxs-lookup"><span data-stu-id="ae457-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="ae457-673">無法供下列使用者使用：</span><span class="sxs-lookup"><span data-stu-id="ae457-673">They can't be used by:</span></span>
    - <span data-ttu-id="ae457-674">應用程式使用者</span><span class="sxs-lookup"><span data-stu-id="ae457-674">Application users</span></span>
    - <span data-ttu-id="ae457-675">系統使用者</span><span class="sxs-lookup"><span data-stu-id="ae457-675">System users</span></span>
    - <span data-ttu-id="ae457-676">整合使用者</span><span class="sxs-lookup"><span data-stu-id="ae457-676">Integration users</span></span>
    - <span data-ttu-id="ae457-677">其他沒有必要授權的使用者</span><span class="sxs-lookup"><span data-stu-id="ae457-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="ae457-678">每個 **OperationSet** 最多只能有 100 項作業。</span><span class="sxs-lookup"><span data-stu-id="ae457-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="ae457-679">每個使用者最多只能有 10 個已開啟的 **OperationSet**。</span><span class="sxs-lookup"><span data-stu-id="ae457-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="ae457-680">Project Operations 目前在專案中最多支援總計 500 個工作。</span><span class="sxs-lookup"><span data-stu-id="ae457-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="ae457-681">**OperationSet** 失敗狀態和失敗記錄目前未提供。</span><span class="sxs-lookup"><span data-stu-id="ae457-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="ae457-682">專案和工作的限制與界限</span><span class="sxs-lookup"><span data-stu-id="ae457-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="ae457-683">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="ae457-683">Error handling</span></span>

   - <span data-ttu-id="ae457-684">若要檢閱由作業集所產生的錯誤，請移至 **設定** \> **排程整合** \> **作業集**。</span><span class="sxs-lookup"><span data-stu-id="ae457-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="ae457-685">若要檢閱專案排程服務所產生的錯誤，請移至 **設定** \> **排程整合** \> **PSS 錯誤記錄**。</span><span class="sxs-lookup"><span data-stu-id="ae457-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="ae457-686">範例案例</span><span class="sxs-lookup"><span data-stu-id="ae457-686">Sample scenario</span></span>

<span data-ttu-id="ae457-687">在此案例中，您將會建立專案、團隊成員、四個工作和兩個資源指派。</span><span class="sxs-lookup"><span data-stu-id="ae457-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="ae457-688">接下來，會更新一項工作、更新專案、刪除一項工作、刪除一個資源指派，以及建立工作相依性。</span><span class="sxs-lookup"><span data-stu-id="ae457-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="ae457-689">其他範例</span><span class="sxs-lookup"><span data-stu-id="ae457-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
