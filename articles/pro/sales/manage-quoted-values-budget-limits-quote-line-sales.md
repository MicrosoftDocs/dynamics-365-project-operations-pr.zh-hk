---
title: 專案型報價明細 (專業版)
description: 本主題提供有關將專案型報價明細用於專案工作的資訊。 (專業版)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087430"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="d8da3-104">專案型報價明細 (專業版)</span><span class="sxs-lookup"><span data-stu-id="d8da3-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="d8da3-105">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d8da3-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d8da3-106">專案型報價明細是為了協助在業務開發上估計專案工作而設計。</span><span class="sxs-lookup"><span data-stu-id="d8da3-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d8da3-107">專案型報價明細的結構已運用下列概念針對專案估計值進行擴充：</span><span class="sxs-lookup"><span data-stu-id="d8da3-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d8da3-108">計費方式</span><span class="sxs-lookup"><span data-stu-id="d8da3-108">Billing Method</span></span>
- <span data-ttu-id="d8da3-109">專案和工作對應</span><span class="sxs-lookup"><span data-stu-id="d8da3-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d8da3-110">已包含交易分類</span><span class="sxs-lookup"><span data-stu-id="d8da3-110">Included Transaction classes</span></span>
- <span data-ttu-id="d8da3-111">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="d8da3-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d8da3-112">可收費率設定</span><span class="sxs-lookup"><span data-stu-id="d8da3-112">Chargeability setup</span></span>
- <span data-ttu-id="d8da3-113">使用報價明細詳細資料的估計</span><span class="sxs-lookup"><span data-stu-id="d8da3-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d8da3-114">報價明細客戶</span><span class="sxs-lookup"><span data-stu-id="d8da3-114">Quote line Customers</span></span>

