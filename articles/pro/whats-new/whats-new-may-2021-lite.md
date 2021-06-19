---
title: 2021 年 5 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 2021 年 5 月所發行 Project Operations 精簡部署中提供之品質更新的資訊。
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060460"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a><span data-ttu-id="5b8e1-103">2021 年 5 月新增功能 - Project Operations 精簡部署</span><span class="sxs-lookup"><span data-stu-id="5b8e1-103">What's new May 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="5b8e1-104">_適用於：精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5b8e1-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b8e1-105">此主題適用於下列 Dynamics 365 Project Operations 元件和版本：</span><span class="sxs-lookup"><span data-stu-id="5b8e1-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

   - <span data-ttu-id="5b8e1-106">Dataverse 環境 4.10.0.186 版上的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-106">Project Operations on Dataverse environment version 4.10.0.186.</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="5b8e1-107">此版本包含的功能</span><span class="sxs-lookup"><span data-stu-id="5b8e1-107">Features included in this release</span></span>

<span data-ttu-id="5b8e1-108">此版本包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="5b8e1-108">The following features are included in this release:</span></span>

- <span data-ttu-id="5b8e1-109">[排程模式](../../project-management/scheduling-modes.md)：專案經理現在可以規定管理專案時所應使用的是固定期間、固定工時還是固定單位排程模式。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-109">[Scheduling modes](../../project-management/scheduling-modes.md): Project managers can now define if a project should be managed using a fixed duration, fixed work, or fixed units scheduling mode.</span></span>

## <a name="quality-updates"></a><span data-ttu-id="5b8e1-110">品質更新</span><span class="sxs-lookup"><span data-stu-id="5b8e1-110">Quality updates</span></span>

