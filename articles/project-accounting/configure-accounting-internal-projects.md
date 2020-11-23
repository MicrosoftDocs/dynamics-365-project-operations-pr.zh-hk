---
title: 設定內部專案會計
description: 本主題提供有關如何為 Project Operations 內部專案設定會計實務的資訊。
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132405"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8e662-103">設定內部專案會計</span><span class="sxs-lookup"><span data-stu-id="8e662-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8e662-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8e662-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8e662-105">內部專案可讓公司追蹤與免收客戶費用活動相關的成本。</span><span class="sxs-lookup"><span data-stu-id="8e662-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8e662-106">內部專案的範例包括：</span><span class="sxs-lookup"><span data-stu-id="8e662-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8e662-107">開發產品 (例如行動應用程式)，以及追蹤與開發相關聯的成本。</span><span class="sxs-lookup"><span data-stu-id="8e662-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8e662-108">管理售前時間與費用。</span><span class="sxs-lookup"><span data-stu-id="8e662-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8e662-109">如果報價已成交，則可以稍後再將此售前內部專案轉換成計費專案。</span><span class="sxs-lookup"><span data-stu-id="8e662-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8e662-110">任何未與 Dynamics 365 Project Operations 中合約建立關聯的專案，都會視為內部專案。</span><span class="sxs-lookup"><span data-stu-id="8e662-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8e662-111">專案成本與營收設定檔不會用來決定專案的會計規則。</span><span class="sxs-lookup"><span data-stu-id="8e662-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8e662-112">內部專案成本一律使用損益原則進行過帳。</span><span class="sxs-lookup"><span data-stu-id="8e662-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8e662-113">用於過帳的總帳科目是在 **總帳過帳設定** 頁面上定義。</span><span class="sxs-lookup"><span data-stu-id="8e662-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8e662-114">時間交易的過帳方式是，借記 **成本** 科目，並貸記 **薪資分攤** 科目。</span><span class="sxs-lookup"><span data-stu-id="8e662-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8e662-115">費用交易的過帳方式是，借記 **成本** 科目，並貸記 **費用抵銷科目**。</span><span class="sxs-lookup"><span data-stu-id="8e662-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="8e662-116">將交易過帳到專案之後，如果專案與專案合約相關聯，則系統會沖銷所有累計交易，並建立新的計費交易。</span><span class="sxs-lookup"><span data-stu-id="8e662-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8e662-117">計費交易遵循各自定義於專案成本與營收設定檔的會計規則。</span><span class="sxs-lookup"><span data-stu-id="8e662-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


