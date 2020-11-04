---
title: 啟用 Project Finder Mobile 應用程式功能
description: 如何啟用 Project Service 的 Project Finder Mobile 應用程式功能
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087507"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="b0d51-103">啟用 Project Finder Mobile 應用程式功能 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b0d51-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b0d51-104">您的資源可以在手機上透過 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]使用 Project Finder Mobile 應用程式，尋找新專案進行處理及更新其技能集。</span><span class="sxs-lookup"><span data-stu-id="b0d51-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="b0d51-105">應用程式適用於 [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] 手機和 [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]。</span><span class="sxs-lookup"><span data-stu-id="b0d51-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="b0d51-106">您需要在參數設定中為組織單位設定一些選項，才能允許使用者檢視專案的資源需求及更新其技能。</span><span class="sxs-lookup"><span data-stu-id="b0d51-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b0d51-107">Project Finder Mobile 應用程式僅適用於 [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]，無法搭配內部部署安裝使用。</span><span class="sxs-lookup"><span data-stu-id="b0d51-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="b0d51-108">移至 **Project Service > 參數** 。</span><span class="sxs-lookup"><span data-stu-id="b0d51-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="b0d51-109">按一下您要使用的參數設定，允許 Project Finder Mobile 應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="b0d51-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="b0d51-110">在 **一般** 區域中，將 **資源看得到資源需求** 設定為 **是** 。</span><span class="sxs-lookup"><span data-stu-id="b0d51-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="b0d51-111">將 **允許資源更新技能** 設定為 **是** 。</span><span class="sxs-lookup"><span data-stu-id="b0d51-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="b0d51-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="b0d51-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="b0d51-113">這是全域設定。</span><span class="sxs-lookup"><span data-stu-id="b0d51-113">This is a global setting.</span></span> <span data-ttu-id="b0d51-114">專案經理可以設定個別專案是否可在該專案的 **專案團隊** 頁面上看見。</span><span class="sxs-lookup"><span data-stu-id="b0d51-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="b0d51-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="b0d51-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="b0d51-116">電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="b0d51-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="b0d51-117">會傳送關於資源要求的電子郵件給下列收件者，於下列時機：</span><span class="sxs-lookup"><span data-stu-id="b0d51-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="b0d51-118">收件者</span><span class="sxs-lookup"><span data-stu-id="b0d51-118">Recipient</span></span>|<span data-ttu-id="b0d51-119">活動</span><span class="sxs-lookup"><span data-stu-id="b0d51-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="b0d51-120">專案經理</span><span class="sxs-lookup"><span data-stu-id="b0d51-120">Project manager</span></span>|<span data-ttu-id="b0d51-121">- 當資源使用 Project Finder Mobile 應用程式註冊專案時。</span><span class="sxs-lookup"><span data-stu-id="b0d51-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="b0d51-122">資源</span><span class="sxs-lookup"><span data-stu-id="b0d51-122">Resource</span></span>|<span data-ttu-id="b0d51-123">- 當資源註冊的專案工作已由另一個資源履行時。</span><span class="sxs-lookup"><span data-stu-id="b0d51-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="b0d51-124">- 當其技能核准要求已核准或遭拒時。</span><span class="sxs-lookup"><span data-stu-id="b0d51-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="b0d51-125">- 當其專案註冊要求已核准或遭拒時。</span><span class="sxs-lookup"><span data-stu-id="b0d51-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="b0d51-126">隱私權注意事項</span><span class="sxs-lookup"><span data-stu-id="b0d51-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="b0d51-127">請參閱</span><span class="sxs-lookup"><span data-stu-id="b0d51-127">See Also</span></span>  
 [<span data-ttu-id="b0d51-128">設定資源</span><span class="sxs-lookup"><span data-stu-id="b0d51-128">Set up resources</span></span>](../psa/set-up-resources.md)
