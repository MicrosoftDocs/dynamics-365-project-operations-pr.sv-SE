---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 27, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146685"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 27, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 27. Den här versionen har versionsnummer V3.10.45.98 och är allmänt tillgänglig via en självuppdatering i januari 2021.

## <a name="update-release-27"></a>Uppdatering version 27

### <a name="bug-fixes"></a>Felkorrigeringar

**Allmänt**

Följande problem har åtgärdats:

- Loggar som genereras av plugin-program i Project Service Automation har inte ställts in på automatisk radering.
- Automatisk uppgradering misslyckas eftersom Project Service Automation-lösningen innehåller ett äldre "null NavBarArea"- och rubrikelement.

**Tid och utgift**

Följande problem har åtgärdats:

- Rutnätet **Tidsinmatning** visar felaktiga data för datumbeteendet **Tidszonoberoende**.
- Rutnätet **Tidsinmatning** visar felaktig tid för datumbeteendet **Tidszonoberoende**.
- Aktivitetsuppslag är inte begränsat till det valda projektet på sidan **Redigera tidsinmatning**.
- Tidsgodkännande för icke-projekttidsposter har blockerats eftersom systemet söker efter en projektgodkännare.
- Korrekta poster på Faktiska värden visar ett felaktigt felmeddelande.
- När en aktivitet innehåller ett null-värde för faktisk kostnad och projektsumman uppdateras, uppstår följande fel: "Angiven nyckel finns inte i registret".
- I specifika instanser visar inte **Gruppera efter**-filter på fliken **Projektuppskattning** inga utgiftsuppskattningar.
- Intervall för **Sommartid** är inte korrekt för tidsposter.

**Projektledning**

Följande problem har åtgärdats:

- Lagrade förbättringar, som förbättrar prestandan relaterad till inläsning av sidan **Projekt**.
- Föråldrad affärsregel som hindrar projektaktiviteter från att slutföras.
- Microsoft Project-tilläggskonturer respekterar inte tilläggets kalender, vilket resulterar i felaktiga resurskrav.
- När du skapar projekt från mallar anges tilldelningsdatum felaktigt, och förhindrar möjligheten att generera resurskrav.
- Användaren kan inte komma åt alternativen **Kategori**, **Beskrivning** eller **Status** via tangentbordet.
- Faktiska försäljningsvärden för projektet är inte inklusive avgifter och försäljningsvärden för material.
- Sammansättning av faktisk försäljning och faktiska kostnader blir fel när olika växelkurser används.
- Beskrivningen i **Standardmall för arbetstimmar** är missvisande.
- Indrag av en aktivitet tar inte bort **Kategori** i användargränssnittet förrän den uppdateras.
- Validering som saknas för att se till att ett projekt flyttas bortom sitt slutdatum är inte tillåtet.

**Sales**

Följande problem har åtgärdats:

- Ett null-referensundantag genereras på en projektoffertrad eftersom **Import från projektuppskattning** syns när ett projekt inte har valts.
- Följande fel, "Object reference not set to an instance of an object" (Objektreferensen är inte inställd på en instans av ett objekt) inträffar när en offert stängs som **Vunnen**.
- Justeringsstatusen anges inte i samband med en faktisk återställning när ett projekt kopplas bort från en kontraktrad.
- När Dynamics 365 Field Service och Project Service Automation båda är installerade visas inte alternativen **Lås prissättning** och **Använd aktuell prissättning** samtidigt på sidan **Faktura**.
- För det japanska språket finns det inkonsekvent översättning med andra kalenderbaserade sidor.
- **Aktivera** och **Inaktivera** har tagits bort från **Prislisteassociation**-entiteter i Project Service Automation.
