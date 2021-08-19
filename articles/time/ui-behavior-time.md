---
title: UI-funktioner för tidspost
description: I det här ämnet finns information om beteendet hos gränssnittet för tidspost.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ef99f220e9ff207a7620a900aa0630e2803f4f7261eccfbf73ed79717648bf92
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999473"
---
# <a name="time-entry-ui-behavior"></a>UI-funktioner för tidspost

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


Rutnätet **Veckovis tidspost** är en anpassad kontroll som har två huvudområden: **Dimensioner** och **Varaktighet**.

## <a name="keyboard-shortcuts"></a>Kortkommandon
| Åtgärd        | Genväg                  |
|------------   |------------------------   |
| Skapa           | Alt + Shift + n           |
| Kopiera rad      | Alt + Shift + c           |
| Redigera post    | Alt + Shift + e           |
| Redigera rad      | Alt + Shift + Ctrl + e    |
| Öppen post    | Alt + Shift + o           |
| Skicka in        | Alt + Shift + s           |
| Återkalla        | Alt + Shift + r           |
| Delete        | Alt + Shift + d           |
| Kopiera vecka     | Alt + Shift + w           |

## <a name="dimensions"></a>Dimensioner
Avsnittet **Dimensioner** visar alla dimensioner som det går att ange tid för. Följande medföljande dimensioner stöds:

  - Project
  - Projektuppgift
  - Roll
  - Type
  - Poststatus

Avsnittet **Dimensioner** tillåter inte infogad redigering. Det här avsnittet är en vy som gör att anpassade fält kan läggas till i rutnätet för veckovisa tidsposter.

## <a name="duration"></a>Giltighetstid
I området varaktighet visas veckodagarna som kolumnrubriker. I det här avsnittet kan du redigera på en rad. När en tidspostrad har skapats med lämpliga dimensioner kan användare snabbt ange hur mycket tid som har lagts ned på de dimensionerna.

## <a name="create-a-new-time-entry"></a>Skapa en ny tidspost

1. I rutnätet för tidsposter väljer du **Ny**. 
2. I dialogrutan **Snabbskapa tidspost** väljer du datum för tidsposten.
3. Ange data för dimensionerna **Projekt**, **Projektuppgift**, **Roll** och **Varaktighet**. Informationen ska läggas till i minuter, timmar eller dagar genom att skriva **h**, **m** eller **d**, tillsammans med siffran. 
4. Ange en beskrivning av posten och eventuella kommentarer som kan delas ut externt gällande en tidspost. 

När du sparar posten visas angivna värden i avsnittet **Dimensioner**. Informationen som anges i fältet **Varaktighet** visas det datum som tidsposten skapades för.

Uppslagsfält säkerhetskopieras med systemvyer. När en användare har angett ett projekt anges fältet **projektuppgift** till vyn **kopiera** som standard. Om du vill skapa tidsposter för uppgifter som inte är tilldelade till användaren klickar du på **ändra vy** i dialogrutan uppslag och markerar vyn **Alla aktiva projektuppgifter**.

## <a name="edit-a-time-entry"></a>Redigera en tidspost 
Information från vissa fält på sidan för tidspost, t.ex. **Beskrivning** och **Externa kommentarer**, visas inte i rutnätet för veckovis tidspost. En liten triangulär indikator visas istället i cellerna **Varaktighet** med dessa ytterligare detaljer. 

1. Om du vill redigera en tidspost väljer du cellen du vill uppdatera i tidsposten.
2. Välj **Redigera information** om du vill uppdatera data i fönstret **Tidspost MainForm**. 

## <a name="copy-a-time-entry-row"></a>Kopiera en tidspostrad
När raden har skapats kan du välja **Kopiera rad** för att kopiera hela raden till en ny rad. När en rad kopieras på det här sättet kopieras även dimensioner och varaktighet. Du kan också välja **Redigera rad** för att uppdatera dimensionsvärden och varaktigheter i området **Varaktighet**.

## <a name="open-a-time-entry-behavior"></a>Öppna en tidsposts beteende
För att stödja optimal och snabbinmatning i de mest framträdande fälten visar rutnätet för veckovis tidspost en delmängd av valda dimensioner och tidslängder. Om du vill visa all information om en enskild tidspost väljer du **Redigera post** och **Öppna**.

## <a name="submit-a-time-entry"></a>Skicka tidspost
Du kan skicka en enstaka post eller en grupp med tidsposter genom att markera ett block med celler eller en hel tidspostrad och sedan välja **Skicka**. Skickade tidsposter visas som transaktioner som väntar på godkännande på godkännarens sida **godkännande**. När du har skickat tidsposter kan du inte redigera dem.

## <a name="recall-a-time-entry"></a>Återkalla tidspost
Du kan återkalla tidsposter som du har skickat in. Du kan återkalla en enskild tidspost, ett block med tidsposter eller en hel rad med tidsposter. Det går att redigera återkallade tidsposter.

## <a name="time-entry-status"></a>Tidspostens status

- **Utkast**: Nya tidsposter tilldelas automatiskt statusen **Utkast**. Det går bara att ta bort tidsposter som har statusen **utkast**.
- **Skickad**: När en tidspost skickas uppdateras statusen till **Skickad**. 
- **Godkänd**: När en skickad tidspost godkänns uppdateras statusen till **Godkänd**. 
- **Returnerad**: Om en tidspost avvisas uppdateras statusen till **Returnerad** och posten blir tillgänglig för korrigering och omsändning. 

## <a name="view-rejection-comments"></a>Visa kommentarer till avvisning
När en tidspost avvisas av en godkännare kan godkännaren lägga till kommentarer som gör det lättare för resursen att förstå orsaken till avslaget. Om du vill visa avslagskommentarerna för en tidspost markerar du **öppna post**. Kommentarerna för avvisningen visas på tidslinjen. Användaren kan svara på de för avslagskommentarerna innan de skickar posten på nytt.

## <a name="copy-week"></a>Kopiera vecka
När några tidsposter har skapats kan användarna skapa flera samtidigt.

1. I formuläret **Tidsposter** väljer du **Kopiera vecka** för att skapa ytterligare tidsposter. 
2. I dialogrutan **Kopiera** i avsnittet **Från period** använder du fälten **Startdatum** och **Slutdatum** för att definiera datumintervallet att kopiera tidsposter från. 
3. I avsnittet **Till period** i fältet **Startdatum**, ange datumet att skapa tidsposter för. 
4. Välj **kopiera**. För det angivna datumet i **Till period** skapas en kopia av tidsposterna för den motsvarande veckodagen i **Från period**. Exempelvis kopieras tidsposten för måndagen från den senaste veckan till måndagen i veckan som anges som **Till period**.

## <a name="import"></a>Import
Samma grundläggande process används för att importera från bokningar, tilldelningar och utbyten. Du kan ange datumintervallet som bokningar importeras från och sedan uttryckligen välja de bokningar som ska kopieras till utkast av tidsposter. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
