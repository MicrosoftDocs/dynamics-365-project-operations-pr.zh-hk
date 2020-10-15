---
title: 預約給專案
description: 本主題提供有關預約資源給專案的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908767"
---
# <a name="book-to-a-project"></a><span data-ttu-id="48994-103">預約給專案</span><span class="sxs-lookup"><span data-stu-id="48994-103">Book to a project</span></span>

<span data-ttu-id="48994-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="48994-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48994-105">專案經理或資源管理員有時需要將資源配置給沒有一般團隊成員所定義之特定需求的專案。</span><span class="sxs-lookup"><span data-stu-id="48994-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="48994-106">這可以透過三種方式之一來達成。</span><span class="sxs-lookup"><span data-stu-id="48994-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="48994-107">從團隊成員網格預約</span><span class="sxs-lookup"><span data-stu-id="48994-107">Book from the team member grid</span></span>
- <span data-ttu-id="48994-108">從排程面板預約</span><span class="sxs-lookup"><span data-stu-id="48994-108">Book from the schedule board</span></span>
- <span data-ttu-id="48994-109">從**專案**表單預約</span><span class="sxs-lookup"><span data-stu-id="48994-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="48994-110">從團隊成員網格預約</span><span class="sxs-lookup"><span data-stu-id="48994-110">Book from the team member grid</span></span>

<span data-ttu-id="48994-111">如果您的組織是在混合資源配置模式下運作，則專案經理可以完成下列步驟，直接將資源預約給專案。</span><span class="sxs-lookup"><span data-stu-id="48994-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="48994-112">從專案中移至團隊成員網格，然後選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="48994-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="48994-113">定義資源的職位名稱和角色。</span><span class="sxs-lookup"><span data-stu-id="48994-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="48994-114">從可用的查詢中選取可預約資源。</span><span class="sxs-lookup"><span data-stu-id="48994-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="48994-115">選取資源之後，定義下列欄位資訊以預約資源：</span><span class="sxs-lookup"><span data-stu-id="48994-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="48994-116">開始日期</span><span class="sxs-lookup"><span data-stu-id="48994-116">Start date</span></span>
    - <span data-ttu-id="48994-117">完成日期</span><span class="sxs-lookup"><span data-stu-id="48994-117">Finish date</span></span>
    - <span data-ttu-id="48994-118">配置方法</span><span class="sxs-lookup"><span data-stu-id="48994-118">Allocation method</span></span>
    - <span data-ttu-id="48994-119">時數 (如果適用)</span><span class="sxs-lookup"><span data-stu-id="48994-119">Hours, if applicable</span></span>
    - <span data-ttu-id="48994-120">專案核准者</span><span class="sxs-lookup"><span data-stu-id="48994-120">Project approver</span></span>

6. <span data-ttu-id="48994-121">選取**儲存後關閉**</span><span class="sxs-lookup"><span data-stu-id="48994-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="48994-122">從排程面板預約</span><span class="sxs-lookup"><span data-stu-id="48994-122">Book from the schedule board</span></span>

<span data-ttu-id="48994-123">資源管理員需要直接將資源預約給專案時，他們可以使用排程面板和專案需求。</span><span class="sxs-lookup"><span data-stu-id="48994-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="48994-124">專案需求是隨時可供預約的資源需求。</span><span class="sxs-lookup"><span data-stu-id="48994-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="48994-125">若要直接從排程面板預約給專案，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="48994-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="48994-126">瀏覽至排程面板，然後在左側頁面上，篩選您考慮要用於需求的資源。</span><span class="sxs-lookup"><span data-stu-id="48994-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="48994-127">在下方窗格中，選取**專案**索引標籤，以檢視專案需求清單。</span><span class="sxs-lookup"><span data-stu-id="48994-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="48994-128">將需求拖曳到資源，並定義下列資訊：</span><span class="sxs-lookup"><span data-stu-id="48994-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="48994-129">開始日期</span><span class="sxs-lookup"><span data-stu-id="48994-129">Start date</span></span>
    - <span data-ttu-id="48994-130">完成日期</span><span class="sxs-lookup"><span data-stu-id="48994-130">Finish date</span></span>
    - <span data-ttu-id="48994-131">預約狀態</span><span class="sxs-lookup"><span data-stu-id="48994-131">Booking status</span></span>
    - <span data-ttu-id="48994-132">預約方式</span><span class="sxs-lookup"><span data-stu-id="48994-132">Booking method</span></span>
    - <span data-ttu-id="48994-133">持續時間</span><span class="sxs-lookup"><span data-stu-id="48994-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="48994-134">從專案表單中預約</span><span class="sxs-lookup"><span data-stu-id="48994-134">Book from the Project form</span></span>

<span data-ttu-id="48994-135">身為專案經理，您可能需要將資源預約給專案，但是只知道準則，而不知資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="48994-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="48994-136">請完成下列步驟，使用排程小幫手根據資源的任何可用屬性來尋找資源。</span><span class="sxs-lookup"><span data-stu-id="48994-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="48994-137">瀏覽至專案，並選取**預約**以開啟排程小幫手。</span><span class="sxs-lookup"><span data-stu-id="48994-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="48994-138">使用排程小幫手左側的篩選，縮小準則的範圍並選取**搜尋**。</span><span class="sxs-lookup"><span data-stu-id="48994-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="48994-139">您可以根據結果中傳回的資源來預約資源。</span><span class="sxs-lookup"><span data-stu-id="48994-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="48994-140">此方法不會為資源建立任何預約。</span><span class="sxs-lookup"><span data-stu-id="48994-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="48994-141">反而是將資源新增至團隊。</span><span class="sxs-lookup"><span data-stu-id="48994-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="48994-142">將團隊成員新增至專案之後，專案經理就可以使用維護預約或延長預約，將必要的預約新增至資源。</span><span class="sxs-lookup"><span data-stu-id="48994-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