<span data-ttu-id="d8da3-115">下表提供有關專案型報價明細的 **一般** 索引標籤上的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="d8da3-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d8da3-116">這些欄位可協助為專案工作設定詳細的全新估計基礎。</span><span class="sxs-lookup"><span data-stu-id="d8da3-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d8da3-117">**欄位**</span><span class="sxs-lookup"><span data-stu-id="d8da3-117">**Field**</span></span> | <span data-ttu-id="d8da3-118">**關聯性、目的和指引**</span><span class="sxs-lookup"><span data-stu-id="d8da3-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="d8da3-119">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="d8da3-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d8da3-120">名字</span><span class="sxs-lookup"><span data-stu-id="d8da3-120">Name</span></span> | <span data-ttu-id="d8da3-121">報價明細的名稱，應可協助您找出估計中報價的分立元件。</span><span class="sxs-lookup"><span data-stu-id="d8da3-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d8da3-122">已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-123">計費方式</span><span class="sxs-lookup"><span data-stu-id="d8da3-123">Billing Method</span></span> | <span data-ttu-id="d8da3-124">在根據商機所建立的報價上，此值是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="d8da3-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d8da3-125">此欄位包含 Dynamics 365 Project Operations 所支援的兩個主要合約模型：</span><span class="sxs-lookup"><span data-stu-id="d8da3-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d8da3-126">- 固定價格</span><span class="sxs-lookup"><span data-stu-id="d8da3-126">- Fixed price</span></span></br><span data-ttu-id="d8da3-127">- 時間和材料。</span><span class="sxs-lookup"><span data-stu-id="d8da3-127">- Time and material.</span></span>| <span data-ttu-id="d8da3-128">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-129">Project</span><span class="sxs-lookup"><span data-stu-id="d8da3-129">Project</span></span> | <span data-ttu-id="d8da3-130">使用此選用欄位來找出將在此業務開發上用來交付工作的專案。</span><span class="sxs-lookup"><span data-stu-id="d8da3-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d8da3-131">將專案對應至報價明細時，不僅有助於設定應收費工作，而且還可協助將專案型估計值提供給報價明細做為報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d8da3-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d8da3-132">未將專案對應至專案型報價明細時，應藉由建立每個報價明細詳細資料，手動建立估計值。</span><span class="sxs-lookup"><span data-stu-id="d8da3-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d8da3-133">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d8da3-134">包含的工作</span><span class="sxs-lookup"><span data-stu-id="d8da3-134">Included Tasks</span></span> | <span data-ttu-id="d8da3-135">指示是否將此報價明細用於所選專案的所有或部分專案工作。</span><span class="sxs-lookup"><span data-stu-id="d8da3-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d8da3-136">此欄位有下列可能值：</span><span class="sxs-lookup"><span data-stu-id="d8da3-136">This field has the following possible values:</span></span></br><span data-ttu-id="d8da3-137">- 所有專案工作</span><span class="sxs-lookup"><span data-stu-id="d8da3-137">- All project tasks</span></span></br><span data-ttu-id="d8da3-138">- 僅限選取的專案工作</span><span class="sxs-lookup"><span data-stu-id="d8da3-138">- Selected project tasks only</span></span></br><span data-ttu-id="d8da3-139">此欄位值為空白就相當於 **所有專案工作** 選項。</span><span class="sxs-lookup"><span data-stu-id="d8da3-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d8da3-140">在專案頁面上選取 **僅限選取的專案工作** 時， **工作帳單設定** 索引標籤可讓您選取特定工作，以便將這些工作與此報價明細建立關聯。</span><span class="sxs-lookup"><span data-stu-id="d8da3-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d8da3-141">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-142">包括時間</span><span class="sxs-lookup"><span data-stu-id="d8da3-142">Include Time</span></span> | <span data-ttu-id="d8da3-143">**是**/**否** 旗標指示所選專案的時間交易或人力成本是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d8da3-144">**否** 值表示時間交易或人力成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d8da3-145">**是** 值表示時間交易或人力成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d8da3-146">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-147">包括費用</span><span class="sxs-lookup"><span data-stu-id="d8da3-147">Include Expense</span></span> | <span data-ttu-id="d8da3-148">**是**/**否** 旗標指示所選專案的費用成本是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d8da3-149">**否** 值表示費用成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d8da3-150">**是** 值表示費用成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d8da3-151">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-152">包括服務費</span><span class="sxs-lookup"><span data-stu-id="d8da3-152">Include Fee</span></span> | <span data-ttu-id="d8da3-153">**是**/**否** 旗標指示所選專案的服務費是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d8da3-154">**否** 值表示服務費不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d8da3-155">**是** 值表示服務費會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d8da3-156">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-157">報價金額</span><span class="sxs-lookup"><span data-stu-id="d8da3-157">Quoted Amount</span></span> | <span data-ttu-id="d8da3-158">這是針對所有為此專案型報價明細預測之工作，報價給客戶的金額。</span><span class="sxs-lookup"><span data-stu-id="d8da3-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d8da3-159">在根據商機所建立的報價上，此值是從商機明細的 **客戶預算** 欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="d8da3-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d8da3-160">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的金額。</span><span class="sxs-lookup"><span data-stu-id="d8da3-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d8da3-161">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-162">估計稅額</span><span class="sxs-lookup"><span data-stu-id="d8da3-162">Estimated Tax</span></span> | <span data-ttu-id="d8da3-163">這是可編輯的欄位，以供使用者在報價明細上新增估計稅金。</span><span class="sxs-lookup"><span data-stu-id="d8da3-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d8da3-164">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的稅額。</span><span class="sxs-lookup"><span data-stu-id="d8da3-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d8da3-165">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-166">稅後報價金額</span><span class="sxs-lookup"><span data-stu-id="d8da3-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d8da3-167">此欄位是稅後報價明細金額，並且為唯讀。</span><span class="sxs-lookup"><span data-stu-id="d8da3-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d8da3-168">此欄位中的金額是以 *報價金額 + 稅金* 計算而得。</span><span class="sxs-lookup"><span data-stu-id="d8da3-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d8da3-169">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-170">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="d8da3-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d8da3-171">此欄位是可編輯的欄位，只能在帳務方式為 **時間和材料** 的專案型報價明細上使用。</span><span class="sxs-lookup"><span data-stu-id="d8da3-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d8da3-172">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d8da3-173">客戶預算</span><span class="sxs-lookup"><span data-stu-id="d8da3-173">Customer Budget</span></span> | <span data-ttu-id="d8da3-174">此欄位是可編輯的欄位，如果報價是根據商機所建立，則該欄位是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="d8da3-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d8da3-175">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="d8da3-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d8da3-176">專案型報價明細的 [一般] 索引標籤上的欄位驗證規則</span><span class="sxs-lookup"><span data-stu-id="d8da3-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d8da3-177">**規則 1** ：如果 **包含的工作** 欄位為空白，或者已設定為 **所有專案工作** ，則會在報價明細中包含專案。</span><span class="sxs-lookup"><span data-stu-id="d8da3-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="d8da3-178">**規則 2** ：如果 **包含的工作** 欄位為空白，或者已設定為 **所有專案工作** ，則只能將專案及特定交易分類包含在報價的專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d8da3-179">**規則 3** ：如果 **包含的工作** 欄位已設定為 **僅限選取的專案工作** ，則可以將專案及特定交易分類包含在報價的多個專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d8da3-180">**規則 4** ：如果商機有多個報價，則可以有來自各種全都參考相同專案且包含相同交易分類之不同報價的報價明細。</span><span class="sxs-lookup"><span data-stu-id="d8da3-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d8da3-181">**規則 5** ：如果報價不屬於同一個商機，則不能包含相同的專案和交易分類。</span><span class="sxs-lookup"><span data-stu-id="d8da3-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d8da3-182">
                    <strong>商機</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d8da3-183">
                    <strong>報價</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d8da3-184">
                    <strong>報價明細</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d8da3-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d8da3-186">
                    <strong>包含的工作</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d8da3-187">
                    <strong>包括時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d8da3-188">
                    <strong>包括費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d8da3-189">
                    <strong>包括</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d8da3-190">
                    <strong>費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d8da3-191">
                    <strong>有效/無效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d8da3-192">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d8da3-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-193">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-194">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-196">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-197">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-198">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-199">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-200">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-201">無效</span><span class="sxs-lookup"><span data-stu-id="d8da3-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-202">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="d8da3-202">Violation of Rule #2.</span></span> <span data-ttu-id="d8da3-203">P1 專案上的時間、費用和服務費已包含在報價明細 QL1 與 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-204">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-205">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d8da3-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-207">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-208">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-209">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-210">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-211">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-211">Yes</span></span> </p>
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
<span data-ttu-id="d8da3-212">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-213">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-215">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-216">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-217">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-218">無</span><span class="sxs-lookup"><span data-stu-id="d8da3-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-219">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-220">無效</span><span class="sxs-lookup"><span data-stu-id="d8da3-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-221">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="d8da3-221">Violation of Rule #2.</span></span> <span data-ttu-id="d8da3-222">P1 專案上的時間和服務費已包含在報價明細 QL1 與 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-223">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-224">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d8da3-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-226">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-227">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-228">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-229">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-230">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-230">Yes</span></span> </p>
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
<span data-ttu-id="d8da3-231">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-232">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-234">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-235">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-236">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-237">無</span><span class="sxs-lookup"><span data-stu-id="d8da3-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-238">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-239">有效</span><span class="sxs-lookup"><span data-stu-id="d8da3-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d8da3-240">P1 專案上的時間和服務費已包含在 QL1 中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d8da3-241">P1 專案上的費用已包含在 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="d8da3-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d8da3-242">要包含在每個報價明細的項目中沒有重疊，並且有效。</span><span class="sxs-lookup"><span data-stu-id="d8da3-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-243">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-244">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d8da3-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-246">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-247">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-248">無</span><span class="sxs-lookup"><span data-stu-id="d8da3-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-249">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-250">無</span><span class="sxs-lookup"><span data-stu-id="d8da3-250">No</span></span> </p>
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
<span data-ttu-id="d8da3-251">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-252">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-254">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-255">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="d8da3-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-256">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-257">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-258">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-259">無效</span><span class="sxs-lookup"><span data-stu-id="d8da3-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-260">違反上述規則 #2</span><span class="sxs-lookup"><span data-stu-id="d8da3-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d8da3-261">Q1 包含專案 P1 一部分工作的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="d8da3-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d8da3-262">QL2 包含整個專案 P1 的時間、費用和服務費，並與 Q1 中包含的項目重疊。</span><span class="sxs-lookup"><span data-stu-id="d8da3-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-263">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-264">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d8da3-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-266">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-267">空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-268">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-269">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-270">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-270">Yes</span></span> </p>
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
<span data-ttu-id="d8da3-271">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-272">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-274">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-275">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="d8da3-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-276">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-277">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-278">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-279">有效</span><span class="sxs-lookup"><span data-stu-id="d8da3-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-280">根據上述規則 #3，</span><span class="sxs-lookup"><span data-stu-id="d8da3-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d8da3-281">Q1 包含專案 P1 一部分工作的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="d8da3-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d8da3-282">QL2 包含專案 P1 一部分工作的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="d8da3-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d8da3-283">唯一的額外驗證是對 QL1 的一部分工作 (這些工作與 QL2 的一部分工作不同) 進行。</span><span class="sxs-lookup"><span data-stu-id="d8da3-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d8da3-284">這樣可確保不會發生重疊。</span><span class="sxs-lookup"><span data-stu-id="d8da3-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d8da3-285">建立與工作的關聯時，系統會完成此作業。</span><span class="sxs-lookup"><span data-stu-id="d8da3-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-286">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-287">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d8da3-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-289">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-290">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="d8da3-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-291">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-292">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-293">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-293">Yes</span></span> </p>
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
<span data-ttu-id="d8da3-294">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-295">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-297">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-298">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-299">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-300">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-301">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d8da3-302">有效</span><span class="sxs-lookup"><span data-stu-id="d8da3-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-303">根據規則 #5，Q1 和 Q2 是同一個商機上的兩個報價，因此都可以對專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="d8da3-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-304">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-305">第 2 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-307">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-308">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-309">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-310">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-311">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-311">Yes</span></span> </p>
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
<span data-ttu-id="d8da3-312">O1</span><span class="sxs-lookup"><span data-stu-id="d8da3-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-313">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-315">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-316">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-317">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-318">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-319">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d8da3-320">有效</span><span class="sxs-lookup"><span data-stu-id="d8da3-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d8da3-321">根據規則 #4，Q1 和 Q2 是兩個各在不同商機上的報價，因此無法對相同專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="d8da3-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d8da3-322">O2</span><span class="sxs-lookup"><span data-stu-id="d8da3-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d8da3-323">第 1 季</span><span class="sxs-lookup"><span data-stu-id="d8da3-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d8da3-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-325">P1</span><span class="sxs-lookup"><span data-stu-id="d8da3-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d8da3-326">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="d8da3-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-327">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d8da3-328">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d8da3-329">.是</span><span class="sxs-lookup"><span data-stu-id="d8da3-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d8da3-330">無效</span><span class="sxs-lookup"><span data-stu-id="d8da3-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

