---
title: 將專案估計值直接從 Project Service Automation 同步處理至 Finance and Operations
description: 本主題說明用於將專案工時估計與專案費用估計直接從 Microsoft Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999743"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cecec-103">將專案估計值直接從 Project Service Automation 同步處理至 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cecec-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cecec-104">本主題說明用於將專案工時估計與專案費用估計直接從 Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。</span><span class="sxs-lookup"><span data-stu-id="cecec-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="cecec-105">專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。</span><span class="sxs-lookup"><span data-stu-id="cecec-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="cecec-106">實際值整合可在 8.0.1 版或更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="cecec-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="cecec-107">Project Service Automation 至 Finance 的資料流程</span><span class="sxs-lookup"><span data-stu-id="cecec-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="cecec-108">Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="cecec-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="cecec-109">可與資料整合功能搭配使用的整合範本會啟用有關專案工時估計與專案費用估計從 Project Service Automation 到 Finance 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="cecec-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cecec-110">下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="cecec-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="cecec-111">[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="cecec-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="cecec-112">專案工時估計</span><span class="sxs-lookup"><span data-stu-id="cecec-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cecec-113">範本與工作</span><span class="sxs-lookup"><span data-stu-id="cecec-113">Template and tasks</span></span>

<span data-ttu-id="cecec-114">若要存取可用範本，請在 Microsoft Power Apps 系統管理中心選取 **專案**，然後選取右上角的 **新增專案** 以選取公用範本。</span><span class="sxs-lookup"><span data-stu-id="cecec-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cecec-115">下列範本與基礎工作會用來將專案工時估計從 Project Service Automation 同步處理至 Finance：</span><span class="sxs-lookup"><span data-stu-id="cecec-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="cecec-116">**資料整合中範本的名稱：** 專案工時估計 (PSA 至 Fin 和 Ops)</span><span class="sxs-lookup"><span data-stu-id="cecec-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cecec-117">**專案中工作的名稱：**</span><span class="sxs-lookup"><span data-stu-id="cecec-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cecec-118">交易關聯</span><span class="sxs-lookup"><span data-stu-id="cecec-118">Transaction relationships</span></span>
    - <span data-ttu-id="cecec-119">費用估計值</span><span class="sxs-lookup"><span data-stu-id="cecec-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="cecec-120">實體集</span><span class="sxs-lookup"><span data-stu-id="cecec-120">Entity set</span></span>

| <span data-ttu-id="cecec-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cecec-121">Project Service Automation</span></span> | <span data-ttu-id="cecec-122">財務</span><span class="sxs-lookup"><span data-stu-id="cecec-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="cecec-123">專案工作</span><span class="sxs-lookup"><span data-stu-id="cecec-123">Project tasks</span></span>              | <span data-ttu-id="cecec-124">專案工時估計的整合實體</span><span class="sxs-lookup"><span data-stu-id="cecec-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="cecec-125">實體流程</span><span class="sxs-lookup"><span data-stu-id="cecec-125">Entity flow</span></span>

<span data-ttu-id="cecec-126">專案工時估計是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案工時預測。</span><span class="sxs-lookup"><span data-stu-id="cecec-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cecec-127">先決條件</span><span class="sxs-lookup"><span data-stu-id="cecec-127">Prerequisites</span></span>

<span data-ttu-id="cecec-128">進行專案工時估計之前，您必須同步處理專案、專案工作和專案費用交易類別。</span><span class="sxs-lookup"><span data-stu-id="cecec-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cecec-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="cecec-129">Power Query</span></span>

<span data-ttu-id="cecec-130">在專案工時估計範本中，您必須使用 Microsoft Power Query for Excel 來完成這些工作：</span><span class="sxs-lookup"><span data-stu-id="cecec-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="cecec-131">設定整合建立新工時預測時，將使用的預設預測模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="cecec-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="cecec-132">在會讓工時預測中整合失敗的工作中，篩除任何資源特定記錄。</span><span class="sxs-lookup"><span data-stu-id="cecec-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="cecec-133">篩除任何空白交易類別列。</span><span class="sxs-lookup"><span data-stu-id="cecec-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="cecec-134">未能完成此工作可能會造成不正確的工時預測。</span><span class="sxs-lookup"><span data-stu-id="cecec-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="cecec-135">設定預設預測模型識別碼</span><span class="sxs-lookup"><span data-stu-id="cecec-135">Set the default forecast model ID</span></span>

