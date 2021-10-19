---
title: Nyheter i augusti 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i augusti 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501393"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i augusti 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier

*Gäller: Project Operations för resursscenarier/icke lagerbaserade scenarier*

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

   - Project Operations i Microsoft Dataverse miljöversion 4.13.0.152.
   - Projektledning och redovisning i Dynamics 365 Finance-miljö version 10.0.20.

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- **Godkännandeuppsättningar**: Med godkännande anges gruppförfrågningar om tid, utgifter eller materialanvändningsgodkännande tillsammans i mindre underuppsättningar med åtgärder. Med hjälp av denna gruppering kan godkännanden bearbetas per projekt i en specifik ordning, och det går att försöka och sekvensera på nytt. Genom att gruppera förfrågningarna ökar tillförlitligheten och spårbarheten för bearbetning av godkännanden för stora godkännandevolymer. Mer information finns i [Godkännandeuppsättningar](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen.

En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av kartan i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av kartan visas på sidan **Dubbelriktad skrivning** i kolumnen **Version**. Aktivera en ny version av kartan genom att välja **tabellmappningsversioner**, välja den senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på ett problem som startar kartan, följ instruktionerna i avsnittet [Saknade tabellkolumner saknas på kartor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbla skrivningar.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2295625 | Milstolpens namn måste kopieras från fakturaschemat till detaljinformation för fakturaraden. |
| Fakturering och prissättning | 2316323 | Rabatten ska inte vara redigerbar på en proformafaktura i Project Operations för resursbaserade scenarier. |
|   Affärsmöjlighetshantering | 2338619 | Affärsreglerna **Affärsmöjlighet** och **Offert** får endast anropas på sidor. |
| Resurshantering | 2316523 | Användning av **Skicka förfrågan** från ett resurskrav med tillhörande roll ska inte generera något fel. |
| Resurshantering | 2326885 | Om du skapar ett resurskrav via ett projekt ska inget fel visas. |
| Tid och utgift | 2335584 | Inaktuella uppgiftsflöden i tidsposten. |
| Tid och utgift | 2336884 | Tidspostknappen **Kopiera vecka** måste fungera för mer än bara den aktuella användaren. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Resor och utgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Felaktiga belopp för leverantörs- och momstransaktioner anges när en utgift skapas från en kreditkortstransaktion. |
| Resor och utgifter | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Den felaktiga avräkningen är rader som skapas när betalningsjournalen skapas. |
| Resor och utgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Felaktiga belopp för momstransaktioner anges när en utgift skapas från en kreditkortstransaktion. |
| Resor och utgifter | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Det kan ta lång tid att ta bort en utgiftsrad. |
| Projektredovisning | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Systemet stöder inte konfiguration av kontinuerlig antalssekvensering när du publicerar en beräkning efter att ha tillämpat KB 4619395. |
| Projektredovisning | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Det kanske inte går att publicera leverantörsfakturan med felmeddelandet "Transaktionerna i verifikationen balanseras inte per 2021-05-17. (redovisningsvaluta: 0,00 – rapportvaluta: 0,01)" |
