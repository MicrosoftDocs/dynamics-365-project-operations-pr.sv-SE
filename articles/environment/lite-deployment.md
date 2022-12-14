---
title: Distribuera Project Operations Lite
description: Den här artikeln innehåller information om hur du installerar Project Operations lite driftsättning - affär till proforma-fakturering.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811001"
---
# <a name="deploy-project-operations-lite"></a>Distribuera Project Operations Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_



Project Operations har stöd för flera distributionsmodeller. Information om hur du fastställer den bästa distributionsmodellen finns i [Distributionstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Den här distributionen, Enkel distribution – avtal till proforma-fakturering, resulterar i en **Dataverse-distribution av Project Operations**.

- [Installera Project Operations i en ny Dataverse-miljö](#new)
- [Installera i en befintlig Dataverse-miljö](#existing)
- [Installera i en befintlig Dataverse-miljö med dubbla skrivkomponenter](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Installera Project Operations Lite i en ny Dataverse-miljö

1. Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med Project Operations-licens skapar du en ny Dataverse-miljö i [administrationscentret för PowerPlatform](https://admin.powerplatform.com). Kontrollera att **Skapa en databas för den här miljön** och **Dynamics 365-appar** är aktiverade. Mer information finns i [Skapa och hantera miljöer i Power Platforms administratörscenter](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Välj **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installera Project Operations Lite i en befintlig Dataverse-miljö 
1. Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens letar du upp miljön i [PowerPlatforms administratörscenter](https://admin.powerplatform.com) där du vill installera Project Operations.
1. Installera **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar. Mer information finns i [Hantera Dynamics 365-appar](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Installera Project Operations Lite i en befintlig Dataverse-miljö där det redan finns lösningar för dubbelriktad skrivning

Om du vill fortsätta köra Project Operations i Lite-distributionsläge gör du följande:

1. Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens letar du upp miljön i [PowerPlatforms administratörscenter](https://admin.powerplatform.com) där du vill installera Project Operations.
1. Installera **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar. Mer information finns i [Hantera Dynamics 365-appar](/power-platform/admin/manage-apps).
1. Eftersom miljön har dubbla skrivkomponenter som gör det enkelt att integrera appar för ekonomi och drift installeras, installerar Project Operations även de funktioner och tillägg som krävs för att integrera Projektrelaterade data för appar för ekonomi och drift. Eftersom du vill köra Project Operations i Lite-distributionen bör dessa integrationskomponenter tas bort eftersom de skapar begränsningar och distributionsscenarier för Lite. Avinstallera manuellt lösningarna **Dynamics 365 Project Operations dubbelskrivning** och **Dynamics 365 Project Operations entitetskartor för dubbelskrivning** för att ta bort dessa komponenter.
1. Gå till **Project Operations -> Inställningar -> Parametrar**. Öppna informationssidan **projektparameter** och ange fältet **Beteende för lösningsuppgradering** till **endast Lite**. På så sätt säkerställer du att alla efterföljande uppgraderingar av Project Operations inte för tillbaka integreringskomponenterna i Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
