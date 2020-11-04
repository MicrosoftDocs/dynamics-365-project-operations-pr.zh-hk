---
title: 預設價目表
description: 本主題提供有關 Project Operations 中預設銷售及成本價目表的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087379"
---
# <a name="default-price-lists"></a><span data-ttu-id="22cc5-103">預設價目表</span><span class="sxs-lookup"><span data-stu-id="22cc5-103">Default price lists</span></span>

<span data-ttu-id="22cc5-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="22cc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="sales-price-lists"></a><span data-ttu-id="22cc5-105">銷售價目表</span><span class="sxs-lookup"><span data-stu-id="22cc5-105">Sales price lists</span></span>

<span data-ttu-id="22cc5-106">Dynamics 365 Project Operations 中的每個專案報價和合約都包含預設銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-106">Every project quote and contract in Dynamics 365 Project Operations contains a default sales price list.</span></span> 

### <a name="price-list-default-on-project-quotes"></a><span data-ttu-id="22cc5-107">專案報價上的價目表預設值</span><span class="sxs-lookup"><span data-stu-id="22cc5-107">Price list default on project quotes</span></span>
<span data-ttu-id="22cc5-108">系統會完成下列程序，以判斷專案報價預設要使用的價目表：</span><span class="sxs-lookup"><span data-stu-id="22cc5-108">The system completes the following process to determine which price list to default on a project quote:</span></span>

1. <span data-ttu-id="22cc5-109">系統查看已附加至客戶專案價目表的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-109">The system looks at the price lists that are attached to the account's project price lists.</span></span> 
2. <span data-ttu-id="22cc5-110">如果有附加至客戶記錄的專案價目表，則系統會查看附加至專案參數 (符合專案報價貨幣) 的銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-110">If there are project price lists attached to the account record, the system looks at the sales price lists attached to the project parameters that match the currency of the project quote.</span></span>
3. <span data-ttu-id="22cc5-111">接下來，系統會檢查價目表的日期有效性 (是否符合專案報價日期範圍)。</span><span class="sxs-lookup"><span data-stu-id="22cc5-111">Next, the system checks the date effectivity of the price lists that match the date range of the project quote.</span></span> <span data-ttu-id="22cc5-112">具體而言，報價建立日期。</span><span class="sxs-lookup"><span data-stu-id="22cc5-112">Specifically, the date the quote was created.</span></span>
4. <span data-ttu-id="22cc5-113">如果有多個對專案報價日期生效的價目表，則專案報價預設使用所有的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-113">If there are multiple price lists that are effective for the date of the project quote, all of the price lists default on the project quote.</span></span>
5. <span data-ttu-id="22cc5-114">如果沒有任何價目表對專案報價日期生效，則專案報價上沒有預設專案價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-114">If no price lists in effect for the date of the project quote, there's no default project price list on the project quote.</span></span> <span data-ttu-id="22cc5-115">專案報價上會出現警告訊息。</span><span class="sxs-lookup"><span data-stu-id="22cc5-115">A warning message will occur on the project quote.</span></span> <span data-ttu-id="22cc5-116">訊息表示因為沒有附加專案價目表，無法設定專案估計值與實際值的價格。</span><span class="sxs-lookup"><span data-stu-id="22cc5-116">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

### <a name="price-list-default-on-project-contracts"></a><span data-ttu-id="22cc5-117">專案合約上的價目表預設值</span><span class="sxs-lookup"><span data-stu-id="22cc5-117">Price list default on project contracts</span></span> 
<span data-ttu-id="22cc5-118">系統會完成下列程序，以判斷專案合約預設要使用的價目表：</span><span class="sxs-lookup"><span data-stu-id="22cc5-118">The system completes the following process to determine which price list to default on a project contract:</span></span>