<span data-ttu-id="cecec-136">若要更新範本中的預設預測模型識別碼，請按一下 **對應** 箭頭以開啟對應。</span><span class="sxs-lookup"><span data-stu-id="cecec-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cecec-137">然後選取 **進階查詢及篩選** 連結。</span><span class="sxs-lookup"><span data-stu-id="cecec-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="cecec-138">如果您使用預設「專案工時估計 (PSA 至 Fin 和 Ops)」範本，請選取 **已套用的步驟** 清單中的 **插入的條件**。</span><span class="sxs-lookup"><span data-stu-id="cecec-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="cecec-139">在 **函數** 項目中，將 **O\_forecast** 取代為應與整合搭配使用的預測模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="cecec-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="cecec-140">預設範本具有示範資料中的預測模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="cecec-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="cecec-141">如果您要建立新範本，就必須新增此欄。</span><span class="sxs-lookup"><span data-stu-id="cecec-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="cecec-142">在 Power Query 中，選取 **新增條件欄**，並輸入新欄的名稱，例如 **ModelID**。</span><span class="sxs-lookup"><span data-stu-id="cecec-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="cecec-143">輸入該欄的條件，如果專案工作不是 Null，則為 \<enter the forecast model ID\>；否則為 Null。</span><span class="sxs-lookup"><span data-stu-id="cecec-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="cecec-144">篩除資源特定記錄</span><span class="sxs-lookup"><span data-stu-id="cecec-144">Filter out resource-specific records</span></span>

<span data-ttu-id="cecec-145">「專案工時估計 (PSA 至 Fin 和 Ops)」範本有一個會移除任何資源特定記錄的預設篩選。</span><span class="sxs-lookup"><span data-stu-id="cecec-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="cecec-146">如果您自行建立範本，就必須新增此篩選。</span><span class="sxs-lookup"><span data-stu-id="cecec-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="cecec-147">選取 **進階查詢及篩選** 連結以篩選 **msdyn\_islinetask** 欄，這樣就只會包含 **否** 記錄。</span><span class="sxs-lookup"><span data-stu-id="cecec-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="cecec-148">篩除空白交易類別列</span><span class="sxs-lookup"><span data-stu-id="cecec-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="cecec-149">您必須新增篩選，以移除任何具有空白交易類別的列。</span><span class="sxs-lookup"><span data-stu-id="cecec-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="cecec-150">不論您是使用預設範本還是自行建立範本，此工作都是必要工作。</span><span class="sxs-lookup"><span data-stu-id="cecec-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="cecec-151">此篩選會從 Project Service Automation 中移除任何可能會在 Finance 中造成工時預測不正確的摘要列。</span><span class="sxs-lookup"><span data-stu-id="cecec-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="cecec-152">選取 **進階查詢及篩選** 連結，以篩除 **msdyn\_transactioncategory\_value** 欄中的 Null 記錄。</span><span class="sxs-lookup"><span data-stu-id="cecec-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cecec-153">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="cecec-153">Template mapping in Data integration</span></span>

<span data-ttu-id="cecec-154">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="cecec-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="cecec-155">此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="cecec-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cecec-156">[![資料整合中的範本工作對應](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cecec-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="cecec-157">專案費用估計</span><span class="sxs-lookup"><span data-stu-id="cecec-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cecec-158">範本與工作</span><span class="sxs-lookup"><span data-stu-id="cecec-158">Template and tasks</span></span>

<span data-ttu-id="cecec-159">下列範本與基礎工作會用來將專案費用估計從 Project Service Automation 同步處理至 Finance：</span><span class="sxs-lookup"><span data-stu-id="cecec-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="cecec-160">**資料整合中範本的名稱：** 專案費用估計 (PSA 至 Fin 和 Ops)</span><span class="sxs-lookup"><span data-stu-id="cecec-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cecec-161">**專案中工作的名稱：**</span><span class="sxs-lookup"><span data-stu-id="cecec-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cecec-162">交易關聯</span><span class="sxs-lookup"><span data-stu-id="cecec-162">Transaction relationships</span></span> 
    - <span data-ttu-id="cecec-163">費用估計值</span><span class="sxs-lookup"><span data-stu-id="cecec-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="cecec-164">實體集</span><span class="sxs-lookup"><span data-stu-id="cecec-164">Entity set</span></span>

