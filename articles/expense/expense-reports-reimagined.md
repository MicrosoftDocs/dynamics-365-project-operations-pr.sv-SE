---
title: Ny typ av utgiftsrapporter
description: I det här ämnet finns information om den omdesignade erfarenheten för utgiftsrapportspost.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122828"
---
# <a name="expense-reports-reimagined"></a>Ny typ av utgiftsrapporter

Utgiftsrapportposten har omdesignats för att förenkla processen och minska den tid som krävs för att slutföra en rapport. Här är de viktigaste komponenterna i den nya utgiftsupplevelsen:

- En ny arbetsyta för utgiftshantering som ger dig tillgång till ombudets utgifter.
- En ny kvittomatchning som gör det lättare att visa kvitton på huvudnivån och förenklar processen för att bifoga kvitton till utgiftsrader.
- Ett nytt skrivskyddat rutnät där du kan visa många fler utgiftsrader och ytterligare kolumner med data. Nu kan du se alla specificerade och uppdelade rader, tillsammans med deras överordnade utgifter.
- Ett förenklat fönster för att redigera utgifter.
- Nya fel-, varnings- och policymeddelanden som ger korrekt sammanhang och förståelse för problemet och hur du löser det. Vi har tagit bort flera av meddelandena som visades innan användarna kunde slutföra sina uppgifter och åtgärda problemen.
- En ny sida för att ange obligatoriska fält, valfria fält och de fält som inte ska tas med. Den här sidan hjälper dig att minska antalet fält som måste anges.
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
| Bättre insyn i delade och specificerade rader | Specificerade och uppdelade rader läggs till direkt i listan över utgifter för att öka synligheten och hjälpa dig att enkelt avgöra om det finns några fel. |
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
