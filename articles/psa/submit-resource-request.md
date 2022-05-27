---
title: 送出資源要求
description: 本主題提供有關送出專案資源要求的資訊。
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d22f52771f55a551416d1ba2f7105d59d7b912f0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577493"
---
# <a name="submitting-a-resource-request"></a>送出資源要求

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

您可以將產生的資源需求當做資源要求送出。 隨後會將要求傳送給資源管理員來履行。

1. 在 Project Service Automation (PSA) 的 **專案** 頁面上，按一下 **團隊** 索引標籤以檢視可預約資源清單。 
2. 從清單中選取具有資源需求的一般資源，然後按一下 **送出要求**。

![送出資源要求。](media/RM-how-to-18.png)

一般團隊成員的要求狀態會變更為 **已送出**。

資源管理員履行要求之後，如果資源管理員是使用具名資源的預約來履行要求，則會以具名資源取代一般資源。 否則，一般資源仍保留在團隊中，如果資源管理員已提案建議具名資源，則要求狀態將會變更為 **需要檢閱**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
