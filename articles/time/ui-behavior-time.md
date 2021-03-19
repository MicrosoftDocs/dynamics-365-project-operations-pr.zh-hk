---
title: 時間項目 UI 行為
description: 本主題提供有關時間項目 UI 行為的資訊。
author: stsporen
manager: AnnBe
ms.date: 03/03/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b552266eddc4efc1b41fc500d157239388ad219b
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499641"
---
# <a name="time-entry-ui-behavior"></a><span data-ttu-id="f40c3-103">時間項目 UI 行為</span><span class="sxs-lookup"><span data-stu-id="f40c3-103">Time entry UI behavior</span></span>

<span data-ttu-id="f40c3-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f40c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f40c3-105">**每週時間項目** 網格是自訂控制項，其中有 **維度** 和 **期間** 這兩個主要區段。</span><span class="sxs-lookup"><span data-stu-id="f40c3-105">The **Weekly time entry** grid is a custom control that has two main sections, **Dimensions** and **Duration**.</span></span>

## <a name="keyboard-shortcuts"></a><span data-ttu-id="f40c3-106">鍵盤快速鍵</span><span class="sxs-lookup"><span data-stu-id="f40c3-106">Keyboard shortcuts</span></span>
| <span data-ttu-id="f40c3-107">動作​​</span><span class="sxs-lookup"><span data-stu-id="f40c3-107">Action</span></span>        | <span data-ttu-id="f40c3-108">捷徑</span><span class="sxs-lookup"><span data-stu-id="f40c3-108">Shortcut</span></span>                  |
|------------   |------------------------   |
| <span data-ttu-id="f40c3-109">新的</span><span class="sxs-lookup"><span data-stu-id="f40c3-109">New</span></span>           | <span data-ttu-id="f40c3-110">Alt + Shift + n</span><span class="sxs-lookup"><span data-stu-id="f40c3-110">Alt + Shift + n</span></span>           |
| <span data-ttu-id="f40c3-111">複製列</span><span class="sxs-lookup"><span data-stu-id="f40c3-111">Copy row</span></span>      | <span data-ttu-id="f40c3-112">Alt + Shift + c</span><span class="sxs-lookup"><span data-stu-id="f40c3-112">Alt + Shift + c</span></span>           |
| <span data-ttu-id="f40c3-113">編輯項目</span><span class="sxs-lookup"><span data-stu-id="f40c3-113">Edit 3ntry</span></span>    | <span data-ttu-id="f40c3-114">Alt + Shift + e</span><span class="sxs-lookup"><span data-stu-id="f40c3-114">Alt + Shift + e</span></span>           |
| <span data-ttu-id="f40c3-115">編輯列</span><span class="sxs-lookup"><span data-stu-id="f40c3-115">Edit row</span></span>      | <span data-ttu-id="f40c3-116">Alt + Shift + Ctrl + e</span><span class="sxs-lookup"><span data-stu-id="f40c3-116">Alt + Shift + Ctrl + e</span></span>    |
| <span data-ttu-id="f40c3-117">開啟項目</span><span class="sxs-lookup"><span data-stu-id="f40c3-117">Open 3ntry</span></span>    | <span data-ttu-id="f40c3-118">Alt + Shift + o</span><span class="sxs-lookup"><span data-stu-id="f40c3-118">Alt + Shift + o</span></span>           |
| <span data-ttu-id="f40c3-119">提交</span><span class="sxs-lookup"><span data-stu-id="f40c3-119">Submit</span></span>        | <span data-ttu-id="f40c3-120">Alt + Shift + s</span><span class="sxs-lookup"><span data-stu-id="f40c3-120">Alt + Shift + s</span></span>           |
| <span data-ttu-id="f40c3-121">回收</span><span class="sxs-lookup"><span data-stu-id="f40c3-121">Recall</span></span>        | <span data-ttu-id="f40c3-122">Alt + Shift + r</span><span class="sxs-lookup"><span data-stu-id="f40c3-122">Alt + Shift + r</span></span>           |
| <span data-ttu-id="f40c3-123">Delete</span><span class="sxs-lookup"><span data-stu-id="f40c3-123">Delete</span></span>        | <span data-ttu-id="f40c3-124">Alt + Shift + d</span><span class="sxs-lookup"><span data-stu-id="f40c3-124">Alt + Shift + d</span></span>           |
| <span data-ttu-id="f40c3-125">複製週次</span><span class="sxs-lookup"><span data-stu-id="f40c3-125">Copy week</span></span>     | <span data-ttu-id="f40c3-126">Alt + Shift + w</span><span class="sxs-lookup"><span data-stu-id="f40c3-126">Alt + Shift + w</span></span>           |

