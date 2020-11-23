---
title: 部署 Project Operations - 精簡
description: 本主題提供有關如何安裝「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0633585fcef91d9218d6140764addb7cf96ab31d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-HK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175693"
---
# <a name="deploy-project-operations---lite"></a>部署 Project Operations - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

Project Operations 支援多個部署模型。 若要判斷最佳部署模型，請參閱[部署類型](determine-deployment-type.md)。


> [!IMPORTANT]
> 此部署 (精簡部署 – 交易至開立預估發票) 會產生 **Project Operations 的只有 Common Data Service 部署專**。

- [將 Project Operations 安裝到新的 CDS 環境中](#new)
- [安裝到現有的 CDS 環境中](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>將 Project Operations 安裝到新的 CDS 環境

1. 以持有 Project Operations 授權的 [全域和 Power Platform 管理員](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)建立新的 CDS 環境。 請確定 **CDS 資料庫** 和 **Dynamics 365 應用程式** 已啟用。 如需詳細資訊，請參閱[在 Power Platform 系統管理中心建立和管理環境](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。
2. 從 Dynamics 365 應用程式的部署清單中選取 **Microsoft Dynamics 365 Project Operations**。


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>將 Project Operations 安裝到現有的 CDS 環境

1. 以持有 Project Operations 授權的[全域或 Power Platform 管理員](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。
2. 從 Dynamics 365 應用程式的部署清單中安裝 **Microsoft Dynamics 365 Project Operations**。 如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](https://docs.microsoft.com/power-platform/admin/manage-apps)。


