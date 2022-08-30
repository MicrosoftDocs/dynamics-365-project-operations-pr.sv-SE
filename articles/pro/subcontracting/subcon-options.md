---
title: Alternativ för underkontraktering av projektteammedlemmar
description: I den här artikeln beskrivs alternativen för underkontraktering för projektteammedlemmar i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261629"
---
# <a name="subcontracting-options-for-project-team-members"></a>Alternativ för underkontraktering av projektteammedlemmar

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I Microsoft Dynamics 365 Project Operations kan du utvärdera de alternativ för underkontraktering som är tillgängliga för en eller flera projektteammedlemmar. Med de tillgängliga alternativen för underkontraktering kan du:

- Skapa en ny underleverantör och/eller skapa nya rader för en befintlig underleverantör för de valda projektteammedlemmarna. 
- Reservera mot en befintlig underleverantör och underleverantörsrad. 

Du kan välja bland de tillgängliga underleverantörsalternativen för generiska projektteammedlemmar, eller välja bland projektteammedlemmar som har bemannats med en namngiven resurs som är kontraktarbetare. 

Det finns inga tillgängliga underleverantörsalternativ för följande:

- Projektteammedlemmar som har bemannats med en anställd. 
- Projektteammedlemmar som redan är associerade med en underleverantör och underleverantörsrad. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Underkontraktering av en obemannad projektteammedlem

Granska och välj bland de tillgängliga underleverantörsalternativen för en generisk eller obemannad projektteammedlem genom att följa stegen nedan:

1. Välj en eller flera poster för projektteammedlem där resursen är en allmän resurs.
2. Kontrollera att inga av de markerade projektteammedlemsposterna redan har underkontrakterats. 
3. Välj **Underleverantörsalternativ** i underrutnätet för projektteammedlemmar. Dialogrutan **Underleverantörsalternativ** öppnas. 
4. Om du bara valde en post för projektteammedlem i steg 1 blir följande alternativ tillgängliga:
    - Skapa nya underleverantörsrader. 
    - Reservera mot en befintlig underleverantör om du valde flera poster för projektteammedlemmar i steg 1, då är det enda tillgängliga alternativet att skapa en ny underleverantörsrad.
5. Möjligheten att reservera mot en befintlig underleverantörsrad gör att du kan välja en underleverantör och underleverantörsrad som du vill reservera mot. När du väljer en underleverantörsrad för att reservera kapacitet bör du se till att den valda underleverantörsraden har rätt tid och att rollen som krävs i projektteamet matchar rollen som köptes på underleverantörsraden.
6. När du väljer att skapa nya underleverantörsrader för projektteamets medlemmar kan du välja vilken underleverantör du vill skapa raderna i. Den underleverantör du väljer för att skapa nya rader i ska ha statusen **Utkast**. Med det här alternativet för att skapa nya underleverantörsrader för de valda projektteammedlemmarna skapas en underleverantörsrad för tid för varje projektteammedlem. Rollen, timmarna och datumen kopieras från projektteammedlemmen till varje underleverantörsrad som skapas. 
7. När en generisk teammedlem associeras till en underleverantör och underleverantörsrad uppdateras fältet **Arbetartyp** på raden för generiska teammedlemmar till **Kontraktarbetare** och värdet **Underleverantörs giltighet** till **Giltig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Underkontraktering av en bemannad projektteammedlem

Precis som generiska eller teammedlemmar som inte är anställda kan du också visa alternativ för underleverantörer för en medarbetare i projektteamet så länge den anställde är kontraktarbetare. Granska och välj bland de tillgängliga underleverantörsalternativen för en anställd eller namngiven projektteammedlem genom att följa stegen nedan:

1. Välj en eller flera poster för projektteammedlem där resursen är en namngiven kontraktarbetare.
2. Kontrollera att inga av de markerade projektteammedlemsposterna redan har underkontrakterats. 
3. Välj **Underleverantörsalternativ** i underrutnätet för projektteammedlemmar. Dialogrutan **Underleverantörsalternativ** öppnas. 
4. Om du bara valde en post för projektteammedlem i steg 1 blir följande alternativ tillgängliga:
      - Skapa nya underleverantörsrader.
      - Reservera mot en befintlig underleverantör
  Om du valde flera poster för projektteammedlemmar i steg 1, då är det enda tillgängliga alternativet att skapa en ny underleverantörsrad.
5. Möjligheten att reservera mot en befintlig underleverantörsrad gör att du kan välja en underleverantör och underleverantörsrad som du vill reservera mot. När du väljer en underleverantörsrad för att reservera kapacitet bör du se till följande:
      - Den markerade underleverantörsraden är för tid. 
      - Rollen som krävs för projektteammedlemmen matchar rollen som köptes på underleverantörsraden. 
      - Den leverantör som kontraktarbetaren är associerad med är samma som leverantören i underleverantörskontraktet.
6. När du väljer att skapa nya underleverantörsrader för projektteamets medlemmar kan du välja vilken underleverantör du vill skapa raderna i. Med det här alternativet bör du se till att den leverantör som kontraktarbetaren tillhör är samma som leverantören i underleverantörskontraktet. 
7. Den underleverantör du väljer för att skapa nya rader i ska ha statusen **Utkast**. Med det här alternativet för att skapa nya underleverantörsrader för de valda projektteammedlemmarna skapas en underleverantörsrad för tid för varje projektteammedlem. Rollen, timmarna och datumen kopieras från projektteammedlemmen till varje underleverantörsrad som skapas.  
8. När en namngiven teammedlem associeras till en underleverantör och underleverantörsrad uppdateras fältet **Arbetartyp** på raden för namngivna teammedlemmar till **Kontraktarbetare** och värdet **Underleverantörs giltighet** till **Giltig**.

## <a name="re-costing-subcontractor-assignments"></a>Omkostnadstilldelning för underleverantörer

När en projektteammedlem (generisk eller namngiven) är länkad till underleverantörsrader med dialogen **Underleverantörsalternativ** omkostnadsförs tilldelningar till uppgifter som teammedlemmen har baserat på inköpsprislistan som bifogas underleverantörskontraktet. Under fliken **Uppskattningar** på sidan **Projektdetaljer** väljer du knappen **Uppdatera priser** för att se uppdaterad prissättning och/eller kostnadsföring till följd av beslutet att underkontraktera.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
