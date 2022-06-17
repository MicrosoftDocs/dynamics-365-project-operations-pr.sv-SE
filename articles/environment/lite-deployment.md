---
title: Distribuera Project Operations – Lite
description: Den här artikeln innehåller information om hur du installerar Project Operations lite driftsättning - affär till proforma-fakturering.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930340"
---
# <a name="deploy-project-operations---lite"></a>Distribuera Project Operations – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_



Project Operations har stöd för flera distributionsmodeller. Information om hur du fastställer den bästa distributionsmodellen finns i [Distributionstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Den här distributionen, Enkel distribution – avtal till proforma-fakturering, resulterar i en **Dataverse-distribution av Project Operations**.

- [Installera Project Operations i en ny Dataverse-miljö](#new)
- [Installera i en befintlig Dataverse-miljö](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Installera Project Operations i en ny Dataverse-miljö

1. Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med Project Operations-licens skapar du en ny Dataverse-miljö i [administrationscentret för PowerPlatform](https://admin.powerplatform.com). Kontrollera att **Skapa en databas för den här miljön** och **Dynamics 365-appar** är aktiverade. Mer information finns i [Skapa och hantera miljöer i Power Platforms administratörscenter](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Välj **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installera Project Operations i en befintlig Dataverse-miljö
1. Se till att miljön inte har konfigurerats med [dubbelskrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), detta eftersom installationen sedan kommer att installera funktionerna för [Project Operations för resursbaserade/icke-lagerbaserade scenarier](project-operations-integrated-deployment-overview.md).
2. Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens letar du upp miljön i [PowerPlatforms administratörscenter](https://admin.powerplatform.com) där du vill installera Project Operations.
3. Installera **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar. Mer information finns i [Hantera Dynamics 365-appar](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