## <a name="dimensions"></a><span data-ttu-id="f40c3-127">維度</span><span class="sxs-lookup"><span data-stu-id="f40c3-127">Dimensions</span></span>
<span data-ttu-id="f40c3-128">**維度** 區段會顯示可據以輸入時間的維度。</span><span class="sxs-lookup"><span data-stu-id="f40c3-128">The **Dimensions** section shows the dimensions that time can be entered against.</span></span> <span data-ttu-id="f40c3-129">下列維度是現成支援的可用維度：</span><span class="sxs-lookup"><span data-stu-id="f40c3-129">The following dimensions are supported out-of-the-box:</span></span>

  - <span data-ttu-id="f40c3-130">Project</span><span class="sxs-lookup"><span data-stu-id="f40c3-130">Project</span></span>
  - <span data-ttu-id="f40c3-131">專案工作</span><span class="sxs-lookup"><span data-stu-id="f40c3-131">Project Task</span></span>
  - <span data-ttu-id="f40c3-132">角色</span><span class="sxs-lookup"><span data-stu-id="f40c3-132">Role</span></span>
  - <span data-ttu-id="f40c3-133">鍵入</span><span class="sxs-lookup"><span data-stu-id="f40c3-133">Type</span></span>
  - <span data-ttu-id="f40c3-134">項目狀態</span><span class="sxs-lookup"><span data-stu-id="f40c3-134">Entry Status</span></span>

<span data-ttu-id="f40c3-135">**維度** 區段不允許直接編輯。</span><span class="sxs-lookup"><span data-stu-id="f40c3-135">The **Dimensions** section doesn't allow inline editing.</span></span> <span data-ttu-id="f40c3-136">此區段是由可讓自訂欄位新增至每週時間輸入網格的檢視表所支援。</span><span class="sxs-lookup"><span data-stu-id="f40c3-136">This section is backed by a view that enables custom fields to be added to the weekly time entry grid.</span></span>

## <a name="duration"></a><span data-ttu-id="f40c3-137">持續時間</span><span class="sxs-lookup"><span data-stu-id="f40c3-137">Duration</span></span>
<span data-ttu-id="f40c3-138">[期間] 區段以欄標題顯示一週中哪幾天。</span><span class="sxs-lookup"><span data-stu-id="f40c3-138">The Duration section shows the days of the week as column headers.</span></span> <span data-ttu-id="f40c3-139">此區段允許直接編輯。</span><span class="sxs-lookup"><span data-stu-id="f40c3-139">This section allows inline editing.</span></span> <span data-ttu-id="f40c3-140">建立包含適當維度的時間項目列之後，使用者就可以快速輸入他們在這些維度上花費的時間量。</span><span class="sxs-lookup"><span data-stu-id="f40c3-140">After a time entry row is created with the appropriate dimensions, users can quickly enter the amount of time that they spent on those dimensions.</span></span>

## <a name="create-a-new-time-entry"></a><span data-ttu-id="f40c3-141">建立新的時間項目</span><span class="sxs-lookup"><span data-stu-id="f40c3-141">Create a new time entry</span></span>

1. <span data-ttu-id="f40c3-142">在時間項目網格中，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-142">In the time entry grid, select **New**.</span></span> 
2. <span data-ttu-id="f40c3-143">在 **時間項目快速建立** 對話方塊中，選取時間項目日期。</span><span class="sxs-lookup"><span data-stu-id="f40c3-143">In the **Time Entry Quick Create** dialog box, select the time entry date.</span></span>
3. <span data-ttu-id="f40c3-144">輸入 **專案**、**專案工作**、**角色** 和 **期間** 維度的資料。</span><span class="sxs-lookup"><span data-stu-id="f40c3-144">Enter data for the **Project**, **Project Task**, **Role**, and **Duration** dimensions.</span></span> <span data-ttu-id="f40c3-145">此資訊應藉由與數字一起鍵入 **h**、**m** 或 **d** 的方式，以分鐘、小時或天數來加入其中。</span><span class="sxs-lookup"><span data-stu-id="f40c3-145">This information should be added in minutes, hours, or days by typing **h**, **m**, or **d**, together with the number.</span></span> 
4. <span data-ttu-id="f40c3-146">輸入時間項目的描述以及任何可供外部共用的時間項目相關註解。</span><span class="sxs-lookup"><span data-stu-id="f40c3-146">Enter a description for the entry and any comments that can be shared externally regarding time entry.</span></span> 

