---
title: Nyheter och ändringar i Project Operations, september 2021 för lagerbaserade/produktionsbaserade scenarier
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i september 2021-versionen av Project Operations för resurs-/produktionsbaserade scenarier.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815857"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Nyheter och ändringar i Project Operations, september 2021 för lagerbaserade/produktionsbaserade scenarier

_**Gäller för:** Project Operations för lagerbaserade/produktionsbaserade scenarier_

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.21
 
## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
|---|---|---|
| Projektledning och redovisning | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Om rollen som inköpsansvarig erhåller åtkomst till en juridisk person får den även åtkomst till alla projekt i alla juridiska entiteter. |
| Projektledning och redovisning | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Ett problem med momsavrundning sker när en kreditfaktura kvittas mot en ursprunglig projektfaktura. |
| Projektledning och redovisning | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Använd en alternativ projektbudget för budgetverifiering. |
| Projektledning och redovisning | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Prisgruppen **Försäljningspris/timme** beräknas inte utifrån projektofferternas uppdelade arbetsstruktur. |
| Projektledning och redovisning | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Uppskattningselimineringen fungerar inte om funktionen **Aktivera projektkontraktsvaluta för uppskattningsberäkning** har aktiverats. |
| Projektledning och redovisning | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Momsfaktorisering efter kvantitet läggs till i försäljningspriset när användningsskatt används i momsgruppen för projektets utgiftsjournal. |
| Projektledning och redovisning | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Villkorlig moms beräknas inte korrekt för den sista betalningen när leverantörskvarhållning och förbetalning tillämpas på inköpsorderfakturor. |
| Projektledning och redovisning | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Justeringsspårning fungerar inte för journaler för ingående saldo. |
| Projektledning och redovisning | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Budgetändringsallokering för projekt efter period** delas upp över alla budgetperioder. När allokeringen skickas, avmarkeras inte posten. |
| Projektledning och redovisning | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Arbete pågår (PIA)-publiceringar i redovisningen har ett felaktigt belopp. |
| Projektledning och redovisning | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Godkännande av journalen för projekttimmar fungerar inte. |
| Projektledning och redovisning | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Försäljningspriset för projektanpassning uppdateras inte med indirekta kostnader när finansieringsbegränsningen är omarkerad. |
| Projektledning och redovisning | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Det går inte att skapa ett artikelkrav när tabellrubriken Försäljning faktureras och uppbackningsinköpsordern för befintliga rader är slutgiltig. |
| Projektledning och redovisning | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Kvarhållningsbeloppet för en faktureringsregel som har en milstolpe för ett annat projekt publiceras inte i motsvarande projekt-ID som valts för milstolpen. Istället publiceras det med det första projektet. |
| Projektledning och redovisning | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | När du väljer **Ekonomisk dimensionsuppsättning** i ett fakturaförslag uppstår följande fel: "Det gick inte att typkonvertera objekt av typen 'Dynamics.AX.Application.FormIntControl' to type 'Dynamics.AX.Application.FormStringControl'." |
| Projektledning och redovisning | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Rapporten **Projektfaktura** hoppar över rader. |
| Projektledning och redovisning | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Ett fel uppstår när du beräknar kostnadskontrollen för ett investeringsprojekt. |
| Projektledning och redovisning | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoden **ProjTable::InitFromCustTable – canDeletePostalAddress** orsakar ett prestandaproblem. |
| Projektledning och redovisning | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Felmeddelandet bör vara tydligare än "Oväntat fel". |
| Projektledning och redovisning | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Batchjobbet för publicering av projektfakturor bearbetar och publicerar fakturaförslaget även om fakturaraderna inte har genererats. |
| Projektledning och redovisning | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Ett avrundningsfel inträffar när konfigurationsnyckeln för offentliga licenser är inaktiverad. Fel kostnad eller försäljningspris genereras i tidsschemat för avtal som har flera finansieringskällor. |
| Projektledning och redovisning | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projektförsäljningspriset på en fakturerad projektinköpsorder beräknas felaktigt när försäljningsprismodellen är **Täckningsgrad**. |
| Projektledning och redovisning | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Systemet tar inte hänsyn till de aktiva dagarna där emellan när den effektiva arbetshastigheten beräknas för en anställd. |
| Projektledning och redovisning | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Ett publiceringsfel uppstår på den företagsinterna servern på grund av följande valideringsfel: "Ingen handelspartner har konfigurerats för juridisk person". |
| Projektledning och redovisning | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Beskrivningen från en inköpsorder som har en utgiftskategori hämtas inte i den publicerade projekttransaktionslistan. |
| Projektledning och redovisning | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Det finns en felaktig konvertering i artikeljournaler som publiceras i ett projekt. |
| Projektledning och redovisning | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Du kan bekräfta en inköpsorder även om finansieringsbegränsningen har överskridits. |
| Projektledning och redovisning | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Avsnittet **Korrigering/Annullera faktura** på en fritextfaktura försvinner när ett projekt-ID väljs. |
| Projektledning och redovisning | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Det finns prestandaproblem när ett projektfakturaförslag läggs upp från en projektförsäljningsorder som innehåller en artikel i lager. |
| Projektledning och redovisning | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Det går inte att lägga upp projektinköpsfakturor eftersom följande fel uppstår: "Funktionen AccDistProcessorProjectExtension.createForProjectRevenueLine har felaktigt anropats." |
| Projektledning och redovisning | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Uppdatera till skapande av batchjobb för projektberäkning i syfte att kunna köra flera underuppgifter. |
| Projektledning och redovisning | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Statusen för en tidsrapport kan inte uppdateras till **Utkast** när arbetsflödet har fastnat i tillståndet **Avbröts**. |
| Projektledning och redovisning | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Lagringsbelopp beräknas inte i fakturaförslaget för kreditfaktura om det finns flera rader. |
| Projektledning och redovisning | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | När du försöker ändra beloppet på en genererad faktura från en inköpsorder uppstår följande fel: "Transaktionerna i verifikationen balanseras inte per XX/XX/XXXX." (redovisningsvaluta: 0,00 – rapportvaluta: 0,01)." |
| Projektledning och redovisning | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Det finns ett prestandaproblem när ett projektfakturaförslag publiceras i batchläge, detta på grund av en sammanfogning med **GeneralJournalAccountEntry**. |
| Projektledning och redovisning | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Prestandaproblem uppstår när en tidsrapport läggs upp. |
| Projektledning och redovisning | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Kostnadsberäkningsstrukturen för uppdelad arbetsstruktur justeras inte korrekt efter att alla uppgifter har utökats eller när en enskild uppgift har utökats manuellt. |
| Projektledning och redovisning | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Projektoffertens Excel-mall kan inte läggas till i menyn **Öppna i Excel**. |
| Projektledning och redovisning | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Skattebefrielsenumret för en juridisk person inkluderas inte på en utskriven projektfaktura. |
| Projektledning och redovisning | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Inga ekonomiska data uppdateras i lagerenhetsfelet när ett projekt justeras i förhållande till kreditrader. |
| Projektledning och redovisning | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | När du har tillämpat KB 461935 kan du inte publicera uppskattningarna om du växlar till kontinuerliga nummersekvenser. |
| Projektledning och redovisning | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** gör att mobilappen Project Timesheet för Android slutar svara. |
| Projektledning och redovisning | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Det omvända PIA-värdet från en fakturabokföring skiljer sig från det ursprungliga, bokförda PIA-värdet i tidsposten. |
| Projektledning och redovisning | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | I tillämpade kvarhållningsärenden är transaktioner i en verifikation ej i balans när fakturerad intäkt för ett projekt bokförs. |
| Projektledning och redovisning | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | När funktionen **Förbättring i schemaläggningsprestanda för projektresurs** har aktiverats avrundas decimalvärden felaktigt efter resurstillgänglighet och -kapacitet. |
| Projektledning och redovisning | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Om funktionen **Skapa projektuppskattningar med hjälp av flera batchuppgifter** aktiveras fungerar skapande av beräkningar i med flera underaktiviteter endast för aktuell period. |
| Resor och utgifter | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | En policy för reserekvisition ignoreras, och arbetsflödet godkänns utan fel. |
| Resor och utgifter | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>I appen Mobile Expense sparas inte följande information på utgiftsraden:</p><ul><li>Projektets ID</li><li>Huruvida utgiften är fakturerbar</li><li>Aktivitetsnumret</li></ul> |
| Resor och utgifter | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Fältet **Bifogade kvitton** anges som **Ja** även om inget kvitto bifogats utgiftsraden. |
| Resor och utgifter | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Ett fel uppstår när du försöker ändra utgiftskategorin till **Personlig**. |
| Resor och utgifter | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Du kan inte bifoga ett kvitto och redigera överordnad utgift efter att en kreditkortstransaktion har delats upp i en personlig utgift. |
| Resor och utgifter | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Utgiftspolicyn för företagsinterna transaktioner med ett projekt-ID fungerar inte korrekt. |
| Resor och utgifter | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Den bokförda datuminformationen saknas för de bokförda utgiftsrapporterna. |
| Resor och utgifter | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Det finns problem med betalningsmetoden i mobilappen Utgifter. |
| Resor och utgifter | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | En reserekvisition som skapats för en arbetare kan användas för en annan arbetares utgiftsrapport före ombudsdatumet. |
| Resor och utgifter | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | När du skapar en utgift kommer ändringar i de ekonomiska måttvärdena inte att uppdateras korrekt på nivån för redovisningsdistribution på arbetsytan för **utgiftshantering**. |
| Resor och utgifter | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Godkännandestatus för huvudutgiftsraden synkroniseras inte med godkännandestatusen för specificerat radarbetsflöde. |
| Resor och utgifter | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ett fel uppstår om du publicerar en utgiftsrapport och momsåterställning har aktiverats. |
| Resor och utgifter | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | En delegat kan inte ta bort kostnadsdokument för en avslutad anställd. |
| Resor och utgifter | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Borttagningen av en utgiftsrad tar längre tid än förväntat och påverkar prestandan. |
| Resor och utgifter | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** förorsakar en överbliven **TaxUncommitted**-post eftersom endast **SourceDocumentLine** tas bort. |
| Resor och utgifter | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** beaktar inte **trvExpTrans.ReferenceDataAreaId** för att skapa den nya nummerserien. |

## <a name="regulatory-updates"></a>Regleringsuppdateringar

Mer information om regleringsuppdateringar för Finance and Operations-appar finns i [regleringsuppdateringar](/dynamics365/finance/localizations/regulatory-updates). Du kan också logga in på Microsoft Dynamics Lifecycle Services (LCS) och använda verktyget för problemsökning för att visa de planerade regelverksuppdateringarna. Med en problemsökning kan du söka efter land eller region, typ av funktion och version.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
