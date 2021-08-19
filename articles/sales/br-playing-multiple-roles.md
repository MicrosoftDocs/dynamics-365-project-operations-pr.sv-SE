---
title: Uppskattad projektförsäljning och -kostnader när en bokningsbar resurs fyller flera roller i ett projekt
description: I detta ämne förklaras hur du använder prissättningsdimensioner för att stödja pris- och kostnadsberäkningar för en resurs som fyller flera roller i ett projekt.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28a67e79b03dfbc38e9786350c931838ef27891a3d26787fc0334e0572528228
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990158"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Uppskattad projektförsäljning och -kostnader när en bokningsbar resurs fyller flera roller i ett projekt 

_**Gäller till:** Project Operations för resursscenarier/icke-lagerbaserade scenarier, Lite-distribution - avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_ 

Projektbaserade företag har ofta behov av en resurs för att fylla flera roller i ett projekt. Varje roll kan prissättas och kostnadsberäknas på olika sätt. Det innebär att samma resurstid på ett projekt skulle kunna få en annan ekonomisk uppskattning beroende på faktura- och kostnadssatser för respektive roll. Du kan ställa in värdena på gruppmedlemsposten för den namngivna resursen med olika åsidosättningar på var och en av de uppgifter som gruppmedlemmen är tilldelad till.

I följande exempel går du igenom hur den enkla åsidosättningen av ett värde gör att en resurs kan ha flera roller i ett projekt med olika kostnads- och fakturasatser.

## <a name="create-tasks"></a>Skapa uppgifter
Om du vill skapa uppgifter måste du lägga till både uppgifter och sammanfattningsuppgifter, varefter du måste tilldela uppgiften innan du lägger till uppgiftens varaktighet. 

### <a name="add-tasks-and-summary-tasks"></a>Lägg till uppgifter och sammanfattningsuppgifter
Följ stegen nedan för att lägga till en uppgift.

1. Gå till **Projekt** och öppna projektet som du vill lägga till uppgifter till.
2. Välj **Lägg till ny uppgift**. Namnge uppgiften och tryck sedan på **Retur**.
3. Ange namnet på en annan uppgift och tryck på **Retur**. Upprepa detta tills du har en fullständig lista över uppgifter.
3. Om du vill dra in uppgifter under **Sammanfattningsuppgifter** markerar du de tre lodräta punkterna efter aktivitetsnamnet och väljer sedan **Underuppgift**. 

  > [!TIP]
  > Om du vill markera mer än en uppgift markerar du en uppgift, trycker samt håller nere **Ctrl** och väljer sedan en annan uppgift.
  >
  > Du kan också välja **Flytta upp underuppgift** om du vill flytta upp uppgifter så att dessa hamnar ovanför **Sammanfattningsuppgifter**.

### <a name="assign-tasks"></a>Tilldela uppgifter

Följ stegen nedan för att tilldela uppgifter.

1. I kolumnen **Tilldelad till** för en uppgift väljer du personikonen.
2. Välj en gruppmedlem i listan eller ange text för att söka efter ett namn.

### <a name="add-task-duration-and-columns"></a>Lägg till uppgiftens varaktighet och kolumner

Det är ofta enklast att börja skapa ditt projekt med varaktighet. Följ stegen nedan för att lägga till varaktigheten för en uppgift.

1. I kolumnen **Varaktighet** för en uppgift anger du det antal dagar du tror kommer att krävas för att slutföra uppgiften. Om du vill använda en annan tidsenhet anger du ett tal plus ordet **timmar**, **veckor** eller **månader**.
2. Om du vill att din uppgift ska visas som en rombformad milstolpe i vyn **Tidslinje** går du till kolumnen **Varaktighet** och anger **0 dagar**.
3. Tryck på **Retur** för att gå till fältet **Varaktighet** för nästa uppgift och fortsätta ange varaktigheter.

  > [!NOTE]
  > Du kan inte ange en varaktighet för sammanfattningsuppgifter.

Du kan lägga till kolumner i projektet i syfte att ange mer information. Detta gör du genom att välja **Lägg till kolumn**. 

