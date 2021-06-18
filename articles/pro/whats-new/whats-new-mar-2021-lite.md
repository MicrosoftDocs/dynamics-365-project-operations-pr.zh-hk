---
title: 2021 年 3 月 - Project Operations 精簡部署新增功能
description: 本主題提供關於 Project Operations Lite 精簡部署 2021 年 3 月版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993893"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="14d40-103">2021 年 3 月 - Project Operations 精簡部署新增功能</span><span class="sxs-lookup"><span data-stu-id="14d40-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="14d40-104">_適用於：精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="14d40-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="14d40-105">此主題適用於下列 Dynamics 365 Project Operations 元件和版本：</span><span class="sxs-lookup"><span data-stu-id="14d40-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="14d40-106">Dataverse 環境的 Project Operations 版本 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="14d40-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="14d40-107">品質更新</span><span class="sxs-lookup"><span data-stu-id="14d40-107">Quality updates</span></span>

| <span data-ttu-id="14d40-108">**功能區域**</span><span class="sxs-lookup"><span data-stu-id="14d40-108">**Feature area**</span></span> | <span data-ttu-id="14d40-109">**參考編號**</span><span class="sxs-lookup"><span data-stu-id="14d40-109">**Reference number**</span></span> | <span data-ttu-id="14d40-110">**品質更新**</span><span class="sxs-lookup"><span data-stu-id="14d40-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="14d40-111">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="14d40-111">Billing and pricing</span></span> | <span data-ttu-id="14d40-112">2133873</span><span class="sxs-lookup"><span data-stu-id="14d40-112">2133873</span></span> | <span data-ttu-id="14d40-113">修正 **銷售單價** 貨幣符號在 **費用估計值** 網格中的顯示。</span><span class="sxs-lookup"><span data-stu-id="14d40-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="14d40-114">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="14d40-114">Billing and pricing</span></span> | <span data-ttu-id="14d40-115">2174616</span><span class="sxs-lookup"><span data-stu-id="14d40-115">2174616</span></span> | <span data-ttu-id="14d40-116">報價成交時，從報價複製而來的合約服務內容詳細資料會參考合約自訂價目表。</span><span class="sxs-lookup"><span data-stu-id="14d40-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="14d40-117">商機管理</span><span class="sxs-lookup"><span data-stu-id="14d40-117">Opportunity Management</span></span> | <span data-ttu-id="14d40-118">2167475</span><span class="sxs-lookup"><span data-stu-id="14d40-118">2167475</span></span> | <span data-ttu-id="14d40-119">修正源自未開單實際值項目之更正發票中的稅額。</span><span class="sxs-lookup"><span data-stu-id="14d40-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="14d40-120">商機管理</span><span class="sxs-lookup"><span data-stu-id="14d40-120">Opportunity Management</span></span> | <span data-ttu-id="14d40-121">2176285</span><span class="sxs-lookup"><span data-stu-id="14d40-121">2176285</span></span> | <span data-ttu-id="14d40-122">不可將銷售合約/報價明細詳細資料中的稅額複製到成本合約/報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="14d40-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="14d40-123">商機管理</span><span class="sxs-lookup"><span data-stu-id="14d40-123">Opportunity Management</span></span> | <span data-ttu-id="14d40-124">2188079</span><span class="sxs-lookup"><span data-stu-id="14d40-124">2188079</span></span> | <span data-ttu-id="14d40-125">不可建立非工作型合約的分割帳單規則。</span><span class="sxs-lookup"><span data-stu-id="14d40-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="14d40-126">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="14d40-126">Planning and Tracking</span></span> | <span data-ttu-id="14d40-127">2138853</span><span class="sxs-lookup"><span data-stu-id="14d40-127">2138853</span></span> | <span data-ttu-id="14d40-128">更新專案複製功能，確保已將參考工作的費用估計明細複製到目的地專案。</span><span class="sxs-lookup"><span data-stu-id="14d40-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="14d40-129">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="14d40-129">Planning and Tracking</span></span> | <span data-ttu-id="14d40-130">2173259</span><span class="sxs-lookup"><span data-stu-id="14d40-130">2173259</span></span> | <span data-ttu-id="14d40-131">更新專案複製功能，以確保此功能不會在特定案例中顯示 **複製 WBS** 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="14d40-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="14d40-132">時間和費用</span><span class="sxs-lookup"><span data-stu-id="14d40-132">Time and Expense</span></span> | <span data-ttu-id="14d40-133">2148910</span><span class="sxs-lookup"><span data-stu-id="14d40-133">2148910</span></span> | <span data-ttu-id="14d40-134">修正 **編輯項目** 頁面在 **時間項目** 網格中的顯示問題。</span><span class="sxs-lookup"><span data-stu-id="14d40-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="14d40-135">時間和費用</span><span class="sxs-lookup"><span data-stu-id="14d40-135">Time and Expense</span></span> | <span data-ttu-id="14d40-136">2159798</span><span class="sxs-lookup"><span data-stu-id="14d40-136">2159798</span></span> | <span data-ttu-id="14d40-137">加強控制，以確保無法編輯已核准的費用項目。</span><span class="sxs-lookup"><span data-stu-id="14d40-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


