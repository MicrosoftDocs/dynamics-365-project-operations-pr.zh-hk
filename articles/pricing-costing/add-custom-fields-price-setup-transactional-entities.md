---
title: 將必要的自訂欄位新增至價格設定與交易實體
description: 本主題提供有關如何將必要的自訂欄位參考新增至實體以及表單和檢視表的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898333"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>將必要的自訂欄位新增至價格設定與交易實體

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

本主題假設您已完成主題[建立自訂欄位和實體以做為定價維度使用](create-custom-fields-entities-pricing-dimensions.md)中的程序。 如果您尚未完成這些程序，請返回並加以完，然後再回到本主題。 

本主題中的程序會告訴您如何將必要的自訂欄位參照新增至實體和使用者介面 (UI) 元素，例如表單和檢視表。

## <a name="add-custom-pricing-dimension-fields"></a>新增自訂定價維度欄位 
建立自訂欄位和實體之後，下一個步驟是透過建立參照欄位，讓價格設定和交易實體感知任何自訂實體或選項組。 依據定價維度清單包含的是選項組維度、實體維度還是這兩個維度都包含而定，分別依照**選項組型自訂定價維度**或**實體型自訂定價維度**或兩者中的步驟操作。

### <a name="option-set-based-custom-pricing-dimensions"></a>選項組型自訂定價維度
自訂定價維度以選項組為準時，將其新增為主要實體的欄位。 在下列程序中，**資源工作地點**和**資源工作時數**會用來做為選項組的定價維度。 這些維度必須先新增為定價實體的欄位**角色價格**和**角色價格加成**。

1. 在 Project Operations 中，選取**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取**實體 > 角色價格**。
3. 展開實體**角色價格**，並選取**欄位**。
4. 選取**新增**建立名為**資源工作地點**的新欄位，然後選取**選項組**做為欄位類型。 
5. 選取**使用現有的選項組**、選取**資源工作地點**選項組，然後選取**儲存**。
6. 重複步驟 1-5，將此欄位新增至**角色價格加成**實體。 
7. 針對**資源工作時數**選項組，重複步驟 1-5。

> [!IMPORTANT]
> 新增欄位至多個實體時，請在所有的實體中使用相同的欄位名稱。 

在專案的銷售和估計階段中，完成**本地**和**現場**工作所需的工作投入估計 (以**正常時數**和**加班時數**計) 會用來估計報價/專案的值。 **資源工作地點**和**資源工作時數**將會新增至估計實體**報價明細詳細資料**、**合約服務內容詳細資料**、**專案團隊成員**以及**估計明細**。

1. 在 Project Operations 中，選取**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取**實體 > 報價明細詳細資料**。
3. 展開**報價明細詳細資料**實體，然後選取**欄位**。
4. 選取**新增**建立名為**資源工作地點**的新欄位，然後選取欄位類型**選項組**。 
5. 選取**使用現有的選項組**，再選取**資源工作地點**，然後選取**儲存**。
6. 重複步驟 1-5，將此欄位新增至**專案合約服務內容詳細資料**、**專案團隊成員**以及**估計明細**實體。
7. 針對**資源工作時數**選項組，重複步驟 1-6。 

進行交付和開立發票時，已完成的工作必須準確定價，才能選取工作是在**本地**還是**現場**執行，以及是在專案實際值上的**正常時數**還是**加班時數**期間完成。 **資源工作地點**和**資源工作時數**欄位應新增至**時間項目**、**實際值**、**發票明細詳細資料**和**帳目明細**實體。

1. 選取**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。
2. 在方案總管的左導覽窗格中，選取**實體 > 時間項目**。
3. 展開**報價明細詳細資料**實體，然後選取**欄位**。
4. 選取**新增**建立名為**資源工作地點**的新欄位，然後選取**選項組**做為欄位類型。 
5. 選取**使用現有的選項組**、選取**資源工作地點**選項組，然後選取**儲存**。
6. 重複步驟 1-5，將此欄位新增至**實際值**、**發票明細詳細資料**和**帳目明細**實體。
7. 針對**資源工作時數**選項組，重複步驟 1-6。 

這樣就完成選項組型自訂維度所需的結構描述變更。

## <a name="entity-based-custom-pricing-dimensions"></a>實體型自訂定價維度

自訂定價維度是實體時，您將會在維度實體與主要實體之間新增 1:N 關聯。 使用上述的「標準職稱」範例，預計每個員工都會獲指派標準職稱。 因此，您將需要從「標準職稱」到「可預約資源」的 1:N 關聯，如果是建立為「可預約資源」到「標準職稱」，則需要 N:1 關聯。

1. 在 Project Operations 中，選取**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取**實體 > 標準職稱**。
3. 展開**標準職稱**實體，然後選取 **1:N 關聯**。
4. 選取**新增**以建立新的 1:N 關聯 (稱為**可預約資源的標準職稱**)。 輸入必要資訊，然後選取**儲存**。

