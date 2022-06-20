---
title: 同步處理資源產能
description: 本文提供有關如何跨行事曆和專案同步處理資源產能的資訊。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920731"
---
# <a name="synchronize-resource-capacity"></a>同步處理資源產能

[!include [banner](../includes/banner.md)]

資源同步處理的程序有助於保證行事曆及基準行事曆的資訊會逐漸滲入專案資源排程中。 如果行事曆已變更，此程序就會對專案資源排程進行必要的更新。 此程式也有助於改善效能，因為會提前同步處理行事曆的資源資訊。 因此會加快進行對資源排程資訊的更新。 建議您以批次方式排定這些程序，而不是逐次排定。 否則，會有人忘記上次同步處理資訊時包含的日期。 如果沒有使用包含的日期，就會在進行日期同步處理時出現期間缺口。

![行事曆同步處理。](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>同步處理資源產能彙總

同步處理程序是專為同步處理所有資源行事曆資訊而設計。 此資訊包含有關任何對專案資源行事曆產能資料表所做變更的基準行事曆資訊。 如果專案中新增了新資源，同步處理有助於保證有更新過的行事曆資訊可供使用。 此同步處理作業隨時都可以進行。

建議您使用批次。 有選項可在產能保留同步處理期間使用。

1. 選取 **專案管理與會計** &gt; **定期** &gt; **產能同步處理** &gt; **同步處理資源產能彙總**。
2. 設定下表中的選項。

    | 選項      | 描述 |
    |-------------|-------------|
    | 期間代碼 | 選擇性選取總帳日期間隔代碼，以設定資源產能彙總同步處理程序的開始和結束日期。 |
    | 開始日期  | 輸入資源產能彙總同步處理程序的開始日期。 |
    | 結束日期    | 輸入資源產能彙總同步處理程序的結束日期。 |

[![同步處理程序。](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]