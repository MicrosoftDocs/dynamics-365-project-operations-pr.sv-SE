---
title: Distribuera Project Operations – Lite
description: I det här ämnet finns information om hur du installerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290111"
---
# <a name="deploy-project-operations---lite"></a>Distribuera Project Operations – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations har stöd för flera distributionsmodeller. Information om hur du fastställer den bästa distributionsmodellen finns i [Distributionstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Den här distributionen, Enkel distribution – avtal till proforma-fakturering, resulterar i en **Common Data Service-distribution av Project Operations**.

- [Installera Project Operations i en ny CDS-miljö](#new)
- [Installera i en befintlig CDS-miljö](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Installera Project Operations i en ny CDS-miljö

1. Som [Global eller Power Platform-administratör](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skapar du en ny CDS-miljö i [PowerPlatforms administratörscenter](https://admin.powerplatform.com). Kontrollera att **CDS-databasen** och **Dynamics 365-apparna** är aktiverade. Mer information finns i [Skapa och hantera miljöer i Power Platforms administratörscenter](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Välj **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Installera Project Operations i en befintlig CDS-miljö

1. Som [Global eller Power Platform-administratör](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens letar du upp miljön i [PowerPlatforms administratörscenter](https://admin.powerplatform.com) där du vill installera Project Operations.
2. Installera **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar. Mer information finns i [Hantera Dynamics 365-appar](https://docs.microsoft.com/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]