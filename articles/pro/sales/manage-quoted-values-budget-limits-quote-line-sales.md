---
title: 專案型報價明細概觀 - 精簡
description: 本主題提供有關將專案型報價明細用於專案工作的資訊。 (專業版)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273000"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="d9175-104">專案型報價明細概觀 - 精簡</span><span class="sxs-lookup"><span data-stu-id="d9175-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="d9175-105">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d9175-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d9175-106">專案型報價明細是為了協助在業務開發上估計專案工作而設計。</span><span class="sxs-lookup"><span data-stu-id="d9175-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d9175-107">專案型報價明細的結構已運用下列概念針對專案估計值進行擴充：</span><span class="sxs-lookup"><span data-stu-id="d9175-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d9175-108">計費方式</span><span class="sxs-lookup"><span data-stu-id="d9175-108">Billing Method</span></span>
- <span data-ttu-id="d9175-109">專案和工作對應</span><span class="sxs-lookup"><span data-stu-id="d9175-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d9175-110">已包含交易分類</span><span class="sxs-lookup"><span data-stu-id="d9175-110">Included Transaction classes</span></span>
- <span data-ttu-id="d9175-111">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="d9175-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d9175-112">可收費率設定</span><span class="sxs-lookup"><span data-stu-id="d9175-112">Chargeability setup</span></span>
- <span data-ttu-id="d9175-113">使用報價明細詳細資料的估計</span><span class="sxs-lookup"><span data-stu-id="d9175-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d9175-114">報價明細客戶</span><span class="sxs-lookup"><span data-stu-id="d9175-114">Quote line Customers</span></span>

