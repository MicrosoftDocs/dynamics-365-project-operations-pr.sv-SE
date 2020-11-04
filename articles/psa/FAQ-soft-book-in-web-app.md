---
title: Hur gör jag en ”preliminär bokning” av resurser i programversion 2.x?
description: Den här artikeln beskriver hur du kan preliminärboka teammedlemmar med Project Service.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 9e5d1c91f8ea98117583996552c2f2834be9c537
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085563"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Hur preliminärbokar jag resurser i webbappen (appen Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan preliminärt schemalägga eller boka en resurs till ett projektteam i syfte att visa att du planerar att tilldela resursen till ett projekt. Preliminärbokningar förbrukar ingen tillgängliga kapacitet för en resurs. Preliminärbokade teammedlemmar kan inte tilldelas projektaktiviteter. Endast resurser med statusen Fast bokning och bekräftelsetypen Bekräftad kan tilldelas uppgifter (förutsatt att de har tillräckligt med fasta bokningstimmar för att täcka tilldelningsinsatsen).

Preliminärbokade teammedlemmar för projektet visas i rutnätet Teammedlem tillsammans med sina preliminärbokade timmar som visas i kolumnen Preliminärbokning. De visas också på schemaläggningstavlan. De anger återigen ingen kapacitetsförbrukning, detta eftersom preliminärbokningar inte förbrukar någon kapacitet för en resurs.

Det finns tre sätt att preliminärboka en teammedlem för ett projekt med hjälp av Project Service-version 2.x. Du kan preliminärboka via schemaläggningstavlan, använda funktionen Behåll bokningar eller genom att skapa en generisk resurs. Dessa metoder beskrivs nedan.

## <a name="soft-book-with-the-schedule-board"></a>Preliminärboka med schemaläggningstavlan

Gör följande för att preliminärboka via schemaläggningstavlan: 
1. Öppna schemaläggningstavlan.
2. Använd projektfliken på den nedre panelen för bokningskrav på schemaläggningstavlan.
3. Hitta det projekt som du vill preliminärboka en resurs på. Om du har många olika projekt, klicka då på kolumnrubriken för projekt och använd sedan filtret för att hitta projektet.
4. Klicka på projektet och dra och släpp det sedan på resursens tidsrutnät.
5. Då öppnas panelen Skapa resursbokning till höger. Justera start-och slutdatum, välj bokningsstatusen "Preliminär" och ange arbetstimmar. 
6. Klicka på Boka.
7. Tillbaka i projektet anges resursen nu som en teammedlem med preliminärbokade timmar i kolumnen Preliminärbokat.

Tänk på att du inte kan tilldela dem till uppgifter på den uppdelade arbetsstrukturen (WBS), detta eftersom resurser måste ha fastbokats för teamet för att tilldelas.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Preliminärboka via funktionen Behåll bokningar

Gör följande för att preliminärboka via Behåll bokningar:
1. Klicka på Nytt i rutnätet för teammedlem.
2. Markera den bokningsbara resursrollen från/till.
3. Välj en fördelningsmetod annan än Ingen:
- Full kapacitet
- Procentandelskapacitet
- Efter timmar - fördela jämnt
- Efter timmar - tidigareläggning
4. Klicka på Spara. Resursen visas i teamets rutnät och deras arbetstider anges som Fast.
5. Behåll resursens bokningar genom att klicka på Behåll bokningar.
6. Expandera resursen om du vill visa bokningar när schemaläggningstavlan öppnas. Bokningen anges då som Fast.
7. Högerklicka på bokningen och - under Ändra Status - markera Preliminärboka och sedan Preliminär. Bokningsstatusen är nu Preliminär.
8. När du stänger schemaläggningstavlan ser du att timmarna för resursen har ändrats från Fast till Preliminär i rutnätet för teammedlem.
Notera att om du fastbokar en resurs till teamet och sedan tilldelar dem uppgifter i WBS kommer detta, när du använder Behåll bokningar för att ändra statusen från Fast till Preliminär, att avlägsna tilldelningarna från aktiviteterna för den resursen, detta eftersom endast fastbokade resurser kan tilldelas till uppgifter.

## <a name="soft-book-by-creating-a-generic-resource"></a>Preliminärboka genom att skapa en generisk resurs

Du kan skapa en preliminärbokning genom att skapa en generisk resursteammedlem, komplettera med schemaläggningstavlan eller resursbegäran och ändra typen i samband med bokning.
I detta syfte, gör på följande sätt:

1. Tilldela roller till de uppgifter som du vill skapa generiske teammedlemmar för i projektets WBS.
2. Klicka på Generera projektteam.
3. I rutnätet för projektteammedlem väljer du den generiska resursen och klickar sedan på Boka.
4. Välj den resurs som du vill boka i schemaläggningstavlan.
5. Ändra bokningsstatusen till "Preliminär" i panelen Skapa resursbokning på schemaläggningstavlan.
6. Klicka på Boka eller Boka och avsluta.

När du har stängt schemaläggningstavlan visas den markerade resursen som tillagd i teamet med såväl preliminärbokade timmar som tilldelade timmar. Du kan också se att den generiska resursen förblir i teamet som en indikator på att uppgifterna tilldelas en preliminärbokad teammedlem.

När du är redo att ändra en preliminärbokad teammedlemsresurs till en fastbokad teammedlem så att du kan tilldela dem till aktiviteter kan du göra följande:

1. Markera resursen och klicka på Behåll bokningar.
2. Expandera resursen om du vill visa bokningar när schemaläggningstavlan öppnas. Bokningen markeras som Preliminär.
3. Högerklicka på bokningen och - under Ändra Status - markera Fastboka och sedan Fast. Bokningsstatusen är nu Fast.
4. När du stänger schemaläggningstavlan ser du att timmarna för resursen har ändrats från Preliminär till Fast i rutnätet för teammedlem. Du kan nu tilldela resursen till aktiviteter (förutsatt att det finns samstämmighet mellan fastbokade timmar och aktivitetens insatstimmar för tilldelningen). Observera att om du har följt stegen för generisk resursexpediering i objekt #3 ovan, så kommer den generiske teammedlemmen att tas bort från teamet när du ändrar statusen för den preliminärbokade bokningsbara resursen till Fast.
