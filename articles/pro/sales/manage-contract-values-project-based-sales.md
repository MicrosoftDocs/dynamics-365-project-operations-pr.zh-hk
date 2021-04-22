---
title: 專案型合約服務內容概觀
description: 本主題提供有關使用專案型合約服務內容的資訊。
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858185"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="32034-103">專案型合約服務內容概觀</span><span class="sxs-lookup"><span data-stu-id="32034-103">Project-based contract lines overview</span></span>

<span data-ttu-id="32034-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="32034-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="32034-105">Dynamics 365 Project Operations 中的專案型合約服務內容，旨在保留業務開發的專案工作特定元件的估計和計費合約。</span><span class="sxs-lookup"><span data-stu-id="32034-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="32034-106">專案型合約服務內容的結構是針對專案評估和計費案例進行延伸，有下列概念：</span><span class="sxs-lookup"><span data-stu-id="32034-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="32034-107">帳務方式</span><span class="sxs-lookup"><span data-stu-id="32034-107">Billing method</span></span>
- <span data-ttu-id="32034-108">專案和工作對應</span><span class="sxs-lookup"><span data-stu-id="32034-108">Project and task mapping</span></span>
- <span data-ttu-id="32034-109">已包含交易分類</span><span class="sxs-lookup"><span data-stu-id="32034-109">Included transaction classes</span></span>
- <span data-ttu-id="32034-110">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="32034-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="32034-111">可收費率設定</span><span class="sxs-lookup"><span data-stu-id="32034-111">Chargeability setup</span></span>
- <span data-ttu-id="32034-112">使用合約服務內容詳細資料進行估計</span><span class="sxs-lookup"><span data-stu-id="32034-112">Estimates using contract line details</span></span>
- <span data-ttu-id="32034-113">合約服務內容客戶</span><span class="sxs-lookup"><span data-stu-id="32034-113">Contract line customers</span></span>

