---
title: 專案時間項目行動工作區
description: 本主題提供有關專案時間項目行動工作區的資訊。 此工作區可讓使用者使用行動裝置來輸入和儲存專案的時間。
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288901"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="5126a-104">專案時間項目行動工作區</span><span class="sxs-lookup"><span data-stu-id="5126a-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5126a-105">本主題提供有關 **專案時間項目** 行動工作區的資訊。</span><span class="sxs-lookup"><span data-stu-id="5126a-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="5126a-106">此工作區可讓使用者使用行動裝置來輸入和儲存專案的時間。</span><span class="sxs-lookup"><span data-stu-id="5126a-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="5126a-107">此行動工作區旨在與 Dynamics 365 Unified Ops 行動應用程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5126a-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="5126a-108">概觀</span><span class="sxs-lookup"><span data-stu-id="5126a-108">Overview</span></span>
<span data-ttu-id="5126a-109">做為日常工作的一部分，專案資源經常是在現場或差旅途中。</span><span class="sxs-lookup"><span data-stu-id="5126a-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="5126a-110">**專案時間項目** 行動工作區可讓使用者在他們選擇的行動裝置上，針對專案輸入其計費或非計費時間。</span><span class="sxs-lookup"><span data-stu-id="5126a-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="5126a-111">因此，專案資源可以隨時隨地記錄時間項目。</span><span class="sxs-lookup"><span data-stu-id="5126a-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="5126a-112">他們也可以檢視已記錄的時間項目。</span><span class="sxs-lookup"><span data-stu-id="5126a-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="5126a-113">具體而言，在 **專案時間項目** 行動工作區中，使用者可以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="5126a-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="5126a-114">對任何選取的日期，輸入您花費在特定工作的小時數。</span><span class="sxs-lookup"><span data-stu-id="5126a-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="5126a-115">依專案名稱或客戶進行搜尋，尋找需要輸入時間的專案。</span><span class="sxs-lookup"><span data-stu-id="5126a-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="5126a-116">指定已花費時間的類別與活動。</span><span class="sxs-lookup"><span data-stu-id="5126a-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="5126a-117">針對專案記錄時間為計費或非計費。</span><span class="sxs-lookup"><span data-stu-id="5126a-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="5126a-118">選擇性輸入任何外部或內部意見。</span><span class="sxs-lookup"><span data-stu-id="5126a-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5126a-119">先決條件</span><span class="sxs-lookup"><span data-stu-id="5126a-119">Prerequisites</span></span>
<span data-ttu-id="5126a-120">視組織已部署的 Microsoft Dynamics 365 版本而定，先決條件會有所不同。</span><span class="sxs-lookup"><span data-stu-id="5126a-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="5126a-121">使用 Dynamics 365 Finance 時的先決條件</span><span class="sxs-lookup"><span data-stu-id="5126a-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="5126a-122">如果您的組織已部署 Finance，則系統系統管理員必須發佈 **專案時間項目** 行動工作區。</span><span class="sxs-lookup"><span data-stu-id="5126a-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="5126a-123">如需指示，請參閱[發佈行動工作區](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace)。</span><span class="sxs-lookup"><span data-stu-id="5126a-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="5126a-124">使用版本 1611 (含平台更新 3) 或更新版本時的先決條件</span><span class="sxs-lookup"><span data-stu-id="5126a-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="5126a-125">如果您的組織已部署版本 1611 (含平台更新 3) 或更新版本，則系統系統管理員必須完成下列先決條件。</span><span class="sxs-lookup"><span data-stu-id="5126a-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5126a-126">先決條件</span><span class="sxs-lookup"><span data-stu-id="5126a-126">Prerequisite</span></span></th>
<th><span data-ttu-id="5126a-127">角色</span><span class="sxs-lookup"><span data-stu-id="5126a-127">Role</span></span></th>
<th><span data-ttu-id="5126a-128">描述</span><span class="sxs-lookup"><span data-stu-id="5126a-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="5126a-129">實作 KB 4018050。</span><span class="sxs-lookup"><span data-stu-id="5126a-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="5126a-130">系統管理員</span><span class="sxs-lookup"><span data-stu-id="5126a-130">System administrator</span></span></td>
<td><span data-ttu-id="5126a-131">KB 4018050 是包含<strong>專案時間項目</strong>行動工作區的 X++ 更新或中繼資料 Hotfix。</span><span class="sxs-lookup"><span data-stu-id="5126a-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="5126a-132">若要實作 KB 4018050，您的系統系統管理員必須依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="5126a-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="5126a-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">從 Microsoft Dynamics Lifecycle Services (LCS) 下載中繼資料 Hotfix</a>。</span><span class="sxs-lookup"><span data-stu-id="5126a-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="5126a-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安裝中繼資料 Hotfix</a>。</span><span class="sxs-lookup"><span data-stu-id="5126a-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="5126a-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">建立的可部署套件</a> (內含<strong>ApplicationSuite</strong> 和 <strong>ProjectMobile</strong> 模型)，然後將可部署套件上傳至 LCS。</span><span class="sxs-lookup"><span data-stu-id="5126a-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="5126a-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">套用可部署套件</a>。</span><span class="sxs-lookup"><span data-stu-id="5126a-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5126a-137">發佈<strong>專案時間項目</strong>行動工作區。</span><span class="sxs-lookup"><span data-stu-id="5126a-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="5126a-138">系統管理員</span><span class="sxs-lookup"><span data-stu-id="5126a-138">System administrator</span></span></td>
<td><span data-ttu-id="5126a-139">請參閱<a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">發佈行動工作區</a>。</span><span class="sxs-lookup"><span data-stu-id="5126a-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="5126a-140">下載並安裝行動應用程式</span><span class="sxs-lookup"><span data-stu-id="5126a-140">Download and install the mobile app</span></span>

