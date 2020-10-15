---
title: 費用概觀
description: 本主題提供有關 Project Operations 中費用功能的資訊。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967393"
---
# <a name="expense-home-page"></a><span data-ttu-id="0def1-103">費用首頁</span><span class="sxs-lookup"><span data-stu-id="0def1-103">Expense home page</span></span>

<span data-ttu-id="0def1-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="0def1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0def1-105">Dynamics 365 Project Operations 支援處理費用的功能。</span><span class="sxs-lookup"><span data-stu-id="0def1-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="0def1-106">使用原則、交易類別和核准的可自訂工作流程，處理在專案上或不在專案上發生的費用。</span><span class="sxs-lookup"><span data-stu-id="0def1-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="0def1-107">在 Project Operations 中，費用有兩個支援的部署模型：</span><span class="sxs-lookup"><span data-stu-id="0def1-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="0def1-108">**完整**：**資源/非庫存型案例適用的 Project Operations** 或**生產訂單型案例適用的 Project Operations** 可以使用完整部署。</span><span class="sxs-lookup"><span data-stu-id="0def1-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="0def1-109">**基本**：**資源/非庫存型案例適用的 Project Operations**和**精簡部署 – 交易至開立預估發票**可以使用基本部署。</span><span class="sxs-lookup"><span data-stu-id="0def1-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="0def1-110">完整</span><span class="sxs-lookup"><span data-stu-id="0def1-110">Full</span></span> 
<span data-ttu-id="0def1-111">完整費用部署提供完整原則強制，其中包含建立原則的功能，例如：</span><span class="sxs-lookup"><span data-stu-id="0def1-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="0def1-112">費用類別限制</span><span class="sxs-lookup"><span data-stu-id="0def1-112">Expense category limits</span></span>
  - <span data-ttu-id="0def1-113">差旅</span><span class="sxs-lookup"><span data-stu-id="0def1-113">Travel</span></span>
  - <span data-ttu-id="0def1-114">按日</span><span class="sxs-lookup"><span data-stu-id="0def1-114">Per diem</span></span>
  - <span data-ttu-id="0def1-115">信用卡匯入</span><span class="sxs-lookup"><span data-stu-id="0def1-115">Credit card imports</span></span>
  - <span data-ttu-id="0def1-116">收據光學字元辨識</span><span class="sxs-lookup"><span data-stu-id="0def1-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="0def1-117">基本</span><span class="sxs-lookup"><span data-stu-id="0def1-117">Basic</span></span> 
<span data-ttu-id="0def1-118">基本費用部署案例只允許您針對某個專案來記錄基本費用。</span><span class="sxs-lookup"><span data-stu-id="0def1-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="0def1-119">如需詳細資訊，請參閱[費用項目 (精簡)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="0def1-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="0def1-120">判斷您的費用部署</span><span class="sxs-lookup"><span data-stu-id="0def1-120">Determine your Expense deployment</span></span>
<span data-ttu-id="0def1-121">若要判斷您是否正在執行基本費用管理部署，請確認位址 URL 是否以 **.crm.dynamics.com** 結尾。</span><span class="sxs-lookup"><span data-stu-id="0def1-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 