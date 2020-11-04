---
title: 設定公司之間的專案發票開立
description: 本主題說明如何設定您組織中兩家公司之間的專案發票開立。
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087559"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="78fe1-103">設定公司之間的專案發票開立</span><span class="sxs-lookup"><span data-stu-id="78fe1-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78fe1-104">本主題說明如何設定您組織中兩家公司之間的專案發票開立。</span><span class="sxs-lookup"><span data-stu-id="78fe1-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="78fe1-105">此工作會使用 USSI 資料集。</span><span class="sxs-lookup"><span data-stu-id="78fe1-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="78fe1-106">在導覽窗格中，移至 **模組 > 應付帳款 > 供應商 > 所有供應商** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="78fe1-107">在 **所有供應商** 清單中，尋找並選取所需的記錄。</span><span class="sxs-lookup"><span data-stu-id="78fe1-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="78fe1-108">在動作窗格上，選取 **一般** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="78fe1-109">選取 **公司之間** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="78fe1-110">將 **使用中** 設定為 **是** 以啟用公司間的交易。</span><span class="sxs-lookup"><span data-stu-id="78fe1-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="78fe1-111">在 **客戶公司** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="78fe1-112">在 **我的客戶** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="78fe1-113">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-113">Select **Save**.</span></span>
9. <span data-ttu-id="78fe1-114">關閉頁面以返回首頁。</span><span class="sxs-lookup"><span data-stu-id="78fe1-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="78fe1-115">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 專案管理與會計參數** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="78fe1-116">選取 **公司之間** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="78fe1-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="78fe1-117">將滑桿移到 **是** ，以啟用公司間的資源排程和時程表。</span><span class="sxs-lookup"><span data-stu-id="78fe1-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="78fe1-118">在清單中，標記所選取的列。</span><span class="sxs-lookup"><span data-stu-id="78fe1-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="78fe1-119">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-119">Select **New**.</span></span>
15. <span data-ttu-id="78fe1-120">在 **瀏覽法律實體** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="78fe1-121">選取 **應計收入** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="78fe1-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="78fe1-122">在 **預設時程表類別** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="78fe1-123">在 **預設費用類別** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="78fe1-124">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-124">Select **Save**.</span></span>
20. <span data-ttu-id="78fe1-125">關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="78fe1-125">Close the page.</span></span>
21. <span data-ttu-id="78fe1-126">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 過帳 > 總帳過帳設定** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="78fe1-127">在 **總帳會計科目類型** 欄位中，選取選項。</span><span class="sxs-lookup"><span data-stu-id="78fe1-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="78fe1-128">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-128">Select **New**.</span></span>
24. <span data-ttu-id="78fe1-129">在 **主要會計科目** 欄位中，指定所需的值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="78fe1-130">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-130">Select **Save**.</span></span>
26. <span data-ttu-id="78fe1-131">關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="78fe1-131">Close the page.</span></span>
27. <span data-ttu-id="78fe1-132">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 轉撥價格** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="78fe1-133">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-133">Select **New**.</span></span>
29. <span data-ttu-id="78fe1-134">在 **生效日期** 欄位中，輸入日期。</span><span class="sxs-lookup"><span data-stu-id="78fe1-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="78fe1-135">在 **瀏覽法律實體** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="78fe1-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="78fe1-136">在 **轉撥價格模型** 欄位中，選取選項。</span><span class="sxs-lookup"><span data-stu-id="78fe1-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="78fe1-137">在 **定價** 欄位中，輸入數字。</span><span class="sxs-lookup"><span data-stu-id="78fe1-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="78fe1-138">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="78fe1-138">Select **Save**.</span></span>

