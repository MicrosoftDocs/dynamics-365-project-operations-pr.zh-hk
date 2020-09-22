---
title: Project Service Automation V3 更新版本 14 的新功能
description: 本主題提供 Project Service Automation V3 更新版本 14 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757264"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="6e00f-103">Project Service Automation V3 更新版本 14 的新功能</span><span class="sxs-lookup"><span data-stu-id="6e00f-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="6e00f-104">我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="6e00f-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6e00f-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="6e00f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6e00f-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="6e00f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6e00f-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="6e00f-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6e00f-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="6e00f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6e00f-109">本主題列出 PSA V3 更新版本 14 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="6e00f-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="6e00f-110">這個版本的組建編號為 V3.10.4.21，依照下列排程提供：</span><span class="sxs-lookup"><span data-stu-id="6e00f-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="6e00f-111">**正式運作 (自我更新)：** 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6e00f-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="6e00f-112">**自動更新：** 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6e00f-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="6e00f-113">更新版本 14</span><span class="sxs-lookup"><span data-stu-id="6e00f-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="6e00f-114">增強功能</span><span class="sxs-lookup"><span data-stu-id="6e00f-114">Enhancements</span></span>

- <span data-ttu-id="6e00f-115">Sales</span><span class="sxs-lookup"><span data-stu-id="6e00f-115">Sales</span></span>

     - <span data-ttu-id="6e00f-116">當報價更新為**以成交關閉**時，會將**報價明細詳細資料**中的自訂欄位值複製到**專案合約服務內容詳細資料**。</span><span class="sxs-lookup"><span data-stu-id="6e00f-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="6e00f-117">確認的專案可以是**以未成交關閉**。</span><span class="sxs-lookup"><span data-stu-id="6e00f-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="6e00f-118">資源管理</span><span class="sxs-lookup"><span data-stu-id="6e00f-118">Resource Management</span></span>

     - <span data-ttu-id="6e00f-119">延長預約時，系統會顯示確認對話方塊提示使用者，以摘要列出預約結果並提供 [維護預約] 的連結。</span><span class="sxs-lookup"><span data-stu-id="6e00f-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="6e00f-120">錯誤修正</span><span class="sxs-lookup"><span data-stu-id="6e00f-120">Bug fixes</span></span>

- <span data-ttu-id="6e00f-121">時間和費用</span><span class="sxs-lookup"><span data-stu-id="6e00f-121">Time and Expense</span></span>

     - <span data-ttu-id="6e00f-122">已修正：改善使用者沒有選取任何要更正的項目時的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="6e00f-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="6e00f-123">資源管理</span><span class="sxs-lookup"><span data-stu-id="6e00f-123">Resource Management</span></span>

     - <span data-ttu-id="6e00f-124">已修正：預約資源多次會溢過可預約資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e00f-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="6e00f-125">Sales</span><span class="sxs-lookup"><span data-stu-id="6e00f-125">Sales</span></span>

     - <span data-ttu-id="6e00f-126">已修正：在使用者另外輸入了專案費用估計值的成本價之前，不會計算總銷售價格。</span><span class="sxs-lookup"><span data-stu-id="6e00f-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="6e00f-127">已修正：如果相關聯的專案合約未處於**草稿**狀態時，以**成交**驗證報價會失敗。</span><span class="sxs-lookup"><span data-stu-id="6e00f-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