| <span data-ttu-id="cecec-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cecec-165">Project Service Automation</span></span> | <span data-ttu-id="cecec-166">財務</span><span class="sxs-lookup"><span data-stu-id="cecec-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="cecec-167">交易人脈</span><span class="sxs-lookup"><span data-stu-id="cecec-167">Transaction Connections</span></span>    | <span data-ttu-id="cecec-168">專案交易關聯的整合實體</span><span class="sxs-lookup"><span data-stu-id="cecec-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="cecec-169">估計明細</span><span class="sxs-lookup"><span data-stu-id="cecec-169">Estimate Lines</span></span>             | <span data-ttu-id="cecec-170">專案費用估計的整合實體</span><span class="sxs-lookup"><span data-stu-id="cecec-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="cecec-171">實體流程</span><span class="sxs-lookup"><span data-stu-id="cecec-171">Entity flow</span></span>

<span data-ttu-id="cecec-172">專案費用估計是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案費用預測。</span><span class="sxs-lookup"><span data-stu-id="cecec-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cecec-173">先決條件</span><span class="sxs-lookup"><span data-stu-id="cecec-173">Prerequisites</span></span>

<span data-ttu-id="cecec-174">進行專案費用估計之前，您必須同步處理專案、專案工作和專案費用交易類別。</span><span class="sxs-lookup"><span data-stu-id="cecec-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cecec-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="cecec-175">Power Query</span></span>

<span data-ttu-id="cecec-176">在專案費用估計範本中，您必須使用 Power Query 來完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="cecec-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="cecec-177">篩選成僅包含費用估計明細記錄。</span><span class="sxs-lookup"><span data-stu-id="cecec-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="cecec-178">設定整合建立新工時預測時，將使用的預設預測模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="cecec-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="cecec-179">轉換帳單類型。</span><span class="sxs-lookup"><span data-stu-id="cecec-179">Transform the billing types.</span></span>
- <span data-ttu-id="cecec-180">轉換交易類型。</span><span class="sxs-lookup"><span data-stu-id="cecec-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="cecec-181">篩選成僅包含費用估計明細</span><span class="sxs-lookup"><span data-stu-id="cecec-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="cecec-182">「專案費用估計 (PSA 至 Fin 和 Ops)」範本有一個只會將費用明細包含在整合中預設篩選。</span><span class="sxs-lookup"><span data-stu-id="cecec-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="cecec-183">如果您自行建立範本，就必須新增此篩選。</span><span class="sxs-lookup"><span data-stu-id="cecec-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="cecec-184">選取 **交易關聯** 工作，然後按一下 **對應** 箭頭以開啟對應。</span><span class="sxs-lookup"><span data-stu-id="cecec-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cecec-185">選取 **進階查詢及篩選** 連結。</span><span class="sxs-lookup"><span data-stu-id="cecec-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="cecec-186">篩選 **msdyn\_transactiontype1** 欄，使其僅包含 **msdyn\_estimateline**。</span><span class="sxs-lookup"><span data-stu-id="cecec-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="cecec-187">設定預設預測模型識別碼</span><span class="sxs-lookup"><span data-stu-id="cecec-187">Set the default forecast model ID</span></span>

