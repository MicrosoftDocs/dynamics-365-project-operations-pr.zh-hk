---
title: 指派一般可預約資源至工作與專案團隊
description: 這主題提供有關為工作與專案團隊預約一般資源的資訊。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145430"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>指派一般可預約資源至工作，並產生資源需求 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

除了預約和指派具名或實際的資源給專案之外，您還可以將一般資源指派至專案工作。 在您準備好以具名資源來為專案配置人員之前，這些資源可以做為具名資源的預留位置。 

1. 在 Project Service Automation (PSA) 中，開啟 **專案** 頁面，然後移至 **排程** 索引標籤，在排程的 **資源** 儲存格中輸入一般資源的職位名稱。 或者，按一下儲存格中的 **資源** 圖示以開啟資源選擇器，然後輸入您要建立的一般資源的名稱。

![建立和指派一般團隊成員](media/RM-how-to-9.png)

這會開啟 **快速建立：專案團隊成員** 面板。 

2. 輸入一般資源團隊成員的角色與組織單位，然後按一下 **儲存**。

![一般團隊成員快速建立](media/RM-how-to-10.png)

3. 建立新的一般資源團隊成員之後，便會將其指派給工作。 您可以繼續將該一般資源指派給工作排程中的其他工作。

![將現有的一般團隊成員指派給工作](media/RM-how-to-11.png)

4. 指派了一般資源之後，即可產生資源需求，並透過直接將資源要求預約或送出給資源管理員來履行該需求。

![產生一般團隊成員的需求](media/RM-how-to-12.png)

在團隊成員網格中，除了可以使用上述資源選擇器之外，還可以直接新增一般資源。 資源會因為根據 **快速建立：專案團隊成員** 面板所指定開始/結束日期與配置方法所產生的資源需求而新增。

如果直接新增一般團隊成員，然後將更多工作指派給一般資源，超過這些工作所獲必須要時數所能支援的範圍時，您就可以看出差異。 按一下 **產生需求**，重新產生需求以平衡工作指派所需的時數。

您也可以按一下團隊網格中的 **資源需求** 連結，以開啟需求並新增技能、偏好資源等。

![資源需求](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]