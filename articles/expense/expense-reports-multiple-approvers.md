---
title: 費用報表和多個核准者
description: 本主題提供有關需要多人核准之費用報表的資訊。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276555"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="928b7-103">費用報表和多個核准者</span><span class="sxs-lookup"><span data-stu-id="928b7-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="928b7-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="928b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="928b7-105">根據您組織的費用核准原則，可能需要多人來核准已提交的費用報表。</span><span class="sxs-lookup"><span data-stu-id="928b7-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="928b7-106">設定費用報表核准工作流程程序時，您可以新增包含一個或多個費用報表核准者之工作或步驟的工作流程元素。</span><span class="sxs-lookup"><span data-stu-id="928b7-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="928b7-107">例如，您可能需要由兩名不同的人員 (提交報表之員工經理以及應付帳款協調員) 來核准所有費用報表。</span><span class="sxs-lookup"><span data-stu-id="928b7-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="928b7-108">如果您認為需要多名費用報表核准者，則可以透過下列任何方式新增工作流程元素：</span><span class="sxs-lookup"><span data-stu-id="928b7-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="928b7-109">新增一個含有一個步驟的核准元素。</span><span class="sxs-lookup"><span data-stu-id="928b7-109">Add one approval element that has one step.</span></span> <span data-ttu-id="928b7-110">例如，步驟可能需要將費用報表指派給使用者群組，並由使用者群組 50% 的成員進行核准。</span><span class="sxs-lookup"><span data-stu-id="928b7-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="928b7-111">新增一個含有多個步驟的核准元素。</span><span class="sxs-lookup"><span data-stu-id="928b7-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="928b7-112">例如，核准元素可能會有下列步驟：</span><span class="sxs-lookup"><span data-stu-id="928b7-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="928b7-113">提交費用報表之員工的經理會核准該報表。</span><span class="sxs-lookup"><span data-stu-id="928b7-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="928b7-114">應付帳款職員會驗證收據和費用報表項目。</span><span class="sxs-lookup"><span data-stu-id="928b7-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="928b7-115">預算負責人會核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="928b7-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="928b7-116">新增多個核准元素，其中每個都有一個步驟。</span><span class="sxs-lookup"><span data-stu-id="928b7-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="928b7-117">例如，您可能會為下列每一個步驟新增不同的核准元素：</span><span class="sxs-lookup"><span data-stu-id="928b7-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="928b7-118">員工的經理會核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="928b7-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="928b7-119">預算負責人會核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="928b7-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]