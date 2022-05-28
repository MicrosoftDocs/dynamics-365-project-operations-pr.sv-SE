---
title: Nyheter i april 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i april 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613276"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i april 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.41.0.45
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.26

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Kategorier för inköp kan användas i projektinköpsorder och väntande leverantörsfakturor. Mer information finns i [Använda inköpskategorier med projektinköpsorder och väntande leverantörsfakturor](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

I följande tabell visas mappningar med dubbelskrivning som har ändrats eller lagts till i mars 2022-versionen av Project Operations.

| Entitetsmappning | Uppdaterad version | Kommentarer |
| -------------- | ------------------- | ------------|
| Exportentitet msdyn\_projectvendorinvoicelines på fakturarad för projektleverantör för Project Operations-integrering | 1.0.0.4 | Denna mappning stöder användning av inköpskategorier med inköpsorder och väntande leverantörsfakturor. |

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| ------------ | ---------------- | -------------- |
| Tid och utgift | 2573900 | Funktionen **Modernt godkännande** måste vara aktiverad som standard. |
| Fakturering och prissättning | 2603313 | Åtgärdade ett dubblettpostfel som förhindrade att offerter och kontraktrader med en produkt lades till. |
| Distribution och konfiguration | 2611368 | Kunderna måste kunna lägga till upp till fem egna entiteter i lösningen med hjälp av den moderna appdesignern. |
| Tid och utgift | 2628285 | Åtgärdade ett problem som påverkade möjligheten att ange rätt resurskategori under importen av tidsposten. |
|   Affärsmöjlighetshantering| 2628815 | Uppdatera teckengränsen för offertradens detaljbeskrivning så att denna överensstämmer med teckengränsen för uppgiftsämnet, detta så att importen lyckas för uppgifter där ämnet är längre än 100 tecken. |
| Tid och utgift| 2629547 | Fältet **Skickades av** för projektgodkännanden måste peka mot den användare som skickade posten. |
| Tid och utgift| 2629865 | Fältet **Kopiera kategori** för uppgifter när projekt kopieras. |
| Tid och utgift| 2636463 | Åtgärdade filtren på godkännanden i moderna godkännandeformulär. |
| Projektplanering och spårning | 2648300 | Åtgärdade ett problem som förhindrade att projektägaren ändras. |
| Fakturering och prissättning | 2563000 | Journalrader för en ofakturerad försäljning där valutan skiljer sig från kontraktvalutan får inte tillåtas. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services (LCS) och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
