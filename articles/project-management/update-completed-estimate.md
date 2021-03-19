---
title: 更新完工估計值
description: 本主題提供有關更新專案投入量推測的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286455"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="98e08-103">更新完工估計值</span><span class="sxs-lookup"><span data-stu-id="98e08-103">Update estimate at completion</span></span>

<span data-ttu-id="98e08-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="98e08-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98e08-105">修訂工作的原始預估值，對專案經理來說很平常。</span><span class="sxs-lookup"><span data-stu-id="98e08-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="98e08-106">專案重新推測是專案經理在專案目前狀態的考量下，對估計值所產生的看法。</span><span class="sxs-lookup"><span data-stu-id="98e08-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="98e08-107">然而，我們不建議專案經理變更基準數字，因為專案基準代表專案排程和成本預估值的既定事實原始資料，這是所有專案利害關係人都同意的。</span><span class="sxs-lookup"><span data-stu-id="98e08-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="98e08-108">有兩種專案經理可用來重新推測工作投入量的方法：</span><span class="sxs-lookup"><span data-stu-id="98e08-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="98e08-109">以工作實際剩餘未完成投入量的新估計值來覆寫尚未完工估計值 (ETC)。</span><span class="sxs-lookup"><span data-stu-id="98e08-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="98e08-110">以新的對工作實際進度的估計值覆寫預設進行百分比。</span><span class="sxs-lookup"><span data-stu-id="98e08-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="98e08-111">上述每一種方法都會導致重新計算工作的 ETC、完工估計值 (EAC) 和進度百分比，以及工作的預計投入量差異。</span><span class="sxs-lookup"><span data-stu-id="98e08-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="98e08-112">系統會重新計算摘要工作的 EAC、ETC 和進度百分比，並產生最新的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="98e08-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]