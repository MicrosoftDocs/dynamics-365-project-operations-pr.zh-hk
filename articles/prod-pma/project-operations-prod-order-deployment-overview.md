---
title: 庫存/生產型案例適用的 Project Operations 部署概觀
description: 此主題提供關於庫存/生產型案例適用的 Project Operations 部署類型的資訊。
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b2a606bc587b99c16d45b19689ba90b422c3c62
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999428"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="221b9-103">庫存/生產型案例適用的 Project Operations 部署概觀</span><span class="sxs-lookup"><span data-stu-id="221b9-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="221b9-104">_**適用於：** 庫存/生產型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="221b9-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="221b9-105">此部署類型具有下列適用於專案型公司的功能：</span><span class="sxs-lookup"><span data-stu-id="221b9-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="221b9-106">使用[分工結構圖](work-breakdown-structures.md)規劃的專案</span><span class="sxs-lookup"><span data-stu-id="221b9-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="221b9-107">為專案採購和消耗庫存</span><span class="sxs-lookup"><span data-stu-id="221b9-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="221b9-108">使用 Dynamics 365 Finance and Operations 應用程式中的 **銷售和行銷** 模組管理專案型銷售</span><span class="sxs-lookup"><span data-stu-id="221b9-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="221b9-109">使用 Finance and Operations 應用程式中成本費率和帳單費率設定的專案定價和成本計算</span><span class="sxs-lookup"><span data-stu-id="221b9-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="221b9-110">Finance and Operations 應用程式中的專案資源管理</span><span class="sxs-lookup"><span data-stu-id="221b9-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="221b9-111">Finance and Operations 應用程式中的專案進度和時間追蹤</span><span class="sxs-lookup"><span data-stu-id="221b9-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="221b9-112">專案和非專案費用的費用管理體驗，包括使用 OCR 功能擷取收據</span><span class="sxs-lookup"><span data-stu-id="221b9-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="221b9-113">使用企業級銷售稅和生效日期匯率系統的發票請款</span><span class="sxs-lookup"><span data-stu-id="221b9-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="221b9-114">WIP 會計和應計項目的可設定專案群組</span><span class="sxs-lookup"><span data-stu-id="221b9-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="221b9-115">專案營收確認</span><span class="sxs-lookup"><span data-stu-id="221b9-115">Project revenue recognition</span></span>

<span data-ttu-id="221b9-116">這種部署類型也提供 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 應用程式所提供之功能的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="221b9-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="221b9-117">選取此部署類型以將 Dynamics 365 Project Operations 用於完整專案生命週期，包括下列主要需求：</span><span class="sxs-lookup"><span data-stu-id="221b9-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="221b9-118">廣泛的專案管理系統，可為排程和財務管理內部和計費專案的庫存項目和工作/生產訂單成本。</span><span class="sxs-lookup"><span data-stu-id="221b9-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="221b9-119">組織已經有 Dynamics 365 Finance 或 Dynamics 365 Supply Chain and Manufacturing 應用程式，而且整合專案型交易將會簡化資料存取和報告需求。</span><span class="sxs-lookup"><span data-stu-id="221b9-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="221b9-120">一個功能齊全的費用管理系統，包括用於追蹤專案和非專案費用的政策執行和報銷。</span><span class="sxs-lookup"><span data-stu-id="221b9-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="221b9-121">企業級銷售稅和匯率引擎，用於為專案產生面向客戶的發票。</span><span class="sxs-lookup"><span data-stu-id="221b9-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="221b9-122">符合國際財務報告準則 (IFRS) 的專案會計和營收確認系統。</span><span class="sxs-lookup"><span data-stu-id="221b9-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]