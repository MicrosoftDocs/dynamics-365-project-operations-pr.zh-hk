---
title: 費用概觀
description: 本主題提供有關 Project Operations 中費用功能的資訊。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764936"
---
# <a name="expense-home-page"></a><span data-ttu-id="15620-103">費用首頁</span><span class="sxs-lookup"><span data-stu-id="15620-103">Expense home page</span></span>

<span data-ttu-id="15620-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="15620-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="15620-105">Dynamics 365 Project Operations 支援處理費用的功能。</span><span class="sxs-lookup"><span data-stu-id="15620-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="15620-106">使用原則、交易類別和核准的可自訂工作流程，處理在專案上或不在專案上發生的費用。</span><span class="sxs-lookup"><span data-stu-id="15620-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="15620-107">在 Project Operations 中，費用有兩個支援的部署模型：</span><span class="sxs-lookup"><span data-stu-id="15620-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="15620-108">**完整**：**資源/非庫存型案例適用的 Project Operations** 或 **生產訂單型案例適用的 Project Operations** 可以使用完整部署。</span><span class="sxs-lookup"><span data-stu-id="15620-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="15620-109">**基本**：**資源/非庫存型案例適用的 Project Operations** 和 **精簡部署 – 交易至開立預估發票** 可以使用基本部署。</span><span class="sxs-lookup"><span data-stu-id="15620-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="15620-110">完整</span><span class="sxs-lookup"><span data-stu-id="15620-110">Full</span></span> 
<span data-ttu-id="15620-111">完整費用部署提供完整的原則強制執行，其中包含用於建立原則的功能，例如：</span><span class="sxs-lookup"><span data-stu-id="15620-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="15620-112">費用類別限制</span><span class="sxs-lookup"><span data-stu-id="15620-112">Expense category limits</span></span>
  - <span data-ttu-id="15620-113">差旅</span><span class="sxs-lookup"><span data-stu-id="15620-113">Travel</span></span>
  - <span data-ttu-id="15620-114">按日</span><span class="sxs-lookup"><span data-stu-id="15620-114">Per diem</span></span>
  - <span data-ttu-id="15620-115">信用卡匯入</span><span class="sxs-lookup"><span data-stu-id="15620-115">Credit card imports</span></span>
  - <span data-ttu-id="15620-116">收據光學字元辨識</span><span class="sxs-lookup"><span data-stu-id="15620-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="15620-117">基本</span><span class="sxs-lookup"><span data-stu-id="15620-117">Basic</span></span> 
<span data-ttu-id="15620-118">基本費用部署案例只允許您針對某個專案來記錄基本費用。</span><span class="sxs-lookup"><span data-stu-id="15620-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="15620-119">如需詳細資訊，請參閱[費用項目 (精簡)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="15620-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="15620-120">判斷您的費用部署</span><span class="sxs-lookup"><span data-stu-id="15620-120">Determine your Expense deployment</span></span>
<span data-ttu-id="15620-121">若要判斷您是否正在執行基本費用管理部署，請確認位址 URL 是否以 **.crm.dynamics.com** 結尾。</span><span class="sxs-lookup"><span data-stu-id="15620-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
