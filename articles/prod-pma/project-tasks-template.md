---
title: Synkronisera projektuppgifter från Project Service Automation direkt till ekonomi och drift
description: Denna artikel beskriver de mallar och underliggande uppgifter som används för att synkronisera projektuppgifter direkt från Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028448"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisera projektuppgifter från Project Service Automation direkt till ekonomi och drift

[!include[banner](../includes/banner.md)]

Denna artikel beskriver de mallar och underliggande uppgifter som används för att synkronisera projektuppgifter direkt från Dynamics 365 Project Service Automation till Dynamics 365 Finance.

> [!NOTE]
> - OProjektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.
> - Om du använder Enterprise Edition 7.3.0 kan du, efter att du har installerat KB 4132657 och KB 4132660, använda mallarna för att integrera projektuppgifter, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och faktiska värden samt för att konfigurera låsning av funktioner. Om du måste återställa redovisningsfördelningarna bör du även installera KB-4131710.
> - Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflöde för Project Service Automation till Finance

Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance. Integreringsmallen som är tillgänglig med funktionen för dataintegrering gör det möjligt för dataflöde om projektuppgifter från Project Service Automation till Finance.

Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.

[![Dataflöde för Project Service Automation-integrering med Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mall och uppgift

Om du vill öppna mallen går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.

Följande mall och underliggande uppgift som används för att synkronisera projektaktiviteter direkt från Project Service Automation till Finance:

- **Namn på mallen i dataintegrering:** projektuppgifter (PSA till Fin and Ops)
- **Namn på aktiviteten i projektet:** projektuppgifter

Innan du kan utföra synkronisering av projektuppgifter måste du synkronisera projektkontrakt och projekt.

## <a name="entity-set"></a>Entitetsuppsättning

| Project Service Automation | Ekonomi                             |
|----------------------------|-------------------------------------|
| Projektuppgifter              | Integrationsentitet för projektuppgift |

## <a name="entity-flow"></a>Entitetsflöde

Projektaktiviteter hanteras i Project Service Automation och synkroniseras med att Finance som projektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Krav och mappningsinställningar

Innan du kan utföra synkronisering av projektuppgifter måste du synkronisera projektkontrakt och projekt.

## <a name="power-query"></a>Power Query

Du måste använda Microsoft Power Query för Excel för att filtrera data om följande villkor uppfylls:

- Du har resursspecifika poster i en projektaktivitet.

Om du måste använda Power Query följer du denna riktlinje:

- Mallen projektaktiviteter (PSA till Fin and Ops) har ett standardfilter som inte innehåller några datorspecifika poster från en projektuppgift genom att ange filtret för **IsLineTask** till **false**. Om du skapar en egen mall måste du lägga till filtret.

## <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.

[![Mallmappning.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]