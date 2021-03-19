---
title: 每日津貼
description: 本主題提供有關費用管理中所用每日津貼規則的資訊。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276330"
---
# <a name="per-diems"></a><span data-ttu-id="185e0-103">每日津貼</span><span class="sxs-lookup"><span data-stu-id="185e0-103">Per diems</span></span>

<span data-ttu-id="185e0-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="185e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="185e0-105">每日津貼是支付給出差工作者的補貼。</span><span class="sxs-lookup"><span data-stu-id="185e0-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="185e0-106">在費用管理中，您可以建立各種差旅狀況的每日津貼規則。</span><span class="sxs-lookup"><span data-stu-id="185e0-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="185e0-107">每日津貼費率可以根據一年時節、出差地點或兩者來定。</span><span class="sxs-lookup"><span data-stu-id="185e0-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="185e0-108">建立每日津貼規則時，您可以指定如果工作者獲得免費贈送的餐飲或服務時，每日津貼費率會扣留的百分比。</span><span class="sxs-lookup"><span data-stu-id="185e0-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="185e0-109">您也可以設定每日津貼費率可套用至工作者差旅的最小及最大時數。</span><span class="sxs-lookup"><span data-stu-id="185e0-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="185e0-110">組態</span><span class="sxs-lookup"><span data-stu-id="185e0-110">Configuration</span></span> 

1. <span data-ttu-id="185e0-111">若要新增每日津貼地點，請移至 **設定** > **計算和代碼** > **每日津貼地點**。</span><span class="sxs-lookup"><span data-stu-id="185e0-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="185e0-112">針對上述新增的每個地點，選取在住宿、餐飲及其他費用的特定開始與結束日期之間有效的每日津貼費率和貨幣。</span><span class="sxs-lookup"><span data-stu-id="185e0-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="185e0-113">每日津貼費率和貨幣是在 **設定** > **計算和代碼** > **每日津貼** 底下進行設定。</span><span class="sxs-lookup"><span data-stu-id="185e0-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="185e0-114">在 **每日津貼地點** 頁面上，設定每日津貼費率分級。</span><span class="sxs-lookup"><span data-stu-id="185e0-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="185e0-115">每日津貼費率分級可讓您定義住宿、餐飲及其他費用每日補貼的分割百分比。</span><span class="sxs-lookup"><span data-stu-id="185e0-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="185e0-116">若要指定早餐、午餐或晚餐的餐費百分比，請更新 **每日津貼** 索引標籤 **費用管理參數** 頁面上的欄位 。</span><span class="sxs-lookup"><span data-stu-id="185e0-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="185e0-117">提交使用每日津貼的費用</span><span class="sxs-lookup"><span data-stu-id="185e0-117">Submit expenses using per diem</span></span>
<span data-ttu-id="185e0-118">若要提交使用每日津貼的費用，請在建立費用報表時使用 **每日津貼** 費用類別。</span><span class="sxs-lookup"><span data-stu-id="185e0-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="185e0-119">輸入 **每個津貼開始日期**、**到目前為止的每日津貼** 和 **每日津貼地點**。</span><span class="sxs-lookup"><span data-stu-id="185e0-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="185e0-120">金額會根據所選地點的每日津貼費率進行計算，而餐費扣減則是根據每日津貼費率分級所計算。</span><span class="sxs-lookup"><span data-stu-id="185e0-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]