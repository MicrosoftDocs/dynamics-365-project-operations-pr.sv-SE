---
title: Synkronisera projektets faktiska värden från Project Service Automation direkt till projektets integreringsjournal för bokföring i Finance and Operations
description: Detta ämne beskriver de mallar och underliggande uppgifter som används för att synkronisera projektets faktiska värden direkt från Microsoft Dynamics 365 Project Service Automation till Finance and Operations.
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
ms.openlocfilehash: 12929c324bb3a7c344edc9be2e3a8f4941ff9ea4
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683560"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkronisera projektets faktiska värden från Project Service Automation direkt till projektets integreringsjournal för bokföring i Finance and Operations

[!include[banner](../includes/banner.md)]

Detta ämne beskriver de mallar och underliggande uppgifter som används för att synkronisera faktiska projektvärden direkt från Dynamics 365 Project Service Automation till Dynamics 365 Finance.

Mallen synkroniserar transaktioner från Project Service Automation till en mellanlagringstabell i Finance. När synkroniseringen har slutförts **måste** importera data från mellanlagringstabellen till integrationsjournalen.

> [!NOTE]
> - Projektets verkliga integreringsfunktion kan starta i version 8.0.1.
> - Om du använder Enterprise Edition 7.3.0 kan du, efter att du har installerat KB 4132657 och KB 4132660, använda mallarna för att integrera projektuppgifter, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och faktiska värden samt för att konfigurera låsning av funktioner. Om du måste återställa redovisningsfördelningarna bör du även installera KB 4131710.
> - Om du använder version 7.3.0 och kopplar avgiftstransaktioner över från Project Service Automation måste du installera KB 4345320 för att kunna ta med avgifterna i projektfakturan.
> - Om du anger momsbelopp för tids- eller utgiftstransaktioner vid Project Service Automation måste du installera uppdatering 7 för Project Service Automation. Annars länkas inte den faktiska momsen till den associerade tiden eller den aktuella kostnaden och de synkroniseras inte med Finance. Kontakta support för mer information.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflöde för Project Service Automation till Finance

Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance. Integreringsmallar som är tillgängliga med funktionen för dataintegrering gör det möjligt för dataflöde om projektets verkliga värden från Project Service Automation till Finance.

Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.

