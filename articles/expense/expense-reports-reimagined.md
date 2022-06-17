---
title: Ny typ av utgiftsrapporter (innehåller video)
description: Den här artikeln innehåller information om den omdesignade och nya upplevelsen för posten i utgiftsrapporten.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c74b4b70722af72bc66dba0662813c29d3d1df04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930294"
---
# <a name="expense-reports-reimagined"></a>Ny typ av utgiftsrapporter

Utgiftsrapportposten har omdesignats för att förenkla processen och minska den tid som krävs för att slutföra en rapport. Här är de viktigaste komponenterna i den nya utgiftsupplevelsen:

- En ny arbetsyta för utgiftshantering som ger dig tillgång till ombudets utgifter.
- En ny kvittomatchning som gör det lättare att visa kvitton på huvudnivån och förenklar processen för att bifoga kvitton till utgiftsrader.
- Ett nytt skrivskyddat rutnät där du kan visa många fler utgiftsrader och andra datakolumner. Nu kan du se alla specificerade och uppdelade rader, tillsammans med deras överordnade utgifter.
- Ett förenklat fönster för att redigera utgifter.
- Nya fel-, varnings- och policymeddelanden som ger korrekt sammanhang och förståelse för problemet och hur du löser det. Vi har tagit bort flera av meddelandena som visades innan användarna kunde slutföra sina uppgifter och åtgärda problemen.
- En ny sida för att ange obligatoriska fält, valfria fält och de fält som inte ska tas med. Den här sidan hjälper dig att minska antalet fält som måste anges.
- En ny utformning och känsla för utgiftsrapporter så att rapporterna inte längre verkar som om de har utformats för redovisningspersoner.

För att aktivera den nya upplevelsen, använd arbetsytan **Funktionshantering** för att aktivera funktionen **Kostnadsrapporter har tänkt om arbetsytan**. När du aktiverar den här funktionen utförs följande åtgärder:

- Den befintliga arbetsytan för utgifter ersätts med den nya arbetsytan.
- Ett nytt menyobjekt för synlighet för utgiftsfält läggs till.
- Inga befintliga menyalternativ för utgiftsrapporter (befintlig sida) eller utgiftsrapportfält tas bort.
- Arbetsflöden och eventuella godkännanden går fortfarande till sidan befintliga utgiftsrapporter.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Nya funktioner

| Ny funktion | Beskrivning |
|---|----|
| Synlighet hos utgiftsfält | På en ny inställningssida kan du ange vilka fält som ska inaktiveras för en organisation. Du kan också ange vilka fält som ska vara obligatoriska och vilka fält som rekommenderas. |
| Obligatoriska fält | Med ny enkel konfiguration kan du göra några fält obligatoriska utan att behöva använda policyramverket. |
| Valfria fält | En andra sida för valfria fält läggs till. På det här sättet känner inte de anställda att de måste ange fälten, men fälten är fortfarande lättillgängliga. |
| Lägg till icke bifogade kvitton | Möjligheten att lägga till icke bifogade kvitton i utgiftsrapporten är mer synlig från arbetsytan och i utgiftsrapporten. |
| Förbättrade meddelandefunktioner | Det finns bättre insyn i utgiftsrader som innehåller varningar eller fel. |
| Färre meddelanden i meddelandefältet| Antalet meddelanden i informationsloggen minskades och en insats gjordes för att förhindra att dubbla meddelanden visas i många fall. |
| Grupperade vanliga åtgärder | Gränssnittet rensades med tillägget av en ny åtgärdsknapp för de flesta vanliga åtgärder på radnivå och en ellipsknapp (...) för rubrik och andra mindre frekventa åtgärder. |
| Ny arbetsyta för att öka synligheten | En ny arbetsyta förenar funktioner och länkar som gör att användarna kan flytta till olika områden. |
| Lägg till befintliga utgifter och kvitton under utgiftsskapande | När du skapar utgiftsrapporter kan du lägga till alla utgifter eller välja ej kopplade utgifter. Ej kopplade utgifter är utgifter som har importerats från företagets kreditkortsflöden eller utgifter som har skapats manuellt av användaren men inte har kopplats till en utgiftsrapport.|
| Kalkylator av valutakurs | En kalkylator av valutakurs läggs till, som gör att du kan beräkna valutakursen för transaktioner i flera valutor. |
| Spara och lägg till nya utgiftsrader | Knapparna **Spara** och **Ny** är tillgängliga när nya utgifter läggs till för att göra det enklare för dig att snabbt lägga till utgiftsrader. |
| Bättre insyn i delade och specificerade rader | Specificerade och uppdelade rader läggs till direkt i listan över utgifter för att öka synligheten och hjälpa dig att enkelt avgöra om det finns några fel. |
| Visa underkategoriinformation på objekterade rader | I specificerade rader för en överordnad kostnad visas underkategorietiketterna i utgiftsrapporten. Med hjälp av specifikation kan du få en översikt över den detaljerade informationen.|
|Specificera återkommande utgifter snabbt | Den nya arbetsytan för utgifter gör det möjligt att enkelt specificera återkommande utgifter genom att lägga till underkategori, startdatum och kvantitet. Kvantiteten avser antalet gånger debiteringen upprepas under en kontinuerlig period. |
| Visa kvitton under specifikation | Kvitton kan visas under specifikation. |
| Val av förskott | Välj en eller flera förskott som ska uppfylla en enda utgiftstransaktion. |
| Saldo av förskott | Granska förskottssaldot i realtid när du skapar en utgiftspost mot godkända och betalda förskott. |

Den första versionen är inriktad på scenarier för utgiftsposter. Scenarier med granskning eller godkännande av utgiftsrapporter fortsätter att använda den befintliga sidan för utgiftsposter.


Följande funktioner stöds inte på arbetsytan för utgiftsrapporter, men är planerade för framtida versioner: 

- Integrering av reserekvisition
- Utgiftspost per dag
- Stöd för interimistiska godkännanden
- Möjlighet att visa arbetsflödeshistorik


[!INCLUDE[footer-include](../includes/footer-banner.md)]
