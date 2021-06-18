---
title: 提案建議專案資源
description: 本主題提供有關如何提案建議專案資源的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 02e47338e34a37e05455e2bc6e6a175210ed6bc7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997988"
---
# <a name="propose-project-resources"></a>提案建議專案資源

[!include [banner](../includes/psa-now-project-operations.md)]

資源管理員可以使用資源要求，提案向專案經理建議資源。

1. 從要求網格或要求本身中選取 **尋找資源**。
2. 在 **排程小幫手** 頁面上，選取資源，然後在 **建立資源預約** 窗格的 **預約狀態** 欄位中選取 **預約**。

    ![提案的資源已選取](media/Resource-Management-image62.png)

發生下列狀態更新：

- 在 **排程小幫手** 頁面上，狀態指示器會更新，以指定該預約是提案所建議，而不是已確認預約。

    ![排程小幫手頁面上提案的預約的狀態指示器](media/Resource-Management-image63.png)

- 在資源要求上，狀態已變更為 **需要檢閱**。

    ![資源要求狀態已變更為 [需要檢閱]。](media/Resource-Management-image64.png)

- 在專案的 **團隊** 索引標籤上，一般團隊成員的 **要求狀態** 值會變更為 **需要檢閱**。

    ![一般團隊成員的要求狀態在 [團隊] 索引標籤上已變更為 [需要檢閱]。](media/Resource-Management-image48.png)

專案經理可以接受或拒絕提案。

資源經理處理資源要求時，可以使用下列任一方法：

- 如果沒有單一資源可用來履行需要的時數，請提案建議多個資源以滿足需求。 提案的時數隨後會在多個可滿足所需時數的資源間進行分割。 在此案例中，時數不能重疊。
- 提案建議比所需資源還要少的資源。 在此案例中，提案的資源產能小於要求者所指定的需要時數。 因此，當要求者接受提案的資源時，就會建立未履行資源需求，以擷取剩餘的索求。
- 如果沒有單一資源可用來完成工作，請預約建議多個資源以滿足索求。
- 預約比所需資源還要少的資源。 在此案例中，預約的工時少於需要的時數。 系統會引導您提案建議的是資源而不是預約，這樣要求者才能驗證並追蹤剩餘的索求。

## <a name="billable-utilization"></a>計費使用率

資源可以有目標計費使用率。 此目標使用率會定義為資源預設角色的屬性，或是透過個別可預約資源的記錄來設定。 使用率計算是根據資源使用核准的時間項目所報告的實際時數來進行。

下列公式用於計算使用率：

- 計費使用率 = 應收費實際時數 ÷ 資源產能
- 非計費使用率 = 帳單類型識別碼為 [不應收費]、[附贈] 或 [不適用] 的實際時間 ÷ 資源產能
- 內部 = 無銷售合約的實際時間 ÷ 資源產能
- 資源產能 = 資源工作時數 – 不在辦公室 – 非工作天數

您可以在 **資源** 窗格中找到 **資源使用率** 檢視表。

![資源使用率檢視表](media/Resource-Management-image65.png)

網格中的每個儲存格表示一個週期 (例如日、週或月) 中資源的計費使用率百分比。 下列公式用於設定儲存格的色彩：

- **綠色：** 計費使用率 \>= 資源目標使用率
- **黃色：** 目標使用率 – 20 \<= 計費使用率 \< 目標使用率
- **紅色：** 計費使用率 \< 目標使用率 – 20。

因為 **資源使用率** 檢視表以排程面板為基礎，所以您可以使用排程面板的篩選功能來篩選結果。

網格要求您必須對角色或個別資源設定目標使用率。 若要進行此設定，請移至 **資源** \> **資源角色**。

此外，還必須將預設角色指派給每個可預約資源。 移至 **資源** \> **資源**。 在 **Project Service** 索引標籤上，確認已定義資源角色，且該角色的 **是預設值** 欄位已設定為 **是**。 您可以新增其他角色，其中 **是預設值 = 否**。 **是預設值 = 是** 的角色會用來對照該角色的目標來評估資源的使用率。

![預設角色已設定](media/Resource-Management-image67.png)

在 **Project Service** 索引標籤上，您也可以設定資源的個別目標使用率。 使用率計算接著會使用該目標使用率來評估資源的目標，而不是資源預設角色的目標。

只有當資源在網格所顯示週期內有獲核准的應收費時間時，才會顯示資源的使用率。

## <a name="resource-availability"></a>資源可用性

資源管理員要能夠檢視資源可用性並更新預約，至關重要。 在某些情況下，沒有正式索求 (資源要求)，但是資源管理員必須回應來自電子郵件、通話或立即訊息等管道的計劃外索求。 資源管理員會使用排程面板來更新資源和預約。

資源工作時數會用來做為計算資源可用性的基準。 資源預約會耗用資源的產能。

![排程面板](media/Resource-Management-image68.png)

排程面板使用色彩與陰影來顯示預約、可用性和過量預約，以及預約的狀態。 排程面板中的設定可讓您顯示圖例。

如果排程面板上的個別可預約資源旁邊出現向右箭頭，則可以展開資源來顯示該資源所預約之工作的詳細資料。

![排程面板上已展開的可預約資源](media/Resource-Management-image69.png)

因為 Dynamics 365 Project Service Automation 使用 Universal Resource Scheduling 引擎，如果您也已安裝 Dynamics 365 Field Service，則可以檢視專案、工單以及任何其他您已給予排程之實體的資源預約詳細資料。

![專案和工單的資源預約詳細資料](media/Resource-Management-image70.png)

若要檢視更多關於個別資源的詳細資料，請在其上按滑鼠右鍵以開啟資源卡片。

![資源卡片](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]