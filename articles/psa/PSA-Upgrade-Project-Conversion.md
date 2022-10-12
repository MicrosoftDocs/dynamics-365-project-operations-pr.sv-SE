---
title: Funktionsändringar för Project Service Automation till Project Operations
description: Denna artikel innehåller en översikt över funktionsändringar för Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621271"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Funktionsändringar för Project Service Automation till Project Operations

När ett projekt har uppgraderats från Microsoft Dynamics 365 Project Service Automation 3.X till Dynamics 365 Project Operations Lite går det inte att redigera projektuppgifter i uppgiftsrutnätets uppdelade arbetsstruktur (WBS). Kunder kommer att kunna granska WBS i spårningsrutnätet där nya fält har lagts till för att ge alla detaljer som är relaterade till uppgiften. För projekt där redigeringar av WBS krävs kan du selektivt konvertera kvalificerade projekt till det nya Project for the Web schemaläggningsupplevelsen.

## <a name="project-conversion-process"></a>Projekt omvandlingsprocess

Konvertera ett projekt genom att följa stegen nedan.

1. Öppna projektets huvudsida och välj **Konvertera** i åtgärdsfönstret.
1. I meddelanderuta för bekräftelse, välj **OK** för att starta projektkonverteringen. Följande åtgärder och förekommer:

    1. Ett meddelandefält som visas på projektets huvudsida visas: "Projektschemat håller på att konverteras. Du kan inte göra ändringar i projektet förrän konverteringen är slutförd."
    1. Du omdirigeras till projektlistan.

    När projektkonverteringen är slutförd sker följande åtgärder:

    1. Den tilldelade projektledaren får ett meddelande till höger om programmet.
    1. Det meddelandefält där det står att konvertering pågår tas bort.
    1. På fliken **Schema** visas den nya schemaläggningsupplevelsen med Project for the Web. Alla användare med rätt licenser och säkerhetsroller kan redigera WBS.
    1. Fältet **Schemaläggningsmotor** uppdateras till **Project for the Web**.
    1. Knappen **Konvertera** tas bort från åtgärdsfönstret.

> [!IMPORTANT]
> Masskonvertering av projekt är inte tillåtet. Alla försök att uppdatera en stor volym projekt samtidigt kommer att fortsätta. Den här begränsningen bidrar till att alla kunder får hög prestanda.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuella uppgifter jämfört med automatiska uppgifter

När en miljö uppgraderas från Project Service Automation till Project Operations, räknas alla uppgifter i WBS automatiskt. Konceptet med manuellt schemalagda uppgifter är inte tillgängligt i Project for the Web. Du kan emellertid ange önskat schemaläggningsbeteende för dina projekt genom att använda inställningen för [schemaläggningsläge](/project-management/scheduling-modes.md) när du skapar nya projekt.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Begränsade åtgärder för projekt före konvertering

I det här avsnittet beskrivs de funktionsskillnader som kan förväntas när projekt inte har konverterats.

### <a name="copy-project"></a>Kopiera projekt

Åtgärden **Kopia** stöds endast för konverterade projekt. Uppgraderade projekt kan inte kopieras före konvertering.

### <a name="move-project"></a>Flytta projekt

Om du ändrar startdatum för ett projekt flyttas inte uppgifternas början såvida inte projektet har konverterats.

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Vilka är skillnaderna mellan konverterade projekt och nya projekt som skapas efter uppgraderingen?

För projekt som konverteras efter det att miljön har uppgraderats anges en flagga som instruerar schemat att endast användas i projektkalendern. Detta överensstämmer med funktionen för Project Service Automation. Däremot anges inte flagga för nya projekt som skapas efter uppgraderingen. Därför gäller arbetstimmarna för resurserna i schemat när de tilldelas en uppgift.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Vad gör jag om mitt projekt inte kan konverteras?

Om ditt projekt inte kan konverteras är det första steget att gå igenom felloggarna för att identifiera eventuella vanliga problem som är relaterade till dina WBS. Om loggarna inte anger något specifikt fel som du kan åtgärda kontaktar du kundsupport så att ärendet kan ses över ytterligare.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hur hanteras företagets stängningar i Project for the Web?

I Project for the Web gäller inte företagets stängningar som definieras på organisationsnivå. Däremot gäller andra typer av ledigt dagar som definieras i en viss mall för arbetstimmar.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Vilka begränsningar finns för funktionen Project for the Web?

Se [Skapa en uppdelad arbetsstruktur: Projektbegräsningar](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kan jag förvänta mig ändringar av kostnaderna och försäljningen?

I sällsynta fall där resurstilldelningens konturer beräknas om, eller där de faller på en annan datumgräns än källprojektet, kan du se skillnader i försäljnings- och kostnadsberäkningar. Som en del av uppgraderingsprocessen förväntas kunderna testa en representativ exempeluppsättning projekt så att de förstår eventuella schemaändringar.
