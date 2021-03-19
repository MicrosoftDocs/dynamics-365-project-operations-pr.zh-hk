---
title: 在合約上建立專項預付金
description: 本主題提供有關視需要在合約上建立預付金的資訊。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273624"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="67166-103">在合約上建立專項預付金</span><span class="sxs-lookup"><span data-stu-id="67166-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="67166-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="67166-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="67166-105">Microsoft Dynamics 365 Project Operations 支援涉及預先付費和預付金的開立發票案例。</span><span class="sxs-lookup"><span data-stu-id="67166-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="67166-106">**Project Operations** 中使用 **預付金** 的程序類似於 **保留款** 合約。</span><span class="sxs-lookup"><span data-stu-id="67166-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="67166-107">完成下列步驟，為客戶開立預付金發票。</span><span class="sxs-lookup"><span data-stu-id="67166-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="67166-108">移至 **專案合約** 頁面，然後選取 **預付金和保留款** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="67166-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="67166-109">在列出所有先前已記錄之預付金和預先付費的子格中，選取 **+ 新增專案合約保留款**。</span><span class="sxs-lookup"><span data-stu-id="67166-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="67166-110">**快速建立** 表單會開啟以用於記錄預付金或預先付費。</span><span class="sxs-lookup"><span data-stu-id="67166-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="67166-111">下表列出用於記錄預付金的欄位以及建立新預付金時要牢記的考量事項：</span><span class="sxs-lookup"><span data-stu-id="67166-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="67166-112">欄位</span><span class="sxs-lookup"><span data-stu-id="67166-112">Field</span></span> | <span data-ttu-id="67166-113">描述</span><span class="sxs-lookup"><span data-stu-id="67166-113">Description</span></span> | <span data-ttu-id="67166-114">下游影響</span><span class="sxs-lookup"><span data-stu-id="67166-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="67166-115">**專案合約客戶**</span><span class="sxs-lookup"><span data-stu-id="67166-115">**Project Contract Customer**</span></span> | <span data-ttu-id="67166-116">此欄位指出要為合約上的哪個客戶開立此預付金的發票。</span><span class="sxs-lookup"><span data-stu-id="67166-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="67166-117">如果合約上有多個客戶，而您想要為其中每一個客戶開立特定保留款或預付款金額的發票時，請為每個客戶個別建立預付金。</span><span class="sxs-lookup"><span data-stu-id="67166-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="67166-118">**描述**</span><span class="sxs-lookup"><span data-stu-id="67166-118">**Description**</span></span> | <span data-ttu-id="67166-119">可協助找出這筆預付金的預付金目的及時間安排描述。</span><span class="sxs-lookup"><span data-stu-id="67166-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="67166-120">此描述會顯示在這筆預付金的發票明細上。</span><span class="sxs-lookup"><span data-stu-id="67166-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="67166-121">**金額**</span><span class="sxs-lookup"><span data-stu-id="67166-121">**Amount**</span></span> | <span data-ttu-id="67166-122">預先付費或預付金的金額。</span><span class="sxs-lookup"><span data-stu-id="67166-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="67166-123">此金額會顯示在這筆預付金的發票明細上。</span><span class="sxs-lookup"><span data-stu-id="67166-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="67166-124">**發票日期**</span><span class="sxs-lookup"><span data-stu-id="67166-124">**Invoice Date**</span></span> | <span data-ttu-id="67166-125">向客戶開立這筆預付金之發票的日期。</span><span class="sxs-lookup"><span data-stu-id="67166-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="67166-126">這是要為此預付金建立發票明細的自動化發票建立程序日期。</span><span class="sxs-lookup"><span data-stu-id="67166-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="67166-127">**發票狀態**</span><span class="sxs-lookup"><span data-stu-id="67166-127">**Invoice Status**</span></span> | <span data-ttu-id="67166-128">這是指示這筆預付金是否已新增至此客戶之草稿發票的選項設定。</span><span class="sxs-lookup"><span data-stu-id="67166-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="67166-129">可能的值是：</span><span class="sxs-lookup"><span data-stu-id="67166-129">The possible values are:</span></span></br><span data-ttu-id="67166-130">- **尚未準備好開立發票**</span><span class="sxs-lookup"><span data-stu-id="67166-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="67166-131">- **已準備好開立發票**</span><span class="sxs-lookup"><span data-stu-id="67166-131">- **Ready to invoice**</span></span> | <span data-ttu-id="67166-132">當預付金或預先付費標示為 **已準備好開立發票** 時，系統會將這筆款項新增為草稿發票上的明細時間。</span><span class="sxs-lookup"><span data-stu-id="67166-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="67166-133">只有已全額開立發票的預付金才能用來對下一個發票期間的專案成本進行差異協調。</span><span class="sxs-lookup"><span data-stu-id="67166-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="67166-134">選取快速建立對話方塊上的 **儲存後關閉**，以記錄預付金或預先付費。</span><span class="sxs-lookup"><span data-stu-id="67166-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]