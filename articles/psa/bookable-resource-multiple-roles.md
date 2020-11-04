---
title: Uppskatta projektförsäljning och kostnader när en bokningsbar resurs fyller flera roller i ett projekt
description: I det här ämnet finns information om hur prissättningsdimensioner kan användas för att stödja prissättning och kostnadsberäkning för en resurs som fyller flera roller i ett projekt.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085592"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Uppskatta projektförsäljning och kostnader när en bokningsbar resurs fyller flera roller i ett projekt 

Projektbaserade företag har ofta ett behov av att en resurs ska utföra flera roller i ett projekt. Var och en av dessa roller kan vara prissatta och utgiftsberäknade på olika sätt, vilket innebär att samma resurs tid i projektet kan få en särskild ekonomisk uppskattning beroende på fakturerings- och kostnadstaxor för varje roll. Med Project Service Automation kan du konfigurera värden för teammedlemmens post för den namngivna resursen och tillåta olika åsidosättningar för varje uppgift som teammedlemmen är tilldelad till.

I följande exempel förklaras hur en enkel åsidosättning av det här värdet tillåter en resurs att ha flera roller i ett projekt med olika kostnads- och faktureringstaxor.

## <a name="create-tasks"></a>Skapa uppgifter
Skapa två projektuppgifter på 40 timmar var. Uppgift A och uppgift B. Välj uppgift A som en föregående uppgift till uppgift B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Ställ in roll och organisationsenhet för en allmän projektteammedlem

1. På sidan **schema** välj raden **uppgift** för uppgift A. 
2. I fältet **Resurser** , välj **Skapa** i den nedrullningsbara listan.
3. På sidan **Snabbregistrering av teammedlem** anger du attributen för den allmänna teammedlemmen som kan utföra uppgiften.
4. Markera lämplig roll och organisationsenhet och välj sedan **Spara och stäng**. En allmän teammedlem skapas och tilldelas den här uppgiften. 

Upprepa stegen för uppgift B och kontrollera att rollen och organisationsenheterna i den allmänna teammedlemmen som har skapats för uppgift B skiljer sig från uppgift A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Ställ in roll och organisationsenhet för en projektuppgift

1. När du har skapat uppgiften A markerar du uppgiften och väljer **Redigera uppgift**.
2. På sidan **uppgiftsinformation** hitta fälten **roll** och **organisationsenhet** och lägg till de värden som krävs för en resurs som skulle utföra denna uppgift. 

  > [!NOTE]
  > Om du genomför de här scenarierna med hjälp av information om demonstrations data för Project Service Automation kan du välja **rådgivningslead** för rollen och **Fabrikam US** som organisationsenhet.

3. Välj uppgift B och välj sedan **redigera uppgift**.
4. På sidan **uppgiftsinformation** hitta fälten **roll** och **organisationsenhet** och lägg till de värden som krävs för en resurs som skulle utföra denna uppgift. Kontrollera att värdena i fälten **roll** och **organisationsenhet** är olika i uppgift B från de för uppgift A. 

  > [!NOTE]
  > Om du genomför de här scenarierna med hjälp av information om demonstrations data för Project Service Automation kan du välja **nätverkstekniker** för rollen och **Fabrikam US** som organisationsenhet.

5. Spara och stäng sidan **uppgiftsinformation**. 

## <a name="team-member-and-estimates-behaviour"></a>Teammedlem och uppskatta beteende 

1. På sidan **uppgiftsinformation** i **teammedlem** välj de två generiska teammedlemmarna och välj sedan **generera krav**. Detta kommer att generera resurskrav. 
2. Välj en rad i teammedlemmen för **rådgivningslead** och välj sedan **boka**. Schemaläggningstavlan öppnas och bokar en resurs för det kravet.
3. Välj en rad i teammedlemmen för **nätverkstekniker** och välj sedan **boka**. Schemaläggningstavlan öppnas och bokar samma resurs öppnas på det kravet.

### <a name="team-member-grid"></a>Rutnät för teammedlem 
I rutnätet **Teammedlem** märker du att de två generiska teammedlemsposterna tas bort och att de har ersatts med en resurs. Det finns en uppsättning värden för den resursen som visar en standarduppsättning med värden för **roll** och **organisationsenhet**.
När du expanderar raden i den teammedlemmens post kan du se enskilda tilldelningar för de båda uppgifterna i teammedlemmen. Varje tilldelningsrad har uppgifter om specifika värden för **roll** och **organisationsenhet**. 

### <a name="estimates-grid"></a>Beräkningsrutnät 
När du navigerar till rutnätet **beräkning** kommer du att lägga märke till att båda tilldelningarna för samma resurs är olika.
Tilldelningen för resursens uppgift A är prissatt med hjälp av attributvärdet för **Roll** för **Rådgivningslead**. Tilldelningen för sanna resurs för uppgift B är prissatt med hjälp av attributvärdet för **Roll** för **nätverkstekniker**.





