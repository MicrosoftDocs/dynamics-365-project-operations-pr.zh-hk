---
title: 定義技能和熟練度
description: 此主題提供有關如何設定熟練模型以評等資源的資訊。
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015358"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="5c88b-103">定義技能和熟練度</span><span class="sxs-lookup"><span data-stu-id="5c88b-103">Define skills and proficiencies</span></span>

<span data-ttu-id="5c88b-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5c88b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c88b-105">技能是在 Dynamics 365 Project Operations 與 (如果存在) Dynamics 365 Field Service 之間共用的資源特性。</span><span class="sxs-lookup"><span data-stu-id="5c88b-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="5c88b-106">若要在 Project Operations 中維護技能存放庫，請移至 **資源** \> **資源技能**。</span><span class="sxs-lookup"><span data-stu-id="5c88b-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="5c88b-107">使用熟練度模型來評等資源</span><span class="sxs-lookup"><span data-stu-id="5c88b-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="5c88b-108">資源的技能由熟練程度模型所評等。</span><span class="sxs-lookup"><span data-stu-id="5c88b-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="5c88b-109">個別評等是在熟練度模型中。</span><span class="sxs-lookup"><span data-stu-id="5c88b-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="5c88b-110">若要建立熟練度模型，請移至 **資源**\>**熟練度模型**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="5c88b-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="5c88b-111">在新的評等模型中，指定最小評等值、最大評等值以及要加以評等的實體。</span><span class="sxs-lookup"><span data-stu-id="5c88b-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="5c88b-112">在 **評等值** 子格中，您可以定義從最小值到最大值的不同評等值。</span><span class="sxs-lookup"><span data-stu-id="5c88b-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="5c88b-113">這些評等值會顯示在 **資源需求**、**排程面板和** 和 **排程小幫手** 篩選上。</span><span class="sxs-lookup"><span data-stu-id="5c88b-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]