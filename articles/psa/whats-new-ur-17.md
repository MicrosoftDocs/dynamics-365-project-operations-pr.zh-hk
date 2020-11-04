---
title: Project Service Automation V3 更新版本 17 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 17 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087456"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="48630-103">Project Service Automation 更新版本 17 V3</span><span class="sxs-lookup"><span data-stu-id="48630-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="48630-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="48630-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="48630-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="48630-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="48630-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="48630-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="48630-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="48630-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="48630-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="48630-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="48630-109">本主題列出 PSA V3 更新版本 17 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="48630-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="48630-110">此版本的組建編號為 V3.10.6.34，已於 2020 年 3 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="48630-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="48630-111">更新版本 17</span><span class="sxs-lookup"><span data-stu-id="48630-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="48630-112">錯誤修正</span><span class="sxs-lookup"><span data-stu-id="48630-112">Bug fixes</span></span>

<span data-ttu-id="48630-113">**一般**</span><span class="sxs-lookup"><span data-stu-id="48630-113">**General**</span></span>

- <span data-ttu-id="48630-114">已修正：更新 Project Service Automation 以實行團隊成員授權 (專案資源中心將會包含團隊成員服務方案中繼資料 3.x)</span><span class="sxs-lookup"><span data-stu-id="48630-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="48630-115">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="48630-115">**Time and Expense**</span></span>

- <span data-ttu-id="48630-116">已修正：無法將費用估計值從非零價格變更為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="48630-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="48630-117">變更會遭忽略。</span><span class="sxs-lookup"><span data-stu-id="48630-117">The change is ignored.</span></span>

<span data-ttu-id="48630-118">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="48630-118">**Project Management**</span></span>

- <span data-ttu-id="48630-119">已修正：已新增對團隊成員職位名稱的 null 值檢查。</span><span class="sxs-lookup"><span data-stu-id="48630-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="48630-120">已修正： **msdyn_resourceassignment** 實體上的 **msdyn_userresourceid** 欄位已被取代。</span><span class="sxs-lookup"><span data-stu-id="48630-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="48630-121">已修正：從 2.x 到 3.x 的升級現在會在工作指派上處理空白努力分佈。</span><span class="sxs-lookup"><span data-stu-id="48630-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="48630-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="48630-122">**Sales**</span></span>

- <span data-ttu-id="48630-123">已修正： **Invoice.PreValidateInvoiceUpdate** 現在會正確處理重新指派記錄負責人。</span><span class="sxs-lookup"><span data-stu-id="48630-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="48630-124">已修正：交易類別為 **時間** 時， **UnitGroup** 對所有實體 (包括 **QuoteLineDetails** 、 **JournalLine** 、 **InvoiceLineDetail** 和 **ContractLineDetails** ) 都是不可編輯的。</span><span class="sxs-lookup"><span data-stu-id="48630-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="48630-125">不過， **單位** 只有對 **JournalLine** 和 **InvoiceLineDetails** 才是不可編輯。</span><span class="sxs-lookup"><span data-stu-id="48630-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