Mer information finns i [Skapa ett projekt](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Ställ in roll- och organisationsenheten för en generisk projektgruppmedlem
Slutför följande steg för att ställa in en roll och en organisationsenhet för en generisk gruppmedlem.

1. På sidan **Uppgifter** väljer du raden **Uppgift** för **Uppgift A**. 
2. I **Tilldelad till** väljer du **Lägg till allmän resurs**. Då öppnas sidan **Snabbregistrering för gruppmedlem**.
3. På sidan **Snabbregistrering av gruppmedlem** anger du attributen för den allmänna gruppmedlemmen som kan utföra uppgiften.
4. Markera lämplig roll och organisationsenhet och välj sedan **Spara och stäng**. En allmän gruppmedlem skapas och tilldelas den här uppgiften. 
5. Upprepa steg 1-4 för **Aktivitet B**. Uppgift **B** måste dock ha en annan roll och organisationsenhet som är tilldelad för den generiska gruppmedlemmen än **Aktivitet A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Ställ in roll- och organisationsenheten för en projektuppgift
Slutför följande steg för att ställa in en roll och en organisationsenhet för en uppgift.

1. När du har skapat **Uppgift A** markerar du uppgiften och väljer sedan ikonen **i** för att öppna fönstret **Uppgiftsinformation**. 
2. I fönstret **Åtgärdsinformation** bläddrar du längst ned och väljer **Visa information** för att öppna sidan **Uppgiftsinformation**.
3. På sidan **Uppgiftsinformation**, under **Roll** och **Organisationsenhet**, lägger du till de värden som krävs för att utföra denna uppgift för resursen. 

  > [!NOTE]
  > Om du slutför detta scenario med hjälp av Project Operations-demodata väljer du **Rådgivningslead** för rollen och **Fabrikam US** som organisationsenhet.

4. Markera **Uppgift B** och välj sedan uppgiften.
5. Välj ikonen **i** för att öppna fönstret **Uppgiftsinformation**. 
6. I fönstret **Uppgiftsinformation** bläddrar du längst ned och väljer **Visa information** för att öppna sidan **Uppgiftsinformation**.
7. På sidan **Uppgiftsinformation**, under **Roll** och **Organisationsenhet**, lägger du till de värden som krävs av en resurs som ska utföra denna uppgift. Värdena i **Roll** och **Organisationsenhet** för **Uppgift B** vår inte vara desamma som värdena för **Uppgift A**. 

  > [!NOTE]
  > Om du slutför detta scenario med hjälp av Project Operations-demodata väljer du **Nätverkstekniker** för rollen och **Fabrikam US** som organisationsenhet.

8. Spara och stäng sidan **uppgiftsinformation**. 

## <a name="team-member-and-estimates-behavior"></a>Gruppmedlems- och uppskattningsbeteende 
Om du vill förstå beteendet i rutnätet **Gruppmedlem** och i uppskattningarna, slutför du följande steg.

1. Välj de två allmänna gruppmedlemmarna i rutnätet **Gruppmedlem** och välj sedan **Generera krav**. Detta kommer att generera resurskrav. 
2. Välj gruppmedlemsraden för **Rådgivningslead** och välj sedan **Boka**. Schematavlan öppnas med en lista med resurser. Välj en resurs och välj sedan **Boka** för att boka resursen till det kravet.
3. Välj gruppmedlemsraden för **Nätverkstekniker** och välj sedan **Boka**. Schematavlan öppnas med en lista med resurser. Välj samma resurs som ovan och välj sedan **Boka** för att boka resursen till det kravet.

### <a name="team-member-grid"></a>Rutnät för gruppmedlem 

På rutnätet **Gruppmedlem** tas de två allmänna gruppmedlemsposterna bort och ersätts med endast en resurs. Det finns en uppsättning värden för den resursen, som är en standarduppsättning med värden för **Roll** och **Organisationsenhet**.

När du expanderar raden för den gruppmedlemsposten kan du se distinkta tilldelningar på gruppmedlemsposten för båda aktiviteter. Varje tilldelningsrad har uppgiftsspecifika värden för **Roll** och **Organisationsenhet**. 

### <a name="estimates-grid"></a>Beräkningsrutnät 

På rutnätet **Uppskattningar** prissätts båda tilldelningar för samma resurs på olika sätt. Tilldelningen för resursen tillhörande **Uppgift A** prissätts med hjälp av attributvärdet **Rådgivningslead** för **Roll**. Tilldelningen för samma resurs för **Uppgift B** prissätts med hjälp av attributvärdet **Nätverkstekniker** för **Roll**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]