<span data-ttu-id="d9175-115">下表提供有關專案型報價明細的 **一般** 索引標籤上的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="d9175-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d9175-116">這些欄位可協助為專案工作設定詳細的全新估計基礎。</span><span class="sxs-lookup"><span data-stu-id="d9175-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d9175-117">**欄位**</span><span class="sxs-lookup"><span data-stu-id="d9175-117">**Field**</span></span> | <span data-ttu-id="d9175-118">**描述**</span><span class="sxs-lookup"><span data-stu-id="d9175-118">**Description**</span></span> | <span data-ttu-id="d9175-119">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="d9175-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d9175-120">名字</span><span class="sxs-lookup"><span data-stu-id="d9175-120">Name</span></span> | <span data-ttu-id="d9175-121">報價明細的名稱，應可協助您找出估計中報價的分立元件。</span><span class="sxs-lookup"><span data-stu-id="d9175-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d9175-122">已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-123">計費方式</span><span class="sxs-lookup"><span data-stu-id="d9175-123">Billing Method</span></span> | <span data-ttu-id="d9175-124">在根據商機所建立的報價上，此值是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="d9175-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d9175-125">此欄位包含 Dynamics 365 Project Operations 支援的兩個主要合約模型：</span><span class="sxs-lookup"><span data-stu-id="d9175-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d9175-126">- 固定價格</span><span class="sxs-lookup"><span data-stu-id="d9175-126">- Fixed price</span></span></br><span data-ttu-id="d9175-127">- 時間和材料。</span><span class="sxs-lookup"><span data-stu-id="d9175-127">- Time and material.</span></span>| <span data-ttu-id="d9175-128">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-129">Project</span><span class="sxs-lookup"><span data-stu-id="d9175-129">Project</span></span> | <span data-ttu-id="d9175-130">使用此選用欄位來找出將在此業務開發上用來交付工作的專案。</span><span class="sxs-lookup"><span data-stu-id="d9175-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d9175-131">將專案對應至報價明細時，不僅有助於設定應收費工作，而且還可協助將專案型估計值提供給報價明細做為報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d9175-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d9175-132">未將專案對應至專案型報價明細時，應藉由建立每個報價明細詳細資料，手動建立估計值。</span><span class="sxs-lookup"><span data-stu-id="d9175-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d9175-133">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d9175-134">包含的工作</span><span class="sxs-lookup"><span data-stu-id="d9175-134">Included Tasks</span></span> | <span data-ttu-id="d9175-135">指示是否將此報價明細用於所選專案的所有或部分專案工作。</span><span class="sxs-lookup"><span data-stu-id="d9175-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d9175-136">此欄位有下列可能值：</span><span class="sxs-lookup"><span data-stu-id="d9175-136">This field has the following possible values:</span></span></br><span data-ttu-id="d9175-137">- 所有專案工作</span><span class="sxs-lookup"><span data-stu-id="d9175-137">- All project tasks</span></span></br><span data-ttu-id="d9175-138">- 僅限選取的專案工作</span><span class="sxs-lookup"><span data-stu-id="d9175-138">- Selected project tasks only</span></span></br><span data-ttu-id="d9175-139">此欄位值為空白就相當於 **所有專案工作** 選項。</span><span class="sxs-lookup"><span data-stu-id="d9175-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d9175-140">在專案頁面上選取 **僅限選取的專案工作** 時，**工作帳單設定** 索引標籤可讓您選取特定工作，以便將這些工作與此報價明細建立關聯。</span><span class="sxs-lookup"><span data-stu-id="d9175-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d9175-141">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-142">包括時間</span><span class="sxs-lookup"><span data-stu-id="d9175-142">Include Time</span></span> | <span data-ttu-id="d9175-143">**是**/**否** 旗標指示所選專案的時間交易或人力成本是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9175-144">**否** 值表示時間交易或人力成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9175-145">**是** 值表示時間交易或人力成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9175-146">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-147">包括費用</span><span class="sxs-lookup"><span data-stu-id="d9175-147">Include Expense</span></span> | <span data-ttu-id="d9175-148">**是**/**否** 旗標指示所選專案的費用成本是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9175-149">**否** 值表示費用成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9175-150">**是** 值表示費用成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9175-151">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-152">包括服務費</span><span class="sxs-lookup"><span data-stu-id="d9175-152">Include Fee</span></span> | <span data-ttu-id="d9175-153">**是**/**否** 旗標指示所選專案的服務費是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9175-154">**否** 值表示服務費不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9175-155">**是** 值表示服務費會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d9175-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9175-156">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-157">報價金額</span><span class="sxs-lookup"><span data-stu-id="d9175-157">Quoted Amount</span></span> | <span data-ttu-id="d9175-158">這是針對所有為此專案型報價明細預測之工作，報價給客戶的金額。</span><span class="sxs-lookup"><span data-stu-id="d9175-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d9175-159">在根據商機所建立的報價上，此值是從商機明細的 **客戶預算** 欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="d9175-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d9175-160">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的金額。</span><span class="sxs-lookup"><span data-stu-id="d9175-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d9175-161">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-162">估計稅額</span><span class="sxs-lookup"><span data-stu-id="d9175-162">Estimated Tax</span></span> | <span data-ttu-id="d9175-163">這是可編輯的欄位，以供使用者在報價明細上新增估計稅金。</span><span class="sxs-lookup"><span data-stu-id="d9175-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d9175-164">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的稅額。</span><span class="sxs-lookup"><span data-stu-id="d9175-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d9175-165">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-166">稅後報價金額</span><span class="sxs-lookup"><span data-stu-id="d9175-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d9175-167">此欄位是稅後報價明細金額，並且為唯讀。</span><span class="sxs-lookup"><span data-stu-id="d9175-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d9175-168">此欄位中的金額是以 *報價金額 + 稅金* 計算而得。</span><span class="sxs-lookup"><span data-stu-id="d9175-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d9175-169">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-170">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="d9175-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d9175-171">此欄位是可編輯的欄位，只能在帳務方式為 **時間和材料** 的專案型報價明細上使用。</span><span class="sxs-lookup"><span data-stu-id="d9175-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d9175-172">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9175-173">客戶預算</span><span class="sxs-lookup"><span data-stu-id="d9175-173">Customer Budget</span></span> | <span data-ttu-id="d9175-174">此欄位是可編輯的欄位，如果報價是根據商機所建立，則該欄位是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="d9175-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d9175-175">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d9175-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d9175-176">專案型報價明細的 [一般] 索引標籤上的欄位驗證規則</span><span class="sxs-lookup"><span data-stu-id="d9175-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d9175-177">**規則 1**：如果 **包含的工作** 欄位為空白，或者已設定為 **所有專案工作**，則會在報價明細中包含專案。</span><span class="sxs-lookup"><span data-stu-id="d9175-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="d9175-178">**規則 2**：如果 **包含的工作** 欄位為空白，或者已設定為 **所有專案工作**，則只能將專案及特定交易分類包含在報價的專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="d9175-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d9175-179">**規則 3**：如果 **包含的工作** 欄位已設定為 **僅限選取的專案工作**，則可以將專案及特定交易分類包含在報價的多個專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="d9175-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d9175-180">**規則 4**：如果商機有多個報價，則可以有來自各種全都參考相同專案且包含相同交易分類之不同報價的報價明細。</span><span class="sxs-lookup"><span data-stu-id="d9175-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d9175-181">**規則 5**：如果報價不屬於同一個商機，則不能包含相同的專案和交易分類。</span><span class="sxs-lookup"><span data-stu-id="d9175-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d9175-182">
                    <strong>商機</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d9175-183">
                    <strong>報價</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9175-184">
                    <strong>報價明細</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9175-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d9175-186">
                    <strong>包含的工作</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d9175-187">
                    <strong>包括時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d9175-188">
                    <strong>包括費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9175-189">
                    <strong>包括</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d9175-190">
                    <strong>費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d9175-191">
                    <strong>有效/無效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d9175-192">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9175-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-193">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-194">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-196">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-197">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-198">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-199">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-200">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-201">無效</span><span class="sxs-lookup"><span data-stu-id="d9175-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-202">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="d9175-202">Violation of Rule #2.</span></span> <span data-ttu-id="d9175-203">P1 專案上的時間、費用和服務費已包含在報價明細 QL1 與 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="d9175-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-204">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-205">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d9175-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-207">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-208">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-209">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-210">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-211">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-212">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-213">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-215">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-216">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-217">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-218">無</span><span class="sxs-lookup"><span data-stu-id="d9175-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-219">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-220">無效</span><span class="sxs-lookup"><span data-stu-id="d9175-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-221">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="d9175-221">Violation of Rule #2.</span></span> <span data-ttu-id="d9175-222">P1 專案上的時間和服務費已包含在報價明細 QL1 與 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="d9175-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-223">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-224">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d9175-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-226">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-227">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-228">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-229">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-230">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-231">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-232">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-234">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-235">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-236">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-237">無</span><span class="sxs-lookup"><span data-stu-id="d9175-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-238">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-239">有效</span><span class="sxs-lookup"><span data-stu-id="d9175-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d9175-240">P1 專案上的時間和服務費已包含在 QL1 中。</span><span class="sxs-lookup"><span data-stu-id="d9175-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d9175-241">P1 專案上的費用已包含在 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="d9175-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d9175-242">要包含在每個報價明細的項目中沒有重疊，並且有效。</span><span class="sxs-lookup"><span data-stu-id="d9175-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-243">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-244">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d9175-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-246">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-247">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-248">無</span><span class="sxs-lookup"><span data-stu-id="d9175-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-249">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-250">無</span><span class="sxs-lookup"><span data-stu-id="d9175-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-251">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-252">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-254">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-255">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="d9175-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-256">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-257">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-258">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-259">無效</span><span class="sxs-lookup"><span data-stu-id="d9175-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-260">違反上述規則 #2</span><span class="sxs-lookup"><span data-stu-id="d9175-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d9175-261">Q1 包含專案 P1 一部分工作的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="d9175-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9175-262">QL2 包含整個專案 P1 的時間、費用和服務費，並與 Q1 中包含的項目重疊。</span><span class="sxs-lookup"><span data-stu-id="d9175-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-263">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-264">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d9175-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-266">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-267">空白</span><span class="sxs-lookup"><span data-stu-id="d9175-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-268">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-269">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-270">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-271">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-272">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-274">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-275">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="d9175-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-276">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-277">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-278">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-279">有效</span><span class="sxs-lookup"><span data-stu-id="d9175-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-280">根據上述規則 #3，</span><span class="sxs-lookup"><span data-stu-id="d9175-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d9175-281">Q1 包含專案 P1 一部分工作的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="d9175-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9175-282">QL2 包含專案 P1 一部分工作的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="d9175-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9175-283">唯一的額外驗證是對 QL1 的一部分工作 (這些工作與 QL2 的一部分工作不同) 進行。</span><span class="sxs-lookup"><span data-stu-id="d9175-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d9175-284">這樣可確保不會發生重疊。</span><span class="sxs-lookup"><span data-stu-id="d9175-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d9175-285">建立與工作的關聯時，系統會完成此作業。</span><span class="sxs-lookup"><span data-stu-id="d9175-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-286">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-287">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d9175-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-289">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-290">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="d9175-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-291">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-292">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-293">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-294">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-295">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-297">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-298">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d9175-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-299">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-300">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-301">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9175-302">有效</span><span class="sxs-lookup"><span data-stu-id="d9175-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-303">根據規則 #5，Q1 和 Q2 是同一個商機上的兩個報價，因此都可以對專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="d9175-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-304">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-305">第 2 季</span><span class="sxs-lookup"><span data-stu-id="d9175-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-307">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-308">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d9175-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-309">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-310">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-311">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-312">O1</span><span class="sxs-lookup"><span data-stu-id="d9175-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-313">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-315">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-316">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d9175-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-317">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-318">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-319">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9175-320">有效</span><span class="sxs-lookup"><span data-stu-id="d9175-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9175-321">根據規則 #4，Q1 和 Q2 是兩個各在不同商機上的報價，因此無法對相同專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="d9175-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9175-322">O2</span><span class="sxs-lookup"><span data-stu-id="d9175-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9175-323">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d9175-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d9175-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-325">P1</span><span class="sxs-lookup"><span data-stu-id="d9175-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9175-326">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d9175-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-327">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9175-328">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9175-329">.是</span><span class="sxs-lookup"><span data-stu-id="d9175-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9175-330">無效</span><span class="sxs-lookup"><span data-stu-id="d9175-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]