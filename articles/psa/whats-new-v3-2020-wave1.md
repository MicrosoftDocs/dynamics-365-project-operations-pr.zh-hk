---
title: Project Service Automation 3.x 版 2020 年第 1 段發行浪潮中新推出或已變更的功能
description: 本主題提供 Project Service Automation 版本 3 2020 年第 1 段發行浪潮中新推出或已變更功能的相關資訊。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150965"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="8a38d-103">Project Service Automation 版本 3 2020 年第 1 段發行浪潮中新推出或已變更的功能</span><span class="sxs-lookup"><span data-stu-id="8a38d-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8a38d-104">本主題著重說明移轉至最新發行的 Project Service Automation (PSA) 3.x 版 2020 年第 1 段發行浪潮時的重要升級考量。</span><span class="sxs-lookup"><span data-stu-id="8a38d-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="8a38d-105">時間項目</span><span class="sxs-lookup"><span data-stu-id="8a38d-105">Time entry</span></span>
<span data-ttu-id="8a38d-106">時間項目體驗已擴充，以便在更多客戶案例中提供可用於擴充時間項目的功能。</span><span class="sxs-lookup"><span data-stu-id="8a38d-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="8a38d-107">這包括用於新增項目類型的功能，這些類型會根據顯示為 **時間來源** 的欄位結構描述名稱 **時間項目設定** 來促使產生特定行為。</span><span class="sxs-lookup"><span data-stu-id="8a38d-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="8a38d-108">已新增名為「時間、費用、狀態和核准」(TESA) 的新解決方案來支援此功能。</span><span class="sxs-lookup"><span data-stu-id="8a38d-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="8a38d-109">升級考量</span><span class="sxs-lookup"><span data-stu-id="8a38d-109">Upgrade consideration</span></span>
<span data-ttu-id="8a38d-110">為了支援此功能，PSA 中的角色已更新為包含新權限。</span><span class="sxs-lookup"><span data-stu-id="8a38d-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="8a38d-111">這些權限會將讀取權限授與新的實體 **時間專案設定**。</span><span class="sxs-lookup"><span data-stu-id="8a38d-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="8a38d-112">除了現有角色之外，還應該將使用者角色 **時間項目使用者** 授與需要記錄時間功能的使用者。</span><span class="sxs-lookup"><span data-stu-id="8a38d-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="8a38d-113">此角色包含新的功能，可確保時間項目會繼續運作。</span><span class="sxs-lookup"><span data-stu-id="8a38d-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="8a38d-114">此外，如果您有任何自訂應用程式模組 (包括時間項目實體的所有表單)，則還必須從模組中移除 **TESA 時間項目快速建立表單**。</span><span class="sxs-lookup"><span data-stu-id="8a38d-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="8a38d-115">目前已擴充的時間項目變更</span><span class="sxs-lookup"><span data-stu-id="8a38d-115">Currently extended time entry changes</span></span>
<span data-ttu-id="8a38d-116">為了盡可能降低對目前時間項目使用者的影響，這個角色變更是繼續使用時間項目所需的唯一核心需求。</span><span class="sxs-lookup"><span data-stu-id="8a38d-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="8a38d-117">如果您已建立自訂檢視表或不同的時間項目體驗，就必須將 **時間項目設定** 欄位設定為正確的 PSA 值。</span><span class="sxs-lookup"><span data-stu-id="8a38d-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
