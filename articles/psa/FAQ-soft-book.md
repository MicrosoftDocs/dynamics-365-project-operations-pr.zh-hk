---
title: 以未確認方式預約資源
description: 本主題提供有關如何對專案團隊成員進行暫訂排程或未確認預約的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: af71ff9d60e237a9d1379b3ccd4c0d5ffce411e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122235"
---
# <a name="soft-book-a-resource"></a>以未確認方式預約資源

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

您可透過暫訂方式將資源排程或「未確認預約」到專案團隊上，以顯示您計劃要將資源指派給專案。 未確認預約不會耗用資源的可用產能，而且您可以將未確認預約的團隊成員指派給專案工作。 不過，正因為未確認預約不耗用資源的產能，您仍可透過「已確認預約」方式來為其他工作預約同一期間內的資源。 一般資源無法進行未確認預約，而未確認預約也不能履行一般資源的要求。

未確認預約的專案團隊成員會在 **專案** 頁面的 **團隊** 索引標籤上列出，而其未確認預約時數則顯示在 **具名資源成員** 檢視表的 **未確認預約時數** 欄中。 排程面板也會列出未確認預約的團隊成員。 因為這些成員已未確認預約，排程面板不會顯示任何對這些資源產能的耗用量。 未確認預約的時間不會出現在 **協調** 索引標籤上，也不會顯示在排程面板 **協調** 索引標籤的 **延長預約** 欄位中。 

有兩種方式可以將團隊成員未確認預約到專案：直接透過排程面板，或在 **團隊** 索引標籤上新增團隊成員。 

## <a name="soft-book-from-the-schedule-board"></a>透過排程面板進行未確認預約
完成下列步驟，以透過排程面板對資源進行未確認預約。 

1. 開啟排程面板，然後在 **預約需求** 面板中選取 **專案** 索引標籤。
2. 尋找您要以未確認方式為其預約資源的專案。 如果清單中有大量專案，請選取 **專案** 欄標題，然後使用篩選來搜尋一個或多個專案。
3. 選取專案，然後將其拖放到資源的時間網格。
5. 在 **建立資源預約** 面板中，調整開始和結束日期、將 **預約狀態** 設定為 **未確認**，然後設定時數。 
6. 按一下 **預約**。 資源立即在 **團隊** 索引標籤上顯示為專案的資源。 在 **具名團隊成員** 檢視表上，您會看到 **未確認預約時數** 欄中的未確認預約時數。

> [!NOTE]
> 您現在可以將未確認預約的資源指派給 **排程** 索引標籤上的工作。在 **協調** 索引標籤上，資源將會顯示相對於工作指派的預約短缺，因為 **協調** 索引標籤僅考慮已確認預約的情況。 您可以使用 **延長預約** 功能對資源進行已確認預約，針對資源指派消除已確認預約的短缺情況。 您需要使用 **維護預約**，手動取消資源的未確認預約。

## <a name="soft-book-on-the-team-tab"></a>團隊索引標籤上的未確認預約

您可以直接在 **團隊** 索引標籤上新增團隊成員，然後使用 **維護預約** 將其預約狀態從 **已確認** 變更為 **未確認**。 依此方式新增團隊成員時，除非您選取的配置方法為 **無**，否則這永遠都會產生已確認預約。

若要使用此方法，請完成下列步驟。

1. 在 **專案** 頁面的 **團隊** 索引標籤上，按一下 **新增**。
2. 選取可預約資源、角色、開始和結束日期。
3. 選取 **無** 以外的配置方法。
4. 選取 **儲存**。 您將會在網格上看到資源，而其時數會顯示在 **已確認預約時數** 欄中。
5. 選取 **維護預約** 以維持資源的預約。
6. 排程面板開啟時，展開資源以顯示其預約。 您會看到預約顯示為 **已確認**。
7. 以滑鼠右鍵按一下預約、然後在 **變更狀態** 下，選取 **未確認預約**\>**未確認**。 預約狀態現在為 **未確認**。
8. 關閉排程面板後，當您查看 **具名團隊成員** 檢視表時，會看到資源的時數已從 **已確認預約時數** 欄移至 **團隊** 索引標籤網格的 **未確認預約時數**。

> [!NOTE]
> 使用 **維護預約** 將狀態從 **已確認** 變更為 **未確認** 時，如果您透過已確認方式將資源預約到團隊，然後再將工作指派給資源，則會保留該資源的工作指派。 不過，在 **協調** 索引標籤中，資源會有預約短缺的情況，因為協調預約與指派時，只會考慮已確認預約。 您可以使用 **協調** 索引標籤上的 **延長預約** 功能對資源進行已確認預約，針對資源指派消除已確認預約的短缺情況。 您需要使用 **維護預約** 來取消資源的未確認預約。

當您準備好將未確認預約團隊成員資源變更為已確認預約團隊成員時，請執行下列動作：

1. 在排程面板上，展開資源以顯示其預約。 您將看到預約顯示為 **未確認**。
2. 以滑鼠右鍵按一下預約、在 **變更狀態** 下選取 **已確認預約**\>**已確認**。 預約狀態現在為 **已確認**。
3. 關閉排程面板、回到專案並開啟 **團隊** 索引標籤之後，當您進入 **具名團隊成員** 檢視表時，會看到資源的時數已從 **未確認預約時數** 欄移到 **團隊** 索引標籤的 **已確認預約時數** 欄。 如果資源已指派給工作，這些資源在 **協調** 索引標籤上將不再顯示預約短缺，因為其預約現在是已確認預約。
