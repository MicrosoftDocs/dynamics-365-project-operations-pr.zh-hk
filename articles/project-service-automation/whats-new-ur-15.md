---
title: Project Service Automation V3 更新版本 15 的新功能
description: 本主題提供 Project Service Automation V3 更新版本 15 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757263"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="3b0fd-103">Project Service Automation V3 更新版本 15 的新功能</span><span class="sxs-lookup"><span data-stu-id="3b0fd-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="3b0fd-104">我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3b0fd-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3b0fd-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3b0fd-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3b0fd-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3b0fd-109">本主題列出 PSA V3 更新版本 15 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="3b0fd-110">此版本的組建編號為 V3.10.5.28，已於 2020 年 1 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="3b0fd-111">更新版本 15</span><span class="sxs-lookup"><span data-stu-id="3b0fd-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="3b0fd-112">增強功能</span><span class="sxs-lookup"><span data-stu-id="3b0fd-112">Enhancements</span></span>

- <span data-ttu-id="3b0fd-113">專案管理</span><span class="sxs-lookup"><span data-stu-id="3b0fd-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3b0fd-114">錯誤修正</span><span class="sxs-lookup"><span data-stu-id="3b0fd-114">Bug fixes</span></span>

- <span data-ttu-id="3b0fd-115">時間和費用</span><span class="sxs-lookup"><span data-stu-id="3b0fd-115">Time and Expense</span></span>

  - <span data-ttu-id="3b0fd-116">已修正：在協調檢視表中新增載入時錯誤處理功能。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="3b0fd-117">已修正：專案資源中心：重新命名**金額**以減少模稜兩可的情況。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="3b0fd-118">已修正：調整**複製時間項目欄**檢視表以包含類型。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="3b0fd-119">已修正：使用小數點編輯網格檢視表中的時間項目期間會導致部分數字發生不明的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="3b0fd-120">專案管理</span><span class="sxs-lookup"><span data-stu-id="3b0fd-120">Project Management</span></span>

  - <span data-ttu-id="3b0fd-121">已修正：**在追蹤檢視表中使用**的下拉式功能表現在會根據選項的寬度展開。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="3b0fd-122">已修正：管理 +13 時區的專案時，工作計算可能會顯示不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="3b0fd-123">已修正：使用 24 小時制行事曆時，**團隊成員結束時間**已更正。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="3b0fd-124">已修正：已在 **msdyn_project** 主要表單中重新啟用 **BPF**。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="3b0fd-125">已修正：指派計算不再忽略一天。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="3b0fd-126">已修正：已在使用者與專案之間的時區不同時，將新的通知橫幅加入至專案表單。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="3b0fd-127">Sales</span><span class="sxs-lookup"><span data-stu-id="3b0fd-127">Sales</span></span>

  - <span data-ttu-id="3b0fd-128">已修正：費用估計值類別查詢可以用來篩選重復資料。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="3b0fd-129">已修正：**PluginDomain.ExecuteInTryCatchBlock(..)** 中的程式碼不再隱藏例外狀況的來源。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="3b0fd-130">已修正：當有 1000 個以上的專案時，不再於**報價明細**表單中的**專案查詢**中收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="3b0fd-131">已修正：人力估計值及費用估計值的**估計值**網格現在會顯示正確的貨幣符號。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="3b0fd-132">已修正：組織將 PSA 從更新版本 14 更新為更新版本 15 之後，**排程**索引標籤不再於**專案**表單上顯示為空白。</span><span class="sxs-lookup"><span data-stu-id="3b0fd-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
