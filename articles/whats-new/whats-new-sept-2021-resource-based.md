---
title: Nyheter september 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Den ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i september 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582916"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter september 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier

*Gäller: Project Operations för resurs-/icke-lagerbaserade scenarier*

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

   - Project Operations i Microsoft Dataverse miljöversion 4.14.0.99.
   - Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av kartan i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av kartan visas på sidan **Dubbelriktad skrivning** i kolumnen **Version**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på ett problem med att starta kartan, följ instruktionerna i avsnittet [Problem med kolumner i saknade register på kartor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Tid och utgift | 1811407 | Justerat projekt godkännaren säkerhetsroll för godkännande av utgiftspost. |
| Tid och utgift | 1811438 | Justerat projekt godkännaren säkerhetsroll för avvisande av arbetsorderns tidspost. |
| Tid och utgift | 2370126 | Uppdaterade **Projektuppgift** och **Roll** ikoner i entiteten **Tidspost**. |
| Tid och utgift | 2379879 | Korrigerade funktionen **Kopiera vecka** i tidsposten när Dynamics 365 för telefon används. |
| Fakturering och prissättning | 2371906 | Totalbeloppet för Proforma-fakturor får inte kunna anpassas i Project Operations för resursbaserade distributioner. |
| Fakturering och prissättning | 2385802 | Åtgärdat felet som inträffar med negativa faktiska timmar när projektsummorna uppdateras. |
| Fakturering och prissättning | 2389675 | Bättre bekräftelsefunktion i proforma-fakturor. Entiteten för långvariga jobb måste ta hänsyn till aktiviteten som krävs för att skriva bekräftelseresultat för redovisning. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Resor och utgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Beloppen för leverantörs- och momstransaktioner som är upplagda från en kostnad som skapats från en kreditkortstransaktion är felaktiga. |
| Resor och utgifter | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Fel rader skapas när betalningsjournal skapas. |
| Resor och utgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Beloppen för och momstransaktioner som är upplagda från en kostnad som skapats från en kreditkortstransaktion är felaktiga. |
| Resor och utgifter | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Det kan ta lång tid att ta bort en utgiftsrad. |
| Projektredovisning | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | När du har tillämpat KB 4619395 ändrar du nummersekvensen till **Kontinuerlig** stöds inte och när du lägger upp en uppskattning uppstår följande fel: "Systemet stöder inte installationen" kontinuerlig "av nummersekvensen Proj_X." |
| Projektredovisning | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Det kan hända att det går fel att bokföra en leverantörsfaktura med följande felmeddelande: "Transaktionerna för verifikation balanseras inte per 2021-05-17. (redovisningsvaluta: 0,00 – rapportvaluta: 0,01)." |
