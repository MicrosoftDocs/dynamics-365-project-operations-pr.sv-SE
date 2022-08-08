---
title: Nyheter i juni 2022 – Project Operations för resurs/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i juni 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031353"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i juni 2022 – Project Operations för resurs/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.43.0.77 eller 4.43.0.119
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

I följande tabell visas mappningar med dubbelskrivning som har ändrats eller lagts till i juni 2022-versionen av Project Operations.

| Entitetsmappning | Uppdaterad version | Kommentarer |
| --- | --- | --- |
| Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices) | 1.0.0.1 | Det gamla fältet har nu inaktiverats och mappats till det nya fältet för statusspårning av leverantörsfaktura. |

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Legotillverkning | 2708885 | Åtgärdade felmeddelandet som visas när en användare skapar en bokningsbar resursbokningsrubrikpost där ingen bokningsbar resurs fylls i. |
| Projektplanering och spårning | 2629441 | Korrigerade arbetsflödesutlösningslogiken för att hjälpa till att förhindra en loop för loopar när projektuppgifter uppdateras. |
| Tid och utgift | 2641209 | För tidsinmatning som importeras från tilldelningar/bokningar måste det finnas en bokningsbar resursreferens. |
| Projektplanering och spårning | 2651148 | Projektdokumentrubriken måste vara försedd med ett meddelande.|
| Projektplanering och spårning | 2653145 | Lade till valideringar för att säkerställa att en projektpost inte kan skapas med icke-giltiga tecken i namnet. |
| Tid och utgift | 2654710 | Korrigerade filtreringen på sidan **Godkännanden**. |
| Fakturering och prissättning | 2667805 | Lade till valideringar för att förhindra att faktiska fakturerade försäljningar skapas om det inte finns några fakturerade försäljningsfakturering. |
| Fakturering och prissättning | 2668378 | Ytterligare valideringar har lagts till för att förhindra att anpassade priser läggs till såvida inte ett logiskt namn och ett fältnamn fylls i. |
| Legotillverkning | 2677485 | Uppdaterade målversionen av leverantörsfakturaraderna med dubbla skrivningsmappning. |
| Tid och utgift | 2700428 | Förbättrad godkännandelogik för att se till att andra godkännandeuppsättningar för projektet kan bearbetas även om en av godkännandeuppsättningarna har fastnat i systemjobb. |

### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services (LCS) och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