<span data-ttu-id="f40c3-147">儲存項目時，輸入的值會顯示在 **維度** 區段中。</span><span class="sxs-lookup"><span data-stu-id="f40c3-147">When you save the entry, the entered values appear in the **Dimensions** section.</span></span> <span data-ttu-id="f40c3-148">在 **期間** 欄位中輸入的資訊會在建立時間項目的日期出現。</span><span class="sxs-lookup"><span data-stu-id="f40c3-148">The information entered in the **Duration** field appears on the date that the time entry was created for.</span></span>

<span data-ttu-id="f40c3-149">系統檢視表支援查詢欄位。</span><span class="sxs-lookup"><span data-stu-id="f40c3-149">Lookup fields are backed by system views.</span></span> <span data-ttu-id="f40c3-150">例如，使用者進入專案後，**專案工作** 欄位預設會設定為 **複製** 檢視表。</span><span class="sxs-lookup"><span data-stu-id="f40c3-150">For example, after a user enters a project, the **Project Task** field is set to the **Copy** view by default.</span></span> <span data-ttu-id="f40c3-151">若要建立未指派給使用者之工作的時間項目，請在查詢對話方塊中選取 **變更檢視表**，然後選取 **所有使用中專案工作** 檢視表。</span><span class="sxs-lookup"><span data-stu-id="f40c3-151">To create time entries for tasks that aren't assigned to a user, select **Change View** in the lookup dialog box, and then select the **All Active Project Tasks** view.</span></span>

## <a name="edit-a-time-entry"></a><span data-ttu-id="f40c3-152">編輯時間項目</span><span class="sxs-lookup"><span data-stu-id="f40c3-152">Edit a time entry</span></span> 
<span data-ttu-id="f40c3-153">時間項目頁面上某些欄位的詳細資料 (例如 **描述** 和 **外部註解**) 不會顯示在每週時間輸入網格中。</span><span class="sxs-lookup"><span data-stu-id="f40c3-153">Details from some fields on the time entry page, such as **Description** and **External Comments**, aren't shown in the weekly time entry grid.</span></span> <span data-ttu-id="f40c3-154">相反的，會有一個小三角形指標出現在含有這些額外詳細資料的 **期間** 儲存格中。</span><span class="sxs-lookup"><span data-stu-id="f40c3-154">Instead, a small triangular indicator appears in the **Duration** cells that have these additional details.</span></span> 

1. <span data-ttu-id="f40c3-155">若要編輯時間項目，請選取您要在時間項目中更新的儲存格。</span><span class="sxs-lookup"><span data-stu-id="f40c3-155">To edit a time entry, select the cell you want to update in the time entry.</span></span>
2. <span data-ttu-id="f40c3-156">選取 **編輯詳細資料** 以更新 **時間項目主要表單** 窗格中的資料。</span><span class="sxs-lookup"><span data-stu-id="f40c3-156">Select **Edit Details** to update the data in the **Time Entry Mainform** pane.</span></span> 

## <a name="copy-a-time-entry-row"></a><span data-ttu-id="f40c3-157">複製時間項目列</span><span class="sxs-lookup"><span data-stu-id="f40c3-157">Copy a time entry row</span></span>
<span data-ttu-id="f40c3-158">建立此列之後，您可以選取 **複製列**，將整列複製到新的一列。</span><span class="sxs-lookup"><span data-stu-id="f40c3-158">After the row has been created, you can select **Copy Row** to copy the whole row to a new row.</span></span> <span data-ttu-id="f40c3-159">以這種方式複製一列時，也會複製維度和期間。</span><span class="sxs-lookup"><span data-stu-id="f40c3-159">When a row is copied in this way, dimensions and durations are also copied.</span></span> <span data-ttu-id="f40c3-160">您也可以選取 **編輯列**，更新維度值並在 **期間** 區段中編輯期間。</span><span class="sxs-lookup"><span data-stu-id="f40c3-160">You can also select **Edit Row** to update dimension values and durations in the **Duration** section.</span></span>

