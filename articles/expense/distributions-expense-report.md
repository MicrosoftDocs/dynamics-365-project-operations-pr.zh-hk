---
title: 費用報表的分配
description: 在費用報表上輸入費用時，您可以將這些費用分配至組織中的多個專案、法律實體或客戶。
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087381"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="40705-103">費用報表的分配</span><span class="sxs-lookup"><span data-stu-id="40705-103">Distributions on an expense report</span></span>

<span data-ttu-id="40705-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="40705-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="40705-105">在費用報表上輸入費用時，您可以將這些費用分配至組織中的多個專案、財務維度或客戶。</span><span class="sxs-lookup"><span data-stu-id="40705-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="40705-106">例如，林文 (Fabrikam 銷售代表) 從哥本哈根出差到法蘭克福。</span><span class="sxs-lookup"><span data-stu-id="40705-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="40705-107">林文在法蘭克福分別與兩個組織接洽，以討論每個組織各自的專案。</span><span class="sxs-lookup"><span data-stu-id="40705-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="40705-108">林文花了七個工作日與組織 A 洽談專案 A，並花費三個工作日與組織 B 洽談專案 B。</span><span class="sxs-lookup"><span data-stu-id="40705-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="40705-109">因為林文在法蘭克福期間洽談了兩個不同的專案，當她輸入費用報表時，林文會視情況分配每個專案的費用。</span><span class="sxs-lookup"><span data-stu-id="40705-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="40705-110">下表顯示林文如何分配費用。</span><span class="sxs-lookup"><span data-stu-id="40705-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="40705-111">費用類型</span><span class="sxs-lookup"><span data-stu-id="40705-111">Expense type</span></span> | <span data-ttu-id="40705-112">總計費用金額</span><span class="sxs-lookup"><span data-stu-id="40705-112">Total expense amount</span></span> | <span data-ttu-id="40705-113">分配至專案 A 的金額</span><span class="sxs-lookup"><span data-stu-id="40705-113">Amount distributed to project A</span></span> | <span data-ttu-id="40705-114">分配至專案 B 的金額</span><span class="sxs-lookup"><span data-stu-id="40705-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="40705-115">車費</span><span class="sxs-lookup"><span data-stu-id="40705-115">Train fare</span></span>   | <span data-ttu-id="40705-116">丹麥克朗 578</span><span class="sxs-lookup"><span data-stu-id="40705-116">DKK 578</span></span>              | <span data-ttu-id="40705-117">丹麥克朗 405</span><span class="sxs-lookup"><span data-stu-id="40705-117">DKK 405</span></span>                         | <span data-ttu-id="40705-118">丹麥克朗 173</span><span class="sxs-lookup"><span data-stu-id="40705-118">DKK 173</span></span>                         |
| <span data-ttu-id="40705-119">飯店</span><span class="sxs-lookup"><span data-stu-id="40705-119">Hotel</span></span>        | <span data-ttu-id="40705-120">歐元 725</span><span class="sxs-lookup"><span data-stu-id="40705-120">EUR 725</span></span>              | <span data-ttu-id="40705-121">歐元 557</span><span class="sxs-lookup"><span data-stu-id="40705-121">EUR 557</span></span>                         | <span data-ttu-id="40705-122">歐元 168</span><span class="sxs-lookup"><span data-stu-id="40705-122">EUR 168</span></span>                         |
| <span data-ttu-id="40705-123">餐費</span><span class="sxs-lookup"><span data-stu-id="40705-123">Meals</span></span>        | <span data-ttu-id="40705-124">歐元 346</span><span class="sxs-lookup"><span data-stu-id="40705-124">EUR 346</span></span>              | <span data-ttu-id="40705-125">歐元 284</span><span class="sxs-lookup"><span data-stu-id="40705-125">EUR 284</span></span>                         | <span data-ttu-id="40705-126">歐元 62</span><span class="sxs-lookup"><span data-stu-id="40705-126">EUR 62</span></span>                          |
