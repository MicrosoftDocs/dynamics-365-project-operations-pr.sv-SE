---
title: Konfigurera redovisning för fakturerbara projekt
description: I det här ämnet finns information om redovisningsalternativ för fakturerbara projekt.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4398ef44d4211a2921270bebe38fc92f18503854
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287665"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurera redovisning för fakturerbara projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations har stöd för olika redovisningsalternativ för fakturerbara projekt som omfattar transaktioner med tid och material och fast pris.

- **Tids- och materialtransaktioner**: dessa transaktioner faktureras allt eftersom arbetet fortskrider utifrån förbrukningen av timmar, utgifter, artiklar eller avgifter i projektet. Dessa transaktionskostnader kan matchas med omsättningen för varje transaktion och projektet faktureras allt eftersom arbetet fortskrider. Projektintäkter kan även påföras när transaktionen utförs. Under faktureringen registreras intäkter och i tillämpliga fall återförs upplupna intäkter.
- **Fastpristransaktioner**: dessa transaktioner faktureras enligt en faktureringsplan som baseras på projektkontraktet. Intäkter för fastpristransaktioner kan registreras vid fakturering eller beräkning och bokföras med jämna mellanrum, enligt metoderna **Slutfört kontrakt** eller **Slutförd procent**.

Ett projekt betraktas som fakturerbart när det är associerat med en eller flera kontraktrader. En kontraktrad för ett projekt definierar för sig vilken faktureringsmetod och vilka transaktionstyper som är tillåtna.

Fabrikam Robotics har till exempel vunnit ett projektkontrakt med Adatum Corporation för optimering av utrustningen. Adatum kommer att betala ett fast belopp på 100 000 kronor för att täcka uppkommande projektutgifter. Det här är en faktureringsmetod för fast pris. Projekttid och -avgifter faktureras per användning. Det här är en faktureringsmetod för tid och material. Allt arbete spåras under ett enda projekt med namnet Adatum utrustningsoptimering.

En medlem i en projektteam skickar åtta timmars arbete med Adatum utrustningsoptimering. När projektledaren godkänner den här tiden använder systemet faktureringsmetoden för tid och material för att skapa verkliga transaktioner, en faktura och ett konto. Den här transaktionen tas inte med i beräkningen av uppskattning av fast pris för intäkt.

En annan medlem i ett projektteam skickar en reseutgift på 20 000 kronor mot Adatum utrustningsoptimering. När projektledaren godkänner den här inlämningen använder systemet faktureringsmetoden för fast pris för att skapa verkliga transaktioner och ett konto för projektutgiften. Kunden faktureras inte utifrån den här transaktionen. De kommer i stället att faktureras med hjälp av separat konfigurerade faktureringsmilstolpar. Den här utgiftstransaktionen, samt utgiftsuppskattningar, tas inte med i beräkningen av uppskattning av fast pris för intäkt.

Redovisningsprinciper för projekttransaktioner definieras i projektkostnads- och intäktsprofiler. För varje projekttransaktion fastställer systemet rätt projektkostnads- och intäktsprofil med hjälp av reglerna för projektkostnad och intäktsprofil som har konfigurerats.

## <a name="define-project-cost-and-revenue-profiles"></a>Definiera projektkostnad och intäktsprofiler 

Projektkostnad och intäktsprofiler bestämmer redovisningsreglerna för projekttransaktioner. Dessa profiler konfigureras i Projekthantering och redovisning. 

Följ stegen nedan om du vill skapa en ny projektkostnads- och intäktsprofil. 

