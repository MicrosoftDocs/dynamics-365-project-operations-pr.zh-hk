---
title: Project Service Automation V3 更新版本 29 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 29 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499698"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="a4b07-103">Project Service Automation V3 更新版本 29 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="a4b07-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a4b07-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="a4b07-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a4b07-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="a4b07-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a4b07-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="a4b07-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a4b07-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="a4b07-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a4b07-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="a4b07-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a4b07-109">本主題列出 Project Service Automation V3 更新版本 29 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="a4b07-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="a4b07-110">此版本的組建編號為 V3.10.45.98，已 2021 年 2 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="a4b07-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="a4b07-111">更新版本 29</span><span class="sxs-lookup"><span data-stu-id="a4b07-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a4b07-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="a4b07-112">Bug fixes</span></span>

<span data-ttu-id="a4b07-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="a4b07-113">**Time and Expense**</span></span>

<span data-ttu-id="a4b07-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="a4b07-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a4b07-115">使用者在時間項目網格中看不到非工作日上記錄的工作時數。</span><span class="sxs-lookup"><span data-stu-id="a4b07-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="a4b07-116">可以在網格上編輯已核准的費用項目。</span><span class="sxs-lookup"><span data-stu-id="a4b07-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="a4b07-117">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="a4b07-117">**Project Management**</span></span>

<span data-ttu-id="a4b07-118">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="a4b07-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a4b07-119">找不到用於確保資源指派投入時數不可為負數的驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="a4b07-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="a4b07-120">自訂動作 **AssignResourcesForTask** 會更新所有欄位，而不是只更新已變更的欄位。</span><span class="sxs-lookup"><span data-stu-id="a4b07-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="a4b07-121">在使用已於 **CreateProject** 事件註冊之外掛程式或工作流程的環境中複製專案時，如果 **CopyWBSToProject** 失敗，則不會更新 **msdyn_bulkgenerationstatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a4b07-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="a4b07-122">展開專案行事曆時，工作日不會依遞增順序排序，造成部分專案工作更新失敗。</span><span class="sxs-lookup"><span data-stu-id="a4b07-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="a4b07-123">變更現有專案的專案經理時會觸發組織單位的設定預設值邏輯。</span><span class="sxs-lookup"><span data-stu-id="a4b07-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="a4b07-124">**銷售**</span><span class="sxs-lookup"><span data-stu-id="a4b07-124">**Sales**</span></span>

<span data-ttu-id="a4b07-125">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="a4b07-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="a4b07-126">沒有任何合約服務內容存在時，**合約** 頁面上的 **合約績效** 索引標籤會在初始化期間以無訊息方式失敗。</span><span class="sxs-lookup"><span data-stu-id="a4b07-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
