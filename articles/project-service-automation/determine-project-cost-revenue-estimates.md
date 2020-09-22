---
title: 決定專案成本與營收預估值
description: 如何決定 Project Service 中的專案成本與營收預估值
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cfa3c0c6-a57d-4d50-90dd-9a517d380257
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fd581cdb84a3a1c0dbbd1b9b27d87ddd959f883
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757231"
---
# <a name="determine-project-cost-and-revenue-estimates"></a><span data-ttu-id="50c2d-103">決定專案成本與營收預估值</span><span class="sxs-lookup"><span data-stu-id="50c2d-103">Determine project cost and revenue estimates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="50c2d-104">專案預估值為專案的分工結構圖中預估和排程的工作提供財務檢視表。</span><span class="sxs-lookup"><span data-stu-id="50c2d-104">Project estimates provide the financial view for the work estimated and scheduled in the project’s work breakdown structure.</span></span> <span data-ttu-id="50c2d-105">估計值檢視表會通知您規劃的工作對成本和營收的影響。</span><span class="sxs-lookup"><span data-stu-id="50c2d-105">The estimates view informs you of the cost and revenue impact of the planned work.</span></span> <span data-ttu-id="50c2d-106">估計值檢視表提供一項工具，可查看許多預先定義維度的資訊，以便通知您專案的財務影響。</span><span class="sxs-lookup"><span data-stu-id="50c2d-106">The estimates view provides a tool to see the information on a number of pre-defined dimensions to best inform you of the financial impact of the project.</span></span>  
  
## <a name="cost-and-sales-value-of-the-project"></a><span data-ttu-id="50c2d-107">專案的成本和銷售值</span><span class="sxs-lookup"><span data-stu-id="50c2d-107">Cost and sales value of the project</span></span>  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="50c2d-108">價目表定義角色專案使用的成本與帳單費率。</span><span class="sxs-lookup"><span data-stu-id="50c2d-108">price lists define the cost and bill rates for roles projects use.</span></span> <span data-ttu-id="50c2d-109">根據與專案的分工結構圖中的工作相關的角色，您可以判斷所涉及工作的成本與營收影響。</span><span class="sxs-lookup"><span data-stu-id="50c2d-109">Based on the roles associated with the tasks in the project’s work breakdown structure, you can determine the cost and revenue impact of the work involved.</span></span>  
  