1. Gå till **Projekthantering och bokföring** > **Konfiguration** > **Bokföring** > **Projektkostnads- och intäktsprofiler**. 
2. Välj **Ny** om du vill skapa en ny projektkostnads- och intäktsprofil.
3. I fältet **Namn** anger du namnet och en kortfattad beskrivning av profilen.
4. I fältet **Faktureringsmetod** väljer du **Tid och material** eller **Fast pris**.
5. Expandera snabbfliken **Transaktionsregister**. Fälten på den här fliken definierar de redovisningsprinciper som används när projekttransaktioner bokförs med hjälp av Project Operations integreringsjournal och sedan faktureras med hjälp av fakturaförslag för projektet.
6. Välj lämplig information i följande fält i snabbfliken **Transaktionsregister**:

    - **Bokför kostnader – timme**:

       - *Inget transaktionsregister*: kostnaden för tidstransaktioner kommer inte att bokföras i transaktionsregistret när Project Operations integreringsjournal bokförs. Revisorn kan emellertid bokföra kostnader med hjälp av funktionen Bokför kostnader senare.
       - **Saldo**: kostnaden för tidstransaktioner debiteras till kontotypen Transaktionsregister, *PIA – kostnadsvärde* och krediteras till *lönefördelningskontot* i transaktionsregistrets bokföringsinställningar. Funktionen Bokför kostnader används för att flytta kostnaden från ett saldokonto till ett resultatkonto periodiskt.
       - **Vinst och förlust**: när du bokför journalen för Project Operations debiteras tidstransaktionens kostnad kontotypen *Kostnad* i transaktionsregistret och krediteras det *lönefördelningskonto* som har definierats under fliken **Kostnad** på sidan för **bokföringsinställningar för transaktionsregister** (**Projektledning och bokföring** \> **Inställningar** \> **Bokföring** \> **Inställningar för bokföring i transaktionsregister**). Det här är den vanligaste inställningen för tids- och materialtransaktioner.
        - *Aldrig transaktionsregister*: kostnaden för tidstransaktioner kommer inte att bokföras i transaktionsregistret.

    - **Bokföra kostnader – utgifter**:

         - **Saldo**: när du bokför integreringsjournalen för Project Operations debiteras kostnaden för utgiftstransaktioner kontotypen *PIA – kostnadsvärde* i transaktionsregistret enligt definitionen under fliken **Kostnad** på sidan **Bokföringsinställningar för transaktionsregister** och krediteras motkontot på journalraden. Standardmotkonton för utgift definieras i **Projekthanterings och bokföring** > **Inställningar** \> **Bokföring** \> **Standardmotkonto för utgifter**. Funktionen **Bokför kostnader** används för att flytta kostnaden från saldokontot till resultatkontot periodiskt.
        - **Resultat**: när du bokför integreringsjournalen för Project Operations debiteras kostnaden för utgiftstransaktioner kontotypen *Kostnad* i transaktionsregistret enligt definitionen under fliken **Kostnad** på sidan **Bokföringsinställningar för transaktionsregister** och krediteras motkontot på journalraden. Standardmotkonton för utgift definieras i **Projekthantering och bokföring** \> **Inställningar** \> **Bokföring** \> **Standardmotkonto för utgifter**.
       
    - **Kontofakturering**:

        - **Saldo**: när du bokför projektfakturaförslaget krediteras en kontotransaktion (faktureringsmilstolpe) till kontotypen *PIA fakturerad – konto* i transaktionsregistret enligt vad som definierats under fliken **Intäkt** på sidan **Bokföringsinställningar för transaktionsregister** och debiteras på kundens saldokonto.
         - **Resultat**: när du bokför projektfakturaförslaget krediteras en kontotransaktion (faktureringsmilstolpe) till kontotypen *Fakturerad intäkt – konto* i transaktionsregistret enligt vad som definierats under fliken **Intäkt** på sidan **Bokföringsinställningar för transaktionsregister** och debiteras på kundens saldokonto. Kundens saldokonton anges i **Kundreskontra** \> **Inställningar** \> **Kundbokföringsprofiler**.

   När du definierar bokföringsprofilerna för tids- och materialfaktureringsmetoderna kan du välja att periodisera intäkter per transaktionstyp (timme, utgift och avgift). Om alternativet **Periodisera intäkt** står på **Ja**, registreras ofakturerade försäljningstransaktioner i integreringsjournalen för Project Operations i huvudboken. Försäljningsvärdet debiteras kontot **PIA – försäljningsvärde** och krediteras kontot **Upplupna intäkter – försäljningsvärde** som har ställts in på sidan **Bokföringsinställningar för transaktionsregister** under fliken **Intäkt**. 
  
  > [!NOTE]
  > Alternativet **Periodisera intäkter** är endast tillgängligt när kostnaden för respektive transaktionstyp **Kostnad** bokförs på resultatkontot.
    
7. Expandera snabbfliken **Uppskattning**. Fälten under den här fliken definierar beräkningsinställningarna för uppskattningar av intäkt från fast pris. Fälten under den här fliken gäller endast för projektkostnads- och intäktsprofiler med faktureringsmetoden **Fast pris**.
8. Välj lämplig information i följande fält i snabbfliken **Uppskattning**:

    - **Princip som används för beräkning vid projektslutförande**:

        - **Slutfört kontrakt**: kostnadsmatchning och intäktsredovisning inträffar inte förrän projektet är slut. Kostnaderna återspeglar PIA i saldot tills projektet är slutfört.
        - **Slutförd procent**: upplupna intäkter beräknas och bokförs i transaktionsregistret varje period utifrån projektets slutförandeprocentsats. Det finns flera tillgängliga metoder för att beräkna slutförandeprocent. Metoderna kan vara automatiska efter konfiguration eller manuella.
        - **Ingen PIA**: den här inställningen används för fastprisprojekt med en kort tidsperiod och där fakturan och kostnaderna inträffar i samma period. I det här fallet ställs värdet för fältet **Kontofakturering** under snabbfliken **Transaktionsregister** automatiskt in på **Resultat** för att säkerställa att intäkter registreras vid fakturering. Processen för intäktsuppskattning används inte för den här projektkostnads- och intäktsprofilen.

    - **Matchningsprincip**: det här fältet avgör hur det beräknade försäljningsvärdet (upplupna intäkter) ska bokföras i transaktionsregistret.

        - Med hjälp av principen **Försäljningsvärde** beräknas försäljningsvärdet genom att matcha kostnader och intäkter och sedan bokföra dem som ett enda belopp.
        - Med hjälp av principen **Produktions och vinst** delas försäljningsvärdet i de realiserade kostnaderna och den beräknade vinsten. Dessa bokförs separat.

    - **Kostnadsmallar**: tillåta att projekttransaktioner grupperas efter transaktionstyp och projektkategori och definiera regler för beräkning av slutförd procentandel för dessa grupper.
    - **Periodkoder**: definiera hur ofta intäktsuppskattningar beräknas för en viss projektkostnads- och intäktsprofil.
    - **Kategorier för uppskattning**: används för bokföring av försäljningsvärde (upplupna intäkter) i projekttransaktioner. Börja med att konfigurera den dedikerade projektkategorin för transaktionstypen **Avgift** och ange sedan flaggan **Uppskattning** för projektkategorin. Därefter, beroende på vald matchningsprincip, väljer du denna projektkategori i värdet **Försäljning** eller fältet **Vinst** i projektkostnads- och intäktsprofilen.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Exempel på konfigurationer för projektkostnads- och intäktsprofiler

