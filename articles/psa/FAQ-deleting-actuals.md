---
title: 為什麼我無法從實際值實體刪除記錄？
description: 本主題提供有關為何您無法從實際值實體刪除記錄的資訊。
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087626"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>為什麼我無法從實際值實體刪除記錄？

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) 不允許您刪除實際值，因為這些值可以做為對下游系統 (例如總帳) 有財務影響的交易事實原始資料。 如果可以刪除實際值，可能就會引發對財務報表交易完整性的質疑。 若要建立稽核線索，客戶必須使用帳目來建立補償交易。

