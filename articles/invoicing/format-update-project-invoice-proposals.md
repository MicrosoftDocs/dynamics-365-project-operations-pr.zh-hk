---
title: 管理專案發票提案
description: 本主題提供有關使用資源/非庫存型案例適用的 Project Operations 處理客戶面向發票的詳細資料。
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4e663a9a0ca5b197e556d8c36233ab25affda876
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275880"
---
# <a name="manage-project-invoice-proposals"></a>管理專案發票提案

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

符合下列兩個條件時，您的帳務部門可以處理專案發票提案：

  - 專案經理確認 Microsoft Dataverse 中的預估發票。
  - 所有包含在預估發票中的時間和材料未開單銷售交易都是使用 Dynamics 365 **Project Operations 整合** 帳目進行過帳。

使用下列步驟，在 Dynamics 365 Finance 中完成專案發票提案。

1. 檢閱時間和材料交易的計費資訊，並將 **Project Operations 整合** 帳目過帳。
2. 檢閱固定價格帳單里程碑的計費資訊。
3. 對專案發票提案進行審查和格式化。
4. 將專案發票過帳並加以列印。

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>管理 Project Operations 整合帳目中的計費資訊

在 Dataverse 中建立的專案實際值會由專案會計師透過 Finance 進行審查和過帳。 如需有關使用整合帳目的詳細資訊，請參閱 [Project Operations 中的整合帳目](../project-accounting/project-operations-integration-journal.md)。

成本實際值與未開單銷售實際值會分別做為不同的明細項目新增至整合帳目：

  - 成本實際值上的單位成本價和成本金額會預設是源自 Dataverse 中的專案實際成本交易。
  - 未開單銷售交易上的單位銷售價和銷售金額預設是源自 Dataverse 中的專案實際未開單銷售交易。

### <a name="billing-sales-tax"></a>帳單銷售稅

帳單的銷售稅計算取決於 **Project Operations 整合** 帳目明細中未開單銷售記錄上的 **帳單銷售稅金群組** 和 **帳單項目銷售稅金群組** 欄位組合。 系統會根據 **專案管理與會計參數** 頁面中 **財務** 索引標籤上的設定，來設定這些欄位值的預設值。

- **銷售稅金群組方法** 決定預設帳單銷售稅金群組的設定邏輯：
  
  - **專案**：永遠預設使用專案中的帳單銷售稅金群組。 您可以選取 **所有專案** 頁面上的 **顯示預設會計**，來檢閱或變更專案上的預設帳單銷售稅金群組。
  - **專案合約**：永遠預設使用專案合約中的帳單銷售稅金群組。 您可以選取 **專案合約** 頁面上的 **顯示預設會計**，來檢閱或變更專案合約上的預設帳單銷售稅金群組。
  - **客戶**：永遠預設使用客戶的帳單銷售稅金群組。
  - **搜尋**：將會在所有上述實體中搜尋，並選取第一個可用的值。 搜尋先從 **專案** 實體開始，接著是 **專案合約** 實體，最後是 **客戶** 實體。

- **項目銷售稅金群組方法** 決定預設帳單項目銷售稅金群組的設定邏輯：
  
  - 對於時間、費用和服務費交易類型，預設帳單項目銷售稅金群組永遠根據 **專案類別** 實體來設定。
  - 對於物料交易類型，預設帳單項目銷售稅金群組會根據 **專案管理與會計參數** 中的 **項目銷售稅金群組方式** 設定來設定。 項目銷售稅金群組的項目編號預設是源自 **發行的產品** 實體。 項目銷售稅金群組的類別預設是源自 **專案類別** 實體。

### <a name="financial-dimensions"></a>財務維度

**Project Operations 整合** 帳目中未開單銷售記錄的財務維度預設是源自 **專案** 實際。 您可以選取 **分配金額** 來審查和調整財務維度。 如果您需要在整合帳目過帳後但在確認預估發票前變更未開單銷售記錄的財務維度，請移至 **所有專案** > **管理** > **已過帳的交易**、選取交易，然後選取 **程序** > **調整會計**。

### <a name="exchange-rates"></a>匯率

Dataverse 中的未開單交易貨幣會在 Finance 中用作交易貨幣，並使用 Finance 中定義的匯率轉換為公司的會計貨幣。


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>管理帳單里程碑的財務屬性 

使用固定價格帳務方式的專案合約服務內容是透過[固定價格里程碑](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line)來開立單票。 專案會計師可以移至 **專案管理與會計** > **所有專案** > **管理** > **賖帳交易**，對 Finance 中的帳單里程碑進行審查。

### <a name="billing-sales-tax"></a>帳單銷售稅

在 Dataverse 中建立新的帳單里程碑時，**銷售稅金群組** 及 **項目銷售稅金群組** 值預設是源自這些設定。 系統會根據 **專案管理與會計參數** 頁面中 **財務** 索引標籤上的設定，來設定這些欄位的預設值。

- **銷售稅金群組方法** 決定設定預設 **帳單銷售稅金群組** 的邏輯：

    - **專案** 永遠預設使用專案中的帳單銷售稅金群組。 您可以選取 **所有專案** 頁面上的 **顯示預設會計**，來檢閱或變更專案上的預設銷售稅金群組。
    - **專案合約** 永遠預設使用專案合約中的帳單銷售稅金群組。 您可以選取 **專案合約** 頁面上的 **顯示預設會計**，來檢閱或變更專案合約上的預設帳單銷售稅金群組。
    - **客戶** 永遠預設使用客戶的帳單銷售稅金群組。
    - **搜尋** 將會在此清單所有的實體中搜尋，並選取第一個可用的值。 搜尋先從 **專案** 實體開始，接著是 **專案合約** 實體，然後是 **客戶** 實體。

