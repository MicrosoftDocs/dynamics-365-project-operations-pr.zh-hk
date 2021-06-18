---
title: 將 Azure 訂閱新增至 LCS 專案
description: 本主題提供有關如何將您的 Azure 訂閱連接至 LCS 專案的資訊。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000643"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="79885-103">將 Azure 訂閱新增至 LCS 專案</span><span class="sxs-lookup"><span data-stu-id="79885-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="79885-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="79885-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="79885-105">雲端託管的環境必須使用現有的 Azure 訂閱來進行部署。</span><span class="sxs-lookup"><span data-stu-id="79885-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="79885-106">本主題說明如何將現有的 Azure 訂閱連接至 LCS 專案。</span><span class="sxs-lookup"><span data-stu-id="79885-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="79885-107">授與管理員同意</span><span class="sxs-lookup"><span data-stu-id="79885-107">Grant admin consent</span></span>

1. <span data-ttu-id="79885-108">在 LCS 專案的 **環境** 區段中，選取 **Microsoft Azure 設定**。</span><span class="sxs-lookup"><span data-stu-id="79885-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure 設定](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="79885-110">在 **專案設定** 頁面的 **Azure 連接器** 索引標籤上，選取 **授權**。</span><span class="sxs-lookup"><span data-stu-id="79885-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="79885-111">這可讓環境部署至此專案。</span><span class="sxs-lookup"><span data-stu-id="79885-111">This allows environments to be deployed to this project.</span></span>

![Azure 連接器](./media/2AzureConnectors.png)

3. <span data-ttu-id="79885-113">再次選取 **授權** 以提供管理員同意。</span><span class="sxs-lookup"><span data-stu-id="79885-113">Select **Authorize** again to provide admin consent.</span></span>

![授與管理員同意](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="79885-115">接受權限要求。</span><span class="sxs-lookup"><span data-stu-id="79885-115">Accept the permissions request.</span></span>

![接受權限要求](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="79885-117">授權現已完成。</span><span class="sxs-lookup"><span data-stu-id="79885-117">The authorization is now complete.</span></span> 

![授權成功](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="79885-119">提供 Dynamics 部署服務存取權給您的 Azure 訂閱</span><span class="sxs-lookup"><span data-stu-id="79885-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="79885-120">前往 [Microsoft Azure 帳單](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade)，並選取您的訂閱。</span><span class="sxs-lookup"><span data-stu-id="79885-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="79885-121">Dynamics 部署服務必須存取此訂閱，才能部署環境。</span><span class="sxs-lookup"><span data-stu-id="79885-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure 訂閱詳細資料](./media/6AzureSubscription.png)

2. <span data-ttu-id="79885-123">選取導覽窗格中的 **存取控制 (IAM)**，然後選取 **新增角色指派**。</span><span class="sxs-lookup"><span data-stu-id="79885-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="79885-124">在右側滑桿中，選取 **參與者角色**，然後在提供的清單中尋找並選取 **Dynamics 部署服務**。</span><span class="sxs-lookup"><span data-stu-id="79885-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="79885-125">選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="79885-125">Select **Save**.</span></span>

![訂閱存取](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="79885-127">將訂閱連接器新增至 LCS 專案</span><span class="sxs-lookup"><span data-stu-id="79885-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="79885-128">在 LCS 專案的 **Microsoft Azure 設定** 頁面上，選取 **新增** 以新增連接器。</span><span class="sxs-lookup"><span data-stu-id="79885-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="79885-129">輸入您的 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="79885-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="79885-130">您可以前往 [Azure 入口網站](https://ms.portal.azure.com/)，在畫面左下角的 **設定** 下方找到您的 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="79885-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="79885-131">在 **設定使用 Azure Resource Manager** 欄位中，選取 **是**。</span><span class="sxs-lookup"><span data-stu-id="79885-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="79885-132">請確定 Azure 訂閱 AAD 租用戶網域與您使用中網域擁有的 Azure 訂閱相符，然後選取 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="79885-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="79885-133">在 **Microsoft Azure 設定** 畫面上，選取 **下一步** 以確認。</span><span class="sxs-lookup"><span data-stu-id="79885-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="79885-134">如果在此畫面中收到錯誤，請返回本主題的[提供 Dynamics 部署服務存取權給您的 Azure 訂閱](#provide)一節，並確定您已完成所有的步驟。</span><span class="sxs-lookup"><span data-stu-id="79885-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="79885-135">將 Azure 管理憑證下載至您電腦的本機資料夾。</span><span class="sxs-lookup"><span data-stu-id="79885-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="79885-136">選取訂閱並移至 **設定** > **管理憑證**，以要求 Azure 訂用帳戶管理員將憑證上傳至 Azure 管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="79885-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="79885-137">此憑證可讓 LCS 代表您與 Azure 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="79885-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="79885-138">如果使用者有權存取訂閱，您可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="79885-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="79885-139">選取 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="79885-139">Select  **Next**.</span></span>
8. <span data-ttu-id="79885-140">選取要在其中進行部署的 Azure 區域，並選取接近您打算使用此系統所在位置的資料中心。</span><span class="sxs-lookup"><span data-stu-id="79885-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="79885-141">選取 **連接**。</span><span class="sxs-lookup"><span data-stu-id="79885-141">Select  **Connect**.</span></span>

<span data-ttu-id="79885-142">您已成功連接 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="79885-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="79885-143">您現在可以部署 Dynamics 365 Finance 雲端託管的環境。</span><span class="sxs-lookup"><span data-stu-id="79885-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
