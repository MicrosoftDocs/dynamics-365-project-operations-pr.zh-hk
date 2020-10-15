---
title: 資源管理模式概觀
description: 本主題提供有關 Dynamics 365 Project Operations 中資源管理功能的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930118"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="f1c27-103">資源管理模式概觀</span><span class="sxs-lookup"><span data-stu-id="f1c27-103">Resource management modes overview</span></span>

<span data-ttu-id="f1c27-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f1c27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f1c27-105">Dynamics 365 Project Operations 支援兩種模式，讓您執行整體預約流程。</span><span class="sxs-lookup"><span data-stu-id="f1c27-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="f1c27-106">管理模式是以專案參數來定義，如果您的業務需求變更，則可加以修改。</span><span class="sxs-lookup"><span data-stu-id="f1c27-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="f1c27-107">集中模式</span><span class="sxs-lookup"><span data-stu-id="f1c27-107">Central mode</span></span>
<span data-ttu-id="f1c27-108">對於將資源集中配置給專案的組織，集中模式提供的方式確保專案經理可以在專案層級定義資源需求。</span><span class="sxs-lookup"><span data-stu-id="f1c27-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="f1c27-109">履行資源需求的職責已委派給資源經理。</span><span class="sxs-lookup"><span data-stu-id="f1c27-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="f1c27-110">專案經理可以接受或拒絕資源管理員提議的資源。</span><span class="sxs-lookup"><span data-stu-id="f1c27-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![集中模式](./media/resource-management-central.png)

<span data-ttu-id="f1c27-112">若要使用集中模式管理資源，請參閱：</span><span class="sxs-lookup"><span data-stu-id="f1c27-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="f1c27-113">指派一般可預約資源至工作，並產生資源需求</span><span class="sxs-lookup"><span data-stu-id="f1c27-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="f1c27-114">透過資源需求預約具名資源</span><span class="sxs-lookup"><span data-stu-id="f1c27-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="f1c27-115">送出資源要求</span><span class="sxs-lookup"><span data-stu-id="f1c27-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="f1c27-116">履行資源要求</span><span class="sxs-lookup"><span data-stu-id="f1c27-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="f1c27-117">接受或拒絕資源要求提案的專案資源</span><span class="sxs-lookup"><span data-stu-id="f1c27-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="f1c27-118">混合模式</span><span class="sxs-lookup"><span data-stu-id="f1c27-118">Hybrid mode</span></span>
<span data-ttu-id="f1c27-119">對於需要彈性配置資源的組織，混合模式使專案經理和資源管理員能夠預約資源。</span><span class="sxs-lookup"><span data-stu-id="f1c27-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![混合模式](./media/resource-management-hybrid.png)

<span data-ttu-id="f1c27-121">除了支援的集中模式程序之外，也請參閱下列主題，以便在混合模式下管理所有其他支援的預約流程：</span><span class="sxs-lookup"><span data-stu-id="f1c27-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="f1c27-122">將資源直接預約給專案：</span><span class="sxs-lookup"><span data-stu-id="f1c27-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="f1c27-123">將具名可預約資源預約給專案團隊並指派工作</span><span class="sxs-lookup"><span data-stu-id="f1c27-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="f1c27-124">透過資源需求預約資源：</span><span class="sxs-lookup"><span data-stu-id="f1c27-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="f1c27-125">指派一般可預約資源至工作，並產生資源需求</span><span class="sxs-lookup"><span data-stu-id="f1c27-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="f1c27-126">透過資源需求預約具名資源</span><span class="sxs-lookup"><span data-stu-id="f1c27-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)