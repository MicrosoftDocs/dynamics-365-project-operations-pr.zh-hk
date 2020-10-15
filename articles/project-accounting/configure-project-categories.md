---
title: 設定專案類別
description: 本主題提供有關設定專案類別的資訊。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895993"
---
# <a name="configure-project-categories"></a><span data-ttu-id="57efb-103">設定專案類別</span><span class="sxs-lookup"><span data-stu-id="57efb-103">Configure project categories</span></span>

<span data-ttu-id="57efb-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="57efb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="57efb-105">Project Operations 提供可在專案中分類營收及費用的強大功能。</span><span class="sxs-lookup"><span data-stu-id="57efb-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="57efb-106">類別提供用於報告和分析專案交易以及加速過帳至總帳的功能。</span><span class="sxs-lookup"><span data-stu-id="57efb-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="57efb-107">下圖說明交易類別、共用類別與專案類別之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="57efb-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="57efb-108">交易類別是專案交易的基本群組。</span><span class="sxs-lookup"><span data-stu-id="57efb-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="57efb-109">在該群組中，有一組可以在應用程式與模組之間共用的共用類別。</span><span class="sxs-lookup"><span data-stu-id="57efb-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="57efb-110">專案類別更進一步深入細節，是最細微的類別等級。</span><span class="sxs-lookup"><span data-stu-id="57efb-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="57efb-111">專案類別是特定法律實體、模組和應用程式的專屬類別。</span><span class="sxs-lookup"><span data-stu-id="57efb-111">Project categories are specific to legal entity, module, and application.</span></span>

![交易類別、共用類別與專案類別之間的關聯性](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="57efb-113">交易類別</span><span class="sxs-lookup"><span data-stu-id="57efb-113">Transaction categories</span></span>

<span data-ttu-id="57efb-114">交易類別代表專案交易的基本群組，並非特定公司或交易類型的專屬類別。</span><span class="sxs-lookup"><span data-stu-id="57efb-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="57efb-115">例如，Contoso Robotics 會使用設計、差旅、安裝及服務交易類別，將專案交易分為群組。</span><span class="sxs-lookup"><span data-stu-id="57efb-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="57efb-116">交易類別是在 Project Operations 模組中定義。</span><span class="sxs-lookup"><span data-stu-id="57efb-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="57efb-117">移至**設定**\>**交易類別**以開啟表單。</span><span class="sxs-lookup"><span data-stu-id="57efb-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="57efb-118">選取**新增**或選取**從 Excel 匯入**以建立新的交易類別。</span><span class="sxs-lookup"><span data-stu-id="57efb-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="57efb-119">共用類別</span><span class="sxs-lookup"><span data-stu-id="57efb-119">Shared categories</span></span>

<span data-ttu-id="57efb-120">Dynamics 365 使用共用類別概念，將不同應用程式 (例如 Dynamics 365 Finance、Dynamics 365 Supply Chain 和 Dynamics 365 Project Operations) 中的費用分類。</span><span class="sxs-lookup"><span data-stu-id="57efb-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="57efb-121">對於建立的每個交易類別，Project Operations 都會自動建立四個相關的共用類別：時數、費用、服務費和項目。</span><span class="sxs-lookup"><span data-stu-id="57efb-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="57efb-122">您可以移至**專案管理與會計**\>**設定**\>**類別**\>**共用類別**，檢閱並協調共用類別。</span><span class="sxs-lookup"><span data-stu-id="57efb-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="57efb-123">專案類別</span><span class="sxs-lookup"><span data-stu-id="57efb-123">Project categories</span></span>

<span data-ttu-id="57efb-124">專案類別代表最細微的類別設定等級，而且必須由專案會計師分別為每個公司進行設定。</span><span class="sxs-lookup"><span data-stu-id="57efb-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="57efb-125">移至**專案管理與會計**\>**設定**\>**類別**\>**專案類別**。</span><span class="sxs-lookup"><span data-stu-id="57efb-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="57efb-126">選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="57efb-126">Select **New**.</span></span>
3. <span data-ttu-id="57efb-127">選取您在上一節所建立之共用類別的**類別識別碼**。</span><span class="sxs-lookup"><span data-stu-id="57efb-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="57efb-128">Project Operations 只允許使用那些與交易類別有關聯的共用類別。</span><span class="sxs-lookup"><span data-stu-id="57efb-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="57efb-129">選取類別群組。</span><span class="sxs-lookup"><span data-stu-id="57efb-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="57efb-130">類別群組</span><span class="sxs-lookup"><span data-stu-id="57efb-130">Category groups</span></span>

<span data-ttu-id="57efb-131">類別群組會在相關專案類別之間用來共用屬性 (主要是過帳設定檔)。</span><span class="sxs-lookup"><span data-stu-id="57efb-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="57efb-132">每個交易類型都必須至少有一個類別群組，而且每個專案類別都已指派給群組。</span><span class="sxs-lookup"><span data-stu-id="57efb-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="57efb-133">Project Operations 中的過帳規範是由專案成本與營收設定檔規則、專案類別和類別群組所定義。</span><span class="sxs-lookup"><span data-stu-id="57efb-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="57efb-134">您可以移至**專案管理與會計**\>**設定**\>**類別**\>**類別群組**來設定類別群組。</span><span class="sxs-lookup"><span data-stu-id="57efb-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
