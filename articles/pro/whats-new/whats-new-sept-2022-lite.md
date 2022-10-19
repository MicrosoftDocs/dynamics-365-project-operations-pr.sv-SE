---
title: Nya september 2022 – Distribution av Project Operations Lite
description: Denna artikel innehåller information om de kvalitetsuppdateringar som är tillgängliga i distributionsversionen av Microsoft Dynamics 365 Project Operations lite för september 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634875"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Nya september 2022 – Distribution av Project Operations Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.46.0.60

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

| Funktionsområde | Funktionsnamn | Mer information |
| --- | --- | --- |
| Administrering av affärsmöjligheter | **Revision och aktivering av offerter**<br>Med Project Operations får försäljningsprocessen fullt stöd. Projektofferter kan aktiveras så att de motsvarar ett tillstånd där offerten är skrivskyddad och granskas. Aktiverade offerter kan revideras för att skapa nya offerter med ett stegvis revisionsnummer. Aktiverade projektofferter eller offertrevisioner kan stängas som vunna eller förlorade. | [Aktivera och revidera en projektoffert](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturering och prissättning | **Tidszonens agnostiska pris är standard**<br>Project Operations har introducerat konceptet med ett tidszon agnostiskt datum för alla projektets faktiska värden. Ett nytt fält, **Transaktionsdatum**, är nu tillgängligt på rader och faktiska värden och används för att lagra datumet då transaktionen inträffade, men utan att konvertera det datumet till Coordinated Universal Time. Det här datumet används i processer nedströms, till exempel för standardpris och skapande av fakturor. | <p>[Avgör kostnadstaxa för projektbaserade beräkningar och utfall](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Fastställa försäljningspriser för projektbaserade beräkningar och utfall](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fakturering och prissättning | **Datum då priset ska gälla åsidosätts i Project Operations**<br>Datumspecifika prisändringar är ett sätt att åsidosätta eller ändra specifika priser i prislistan. | [Datumspecifika prisändringar](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tid och utgift | **Global godkännare**<br>Med den här funktionen kan oberoende ISV (programvaruleverantör) och centraliserat godkännande aktiveras, oavsett projekt- eller teammedlemsstatus i projektet. | [Säkerhet och godkännanden](/dynamics365/project-operations/approvals/approvals-security) |
|Projektplanering och spårning|**Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter** </br> </br>Med redigerings-API:t för resurstilldelningsredigering kan utvecklare programmässigt ange en uppgiftstilldelningsobjekts insats i alla datumintervall som stöds för en mer detaljerad planering av tidsfasad insats.|[Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2754422 | Material och kostnader för förs inte över till Dynamics 365 Finance när projekt kopieras i Dataverse. |
| Tid och utgift | 2787409 | En icke-giltig godkännare kan godkänna en icke-projekttidspost. |
| Administrering av affärsmöjligheter | 2788907 | Uppdaterat felmeddelande om unique validation för orderrader som innehåller flaggar. |
| Tid och utgift | 2842253 | Null-undantagshantering för tidsgodkännande. |
| Fakturering och prissättning | 2844181 | Misslyckande att få korrelations-ID blockerar fakturaskapande. |
| Fakturering och prissättning | 2876628 | QLD, CLD – Beräkna prislistematchning bör använda tidigare datumintervallfält i prislistan. |
| Legotillverkning | 2893222 | Om ingen roll har angetts för en underleverantörsrad bör det vara möjligt att välja den raden på en teammedlem för alla roller. |