<span data-ttu-id="5126a-141">下載並安裝 Finance and Operations 行動應用程式：</span><span class="sxs-lookup"><span data-stu-id="5126a-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="5126a-142">適用於 Android 手機</span><span class="sxs-lookup"><span data-stu-id="5126a-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="5126a-143">適用於 iPhone</span><span class="sxs-lookup"><span data-stu-id="5126a-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="5126a-144">登入行動應用程式</span><span class="sxs-lookup"><span data-stu-id="5126a-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="5126a-145">在行動裝置上啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="5126a-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="5126a-146">輸入您的 Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="5126a-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="5126a-147">第一次登入時，系統會提示您輸入您的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="5126a-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="5126a-148">輸入您的認證。</span><span class="sxs-lookup"><span data-stu-id="5126a-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="5126a-149">登入後，會顯示您公司可用的工作區。</span><span class="sxs-lookup"><span data-stu-id="5126a-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="5126a-150">請注意，如果系統管理員稍後發佈了新的工作區，您就必須重新整理行動工作區的清單。</span><span class="sxs-lookup"><span data-stu-id="5126a-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="5126a-151">[![拖動以重新整理](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="5126a-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="5126a-152">使用專案時間項目行動工作區來輸入時間</span><span class="sxs-lookup"><span data-stu-id="5126a-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="5126a-153">在行動裝置上，選取 **專案時間項目** 工作區。</span><span class="sxs-lookup"><span data-stu-id="5126a-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="5126a-154">選取 **時間項目**。</span><span class="sxs-lookup"><span data-stu-id="5126a-154">Select **Time entry**.</span></span> <span data-ttu-id="5126a-155">隨即顯示本週的行事曆日期。</span><span class="sxs-lookup"><span data-stu-id="5126a-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="5126a-156">針對所選取的日期，選取 **動作** &gt; **新增輸入**。</span><span class="sxs-lookup"><span data-stu-id="5126a-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="5126a-157">輸入要記錄的小時數。</span><span class="sxs-lookup"><span data-stu-id="5126a-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="5126a-158">選取時間項目的專案。</span><span class="sxs-lookup"><span data-stu-id="5126a-158">Select the project for the time entry.</span></span> <span data-ttu-id="5126a-159">清單會顯示已載入至您的應用程式中供離線使用的專案。</span><span class="sxs-lookup"><span data-stu-id="5126a-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="5126a-160">預設會載入 50 個項目，但是開發人員可以變更此數目。</span><span class="sxs-lookup"><span data-stu-id="5126a-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="5126a-161">如需詳細資訊，請參閱[平台行動](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)。</span><span class="sxs-lookup"><span data-stu-id="5126a-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="5126a-162">如果您的專案不在清單中，請選取 **搜尋**。</span><span class="sxs-lookup"><span data-stu-id="5126a-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="5126a-163">依名稱搜尋，或切換為依專案名稱或客戶進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="5126a-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="5126a-164">選取類別。</span><span class="sxs-lookup"><span data-stu-id="5126a-164">Select a category.</span></span> <span data-ttu-id="5126a-165">清單會顯示已載入至您的應用程式中供離線使用的類別。</span><span class="sxs-lookup"><span data-stu-id="5126a-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="5126a-166">預設會載入 50 個項目，但是開發人員可以變更此數目。</span><span class="sxs-lookup"><span data-stu-id="5126a-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="5126a-167">如需詳細資訊，請參閱[平台行動](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)。</span><span class="sxs-lookup"><span data-stu-id="5126a-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="5126a-168">如果您的類別不在清單中，請選取 **搜尋**。</span><span class="sxs-lookup"><span data-stu-id="5126a-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="5126a-169">依類別搜尋，或切換為依類別名稱進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="5126a-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="5126a-170">選取活動。</span><span class="sxs-lookup"><span data-stu-id="5126a-170">Select an activity.</span></span> <span data-ttu-id="5126a-171">清單會顯示已載入至您的應用程式中供離線使用的活動。</span><span class="sxs-lookup"><span data-stu-id="5126a-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="5126a-172">預設會載入 50 個項目，但是開發人員可以變更此數目。</span><span class="sxs-lookup"><span data-stu-id="5126a-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="5126a-173">如需詳細資訊，請參閱[平台行動](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page)。</span><span class="sxs-lookup"><span data-stu-id="5126a-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="5126a-174">如果您的活動不在清單中，請選取 **搜尋**。</span><span class="sxs-lookup"><span data-stu-id="5126a-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="5126a-175">依活動編號搜尋，或切換為依目的進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="5126a-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="5126a-176">選取明細屬性。</span><span class="sxs-lookup"><span data-stu-id="5126a-176">Select the line property.</span></span>
12. <span data-ttu-id="5126a-177">選用：輸入任何外部及內部意見。</span><span class="sxs-lookup"><span data-stu-id="5126a-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="5126a-178">選取 **完成**。</span><span class="sxs-lookup"><span data-stu-id="5126a-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]