## <a name="open-a-time-entry-behavior"></a><span data-ttu-id="f40c3-161">開啟時間項目行為</span><span class="sxs-lookup"><span data-stu-id="f40c3-161">Open a time entry behavior</span></span>
<span data-ttu-id="f40c3-162">為了在最顯著的欄位中支援最佳且快速輸入，每週時間項目網格會顯示所選維度及時間期間的子集。</span><span class="sxs-lookup"><span data-stu-id="f40c3-162">To support optimal and quick entry in the most prominent fields, the weekly time entry grid shows a subset of selected dimensions and time durations.</span></span> <span data-ttu-id="f40c3-163">若要檢視單一時間項目的所有詳細資料，請在 **編輯專案** 下選取 **開啟**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-163">To view all the details of a single time entry, under **Edit Entry**, select **Open**.</span></span>

## <a name="submit-a-time-entry"></a><span data-ttu-id="f40c3-164">送出時間項目</span><span class="sxs-lookup"><span data-stu-id="f40c3-164">Submit a time entry</span></span>
<span data-ttu-id="f40c3-165">您可以送出單一時間項目或一組時間項目，方法是選取儲存格區塊或整個時間項目列，然後選取 **送出**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-165">You can submit a single time entry or a group of time entries by selecting a block of cells or a whole time entry row, and then selecting **Submit**.</span></span> <span data-ttu-id="f40c3-166">送出的時間項目會在核准者的 **核准** 頁面上顯示為等待核准。</span><span class="sxs-lookup"><span data-stu-id="f40c3-166">Submitted time entries appear as entries that are pending approval on the approvers' **Approval** page.</span></span> <span data-ttu-id="f40c3-167">成功送出時間項目之後，就無法加以編輯。</span><span class="sxs-lookup"><span data-stu-id="f40c3-167">After time entries are successfully submitted, they can't be edited.</span></span>

## <a name="recall-a-time-entry"></a><span data-ttu-id="f40c3-168">回收時間項目</span><span class="sxs-lookup"><span data-stu-id="f40c3-168">Recall a time entry</span></span>
<span data-ttu-id="f40c3-169">您可以回收已送出的時間項目。</span><span class="sxs-lookup"><span data-stu-id="f40c3-169">You can recall time entries that you've submitted.</span></span> <span data-ttu-id="f40c3-170">您可以回收單一時間項目、時間項目區塊或整列時間項目。</span><span class="sxs-lookup"><span data-stu-id="f40c3-170">You can recall a single time entry, a block of time entries, or a whole row of time entries.</span></span> <span data-ttu-id="f40c3-171">可以編輯已回收的時間項目。</span><span class="sxs-lookup"><span data-stu-id="f40c3-171">Recalled time entries can be edited.</span></span>

## <a name="time-entry-status"></a><span data-ttu-id="f40c3-172">時間項目狀態</span><span class="sxs-lookup"><span data-stu-id="f40c3-172">Time entry status</span></span>

- <span data-ttu-id="f40c3-173">**草稿**：系統會自動為新的時間項目指派 **草稿** 狀態。</span><span class="sxs-lookup"><span data-stu-id="f40c3-173">**Draft**: New time entries are automatically assigned a status of **Draft**.</span></span> <span data-ttu-id="f40c3-174">只有狀態為 **草稿** 的時間項目可以被刪除。</span><span class="sxs-lookup"><span data-stu-id="f40c3-174">Only time entries that have a status of **Draft** can be deleted.</span></span>
- <span data-ttu-id="f40c3-175">**已提交**：提交時間項目時，狀態會更新為 **已提交**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-175">**Submitted**: When a time entry is submitted, the status is updated to **Submitted**.</span></span> 
- <span data-ttu-id="f40c3-176">**已核准**：提交的時間項目獲核准時，狀態會更新為 **已核准**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-176">**Approved**: When a submitted time entry is approved, the status is updated to **Approved**.</span></span> 
- <span data-ttu-id="f40c3-177">**已退回**：如果時間項目遭拒絕，狀態會更新為 **已退回**，而項目會變成可供更正並重新提交。</span><span class="sxs-lookup"><span data-stu-id="f40c3-177">**Returned**: If a time entry is rejected, the status is updated to **Returned**, and the entry becomes available for correction and resubmission.</span></span> 

