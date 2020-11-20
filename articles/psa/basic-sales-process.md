---
title: Försäljningsprocesser
description: I det här ämnet finns information om de grundläggande försäljningsprocesserna.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38e02018e46943f53680babd12c7bede0a5d19de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129340"
---
# <a name="sales-processes"></a>Försäljningsprocesser

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

De försäljningsprocesser som används i en projektbaserad organisation skiljer sig från de försäljningsprocesser som används i en produktbaserad organisation. Skillnaden beror på att försäljningscykler för projektbaserade organisationer är längre och kräver anpassad uppskattningsteknik för att analysera och skapa offerter för varje avtal. Dynamics 365 Project Service Automation använder en del av samma funktioner som används i försäljningsprocessen för Dynamics 365 Sales. Här följer några exempel:

- En lead-entitet används för att spåra försäljningsprocessen.
- Kvalificera leads följs upp som affärsmöjligheter. Försäljningsprocessen kan också inledas med en affärsmöjlighet.
- Åtkomst till alla relaterade artefakter för en affärsmöjlighet. Dessa artefakter omfattar säljteamet, intressenter, sannolikhet, klassificering, försäljningsfaser och affärsprocesser.
- Flera offerter skapas för en affärsmöjlighet.
- En offert markeras som **stängd som vunnen** för att skapa en försäljningsorder. I PSA är försäljningsordern anpassad och kallas projektkontrakt.

I följande illustration visas en typisk försäljningsprocess i en projektbaserad organisation.

