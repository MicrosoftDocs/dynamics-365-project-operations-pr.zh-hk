---
title: 公司間開立開票概觀
description: 此主題提供專案的公司間開立發票的資訊與範例。
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287355"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="50eeb-103">公司間開立開票概觀</span><span class="sxs-lookup"><span data-stu-id="50eeb-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="50eeb-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="50eeb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="50eeb-105">您的組織可能有多個會在專案中互相轉移產品與服務的部門、子公司及其他法律實體。</span><span class="sxs-lookup"><span data-stu-id="50eeb-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="50eeb-106">提供服務或產品的法律實體稱為 *貸方法律實體*。</span><span class="sxs-lookup"><span data-stu-id="50eeb-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="50eeb-107">接收服務或產品的法律實體稱為 *借方法律實體*。</span><span class="sxs-lookup"><span data-stu-id="50eeb-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="50eeb-108">下圖顯示典型案例，其中的兩個法律實體 Contoso Robotics USA (借方法律實體) 和 Contoso Robotics UK (貸方法律實體) 共享資源，為客戶 Adventure Works 交付專案。</span><span class="sxs-lookup"><span data-stu-id="50eeb-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="50eeb-109">在此案例中，Contoso Robotics USA 已簽約要交付工作給 Adventure Works。</span><span class="sxs-lookup"><span data-stu-id="50eeb-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![公司間開立開票](./media/IntercompanyScenario.png) 

<span data-ttu-id="50eeb-111">Dynamics 365 Project Operations 使用以下流程來處理公司間交易：</span><span class="sxs-lookup"><span data-stu-id="50eeb-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="50eeb-112">貸方法律實體的資源透過針對借方法律實體中的專案預約時間和費用，來記錄公司間時間或費用交易。</span><span class="sxs-lookup"><span data-stu-id="50eeb-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="50eeb-113">時間和費用成本透過使用借方公司的單位成本價目表記錄在貸方公司中。</span><span class="sxs-lookup"><span data-stu-id="50eeb-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="50eeb-114">公司間未開單銷售交易透過使用借方公司的單位成本價目表記錄在貸方公司中。</span><span class="sxs-lookup"><span data-stu-id="50eeb-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="50eeb-115">未開單營收是使用專案合約銷售價目表在借方公司中進行記錄。</span><span class="sxs-lookup"><span data-stu-id="50eeb-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="50eeb-116">當記錄未開單營收時，可以向客戶收費。</span><span class="sxs-lookup"><span data-stu-id="50eeb-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="50eeb-117">客戶無需等到公司間發票處理完成。</span><span class="sxs-lookup"><span data-stu-id="50eeb-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="50eeb-118">會在貸方公司中定期建立公司間客戶發票。</span><span class="sxs-lookup"><span data-stu-id="50eeb-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="50eeb-119">發票是手動建立的，或是使用週期自動程序建立。</span><span class="sxs-lookup"><span data-stu-id="50eeb-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="50eeb-120">可以為每個貸方法律實體建立單一發票，或依專案建立不同的發票。</span><span class="sxs-lookup"><span data-stu-id="50eeb-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="50eeb-121">將公司間客戶發票過帳到貸方法律實體中時，將在借方法律實體中建立對應的擱置中廠商發票。</span><span class="sxs-lookup"><span data-stu-id="50eeb-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="50eeb-122">在過帳發票時，擱置中廠商發票中的成本將記錄至專案分類帳。</span><span class="sxs-lookup"><span data-stu-id="50eeb-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="50eeb-123">下圖顯示公司間開立發票，因其與會計事件相關且預期過帳到總帳。</span><span class="sxs-lookup"><span data-stu-id="50eeb-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![公司間流程](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="50eeb-125">其他資源</span><span class="sxs-lookup"><span data-stu-id="50eeb-125">Additional resources</span></span>

- [<span data-ttu-id="50eeb-126">設定公司間開立發票</span><span class="sxs-lookup"><span data-stu-id="50eeb-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="50eeb-127">記錄公司間交易</span><span class="sxs-lookup"><span data-stu-id="50eeb-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="50eeb-128">建立公司間客戶與廠商發票</span><span class="sxs-lookup"><span data-stu-id="50eeb-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]