---
title: 了解專案狀態
description: 本主題提供有關在 Dynamics 365 Project Operations 中指派給專案的狀態的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965703"
---
# <a name="understand-project-status"></a><span data-ttu-id="73d1b-103">了解專案狀態</span><span class="sxs-lookup"><span data-stu-id="73d1b-103">Understand project status</span></span>

<span data-ttu-id="73d1b-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="73d1b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="73d1b-105"> **專案實體** 頁面的 **狀態** 區段會根據成本與投入量提供專案健全狀況的摘要。</span><span class="sxs-lookup"><span data-stu-id="73d1b-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="73d1b-106">狀態摘要欄位</span><span class="sxs-lookup"><span data-stu-id="73d1b-106">Status summary fields</span></span>

- <span data-ttu-id="73d1b-107"> **整體專案狀態** 欄位是顯示專案整體狀態的可編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="73d1b-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="73d1b-108">此欄位會使用色彩代碼 (例如綠色、黃色和紅色) 來表示風險增加。</span><span class="sxs-lookup"><span data-stu-id="73d1b-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="73d1b-109"> **註解** 欄位可讓專案經理輸入關於狀態的特定註解。</span><span class="sxs-lookup"><span data-stu-id="73d1b-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="73d1b-110"> **狀態更新日期** 欄位無法編輯。</span><span class="sxs-lookup"><span data-stu-id="73d1b-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="73d1b-111">此欄位中的值是指示狀態上次更新時間的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="73d1b-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="73d1b-112"> **排程效能** 和 **成本績效** 欄位是從追蹤網格進行設定。</span><span class="sxs-lookup"><span data-stu-id="73d1b-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="73d1b-113">當 **投入量追蹤** 檢視表中根節點的排程與成本差異為正值時，您可以將這些欄位更新為 **提前**。</span><span class="sxs-lookup"><span data-stu-id="73d1b-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="73d1b-114">當根節點的排程與成本差異是負值時，可以將這些欄位設定為 **落後**。</span><span class="sxs-lookup"><span data-stu-id="73d1b-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>