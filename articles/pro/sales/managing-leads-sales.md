---
title: 管理潛在客戶 (專案版)
description: 本主題提供有關管理專案型潛在客戶的資訊 (專案版)。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896353"
---
# <a name="manage-leads-pro"></a>管理潛在客戶 (專案版)

_**適用於：** 精簡部署 - 交易至開立預估發票_

在 Project Operations 中，可以管理專案型潛在客戶並授與其資格。 潛在客戶管理程序包括建立工作型潛在客戶以及授與這些潛在客戶資格。 

## <a name="list-of-project-sales-leads"></a>專案銷售潛在客戶清單

在**銷售**區段的左導覽窗格中，開啟**潛在客戶**清單頁面，以檢視系統中所有潛在客戶記錄的清單。 如果您也有 Dynamics 365 Sales 或 Dynamics 365 Field Service 應用程式，則顯示的潛在客戶清單是工作型潛在客戶及其他可建立之類型的潛在客戶。

您可以建立依據**類型**值的篩選來建立篩選過的檢視，只查看專案型潛在客戶。 例如，您可以選擇只顯示工作型潛在客戶。

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>建立專案型交易的新潛在客戶

授與專案型潛在客戶資格時，會建立商機和客戶。 專案型商機是商機階段中銷售追隨活動的起點。 專案型商機具有銷售專案工作所需的獨特功能。 這些功能包括：

- 時間和材料以及固定價格帳務方式
- 專案上所產生人力資源、費用和材料的多個有效日期價目表。

為了讓合格的潛在客戶自動建立商機，請在建立潛在客戶時，將**類型**屬性設定為**工作型**。 如果您選擇不同的類型，則潛在客戶無法在授與其資格時建立專案型商機。 如果未建立專案型商機，則下游銷售處理中將無法使用專案特定的功能。

下表包含潛在客戶的重要欄位資訊，以及這些欄位的下游含意。

| **欄位** | **位置** | **關聯性、目的和指引** | **下游影響** |
| --- | --- | --- | --- |
| 主題 | [一般] 索引標籤 | 此文字欄位應包含交易的簡短描述。 | 潛在客戶的主題會預設為商機的主題，以及報價與專案合約的名稱。 |
| 鍵入 | [一般] 索引標籤 | 此選項組欄位具有下列選項：</br>- 工作型 (只有在 Project Operations 已安裝時提供)</br>- 項目型 (只有在 Project Operations 和 Sales 已安裝時提供)</br>- 服務維護型 (安裝 Field Service 時提供) | 此欄位的值在潛在客戶上設定為**工作型**時，會授與潛在客戶資格以建立專案型商機。 若要在此交易的下游銷售處理中啟用所有專案特定擴充及功能，必須有專案型商機。 |
| 名字 | [一般] 索引標籤 | 潛在客戶連絡人的名字 | 授與專案型潛在客戶資格時，會建立客戶、連絡人和商機。 連絡人的名字是此處所設定的值。 |
| 姓氏 | [一般] 索引標籤 | 潛在客戶連絡人的姓氏 | 授與專案型潛在客戶資格時，會建立客戶、連絡人和商機。 連絡人姓氏是此處所設定的值。 |
| 公司 | [一般] 索引標籤 | 潛在客戶公司的名稱 | 授與專案型潛在客戶資格時，會建立客戶、連絡人和商機。 已建立客戶的名稱是此處所設定的值。 |
| 貨幣 | 詳細資料索引標籤 | 潛在客戶的貨幣 | 授與專案型潛在客戶資格時，會建立客戶、連絡人和商機。 已建立客戶的貨幣是此處所設定的值。 |

## <a name="qualify-a-new-project-based-lead"></a>授與新專案型潛在客戶資格

**類型**值設定為**工作型**的潛在客戶稱為專案型潛在客戶。 授與專案型潛在客戶資格時，會建立下列項目：

- 使用潛在客戶**公司**欄位的客戶。
- 與採用潛在客戶**名字**及**姓氏**欄位值之客戶相關聯的連絡人記錄。
- **類型**欄位已設定為&quot;**工作型**的專案型商機。

如需有關授與潛在客戶資格的詳細資訊，請參閱[授與客戶資格或轉換潛在客戶](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales)。

## <a name="business-process-flow-for-project-based-deals"></a>專案型交易的商務程序流程

Project Operations 中的專案型交易支援下列商務程序流程：

- 潛在客戶變商機商務程序
- 商機銷售處理

潛在客戶變商機商務程序支援下列階段：

| 階段名稱 | 對應的實體 | 功能 |
| --- | --- | --- |
| 授與資格​​ | 潛在客戶​​ | 授與潛在客戶資格以建立客戶、連絡人和商機。 |
| 開發 | 商機​​ | 開發商機以新增有關所涉及工作、主要利害關係人和競爭者的詳細資訊。 |
| 提案 | 商機​​ | 開發提案，並取得內部審查團隊的核准。 |
| 關閉​​ | 商機​​ | 贏得商機以完成交易。 |