> ![Försäljningsprocess i en projektbaserad organisation](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Beräkna en försäljning
Försäljningsvärdet kan beräknas på grundval av projekt som tidigare har levererats och projektets komplexitet. För projekt som involverar tillägg för tidigare projekt, eller projekt där leverantörens expertis är hög och välkända arbetsmallar används, kan du använda en enklare beräkningsprocess. Mer komplexa projekt har ofta en längre inköpsprocess. Därför finns det fler stadier i försäljningsberäkningsprocessen. Tidigt i processen använder försäljningsteamet indata från kontoansvariga och ämnesexperter (SMF) för att skapa en beräkning på hög nivå för varje enskild del av det arbete som offereras. Dessa arbetskomponenter representeras av offertrader. 

Du kan skapa en beräkning på hög nivå av offerten. Detta innebär att beräkningen ersätts med en mer detaljerad beräkning som bygger på en projektplan som du skapar med hjälp av standardiserade projektmallar. Med hjälp av de här mallarna kan du skapa ett schema och bestämma valutavärden för offerten och dess komponenter (offertrader). 

Du kan skapa flera offerter för ett projekt och gruppera dem under en enskild typ av affärsmöjlighetsentitet. En av dessa offerter markeras som **stängd som vunnen** och ett projektkontrakt eller en arbetsuppgift (SOW) skapas. Ett projektkontrakt innehåller det kontrakterade värdet för varje komponent (kontraktrad) som kunden accepterar för leverans. En SOW skapas vanligtvis som ett Microsoft Word-dokument. Alla fakturor som skickas till kunden under projektets leverans refererar till projektkontraktet eller SOW.

Du kan också skapa alternativa offerter under ett affärsmöjlighets entitetstyp eller ställa in systemet så att ett projektkontrakt skapas när en offert har vunnits. I det här fallet kan du bifoga ett Word-dokument som representerar SOW för projektkontraktposten.

![Stänga en offert för att skapa ett projektkontrakt](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurera försäljningsprocessen
Du kan använda affärsprocessflöden (BPF) i Microsoft Dynamics 365 för att konfigurera försäljningsprocessen. BPF ger din försäljningspersonal ett guidat visuellt gränssnitt som de kan använda för att flytta framåt mellan de stadier som är typiska för ditt företag.

Företaget kan till exempel ha följande sex steg i försäljningsprocessen:

1. Kvalificera
2. Beräkning
3. Intern granskning
4. Kontrakt
5. Leverera
6. Stäng

Dessa sex steg representeras av (\>) som du väljer att visa i varje affärsmöjlighets entitetstyp du skapar.

![Konfiguration av affärsprocess i Dynamics 365](media/basic-guide-3.png)
 
Din organisation kan använda olika entiteter för att representera samma avtal som de utvecklas. Tidigt i försäljningsprocessen representeras en affär av entiteten för affärsmöjlighet. När tiden passerar och mer information uppstår kan du använda beräkningar på hög nivå för att skapa en eller flera offerter. Om en av dessa offerter ses över av interna och kundens intressenter, representerar den offertentiteten affären. När kunden har accepterat offerten representerar ett projektkontrakt eller ett SOW affären. För att stödja detta beteende är BPF strukturerade så att varje stadium i processen länkas till en annan databastabell.

Stadiet **Kvalificera** i försäljningsprocessen kan backas upp av en entitet för affärsmöjlighet. Faserna **Beräkna** och **Intern granskning** kan backas upp av offertentiteten. Faserna **kontrakt**, **leverans** och **stäng** kan backas upp entiteten projektkontrakt.

När du går igenom faserna uppmanas du att skapa rätt entitetsposter för att få hjälp och guida dig genom processen. Faserna kan vara villkorliga. Om du t.ex. endast behöver en intern granskning av en offert om en anpassad prislista används i offerten, kan du konfigurera villkoret i rätt stadium av affärsprocessen. Fasen **intern granskning** visas sedan endast för offerter med en anpassad prislista. För alla andra avtal och offerter följs fasen **beräkna** fasen av fasen **kontrakt**.

> [!NOTE]
> PSA har specifika sidor för entiteterna affärsmöjlighet, offert, order och faktura. Du måste skapa affärsmöjligheter, offerter, order och fakturor för Projekt Service med projektinformationssidorna för dessa entiteter. Om du använder en annan sida för att skapa en post kan du inte öppna posten från sidan **projektinformation**. Om du vill öppna en post från sidan **projektinformation** måste du ta bort posten och skapa den på nytt på sidan **projektinformation**. På sidan **projektinformation** säkerställer affärslogiken för var och en av de här entitetstyperna att fältet **Typ** är korrekt inställt och alla obligatoriska koncept är korrekt initierade.

> ![Projektinformation för en ny order](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Skillnader mellan Project Service Automation och Sales
Även om försäljnings processen i PSA använder de grundläggande funktionerna i försäljningsprocessen i Sales, har den vissa viktiga skillnader på grund av variationer i affärspraxis i projektbaserade organisationer. Här följer några exempel:

- **Projektofferter** – I Project Service Automation stängs en offert efter att ett projektkontrakt har skapats från en offert. I Sales kan du hålla en offert öppen när du har vunnit den. Anledningen till skillnaden är att en matchning mellan en offert och ett projektkontrakt är bättre för projektbaserade organisationer. 
- **Aktivering och revidering** – i PSA är aktivering och revideringar inte tillåtna i projektofferter. I Sales kan en offert låsas för att förhindra ytterligare redigeringar.
- **Stänga en offert som förlorad eller vunnen** – i PSA, när en projektoffert stängs som vunnen eller förlorad, förblir affärsmöjligheten öppen. Alla andra offerter i affärsmöjligheten stängs som förlorade. I Sales när en offert stängs som vunnen eller förlorad ombeds användaren att utföra en åtgärd för affärsmöjligheten. Beroende på användarindata kan den underliggande affärsmöjligheten vara stängd eller öppen.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Spåra ändringar av offerter och projektplaner i försäljningscykeln
Du kan inte följa upp ändringar i en offert i PSA. I stället måste du markera den befintliga offerten **Stängd som förlorad** och sedan skapa en ny offert. Du kan kopiera en offert eller klona en projektrelaterad offert med hjälp av PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Spåra kommentarer och godkännanden av offerter och projektkontrakt
Du kan hantera granskning och godkännande av offerter och projektkontrakt med hjälp av postväggar och inlägg. Din organisation kan skapa anpassade arbetsflöden och plugin-program för att tilldela, omdirigera, eskalera och hantera meddelanden om gransknings- och godkännandeuppgifter.