<span data-ttu-id="cecec-188">若要更新範本中的預設預測模型識別碼，請選取 **費用估計** 工作，然後按一下 **對應** 箭頭以開啟對應。</span><span class="sxs-lookup"><span data-stu-id="cecec-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cecec-189">選取 **進階查詢及篩選** 連結。</span><span class="sxs-lookup"><span data-stu-id="cecec-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="cecec-190">如果您使用預設「專案費用估計 (PSA 至 Fin 和 Ops)」範本，請在 Power Query 中，從 **已套用的步驟** 區段中選取第一個 **插入的條件**。</span><span class="sxs-lookup"><span data-stu-id="cecec-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="cecec-191">在 **函數** 項目中，將 **O\_forecast** 取代為應與整合搭配使用的預測模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="cecec-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="cecec-192">預設範本具有示範資料中的預測模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="cecec-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="cecec-193">如果您要建立新範本，就必須新增此欄。</span><span class="sxs-lookup"><span data-stu-id="cecec-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="cecec-194">在 Power Query 中，選取 **新增條件欄**，並輸入新欄的名稱，例如 **ModelID**。</span><span class="sxs-lookup"><span data-stu-id="cecec-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="cecec-195">輸入該欄的條件，如果估計明細識別碼不是 Null，則為 \<enter the forecast model ID\>；否則為 Null。</span><span class="sxs-lookup"><span data-stu-id="cecec-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="cecec-196">轉換帳單類型</span><span class="sxs-lookup"><span data-stu-id="cecec-196">Transform the billing types</span></span>

<span data-ttu-id="cecec-197">「專案費用估計 (PSA 至 Fin 和 Ops)」範本包含一個用來轉換整合期間從 Project Service Automation 所收到帳單類型的條件欄。</span><span class="sxs-lookup"><span data-stu-id="cecec-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="cecec-198">如果您自行建立範本，就必須新增此條件欄。</span><span class="sxs-lookup"><span data-stu-id="cecec-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="cecec-199">選取 **進階查詢及篩選** 連結，然後選取 **新增條件欄**。</span><span class="sxs-lookup"><span data-stu-id="cecec-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="cecec-200">輸入新欄的名稱，例如 **BillingType**。</span><span class="sxs-lookup"><span data-stu-id="cecec-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="cecec-201">接著輸入下列條件︰</span><span class="sxs-lookup"><span data-stu-id="cecec-201">Then enter the following condition:</span></span>

<span data-ttu-id="cecec-202">如果 **msdyn\_billingtype** = 192350000，則為 **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="cecec-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="cecec-203">否則如果 **msdyn\_billingtype** = 192350001，則為 **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="cecec-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="cecec-204">否則如果 **msdyn\_billingtype** = 192350002，則為 **免費贈送**</span><span class="sxs-lookup"><span data-stu-id="cecec-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="cecec-205">否則為 **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="cecec-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="cecec-206">轉換交易類型</span><span class="sxs-lookup"><span data-stu-id="cecec-206">Transform the transaction types</span></span>

<span data-ttu-id="cecec-207">「專案費用估計 (PSA 至 Fin 和 Ops)」範本包含一個用來轉換整合期間從 Project Service Automation 所收到交易類型的條件欄。</span><span class="sxs-lookup"><span data-stu-id="cecec-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="cecec-208">如果您自行建立範本，就必須新增此條件欄。</span><span class="sxs-lookup"><span data-stu-id="cecec-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="cecec-209">選取 **進階查詢及篩選** 連結，然後選取 **新增條件欄**。</span><span class="sxs-lookup"><span data-stu-id="cecec-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="cecec-210">輸入新欄的名稱，例如 **TransactionType**。</span><span class="sxs-lookup"><span data-stu-id="cecec-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="cecec-211">接著輸入下列條件︰</span><span class="sxs-lookup"><span data-stu-id="cecec-211">Then enter the following condition:</span></span>

<span data-ttu-id="cecec-212">如果 **msdyn\_transactiontypecode** = 192350000，則為 **成本**</span><span class="sxs-lookup"><span data-stu-id="cecec-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="cecec-213">否則如果 **msdyn\_transactiontypecode** = 192350005，則為 **銷售**</span><span class="sxs-lookup"><span data-stu-id="cecec-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="cecec-214">否則為 **Null**</span><span class="sxs-lookup"><span data-stu-id="cecec-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cecec-215">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="cecec-215">Template mapping in Data integration</span></span>

<span data-ttu-id="cecec-216">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="cecec-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="cecec-217">此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="cecec-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cecec-218">[![費用評估交易的範本對應](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cecec-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="cecec-219">[![費用估計值的範本對應](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cecec-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]