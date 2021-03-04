---
title: 銷售估計和專案
description: 本主題提供有關如何利用銷售處理中的排程和估計的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148400"
---
# <a name="sales-estimates-and-projects"></a>銷售估計和專案

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在銷售處理期間，您可以將專案連結至銷售報價來建立銷售估計。 如此一來，就能在銷售處理期間進行具有決定性的估計，以便利用專案排程和估計功能。 如果銷售完成，用作銷售估計目的排程就可以用來做為進一步改善專案計劃的基礎。

## <a name="linking-a-project-to-a-quote-line"></a>連結專案與報價明細

建立專案型報價明細時，您可以建立新專案，或是與 **報價明細** 頁面上的現有專案建立關聯。 

> ![報價明細表單](media/project-8.png)
 
從報價明細詳細資料建立新專案時，您可以利用專案範本。 專案範本是表示組織中特具代表性之專案計劃與財務估計的模型專案。 這些範本也可能表示過去專案的專案計劃及估計複本。

> ![報價明細詳細資料](media/project-9.png)
  
從報價建立您的專案時，專案會自動與報價明細建立關聯。

## <a name="components-of-estimates-in-a-project"></a>專案中的估計元件

排程可讓您將作業分成工作、維持工作的階層、判斷完成工作所需的資源，以及指派完成工作所需投入努力的估計。

您可以使用 **專案** 頁面 **排程** 索引標籤上的欄位，來定義工作投入和排程估計。 由於價目表與專案相關聯，因此財務估計會使用價目表中定義的成本和銷售價格進行計算。

## <a name="importing-estimates-from-a-project-into-a-quote"></a>從專案將估計值匯入至報價

定義專案估計值之後，您可以將這些值匯入至報價明細。 在 **報價明細詳細資料** 頁面上，選取功能區上的 **從估計值匯入**，以依據交易類型、角色或工作層級來摘要專案估計值。