Tid och material – ingen PIA

![Kostnads- och intäktsprofil: tid och material – ingen PIA](media/time-material-no-wip.png)

Tid och material – PIA (intäkt)

![Kostnads- och intäktsprofil: tid och material – PIA](media/time-material-with-wip.png)

Fast pris – ingen PIA

![Kostnads- och intäktsprofil: fast pris – ingen PIA](media/fixed-price-no-wip.png)

Fast pris – slutfört kontrakt

![Kostnads- och intäktsprofil: fast pris – slutfört kontrakt](media/fixed-price-completed-contract.png)

Fast pris – procent färdigt

![Kostnads- och intäktsprofil: fast pris – procent färdigt](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exempel på redovisningshändelser för exempel på projektkostnads- och intäktsprofiler.

| Redovisningshändelse                  | Tid och material – ingen PIA                       | Tid och material – PIA                                                                                           | Fast pris – ingen PIA                                            | Fast pris – slutfört kontrakt                                                                            | Fast pris – procent färdigt                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Bokföra tidstransaktioner    | Debet – kostnad <br>Kredit – löneallokering          | Debet – kostnad <br>Kredit – löneallokering <br>Debet – försäljningsvärde för PIA <br>Kredit – försäljningsvärde för upplupna intäkter                | Debet – kostnad <br>Kredit – löneallokering                         | Debet – kostnad <br>Kredit – löneallokering                                                                    | Debet – kostnad <br>Kredit – löneallokering                       |
| Bokföra utgiftstransaktioner | Debet – kostnad <br>Kredit – motkonto för utgift | Debet – kostnad <br>Kredit – motkonto för utgift <br>Debet – försäljningsvärde för PIA <br>Kredit – försäljningsvärde för upplupna intäkter      | Debet – kostnad <br>Kredit – motkonto för utgift                 | Debet – kostnad<br> Kredit – motkonto för utgift                                                            | Debet – kostnad <br>Kredit – motkonto för utgift               |
| Kundfakturering                | Debet – Kundsaldo <br>Kredit – fakturerad intäkt | Debet – Kundsaldo <br>Kredit – fakturerad intäkt <br>Kredit – debet för PIA-försäljning – försäljningsvärde för upplupna intäkter | Debet – Kundsaldo <br>Kredit – fakturerad intäkt – konto | Debet – Kundsaldo <br>Kredit – PIA – fakturerad på konto                                                  | Debet – Kundsaldo <br>Kredit – PIA – fakturerad på konto    |
| Bokföra uppskattad intäkt             | Gäller inte                                   | Gäller inte                                                                                                    | Gäller inte                                                  | Debet – värde för PIA-kostnad <br>Kredit – kostnad                                                                         | Debet – PIA – försäljningsvärde <br>Kredit – försäljningsvärde för upplupna intäkter |
| Ta bort                         | Gäller inte                                   | Gäller inte                                                                                                    | Gäller inte                                                  | Debet – värde för PIA-kostnad <br>Debet – kostnad <br>Kredit – upplupna intäkter – försäljningsvärde <br>Debet – PIA, fakturerad på konto | Debet – PIA – fakturerad på konto <br>Kredit – PIA, försäljningsvärde     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurera regler för projektkostnads- och intäktsprofiler

Reglerna för projektkostnads- och intäktsprofiler avgör vilken projektkostnads- och intäktsprofil som måste användas när du bearbetar några fakturerbara projekttransaktioner. Definiera reglerna genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Bokföring** \> **Regler för projektkostnads- och intäktsprofiler**.

Regler kan definieras efter projektkontrakt, projektgrupp eller efter ett specifikt projekt. Systemet kommer alltid att välja den högsta detaljeringsregeln först.


[!INCLUDE[footer-include](../includes/footer-banner.md)]