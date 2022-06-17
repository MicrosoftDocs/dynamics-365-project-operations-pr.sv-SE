---
title: Nyheter i juli 2021 i Project Operations för lagerbaserade/produktionsbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i juli 2021-versionen av Project Operations för lagerbaserade/produktionsbaserade scenarier.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: df9a68c5a12e6aec140867eb1db3d88279c05795
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933652"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Nyheter i juli 2021 i Project Operations för lagerbaserade/produktionsbaserade scenarier

_**Gäller för:** Project Operations för lagerbaserade/produktionsbaserade scenarier_

Denna artikel gäller följande Dynamics 365 Project Operations komponenter och versioner:

- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.20
 
### <a name="quality-updates"></a>Kvalitetsuppdateringar
                                                                                                                                                                                  
| Funktionsområde                      | Referensnummer| Kvalitetsuppdatering                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektledning och redovisning | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Kostnadsinköpsposter från en inköpsrekvisition rensas så fort köpordern har släppts från inköpsrekvisitionsfrågan.                                                                           |
| Projektledning och redovisning | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Budgetvalidering sker två gånger på en inköpsrekvisition. Dubbletten innebär att rekvisitionen inte kan stängas och att motsvarande order inte skapas.                                                                                                                        |
| Projektledning och redovisning | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Faktureringsregeln **Procent att räkna på** kunde inte slutföras på grund av en avrundningsproblem.                                                                              |
| Projektledning och redovisning | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | När du justerar transaktionen och procentsatsen har decimaler justeras inte kostnaden och försäljningspriset korrekt.                                      |
| Projektledning och redovisning | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Redovisningskällautforskaren visar timmar för en enda tidrapportrad för flera tidrapportrader med olika aktiviteter.                                      |
| Projektledning och redovisning | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Sparade vyer och information om tidsschemasdetaljer gör att systemet alltid öppnar informationen för första gången i listan när de försöker öppna en timevyn.  |
| Projektledning och redovisning | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Projektrotnoden försvinner och poster för uppdelad arbetsstruktur tas bort efter import.                                                                                             |
| Projektledning och redovisning | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | När objekt tas emot och utfärdas delvis från artikelkraven uppdateras fel budgetanvändningssaldo. |
| Projektledning och redovisning | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | I projekthållna köporder visas inte summorna korrekt i rutan **Totalsummor** eller rutnätet **Väntande faktura**.                                                                  |
| Projektledning och redovisning | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | När du stänger lagret, justeras projektartikelkostnaden till saldokontot i stället för vinst- och förlustkontot.                                                            |
| Projektledning och redovisning | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | I en projekttransaktion och en beräkningsvaluta används USD som redovisningsvaluta, men beloppet visar vad CAD-motsvarigheten skulle vara.              |
| Projektledning och redovisning | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Åtagna kostnader med ett artikelbehov och inköpsorder är felaktiga i inköpsorderfakturaprocessen med delproduktkvitto och delfakturering.       |
| Projektledning och redovisning | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Projektanpassningen uppdaterar inte försäljningsbeloppet korrekt med indirekta kostnader.                                                                                    |
| Projektledning och redovisning | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabell **Tidkort** saknar ett definierat förhållande med **Arbets/resurs**.                                                                                   |
| Projektledning och redovisning | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Det går inte att fylla i fältet **Aktivitetsnummer** när du väljer det i listrutan för en tidsförkortning.                                                                 |
| Projektledning och redovisning | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Du kan inte lägga till ett anpassat fält för **Syfte** eller **Aktivitetsbeskrivning** till följande sidor: **Projektposterad transaktion**, **Skapa fakturaförslag** eller **Fakturaförslag**.  |
| Projektledning och redovisning | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Fel leveransdatorkontroll tillhandahålls när du skapar artikelkrav med hjälp av datahantering (**ProjSalesItemRequirementEntity**).                                              |
| Projektledning och redovisning | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | När du väljer ett Projektkontrakt-ID i Finance öppnas sidan Project Operations för att skapa en ny post, istället för att öppna det befintliga projektkontraktet.                                                                                                                 |
| Projektledning och redovisning | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Etiketten, ”@SYS4083080” (”Det går inte att hitta en unik arbetarpost som motsvarar de angivna värdena ”) översätts inte till danska.                                |
| Projektledning och redovisning | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Fältet **Momsgrupp för artikelförsäljning** kan inte redigeras på ett fakturaförslag.                                                                               |
| Projektledning och redovisning | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Bekräftad kostnad dras över med ej avdragsgilla momsbelopp.                                                                                                    |
| Projektledning och redovisning | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Om du publicerar en anläggning med flera projekt och olika ekonomiska mått skapas oväntade värden i huvudboken.                             |
| Projektledning och redovisning | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Fakturaförslagsrader dupliceras på grund av flera instanser av den periodiska processen för **importera från mellanlagring** som körs samtidigt.                                      |
| Projektledning och redovisning | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Det finns ett fel i inlägg i fakturautanteckningen för kreditfakturan, så transaktionerna på kreditfakturan balanserar inte.    |
| Projektledning och redovisning | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Kostnader för projekt som har förts in blir inkorrekta efter att väntande fakturor har släppts.                                                                             |
| Projektledning och redovisning | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Det går inte att skapa en kreditfaktura för en projektförsäljningsorder när momsen är i en annan valuta än företagsvalutan.                                      |
| Projektledning och redovisning | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Genom att radera ett kontrakt raderas också adressen som är kopplad till kunden                                                                                     |
| Projektledning och redovisning | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Det går inte att publicera ett fakturaförslag på grund av en korrigering av en negativ tidstransaktion.                                                                    |
| Resor och utgifter                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Moms beräknas på olika sätt i utgiftsrapporter.                                                                                                                  |
| Resor och utgifter                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Versionsuppdatering **DB72_Expense.updateTrvExpTransProjTransId()** tillåter inte **trvExpTrans.ReferenceDataAreaId** att skapa den nya nummersekvensen.                    |
| Resor och utgifter                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Det in arkiverade beloppet visas inte med det obligatoriska fältet.                                                                                                             |
| Resor och utgifter                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Förbättringar av prestanda när det gäller att lägga till utgifter i utgiftsrapporten med hjälp av det nya användargränssnittet för utgifter.                                                            |
| Resor och utgifter                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Du kan ta bort bokförda utgiftsrapporter.                                                                                           |
| Resor och utgifter                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Meddelandet om utgiftspolicyn visas flera gånger.                                                                                                       |
| Resor och utgifter                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Fältet **Betalningsmetod** ingår i fönstret **Nya utgifter**.                                                                                                      |
| Resor och utgifter                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Verktyget **Återställ dokumentstatus för utgift** bör återställa statusen för utgiftsrapporten till **Utkast** om arbetsflödet inte hittas. 

### <a name="regulatory-updates"></a>Regleringsuppdateringar
Information om regeluppdateringar för appar för ekonomi och drift finns i [Regeluppdateringar](/dynamics365/finance/localizations/regulatory-updates). Du kan också logga in på Lifecycle Services (LCS) och visa de planerade regeluppdateringarna med sökverktyget Problem. Med problemsökning kan du söka efter land, typ av funktion och utgåva.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
