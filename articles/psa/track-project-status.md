---
title: 追蹤專案狀態
description: 如何追蹤 Project Service 中的專案狀態
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014413"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="65811-103">追蹤專案狀態 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="65811-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="65811-104">使用 [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]追蹤客戶專案的進度。</span><span class="sxs-lookup"><span data-stu-id="65811-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="65811-105">做為互動進度，專案階段會更新以反映互動的階段：</span><span class="sxs-lookup"><span data-stu-id="65811-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="65811-106">**新增**</span><span class="sxs-lookup"><span data-stu-id="65811-106">**New**</span></span>    | <span data-ttu-id="65811-107">當您建立專案時，階段會設為 **新**。</span><span class="sxs-lookup"><span data-stu-id="65811-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="65811-108">如果您從範本建立專案，在此階段專案可能會有排程、估計值和團隊資料。</span><span class="sxs-lookup"><span data-stu-id="65811-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="65811-109">否則，它會是專案的簡述，而您需要手動輸入專案元件的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="65811-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="65811-110">**報價**</span><span class="sxs-lookup"><span data-stu-id="65811-110">**Quote**</span></span>   |      <span data-ttu-id="65811-111">當您將專案與報價建立關聯或從報價建立專案時，專案階段會設為 **報價**，且估計的開始和結束日期也會更新。</span><span class="sxs-lookup"><span data-stu-id="65811-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="65811-112">當專案處於報價階段時，報價上的詳細資料會顯示在 **專案** 頁面的 **銷售** 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="65811-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="65811-113">**計劃**</span><span class="sxs-lookup"><span data-stu-id="65811-113">**Plan**</span></span>   |                                     <span data-ttu-id="65811-114">當您的專案報價成交，且互動進度來到合約階段時，專案階段會更新為 **計劃**。</span><span class="sxs-lookup"><span data-stu-id="65811-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="65811-115">合約詳細資料會顯示在 **專案** 頁面的 **銷售** 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="65811-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="65811-116">**完成**</span><span class="sxs-lookup"><span data-stu-id="65811-116">**Complete**</span></span> |                    <span data-ttu-id="65811-117">當專案工作完成時，您可以將階段轉換成 **完成**。</span><span class="sxs-lookup"><span data-stu-id="65811-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="65811-118">專案階段設定為完成時，表示工作已 100% 完成，但專案仍未結案，以便記錄任何剩餘時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="65811-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="65811-119">**關閉**</span><span class="sxs-lookup"><span data-stu-id="65811-119">**Close**</span></span>   |           <span data-ttu-id="65811-120">當所有交易都已記錄在專案上，且不會再有任何需要記錄的項目時，您可以手動設定階段為 **結案**。</span><span class="sxs-lookup"><span data-stu-id="65811-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="65811-121">當專案設定為 **結案** 時，您就無法再於專案上記錄任何交易，且專案將變成唯讀。</span><span class="sxs-lookup"><span data-stu-id="65811-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="65811-122">若要追蹤專案狀態</span><span class="sxs-lookup"><span data-stu-id="65811-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="65811-123">移至 **Project Service > 專案**。</span><span class="sxs-lookup"><span data-stu-id="65811-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="65811-124">按一下您要處理的專案。</span><span class="sxs-lookup"><span data-stu-id="65811-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="65811-125">在橫跨畫面頂端的列中，選取專案名稱旁的向下箭頭，然後按一下 **專案追蹤**。</span><span class="sxs-lookup"><span data-stu-id="65811-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="65811-126">在工作清單上方的下拉式清單中，選取 **努力追蹤** 或 **成本追蹤**。</span><span class="sxs-lookup"><span data-stu-id="65811-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="65811-127">按兩下任何工作進行編輯。</span><span class="sxs-lookup"><span data-stu-id="65811-127">Double-click any task to edit it.</span></span> <span data-ttu-id="65811-128">您也可以移動或調整甘特圖表中各列的大小，以變更工作的時間和進度。</span><span class="sxs-lookup"><span data-stu-id="65811-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="65811-129">請參閱</span><span class="sxs-lookup"><span data-stu-id="65811-129">See Also</span></span>  
 [<span data-ttu-id="65811-130">專案經理指南</span><span class="sxs-lookup"><span data-stu-id="65811-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]