## <a name="cost-price-defaulting"></a><span data-ttu-id="50c2d-110">預設成本價</span><span class="sxs-lookup"><span data-stu-id="50c2d-110">Cost price defaulting</span></span>  
<span data-ttu-id="50c2d-111">每一個專案都屬於組織 (在專案的**擁有單位**中指出)。</span><span class="sxs-lookup"><span data-stu-id="50c2d-111">Every project belongs to an organization (indicated in **Owning Unit** in the project).</span></span> <span data-ttu-id="50c2d-112">與擁有組織單位相關的價目表決定成本單價。</span><span class="sxs-lookup"><span data-stu-id="50c2d-112">The price list associated with the owning organizational unit determines the unit cost price.</span></span> <span data-ttu-id="50c2d-113">[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]決定角色的成本價，藉由搜尋成本價目表中角色、單位和組織單位的組合，取得估計明細生效日期的正確成本價。</span><span class="sxs-lookup"><span data-stu-id="50c2d-113">The [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determine cost prices for roles by searching for the combination of role, unit, and organizational unit in the cost price list to get the correct cost price for the date effective on estimate lines.</span></span>  
  
<span data-ttu-id="50c2d-114">如果角色、單位和</span><span class="sxs-lookup"><span data-stu-id="50c2d-114">If the combination of role, unit.</span></span> <span data-ttu-id="50c2d-115">組織單位的組合未從擁有單位的價目表產生成本價，則會忽略單位，而採納角色和組織單位的組合。</span><span class="sxs-lookup"><span data-stu-id="50c2d-115">and organizational unit doesn’t result in a cost price from the owning unit’s price list, the unit is disregarded in favor of the combination of role and organizational unit.</span></span> <span data-ttu-id="50c2d-116">如果有成本價，此價格會轉換成您在估計明細上選擇的單位。</span><span class="sxs-lookup"><span data-stu-id="50c2d-116">If there is a cost price, this price is converted to the unit you chose on the estimate line.</span></span>  
  
<span data-ttu-id="50c2d-117">如果角色和組織單位的組合未產生成本價，則會忽略組織單位，而採納角色和單位的組合，且價格會在套用任何轉換 (如需要) 之後預設。</span><span class="sxs-lookup"><span data-stu-id="50c2d-117">If the combination of role and organizational unit doesn’t result in a cost price, the organizational unit is disregarded in favor of the role and unit combination, and the price is defaulted after applying any conversion, if required.</span></span>  
  
 <span data-ttu-id="50c2d-118">如果該角色沒有價格，則估計明細中的成本價會預設為 0.00。</span><span class="sxs-lookup"><span data-stu-id="50c2d-118">If there isn’t a price for the role, then the cost price defaults to 0.00 on the estimate line.</span></span>  
  
 <span data-ttu-id="50c2d-119">在專案成本估計明細上的所有成本金額都是採用擁有組織單位的貨幣。</span><span class="sxs-lookup"><span data-stu-id="50c2d-119">All cost amounts on project cost estimate lines are in the currency of the owning organizational unit.</span></span>  
  
## <a name="sales-price-defaulting"></a><span data-ttu-id="50c2d-120">預設售價</span><span class="sxs-lookup"><span data-stu-id="50c2d-120">Sales price defaulting</span></span>  
<span data-ttu-id="50c2d-121">銷售價目表是根據專案附屬的銷售實體而定。</span><span class="sxs-lookup"><span data-stu-id="50c2d-121">The sales price list is based on the sales entity that the project is attached to.</span></span> <span data-ttu-id="50c2d-122">與報價或合約相關的銷售價目表決定銷售單價。</span><span class="sxs-lookup"><span data-stu-id="50c2d-122">The sales price list associated with the quote or contract determines the unit sales price.</span></span> <span data-ttu-id="50c2d-123">如果報價或合約有自訂價目表，這將會是專案估計值的預設銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="50c2d-123">If the quote or contract has a custom price list, this will be the default sales price list for project estimates.</span></span> <span data-ttu-id="50c2d-124">如果與銷售實體沒有關聯，則在參數設定中設定的預設銷售價目表會是專案的預設銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="50c2d-124">If there is no association to the sales entities, then the default sales price list configured in parameters settings will be the default sales price list for the project.</span></span> <span data-ttu-id="50c2d-125">每個估計明細都有相關的資源組織單位，表示將從中預約資源來完成工作的組織單位。</span><span class="sxs-lookup"><span data-stu-id="50c2d-125">Each estimate line has a resource organizational unit associated to indicate the organizational unit from which the resources will be booked for completing the task.</span></span> <span data-ttu-id="50c2d-126">相關角色的售價的決定方式，是藉由搜尋銷售價目表中角色、單位和資源單位的組合，取得估計明細生效日期的正確售價。</span><span class="sxs-lookup"><span data-stu-id="50c2d-126">The sales price for the associated roles is determined by searching for the combination of role, unit, and resource organizational unit in the sales price list to get the correct sales price for the date effective on the estimate lines.</span></span>  
  
<span data-ttu-id="50c2d-127">如果角色、單位和資源組織單位的組合未從銷售價目表產生售價，系統將忽略單位，並搜尋角色和資源組織單位的組合。</span><span class="sxs-lookup"><span data-stu-id="50c2d-127">If the combination of role, unit, and resource organizational unit doesn’t result in a sales price from the sales price list, the system will disregard unit and search for the combination of role and resource organizational unit.</span></span> <span data-ttu-id="50c2d-128">如果找到售價，此售價將會轉換成您在銷售估計明細上選擇的單位。</span><span class="sxs-lookup"><span data-stu-id="50c2d-128">If a sales price is found, this will be converted to the unit you chose on the sales estimate line.</span></span>  
  
<span data-ttu-id="50c2d-129">如果系統未找到角色的價格，則估計明細中的售價必須預設為 0.00。</span><span class="sxs-lookup"><span data-stu-id="50c2d-129">If the system doesn’t find a price for the role, then the sales price must default to 0.00 on the estimate line.</span></span>  
  
<span data-ttu-id="50c2d-130">估計值檢視表包含網格檢視表，會顯示估計明細的固定網格，當中包含單位和總成本和售價。</span><span class="sxs-lookup"><span data-stu-id="50c2d-130">The estimates view has a grid view that displays a flat grid of estimate lines with unit and total cost and sales price.</span></span>  
  
## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="50c2d-131">專案估計值的分時期檢視表</span><span class="sxs-lookup"><span data-stu-id="50c2d-131">Time-phased view of project estimates</span></span>  
<span data-ttu-id="50c2d-132">在專案估計值的分時期檢視表中，根據預設網格檢視表中的估計值資料會依角色進行樞紐分析，並顯示估計值資料散佈在所選擇時幅的時間表上。</span><span class="sxs-lookup"><span data-stu-id="50c2d-132">In the time-phased view for project estimates, the estimates data from the grid view is pivoted by default by role, and shows a spread of estimate data across the timeline in the chosen timescale.</span></span>  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a><span data-ttu-id="50c2d-133">根據工作模式的努力估計值配置</span><span class="sxs-lookup"><span data-stu-id="50c2d-133">Effort estimate allocation based on task mode</span></span>  
<span data-ttu-id="50c2d-134">在分時期檢視表中，估計投入工作的總努力程度會藉由配置每單位所選擇時幅的時段的特定努力時數分散。</span><span class="sxs-lookup"><span data-stu-id="50c2d-134">In the time-phased view, total effort estimated for the task is distributed by allocating a certain number of effort hours per unit time period of the chosen timescale.</span></span> <span data-ttu-id="50c2d-135">在 Project Service 中，工作模式決定努力在工作期間的配置方式。</span><span class="sxs-lookup"><span data-stu-id="50c2d-135">In project service, the task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="50c2d-136">兩種配置方式分別是平均配置和根據配置的工作時數</span><span class="sxs-lookup"><span data-stu-id="50c2d-136">The two kinds of allocation are even allocation and work hours based allocation</span></span>  
  
## <a name="work-hours-based-allocation"></a><span data-ttu-id="50c2d-137">根據配置的工作時數</span><span class="sxs-lookup"><span data-stu-id="50c2d-137">Work hours based allocation</span></span>  
<span data-ttu-id="50c2d-138">工作的自動排程工作模式會控制對工作估計的資源數，這些資源估計為在每天的完整工作時數期間利用。</span><span class="sxs-lookup"><span data-stu-id="50c2d-138">Auto scheduling task mode for a task governs that for the number of resources estimated on the task, they are estimated to be utilized for the full work hours per day.</span></span> <span data-ttu-id="50c2d-139">這也適用於配置努力，將它分割到分時期檢視表中各項工作的期間。</span><span class="sxs-lookup"><span data-stu-id="50c2d-139">This applies when allocating the effort by splitting it across the duration of tasks in the time phased view as well.</span></span> <span data-ttu-id="50c2d-140">例如，在「天」時幅，用於估計由一個資源完成的工作，每天配置的努力將不會超過專案行事曆中定義的每天工作時數。</span><span class="sxs-lookup"><span data-stu-id="50c2d-140">For instance, on a ‘Day’ timescale, for a task estimated to be completed by one resource, the effort allocated per day will not exceed work hours per day defined in the project’s calendar.</span></span> <span data-ttu-id="50c2d-141">因此，努力配置永遠可確保資源估計為整天使用。</span><span class="sxs-lookup"><span data-stu-id="50c2d-141">Therefore, the effort allocation always ensures that the resources are estimated to be utilized for the full day.</span></span>  
  
## <a name="even-distribution"></a><span data-ttu-id="50c2d-142">平均分佈</span><span class="sxs-lookup"><span data-stu-id="50c2d-142">Even distribution</span></span>  
<span data-ttu-id="50c2d-143">手動排程工作模式不會採用工作時數、專案行事曆，或工作上定義的資源數。</span><span class="sxs-lookup"><span data-stu-id="50c2d-143">Manually scheduled task mode doesn't honor the work hours, project calendar, or number of resources defined on the task.</span></span> <span data-ttu-id="50c2d-144">工作排程是根據使用者輸入而定。</span><span class="sxs-lookup"><span data-stu-id="50c2d-144">The task schedule is based on user input.</span></span> <span data-ttu-id="50c2d-145">對於這類工作，所選擇時幅的每單位時段的努力配置沒有任何限制因素。</span><span class="sxs-lookup"><span data-stu-id="50c2d-145">For such tasks, the effort allocation per unit time period of the chosen timescale doesn't have any limiting factors.</span></span> <span data-ttu-id="50c2d-146">投入工作的總努力程度會平均分割，並配置給所選擇時幅的每單位時段。</span><span class="sxs-lookup"><span data-stu-id="50c2d-146">The total effort on the task is equally split and allocated for each unit time period on the chosen timescale.</span></span>  
  
<span data-ttu-id="50c2d-147">如此一來，工作上定義的工作模式會決定分時期估計值中，每單位時段的努力分佈或努力配置。</span><span class="sxs-lookup"><span data-stu-id="50c2d-147">In this way, the task mode defined on the task determines the effort distribution or allocation of effort per unit time period in time-phased estimates.</span></span>  
  
## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="50c2d-148">分組和分時期選項</span><span class="sxs-lookup"><span data-stu-id="50c2d-148">Grouping and time-phasing options</span></span>  
<span data-ttu-id="50c2d-149">此檢視表可協助您了解以每天、每週、每個月或每年為基礎的努力、成本和銷售估計值的分佈。</span><span class="sxs-lookup"><span data-stu-id="50c2d-149">This view helps you understand the distribution of the effort, cost, and sales estimates on a per day, week, month, or year basis.</span></span> <span data-ttu-id="50c2d-150">[群組依據] 選項可在另外兩個維度上樞紐分析估計值資料：類別及資源。</span><span class="sxs-lookup"><span data-stu-id="50c2d-150">The Group By option allows pivoting the estimates data on two other dimensions: category and resource.</span></span> <span data-ttu-id="50c2d-151">在網格檢視表和分時期檢視表上，您都可以選擇要顯示的欄位。</span><span class="sxs-lookup"><span data-stu-id="50c2d-151">On both the grid view and the time-phased view you can choose the fields to be displayed.</span></span> <span data-ttu-id="50c2d-152">每個時間區塊的總計會顯示在底部，指出</span><span class="sxs-lookup"><span data-stu-id="50c2d-152">Totals for each of the time blocks is displayed at the bottom indicating the total estimated effort, cost.</span></span> <span data-ttu-id="50c2d-153">一天、一週、一個月或一年估計的努力、成本和銷售總計。</span><span class="sxs-lookup"><span data-stu-id="50c2d-153">and sales for the day, week, month, or year.</span></span>  
  
<span data-ttu-id="50c2d-154">成本和售價預設會根據日期生效，角色的費率便更時，它在分時期檢視表中將會更透明，當檢視「資源」上樞紐分析的且依週分時期的估計值資料時。</span><span class="sxs-lookup"><span data-stu-id="50c2d-154">The cost and sales price defaulting takes is date effective—when the rates for the roles change it will be more transparent in the time-phased view when viewing estimate data pivoted on ‘Resource’ and time-phased by week.</span></span>  
  
## <a name="expense-estimates"></a><span data-ttu-id="50c2d-155">費用估計值</span><span class="sxs-lookup"><span data-stu-id="50c2d-155">Expense estimates</span></span>  
<span data-ttu-id="50c2d-156">專案中將發生的任何不是直接與所要擴充人力相關的費用，都可記錄在網格檢視表的專案估計值中。</span><span class="sxs-lookup"><span data-stu-id="50c2d-156">Any expense that will be incurred in the project that is notdirectly related to labor to be expended can be recorded in the project estimates in the grid view.</span></span> <span data-ttu-id="50c2d-157">使用網格檢視表中的**新增費用估計值**選項，就可以完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="50c2d-157">Using the **Add expense estimate** option in the grid view, you can accomplish this.</span></span> <span data-ttu-id="50c2d-158">費用估計值可以針對特定工作或整個專案記錄，您可以在這些明細項目上選擇費用類別，並選擇暫訂日期，當費用預期將發生時。</span><span class="sxs-lookup"><span data-stu-id="50c2d-158">The expense estimates can be recorded for a specific task or for the entire project;you can choose expense categories on these lines and choose a tentative date when the expense is expected to be incurred.</span></span> <span data-ttu-id="50c2d-159">如果相關的成本和銷售價目表有預設的價格，或針對費用類別定義的加成百分比，它會在估計明細上依關聯預設。</span><span class="sxs-lookup"><span data-stu-id="50c2d-159">If the associated cost and sales price list have default prices, or markup percentages defined for expense categories, it will be defaulted on the estimate line on association.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="50c2d-160">請參閱</span><span class="sxs-lookup"><span data-stu-id="50c2d-160">See Also</span></span>  
 [<span data-ttu-id="50c2d-161">專案經理指南</span><span class="sxs-lookup"><span data-stu-id="50c2d-161">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
