---
title: 期間類型
description: 此主題提供有關如何設定營收估計的期間類型的資訊。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531599"
---
# <a name="period-types"></a><span data-ttu-id="5b667-103">期間類型</span><span class="sxs-lookup"><span data-stu-id="5b667-103">Period types</span></span>

<span data-ttu-id="5b667-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5b667-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5b667-105">期間類型定義了估計專案營收的頻率。</span><span class="sxs-lookup"><span data-stu-id="5b667-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="5b667-106">此主題提供有關如何設定營收估計的期間類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b667-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="5b667-107">建立與使用期間類型</span><span class="sxs-lookup"><span data-stu-id="5b667-107">Create and work with period types</span></span>
<span data-ttu-id="5b667-108">若要建立和使用期間類型，請完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5b667-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="5b667-109">在您的 Dynamics 365 Finance 環境中，移至 **專案管理和會計** > **設定** > **估計值** > **期間類型**。</span><span class="sxs-lookup"><span data-stu-id="5b667-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="5b667-110">選取 **新增** 以建立新的期間類型。</span><span class="sxs-lookup"><span data-stu-id="5b667-110">Select **New** to create new period type.</span></span> <span data-ttu-id="5b667-111">輸入名稱和描述。</span><span class="sxs-lookup"><span data-stu-id="5b667-111">Enter a name and description.</span></span>
3. <span data-ttu-id="5b667-112">在 **頻率** 欄位中選取值：</span><span class="sxs-lookup"><span data-stu-id="5b667-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="5b667-113">如果您選取 **週**、**兩週**、**半月**、**月**、**日**、**季** 或 **年**，就會使用行事曆來產生期間。</span><span class="sxs-lookup"><span data-stu-id="5b667-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="5b667-114">如果您選取 **分類帳期間**，則會使用總帳設定中的分類帳期間來產生期間。</span><span class="sxs-lookup"><span data-stu-id="5b667-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="5b667-115">如果您選取 **無限制**，則可以指定自訂期間。</span><span class="sxs-lookup"><span data-stu-id="5b667-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="5b667-116">選取期間類型記錄，然後選取 **產生期間**，以建立期間類型的期間。</span><span class="sxs-lookup"><span data-stu-id="5b667-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="5b667-117">根據您所選取的期間頻率，您可以選擇指定開始日期或要產生的期間數。</span><span class="sxs-lookup"><span data-stu-id="5b667-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="5b667-118">選取 **期間** 以檢閱產生的期間。</span><span class="sxs-lookup"><span data-stu-id="5b667-118">Select **Periods** to review generated periods.</span></span>

