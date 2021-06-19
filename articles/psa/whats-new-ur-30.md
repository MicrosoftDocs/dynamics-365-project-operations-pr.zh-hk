---
title: Project Service Automation V3 更新版本 30 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 30 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010453"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="0b142-103">Project Service Automation V3 更新版本 30 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="0b142-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0b142-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="0b142-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0b142-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="0b142-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0b142-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="0b142-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0b142-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="0b142-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0b142-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution.md)。</span><span class="sxs-lookup"><span data-stu-id="0b142-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="0b142-109">本主題列出 Project Service Automation V3 更新版本 30 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="0b142-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="0b142-110">此版本的組建編號是 V3.10.51.61，已於 2021 年 4 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="0b142-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="0b142-111">更新版本 30</span><span class="sxs-lookup"><span data-stu-id="0b142-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0b142-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="0b142-112">Bug fixes</span></span>

<span data-ttu-id="0b142-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="0b142-113">**Time and Expense**</span></span>

<span data-ttu-id="0b142-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="0b142-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="0b142-115">在 **快速建立** 頁面上建立並儲存時間項目時，如果 **角色** 欄位已移除，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b142-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="0b142-116">時間項目篩選套用錯誤的篩選運算子。</span><span class="sxs-lookup"><span data-stu-id="0b142-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="0b142-117">選取時間項目控制項上的 **複製週次** 時，未自動顯示複製的工時表。</span><span class="sxs-lookup"><span data-stu-id="0b142-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="0b142-118">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="0b142-118">**Resource Management**</span></span>

<span data-ttu-id="0b142-119">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="0b142-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="0b142-120">延長預約時，指派給已確認預約的預約狀態不正確。</span><span class="sxs-lookup"><span data-stu-id="0b142-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="0b142-121">延長預約會採用預約設定中繼資料中定義為 **已認可** 的預約狀態。</span><span class="sxs-lookup"><span data-stu-id="0b142-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="0b142-122">未指定有效的預約狀態時，錯誤訊息未正確當地語系化。</span><span class="sxs-lookup"><span data-stu-id="0b142-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="0b142-123">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="0b142-123">**Project Management**</span></span>

<span data-ttu-id="0b142-124">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="0b142-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="0b142-125">專案不可以是使用一種貨幣所建立，卻又包含使用其他貨幣的相關工作。</span><span class="sxs-lookup"><span data-stu-id="0b142-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="0b142-126">**銷售**</span><span class="sxs-lookup"><span data-stu-id="0b142-126">**Sales**</span></span>

<span data-ttu-id="0b142-127">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="0b142-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="0b142-128">複製價目表時，未更新價格。</span><span class="sxs-lookup"><span data-stu-id="0b142-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="0b142-129">當成本明細具有來源的值時，以成交關閉報價會失敗。</span><span class="sxs-lookup"><span data-stu-id="0b142-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="0b142-130">在 **專案工作** 實體上，**估計成本** 已重新命名為 **規劃成本 (基準貨幣)**。</span><span class="sxs-lookup"><span data-stu-id="0b142-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="0b142-131">建立或刪除發票時，產生 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="0b142-131">A null reference exception is generated when invoices are created or deleted.</span></span>
