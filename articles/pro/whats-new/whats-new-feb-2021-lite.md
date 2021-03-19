---
title: 2021 年 2 月 - Project Operations 精簡部署新增功能
description: 本主題提供關於 Project Operations Lite 精簡部署 2021 年 2 月版本中所提供之品質更新的資訊。
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: df6490d3d9c28b095efd5ef856064de4b1517055
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272190"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a><span data-ttu-id="3d32f-103">2021 年 2 月 - Project Operations 精簡部署新增功能</span><span class="sxs-lookup"><span data-stu-id="3d32f-103">What's new February 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="3d32f-104">此主題適用於下列 Dynamics 365 Project Operations 元件和版本：</span><span class="sxs-lookup"><span data-stu-id="3d32f-104">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

  - <span data-ttu-id="3d32f-105">Dataverse 環境的 Project Operations 版本 4.7.0.95</span><span class="sxs-lookup"><span data-stu-id="3d32f-105">Project Operations on Dataverse environment version 4.7.0.95</span></span>

## <a name="quality-updates"></a><span data-ttu-id="3d32f-106">品質更新</span><span class="sxs-lookup"><span data-stu-id="3d32f-106">Quality updates</span></span>

| <span data-ttu-id="3d32f-107">**功能區域**</span><span class="sxs-lookup"><span data-stu-id="3d32f-107">**Feature Area**</span></span> | <span data-ttu-id="3d32f-108">**參考編號**</span><span class="sxs-lookup"><span data-stu-id="3d32f-108">**Reference number**</span></span> | <span data-ttu-id="3d32f-109">**品質更新**</span><span class="sxs-lookup"><span data-stu-id="3d32f-109">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3d32f-110">**帳單和定價**</span><span class="sxs-lookup"><span data-stu-id="3d32f-110">**Billing and Pricing**</span></span> | <span data-ttu-id="3d32f-111">2053736</span><span class="sxs-lookup"><span data-stu-id="3d32f-111">2053736</span></span> | <span data-ttu-id="3d32f-112">現在可移至 **發票** > **相關資訊** 存取發票明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3d32f-112">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="3d32f-113">**帳單和定價**</span><span class="sxs-lookup"><span data-stu-id="3d32f-113">**Billing and Pricing**</span></span> | <span data-ttu-id="3d32f-114">2122613</span><span class="sxs-lookup"><span data-stu-id="3d32f-114">2122613</span></span> | <span data-ttu-id="3d32f-115">**啟用** 和 **停用** 動作已從 **價目表** 關聯實體中移除。</span><span class="sxs-lookup"><span data-stu-id="3d32f-115">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="3d32f-116">**帳單和定價**</span><span class="sxs-lookup"><span data-stu-id="3d32f-116">**Billing and Pricing**</span></span> | <span data-ttu-id="3d32f-117">2128606</span><span class="sxs-lookup"><span data-stu-id="3d32f-117">2128606</span></span> | <span data-ttu-id="3d32f-118">解決 **GetEstimatesForProject** 外掛程式中有關 **ullReferenceException** 的問題。</span><span class="sxs-lookup"><span data-stu-id="3d32f-118">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="3d32f-119">**部署和設定**</span><span class="sxs-lookup"><span data-stu-id="3d32f-119">**Deployment and configuration**</span></span> | <span data-ttu-id="3d32f-120">2140569</span><span class="sxs-lookup"><span data-stu-id="3d32f-120">2140569</span></span> | <span data-ttu-id="3d32f-121">不可將 Project 解決方案安裝在 Dataverse Teams 環境中。</span><span class="sxs-lookup"><span data-stu-id="3d32f-121">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="3d32f-122">**部署和設定**</span><span class="sxs-lookup"><span data-stu-id="3d32f-122">**Deployment and configuration**</span></span> | <span data-ttu-id="3d32f-123">2086991</span><span class="sxs-lookup"><span data-stu-id="3d32f-123">2086991</span></span> | <span data-ttu-id="3d32f-124">限制自訂 Web 資源的當地語系化。</span><span class="sxs-lookup"><span data-stu-id="3d32f-124">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="3d32f-125">**商機管理**</span><span class="sxs-lookup"><span data-stu-id="3d32f-125">**Opportunity Management**</span></span> | <span data-ttu-id="3d32f-126">2136794</span><span class="sxs-lookup"><span data-stu-id="3d32f-126">2136794</span></span> | <span data-ttu-id="3d32f-127">在 **確認發票** 或 **將發票標示為已付** 程序失敗時顯示正確的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3d32f-127">Display correct error message when **Confirm invoice** or **Mark invoice as paid** process fails,</span></span> |
| <span data-ttu-id="3d32f-128">**商機管理**</span><span class="sxs-lookup"><span data-stu-id="3d32f-128">**Opportunity Management**</span></span> | <span data-ttu-id="3d32f-129">2146376</span><span class="sxs-lookup"><span data-stu-id="3d32f-129">2146376</span></span> | <span data-ttu-id="3d32f-130">不應收費實際值中已更正的稅金金額是從發票確認所建立。</span><span class="sxs-lookup"><span data-stu-id="3d32f-130">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="3d32f-131">**專案規劃和追蹤**</span><span class="sxs-lookup"><span data-stu-id="3d32f-131">**Project Planning and Tracking**</span></span> | <span data-ttu-id="3d32f-132">2099879</span><span class="sxs-lookup"><span data-stu-id="3d32f-132">2099879</span></span> | <span data-ttu-id="3d32f-133">Dataverse 環境部署必須使用靜態識別碼建立預設交易類別，不可每個環境隨機產生一個類別。</span><span class="sxs-lookup"><span data-stu-id="3d32f-133">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="3d32f-134">**專案規劃和追蹤**</span><span class="sxs-lookup"><span data-stu-id="3d32f-134">**Project Planning and Tracking**</span></span> | <span data-ttu-id="3d32f-135">2128577</span><span class="sxs-lookup"><span data-stu-id="3d32f-135">2128577</span></span> | <span data-ttu-id="3d32f-136">修正 Project Service 使用者權限，以更新資源指派上的交易類別。</span><span class="sxs-lookup"><span data-stu-id="3d32f-136">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="3d32f-137">**專案規劃和追蹤**</span><span class="sxs-lookup"><span data-stu-id="3d32f-137">**Project Planning and Tracking**</span></span> | <span data-ttu-id="3d32f-138">2164035</span><span class="sxs-lookup"><span data-stu-id="3d32f-138">2164035</span></span> | <span data-ttu-id="3d32f-139">修正 **複製專案** 功能的問題。</span><span class="sxs-lookup"><span data-stu-id="3d32f-139">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="3d32f-140">**時間項目**</span><span class="sxs-lookup"><span data-stu-id="3d32f-140">**Time entry**</span></span> | <span data-ttu-id="3d32f-141">2129161</span><span class="sxs-lookup"><span data-stu-id="3d32f-141">2129161</span></span> | <span data-ttu-id="3d32f-142">套用更嚴格的限制，以確保使用者無法變更和更新已提交或核准的時間項目。</span><span class="sxs-lookup"><span data-stu-id="3d32f-142">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="3d32f-143">**時間項目**</span><span class="sxs-lookup"><span data-stu-id="3d32f-143">**Time entry**</span></span> | <span data-ttu-id="3d32f-144">2103572</span><span class="sxs-lookup"><span data-stu-id="3d32f-144">2103572</span></span> | <span data-ttu-id="3d32f-145">非專案時間項目的時間核准不得尋找專案核准者角色。</span><span class="sxs-lookup"><span data-stu-id="3d32f-145">Time approval for non-project time entries must not be looking for project approver role.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]