---
title: 檢閱提案的資源
description: 本文提供有關如何提案建議專案資源的資訊。
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f20dda2b7b384608b8f4b548c18ac21d07fee07
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924871"
---
# <a name="review-proposed-resources"></a>檢閱提案的資源

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

資源管理員可以使用資源要求，提案向專案經理建議資源。

若要檢閱建議的資源，請依照下列步驟進行：

1. 從 **要求** 網格或要求本身中選取 **尋找資源**。
2. 在 **排程小幫手** 頁面上，選取資源，然後確認所有建議的時數皆已包含在已提案的預約中。
3. 在 **建立資源預約** 窗格中，將 **預約狀態** 欄位設定為 **已提案**，然後選取 **預約**。

    > [!NOTE]
    > 將 **預約狀態** 設定為 **已提案** 並不會以已確認預約方式來預約資源，也不會將一般資源取代為具名團隊成員。

    發生下列狀態更新：

    - 在 **排程小幫手** 頁面上，狀態指示器會更新，以指出該預約是提案所建議，而不是已確認預約。
    - 在資源要求上，狀態已變更為 **需要檢閱**。
    - 在專案的 **團隊** 索引標籤上，一般團隊成員的 **要求狀態** 值會變更為 **需要檢閱**。

專案經理可以接受或拒絕提案。

資源經理處理資源要求時，可以使用下列任一方法：

- 如果沒有單一資源可用來履行需要的時數，請提案建議多個資源以滿足需求。 提案的時數隨後會在多個可滿足所需時數的資源間進行分割。 在此案例中，時數不能重疊。
- 提案建議比所需資源還要少的資源。 在此案例中，提案的資源產能小於要求者所指定的需要時數。 當要求者接受提案的資源時，就會建立未履行資源需求，以擷取剩餘的索求。
- 如果沒有單一資源可用來完成工作，請預約建議多個資源以滿足索求。
- 預約比所需資源還要少的資源。 在此案例中，預約的工時少於需要的時數。 系統引導您提案建議的是資源而不是預約，這樣要求者才能驗證並追蹤剩餘的索求。

## <a name="resource-availability"></a>資源可用性

資源管理員必須有能力檢視資源可用性並更新預約。 在某些情況下，並沒有正式索求 (資源要求)。 不過，資源管理員必須回應來自電子郵件、通話或立即訊息等其他管道的計劃外索求。 資源管理員會使用 **排程面板** 來更新資源和預約。

資源工作時數會用來做為計算資源可用性的基準。 資源預約會耗用資源的產能。

**排程面板** 使用色彩與陰影來顯示預約、可用性、過量預約，以及預約的狀態。 **排程面板** 上的設定可讓您顯示圖例。

如果 **排程面板** 上的個別可預約資源旁邊出現向右箭頭，則可以展開資源來顯示該資源所預約之工作的詳細資料。

因為 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，如果您也已安裝 Dynamics 365 Field Service，則可以檢視專案、工單以及任何其他您已給予排程之實體的資源預約詳細資料。

若要檢視關於個別資源的其他詳細資料，請在其上按滑鼠右鍵以開啟資源卡片。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
