---
title: 產品型合約服務內容概觀 - 精簡
description: 此主題提供有關產品型合約服務內容的資訊。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177898"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="72e53-103">產品型合約服務內容概觀 - 精簡</span><span class="sxs-lookup"><span data-stu-id="72e53-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="72e53-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="72e53-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72e53-105">您可以在 Dynamics 365 Project Operations 中建立產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="72e53-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="72e53-106">產品型合約服務內容可以是手動建立的明細，也可以是產品類別目錄中的項目。</span><span class="sxs-lookup"><span data-stu-id="72e53-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="72e53-107">產品類別目錄</span><span class="sxs-lookup"><span data-stu-id="72e53-107">Product catalog</span></span>

<span data-ttu-id="72e53-108">產品類別目錄中的產品有預設單位和單位群組。</span><span class="sxs-lookup"><span data-stu-id="72e53-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="72e53-109">如果有數種產品共用同一組屬性，您可以建立同樣有這些屬性的產品系列。</span><span class="sxs-lookup"><span data-stu-id="72e53-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="72e53-110">一個產品系列中所有的產品都會繼承同一組屬性。</span><span class="sxs-lookup"><span data-stu-id="72e53-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="72e53-111">例如，公司銷售各種不同軟體的訂閱授權。</span><span class="sxs-lookup"><span data-stu-id="72e53-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="72e53-112">所有訂閱軟體都有下列兩個屬性：</span><span class="sxs-lookup"><span data-stu-id="72e53-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="72e53-113">使用者數目</span><span class="sxs-lookup"><span data-stu-id="72e53-113">Number of users</span></span>
- <span data-ttu-id="72e53-114">訂閱期間 (以月為單位)</span><span class="sxs-lookup"><span data-stu-id="72e53-114">Subscription duration (in months)</span></span>

<span data-ttu-id="72e53-115">若要維護此類型的目錄，請建立名為 **訂閱軟體** 的產品系列。</span><span class="sxs-lookup"><span data-stu-id="72e53-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="72e53-116">將 **使用者數目** 及 **訂閱期間** 屬性新增至產品系列。</span><span class="sxs-lookup"><span data-stu-id="72e53-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="72e53-117">然後，將個別產品新增至 **訂閱軟體** 產品系列。</span><span class="sxs-lookup"><span data-stu-id="72e53-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="72e53-118">將產品類別目錄項目新增至專案合約</span><span class="sxs-lookup"><span data-stu-id="72e53-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="72e53-119">專案合約有兩種類型的明細區段，即專案型和產品型。</span><span class="sxs-lookup"><span data-stu-id="72e53-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="72e53-120">產品型明細包含合約中產品價目表的所有產品和單位。</span><span class="sxs-lookup"><span data-stu-id="72e53-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="72e53-121">您可以新增不屬於合約產品價目表的產品。</span><span class="sxs-lookup"><span data-stu-id="72e53-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="72e53-122">您可以從其他價目表選取產品，也可以直接從產品類別目錄選取產品。</span><span class="sxs-lookup"><span data-stu-id="72e53-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="72e53-123">直接從產品類別目錄選取產品時，該產品的預設價目表可用來取得產品的銷售價格。</span><span class="sxs-lookup"><span data-stu-id="72e53-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="72e53-124">如果未設定預設價目表，價格會設定為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="72e53-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="72e53-125">如果合約服務內容是根據產品類別目錄所建立，您可以直接在合約服務內容上覆寫銷售價格。</span><span class="sxs-lookup"><span data-stu-id="72e53-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="72e53-126">合約服務內容的 **定價** 欄位有兩個值：</span><span class="sxs-lookup"><span data-stu-id="72e53-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="72e53-127">**自訂定價**</span><span class="sxs-lookup"><span data-stu-id="72e53-127">**Override pricing**</span></span>
- <span data-ttu-id="72e53-128">**使用預設**</span><span class="sxs-lookup"><span data-stu-id="72e53-128">**Use default**</span></span>

<span data-ttu-id="72e53-129">如果將 **定價** 欄位設定為 **自訂價格**，就不會設定預設價格。</span><span class="sxs-lookup"><span data-stu-id="72e53-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="72e53-130">輸入合約服務內容上的產品價格。</span><span class="sxs-lookup"><span data-stu-id="72e53-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="72e53-131">如果將此欄位設定為 **使用預設值**，則會使用預設銷售價，而且無法編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="72e53-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="72e53-132">安裝 Project Operations 之後，合約的產品型明細上會輸入預設銷售價格。</span><span class="sxs-lookup"><span data-stu-id="72e53-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="72e53-133">**定價** 欄位會設定為 **自訂價格**，因此您可以編輯合約服務內容上的預設價格。</span><span class="sxs-lookup"><span data-stu-id="72e53-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="72e53-134">這是 Project Operations 覆寫 Dynamics 365 Sales 中產品型明細的特有行為。</span><span class="sxs-lookup"><span data-stu-id="72e53-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
