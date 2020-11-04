---
title: 從商機建立專案報價
description: 本主題提供有關從商機建立專案報價的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087412"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="3346e-103">從商機建立專案報價</span><span class="sxs-lookup"><span data-stu-id="3346e-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="3346e-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="3346e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3346e-105">您可以透過下列方式從專案商機建立報價：</span><span class="sxs-lookup"><span data-stu-id="3346e-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="3346e-106">透過 **專案商機** 頁面上的 **報價** 索引標籤</span><span class="sxs-lookup"><span data-stu-id="3346e-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="3346e-107">透過商機銷售處理流程</span><span class="sxs-lookup"><span data-stu-id="3346e-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="3346e-108">透過更新現有報價上的商機參考</span><span class="sxs-lookup"><span data-stu-id="3346e-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="3346e-109">透過 [專案商機] 頁面上的 [報價] 索引標籤</span><span class="sxs-lookup"><span data-stu-id="3346e-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="3346e-110">若要從商機建立專案報價，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3346e-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="3346e-111">開啟 **專案商機** 頁面，並選取 **報價** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3346e-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="3346e-112">在 **報價** 子格上，選取 **+** 以根據商機建立新的專案報價。</span><span class="sxs-lookup"><span data-stu-id="3346e-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="3346e-113">所有商機明細及相關專案價目表都會從商機複製到新的報價。</span><span class="sxs-lookup"><span data-stu-id="3346e-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="3346e-114">透過商機銷售處理流程</span><span class="sxs-lookup"><span data-stu-id="3346e-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="3346e-115">若要透過商機銷售處理流程建立報價，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3346e-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="3346e-116">從商機銷售處理流程中開啟商機。</span><span class="sxs-lookup"><span data-stu-id="3346e-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="3346e-117">選取 **授與資格** 階段。</span><span class="sxs-lookup"><span data-stu-id="3346e-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="3346e-118">選取 **下一步** ，然後選取 **+ 建立** 以建立新報價。</span><span class="sxs-lookup"><span data-stu-id="3346e-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="3346e-119">這個新報價的 **摘要** 索引標籤上的大部分資訊都已預設使用商機中的資訊。</span><span class="sxs-lookup"><span data-stu-id="3346e-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="3346e-120">輸入任何遺漏的必要資訊，或視需要更新 **摘要** 索引標籤上的預設值。</span><span class="sxs-lookup"><span data-stu-id="3346e-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="3346e-121">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="3346e-121">Select **Save**.</span></span> <span data-ttu-id="3346e-122">新的報價已建立，並已關聯至商機。</span><span class="sxs-lookup"><span data-stu-id="3346e-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="3346e-123">您現在可以在 **商機** 頁面的 **報價** 索引標籤上檢視報價資訊。</span><span class="sxs-lookup"><span data-stu-id="3346e-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="3346e-124">商機銷售處理會進入下一個階段 **提案** 。</span><span class="sxs-lookup"><span data-stu-id="3346e-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="3346e-125">透過更新現有報價上的商機參考</span><span class="sxs-lookup"><span data-stu-id="3346e-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="3346e-126">現有報價可以連結至商機。</span><span class="sxs-lookup"><span data-stu-id="3346e-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="3346e-127">完成下列步驟，以更新現有報價上的商機資訊。</span><span class="sxs-lookup"><span data-stu-id="3346e-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="3346e-128">開啟 **報價** 頁面，並選取 **摘要** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3346e-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="3346e-129">在 **商機** 欄位中，選取要連結至報價的商機。</span><span class="sxs-lookup"><span data-stu-id="3346e-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="3346e-130">您可以在商機的 **報價** 網格中查看報價。</span><span class="sxs-lookup"><span data-stu-id="3346e-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="3346e-131">商機可以使用商機銷售處理進入下一個階段 **提案** 。</span><span class="sxs-lookup"><span data-stu-id="3346e-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="3346e-132">將商機移至此階段時，您可以從與此商機相關聯的報價清單中選取此報價。</span><span class="sxs-lookup"><span data-stu-id="3346e-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="3346e-133">選取此報價即表示您要隨之向前進展。</span><span class="sxs-lookup"><span data-stu-id="3346e-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="3346e-134">在其中一項報價成交之前，所有與商機相關聯的其他報價仍然可用且有效。</span><span class="sxs-lookup"><span data-stu-id="3346e-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="3346e-135">您可以將銷售處理移回先前的階段 **授與資格** ，並選擇另一個要隨之向前進展的報價。</span><span class="sxs-lookup"><span data-stu-id="3346e-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
