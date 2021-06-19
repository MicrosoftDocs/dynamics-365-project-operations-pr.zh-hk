---
title: 關閉定價維度
description: 本主題提供有關如何關閉定價維度的資訊。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004558"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="fe30f-103">關閉定價維度</span><span class="sxs-lookup"><span data-stu-id="fe30f-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="fe30f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="fe30f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fe30f-105">您可能每隔幾年就需要檢閱並更新您的定價策略。</span><span class="sxs-lookup"><span data-stu-id="fe30f-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="fe30f-106">任何您所進行的更新可能都需要您關閉現有的定價維度，並建立新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="fe30f-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="fe30f-107">例如，您可能先前已依 **角色** 定價，但現在決定依據 **工作經驗** 進行定價。</span><span class="sxs-lookup"><span data-stu-id="fe30f-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="fe30f-108">這可能會要求您必須關閉以 **角色** 為定價維度的設定，並將 **工作經驗** 建立為新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="fe30f-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="fe30f-109">關閉定價維度 (不論是預設還是自訂否) 的動作，都可以藉由將定價維度的 **適用於成本** 和 **適用於銷售** 欄位設定為 **否** 來完成。</span><span class="sxs-lookup"><span data-stu-id="fe30f-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="fe30f-110">不過，這樣做時，您可能會收到錯誤訊息 **如果有相關聯的價格記錄，則無法更新或刪除定價維度。**</span><span class="sxs-lookup"><span data-stu-id="fe30f-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![關閉定價維度時可能發生商務程序錯誤](media/Business-Process-Error.png)

<span data-ttu-id="fe30f-112">此錯誤訊息表示存在先前為所要關閉維度設定的價格記錄。</span><span class="sxs-lookup"><span data-stu-id="fe30f-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="fe30f-113">必須先刪除參照該維度的所有 **角色價格** 和 **角色價格加成** 記錄，才能將維度的適用性設為 **否**。</span><span class="sxs-lookup"><span data-stu-id="fe30f-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="fe30f-114">此規則適用於內建定價維度以及任何您可能已建立的自訂定價維度。</span><span class="sxs-lookup"><span data-stu-id="fe30f-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="fe30f-115">這項驗證的原因是，每個 **角色價格** 記錄都必須有一個唯一的維度組合。</span><span class="sxs-lookup"><span data-stu-id="fe30f-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="fe30f-116">例如，在名為 **2018 年美國成本費率** 的價目表中，您有下列 **角色價格** 列。</span><span class="sxs-lookup"><span data-stu-id="fe30f-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="fe30f-117">標準職稱</span><span class="sxs-lookup"><span data-stu-id="fe30f-117">Standard Title</span></span>         | <span data-ttu-id="fe30f-118">組織單位</span><span class="sxs-lookup"><span data-stu-id="fe30f-118">Org Unit</span></span>    |<span data-ttu-id="fe30f-119">單位</span><span class="sxs-lookup"><span data-stu-id="fe30f-119">Unit</span></span>   |<span data-ttu-id="fe30f-120">價格</span><span class="sxs-lookup"><span data-stu-id="fe30f-120">Price</span></span>  |<span data-ttu-id="fe30f-121">貨幣</span><span class="sxs-lookup"><span data-stu-id="fe30f-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="fe30f-122">系統工程師</span><span class="sxs-lookup"><span data-stu-id="fe30f-122">Systems Engineer</span></span>|<span data-ttu-id="fe30f-123">Contoso 美國</span><span class="sxs-lookup"><span data-stu-id="fe30f-123">Contoso US</span></span>|<span data-ttu-id="fe30f-124">小時</span><span class="sxs-lookup"><span data-stu-id="fe30f-124">Hour</span></span>| <span data-ttu-id="fe30f-125">100</span><span class="sxs-lookup"><span data-stu-id="fe30f-125">100</span></span>|<span data-ttu-id="fe30f-126">USD</span><span class="sxs-lookup"><span data-stu-id="fe30f-126">USD</span></span>|
| <span data-ttu-id="fe30f-127">資深系統工程師</span><span class="sxs-lookup"><span data-stu-id="fe30f-127">Senior Systems Engineer</span></span>|<span data-ttu-id="fe30f-128">Contoso 美國</span><span class="sxs-lookup"><span data-stu-id="fe30f-128">Contoso US</span></span>|<span data-ttu-id="fe30f-129">小時</span><span class="sxs-lookup"><span data-stu-id="fe30f-129">Hour</span></span>| <span data-ttu-id="fe30f-130">150</span><span class="sxs-lookup"><span data-stu-id="fe30f-130">150</span></span>| <span data-ttu-id="fe30f-131">USD</span><span class="sxs-lookup"><span data-stu-id="fe30f-131">USD</span></span>|


<span data-ttu-id="fe30f-132">當您關閉以 **標準職稱** 為定價維度的設定，而定價引擎搜尋價格時，只會使用輸入內容中的 **組織單位** 值。</span><span class="sxs-lookup"><span data-stu-id="fe30f-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="fe30f-133">如果輸入內容的 **組織單位** 是「Contoso US」，則結果並非決定性，因為這兩個列都會相符。</span><span class="sxs-lookup"><span data-stu-id="fe30f-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="fe30f-134">為了避免這種案例，當您建立 **角色價格** 記錄時，系統會驗證維度組合是否為唯一。</span><span class="sxs-lookup"><span data-stu-id="fe30f-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="fe30f-135">如果維度在建立 **角色價格** 記錄後已關閉，則可能會違反此限制。</span><span class="sxs-lookup"><span data-stu-id="fe30f-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="fe30f-136">因此，關閉維度之前，必須先刪除所有已填入該維度值的 **角色價格** 和 **角色價格加成** 列。</span><span class="sxs-lookup"><span data-stu-id="fe30f-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]