## <a name="view-rejection-comments"></a><span data-ttu-id="f40c3-178">檢視拒絕註解</span><span class="sxs-lookup"><span data-stu-id="f40c3-178">View rejection comments</span></span>
<span data-ttu-id="f40c3-179">核准者拒絕時間項目時，該核准者可能會加入註解，幫助資源了解拒絕原因。</span><span class="sxs-lookup"><span data-stu-id="f40c3-179">When a time entry is rejected by an approver, the approver might add comments to help the resource understand the reason for the rejection.</span></span> <span data-ttu-id="f40c3-180">若要檢視時間項目的拒絕註解，請選取 **開啟專案**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-180">To view the rejection comments for a time entry, select **Open entry**.</span></span> <span data-ttu-id="f40c3-181">這些拒絕註解會顯示在時間表中。</span><span class="sxs-lookup"><span data-stu-id="f40c3-181">The rejection comments will be shown in the timeline.</span></span> <span data-ttu-id="f40c3-182">使用者可以在重新提交此項目之前，先回應拒絕註解。</span><span class="sxs-lookup"><span data-stu-id="f40c3-182">The user can respond to the rejection comments before they resubmit the entry.</span></span>

## <a name="copy-week"></a><span data-ttu-id="f40c3-183">複製週次</span><span class="sxs-lookup"><span data-stu-id="f40c3-183">Copy week</span></span>
<span data-ttu-id="f40c3-184">建立幾個時間項目之後，使用者可以同時建立多個時間項目。</span><span class="sxs-lookup"><span data-stu-id="f40c3-184">After a few time entries have been created, users can create multiple time entries at the same time.</span></span>

1. <span data-ttu-id="f40c3-185">在 **時間項目** 表單中，選取 **複製週次** 以大量建立其他時間項目。</span><span class="sxs-lookup"><span data-stu-id="f40c3-185">In the **Time Entries** form, select **Copy Week** to bulk-create additional time entries.</span></span> 
2. <span data-ttu-id="f40c3-186">在 **複製** 對話方塊的 **開始期間** 區段中，使用 **開始日期** 和 **結束日期** 欄位來定義要從中複製時間項目的日期範圍。</span><span class="sxs-lookup"><span data-stu-id="f40c3-186">In the **Copy** dialog box, in the **From period** section, use the **Start Date** and **End Date** fields to define the date range to copy time entries from.</span></span> 
3. <span data-ttu-id="f40c3-187">在 **結束期間** 區段的 **開始日期** 欄位中，指定建立時間項目的日期。</span><span class="sxs-lookup"><span data-stu-id="f40c3-187">In the **To Period** section, in the **Start Date** field, specify the date to create time entries for.</span></span> 
4. <span data-ttu-id="f40c3-188">請選取 **複製**。</span><span class="sxs-lookup"><span data-stu-id="f40c3-188">Select **Copy**.</span></span> <span data-ttu-id="f40c3-189">對於 **結束期間** 的指定日期，會建立 **開始期間** 中對應星期幾的時間項目複本。</span><span class="sxs-lookup"><span data-stu-id="f40c3-189">For the specified date in the **To period**, a copy of the time entries for the corresponding day of the week in the **From period** is created.</span></span> <span data-ttu-id="f40c3-190">例如，將上週星期一的時間項目複製到指定為 **結束期間** 的週的星期一。</span><span class="sxs-lookup"><span data-stu-id="f40c3-190">For example, Monday's time entry from last week is copied into Monday of the week that is specified as the **To period**.</span></span>

## <a name="import"></a><span data-ttu-id="f40c3-191">匯入</span><span class="sxs-lookup"><span data-stu-id="f40c3-191">Import</span></span>
<span data-ttu-id="f40c3-192">您可以使用相同的基本程序，從預約、指派和交換中匯入。</span><span class="sxs-lookup"><span data-stu-id="f40c3-192">The same basic process is used to import from bookings, assignments, and exchanges.</span></span> <span data-ttu-id="f40c3-193">您可以指定匯入預約的日期範圍，然後明確選取應複製到草稿時間項目中的預約。</span><span class="sxs-lookup"><span data-stu-id="f40c3-193">You can specify the date range that bookings are imported from and then explicitly select the bookings that should be copied into draft time entries.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
