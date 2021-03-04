---
title: 費用報表上的個人費用
description: 本主題說明兩種在 Microsoft Dynamics 365 Finance 中處理工作者個人費用的方法。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6b9d4fa0f69b4b0fe4bd1786958d22e5580a321
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 01/14/2021
ms.locfileid: "5114749"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="09a1f-103">費用報表上的個人費用</span><span class="sxs-lookup"><span data-stu-id="09a1f-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="09a1f-104">在商務差旅期間，工作者有時可能會有從其公司信用卡扣款的個人費用。</span><span class="sxs-lookup"><span data-stu-id="09a1f-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="09a1f-105">如果您沒有定義處理個人費用的程序，則可能會在工作者提交其逐條列舉的費用報表時，中斷費用報表的核准程序。</span><span class="sxs-lookup"><span data-stu-id="09a1f-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="09a1f-106">有兩種用來處理工作者個人費用的方法：</span><span class="sxs-lookup"><span data-stu-id="09a1f-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="09a1f-107">**由員工支付** – 您的組織不支付出現在公司信用卡帳單的個人費用。</span><span class="sxs-lookup"><span data-stu-id="09a1f-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="09a1f-108">相反的是，建立一併顯示已從公司信用卡扣款之個人費用與公司費用的報表。</span><span class="sxs-lookup"><span data-stu-id="09a1f-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="09a1f-109">**由公司支付** – 您的組織會支付公司信用卡的全部帳單，然後工作者的帳戶中借記個人費用。</span><span class="sxs-lookup"><span data-stu-id="09a1f-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="09a1f-110">您可以在 **費用管理參數** 頁面上選取您的組織所使用的方法。</span><span class="sxs-lookup"><span data-stu-id="09a1f-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