[![Dataflöde för integrering av Project Service Automation med Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projektets faktiska värden från Project Service Automation

### <a name="template-and-tasks"></a>Mall och uppgifter

Om du vill öppna tillgängligare mallar går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.

Följande mall och underliggande uppgift som används för att synkronisera projektets faktiska värden direkt från Project Service Automation till Finance:

- **Namn på mallen i dataintegrering:** projektets faktiska värden (PSA till Fin and Ops)
- **Namn på aktiviteterna i projektet:**

    - Faktiska värden
    - TransactionConnections

### <a name="entity-set"></a>Entitetsuppsättning

| Project Service Automation | Ekonomi                                   |
|----------------------------|----------------------------------------------------------|
| Faktiska värden                    | Integrationsentitet för projektets faktiska värden                   |
| Transaktionskopplingar    | Integrationsentitet för projekttransaktionsrelationer |

### <a name="entity-flow"></a>Entitetsflöde

Projektets faktiska värden hanteras i Project Service Automation och synkroniseras med projektets integreringsjournal i Finance. Redovisningen tillämpas utifrån de ekonomiska dimensionerna och bokföringsinställningarna.

### <a name="prerequisites"></a>Förutsättningar

Innan synkronisering av verkliga värden kan inträffa måste du konfigurera integreringsparametrarna för Project Service Automation och synkronisera projekt, projektaktiviteter och transaktionskategorier för projektutgifter.

### <a name="power-query"></a>Power Query

Du måste använda Microsoft Power Query för Excel i uppskattningsmallen för projekt för att kunna slutföra följande uppgifter:

- Omvandla transaktionstypen i Project Service Automation till rätt transaktionstyp i Finance. Den här omvandlingen har redan definierats i mallen projektets faktiska värden (PSA till Fin and Ops).
- Omvandla faktureringstypen i Project Service Automation till rätt faktureringstyp i Finance. Den här omvandlingen har redan definierats i mallen projektets faktiska värden (PSA till Fin and Ops). Faktureringstypen mappas sedan till radegenskapen utifrån konfigurationen på sidan **Project Service Automation integreringsparametrar**.
- Filtrera efter specifika resursorganisationsenheter som måste synkroniseras med mallen.
- Om verkliga värden för koncernintern tid eller koncerninterna utgifter ska synkroniseras med Finance måste du omvandla organisationsenheten till rätt juridisk person i Finance. I mallen projektets faktiska värden (PSA till Fin and Ops) definieras en villkorskolumn utifrån demonstrationsdata. Du måste uppdatera den sist infogade villkorliga kolumnen till rätt juridiska entiteter. Annars kan ett integrationsfel inträffa, eller så kan felaktiga faktiska transaktioner importeras till Finance.
- Om verkliga värden för koncernintern tid eller koncerninterna utgifter inte synkroniseras med Finance måste du ta bort den senast infogade villkorliga kolumnen från mallen. Annars kan ett integrationsfel inträffa, eller så kan felaktiga faktiska transaktioner importeras till Finance.

#### <a name="contract-organizational-unit"></a>Omvandla organisationsenheter
Du uppdaterar den infogade villkorliga kolumnen i mallen genom att klicka på pilen **mappning** för att öppna mappningen. Välj länken **Avancerade frågor och filter** för att öppna Power Query.

- Om du använder standardmallen för faktiska projektvärden ("PSA till Fin och Ops"), välj då senaste **Infogat villkor** i avsnittet **Tillämpade steg** i Power Query. I inmatningen **Funktion** ersätt **USSI** med namnet på den juridiska personen som ska användas tillsammans med integrationen. Lägg till ytterligare villkor i posten **funktion** som du behöver och uppdatera villkoret **else** från **USMF** till rätt juridisk person.
- Om du skapar en ny mall måste du lägga till kolumnen som stöd för koncernintern tid och utgifter. Markera **Lägg till villkorlig kolumn** och ange ett namn för kolumnen, t.ex. **LegalEntity**. Ange ett villkor för kolumnen där, om **msdyn\_contractorganizationalunitid.msdyn\_name** är \<organizational unit\>, så \<enter the legal entity\>, annars null.

### <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.

[![Mallmappning – faktiska värden.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mallmappning – transaktionsanslutningar.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importera från mellanlagringstabellen efter integrering med Project Service Automation

Den periodiska processen Importera från mellanlagringstabellen måste köras efter synkronisering av fakta från Project Service Automation till Finance. Med den här processen importeras projekttransaktionerna från mellanlagringstabellen till integrationsjournalen för Project Service Automation, där redovisningen tillämpas och de importerade transaktionerna kan bokföras. Vi rekommenderar att du kör den här processen i batchläge, den kan konfigureras att köras som en återkommande batch.

## <a name="update-actuals-from-finance"></a>Uppdatera verkliga värden från Finance

### <a name="template-and-tasks"></a>Mall och uppgifter

Följande mall och underliggande uppgifter används för att synkronisera verifikationsnummer och moms för bokförda projekt transaktioner från Finance till Project Service Automation:

- **Namn på mallen i dataintegrering:** uppdatering av projektets faktiska värden (Fin Ops till PSA)
- **Namn på aktiviteterna i projektet:**

    - Faktiska värden 
    - TransactionConnections

### <a name="entity-set"></a>Entitetsuppsättning

| Ekonomi                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integrationsentitet för projektets faktiska värden                   | Faktiska värden                    |
| Integrationsentitet för projekttransaktionsrelationer | Transaktionskopplingar    |

### <a name="entity-flow"></a>Entitetsflöde

Projektets faktiska värden hanteras i Project Service Automation och synkroniseras med projektets integreringsjournal i Finance. När verkliga värden har bokförts i Finance uppdateras de i Project Service Automation med verifikationsnumret från Finance. Om moms lades till i Finance skapas nya faktiska värden för moms i Project Service Automation.

### <a name="power-query"></a>Power Query

Du måste använda Power Query i uppdateringsmallen för faktiska projektvärden för att kunna slutföra följande uppgifter:

- Omvandla transaktionstypen i Finance till rätt transaktionstyp i Project Service Automation. Den här omvandlingen har redan definierats i mallen uppdatering av projektets faktiska värden (Fin Ops till PSA).
- Omvandla faktureringstypen i Finance till rätt faktureringstyp i Project Service Automation. Den här omvandlingen har redan definierats i mallen uppdatering av projektets faktiska värden (Fin Ops till PSA).

### <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

I följande illustration visas exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Finance till Project Service Automation.

[![Mallmappning – uppdatering av faktiska värden.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mallmappning – transaktionsuppdatering.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]