---
title: Nyheter och ändringar i Project Operations, oktober 2021 för lagerbaserade/produktionsbaserade scenarier
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i oktober 2021-versionen av Project Operations för resurs-/produktionsbaserade scenarier.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818481"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Nyheter och ändringar i Project Operations, oktober 2021 för lagerbaserade/produktionsbaserade scenarier

_**Gäller för:** Project Operations för lagerbaserade/produktionsbaserade scenarier_

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.22
 
## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
|--------------|------------------|----------------|
| Projektledning och redovisning | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Belopp för pågående projektarbete (PIA) och ansamlade intäktsbelopp återförs inte korrekt när en koncernintern kundfaktura publiceras. |
| Projektledning och redovisning | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funktionen **Förhindra att projekt stängs vid öppna transaktioner** fungerar inte. |
| Projektledning och redovisning | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Faktureringsklassificeringen på en fritextfaktura fyller inte i mått från projekt automatiskt när den funktionen har aktiverats. |
| Projektledning och redovisning | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | I icke-företagsinterna scenarier återförs PIA- och ansamlade intäktsbelopp återförs inte korrekt när projektfakturan publiceras. |
| Projektledning och redovisning | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debet- och kreditvärden byter plats när tillägget för Microsoft Excel används tillsammans med utgiftsjournalen för projekt och fältet **Motkontotyp** anges som **Projekt**. |
| Projektledning och redovisning | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Det belopp som publiceras i projekttransaktioner överdrivs i en projektinköpsorder som innehåller lagerartiklar och som har icke-avdragbara momsbelopp när **UseTax** har markerats. |
| Projektledning och redovisning | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Systemet delar beloppet mellan projektvinst- och projektförlustrapporterna samt projektets PIA-rapporter. |
| Projektledning och redovisning | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Lagerbehållningen blir fel när ett delvis returnerat artikelkrav har justerats. |
| Projektledning och redovisning | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resursnamn dupliceras i Project Operations när de redigeras i Microsoft Project. |
| Projektledning och redovisning | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Koncerninterna utgiftsrapporter med information om koncerninterna leverantörsreskontrakostnader som väntar på att faktureras publiceras först i bokföringstypen **PIA-kostnad för projekt**. I samband med bearbetning publiceras beräkningsrelaterade kostnader emellertid i bokföringstypen **Projektkostnad** istället för i den förväntade bokföringstypen **Företagsintern kostnad**. |
| Projektledning och redovisning | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Leverantörens behållningsresultat i transaktioner för projektutgifter visas emellertid inte. |
| Projektledning och redovisning | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Tidsschemat måste avrunda transaktionsbeloppet i transaktionsvalutan till ett angivet antal decimaler för alla redovisningsdistributioner och allmänna journalallokeringsposter. |
| Projektledning och redovisning | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Antalet projektobjektkrav uppdateras automatiskt när de planerade orderna har bestämts. |
| Projektledning och redovisning | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Verifikationsnummer, leverantörssaldo för transaktionstyp samt kontonummer kan inte återställas på förbetalda fakturor för ett inköpsnummer. |
| Projektledning och redovisning | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Den koncerninterna leverantörsfakturan blir felaktig när integrering av leverantörsfaktura aktiveras. |
| Projektledning och redovisning | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | När du skapar en projektutgiftsmall visas kostnadsbeloppet i fältet **Kredit**. |
| Projektledning och redovisning | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Betalningsvillkoren i projektfakturor fungerar inte som förväntat. |
| Projektledning och redovisning | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Tidsrapportverifieringar kan återanvändas när nummersekvensen har angetts som kontinuerlig. |
| Projektledning och redovisning | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANKRIKE: Logiken för **Manuellt kvarhållningsbelopp** överensstämmer inte med logiken för **Automatiskt kvarhållningsbelopp** i förslaget till projektavtalsfaktura. |
| Projektledning och redovisning | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | När kvarhållning av leverantör frigörs får verifikationspubliceringen ytterligare rader som är felaktiga. |
| Projektledning och redovisning | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | När fältet **Fakturadatum** på sidan **Skapa fakturaförslag** ändras kan följande fel uppstå: "Objektreferensen har inte angetts till någon objektinstans." |
| Projektledning och redovisning | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Ett fel uppstår när du försöker godkänna en tidsrapport från arbetsflödet **TSLine**, och det finns en tidsrapportpolicy för lördag och söndag. |
| Projektledning och redovisning | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Projektobjekttypen för ingående saldo exkluderas från **Transaktionssammanfattningar för fakturaförslag** när fakturaförslagets fakturabelopp beräknas. |
| Projektledning och redovisning | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Om kostnaden för en projektproduktionsorder är 0 (noll) inträffar följande fel när du försöker beräkna: "Försökte dela med noll". |
| Projektledning och redovisning | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilappen Project Timesheet för Android slutar svara. Problemet är relaterat till **TimeEntryDataManager ArgumentNullException**. |
| Projektledning och redovisning | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Integreringsjournalen för Project Operations misslyckas vid publicering eftersom ett konto saknar mått. Kontot som saknar måtten är emellertid inte det konto du publicerar inlägg i. |
| Projektledning och redovisning | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtret **ToDate** i sökningar rensas inte när den tas bort från dialogrutan **Välj** på sidan **Inläggskostnad**. |
| Projektledning och redovisning | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Återställ all distribution** misslyckas och ett felmeddelande visas för de tidsrapporter som har skapats för ett projekt av den typen **Endast tid**. |
| Projektledning och redovisning | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Fliken **Projekt** kan inte redigeras på en väntande leverantörsfaktura när kategorin för inköp tilldelas objektet. |
| Projektledning och redovisning | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeringsfönstret saknas om du inte är inloggad i Project Operations Dataverse. |
| Projektledning och redovisning | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | För företagsinterna projektanpassningstransaktioner finns problem i destinationsföretaget. |
| Projektledning och redovisning | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Bekräftade kostnader för ett projekt beräknar fel kvantitet och kostnadspris om inköpsordern har bearbetats av **Årsbokslutsprocessen för inköpsorder** i redovisningen. |
| Projektledning och redovisning | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | När en projektproduktionsorder med kvalitetsorder rapporteras som slutförd visas följande fel: "Ingen virtuell transaktion har märkts med lagertransaktion." |
| Projektledning och redovisning | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | När en projektrelaterad faktura för leverantörsreskontra har lagts upp uppstår följande fel: "Uppräknad text Projekt – kostnad – artikel finns ej." |
| Projektledning och redovisning | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirekta kostnader fördubblas när du ansamlar intäkter manuellt. |
| Projektledning och redovisning | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Periodiseringsintäkter och PIA-inlägg ger inga transaktioner. |
| Projektledning och redovisning | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktiveringen av det väntande priset misslyckas för en standardkostnadsartikel när det finns en mottagen projektinköpsorder. |
| Projektledning och redovisning | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Det omvända PIA-värdet från en fakturabokföring skiljer sig från det ursprungliga, bokförda PIA-värdet i en tidspost. |
| Projektledning och redovisning | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ett bokföringsproblem har uppstått för projektfakturerade intäkter i tillämpade kvarhållningsärenden där verifikationstransaktioner ej är i balans. |
| Projektledning och redovisning | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | När en uppskattning skapas efter att ett fakturaförslag har publicerats, blockeras importen av korrigeringsrader i Project Operations. |
| Projektledning och redovisning | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Ändringar av en helt fakturerad milstolpepost bör inte vara möjliga. |
| Projektledning och redovisning | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | När du använder automatiska avgifter går det inte att lägga upp en koncernintern kundfaktura för en tidsrapport, och ett felmeddelande visas. |
| Projektledning och redovisning | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adressen i ett underprojekt uppdateras inte korrekt. |
| Projektledning och redovisning | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Kostnadspriset för artikelkraven uppdateras med inköpspriset för konsoliderade inköpsorder. |
| Projektledning och redovisning | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Den upplagda kostnaden är inte korrekt efter att inköpspriset har uppdaterats och parametern **Aktivera ändringshantering** har aktiverats. |
| Resor och utgifter | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alla användarutgifter visas när du söker efter en kategori i mobilappen Utgifter. |
| Resor och utgifter | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Felaktiga belopp för leverantörs- och momstransaktioner publiceras från en utgift som skapats från en kreditkortstransaktion. |
| Resor och utgifter | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Ett irrelevant varningsmeddelande visas när du uppdaterar sidorna för utgiftsrapport. |
| Resor och utgifter | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Fel tillfällig godkännare används när du tar bort en tillfällig godkännare och sedan skickar in via arbetsflödet igen. |
| Resor och utgifter | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ett publiceringsfel relaterat till konfigurationen för körsträcka uppstår. |
| Resor och utgifter | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distributionen uppdaterar inte den juridiska entiteten när en icke-bifogad transaktion läggs till på nytt i utgiftsrapporten för en företagsintern utgift. |

### <a name="regulatory-updates"></a>Regleringsuppdateringar

Mer information om regleringsuppdateringar för Finance and Operations-appar finns i [regleringsuppdateringar](/dynamics365/finance/localizations/regulatory-updates). Du kan också logga in på Microsoft Dynamics Lifecycle Services (LCS) och använda verktyget för problemsökning för att visa de planerade regelverksuppdateringarna. Med en problemsökning kan du söka efter land eller region, typ av funktion och version.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
