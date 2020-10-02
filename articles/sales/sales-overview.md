---
title: Översikt över försäljning
description: I det här ämnet finns information om de grundläggande försäljningsprocesserna.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: e66d96a940f3b22d5d1f3372d2b6767a4482d925
ms.sourcegitcommit: 7750485f8685a2ca5e1b3c165ead24a3b583c447
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3892362"
---
# <a name="sales-processes-overview"></a>Översikt över försäljning

De försäljningsprocesser som används i en projektbaserad organisation skiljer sig från de försäljningsprocesser som används i en produktbaserad organisation. Detta beror på att försäljningscykler för projektbaserade organisationer är längre och kräver anpassad uppskattningsteknik för att analysera och skapa offerter för varje avtal. Dynamics 365 Project Operations använder en del av följande funktioner som används i försäljningsprocessen:

- En leadpost används för att spåra försäljningsprocessen.
- Kvalificera leads följs upp som affärsmöjligheter.
- Åtkomst till alla relaterade artefakter för en affärsmöjlighet. Dessa artefakter omfattar säljteamet, intressenter, sannolikhet, klassificering, försäljningsfaser och affärsprocesser.
- Flera offerter skapas för en affärsmöjlighet.
- En offert ges statusen som **stängd som vunnen** för att skapa en försäljningsorder. I Project Operations är försäljningsordern anpassad och kallas projektkontrakt.

## <a name="estimate-a-sale"></a>Beräkna en försäljning
Försäljningsvärdet kan beräknas på grundval av projekt som tidigare har levererats och projektets komplexitet. För projekt som involverar tillägg för tidigare projekt, eller projekt där leverantörens expertis är hög och välkända arbetsmallar används, kan du använda en enklare beräkningsprocess. Mer komplexa projekt har ofta en längre inköpsprocess. Därför finns det fler stadier i försäljningsberäkningsprocessen. Tidigt i processen använder försäljningsteamet indata från kontoansvariga och ämnesexperter (SMF) för att skapa en beräkning på hög nivå för varje enskild del av det arbete som offereras. Dessa arbetskomponenter representeras av offertrader. 

Du kan skapa en beräkning på hög nivå av offerten. Detta innebär att beräkningen ersätts med en mer detaljerad beräkning som bygger på en projektplan som du skapar med hjälp av standardiserade projektmallar. Med hjälp av de här mallarna kan du skapa ett schema och bestämma valutavärden för offerten och dess komponenter (offertrader). 

Du kan skapa flera offerter för ett projekt och gruppera dem under en enskild typ av affärsmöjlighetspost. En av dessa offerter markeras som **stängd som vunnen** och ett projektkontrakt eller en arbetsuppgift (SOW) skapas. Ett projektkontrakt innehåller det kontrakterade värdet för varje komponent (kontraktrad) som kunden accepterar för leverans. En SOW skapas vanligtvis som ett Microsoft Word-dokument. Alla fakturor som skickas till kunden under projektets leverans refererar till projektkontraktet eller SOW.

Du kan också skapa alternativa offerter under ett affärsmöjlighetspost eller ställa in systemet så att ett projektkontrakt skapas när en offert har vunnits. I det här fallet kan du bifoga ett Word-dokument som representerar SOW för projektkontraktposten.

## <a name="configure-the-sales-process"></a>Konfigurera försäljningsprocessen
Du kan använda affärsprocessflöden för att konfigurera försäljningsprocessen. Dessa flöden tillhandahåller ett guidat visuellt gränssnitt för att flytta fram affärer steg för steg i försäljningsprocessen.

Företaget kan till exempel ha följande sex steg i försäljningsprocessen:

1. Kvalificera
2. Beräkning
3. Intern granskning
4. Kontrakt
5. Leverera
6. Stängning
 
Din organisation kan använda olika entiteter för att representera samma avtal som de utvecklas. Tidigt i försäljningsprocessen representeras en affär av entiteten för affärsmöjlighet. När tiden passerar och mer information uppstår kan du använda beräkningar på hög nivå för att skapa en eller flera offerter. Om en av dessa offerter ses över av interna och kundens intressenter, representerar den offertentiteten affären. När kunden har accepterat offerten representerar ett projektkontrakt eller ett SOW affären. För att stödja detta beteende är BPF strukturerade så att varje stadium i processen länkas till en annan databastabell.

Stadiet **Kvalificera** i försäljningsprocessen kan backas upp av en entitet för affärsmöjlighet. Faserna **Beräkna** och **Intern granskning** kan backas upp av offertentiteten. Faserna **kontrakt**, **leverans** och **stäng** kan backas upp entiteten projektkontrakt.

När du går igenom faserna uppmanas du att skapa rätt entitetsposter för att få hjälp och guida dig genom processen. Faserna kan vara villkorliga. Om du t.ex. endast behöver en intern granskning av en offert om en anpassad prislista används i offerten, kan du konfigurera villkoret i rätt stadium av affärsprocessen. Fasen **intern granskning** visas sedan endast för offerter med en anpassad prislista. För alla andra avtal och offerter följs fasen **beräkna** fasen av fasen **kontrakt**.

> [!NOTE]
> Project Operations har specifika sidor för affärsmöjlighets-, offert-, order- och fakturaentitetsposter. Du måste skapa posterna med hjälp av projektinformationssidorna för dessa entiteter. Annars kan du inte öppna posterna från sidan **projektinformation**. Om du vill öppna en post från **Projektinformation** måste du ta bort posten och skapa den på nytt med hjälp av sidan **Projektinformation** där affärslogiken för var och en av dessa enhetstyper säkerställer att sidan **Typ** för posten anges korrekt och att alla obligatoriska begrepp är korrekt initierade.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Spåra ändringar av offerter och projektplaner i försäljningscykeln
I Project Operations kan du inte följa upp ändringar i en offert. I stället måste du markera den befintliga offerten **Stängd som förlorad** och sedan skapa en ny offert. Du kan kopiera en offert eller klona en projektrelaterad offert.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Spåra kommentarer och godkännanden av offerter och projektkontrakt
Du kan hantera granskning och godkännande av offerter och projektkontrakt med hjälp av postväggar och inlägg. Din organisation kan skapa anpassade arbetsflöden och plugin-program för att tilldela, omdirigera, eskalera och hantera meddelanden om gransknings- och godkännandeuppgifter.