1. <span data-ttu-id="22cc5-119">如果合約是從報價建立，報價上的專案價目表會個別複製並附加到專案合約。</span><span class="sxs-lookup"><span data-stu-id="22cc5-119">If the contract is created from a quote, the project price lists on the quote are copied over separately and attached to the project contract.</span></span>
2. <span data-ttu-id="22cc5-120">如果合約是從頭開始建立，系統會查看附加至客戶專案價目表的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-120">If the contract is created from scratch, the system looks at the price lists that are attached to the project price lists of the account.</span></span> <span data-ttu-id="22cc5-121">如果沒有附加至客戶記錄的專案價目表，則系統會尋找附加至專案參數 (符合專案合約貨幣) 的銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-121">If there aren't project price lists attached to the account record, the system looks for sales price lists attached to the project parameters that match the currency of the project contract.</span></span>
4. <span data-ttu-id="22cc5-122">接下來，系統會檢查價目表的日期有效性 (是否符合專案合約日期範圍)。</span><span class="sxs-lookup"><span data-stu-id="22cc5-122">Next, the system checks the date effectivity of the price lists that match the date range of the project contract.</span></span> <span data-ttu-id="22cc5-123">具體而言，合約建立日期。</span><span class="sxs-lookup"><span data-stu-id="22cc5-123">Specifically, the date the contract was created.</span></span>
5. <span data-ttu-id="22cc5-124">如果有多個對合約日期生效的價目表，則合約預設使用所有的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-124">If there are multiple price lists that are effective for the date of the contract, all of the price lists default on the contract.</span></span>
6. <span data-ttu-id="22cc5-125">如果沒有任何價目表對合約日期生效，則合約沒有預設使用的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-125">If there are no price lists in effect for the date of the contract, no project price lists default to the contract.</span></span> <span data-ttu-id="22cc5-126">專案合約上會出現警告訊息。</span><span class="sxs-lookup"><span data-stu-id="22cc5-126">A warning message will occur on the project contract.</span></span> <span data-ttu-id="22cc5-127">訊息表示因為沒有附加專案價目表，無法設定專案估計值與實際值的價格。</span><span class="sxs-lookup"><span data-stu-id="22cc5-127">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

## <a name="cost-price-lists"></a><span data-ttu-id="22cc5-128">成本價目表</span><span class="sxs-lookup"><span data-stu-id="22cc5-128">Cost price lists</span></span>

<span data-ttu-id="22cc5-129">Project Operations 中的任何實體都不會預設使用成本價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-129">Cost price lists don't default to any entity in Project Operations.</span></span> <span data-ttu-id="22cc5-130">對於專案成本所要使用之成本價目表的判斷一直都是在此刻完成。</span><span class="sxs-lookup"><span data-stu-id="22cc5-130">Determining the cost price list to use for project costs is always done in the moment.</span></span> <span data-ttu-id="22cc5-131">系統會完成下列程序，以判斷哪個價目表要用於專案成本：</span><span class="sxs-lookup"><span data-stu-id="22cc5-131">The system completes the following process to determine which price list to use for project costs:</span></span>

1. <span data-ttu-id="22cc5-132">系統首先查看附加至專案承包組織單位的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-132">The system first looks at the price lists that are attached to the contracting organization unit of the project.</span></span>
2. <span data-ttu-id="22cc5-133">系統接著查看價目表的日期有效性 (是否符合新加入估計或實際明細的日期)。</span><span class="sxs-lookup"><span data-stu-id="22cc5-133">The system then looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> <span data-ttu-id="22cc5-134">在此情況下， *估計明細* 是指 Project Operations 中的全部三種估計內容。</span><span class="sxs-lookup"><span data-stu-id="22cc5-134">In this situation, *estimate line* refers to all three contexts of estimation in Project Operations:</span></span>

    - <span data-ttu-id="22cc5-135">專案估計明細</span><span class="sxs-lookup"><span data-stu-id="22cc5-135">Project estimate line</span></span>
    - <span data-ttu-id="22cc5-136">報價明細詳細資訊</span><span class="sxs-lookup"><span data-stu-id="22cc5-136">Quote line detail</span></span>
    - <span data-ttu-id="22cc5-137">合約服務內容詳細資料</span><span class="sxs-lookup"><span data-stu-id="22cc5-137">Contract line detail</span></span>
  
3. <span data-ttu-id="22cc5-138">如果有多個價目表對新加入估計值或實際值的日期生效，則會選取最近建立的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-138">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
4. <span data-ttu-id="22cc5-139">如果沒有附加至專案承包組織單位的價目表，則系統會查看附加至專案參數 (符合專案貨幣) 的成本價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-139">If there no price lists attached to the contracting organization unit of the project, the system looks at cost price lists attached to project parameters that match the currency of the project.</span></span>
5. <span data-ttu-id="22cc5-140">系統接下來查看價目表的日期有效性 (是否符合新加入估計或實際明細的日期)。</span><span class="sxs-lookup"><span data-stu-id="22cc5-140">Next the system looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> 
6. <span data-ttu-id="22cc5-141">如果有多個價目表對新加入估計值或實際值的日期生效，則會選取最近建立的價目表。</span><span class="sxs-lookup"><span data-stu-id="22cc5-141">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
7. <span data-ttu-id="22cc5-142">如果沒有任何已附加至專案參數的成本價目表符合貨幣及有效日期，則系統會在新加入的估計或實際明細上預設成本費率為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="22cc5-142">If there are no cost price lists attached to the project parameters that match the currency and effective date, the system defaults the cost rate to zero (0) on the incoming estimate or actual line.</span></span>
