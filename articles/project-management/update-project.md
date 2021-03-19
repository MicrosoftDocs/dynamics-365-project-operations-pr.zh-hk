---
title: 更新專案
description: 本主題提供有關更新 Project Operations 中專案的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286410"
---
# <a name="update-a-project"></a><span data-ttu-id="c18db-103">更新專案</span><span class="sxs-lookup"><span data-stu-id="c18db-103">Update a project</span></span>

<span data-ttu-id="c18db-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="c18db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c18db-105">以下是建立專案後可在其中更新的欄位摘要，以及這些更新作業的任何適用含意。</span><span class="sxs-lookup"><span data-stu-id="c18db-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="c18db-106">專案詳細資料欄位</span><span class="sxs-lookup"><span data-stu-id="c18db-106">Project detail fields</span></span>

- <span data-ttu-id="c18db-107">**名稱**：選取專案的標題。</span><span class="sxs-lookup"><span data-stu-id="c18db-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="c18db-108">**描述**：專案的概觀。</span><span class="sxs-lookup"><span data-stu-id="c18db-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="c18db-109">**客戶**：專案將交付到的公司。</span><span class="sxs-lookup"><span data-stu-id="c18db-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="c18db-110">**行事曆範本**：專案的工作時數。</span><span class="sxs-lookup"><span data-stu-id="c18db-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="c18db-111">當欄位變更時，會重新計算整個排程。</span><span class="sxs-lookup"><span data-stu-id="c18db-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="c18db-112">**貨幣**：專案的貨幣。</span><span class="sxs-lookup"><span data-stu-id="c18db-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="c18db-113">此欄位是根據在合約單位中定義的貨幣來設定預設值。</span><span class="sxs-lookup"><span data-stu-id="c18db-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="c18db-114">更新合約單位時，也會更新此欄位。</span><span class="sxs-lookup"><span data-stu-id="c18db-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="c18db-115">**合約單位**：代表公司中主要負責贏得銷售和管理客戶工作與服務交付之群組或部門的組織單位。</span><span class="sxs-lookup"><span data-stu-id="c18db-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="c18db-116">**專案經理**：有權責可以審查和核准時間項目及費用的專案團隊成員。</span><span class="sxs-lookup"><span data-stu-id="c18db-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="c18db-117">評估值欄位</span><span class="sxs-lookup"><span data-stu-id="c18db-117">Estimate fields</span></span>

- <span data-ttu-id="c18db-118">**估計開始日期**：專案將開始的日期。</span><span class="sxs-lookup"><span data-stu-id="c18db-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="c18db-119">更新此欄位時，專案中的任何工作都會與開始日期成比例原則移動新的開始日期。</span><span class="sxs-lookup"><span data-stu-id="c18db-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="c18db-120">**完成日期**：排定專案結束的日期。</span><span class="sxs-lookup"><span data-stu-id="c18db-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="c18db-121">**投入量**：專案的估計投入量。</span><span class="sxs-lookup"><span data-stu-id="c18db-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="c18db-122">將工作新增至專案時，此欄位將無法再編輯。</span><span class="sxs-lookup"><span data-stu-id="c18db-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="c18db-123">**估計人力成本**：專案的估計人力成本。</span><span class="sxs-lookup"><span data-stu-id="c18db-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="c18db-124">將人力成本新增至專案時，此欄位將無法再編輯。</span><span class="sxs-lookup"><span data-stu-id="c18db-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="c18db-125">**估計費用**：專案的估計位於。</span><span class="sxs-lookup"><span data-stu-id="c18db-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="c18db-126">將費用新增至專案時，此欄位將無法再編輯。</span><span class="sxs-lookup"><span data-stu-id="c18db-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="c18db-127">專案實際值欄位</span><span class="sxs-lookup"><span data-stu-id="c18db-127">Project actual fields</span></span>
- <span data-ttu-id="c18db-128">**實際開始**：專案開始的日期。</span><span class="sxs-lookup"><span data-stu-id="c18db-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="c18db-129">**實際完成**：可在專案完成時進行更新。</span><span class="sxs-lookup"><span data-stu-id="c18db-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="c18db-130">專案狀態欄位</span><span class="sxs-lookup"><span data-stu-id="c18db-130">Project status fields</span></span>

- <span data-ttu-id="c18db-131">**整體專案狀態**：專案經理所提供的整體專案健全狀況。</span><span class="sxs-lookup"><span data-stu-id="c18db-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="c18db-132">**註解**：專案經理所提供有關專案目前健全狀況的敘述。</span><span class="sxs-lookup"><span data-stu-id="c18db-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]