| <span data-ttu-id="5b8e1-111">**功能區域**</span><span class="sxs-lookup"><span data-stu-id="5b8e1-111">**Feature area**</span></span> | <span data-ttu-id="5b8e1-112">**參考編號**</span><span class="sxs-lookup"><span data-stu-id="5b8e1-112">**Reference number**</span></span> | <span data-ttu-id="5b8e1-113">**品質更新**</span><span class="sxs-lookup"><span data-stu-id="5b8e1-113">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5b8e1-114">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="5b8e1-114">Billing and pricing</span></span> | <span data-ttu-id="5b8e1-115">2224568</span><span class="sxs-lookup"><span data-stu-id="5b8e1-115">2224568</span></span> | <span data-ttu-id="5b8e1-116">新增邏輯，以啟用涉及叫用發票確認外掛程式的自訂。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-116">Added logic to enable customizations that involve invoking the invoice confirmation plug-in.</span></span> |
| <span data-ttu-id="5b8e1-117">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="5b8e1-117">Billing and pricing</span></span> | <span data-ttu-id="5b8e1-118">2101098</span><span class="sxs-lookup"><span data-stu-id="5b8e1-118">2101098</span></span> | <span data-ttu-id="5b8e1-119">改善預估發票預設欄位的邏輯。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-119">Improved the logic of default fields to proforma invoice.</span></span> <span data-ttu-id="5b8e1-120">這些欄位包括 **帳單地址**、**帳單姓名** 和 **付款條款**。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-120">These fields include, **Bill-to address**, **Bill to name**, and **Payment terms**.</span></span> <span data-ttu-id="5b8e1-121">此欄位現在預設會根據對應的專案合約客戶記錄來設定。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-121">The fields now default from the corresponding project contract customer record.</span></span> |
| <span data-ttu-id="5b8e1-122">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="5b8e1-122">Billing and pricing</span></span> | <span data-ttu-id="5b8e1-123">2021413</span><span class="sxs-lookup"><span data-stu-id="5b8e1-123">2021413</span></span> | <span data-ttu-id="5b8e1-124">更新 **工作** 實體的 **實際成本** 與 **銷售** 欄位，以包含工作上未開單及已開單費用中的銷售值。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-124">Updated the **Actual cost** and **Sales** fields on the **Task** entity to include sales values from unbilled and billed expenses on tasks.</span></span> |
| <span data-ttu-id="5b8e1-125">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="5b8e1-125">Billing and pricing</span></span> | <span data-ttu-id="5b8e1-126">2182110</span><span class="sxs-lookup"><span data-stu-id="5b8e1-126">2182110</span></span> | <span data-ttu-id="5b8e1-127">複製專案合約時，目的地專案合約中會重新產生合約服務內容，以確保其唯一性。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-127">When copying a project contract, the contract line ID is regenerated in the destination project contract to ensure it's unique.</span></span> |
| <span data-ttu-id="5b8e1-128">商機管理</span><span class="sxs-lookup"><span data-stu-id="5b8e1-128">Opportunity Management</span></span> | <span data-ttu-id="5b8e1-129">2186741</span><span class="sxs-lookup"><span data-stu-id="5b8e1-129">2186741</span></span> | <span data-ttu-id="5b8e1-130">新增驗證，以確保無法更新現有報價明細詳細資料上的 **來源** 欄位和交易類型。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-130">Added validations to ensure the **Origin** field and transaction type can't be updated on existing quote line details.</span></span> |
| <span data-ttu-id="5b8e1-131">商機管理</span><span class="sxs-lookup"><span data-stu-id="5b8e1-131">Opportunity Management</span></span> | <span data-ttu-id="5b8e1-132">2191353</span><span class="sxs-lookup"><span data-stu-id="5b8e1-132">2191353</span></span> | <span data-ttu-id="5b8e1-133">不得允許在時間和材料合約服務內容上建立里程碑。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-133">Milestone creation must not be allowed on a time and material contract line.</span></span> |
| <span data-ttu-id="5b8e1-134">商機管理</span><span class="sxs-lookup"><span data-stu-id="5b8e1-134">Opportunity Management</span></span> | <span data-ttu-id="5b8e1-135">2216956</span><span class="sxs-lookup"><span data-stu-id="5b8e1-135">2216956</span></span> | <span data-ttu-id="5b8e1-136">修正 **更新價格** 的問題。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-136">Fixed issues with **Update prices**.</span></span> |
| <span data-ttu-id="5b8e1-137">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-137">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-138">2182979</span><span class="sxs-lookup"><span data-stu-id="5b8e1-138">2182979</span></span> | <span data-ttu-id="5b8e1-139">專案複製功能已改善，可確保費用估計明細是從原始專案複製而來。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-139">Project copy function improved to ensure that expense estimate lines are copied from the original project.</span></span> |
| <span data-ttu-id="5b8e1-140">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-140">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-141">2184144</span><span class="sxs-lookup"><span data-stu-id="5b8e1-141">2184144</span></span> | <span data-ttu-id="5b8e1-142">專案複製功能已改善，可確保資源職位名稱是從原始專案複製而來。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-142">Project copy function improved to ensure the resource position name is copied from the original project.</span></span> |
| <span data-ttu-id="5b8e1-143">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-143">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-144">2184799</span><span class="sxs-lookup"><span data-stu-id="5b8e1-144">2184799</span></span> | <span data-ttu-id="5b8e1-145">加強複製專案時的控制，以確保正在進行複製時無法變更估計開始日期。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-145">Tightened the control when copying a project to ensure the estimated start date can't be changed while the copy is in progress.</span></span> |
| <span data-ttu-id="5b8e1-146">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-146">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-147">2185134</span><span class="sxs-lookup"><span data-stu-id="5b8e1-147">2185134</span></span> | <span data-ttu-id="5b8e1-148">進行專案複製時，目的地專案估計開始日期已設定為今天的日期。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-148">During the copy of a project, the destination project estimated start date is set to today's date.</span></span> |
| <span data-ttu-id="5b8e1-149">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-149">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-150">2196373</span><span class="sxs-lookup"><span data-stu-id="5b8e1-150">2196373</span></span> | <span data-ttu-id="5b8e1-151">複製專案時，確保專案經理和團隊成員記錄在專案團隊中不會重複。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-151">Ensure project manager and team member records are not duplicated in the project team when copying a project.</span></span> |
| <span data-ttu-id="5b8e1-152">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-152">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-153">2211833</span><span class="sxs-lookup"><span data-stu-id="5b8e1-153">2211833</span></span> | <span data-ttu-id="5b8e1-154">資源指派會從源專案工作複製到目的地專案。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-154">Resource assignments are copied from the source project task to the destination project.</span></span> |
| <span data-ttu-id="5b8e1-155">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-155">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-156">2186541</span><span class="sxs-lookup"><span data-stu-id="5b8e1-156">2186541</span></span> | <span data-ttu-id="5b8e1-157">修正 **估計值** 網格依 **資源** 分組時發生的問題。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-157">Fixed issues in the **Estimates** grid when grouping by **Resource**.</span></span> |
| <span data-ttu-id="5b8e1-158">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="5b8e1-158">Planning and Tracking</span></span> | <span data-ttu-id="5b8e1-159">2166906</span><span class="sxs-lookup"><span data-stu-id="5b8e1-159">2166906</span></span> | <span data-ttu-id="5b8e1-160">工作中的交易類別必須已複製到 **資源指派** 實體。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-160">The transaction category from a task must be copied to the **Resource assignment** entity.</span></span> |
| <span data-ttu-id="5b8e1-161">資源管理</span><span class="sxs-lookup"><span data-stu-id="5b8e1-161">Resource Management</span></span> | <span data-ttu-id="5b8e1-162">2125362</span><span class="sxs-lookup"><span data-stu-id="5b8e1-162">2125362</span></span> | <span data-ttu-id="5b8e1-163">修正使用根據工作時數配置方法建立一般團隊成員的問題。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-163">Fixed issues with creating a generic team member using the hours-based allocation method.</span></span> |
| <span data-ttu-id="5b8e1-164">時間和費用</span><span class="sxs-lookup"><span data-stu-id="5b8e1-164">Time and Expense</span></span> | <span data-ttu-id="5b8e1-165">2113603</span><span class="sxs-lookup"><span data-stu-id="5b8e1-165">2113603</span></span> | <span data-ttu-id="5b8e1-166">修正從 **時間項目** 頁面中移除屬性的自訂相關問題。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-166">Fixed customization-related issue with removing attributes from the **Time entry** page.</span></span> <span data-ttu-id="5b8e1-167">系統會先檢查頁面上是否有該屬性，再使用指令碼來存取屬性。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-167">The system checks if the attribute exists on the page before accessing the attribute by using a script.</span></span> |
| <span data-ttu-id="5b8e1-168">時間和費用</span><span class="sxs-lookup"><span data-stu-id="5b8e1-168">Time and Expense</span></span> | <span data-ttu-id="5b8e1-169">2204377</span><span class="sxs-lookup"><span data-stu-id="5b8e1-169">2204377</span></span> | <span data-ttu-id="5b8e1-170">選取 **複製週次** 時，必須自動顯示已複製的工時表。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-170">Copied timesheets must show automatically when you select **Copy Week**.</span></span> |
| <span data-ttu-id="5b8e1-171">時間和費用</span><span class="sxs-lookup"><span data-stu-id="5b8e1-171">Time and Expense</span></span> | <span data-ttu-id="5b8e1-172">2209059</span><span class="sxs-lookup"><span data-stu-id="5b8e1-172">2209059</span></span> | <span data-ttu-id="5b8e1-173">Dynamics 365 Field Service 時間項目的 **狀態** 欄位是可編輯的。</span><span class="sxs-lookup"><span data-stu-id="5b8e1-173">The **Status** field is editable for Dynamics 365 Field Service time entries.</span></span> |