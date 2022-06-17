---
title: Uppskattad projektförsäljning och -kostnader när en bokningsbar resurs fyller flera roller för ett projekt
description: Den här artikeln innehåller information om hur prismått kan användas för att stödja prissättning och kostnad för en resurs som fyller flera roller i ett projekt.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5adaa7b83aae69c15aa268e723417172f1b56f42
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916172"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Uppskattad projektförsäljning och -kostnader när en bokningsbar resurs fyller flera roller för ett projekt 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektbaserade företag har ofta behov av en resurs för att utföra flera roller i ett projekt. Var och en av dessa roller kan vara prissatta och utgiftsberäknade på olika sätt, vilket innebär att samma resurs tid i projektet kan få en särskild ekonomisk uppskattning beroende på fakturerings- och kostnadstaxor för respektive roll. Med Project Service Automation kan du konfigurera värden för teammedlemmens post för den namngivna resursen och tillåta olika åsidosättningar för varje uppgift som teammedlemmen är tilldelad till.

I följande exempel förklaras hur en enkel åsidosättning av det här värdet tillåter en resurs att ha flera roller i ett projekt med olika kostnads- och faktureringstaxor.

## <a name="create-tasks"></a>Skapa uppgifter
Skapa två projektuppgifter på 40 timmar var. Uppgift A och uppgift B. Välj uppgift A som en föregående uppgift till uppgift B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Ställ in roll och organisationsenhet för en allmän projektteammedlem

1. På sidan **schema** välj raden **uppgift** för uppgift A. 
2. I fältet **Resurser**, välj **Skapa** i den nedrullningsbara listan.
3. På sidan **Snabbregistrering av teammedlem** anger du attributen för den allmänna teammedlemmen som kan utföra uppgiften.
4. Markera lämplig roll och organisationsenhet och välj sedan **Spara och stäng**. En allmän teammedlem skapas och tilldelas den här uppgiften. 

Upprepa stegen för uppgift B och kontrollera att rollen och organisationsenheterna i den allmänna teammedlemmen som har skapats för uppgift B skiljer sig från uppgift A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Ställ in roll och organisationsenhet för en projektuppgift

1. När du har skapat uppgiften A markerar du uppgiften och väljer **Redigera uppgift**.
2. På sidan **uppgiftsinformation** hitta fälten **roll** och **organisationsenhet** och lägg till de värden som krävs för en resurs som skulle utföra denna uppgift. 

  > [!NOTE]
  > Om du genomför de här scenarierna med hjälp av information om demonstrations data för Project Service Automation kan du välja **rådgivningslead** för rollen och **Fabrikam US** som organisationsenhet.

3. Välj uppgift B och välj sedan **redigera uppgift**.
4. På sidan **uppgiftsinformation** hitta fälten **roll** och **organisationsenhet** och lägg till de värden som krävs för en resurs som skulle utföra denna uppgift. Kontrollera att värdena i fälten **Roll** och **Organisationsenhet** skiljer sig för Aktivitet B från värdena för Aktivitet A. 

  > [!NOTE]
  > Om du genomför de här scenarierna med hjälp av information om demonstrations data för Project Service Automation kan du välja **nätverkstekniker** för rollen och **Fabrikam US** som organisationsenhet.

5. Spara och stäng sidan **uppgiftsinformation**. 

## <a name="team-member-and-estimates-behavior"></a>Gruppmedlems- och uppskattningsbeteende 

1. På sidan **uppgiftsinformation** i **teammedlem** välj de två generiska teammedlemmarna och välj sedan **generera krav**. 
2. Välj en rad i teammedlemmen för **rådgivningslead** och välj sedan **boka**. Schemaläggningstavlan öppnas och bokar en resurs för det kravet.
3. Välj en rad i teammedlemmen för **nätverkstekniker** och välj sedan **boka**. Schemaläggningstavlan öppnas och bokar samma resurs öppnas på det kravet.

### <a name="team-member-grid"></a>Rutnät för teammedlem 
I rutnätet **Teammedlem** märker du att de två generiska teammedlemsposterna tas bort och att de har ersatts med en resurs. Det finns en uppsättning värden för den resursen som visar en standarduppsättning med värden för **roll** och **organisationsenhet**.
När du expanderar raden i den teammedlemmens post kan du se enskilda tilldelningar för de båda uppgifterna i teammedlemmen. Varje tilldelningsrad har uppgiftsspecifika värden för **Roll** och **Organisationsenhet**. 

### <a name="estimates-grid"></a>Beräkningsrutnät 
När du navigerar till rutnätet **beräkning** kommer du att lägga märke till att båda tilldelningarna för samma resurs är olika.
Tilldelningen för resursens uppgift A är prissatt med hjälp av attributvärdet för **Roll** för **Rådgivningslead**. Tilldelningen för sanna resurs för uppgift B är prissatt med hjälp av attributvärdet för **Roll** för **nätverkstekniker**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
