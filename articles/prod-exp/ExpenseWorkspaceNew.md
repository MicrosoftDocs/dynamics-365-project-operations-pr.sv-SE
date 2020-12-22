---
title: Nydesignade utgiftsrapporter
description: I det här ämnet finns information om den omdesignade upplevelsen för utgiftsrapportspost i Microsoft Dynamics 365 Finance. Den nya upplevelsen förenklar och påskyndar genomförandet av utgiftsrapporter.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f2acd9eab52629b0baeb82a399993fbc6337c722
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650161"
---
# <a name="redesigned-expense-reports"></a>Nydesignade utgiftsrapporter
[!include[banner](../includes/banner.md)]

Utgiftsrapportposten har omdesignats för att förenkla och påskynda genomförandet av utgiftsrapporter. Här är de viktigaste komponenterna i den nya utgiftsupplevelsen:

- En ny arbetsyta för utgiftshantering som ger dig tillgång till ombudets utgifter.
- En ny kvittomatchning som gör det lättare att visa kvitton på huvudnivån och förenklar processen för att bifoga kvitton till utgiftsrader.
- Ett nytt skrivskyddat rutnät där du kan visa många fler utgiftsrader och ytterligare kolumner med data. Nu kan du se alla specificerade och uppdelade rader, tillsammans med deras överordnade utgifter.
- Ett förenklat fönster för att redigera utgifter.
- Nya fel-, varnings- och policymeddelanden som hjälper till att garantera att du har rätt kontext för att förstå vad problemet är och hur du kan lösa det. Microsoft har tagit bort många meddelanden som visades innan användarna hade möjlighet att utföra sina uppgifter och åtgärda problemen, t.ex. ett ofullständigt specifikationsmeddelande.
- En ny sida för att ange vilka fält som krävs av organisationen, vilka fält som är valfria och vilka fält som inte ska registreras. Den här sidan hjälper dig att minska antalet fält som användare måste ange.
- En ny utformning och känsla för utgiftsrapporter så att rapporterna inte längre verkar som om de har utformats för redovisningspersoner.

Om du vill aktivera den nya upplevelsen kan du använda arbetsytan **Funktionshantering** för att aktivera funktionen **Omdesignade utgiftsrapporter**. När du aktiverar den här funktionen utförs följande åtgärder:

- Den befintliga arbetsytan för utgifter ersätts med den nya arbetsytan.
- Ett nytt menyobjekt för synlighet för utgiftsfält läggs till.
- Inga befintliga menyalternativ för utgiftsrapporter (befintlig sida) eller utgiftsrapportfält tas bort.
- Arbetsflöden och eventuella godkännanden går fortfarande till sidan befintliga utgiftsrapporter.

## <a name="getting-started-video-for-new-users"></a>Kom igång-video för nya användare

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Videon [Utgiftsupplevelse i Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (ovan) ingår i [spellistan Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som är tillgänglig på YouTube.

## <a name="new-features"></a>Nya funktioner

| Ny funktion | Beskrivning |
|---|----|
| Synlighet hos utgiftsfält | På en ny konfigurationssida kan du ange vilka fält som ska inaktiveras för en organisation, vilka fält som ska vara obligatoriska och vilka fält som rekommenderas. |
| Obligatoriska fält | Med ny enkel konfiguration kan du göra några fält obligatoriska utan att behöva använda policyramverket. |
| Valfria fält | En andra sida för valfria fält läggs till. På det här sättet känner inte de anställda att de måste ange fälten, men fälten är fortfarande lättillgängliga. |
| Lägg till icke bifogade kvitton | Möjligheten att lägga till icke bifogade kvitton i utgiftsrapporten är mer synlig från arbetsytan och i utgiftsrapporten. |
| Förbättrade meddelandefunktioner | Det finns bättre insyn i utgiftsrader som innehåller varningar eller fel. |
| Färre meddelanden i meddelandefältet| Antalet meddelanden i informationsloggen minskades och en insats gjordes för att förhindra att dubbla meddelanden visas i många fall. |
| Grupperade vanliga åtgärder | Gränssnittet rensades med tillägget av en ny åtgärdsknapp för de flesta vanliga åtgärder på radnivå och en ellipsknapp (...) för rubrik och andra mindre frekventa åtgärder. |
| Ny arbetsyta för att öka synligheten | En ny arbetsyta förenar funktioner och länkar som gör att användarna kan flytta till olika områden. |
| Lägg till befintliga utgifter och kvitton under utgiftsskapande | När du skapar utgiftsrapporter kan du lägga till alla eller valda utgifter och kvitton. |
| Kalkylator av valutakurs | En kalkylator av valutakurs läggs till, som gör att du kan beräkna valutakursen för transaktioner i flera valutor. |
| Spara och lägg till nya utgiftsrader | Knapparna **Spara** och **Ny** är tillgängliga när nya utgifter läggs till för att göra det enklare för dig att snabbt lägga till utgiftsrader. |
| Bättre insyn i delade och specificerade rader | Specificerade och uppdelade rader läggs till direkt i listan över utgifter för att öka synligheten och hjälpa dig att enkelt avgöra om det finns några policyfel eller andra fel. |
| Visa kvitton under specifikation | Kvitton kan visas under specifikation. |

Den första versionen är inriktad på scenarier för utgiftsposter. Scenarier med granskning eller godkännande av utgiftsrapporter fortsätter att använda den befintliga sidan för utgiftsposter.

Följande funktioner finns på den befintliga sidan, men finns ännu inte på den nya sidan. De här funktionerna kommer att återinföras under de kommande versionerna:

- Godkännanden
- Godkännanden av leverantörsreskontra och möjligheten att redigera redovisningen
- Flera postpunkter
- Integrering av reserekvisition
- Dataentitet för synlighet av utgiftsfält
- Post för traktamentsutgifter
- Arbetsflöde på radnivå
- Stöd för interimistiska godkännanden
- Avancerad specifikation
