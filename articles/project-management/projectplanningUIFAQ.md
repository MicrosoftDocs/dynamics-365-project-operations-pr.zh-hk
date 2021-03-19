---
title: 在工作窗格中工作時的疑難排解
description: 本主題提供在工作窗格中工作時所需的疑難排解資訊。
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286590"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="4a0f5-103">在工作窗格中工作時的疑難排解</span><span class="sxs-lookup"><span data-stu-id="4a0f5-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="4a0f5-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="4a0f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4a0f5-105">本主題說明如何修正您使用成本管理時可能遇到的問題。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="4a0f5-106">啟用 Cookie</span><span class="sxs-lookup"><span data-stu-id="4a0f5-106">Enable cookies</span></span>

<span data-ttu-id="4a0f5-107">Project Operations 需要啟用第三方 Cookie，以便呈現分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="4a0f5-108">如果未啟用第三方 Cookie，當您在 **專案** 頁面上選取 **工作** 索引標籤時，看到的不是工作，而是空白頁面。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![未啟用第三方 Cookie 時的空白索引標籤](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="4a0f5-110">因應措施</span><span class="sxs-lookup"><span data-stu-id="4a0f5-110">Workaround</span></span>
<span data-ttu-id="4a0f5-111">對於 Microsoft Edge或 Google Chrome 瀏覽器，下列程式概述如何更新瀏覽器設定以啟用第三方 Cookie。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="4a0f5-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a0f5-112">Microsoft Edge</span></span>

1. <span data-ttu-id="4a0f5-113">開啟 Edge 瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="4a0f5-114">選取右上角的 **省略符號** (...)，然後選取 **設定**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="4a0f5-115">在 **Cookie 和網站權限** 底下，選取 **Cookie 和網站資料**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="4a0f5-116">關閉 **封鎖第三方 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="4a0f5-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="4a0f5-117">Google Chrome</span></span>

1. <span data-ttu-id="4a0f5-118">開啟 Chrome 瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="4a0f5-119">選取右上角的三個垂直點，然後選取 **設定**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="4a0f5-120">在 **隱私權和安全性** 底下，選取 **Cookie 和其他網站資料**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="4a0f5-121">選取 **允許所有 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a0f5-122">如果您封鎖第三方 Cookie，其他網站的所有 Cookie 和網站資料也都會遭到封鎖，即使您的例外清單中允許該網站也一樣。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="4a0f5-123">PEX 端點</span><span class="sxs-lookup"><span data-stu-id="4a0f5-123">PEX Endpoint</span></span>

<span data-ttu-id="4a0f5-124">Project Operations 需要專案參數參照 PEX 端點。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="4a0f5-125">必須有此端點，才能與用於呈現分工結構圖的服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="4a0f5-126">如果未啟用此參數，您就會收到「專案參數無效」錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="4a0f5-127">因應措施</span><span class="sxs-lookup"><span data-stu-id="4a0f5-127">Workaround</span></span>
 ![專案參數上的 PEX 端點欄位](media/projectparameter.png)

1. <span data-ttu-id="4a0f5-129">將 **PEX 端點** 欄位新增至 **專案參數** 頁面。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="4a0f5-130">以下列值來更新欄位：`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="4a0f5-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="4a0f5-131">從 **專案參數** 頁面移除欄位。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="4a0f5-132">Project 網頁版的權限</span><span class="sxs-lookup"><span data-stu-id="4a0f5-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="4a0f5-133">Project Operations 需要依賴外部排程服務。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="4a0f5-134">此服務要求使用者必須已獲指派數個可讀取和寫入與分工結構圖相關之實體的角色。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="4a0f5-135">這些實體包括專案工作、資源指派和工作相依性。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="4a0f5-136">如果使用者移至 **工作** 索引標籤時無法呈現分工結構圖，可能是因為尚未啟用 Project Operations 適用的 Project。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="4a0f5-137">使用者可能會收到資訊安全角色錯誤，或收到與拒絕存取相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="4a0f5-138">因應措施</span><span class="sxs-lookup"><span data-stu-id="4a0f5-138">Workaround</span></span>

1. <span data-ttu-id="4a0f5-139">移至 **設定 > 安全性 > 使用者 > 應用程式使用者**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![應用程式記錄](media/applicationuser.jpg)
   
2. <span data-ttu-id="4a0f5-141">按兩下應用程式使用者記錄，以驗證：</span><span class="sxs-lookup"><span data-stu-id="4a0f5-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="4a0f5-142">使用者可以存取專案。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-142">The user has access to the project.</span></span> <span data-ttu-id="4a0f5-143">這項驗證通常是透過確定使用者具備 **專案經理** 資訊安全角色來完成。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="4a0f5-144">Microsoft Project 應用程式使用者存在且已正確設定。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="4a0f5-145">如果此使用者不存在，您可以建立新的使用者記錄。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="4a0f5-146">選取 **新增使用者**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-146">Select **New Users**.</span></span> <span data-ttu-id="4a0f5-147">將輸入表單變更至 **應用程式使用者**，然後新增 **應用程式識別碼**。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![應用程式使用者詳細資料](media/applicationuserdetails.jpg)

4. <span data-ttu-id="4a0f5-149">確認是否已將正確的授權指派給使用者，以及已在授權的服務方案詳細資料中啟用該服務。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="4a0f5-150">確認使用者是否可以開啟 project.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="4a0f5-151">透過專案參數確認系統是否指向正確的專案端點。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="4a0f5-152">確認是否已建立 Project 應用程式使用者。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="4a0f5-153">將下列資訊安全角色套用至使用者：</span><span class="sxs-lookup"><span data-stu-id="4a0f5-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="4a0f5-154">Dataverse 使用者</span><span class="sxs-lookup"><span data-stu-id="4a0f5-154">Dataverse User</span></span>
  - <span data-ttu-id="4a0f5-155">Project Operations 系統</span><span class="sxs-lookup"><span data-stu-id="4a0f5-155">Project Operations System</span></span>
  - <span data-ttu-id="4a0f5-156">Project 系統</span><span class="sxs-lookup"><span data-stu-id="4a0f5-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="4a0f5-157">更新分工結構圖時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="4a0f5-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="4a0f5-158">對分工結構圖進行一項或多項更新時，變更最終會失敗且不會儲存。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="4a0f5-159">排程窗格中發生錯誤，指出「無法儲存您最近所做的變更」。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="4a0f5-160">因應措施</span><span class="sxs-lookup"><span data-stu-id="4a0f5-160">Workaround</span></span>

1. <span data-ttu-id="4a0f5-161">確認是否已將正確的授權指派給使用者，以及已在授權的服務方案詳細資料中啟用該服務。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="4a0f5-162">確認使用者是否可以開啟 project.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="4a0f5-163">確認系統是否指向正確的專案端點。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="4a0f5-164">確認是否已建立 Project 應用程式使用者。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="4a0f5-165">將下列資訊安全角色套用至使用者：</span><span class="sxs-lookup"><span data-stu-id="4a0f5-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="4a0f5-166">Dataverse 使用者或基本使用者</span><span class="sxs-lookup"><span data-stu-id="4a0f5-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="4a0f5-167">Project Operations 系統</span><span class="sxs-lookup"><span data-stu-id="4a0f5-167">Project Operations System</span></span>
  - <span data-ttu-id="4a0f5-168">Project 系統</span><span class="sxs-lookup"><span data-stu-id="4a0f5-168">Project System</span></span>
  - <span data-ttu-id="4a0f5-169">Project Operations 雙重寫入系統 (如果您要部署資源/非庫存型案例適用的 Project Operations，就必須有此角色)。</span><span class="sxs-lookup"><span data-stu-id="4a0f5-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]