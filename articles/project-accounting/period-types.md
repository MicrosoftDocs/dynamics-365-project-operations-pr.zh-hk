---
title: 期間類型
description: 此主題提供有關如何設定營收估計的期間類型的資訊。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531599"
---
# <a name="period-types"></a>期間類型

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

期間類型定義了估計專案營收的頻率。 此主題提供有關如何設定營收估計的期間類型的資訊。 

## <a name="create-and-work-with-period-types"></a>建立與使用期間類型
若要建立和使用期間類型，請完成下列步驟：

1. 在您的 Dynamics 365 Finance 環境中，移至 **專案管理和會計** > **設定** > **估計值** > **期間類型**。
2. 選取 **新增** 以建立新的期間類型。 輸入名稱和描述。
3. 在 **頻率** 欄位中選取值：

    - 如果您選取 **週**、**兩週**、**半月**、**月**、**日**、**季** 或 **年**，就會使用行事曆來產生期間。 
    - 如果您選取 **分類帳期間**，則會使用總帳設定中的分類帳期間來產生期間。
    - 如果您選取 **無限制**，則可以指定自訂期間。
4. 選取期間類型記錄，然後選取 **產生期間**，以建立期間類型的期間。 根據您所選取的期間頻率，您可以選擇指定開始日期或要產生的期間數。
5. 選取 **期間** 以檢閱產生的期間。
