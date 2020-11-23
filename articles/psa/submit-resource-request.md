---
title: 送出資源要求
description: 本主題提供有關送出專案資源要求的資訊。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131324"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="0785a-103">送出資源要求</span><span class="sxs-lookup"><span data-stu-id="0785a-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0785a-104">您可以將產生的資源需求當做資源要求送出。</span><span class="sxs-lookup"><span data-stu-id="0785a-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="0785a-105">隨後會將要求傳送給資源管理員來履行。</span><span class="sxs-lookup"><span data-stu-id="0785a-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="0785a-106">在 Project Service Automation (PSA) 的 **專案** 頁面上，按一下 **團隊** 索引標籤以檢視可預約資源清單。</span><span class="sxs-lookup"><span data-stu-id="0785a-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="0785a-107">從清單中選取具有資源需求的一般資源，然後按一下 **送出要求**。</span><span class="sxs-lookup"><span data-stu-id="0785a-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![送出資源要求](media/RM-how-to-18.png)

<span data-ttu-id="0785a-109">一般團隊成員的要求狀態會變更為 **已送出**。</span><span class="sxs-lookup"><span data-stu-id="0785a-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="0785a-110">資源管理員履行要求之後，如果資源管理員是使用具名資源的預約來履行要求，則會以具名資源取代一般資源。</span><span class="sxs-lookup"><span data-stu-id="0785a-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="0785a-111">否則，一般資源仍保留在團隊中，如果資源管理員已提案建議具名資源，則要求狀態將會變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="0785a-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
