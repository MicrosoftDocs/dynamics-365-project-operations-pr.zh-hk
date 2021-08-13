---
title: 更新專案
description: 本主題提供有關更新 Project Operations 中專案的資訊。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000918"
---
# <a name="update-a-project"></a>更新專案

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

以下是建立專案後可在其中更新的欄位摘要，以及這些更新作業的任何適用含意。

## <a name="project-detail-fields"></a>專案詳細資料欄位

- **名稱**：選取專案的標題。
- **描述**：專案的概觀。
- **客戶**：專案將交付到的公司。
- **行事曆範本**：專案的工作時數。 當欄位變更時，會重新計算整個排程。
- **貨幣**：專案的貨幣。 此欄位是根據在合約單位中定義的貨幣來設定預設值。 更新合約單位時，也會更新此欄位。
- **合約單位**：代表公司中主要負責贏得銷售和管理客戶工作與服務交付之群組或部門的組織單位。 
- **專案經理**：有權責可以審查和核准時間項目及費用的專案團隊成員。

## <a name="estimate-fields"></a>評估值欄位

- **估計開始日期**：專案將開始的日期。 更新此欄位時，專案中的任何工作都會與開始日期成比例原則移動新的開始日期。
- **完成日期**：排定專案結束的日期。
- **投入量**：專案的估計投入量。 將工作新增至專案時，此欄位將無法再編輯。
- **估計人力成本**：專案的估計人力成本。 將人力成本新增至專案時，此欄位將無法再編輯。
- **估計費用**：專案的估計位於。 將費用新增至專案時，此欄位將無法再編輯。

## <a name="project-actual-fields"></a>專案實際值欄位
- **實際開始**：專案開始的日期。
- **實際完成**：可在專案完成時進行更新。

## <a name="project-status-fields"></a>專案狀態欄位

- **整體專案狀態**：專案經理所提供的整體專案健全狀況。
- **註解**：專案經理所提供有關專案目前健全狀況的敘述。



[!INCLUDE[footer-include](../includes/footer-banner.md)]