---
title: 技能和熟練度模型
description: 此主題提供有關如何使用技能和熟練模型的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d46382939e22c1ee1d9f5517798aabb3520ae3bd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599895"
---
# <a name="skills-and-proficiency-models"></a>技能和熟練度模型

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

技能是在 Dynamics 365 Project Service Automation 與 (如果存在) Dynamics 365 Field Service 之間共用的資源特性。 

若要在 Project Service Automation 中維護技能存放庫，請移至 **資源** \> **資源技能**。 

> ![資源技能。](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>使用熟練度模型來評等資源

資源的技能由熟練程度模型所評等。 個別評等是在熟練度模型中。 

1. 若要建立熟練度模型，請移至 **資源**\>**熟練度模型**，然後選取 **新增**。
2. 在新的評等模型中，指定最小評等值、最大評等值以及要加以評等的實體。
3. 在 **評等值** 子格中，您可以定義從最小值到最大值的不同評等值。

> ![定義的最小與最大評等。](media/Resource-Management-image85.png)

這些評等值會顯示在 **資源需求**、**排程面板和** 和 **排程小幫手** 篩選上。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
