---
title: 專案階段類型
description: 本主題提供有關專案階段的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123090"
---
# <a name="project-stage-types"></a><span data-ttu-id="da202-103">專案階段類型</span><span class="sxs-lookup"><span data-stu-id="da202-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="da202-104">專案階段為了反映專案進展時的狀態而設計。</span><span class="sxs-lookup"><span data-stu-id="da202-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="da202-105">自訂可以用來讓系統自動更新階段的商務程序流程、Power Automate 或外掛程式擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da202-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="da202-106">下列階段已在預設 BPF 中定義：</span><span class="sxs-lookup"><span data-stu-id="da202-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="da202-107">新增​​</span><span class="sxs-lookup"><span data-stu-id="da202-107">New</span></span>
- <span data-ttu-id="da202-108">報價</span><span class="sxs-lookup"><span data-stu-id="da202-108">Quote</span></span>
- <span data-ttu-id="da202-109">計劃</span><span class="sxs-lookup"><span data-stu-id="da202-109">Plan</span></span>
- <span data-ttu-id="da202-110">交付</span><span class="sxs-lookup"><span data-stu-id="da202-110">Deliver</span></span>
- <span data-ttu-id="da202-111">完成</span><span class="sxs-lookup"><span data-stu-id="da202-111">Complete</span></span>
- <span data-ttu-id="da202-112">關閉</span><span class="sxs-lookup"><span data-stu-id="da202-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="da202-113">新增</span><span class="sxs-lookup"><span data-stu-id="da202-113">New</span></span>

<span data-ttu-id="da202-114">建立專案時，專案階段會設定為 **新增**。</span><span class="sxs-lookup"><span data-stu-id="da202-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="da202-115">如果專案是從範本建立，則可能會有排程、估計值及團隊資料。</span><span class="sxs-lookup"><span data-stu-id="da202-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="da202-116">否則，就只是專案的大綱，您必須輸入剩餘的元件。</span><span class="sxs-lookup"><span data-stu-id="da202-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="da202-117">報價</span><span class="sxs-lookup"><span data-stu-id="da202-117">Quote</span></span>

<span data-ttu-id="da202-118">將專案與報價建立關聯或從報價建立專案時，專案階段會設定為 **報價**，而估計的開始和結束日期也會更新。</span><span class="sxs-lookup"><span data-stu-id="da202-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="da202-119">專案處於 **報價** 階段時，**專案實體** 上的 **銷售** 索引標籤會顯示報價的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="da202-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="da202-120">計劃</span><span class="sxs-lookup"><span data-stu-id="da202-120">Plan</span></span>

<span data-ttu-id="da202-121">當您贏得與專案相關聯的報價，且專案已進入 **合約** 階段時，專案階段會更新為 **計劃**。</span><span class="sxs-lookup"><span data-stu-id="da202-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="da202-122">專案處於 **計劃** 階段時，**專案實體** 頁面會顯示合約的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="da202-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="da202-123">交付</span><span class="sxs-lookup"><span data-stu-id="da202-123">Deliver</span></span>

<span data-ttu-id="da202-124">專案計劃完成，且您已準備好開始專案時，專案經理應將專案階段更新為 **交付**，以顯示專案已開始。</span><span class="sxs-lookup"><span data-stu-id="da202-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="da202-125">完成</span><span class="sxs-lookup"><span data-stu-id="da202-125">Complete</span></span> 

<span data-ttu-id="da202-126">專案的工作完成後，專案經理就可以將階段更新為 **完成**。</span><span class="sxs-lookup"><span data-stu-id="da202-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="da202-127">專案經理藉由將專案階段更新為 **完成**，指出工作已百分之百完成，但專案仍保持開啟狀態，讓您可以記錄任何擱置的時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="da202-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="da202-128">關閉</span><span class="sxs-lookup"><span data-stu-id="da202-128">Close</span></span>

<span data-ttu-id="da202-129">將專案所有的交易都記錄下來後，專案經理就可以將階段更新為 **關閉**。</span><span class="sxs-lookup"><span data-stu-id="da202-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="da202-130">此時，無法記錄任何交易，且專案會設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="da202-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
