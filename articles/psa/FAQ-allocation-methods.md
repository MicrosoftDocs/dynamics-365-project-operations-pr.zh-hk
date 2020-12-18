---
title: Project Service Automation 中的預約配置方法
description: 本主題提供有關您可以預約配置的不同方式的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 3dc87a66a4b881a06f2b888c26d9dfaefb419f16
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131410"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Project Service Automation 中的預約配置方法

不論您是直接將團隊成員新增至 **團隊** 索引標籤上的專案，還是透過排程面板將資源預約到專案或需求，您都有一些可以用來預約配置的不同方法。 本主題說明每個方法的運作方式，以及哪些方法可能導致過量預約資源。

## <a name="full-capacity"></a>完整產能 
[完整產能] 方法會預約資源指定之開始日期到結束日期的完整產能。 例如，如果資源的行事曆是設定為每日工作八小時 (一週五日)，則設定涵蓋五個工作日的開始和結束日期會預約 40 小時的資源。 預約是在不考慮資源剩餘產能的情況下完成。 如果其他專案已預約該期間的資源，則此 40 小時會預約為額外時數，這可能導致過量預約。

## <a name="remaining-capacity"></a>剩餘產能
[剩餘產能] 方法只有在您使用排程面板直接預約給專案時，才可使用。 此方法會預約資源在指定之日期範圍內的可用產能。 例如，如果資源每週有 40 小時的產能，而其中已經預約 10 小時，則對同一週進行預約會產生對該週 30 小時剩餘產能的預約。

## <a name="percentage-capacity"></a>產能百分比
[產能百分比] 方法會預約資源在指定之開始到結束日期一定百分比資源的產能。 例如，如果資源的行事曆是設定為每日工作八小時 (一週五日)，則以 50% 產能設定涵蓋五個工作日的開始和結束日期會預約 20 小時的資源。 每日的個別預約是在整個期間平均分攤，在此範例中為每日四小時。 預約是在不考慮資源剩餘產能的情況下完成。 如果其他專案已預約該期間的資源，則此 20 小時會預約為額外時數，這可能導致過量預約。

## <a name="evenly-distribute-hours"></a>平均分配時數
[平均分配時數] 方法會預約指定時數的資源，並在指定之開始到結束日期內平均分配每日的時數。 例如，如果您將資源預約在五日期間內的 20 小時，此方法會以每日四個小時平均分配 20 小時。 預約是在不考慮資源剩餘產能的情況下完成。 如果其他專案已預約該期間的資源，則此 20 小時會預約為額外時數，這可能導致過量預約。

## <a name="front-load-hours"></a>前重後輕時數
[前重後輕時數] 方法會預約指定時數的資源，並在指定之開始和結束日期內以前重後輕的方式分配每日的時數。 前重後輕方法會依照「先到先用」順序使用資源的可用產能。 例如，如果資源的工作排程是每日八小時 (一週五日)，但目前這幾日沒有預約，則預約資源在五個工作日期間的 20 小時會產生下列每日預約模式： 

|         預約          |    第 1 日。    |    第 2 日。    |    第 3 日。    |    第 4 日。    |    第 5 日。    |    總數    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    現有預約數    |    12        |    12        |    12        |    12        |    12        |    12        |
|    新增預約數          |    8        |    8        |    4        |    0        |    0        |    20       |

前重後輕方法會將現有預約數和可用產能納入考量。 例如，如果相同資源的工作週已經有 20 小時的預約，則新預約會耗用剩餘的產能，如下所示：

|   預約          | 第 1 日。 | 第 2 日。 | 第 3 日。 | 第 4 日。 | 第 5 日。 | 總數 |
|---------------------|-------|-------|-------|-------|-------|-------|
| 現有預約數 | 8     | 8     | 4     | 12     | 12     | 20    |
| 新增預約數       | 0     | 0     | 4     | 8     | 8     | 20    |

因為可用產能已納入考量，如果資源沒有可供預約吸收的剩餘產能，您可能會收到錯誤訊息。 使用此方法時，您不可過量預約。

## <a name="none"></a>無
[無] 方法只有當您在專案內透過 **團隊** 索引標籤進行預約時，才可使用。 此方法會新增資源做為專案上的團隊成員，但不會建立任何吸收資源產能的預約。 如果建立專案時新增預設專案經理團隊成員，會使用此方法。 建立專案的專案經理使用者預設會新增至專案，讓專案實體記錄有負責人，以及使專案存在一個核准者。 因為此使用者沒有任何預約，如果您確實想要預約資源，則可以使用不同的配置方法將資源刪除然後重新加入，或是將資源新增至工作，然後使用 **協調** 索引標籤上的 **延長預約** 來為指派建立預約。

## <a name="allocation-methods-that-lead-to-overbooking"></a>導致過量預約的配置方法
總而言之，如果資源已指定用於其他專案 (或已調撥給其他工單或可排程的實體)，下列配置方法將會導致過量預約：

- 完整產能
- 產能百分比
- 平均分配時數

使用這三種的其中一個配置方法時，您不會收到資源已過量預約的通知。 若要修正過量預約，您必須使用排程面板。