---
title: 使用複製專案來開發專案範本
description: 本主題提供有關如何使用 [複製專案] 自訂動作建立專案範本的資訊。
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131640"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="f86f9-103">使用複製專案來開發專案範本</span><span class="sxs-lookup"><span data-stu-id="f86f9-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="f86f9-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f86f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f86f9-105">Dynamics 365 Project Operations 支援複製專案以及將任何指派還原回一般資源 (代表角色) 的功能。</span><span class="sxs-lookup"><span data-stu-id="f86f9-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="f86f9-106">客戶可以使用此功能來建立基本專案範本。</span><span class="sxs-lookup"><span data-stu-id="f86f9-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="f86f9-107">選取 **複製專案** 時，目標專案的狀態會更新。</span><span class="sxs-lookup"><span data-stu-id="f86f9-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="f86f9-108">使用 **狀態原因** 來判斷複製動作何時完成。</span><span class="sxs-lookup"><span data-stu-id="f86f9-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="f86f9-109">選取 **複製專案** 時，如果在目標專案實體中偵測不到目標日期，也會將專案的開始日期更新為目前的開始日期。</span><span class="sxs-lookup"><span data-stu-id="f86f9-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="f86f9-110">複製專案自訂動作</span><span class="sxs-lookup"><span data-stu-id="f86f9-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="f86f9-111">名稱</span><span class="sxs-lookup"><span data-stu-id="f86f9-111">Name</span></span> 

<span data-ttu-id="f86f9-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="f86f9-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="f86f9-113">輸入參數</span><span class="sxs-lookup"><span data-stu-id="f86f9-113">Input parameters</span></span>
<span data-ttu-id="f86f9-114">有三個輸入參數：</span><span class="sxs-lookup"><span data-stu-id="f86f9-114">There are three input parameters:</span></span>

| <span data-ttu-id="f86f9-115">參數</span><span class="sxs-lookup"><span data-stu-id="f86f9-115">Parameter</span></span>          | <span data-ttu-id="f86f9-116">鍵入</span><span class="sxs-lookup"><span data-stu-id="f86f9-116">Type</span></span>   | <span data-ttu-id="f86f9-117">值</span><span class="sxs-lookup"><span data-stu-id="f86f9-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="f86f9-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="f86f9-118">ProjectCopyOption</span></span>  | <span data-ttu-id="f86f9-119">String</span><span class="sxs-lookup"><span data-stu-id="f86f9-119">String</span></span> | <span data-ttu-id="f86f9-120">**{"removeNamedResources":true}** 或 **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="f86f9-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="f86f9-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="f86f9-121">SourceProject</span></span>      | <span data-ttu-id="f86f9-122">實體參考</span><span class="sxs-lookup"><span data-stu-id="f86f9-122">Entity Reference</span></span> | <span data-ttu-id="f86f9-123">來源專案</span><span class="sxs-lookup"><span data-stu-id="f86f9-123">Source Project</span></span> |
| <span data-ttu-id="f86f9-124">目標</span><span class="sxs-lookup"><span data-stu-id="f86f9-124">Target</span></span>             | <span data-ttu-id="f86f9-125">實體參考</span><span class="sxs-lookup"><span data-stu-id="f86f9-125">Entity Reference</span></span> | <span data-ttu-id="f86f9-126">目標專案</span><span class="sxs-lookup"><span data-stu-id="f86f9-126">Target Project</span></span> |


- <span data-ttu-id="f86f9-127">**{"clearTeamsAndAssignments":true}**：Project 網頁版的預設行為，並將移除所有指派和團隊成員。</span><span class="sxs-lookup"><span data-stu-id="f86f9-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="f86f9-128">**{"removeNamedResources":true}**：Project Operations 的預設行為，並將指派還原為一般資源。</span><span class="sxs-lookup"><span data-stu-id="f86f9-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="f86f9-129">如需更多有關動作的預設行為，請參閱[使用 Web API 動作](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="f86f9-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="f86f9-130">指定要複製的欄位</span><span class="sxs-lookup"><span data-stu-id="f86f9-130">Specify fields to copy</span></span> 
<span data-ttu-id="f86f9-131">呼叫動作時，**複製專案** 會查看專案檢視表 **複製專案欄**，以判斷要在複製專案時複製哪些欄位。</span><span class="sxs-lookup"><span data-stu-id="f86f9-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
