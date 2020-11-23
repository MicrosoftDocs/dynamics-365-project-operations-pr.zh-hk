---
title: 複製專案型商機
description: 本主題提供有關在 Project Operations 中複製專案型商機的資訊。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26ae5cc267bb06f958bbf9cdce2d80ccde9d3d24
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181719"
---
# <a name="copy-project-based-opportunities"></a><span data-ttu-id="1c0fc-103">複製專案型商機</span><span class="sxs-lookup"><span data-stu-id="1c0fc-103">Copy project-based opportunities</span></span>

<span data-ttu-id="1c0fc-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="1c0fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1c0fc-105">您可以輕鬆地透過複製專案商機，建立新的專案商機。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-105">Project opportunities can easily be copied to create new project opportunities.</span></span> 

1. <span data-ttu-id="1c0fc-106">移至 **專案商機** 清單頁面，並從清單選取商機。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-106">Go to the **Project Opportunities** list page and select an opportunity from the list.</span></span> <span data-ttu-id="1c0fc-107">或者，開啟特定商機的詳細資料頁面。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-107">Or, open the details page of a specific opportunity.</span></span> 
2. <span data-ttu-id="1c0fc-108">從任一頁面選取 **複製**。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-108">From either page, select **Copy**.</span></span> <span data-ttu-id="1c0fc-109">對話方塊頁面會開啟，其中包含下列欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-109">A dialog page will open that contains the following field information.</span></span> <span data-ttu-id="1c0fc-110">視此對話方塊中選取的值而定，複製程序可能會變更。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-110">Depending on the values selected in this dialog, the copy process may change.</span></span>

    | <span data-ttu-id="1c0fc-111">**欄位**</span><span class="sxs-lookup"><span data-stu-id="1c0fc-111">**Field**</span></span> | <span data-ttu-id="1c0fc-112">**描述**</span><span class="sxs-lookup"><span data-stu-id="1c0fc-112">**Description**</span></span> | <span data-ttu-id="1c0fc-113">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="1c0fc-113">**Downstream impact**</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="1c0fc-114">主題</span><span class="sxs-lookup"><span data-stu-id="1c0fc-114">Topic</span></span> | <span data-ttu-id="1c0fc-115">輸入目標商機的相關主題。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-115">Enter the relevant topic of the target opportunity.</span></span> <span data-ttu-id="1c0fc-116">對話方塊開啟時，系統會將其設定為來源商務的主題，並在其後附加 **複製**。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-116">When the dialog opens, the system will set it to the topic of the source opportunity with **copy** appended to it.</span></span> | <span data-ttu-id="1c0fc-117">此欄位沒有任何下游影響。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-117">There's no downstream impact for this field.</span></span> |
    | <span data-ttu-id="1c0fc-118">帳戶</span><span class="sxs-lookup"><span data-stu-id="1c0fc-118">Account</span></span> | <span data-ttu-id="1c0fc-119">參考客戶的公司或客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-119">References the customer's company or account record.</span></span> <span data-ttu-id="1c0fc-120">對話方塊開啟時，系統會將其設定為來源商機上的客戶。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-120">Wen the dialog opens, the system will set it to the account on the source opportunity.</span></span> | <span data-ttu-id="1c0fc-121">此欄位是商機上的主要客戶。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-121">This field is the primary customer on the opportunity.</span></span> |
    | <span data-ttu-id="1c0fc-122">合約單位</span><span class="sxs-lookup"><span data-stu-id="1c0fc-122">Contracting Unit</span></span> | <span data-ttu-id="1c0fc-123">負責交付與此交易相關之專案的組織單位。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-123">The organization unit responsible for the delivery of the projects associated with this deal.</span></span> <span data-ttu-id="1c0fc-124">對話方塊開啟時，系統會將其設定為來源商機的合約單位。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-124">When the dialog opens, the system will set it to the contracting unit of the source opportunity.</span></span> | <span data-ttu-id="1c0fc-125">合約單位是在完成交易後執行專案的公司部門。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-125">The contracting unit is the division of the company that executes the projects after the deal is closed.</span></span> <span data-ttu-id="1c0fc-126">每個合約單位都有貨幣，而此貨幣可用來報告專案期間所產生的估計和實際成本。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-126">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the project.</span></span> |
    | <span data-ttu-id="1c0fc-127">貨幣</span><span class="sxs-lookup"><span data-stu-id="1c0fc-127">Currency</span></span> | <span data-ttu-id="1c0fc-128">進行交易所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-128">The currency that the deal is transacted in.</span></span> <span data-ttu-id="1c0fc-129">對話方塊頁面開啟時，系統會將其設定為來源商機的貨幣。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-129">When the dialog page opens, the system will set it to the currency of the source opportunity.</span></span> | <span data-ttu-id="1c0fc-130">貨幣會用來預設價目表，並建立對報價的財務估計值。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-130">Currency is used to default a price list and build financial estimates on the quote.</span></span> <span data-ttu-id="1c0fc-131">最終會在交易成交時使用此貨幣來為客戶開立發票。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-131">Eventually, the currency is used to invoice the customer when the deal is won.</span></span> |
    | <span data-ttu-id="1c0fc-132">複製定價</span><span class="sxs-lookup"><span data-stu-id="1c0fc-132">Copy pricing</span></span> | <span data-ttu-id="1c0fc-133">[是/否] 值，指示是否應從源商機複製商機的定價。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-133">A Yes/No value that indicates if the pricing on the opportunity should be copied from the source opportunity.</span></span> | <span data-ttu-id="1c0fc-134">如果選取 **是**，則將價目表從來源複製到目標商機。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-134">If **Yes** is selected, price lists are copied from the source to the target opportunity.</span></span> <span data-ttu-id="1c0fc-135">如果選取 **否**，則根據已設定的最新價目表來設定預設價目表。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-135">If **No** is selected, price lists are defaulted based on the latest price lists that were set up.</span></span> |

3. <span data-ttu-id="1c0fc-136">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-136">Select **OK**.</span></span> <span data-ttu-id="1c0fc-137">系統會根據選取的參數建立專案商機的複本，並開啟新的專案商機。</span><span class="sxs-lookup"><span data-stu-id="1c0fc-137">The system creates a copy of the project opportunity based on the selected parameters and the new project opportunity is opened.</span></span>
