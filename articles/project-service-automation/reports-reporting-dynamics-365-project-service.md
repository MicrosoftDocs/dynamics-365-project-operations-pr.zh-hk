---
title: 報表首頁
description: 本主題提供有關 Dynamics 365 Project Service Automation 中報表的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ee9bdfc6-123d-4146-8706-eab76fa37b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 42e24f42fd80b445718f81f4ff40e52c8cdaa7ba
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757318"
---
# <a name="reporting-home-page"></a><span data-ttu-id="3ef79-103">報表首頁</span><span class="sxs-lookup"><span data-stu-id="3ef79-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3ef79-104">Microsoft Dynamics 365 Project Service Automation 可讓專案型組織有效管理其業務運作。</span><span class="sxs-lookup"><span data-stu-id="3ef79-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="3ef79-105">在任何專案上，團隊成員都必須管理商機、報價，並規劃工作、為專案提供資源、根據計畫管理工作、處理工作帳務，然後完成專案。</span><span class="sxs-lookup"><span data-stu-id="3ef79-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="3ef79-106">就營運狀態提出報表的能力，對判斷組織的健全狀況並採用任何必要更正動作，至關重要。</span><span class="sxs-lookup"><span data-stu-id="3ef79-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="3ef79-107">PSA 使用 Microsoft Dynamics 365 報告方法與技術來提供其所有報表。</span><span class="sxs-lookup"><span data-stu-id="3ef79-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="3ef79-108">如需報表選項的詳細資訊，請參閱 [Dynamics 365 Customer Engagement (on-premises) 版本 9 的報表撰寫指南](../analytics/reporting-analytics-with-dynamics-365.md)。</span><span class="sxs-lookup"><span data-stu-id="3ef79-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](../analytics/reporting-analytics-with-dynamics-365.md).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="3ef79-109">報表精靈</span><span class="sxs-lookup"><span data-stu-id="3ef79-109">Report Wizard</span></span>

<span data-ttu-id="3ef79-110">報表精靈可讓非開發人員建立簡單報表。</span><span class="sxs-lookup"><span data-stu-id="3ef79-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="3ef79-111">因為應用程式是在現有平台的基礎上建置，體驗與[使用報表精靈建立或編輯報表](../basics/create-edit-copy-report-wizard.md)中所記載的並無二致。</span><span class="sxs-lookup"><span data-stu-id="3ef79-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](../basics/create-edit-copy-report-wizard.md).</span></span> <span data-ttu-id="3ef79-112">但是，您會用到 Project Service Automation 特有的實體。</span><span class="sxs-lookup"><span data-stu-id="3ef79-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="3ef79-113">自訂 SQL Server Reporting Services 報表</span><span class="sxs-lookup"><span data-stu-id="3ef79-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="3ef79-114">如果您的業務需要無法使用報表精靈建立的特定報表，則可以建立自訂報表。</span><span class="sxs-lookup"><span data-stu-id="3ef79-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="3ef79-115">您必須安裝 Microsoft Visual Studio，以及適當的 Microsoft SQL Server Data Tools 與報表製作擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3ef79-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="3ef79-116">如需工具和版本的詳細資訊，請參閱[使用 SQL Server Data Tools  的報表撰寫環境](../analytics/report-writing-environment-using-sql-server-data-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="3ef79-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span></span> <span data-ttu-id="3ef79-117">如需有關如何建立自訂報表的詳細資訊，請參閱[使用 SQL Server Data Tools 建立新報表](../analytics/create-a-new-report-using-sql-server-data-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="3ef79-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="3ef79-118">Power BI 見解探索應用程式</span><span class="sxs-lookup"><span data-stu-id="3ef79-118">Power BI insights apps</span></span>

<span data-ttu-id="3ef79-119">Microsoft Power BI 和 Dynamics 365 合起來以見解探索應用程式的形式，提供您有效的方法來使用您的資料。</span><span class="sxs-lookup"><span data-stu-id="3ef79-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="3ef79-120">如需有關見解探索應用程式可用性的詳細資訊，請參閱 [Power BI 見解探索應用程式頁面](https://powerbi.microsoft.com/power-bi-insights-apps/)。</span><span class="sxs-lookup"><span data-stu-id="3ef79-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="3ef79-121">其他資源</span><span class="sxs-lookup"><span data-stu-id="3ef79-121">Additional resources</span></span>
<span data-ttu-id="3ef79-122">如需 PSA 中報表功能的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3ef79-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="3ef79-123">使用 Project Service 資料模型</span><span class="sxs-lookup"><span data-stu-id="3ef79-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="3ef79-124">儀表板 </span><span class="sxs-lookup"><span data-stu-id="3ef79-124">Dashboards</span></span>](reports-dashboards.md)

