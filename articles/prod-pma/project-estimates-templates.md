---
title: Synkronisera projektuppskattningar från Project Service Automation direkt till ekonomi och drift
description: Den här artikeln beskriver de mallar och underliggande uppgifter som används för att synkronisera projektets timuppskattningar och projektets utgiftsuppskattningar direkt från Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Finance.
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
ms.openlocfilehash: 2a71a2a7ca0c9179ddd5667364d8b5c9e413b917
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029827"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisera projektuppskattningar från Project Service Automation direkt till ekonomi och drift

[!include[banner](../includes/banner.md)]

Den här artikeln beskriver de mallar och underliggande uppgifter som används för att synkronisera projektets timuppskattningar och projektets utgiftsuppskattningar direkt från Dynamics 365 Project Service Automation till Dynamics 365 Finance.

> [!NOTE]
> - Projektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.
> - Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflöde för Project Service Automation till Finance

Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance. Integreringsmallar som är tillgänglig med funktionen för dataintegrering gör det möjligt för dataflöde timberäkningar och projektutgiftsberäkningar från Project Service Automation till Finance.

Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.

[![Dataflöde för Project Service Automation-integrering med Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekttimberäkningar

### <a name="template-and-tasks"></a>Mall och uppgifter

Om du vill öppna tillgängligare mallar går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.

Följande mall och underliggande uppgift som används för att synkronisera uppskattning av projekttid direkt från Project Service Automation till Finance:

- **Namn på mallen i dataintegrering:** projekttimberäkningar (PSA till Fin and Ops)
- **Namn på aktiviteterna i projektet:**

    - Transaktionsrelationer
    - Utgiftsberäkningar

### <a name="entity-set"></a>Entitetsuppsättning

| Project Service Automation | Ekonomi                                       |
|----------------------------|-----------------------------------------------|
| Projektuppgifter              | Integreringsentitet för uppskattning av projekttid |

### <a name="entity-flow"></a>Entitetsflöde

Projekttimberäkningar i Project Service Automation och synkroniseras med att Finance som prognosen för projekttid.

### <a name="prerequisites"></a>Förutsättningar

Innan du kan utföra en synkronisering av uppskattningar av projekttimmar måste du synkronisera projekt, projektaktiviteter och transaktionskategorier för projektutgifter.

### <a name="power-query"></a>Power Query

Du måste använda Microsoft Power Query för Excel i uppskattningsmallen för projekttimmar för att kunna slutföra följande uppgifter:

- Ange standard prognosmodell-ID som används när integreringen skapar nya timprognoser.
- Filtrera bort eventuella resursspecifika poster i den aktivitet som inte ska integreras i timprognoser.
- Filtrera bort tomma rader för transaktionskategori. Om du inte slutför den här uppgiften kan timprognoser bli ogiltiga.

#### <a name="set-the-default-forecast-model-id"></a>Ange standard modell-ID för prognos

Du uppdaterar standard modell-ID för prognos genom att klicka på pilen **mappning** för att öppna mappningen. Välj sedan länken **Avancerad fråga och filtrering**.

- Om du använder standardmallen projekttimberäkningar (PSA till Fin and Ops) välj **Infogade villkoret** i listan **Använda steg**. I inmatningen **Funktion** ersätt **O\_prognos** med namnet på det modell-ID för prognos som ska användas tillsammans med integrationen. Standardmallen har ett prognosmodell-ID från demonstrationsdata.
- Om du skapar en ny mall måste du lägga till den här kolumnen. I Power Query markerar du **Lägg till villkorskolumn** och anger ett namn för den nya kolumnen, till exempel **ModelID**. Ange villkoret för kolumnen där, om projektuppgiften inte är null, så \<enter the forecast model ID\>, annars null.

#### <a name="filter-out-resource-specific-records"></a>Filtrera bort specifika resursposter

Mallen projekttimberäkningar (PSA till Fin and Ops) har ett standardfilter som tar bort eventuella resursbaserade poster. Om du skapar en egen mall måste du lägga till filtret. Välj den länken **avancerade frågan och filtrering** för att filtrera kolumnen **msdyn\_islinetask** så att endast **falska** poster tas med.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrera bort tomma rader för transaktionskategori

Du måste lägga till ett filter om du vill ta bort rader som har tomma transaktionskategorier. Den här uppgiften krävs oavsett om du använder standardmallen eller skapar en egen mall. Det här filtret tar bort sammanfattningsrader från Project Service Automation som kan resultera i att timuppskattningarna i Finance blir felaktiga. Välj länken **Avancerad fråga och filter** om du vill filtrera bort null-poster i kolumnen **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.

[![Malluppgiftsmappning i dataintegration.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Beräkning av projektutgifter

### <a name="template-and-tasks"></a>Mall och uppgifter

Följande mall och underliggande uppgift som används för att synkronisera uppskattning av projektutgifter direkt från Project Service Automation till Finance:

- **Namn på mallen i dataintegrering:** uppskattning av projektutgifter (PSA till Fin and Ops)
- **Namn på aktiviteterna i projektet:**

    - Transaktionsrelationer 
    - Utgiftsberäkningar

### <a name="entity-set"></a>Entitetsuppsättning

| Project Service Automation | Ekonomi                                                  |
|----------------------------|----------------------------------------------------------|
| Transaktionskopplingar    | Integrationsentitet för projekttransaktionsrelationer |
| Beräkningsrader             | Integreringsentitet för uppskattning av projektutgifter         |

### <a name="entity-flow"></a>Entitetsflöde

Uppskattning av projektutgifter i Project Service Automation och synkroniseras med att Finance som uppskattning av projektutgifter.

### <a name="prerequisites"></a>Förutsättningar

Innan du kan utföra en synkronisering av uppskattning av projektutgifter måste du synkronisera projekt, projektaktiviteter och transaktionskategorier för projektutgifter.

### <a name="power-query"></a>Power Query

Du måste använda Power Query i mallen för projektets utgiftsuppskattningar för att slutföra följande uppgifter:

- Filtrera så att endast radposter för uppskattning av projekt.
- Ange standard prognosmodell-ID som används när integreringen skapar nya timprognoser.
- Omvandla faktureringstyperna.
- Omvandla transaktionstyper.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrera så att endast för uppskattning av utgiftsrader

Mallen beräkning av projektutgifter (PSA till Fin and Ops) har ett standardfilter som endast innehåller utgiftsrader i integrationen. Om du skapar en egen mall måste du lägga till filtret. Välj uppgiften **transaktionsrelationer** och klicka sedan på pilen **Mappning**. Välj länken **Avancerad fråga och filtrering**. Filtrera kolumnen **msdyn\_transactiontype1** så att den endast innehåller **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Ange standard modell-ID för prognos

Du uppdaterar standard modell-ID för prognos genom att välja uppgiften **Utgiftsberäkningar** och klicka sedan pilen **Mappning** för att öppna mappningen. Välj länken **Avancerad fråga och filtrering**.

- Om du använder standardmallen för faktiska projektutgifter ("PSA till Fin och Ops"), välj då första **Infogade villkor** i avsnittet **Tillämpade steg** i Power Query. I inmatningen **Funktion** ersätt **O\_prognos** med namnet på det modell-ID för prognos som ska användas tillsammans med integrationen. Standardmallen har ett prognosmodell-ID från demonstrationsdata.
- Om du skapar en ny mall måste du lägga till den här kolumnen. I Power Query markerar du **Lägg till villkorskolumn** och anger ett namn för den nya kolumnen, till exempel **ModelID**. Ange villkoret för kolumnen där, om ID för uppskattningsrad inte är null, så \<enter the forecast model ID\>, annars null.

#### <a name="transform-the-billing-types"></a>Omvandla faktureringstyperna

Mallen beräkning av projektutgifter (PSA till Fin and Ops) innehåller en villkorlig kolumn som används för att omvandla de faktureringstyper som tas emot från Project Service Automation under integrationen. Om du skapar en egen mall måste du lägga till villkorlig kolumn. Välj länken **Avancerad fråga och filtrering** och välj sedan **Lägg till villkorlig kolumn**. Ange ett namn för den nya kolumnen t.ex. **Faktureringstyp**. Ange därefter följande villkor:

Om **msdyn\_billingtype** = 192350000, sedan **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, sedan **Debiterbar**  
else if **msdyn\_billingtype** = 192350002, sedan **Kostnadsfri**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Omvandla transaktionstyper

Mallen beräkning av projektutgifter (PSA till Fin and Ops) innehåller en villkorlig kolumn som används för att omvandla de transaktionstyper som tas emot från Project Service Automation under integrationen. Om du skapar en egen mall måste du lägga till villkorlig kolumn. Välj länken **Avancerad fråga och filtrering** och välj sedan **Lägg till villkorlig kolumn**. Ange ett namn för den nya kolumnen t.ex. **TransactionType**. Ange därefter följande villkor:

Om **msdyn\_transactiontypecode** = 192350000, sedan **Kostnad**  
else if **msdyn\_transactiontypecode** = 192350005, sedan **Försäljning**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

I följande illustration visas exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.

[![Mallmappning av transaktioner av utgiftsuppskattning.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mallmappning av utgiftsuppskattningar.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]