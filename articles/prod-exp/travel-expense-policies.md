---
title: 設定費用原則
description: 您可以設定您的工作者在 Microsoft Dynamics 365 Finance 中輸入和提交費用報表和差旅申請時必須遵循的費用原則。
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271290"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="5506f-103">設定費用原則</span><span class="sxs-lookup"><span data-stu-id="5506f-103">Set up expense policies</span></span>

<span data-ttu-id="5506f-104">您可以定義您的工作者在輸入和提交費用報表和差旅申請時必須遵循的原則。</span><span class="sxs-lookup"><span data-stu-id="5506f-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="5506f-105">實行費用原則可以協助您有效管理費用。</span><span class="sxs-lookup"><span data-stu-id="5506f-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="5506f-106">例如，您可以設定紐約市住宿費用的原則，規定每夜費用不能超過美元 250。</span><span class="sxs-lookup"><span data-stu-id="5506f-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="5506f-107">如果工作者提交住房費超過此金額的費用報表或差旅申請，系統就會通知</span><span class="sxs-lookup"><span data-stu-id="5506f-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="5506f-108">工作者已超過費用原則的金額。</span><span class="sxs-lookup"><span data-stu-id="5506f-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="5506f-109">您可以在定義原則時設定工作者會收到的訊息</span><span class="sxs-lookup"><span data-stu-id="5506f-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="5506f-110">。</span><span class="sxs-lookup"><span data-stu-id="5506f-110">define the policy.</span></span>      
        
<span data-ttu-id="5506f-111">您可以定義三種類型的原則：</span><span class="sxs-lookup"><span data-stu-id="5506f-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="5506f-112">警告 – 允許工作者提交費用報表或差旅申請，但會標示費用給所有核准者處理並</span><span class="sxs-lookup"><span data-stu-id="5506f-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="5506f-113">供稍後提報。</span><span class="sxs-lookup"><span data-stu-id="5506f-113">for later reporting.</span></span>        

- <span data-ttu-id="5506f-114">錯誤 – 要求工作者必須先將費用修訂成符合原則，才能提交費用報表或差旅申請。</span><span class="sxs-lookup"><span data-stu-id="5506f-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="5506f-115">正當理由 – 要求工作者或經理必須先輸入超出原則金額的正當理由，才能提交費用報表或差旅申請。</span><span class="sxs-lookup"><span data-stu-id="5506f-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="5506f-116">原則提示</span><span class="sxs-lookup"><span data-stu-id="5506f-116">Policy tips</span></span>
<span data-ttu-id="5506f-117">以下是一些可在建立費用管理新原則時協助您的建議。</span><span class="sxs-lookup"><span data-stu-id="5506f-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="5506f-118">原則有生效日期，如果原則的建立日期是在費用發生日期之後，則原則無法生效。</span><span class="sxs-lookup"><span data-stu-id="5506f-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="5506f-119">例如，如果您現在要建立新的原則以強制 $50 的最高餐費，則任何戳至昨天所輸入的現有費用都不會依據此原則進行檢查。</span><span class="sxs-lookup"><span data-stu-id="5506f-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="5506f-120">針對可逐條列舉的費用類別建立原則時，請考慮新增費用明細類型的條件。</span><span class="sxs-lookup"><span data-stu-id="5506f-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="5506f-121">有些原則 (例如，需要收據) 可能不適合逐條列舉的明細，只能套用至標題列或非逐條列舉的明細。</span><span class="sxs-lookup"><span data-stu-id="5506f-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="5506f-122">預設會依據來源實體評估費用管理原則。</span><span class="sxs-lookup"><span data-stu-id="5506f-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="5506f-123">在公司間交易案例中，您可以將原則設定為改依目的地實體 (借用實體) 進行評估。</span><span class="sxs-lookup"><span data-stu-id="5506f-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="5506f-124">若要依據目的地實體執行原則，請開啟 **功能管理** 工作區中的 [依據借用法律實體評估費用原則] 功能。</span><span class="sxs-lookup"><span data-stu-id="5506f-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="5506f-125">評估原則的時機</span><span class="sxs-lookup"><span data-stu-id="5506f-125">When to evaluate policies</span></span>

<span data-ttu-id="5506f-126">在費用管理參數中，有選項供您選擇在儲存明細時或在提交費用報表時評估費用管理原則。</span><span class="sxs-lookup"><span data-stu-id="5506f-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="5506f-127">如果您選擇在儲存明細時進行評估，這可確保使用者及早了解一次全部完成其費用報表所需執行的工作。</span><span class="sxs-lookup"><span data-stu-id="5506f-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="5506f-128">否則，在提交至工作流程的過程中，如果結束時會進行驗證，您可以將原則評估延遲並節省時間。</span><span class="sxs-lookup"><span data-stu-id="5506f-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]