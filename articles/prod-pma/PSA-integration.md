---
title: Översikt över Project Service Automation
description: Det här ämnet innehåller information om integreringslösningen mellan Dynamics 365 Project Service Automation och Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8588e664f140ca1b0dd740d27fe6a5137da595
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685584"
---
# <a name="project-service-automation-overview"></a>Översikt över Project Service Automation

[!include[banner](../includes/banner.md)]


Integreringslösningen mellan Project Service Automation använder funktionen för dataintegrering för att synkronisera data mellan instanser av Dynamics 365 Finance och Dynamics 365 Project Service Automation via Common Data Service. Med hjälp av integreringsmallarna som är tillgängliga med funktionen för dataintegrering kan du aktivera projekt-, projektkontrakt och projektkontraktrader, milstolpar i projekt, projektuppgifter, kategorier av utgiftstransaktioner, timuppskattningar och utgiftsuppskattningar från Project Service Automation till Finance.

> [!NOTE]
> - Om du använder version 7.3.0 måste du installera KB 4074835. Du kan sedan integrera projekt med fast pris.
> - Om du använder version 7.3.0 och kopplar avgiftstransaktioner över från Project Service Automation måste du installera KB 4345320 för att kunna ta med avgifterna i projektfakturan.
> - Om du använder version 8.0 kan du använda integrering av projektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning.
> - Om du använder version 8.0.1 eller senare kan du synkronisera verkliga värden.

Innan du kan integrera Project Service Automation till Finance måste du konfigurera integreringsparametrarna för Project Service Automation. Mer information finns i [integreringsparametrar för Project Service Automation](PSA-parameters.md).

Den här integreringslösningen möjliggör direkt synkronisering i följande situationer:

- Underhåll projektkontrakt i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Skapa projekt i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Underhåll projektkontraktrader i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Underhåll milstolpar för projektkontraktrader i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Underhåll projektuppgifter i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Underhåll kategorier för utgiftstransaktioner i Finance och synkronisera dem direkt från Finance till Project Service Automation.
- Skapa uppskattning av projekttid i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Skapa uppskattning av projektutgift i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.
- Skapa för projekttid, utgift och faktiska avgifter Project Service Automation och skapa projekttransaktion i Project Service Automation integreringsjournal så att de kan bokföras i Finance.

## <a name="data-synchronization"></a>Datasynkronisering

Följande illustration visar hur datasynkroniseras som en del av integrationen mellan Project Service Automation och Finance.

> [!NOTE]
> Alla mallar är inte tillgängliga för tillfället. Mallarna kommer att publiceras när de slutförts.

[![Project Service Automation-integrering med Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemkrav för Finance

Om du vill använda Project Service Automation till Finance integreringslösningen måste du installera Enterprise Edition 7.3 med plattformsuppdatering 12 eller senare.

## <a name="system-requirements-for-project-service-automation"></a>Systemkrav för Project Service Automation

Om du vill använda integreringslösningen Project Service Automation till Finance måste du installera följande komponenter:

- Dynamics 365 Project Service Automation version 9.0.0.0 eller senare
- Lösningen potentiell kund till kontant för Dynamics 365 Sales, version 1.14.0.0 (v14) eller senare
- Project Service Automation till Finance-lösning för Dynamics 365 Project Service Automation version 1.0.0.0 eller senare

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installera integreringslösningen Project Service Automation till Finance i Project Service Automation-instansen

Hämta integreringslösningen Project Service Automation till Finance från [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) och följ anvisningarna i lösningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]