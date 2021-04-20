---
title: Nyheter i april 2021 – Project Operations för resursscenarier/icke lagerbaserade scenarier
description: Den ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i april 2021-versionen av Project Operations för resurs-/ej lagerbaserade scenarier.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868015"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i april 2021 – Project Operations för resursscenarier/icke lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

- Project Operations i Dataverse-miljöversion 4.9.0.221
- Projektledning och redovisning i Dynamics 365 Finance-miljö version 10.0.17

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- Material som inte är i lager för projekt. Viktiga funktioner är:
  - Uppskatta och prissätta icke lagrade material under försäljningscykeln för ett projekt. För mer information, se [Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Spåra användning av icke-lagermaterial under projektleveransen. För mer information, se [Registrera materialanvändning för projekt och projektuppgifter](../material/material-usage-log.md).
  - Fakturera kostnader för använt icke-lagermaterial. Mer information finns i [Hantera eftersläpad fakturering](../proforma-invoicing/manage-billing-backlog.md).
- Uppgiftsbaserad fakturering: Lagt till möjligheten att associera projektuppgifter till projektkontraktsrader och därigenom utsätta dem för samma faktureringsmetod, fakturafrekvens och kunder som de på kontraktsraden. Denna förening säkerställer korrekt fakturering, redovisning, intäktsuppskattning och erkännande för att arbeta i enlighet med denna inställning för projektuppgifter.
- Nya API:er i Dynamics 365 Dataverse tillåter att åtgärder skapas, uppdateras och tas bort med **Schemaläggningsentiteter**. För mer information, se [Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations i Dynamics 365 Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2124532 | Knappen **Korrigera faktura** visas på en proforma-faktura när lagringsbeloppet eller det tillämpade lagringsbeloppet finns på originalfakturan. Knappen visas endast för miljöer med Finance version 10.0.19 eller senare. |
| Fakturering och prissättning | 2224568 | Lade till logik för att aktivera anpassningar som omfattar plugin-programmet för fakturabekräftelsen. |
| Fakturering och prissättning | 2101098 | Förbättrad logiken för standardfält till proforma-faktura: **Faktureringsadress**, **Faktureringsnamn** och **Betalningsvillkor** nu standard från motsvarande projektkontrakts kundpost. |
| Fakturering och prissättning | 2021413 | Uppdaterade fälten **Faktisk kostnad** och **Försäljning** i entiteten **Uppgift** för att inkludera försäljningsvärden från obelagda och fakturerade kostnader för uppgifter. |
| Fakturering och prissättning | 2182110 | När du kopierar ett projektkontrakt återskapas kontraktrads-ID:t i målprojektkontraktet så att det är unikt. |
| Administrering av affärsmöjligheter | 2186741 | Lade till valideringar för att säkerställa fältet **Ursprung** och **Transaktionstyp** kan inte uppdateras om befintliga detaljer för offertrader. |
| Administrering av affärsmöjligheter | 2191353 | Milstolpar får inte skapas på en tids- och materialkontraktrad. |
| Administrering av affärsmöjligheter | 2216956 | Åtgärdade problem med **Uppdatera priser**. |
| Planering och spårning | 2182979 | Projektkopieringsfunktionen har förbättrats så att utläggsberäkningsraderna kopieras från det ursprungliga projektet. |
| Planering och spårning | 2184144 | Projektkopieringsfunktionen har förbättrats så att resurspositionens namn kopieras från det ursprungliga projektet. |
| Planering och spårning | 2184799 | Projektkopia: Kontroll som är försedd med syfte att säkerställa att det uppskattade startdatumet inte kan ändras medan kopiering pågår. |
| Planering och spårning | 2185134 | Projektkopia: Beräknat startdatum för målprojektet har angetts till dagens datum. |
| Planering och spårning | 2196373 | Projektkopia: Kontrollera att projektansvarig- och teammedlemsposter inte dupliceras i projektteamet. |
| Planering och spårning | 2211833 | Projektkopia: Resurstilldelningar kopieras från källprojektuppgiften till målprojektet. |
| Planering och spårning | 2186541 | Åtgärdade problem i rutnätet **Beräkningar** när du grupperar efter resurs. |
| Planering och spårning | 2166906 | Transaktionskategorin från en uppgift måste kopieras till entiteten **Resurstilldelning**. |
| Resurshantering | 2125362 | Åtgärdade problem med att skapa en generisk teammedlem med en timbaserad allokeringsmetod. |
| Tid och utgift | 2113603 | Åtgärdade det anpassningsrelaterade problemet genom att ta bort attribut från sidan **Tidspost**. Nu kontrollerar systemet om attributet finns på sidan innan det går att komma åt dem med hjälp av ett skript. |
| Tid och utgift | 2204377 | Kopierade tidsscheman måste visas automatiskt när du väljer **Kopiera vecka** under tidsposten. |
| Tid och utgift | 2209059 | Fältet **Status** kan redigeras för Dynamics 365 Field Service tidsposter. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Projektledning och redovisning | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminering av omvänd uppskattning fungerar inte i **regelbundet**.  |
| Projektledning och redovisning | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Med funktionen **Justering av redovisning** skapar ett problem med storbokskonton som har markerats **Tillåt inte manuell inmatning**. |
| Projektledning och redovisning | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Lade till affärslogik för att bearbeta korrigeringsfakturor, inklusive kvarhållarbelopp eller tillämpat kvarhållarbelopp. |
| Projektledning och redovisning | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Bokföringen av PIA-försäljningsvärde i koncernintern projektfakturering väljer ett oväntat konto. |
| Projektledning och redovisning | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | När du arbetar med hållare i Project Operations, orsakar ändringar av standardprojektet på kontraktet efter det att förskottsbetalningarna faktureras problem med inkommande kostnader. |
| Projektledning och redovisning | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Om du tar bort ett projekt från ett kontrakt i Project Operations bör du vid behov återställa standardprojektet för kontraktet. |
| Projektledning och redovisning | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | I Project Operations visas fel utgiftsrader i listan **Lägg till rad** på fakturan. |
| Projektledning och redovisning | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | I Project Operations, sidan **Inköpsavtal** i juridiska entiteter för Finance som är integrerade med Project Operations. |
| Projektledning och redovisning | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | På grund av ett Dataverse integrationsfel kan du inte konvertera en offert till en vunnen i Project Operations. |
| Projektledning och redovisning | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** kan ställa in finansieringskällans fakturadress från en annan kund.  |
| Projektledning och redovisning | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | I Project Operations väljs inga mått när du skapar en inläggsfaktura för en transaktionen. |
| Resa och utgift | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Förskottssaldot uppdateras inte för en utgiftsrapport om den godkänns och läggs upp rad för rad. |
| Resor och utgifter | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Moms för standardiserade utgiftsrapporter beräknas inte korrekt. |
| Resor och utgifter | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Ytterligare fält som är relaterade till projekt visas på den omarbetade sidan **Koncerninterna utgiftsrapporter**. |
| Resor och utgifter | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Ett felaktigt felmeddelande visas i rubriken för utgiftsrapporter. |
| Resor och utgifter | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | En utgiftsrapport har angetts felaktigt i ett scenario där momsen har angetts i destinationsadressen. |
| Resor och utgifter | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Rapportinskicksdatum skrivs inte ut på godkända utgiftsrapporter. |
| Resor och utgifter | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Fälten **Godkänt datum** och **Avvisat datum** fylls inte i när en utlägg har godkänts. |
| Resor och utgifter | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | En reserekvisition som skapats för en arbetare kan användas för en annan arbetares utgiftsrapport. |
| Resor och utgifter | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Utgiftskategorier är låsta när du lägger till en ny utläggsrad. |
| Resor och utgifter | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Att specificera en redan delad utgiftsrapport resulterar i en ofullständig bokning av verifikationen Leverantör\Redovisning och delar upp källutforskaren för redovisning eftersom **TRVEXPTRANS.SOURCEDOCUMENTLINE** dupliceras. |
| Resor och utgifter | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Reserekvisitionspolicyn fungerar inte som förväntat. |
| Resor och utgifter | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Leverantörens kontonamn visas inte i de upplagda projekttransaktionerna för utgiftsrapporter. |
| Resor och utgifter | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | I Project Operations går det inte att godkänna tid med en uppgift för ett projekt. |
| Resor och utgifter | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Förskottsreturkategorin uppdaterar inte förskottssaldon när de läggs upp. |
| Resor och utgifter | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Försäljningspriset beräknas felaktigt i utgiftsrapporter som skapats i en valuta med hjälp av importerade kreditkortstransaktioner och är associerade med ett projekt. |
| Resor och utgifter | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Återställa dataentiteten **TrvRequisitionLine** och det associerade unika indexet. |
| Resor och utgifter | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Lade till instrumentering i genereringen av **SOURCEDOCUMENTLINE**. |
| Resor och utgifter | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Fel reskontrajournal visas i ett scenario där momsen har angetts i destinationsadressen. |
| Resor och utgifter | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | För Project Operations används för att förfina utgifter och tas inte bort från Finance när de tas bort från Dataverse. |
| Resor och utgifter | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | När en utgiftskategori är en kategori som inte är en projektkategori kopieras inte de ekonomiska mått som valts på sidan **Utgifter** till utgiftsrapporten. |
