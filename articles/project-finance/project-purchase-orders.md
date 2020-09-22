---
title: 專案採購單
description: 本文說明各種可用來建立專案採購單的方法。 您使用的方法取決於採購單的用途，以及專案的採購項目何時取用和收費。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757253"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="ce3fd-104">專案採購單</span><span class="sxs-lookup"><span data-stu-id="ce3fd-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce3fd-105">本文說明各種可用來建立專案採購單的方法。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="ce3fd-106">您使用的方法取決於採購單的用途，以及專案的採購項目何時取用和收費。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="ce3fd-107">建立採購單的方法</span><span class="sxs-lookup"><span data-stu-id="ce3fd-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="ce3fd-108">您可以使用下列其中一個方法，在 [專案管理與會計] 中建立採購單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="ce3fd-109">採購單的用途決定採購單何時使用，以及因此在何時向專案收取項目的費用。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce3fd-110">方法</span><span class="sxs-lookup"><span data-stu-id="ce3fd-110">Method</span></span></th>
<th><span data-ttu-id="ce3fd-111">用途</span><span class="sxs-lookup"><span data-stu-id="ce3fd-111">Purpose</span></span></th>
<th><span data-ttu-id="ce3fd-112">取用項目</span><span class="sxs-lookup"><span data-stu-id="ce3fd-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce3fd-113">直接從專案建立採購單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="ce3fd-114">使用此方法，向外部供應商購買要在專案上取用的項目。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="ce3fd-115">您可以用兩種方式建立採購單：</span><span class="sxs-lookup"><span data-stu-id="ce3fd-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="ce3fd-116">從專案本身。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-116">From the project itself.</span></span> <span data-ttu-id="ce3fd-117">在此情況下，已經為採購單定義專案。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="ce3fd-118">瀏覽至專案採購單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="ce3fd-119">您必須供應商和專案都選取，才能建立其採購單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="ce3fd-120">更新供應商發票時，會取用項目。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce3fd-121">從銷售訂單建立採購單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="ce3fd-122">從專案建立銷售訂單時，使用此方法來購買項目。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="ce3fd-123">開立銷售訂單的發票給客戶時，會取用項目。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce3fd-124">從項目需求建立採購單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="ce3fd-125">從專案建立項目需求時，使用此方法來購買項目。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="ce3fd-126">更新項目需求裝箱單時，會取用項目。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="ce3fd-127">更新供應商發票或裝箱單時，系統會提示更新項目需求上的裝箱單。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="ce3fd-128">如需詳細資訊，請參閱[從項目需求擷取採購單上的項目](tasks/receive-items-purchase-order-item-requirement.md)。</span><span class="sxs-lookup"><span data-stu-id="ce3fd-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

