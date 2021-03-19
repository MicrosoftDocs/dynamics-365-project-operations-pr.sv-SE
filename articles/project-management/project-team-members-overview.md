---
title: Projektets teammedlemmar
description: I det här ämnet finns information om hur du arbetar med information om medlemmar i projektteam, attribut och schemaläggning.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3526c5e2c968bdaa4d957592aed8d1b21c64b799
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286675"
---
# <a name="project-team-members"></a>Projektets teammedlemmar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Medlemmar i projektteamet är projektdeltagare som utför arbetet i ett projekt. Syftet med rutnätet med teammedlemmar är att tillhandahålla en lista över namngivna resurser som deltar i åtagandet, och allmänna teammedlemmar som är platshållarresurser och bemannas senare.

Från rutnätet med teammedlemmar kan projektledaren och de andra projektdeltagare se vilka som har kopplats till projektet. De kan också visa en sammanfattning av deras bokningar, planerade insatser och enskilda resurstilldelningar. Med rutnätet med teammedlemmar kan projektledarna definiera resurskrav för allmänna teammedlemmar och hantera bokningar av befintliga teammedlemmar.

I följande tabell visas nyckelattribut för en medlem i projektteamet.

| Fältnamn          | Beskrivning                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allokeringsmetod        | Allokeringsmetoden som används för att boka resurser i projektet.                                                                         |
| Faktureringstyp             | Välj om teammedlemmen klassificeras som fakturerbar.                                                                                                                                       |
| Bokningsbar resurs        | Den bokningsbara resursen som har valts för att ersätta den allmänna resursen.                                                                                                                   |
| Borttagningsstatus            | Den borttagningsstatus för teammedlemmen som ska spåras om det finns en borttagningsbegäran skickad till PSS, och huruvida PSS skickar tillbaka svar inom den förväntade tiden. |
| Total arbetsinsats (timmar)     | Summan av teammedlemmarnas insatser i sina tilldelningar.                                                                                                                         |
| Arbetet slutfört (timmar) | En spårning av de insatser som åstadkommits av teammedlemmen i sina tilldelningar.                                                                                           |
| Resterande insats (timmar) | En spårning av de insatser som inte slutförts av teammedlemmen i sina tilldelningar.                                                                                    |
| Slutför                   | Slutdatum för resursteamets medlemskap.                                                                                                                                            |
| Antal fast bokade timmar        | Teammedlemmens fast bokade tid.                                                                                                                                                                |
| Positionens namn            | Namnet som användes för att identifiera den generiska resursen.                                                                                                                                   |
| Resursenhet          | Organisationsenheten för resursen som utför arbetet.                                                                                                                      |
| Projektgodkännare         | Välj om teammedlemmen kan godkänna tid och utgifter.                                                                                                                     |
| Timmar som krävs           | Begärda timmar för teammedlem från teammedlemskrav.                                                                                                                       |
| Roll                     | Rollen som teammedlemmen fyller i det här teamet.                                                                                                                                |
| Beskrivning av position     | Ange en beskrivning av rollen för den här teammedlemmen.                                                                                                                             |
| Antal preliminärt bokade timmar        | Teammedlemmens preliminärt bokade tid.                                                                                                                                                                 |
| Början                    | Startdatum för resursteamets medlemskap.                                                                                                                                          |

Från rutnätet med projektmedlemmar kan du utföra följande åtgärder:

- **Boka**: för organisationer som använder hybridbokningsmetoden gör bokningsåtgärden det möjligt för användare att boka en namngiven resurs baserat på de krav som genererats från den generiska teammedlemmen
- **Generera krav**: den här åtgärden genererar kravet.
- **Ange mönster**: gör det möjligt för projektledarna att justera resurskravens profiler på en detaljerad nivå. Projektledarna kan justera efter projektets specifika behov i de fall då standarddistributionen inte passar.
- **Skicka förfrågan**: för organisationer som använder metoden för central bokning.
- **Redigera**: attribut för team medlem kan redigeras, t.ex. organisationsenhets-, roll- och befattningsnamn.
- **Underhåll bokningar**: när du behöver uppdatera en resursbokning kan du låta projektledaren justera:

    - Början
    - Sluta
    - Total insatsallokering

- **Ny**: förutom att lägga till resurser direkt från schemat kan projektledarna lägga till nya namngivna eller generiska teammedlemmar från rutnätet med teammedlemmar.
- **Ta bort**: genom att välja en eller flera teammedlemmar kan projektledarna ta bort resurser som inte längre ska ingå i projektet. Om du tar bort en teammedlem tas även alla associerade resurstilldelningar bort och alla befintliga bokningar avbryts.


[!INCLUDE[footer-include](../includes/footer-banner.md)]