<span data-ttu-id="32034-114">下表包含專案合約服務內容的 **一般** 索引標籤上的欄位，可協助為專案工作的詳細、基礎估計和帳單安排奠定基礎。</span><span class="sxs-lookup"><span data-stu-id="32034-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="32034-115">欄位</span><span class="sxs-lookup"><span data-stu-id="32034-115">Field</span></span> | <span data-ttu-id="32034-116">描述</span><span class="sxs-lookup"><span data-stu-id="32034-116">Description</span></span> | <span data-ttu-id="32034-117">下游影響</span><span class="sxs-lookup"><span data-stu-id="32034-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="32034-118">**名稱**</span><span class="sxs-lookup"><span data-stu-id="32034-118">**Name**</span></span> | <span data-ttu-id="32034-119">合約服務內容的名稱。</span><span class="sxs-lookup"><span data-stu-id="32034-119">Name of the contract line.</span></span> <span data-ttu-id="32034-120">這可識別所估計合約的獨立元件。</span><span class="sxs-lookup"><span data-stu-id="32034-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="32034-121">對於根據報價建立的專案合約，此值會從專案型報價明細的對應值中複製。</span><span class="sxs-lookup"><span data-stu-id="32034-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="32034-122">在建立發票時，會複製到從此合約服務內容建立的專案發票明細上的名稱。</span><span class="sxs-lookup"><span data-stu-id="32034-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="32034-123">**計費方式**</span><span class="sxs-lookup"><span data-stu-id="32034-123">**Billing Method**</span></span> | <span data-ttu-id="32034-124">對於根據報價建立的專案合約，此值會從報價明細的對應欄位複製。</span><span class="sxs-lookup"><span data-stu-id="32034-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="32034-125">這是一個選項組，代表 Project Operations 所支援的兩種主要合約模型：</span><span class="sxs-lookup"><span data-stu-id="32034-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="32034-126">- **固定價格**</span><span class="sxs-lookup"><span data-stu-id="32034-126">- **Fixed Price**</span></span></br><span data-ttu-id="32034-127">- **時間和資料**</span><span class="sxs-lookup"><span data-stu-id="32034-127">- **Time and Material**</span></span> | <span data-ttu-id="32034-128">根據參考之合約服務內容的計費方式，將處理實際交易。</span><span class="sxs-lookup"><span data-stu-id="32034-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="32034-129">如果實際值參考的合約服務內容有時間和資料計費方式，就會建立成本和未開單銷售實際記錄。</span><span class="sxs-lookup"><span data-stu-id="32034-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="32034-130">如果實際值參考的合約服務內容有固定價格計費方式，則只會建立成本實際值。</span><span class="sxs-lookup"><span data-stu-id="32034-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="32034-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="32034-131">**Project**</span></span> | <span data-ttu-id="32034-132">您可以使用這個欄位來找出用來在此業務開發中傳遞工作的專案。</span><span class="sxs-lookup"><span data-stu-id="32034-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="32034-133">此值將會與 **包含的工作** 及 **包含的交易分類** 搭配使用，以解析實際或估計明細記錄上的合約服務內容參考。</span><span class="sxs-lookup"><span data-stu-id="32034-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="32034-134">**包含的工作**</span><span class="sxs-lookup"><span data-stu-id="32034-134">**Included Tasks**</span></span> | <span data-ttu-id="32034-135">表示此合約服務內容是否包含所選取專案的所有專案工作，或只包含部分工作。</span><span class="sxs-lookup"><span data-stu-id="32034-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="32034-136">這是選項組，其可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="32034-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="32034-137">- **所有專案工作**</span><span class="sxs-lookup"><span data-stu-id="32034-137">- **All Project Tasks**</span></span></br><span data-ttu-id="32034-138">- - **僅限選取的專案工作**。</span><span class="sxs-lookup"><span data-stu-id="32034-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="32034-139">此欄位中的空白值等於選取 **所有專案工作**。</span><span class="sxs-lookup"><span data-stu-id="32034-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="32034-140">如果選取 **僅限選取的工作**，您可以選取特定工作，並在 **專案** 頁面的 **工作帳單設定** 索引標籤上，將它們關聯至此合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="32034-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="32034-141">此值將與 **專案** 及 **包含的交易** 類別搭配使用，以解析實際值或估計明細記錄上的合約服務內容參考。</span><span class="sxs-lookup"><span data-stu-id="32034-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="32034-142">**包括時間**</span><span class="sxs-lookup"><span data-stu-id="32034-142">**Include Time**</span></span> | <span data-ttu-id="32034-143">**是**/**否** 值表示此合約服務內容中是否包含所選專案的時間交易或人力成本。</span><span class="sxs-lookup"><span data-stu-id="32034-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="32034-144">**否** 值表示時間交易或人力成本不會包括在此合約服務內容上。</span><span class="sxs-lookup"><span data-stu-id="32034-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="32034-145">**是** 值表示會包含。</span><span class="sxs-lookup"><span data-stu-id="32034-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="32034-146">此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。</span><span class="sxs-lookup"><span data-stu-id="32034-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="32034-147">**包括費用**</span><span class="sxs-lookup"><span data-stu-id="32034-147">**Include Expense**</span></span> | <span data-ttu-id="32034-148">**是**/**否** 值表示此合約服務內容中是否包含所選專案的費用成本。</span><span class="sxs-lookup"><span data-stu-id="32034-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="32034-149">**否** 值表示費用成本不會包括在此合約服務內容上。</span><span class="sxs-lookup"><span data-stu-id="32034-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="32034-150">**是** 值表示會包含。</span><span class="sxs-lookup"><span data-stu-id="32034-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="32034-151">此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。</span><span class="sxs-lookup"><span data-stu-id="32034-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="32034-152">**包含的材料**</span><span class="sxs-lookup"><span data-stu-id="32034-152">**Include Materials**</span></span> | <span data-ttu-id="32034-153">**是**/**否** 值表示此合約服務內容中是否包含所選專案的材料成本。</span><span class="sxs-lookup"><span data-stu-id="32034-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="32034-154">**否** 值表示此合約服務內容中將不包含所選專案的材料成本。</span><span class="sxs-lookup"><span data-stu-id="32034-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="32034-155">**是** 值表示會包含。</span><span class="sxs-lookup"><span data-stu-id="32034-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="32034-156">此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。</span><span class="sxs-lookup"><span data-stu-id="32034-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="32034-157">**包括服務費**</span><span class="sxs-lookup"><span data-stu-id="32034-157">**Include Fee**</span></span> | <span data-ttu-id="32034-158">**是**/**否** 值表示此合約服務內容中是否包含所選專案的服務費成本。</span><span class="sxs-lookup"><span data-stu-id="32034-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="32034-159">**否** 值表示服務費不會包括在此合約服務內容上。</span><span class="sxs-lookup"><span data-stu-id="32034-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="32034-160">**是** 值表示會包含。</span><span class="sxs-lookup"><span data-stu-id="32034-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="32034-161">此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。</span><span class="sxs-lookup"><span data-stu-id="32034-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="32034-162">**合約金額**</span><span class="sxs-lookup"><span data-stu-id="32034-162">**Contracted Amount**</span></span> | <span data-ttu-id="32034-163">在固定價格合約服務內容上，此金額是已同意的值，將針對與此合約服務內容相關聯的所有工作元件，開發票給客戶。</span><span class="sxs-lookup"><span data-stu-id="32034-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="32034-164">在時間和資料合約服務內容上，此金額是估計值，將針對與此合約服務內容相關聯的所有工作元件，開發票給客戶。</span><span class="sxs-lookup"><span data-stu-id="32034-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="32034-165">對於根據報價建立的專案合約，此值會從報價明細的對應欄位複製。</span><span class="sxs-lookup"><span data-stu-id="32034-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="32034-166">當專案型合約服務內容有明細詳細資料時，會鎖定此欄位不予編輯，並根據合約服務內容詳細資料的金額進行匯總。</span><span class="sxs-lookup"><span data-stu-id="32034-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="32034-167">當合約服務內容有明細詳細資料時，可變更明細詳細資料的金額，以修改此值。</span><span class="sxs-lookup"><span data-stu-id="32034-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="32034-168">在固定價格合約服務內容上，此值是用來產生週期帳單里程碑上的稅前金額。</span><span class="sxs-lookup"><span data-stu-id="32034-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="32034-169">**估計稅額**</span><span class="sxs-lookup"><span data-stu-id="32034-169">**Estimated Tax**</span></span> | <span data-ttu-id="32034-170">使用者可以編輯此欄位，以在合約服務內容上輸入估計的稅額。</span><span class="sxs-lookup"><span data-stu-id="32034-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="32034-171">當專案型合約服務內容有明細詳細資料時，會鎖定此欄位不予編輯，並根據合約服務內容詳細資料的稅額進行匯總。</span><span class="sxs-lookup"><span data-stu-id="32034-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="32034-172">當合約服務內容有明細詳細資料時，可變更明細詳細資料的稅額，以修改此值。</span><span class="sxs-lookup"><span data-stu-id="32034-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="32034-173">在固定價格合約服務內容上，此值是用來產生週期帳單里程碑上的稅金。</span><span class="sxs-lookup"><span data-stu-id="32034-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="32034-174">**稅後合約金額**</span><span class="sxs-lookup"><span data-stu-id="32034-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="32034-175">稅後合約服務內容金額。</span><span class="sxs-lookup"><span data-stu-id="32034-175">The contract line amount after tax.</span></span> <span data-ttu-id="32034-176">此欄位為唯讀，其計算方式為 **合約金額 + 稅金**。</span><span class="sxs-lookup"><span data-stu-id="32034-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="32034-177">在固定價格合約服務內容上，此值是用來產生週期帳單里程碑。</span><span class="sxs-lookup"><span data-stu-id="32034-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="32034-178">**不得超過限制**</span><span class="sxs-lookup"><span data-stu-id="32034-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="32034-179">使用者可以編輯此欄位，而此欄位只能用於將計費方式設定為時間與資料的專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="32034-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="32034-180">使用者可以編輯此欄位。</span><span class="sxs-lookup"><span data-stu-id="32034-180">The user can edit this field.</span></span> <span data-ttu-id="32034-181">當時間和資料的實際值參考此合約服務內容的時間和資料時，實際值的金額會根據合約服務內容的不得超過限制進行評估。</span><span class="sxs-lookup"><span data-stu-id="32034-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="32034-182">在考慮已經花費和認可的金額之後，完成此評估。</span><span class="sxs-lookup"><span data-stu-id="32034-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="32034-183">**客戶預算**</span><span class="sxs-lookup"><span data-stu-id="32034-183">**Customer Budget**</span></span> | <span data-ttu-id="32034-184">如果合約是從報價建立的，則此欄位可編輯，並從報價明細的對應欄位複製。</span><span class="sxs-lookup"><span data-stu-id="32034-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="32034-185">此欄位只用於提供資訊，對下游沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="32034-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="32034-186">專案型合約服務內容的一般索引標籤的選項驗證規則</span><span class="sxs-lookup"><span data-stu-id="32034-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="32034-187">規則 1：如果 **包含的工作** 欄位為空白，或設為 **所有專案工作**，則專案的所有工作都會包括在合約服務內容上。</span><span class="sxs-lookup"><span data-stu-id="32034-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="32034-188">規則 2：當 **包含的工作** 欄位空白或將已明確設定為 **所有專案工作** 時，專案和特定交易類別只能包含於合約的一個專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="32034-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="32034-189">規則 3：當 **包含的工作** 欄位設定為 **僅限選取的專案工作** 時，專案和特定交易類別可以包含於合約的多個專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="32034-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="32034-190">
                    <strong>合約</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32034-191">
                    <strong>合約服務內容</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="32034-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="32034-193">
                    <strong>包含的工作</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="32034-194">
                    <strong>包括時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="32034-195">
                    <strong>包括費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="32034-196">
                    <strong>包含的材料</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="32034-197">
                    <strong>包括​​</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="32034-198">
                    <strong>費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="32034-199">
                    <strong>有效/無效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="32034-200">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32034-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-201">C1</span><span class="sxs-lookup"><span data-stu-id="32034-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-202">CL1</span><span class="sxs-lookup"><span data-stu-id="32034-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-203">P1</span><span class="sxs-lookup"><span data-stu-id="32034-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-204">空白</span><span class="sxs-lookup"><span data-stu-id="32034-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-205">.是</span><span class="sxs-lookup"><span data-stu-id="32034-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-206">.是</span><span class="sxs-lookup"><span data-stu-id="32034-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-207">.是</span><span class="sxs-lookup"><span data-stu-id="32034-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-208">.是</span><span class="sxs-lookup"><span data-stu-id="32034-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-209">無效</span><span class="sxs-lookup"><span data-stu-id="32034-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-210">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="32034-210">Violation of Rule #2.</span></span> <span data-ttu-id="32034-211">P1 專案的時間、費用、材料和服務費包含在合約服務內容 CL1 及 CL2 中。</span><span class="sxs-lookup"><span data-stu-id="32034-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-212">C1</span><span class="sxs-lookup"><span data-stu-id="32034-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-213">CL2</span><span class="sxs-lookup"><span data-stu-id="32034-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-214">P1</span><span class="sxs-lookup"><span data-stu-id="32034-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-215">空白</span><span class="sxs-lookup"><span data-stu-id="32034-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-216">.是</span><span class="sxs-lookup"><span data-stu-id="32034-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-217">.是</span><span class="sxs-lookup"><span data-stu-id="32034-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-218">.是</span><span class="sxs-lookup"><span data-stu-id="32034-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-219">.是</span><span class="sxs-lookup"><span data-stu-id="32034-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-220">C1</span><span class="sxs-lookup"><span data-stu-id="32034-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-221">CL1</span><span class="sxs-lookup"><span data-stu-id="32034-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-222">P1</span><span class="sxs-lookup"><span data-stu-id="32034-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-223">空白</span><span class="sxs-lookup"><span data-stu-id="32034-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-224">.是</span><span class="sxs-lookup"><span data-stu-id="32034-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-225">無</span><span class="sxs-lookup"><span data-stu-id="32034-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-226">.是</span><span class="sxs-lookup"><span data-stu-id="32034-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-227">.是</span><span class="sxs-lookup"><span data-stu-id="32034-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-228">無效</span><span class="sxs-lookup"><span data-stu-id="32034-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-229">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="32034-229">Violation of Rule #2.</span></span> <span data-ttu-id="32034-230">P1 專案的時間、材料和服務費包含在合約服務內容 CL1 及 CL2 中。</span><span class="sxs-lookup"><span data-stu-id="32034-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-231">C1</span><span class="sxs-lookup"><span data-stu-id="32034-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-232">CL2</span><span class="sxs-lookup"><span data-stu-id="32034-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-233">P1</span><span class="sxs-lookup"><span data-stu-id="32034-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-234">空白</span><span class="sxs-lookup"><span data-stu-id="32034-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-235">.是</span><span class="sxs-lookup"><span data-stu-id="32034-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-236">.是</span><span class="sxs-lookup"><span data-stu-id="32034-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-237">.是</span><span class="sxs-lookup"><span data-stu-id="32034-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-238">.是</span><span class="sxs-lookup"><span data-stu-id="32034-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-239">C1</span><span class="sxs-lookup"><span data-stu-id="32034-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-240">CL1</span><span class="sxs-lookup"><span data-stu-id="32034-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-241">P1</span><span class="sxs-lookup"><span data-stu-id="32034-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-242">空白</span><span class="sxs-lookup"><span data-stu-id="32034-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-243">.是</span><span class="sxs-lookup"><span data-stu-id="32034-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-244">無</span><span class="sxs-lookup"><span data-stu-id="32034-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-245">.是</span><span class="sxs-lookup"><span data-stu-id="32034-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-246">.是</span><span class="sxs-lookup"><span data-stu-id="32034-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-247">有效</span><span class="sxs-lookup"><span data-stu-id="32034-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-248">P1 專案的時間、材料和服務費包含在 CL1 中。</span><span class="sxs-lookup"><span data-stu-id="32034-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="32034-249">P1 專案上的費用已包含在 CL2 中。</span><span class="sxs-lookup"><span data-stu-id="32034-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="32034-250">每個合約服務內容所包含的內容之間沒有任何重疊，因此有效。</span><span class="sxs-lookup"><span data-stu-id="32034-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-251">C1</span><span class="sxs-lookup"><span data-stu-id="32034-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-252">CL2</span><span class="sxs-lookup"><span data-stu-id="32034-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-253">P1</span><span class="sxs-lookup"><span data-stu-id="32034-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-254">空白</span><span class="sxs-lookup"><span data-stu-id="32034-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-255">無</span><span class="sxs-lookup"><span data-stu-id="32034-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-256">.是</span><span class="sxs-lookup"><span data-stu-id="32034-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-257">無</span><span class="sxs-lookup"><span data-stu-id="32034-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-258">無</span><span class="sxs-lookup"><span data-stu-id="32034-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-259">C1</span><span class="sxs-lookup"><span data-stu-id="32034-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-260">CL1</span><span class="sxs-lookup"><span data-stu-id="32034-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-261">P1</span><span class="sxs-lookup"><span data-stu-id="32034-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-262">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="32034-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-263">.是</span><span class="sxs-lookup"><span data-stu-id="32034-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-264">.是</span><span class="sxs-lookup"><span data-stu-id="32034-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-265">.是</span><span class="sxs-lookup"><span data-stu-id="32034-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-266">.是</span><span class="sxs-lookup"><span data-stu-id="32034-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-267">無效</span><span class="sxs-lookup"><span data-stu-id="32034-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-268">違反規則 #2</span><span class="sxs-lookup"><span data-stu-id="32034-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="32034-269">C1 包含專案 P1 上工作子集的時間、材料、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="32034-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="32034-270">CL2 包含整個專案 P1 的時間、材料、費用和服務費，因此與 C1 中所包含的內容重疊。</span><span class="sxs-lookup"><span data-stu-id="32034-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-271">C1</span><span class="sxs-lookup"><span data-stu-id="32034-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-272">CL2</span><span class="sxs-lookup"><span data-stu-id="32034-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-273">P1</span><span class="sxs-lookup"><span data-stu-id="32034-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-274">空白</span><span class="sxs-lookup"><span data-stu-id="32034-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-275">.是</span><span class="sxs-lookup"><span data-stu-id="32034-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-276">.是</span><span class="sxs-lookup"><span data-stu-id="32034-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-277">.是</span><span class="sxs-lookup"><span data-stu-id="32034-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-278">.是</span><span class="sxs-lookup"><span data-stu-id="32034-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-279">C1</span><span class="sxs-lookup"><span data-stu-id="32034-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-280">CL1</span><span class="sxs-lookup"><span data-stu-id="32034-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-281">P1</span><span class="sxs-lookup"><span data-stu-id="32034-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-282">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="32034-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-283">.是</span><span class="sxs-lookup"><span data-stu-id="32034-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-284">.是</span><span class="sxs-lookup"><span data-stu-id="32034-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-285">.是</span><span class="sxs-lookup"><span data-stu-id="32034-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-286">.是</span><span class="sxs-lookup"><span data-stu-id="32034-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-287">有效</span><span class="sxs-lookup"><span data-stu-id="32034-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="32034-288">根據規則 3</span><span class="sxs-lookup"><span data-stu-id="32034-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="32034-289">C1 包含專案 P1 上工作子集的時間、材料、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="32034-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="32034-290">CL2 包含專案 P1 的工作子集的時間、材料、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="32034-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="32034-291">唯一的額外驗證是要求 CL1 上的工作子集與 CL2 上的工作子集不同，以確保其間沒有任何重疊。</span><span class="sxs-lookup"><span data-stu-id="32034-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="32034-292">建立與工作的關聯時，系統會完成此作業。</span><span class="sxs-lookup"><span data-stu-id="32034-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="32034-293">C1</span><span class="sxs-lookup"><span data-stu-id="32034-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32034-294">CL2</span><span class="sxs-lookup"><span data-stu-id="32034-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-295">P1</span><span class="sxs-lookup"><span data-stu-id="32034-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="32034-296">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="32034-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-297">.是</span><span class="sxs-lookup"><span data-stu-id="32034-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="32034-298">.是</span><span class="sxs-lookup"><span data-stu-id="32034-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-299">.是</span><span class="sxs-lookup"><span data-stu-id="32034-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="32034-300">.是</span><span class="sxs-lookup"><span data-stu-id="32034-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
