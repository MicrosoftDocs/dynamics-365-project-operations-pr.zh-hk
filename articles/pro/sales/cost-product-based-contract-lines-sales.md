---
title: 計算產品型合約服務內容的成本 - 精簡
description: 本主題提供有關建立產品型合約服務內容的資訊
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003568"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="49b16-103">計算產品型合約服務內容的成本 - 精簡</span><span class="sxs-lookup"><span data-stu-id="49b16-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="49b16-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="49b16-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="49b16-105">Dynamics 365 Project Operations 中的產品型合約服務內容包含 **成本價** 欄位，其中儲存用於計算下游獲利率的產品成本價。</span><span class="sxs-lookup"><span data-stu-id="49b16-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="49b16-106">建立目錄產品的產品型合約服務內容時，該合約服務內容的成本預設是源自產品目錄中的 **標準成本** 欄位。</span><span class="sxs-lookup"><span data-stu-id="49b16-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="49b16-107">產品類別目錄中的 **標準成本** 欄位是以組織的基準貨幣來設定。</span><span class="sxs-lookup"><span data-stu-id="49b16-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="49b16-108">合約服務內容預設使用單位成本時，此成本會轉換為合約上的銷售貨幣。</span><span class="sxs-lookup"><span data-stu-id="49b16-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="49b16-109">產品型合約服務內容的單位成本</span><span class="sxs-lookup"><span data-stu-id="49b16-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="49b16-110">產品型合約服務內容上設有單位成本，可讓每個銷售單位各有不同的產品成本。</span><span class="sxs-lookup"><span data-stu-id="49b16-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="49b16-111">雖然不一定需要，但還是存在供應商可能給予客戶產品成本折扣的特定案例。</span><span class="sxs-lookup"><span data-stu-id="49b16-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="49b16-112">試想以下情況：</span><span class="sxs-lookup"><span data-stu-id="49b16-112">Consider the following scenario:</span></span>

<span data-ttu-id="49b16-113">Fabrikam Robotics 正在 Adatum Corporation 的裝配線上安裝機器人手臂。</span><span class="sxs-lookup"><span data-stu-id="49b16-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="49b16-114">Fabrikam 提供安裝服務，但機器人手臂是來自 Trey Research。</span><span class="sxs-lookup"><span data-stu-id="49b16-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="49b16-115">如果在 Adatum Corporation 安裝機器人手臂會為 Trey Research 的機器人手臂開拓新市場，他們就可能會向 Fabrikam 提供這筆交易的特殊折扣。</span><span class="sxs-lookup"><span data-stu-id="49b16-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="49b16-116">在此案例中，Fabrikam 會為機器人手臂建立產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="49b16-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="49b16-117">此合約的單位成本已輸入。</span><span class="sxs-lookup"><span data-stu-id="49b16-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="49b16-118">此成本與 Trey Research 的機器人手臂成本不同。</span><span class="sxs-lookup"><span data-stu-id="49b16-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]