也必須將標準職稱新增至定價實體**角色價格**和**角色價格加成**。 這也是在**標準職稱**及**角色價格**實體與**標準職稱**及**角色價格加成**實體之間使用 1:N 關聯所完成。

1. 在方案總管的左導覽窗格中，選取**實體 > 標準職稱**。
2. 展開**標準職稱**實體，然後選取 **1:N 關聯**。
3. 選取**新增**以建立新的 1:N 關聯 (稱為**角色價格的標準職稱**)。 輸入必要資訊，然後選取**儲存**。
4. 重複步驟 1 - 4，建立**標準職稱**與**角色價格加成**實體之間的 1:N 關聯。

在專案的銷售與估計階段中，若要對報價/專案定價，每個標準職稱都必須有工作投入的估計。 這表示需要從標準職稱到其中每個估計實體的 1:N 關聯： 

- **報價明細詳細資訊**
- **專案合約服務內容詳細資料**
- **專案團隊成員**
- **估計明細**

5. 重複步驟 1 - 5，建立從**標準職稱**到**報價明細詳細資訊**、**專案合約服務內容詳細資料**、**專案團隊成員**和**估計明細**的 1:N 關聯。

  在交付和開立發票階段中，每個標準職稱所完成的工作都必須根據專案實際值準確地定價。 這表示必須有從**標準職稱**到**時間項目**、**實際值**、**發票明細詳細資料**和**帳目明細**實體的 1:N 關聯。

6. 重複步驟 1 - 6，建立從**標準職稱**到**時間項目**、**實際值**、**發票明細詳細資料**和**帳目明細**實體的 1:N 關聯。

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>使用平台的對應功能設定維度值預設。
至於時間項目，讓系統根據記錄時間項目的可預約資源的時間項目來預設標準職稱，會很有幫助。 使用下列步驟，在從**可預約資源**到**時間項目**的 1:N 關聯上新增欄位對應。

1. 在方案總管的左導覽窗格中，選取**實體 > 標準職稱**。
2. 展開**標準職稱**實體，然後選取 **1:N 關聯**。
3. 按兩下**時間項目的可預約資源**。 在**關聯**頁面上，選取**使用欄位對應**。 
4. 選取**新增**，在**可預約資源**實體的**標準職稱**欄位到**時間項目**實體的**標準職稱**參照欄位之間建立新的欄位對應。 

這樣就完成實體型自訂維度所需的結構描述變更。

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>將自訂欄位新增至表單、檢視表和商務規則

進行所有必要的結構描述變更之後，下一個步驟是將欄位新增至表單和檢視表，讓欄位可以在 UI 中看到。

1. 開啟表單或檢視表。 在右導覽窗格中，選取欄位，並將其拖曳至表單畫布。 
2. 如果您正在編輯檢視表，請使用右導覽窗格，選取**新增欄位**，然後在**欄位清單**對話方塊中選取所需的欄位，然後選取**確定**。

下表提供現成可用表單及檢視表的完整清單 (依實體排列)，這需要使用新的欄位來更新。 如果您在這些實體的自訂中有任何其他檢視表或表單，也請將新欄位新增至其中。

| Entity        | 需要新欄位的表單   |需要新欄位的檢視表      |
| ------------------------------|---------------------------------|----------------------------------|
|  角色價格|• 資訊 |• 使用中資源類別價格<br> • 資源類別價格相關檢視表|
|  角色價格加成|• 資訊|• 使用中角色價格加成<br>• 角色價格加成相關檢視|
|  報價明細詳細資訊|• 專案資訊<br>• 專案快速建立|• 使用中報價明細詳細資訊<br>• 合併的報價明細詳細資料<br>• 報價明細詳細資料相關檢視表|
|  • 專案合約服務內容詳細資料|• 專案資訊<br>• 專案快速建立|• 合併的合約服務內容詳細資料<br>• 使用中合約服務內容詳細資料<br>• 合約服務內容詳細資料相關檢視表|
|  專案團隊成員|• 資訊<br>• 新表單|• 使用中專案團隊成員<br>• 專案團隊成員<br>• 專案團隊成員相關檢視表|
|  時間項目|• 資訊<br>• 建立時間項目|• 我依日期的時間項目<br>• 我本週的時間項目<br>• 供核准的時間項目|
|  帳目明細|• 資訊<br>• 快速建立|• 使用中帳目明細<br>• 帳目明細相關檢視表|
|  發票明細詳細資料|• 資訊<br>• 快速建立|• 使用中發票明細詳細資料<br>• 應收費發票交易<br>• 附贈發票交易<br>• 發票明細詳細資料相關檢視表<br>• 不應收費發票交易|
|  實際|• 資訊<br>• 使用中實際值|• 實際值相關檢視表|

可能也需要根據您定義的內容，在商務規則上新增自訂欄位。 現成可用的範例適用於商務規則**根據狀態的時間項目編輯功能**。 此規則定義時間項目處於不可編輯狀態 (**已核准**) 時，需要鎖定哪些欄位。 將欄位新增至此商務規則，以便在時間項目處於**草稿**或**已退回**以外的狀態時，鎖定欄位不得編輯。