- **固定價格里程碑項目銷售稅金群組** 會用來設定 **項目銷售稅金群組** 欄位的預設值。

### <a name="financial-dimensions"></a>財務維度

固定價格帳單里程碑的預設財務維度是在專案合約服務內容中設定。 移至 **專案合約** > **顯示預設會計**，並在 **合約服務內容** 索引標籤上，選取 **價格合約服務內容**，然後設定您要用來做為預設值的財務維度值。

專案會計師直到建立專案發票提案之前，都可以編輯發票里程碑上的銷售稅和財務維度資訊。


## <a name="create-project-invoice-proposals"></a>建立專案發票提案

您可以移至 **專案發票** > **專案發票提案**，在 **專案管理與會計** 模組中審查專案發票提案。

在 Dataverse 中確認預估發票時，系統會在 Finance 中建立專案發票提案標題。 為了便於對帳，系統會將 Finance 中的專案發票提案編號設定為與 Dataverse 中的預估發票識別碼相同的數字。 由於預估發票不一定是依照其建立順序進行確認，因此 Finance 中的專案發票提案編號序列必須允許對較低和較高的編號進行變更。 使用下列步驟來設定編號序列：

1. 在 Finance 中，移至 **組織管理** > **編號序列** > **編號序列**。
2. 在 **區域** 篩選中，選取 **專案**。
3. 在 **參考** 篩選中，選取 **發票提案**。
4. 使用 **公司** 欄位來篩選每個已啟用 Project Operations Dataverse 整合的法律實體。
5. 開啟 **編號序列詳細資料**，並在 **一般** 索引標籤上進行下列設定：

    - **允許使用者變更：至較低編號** = **是**
    - **允許使用者變更：至較高編號** = **是**

專案發票提案明細是系統使用週期程序 **從暫存資料表匯入** (**專案管理與會計** > **定期** > **Project Operations 整合** > **從暫存資料表匯入**) 所新增。 您可以使用手動方式或定期排程來執行此程序。 在所有明細都已準備好開立發票之前，系統不會將明細加入至發票提案文件。 時間和材料交易只有在使用 **Project Operations 整合** 帳目過帳時，才算已準備好開立發票。

## <a name="format-and-print-invoice-proposals"></a>格式化並列印發票提案

專案會計師可以使用 **格式化發票提案** 頁面和列印管理功能來自訂專案發票列印成品。

### <a name="format-invoice-proposals"></a>格式化發票提案

**格式化發票提案** 頁面可讓自訂群組交易顯示在客戶專案發票中。

1. 在 **專案發票提案** 頁面上，選取 **列印** > **格式化發票提案**。
2. 選取 **新增**，為專案發票列印成品建立新的群組。
3. 在 **詳細資料/摘要** 欄位中，選取此群組的選項：

    - 選取 **詳細資料** 以列印客戶發票的交易詳細資料。
    - 選取 **摘要** 以列印客戶發票的交易摘要。

> [!NOTE]
> **格式化發票提案** 頁面上的 **詳細資料/摘要** 欄位選取項目會覆寫在 **發票提案** 頁面上的 **發票格式** 欄位中選取的選項，以列印詳細的發票或摘要的發票。

- 在 **可用交易** 索引標籤中選取要包含在此區段的交易明細，並選取 **包含交易** 將這些交易移到 **選取的交易**。
- 選取 **上移** 和 **下移** 來變更區段的順序。
- 選取 **預覽列印** 以預覽格式化的發票。

### <a name="print-management"></a>列印管理

列印管理使用不同的報表檔案來列印、指定目的地，以及自訂發票的頁尾文字。 您可以在模組層級設定列印管理，但是可以針對特定客戶、合約或發票提案覆寫這些設定。 若要在 **專案發票提案** 頁面上存取此功能，請選取 **列印** > **列印管理**。

列印管理安裝程式會顯示為樹狀檢視，其中每個節點層級都會顯示要調整的可用文件。 您可以在模組、客戶、合約或發票提案文件層級指派自訂列印成品。 若要修改原始檔案列印成品，請展開所需的節點，然後選取 **原始項目**。 在 **報表格式** 欄位中，選取要用於列印的報表格式。 您可以透過[商務文件管理架構](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management)來使用自訂報表格式。

## <a name="post-invoice-proposals"></a>將發票提案過帳

審查並編輯過發票之後，而且您也滿意發票提案明細時，請檢查發票總額和銷售稅。 在 **詳細資料** 群組中，選取 **總計**，然後選 **過帳** 以將發票過帳。

若要在過帳前檢視發票，請清除 **過帳** 核取方塊。 發票上會列印 **估價**，表示這是範例發票。 若要列印發票，請選取 **列印發票** 核取方塊。

除了 **發票提案** 頁面之外，還可以執行定期作業 **過帳發票提案** 來對發票提案進行過帳。 若要尋找此作業，請移至 **專案管理與會計** > **定期** > **專案發票** > **過帳發票提案**。

此頁面會顯示所有已準備好進行過帳的發票提案。 您可以選取 **批次** 來排定發票提案過帳。 將 **批次處理參數** 設定為 **是**，然後選取 **週期** 以設定批次處理的週期。


[!INCLUDE[footer-include](../includes/footer-banner.md)]