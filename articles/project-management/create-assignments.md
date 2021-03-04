---
title: 建立資源指派
description: 本主題提供有關建立一般及具名資源指派的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 829c1d1de7270e7cafbb98ef80235ae6404f77f7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131775"
---
# <a name="create-resource-assignments"></a>建立資源指派

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


資源指派是專案團隊成員與分葉節點工作的直接關聯。 本主題提供有關不同指派資源方式的資訊。

## <a name="create-a-generic-team-member-through-task-assignment"></a>透過工作指派建立一般團隊成員


透過工作指派建立一般團隊成員時，您會建立預留位置或一般資源。 此一般資源描述您最終要在工作上使用之具名資源的特性。 您接著會產生用來搜尋並預約具名資源的需求 (或使用需求送出要求)。

1. 在工作的排程網格中，選取 **資源** 儲存格中的資源圖示。
2. 輸入要做為預留位置資源名稱的名稱。 例如，「方案經理」。
3. 選取 **建立**，並在右側的 **快速建立專案團隊成員** 欄位中，設定一般資源的角色。
4. 在工作的 **資源選取器** 上選取資源，視需要將工作指派給此預留位置資源。 **團隊成員** 下方列出的資源。
5. 完成指派一般資源時，選取 **團隊** 索引標籤上的一般資源，然後選取 **產生需求** 以建立一般資源的資源需求。
6. 選取一般資源的 **預約**，然後使用排程面板來尋找並預約實際資源。 您也可以送出要求資源管理員履行的需求。
7. 使用具名資源完全履行一般資源 (部分資源需求履行不會產生資源指派) 時，一般資源會從團隊中移除。 一般資源的工作指派會指派給履行一般資源之資源需求的具名資源。

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>從所有可預約資源清單中指派具名預約

您可以使用 **資源選擇器** 中的搜尋方塊，搜尋所有使用中可預約資源，並將這些資源指派給任何分葉節點工作。 以此方式指派的資源會新增至沒有任何預約的團隊。 這類似於新增團隊成員後，再選取 **無** 做為配置方法。 資源會在 **團隊**、**資源指派** 和 **協調** 索引標籤中顯示為只有指派且預約短缺的資源。 如果您想要使用其可用產能，請加以預約。

1. 從工作網格、面板或時間表，瀏覽至 **指派至** 儲存格。
2. 在搜尋方塊中，開始輸入名稱。 該名稱的搜尋結果會顯示在 **資源選取器** 的 **其他資源** 下方。
3. 選取您要指派給工作的資源，或選取 **其他團隊資源** 底下的資源名稱。


[!INCLUDE[footer-include](../includes/footer-banner.md)]