---
title: 專案階段
description: 本主題提供有關專案階段的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757240"
---
# <a name="project-stages"></a>專案階段 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

專案階段會更新，以反映專案進展時的狀態。 預設商務程序流程會自動更新專案階段的部分階段，而其他階段則由專案經理手動進行更新。 

下列階段已在預設 BPF 中定義：

- 新增
- 報價
- 計劃
- 交付
- 完成
- 關閉 

## <a name="new"></a>新增

建立專案時，專案階段會設定為 **新增**。 如果專案是從範本建立，則可能會有排程、估計值及團隊資料。 否則，就只是專案的大綱，您必須輸入剩餘的元件。

## <a name="quote"></a>報價

將專案與報價建立關聯或從報價建立專案時，專案階段會設定為**報價**，而估計的開始和結束日期也會更新。 專案處於**報價**階段時，**專案實體**上的**銷售**索引標籤會顯示報價的詳細資料。

## <a name="plan"></a>計劃

當您贏得與專案相關聯的報價，且專案已進入**合約**階段時，專案階段會更新為**計劃**。 專案處於**計劃**階段時，**專案實體**頁面會顯示合約的詳細資料。

## <a name="deliver"></a>交付

專案計劃完成，且您已準備好開始專案時，專案經理應將專案階段更新為**交付**，以顯示專案已開始。

## <a name="complete"></a>完成 

專案的工作完成後，專案經理就可以將階段更新為**完成**。 專案經理藉由將專案階段更新為**完成**，指出工作已百分之百完成，但專案仍保持開啟狀態，讓您可以記錄任何擱置的時間或費用項目。

## <a name="close"></a>關閉

將專案所有的交易都記錄下來後，專案經理就可以將階段更新為**關閉**。 此時，無法記錄任何交易，且專案會設定為唯讀。
