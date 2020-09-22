---
title: 檢視資源的應收費使用率
description: 本主題提供有關資源使用率檢視表的資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757214"
---
# <a name="view-chargeable-utilization-for-resources"></a>檢視資源的應收費使用率
 
**Project Service 資源使用率**頁面上的**使用率檢視表**會顯示每個可預約資源的應收費使用率。 檢視表是以排程面板為基礎所建立，因此您會發現許多相同的功能。

> ![使用率檢視表的螢幕擷取畫面](media/FAQ-utilization-1.png)
 

應收費使用率計算依下列方式運作：

   應收費使用率 = (應收費實際時數) / (資源產能)

儲存格表示所選期間 (日、週或月) 的已計算應收費使用率。

每個儲存格中的色彩顯示資源相較於其目標應收費使用率的應收費使用率。 

您可以在資源的預設角色或個別資源本身設定目標使用率。 計算會先查看個別資源以取得目標，然後參考資源的預設角色。

## <a name="set-target-on-a-resource"></a>對資源設定目標

1. 移至**資源** \> **資源**。 
2. 選取要開啟記錄的資源。 
3. 在 **Project Service** 索引標籤上，您可以設定資源的目標使用率。

> ![使用 [Project Service] 索引標籤設定目標使用率的螢幕擷取畫面](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>設定角色的目標使用率

1. 移至**資源**\>**資源角色**。 
2. 選取角色並開啟記錄。 
3. 設定角色的目標使用率。

> ![使用 [資源角色] 設定目標使用率的螢幕擷取畫面](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>計算資源的應收費使用率

若要計算資源的應收費使用率，您必須完成一些先決條件。 

### <a name="set-default-role-for-individual-resource"></a>設定個別資源的預設角色

首先，必須對個別資源或資源角色設定目標使用率。 如果您使用資源角色設定目標，則每項個別資源都必須有預設角色。 

1. 若要進行此設定，請移至**資源**\>**資源**。 
2. 選取資源、開啟記錄，然後選取 **Project Service** 索引標籤。 
3. 在**資源角色**網格中，確定資源有一個角色，且**是預設值**已設定為**是**。
 
### <a name="change-billing-type-for-resource-role"></a>變更資源角色的帳單類型

必須設定資源角色，才會有**應收費**的帳單類型。 

1. 移至**資源**\>**資源角色**。 
2. 開啟要更新的記錄，然後將帳單類型設定為**應收費**。

### <a name="set-working-hours-for-resource-role"></a>設定資源角色的工作時數
 
資源必須有工作時數，才能計算產能。 

1. 移至**資源** \> **資源**。 
2. 選取要開啟記錄的資源，然後選取**顯示工作時數**。 
3. 您可套用**資源清單**檢視表的**工作時數範本**，以大量更新資源清單。

## <a name="troubleshooting-chargeable-actual-hours"></a>應收費實際時數疑難排解

應收費實際時數的來源是**實際值**實體。 帳單類型為**應收費**的實際值會納入計算，因此您必須有實際值為應收費的專案。

如果您沒有看到應收費使用率，以下是一些您可以檢查的項目：

- 資源有針對產能所定義的工作時數。
- 資源有個別定義的使用率目標，或是有指派給它的預設角色。 角色有其定義的使用率目標。
- 實際值在您預期要進行使用率計算的期間有**應收費**的帳單類型。 如果您看到帳單類型為 [應收費] 以外類型的實際值，請檢查下列項目：

  - 實際值上使用的角色有 [應收費] 以外的預設計費類型。
  - 支援專案的專案合約服務內容上的角色已設定為不應收費。
  - 專案沒有相關聯的合約服務內容。

