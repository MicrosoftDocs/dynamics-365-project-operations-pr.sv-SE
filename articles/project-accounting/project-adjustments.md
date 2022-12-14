---
title: Projektjusteringar
description: Den här artikeln innehåller information om projektledning.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788310"
---
# <a name="project-adjustments"></a>Projektjusteringar

_**Gäller för:** Project Operations för lagerbaserade/produktionsbaserade scenarier_

## <a name="adjustments-overview"></a>Översikt över justeringar

Du kan konfigurera Microsoft Dynamics 365 Project Operations så att användarna kan ändra de upplagda transaktionerna. Du kan justera projekttransaktioner individuellt eller så kan du välja flera transaktioner åt gången i en lista över alla projekttransaktioner. Projektjusteringar används till exempel för att massuppdatera den fakturerbara statusen, räkna om kostnaden efter en konfigurationsändring eller uppdatera finansieringskällor.

Användarna kan använda projektanpassningsfunktionen på flera sätt:

- Genom att använda sidan **Justera transaktioner** som du kommer åt från **Projektledning och redovisning** \> **Inställningar**.
- Genom att använda knappen **Justering** på sidan **Bokförda projekttransaktioner** som du kan komma åt från **Projektledning och redovisning** \> **Transaktioner**.
- Genom att använda knappen **Justering** på sidan **Bokförda projekttransaktioner** i kontexten för ett projekt. Du kommer åt denna sida från **Projektledning och redovisning** \> **Alla projekt**.

För att tillåta justeringar måste du aktivera en eller flera transaktionsstatusar från **Projektledning och redovisning** \> **Parametrar för projektledning och redovisning** på fliken **Allmänt** under avsnittet **Tillåt justering av transaktionsstatus**. Exempel på transaktionsstatus är upplagda transaktioner, fakturerade transaktioner eller eliminerade transaktioner. Alla transaktionsstatusar som anges som **Nej** har transaktioner i den statusen som inte visas i justeringsprocessen och som kan väljas för justering.

Ett konfigurationsalternativ med namnet **Skapa alltid justeringstransaktion** är för närvarande tillgängligt i Projekthanterings- och redovisningsparametrar. Du kan inaktivera det här alternativet om du vill uppdatera den ursprungliga transaktionen i stället för att skapa nya transaktioner under justering i en deluppsättning av scenarier. Parametern ska vara inaktuell den 1 mars 2023. Efter 1 mars 2023 fungerar systemet alltid som om alternativet är aktiverat.

## <a name="adjustments-process-flow"></a>Justeringsprocessflöde

I följande steg visas det typiska flödet för bearbetningsanpassningar.

1. Öppna sidan för **Projektanpassningar**.
2. Markera **Välj** om du vill söka efter transaktioner som uppfyller de förväntade villkoren för justering.
3. Välj alla transaktioner eller en delmängd av transaktionerna som ska justeras i listan.
4. Välj **Justera** och ändra attributen på raden. Alternativt, om värdena angavs manuellt under transaktionsposten, kan du välja att ange standardsystemvärden.
5. Listan med transaktioner returneras och en bock visas i kolumnen **Väntande justering** för att ange var ändringar har gjorts. Alla ändringar som har väntande ändringar visas i den nedre delen av sidan. Där kan du göra ytterligare detaljerade ändringar utöver vad som visades på föregående sida.
6. Välj **Bokför** för att bokföra justeringstransaktioner.

Beroende på konfigurationen skapas vanligtvis nya transaktioner för justeringen.

- Fältet **Fakturastatus** för den ursprungliga transaktionen har angetts till **Justerad**.
- En återföringstransaktion skapas för att återföra den ursprungliga transaktionen och **Status** anges till **Justerat**.
- En ny transaktionen skapas med de ändringar som gjordes under justeringsprocessen.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Välja flera upplagda projekttransaktioner samtidigt för justering och kreditfakturor

En ny funktion som introducerades i 10.0.30-versionen gör det möjligt att välja flera transaktioner för justering samtidigt från sidan **Bokförda projekttransaktioner**.

Innan du kan använda den här funktionen måste du aktivera den i ditt system. Administratörer kan använda arbetsytan **Funktionshantering** för att kontrollera funktionens status och aktivera den vid behov. På arbetsytan **Funktionshantering** söker du efter **Välja flera upplagda projekttransaktioner samtidigt för justering och kreditfakturor** och välj sedan **Aktivera nu**.

Denna funktion aktiverar följande huvudfunktioner:

- Du kommer åt den från sidan med den upplagda transaktionen i ett projekt med den befintliga knappen **Justering**.
- Den aktiverar en flerradig urvalskontroll på sidan **Bokförda projekttransaktioner** . Du kan använda filter på listsidan och markera posterna innan du börjar justera.
- Knappen **Justering** inaktiveras om det inte går att justera en enskild transaktion, eller om du väljer en kombination av kreditfakturor och journaler tillsammans i stället för enskilt.
- På grund av tillägget av flerradsvalskontrollen är länken **Bekräftad kostnad** i menyfliksområdet är inte längre inaktiverat om flera rader är markerade.
- Följande varningsmeddelande läggs till: "Du har markerat fler än (markerade nummer) poster som ska justeras. Det kan ta en stund att fortsätta med den här åtgärden. Är du säker på att du vill fortsätta med denna åtgärd?

Den här funktionen tar även bort steg 2 från det processflöde som beskrivs ovan i den här artikeln. Därför tas alla transaktioner som valts innan sidan **Justera transaktioner** öppnades med i listan med transaktioner för justering. Du behöver inte använda knappen **Välj** för att söka efter dem.

> [!NOTE] 
> Även om funktionen är inaktiverad kan du välja flera poster som ska justeras. Men endast en post *förblir markerad* och dialogrutan **Välj transaktioner** visas direkt efter att du har valt att öppna ändringar.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Justeringstransaktionsstatus som kan aktiveras eller inaktiveras för anpassningar

Följande statusar kan aktiveras eller inaktiveras på fliken **Allmänt** på sidan **Parametrar för projektledning och redovisning** :

- Bokfört
- Fakturaförslag
- Fakturerad
- Beräknad
- Borttagen
- Ingående saldo (timme)

## <a name="adjustment-parameters"></a>Justeringsparametrar

Dessa parametrar visas på sidan **Parametrar för projektledning och redovisning** på fliken **Allmänt** under gruppen **Justering** och kommer att ändra beteendet för hur justeringar bearbetas. 

| Parameternamn | Description |
|----------------|-------------
| Skapa alltid justeringstransaktion | Om parametern är aktiverad skapas alltid en ny, justerad transaktioner och en ny justerad transaktioner med ekonomiska effekter eller rapporteringspåverkan. Om parametern är inaktiverad uppdateras den ursprungliga transaktionen i stället för att en ny och ny transaktionen skapas för ett scenario, till exempel en uppdatering av transaktionstexten. |
| Uppdatera fält automatiskt | Om parametern är aktiverad beräknas kostnads- och försäljningspriset om i systemet. |
| Använda justeringsdatum som nytt projekt | Den här parametern används för att flytta transaktioner till en räkenskapsperiod innan systemet har stöd för den här funktionen. Vi rekommenderar inte att du använder den eftersom den ändrar affärsdatumet för transaktionen och kommer att tas bort i en framtida version. |
| Tillåt stängda aktiviteter | Vanligtvis kan transaktioner inte skapas för stängda aktiviteter. Om parametern är aktiverad åsidosätts detta beteende. Därför kan ändringar skapas för stängda aktiviteter. |
