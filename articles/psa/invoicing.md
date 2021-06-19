---
title: Fakturering i Project Service Automation
description: I det här ämnet finns information om fakturering.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e0dc911bb0ca72af547262a5716ef1091ea81c81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015083"
---
# <a name="invoicing-in-project-service-automation"></a>Fakturering i Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fakturering i Dynamics 365 Project Service Automation kan vara användbart eftersom det ger projektledarna en annan godkännandenivå innan de skapar fakturor för kunder. Den första godkännandenivån slutförs när tids- och utgiftsposter som skickats från projektteammedlemmar har godkänns.

PSA har inte utformats för att skapa kundfakturor, av följande orsaker:

- Den innehåller inte skatteinformation.
- Det går inte att konvertera andra valutor till faktureringsvalutan med hjälp av korrekt konfigurerade valutakurser.
- Det går inte att formatera fakturor korrekt så att de kan skrivas ut.

I stället kan du använda ett finans- eller bokföringssystem för att skapa kundfakturor som använder informationen från fakturaförslag som genereras i PSA.

## <a name="creating-project-invoices-in-psa"></a>Skapa projektfakturor i PSA

Du kan skapa projektfakturor en i taget eller i bulk. Du kan skapa dem manuellt, eller så kan de konfigureras så att de genereras i automatiska körningar.

### <a name="manually-create-project-invoices-in-psa"></a>Skapa projektfakturor manuellt i PSA

På listsidan **projektkontrakt** kan du skapa projektfakturor separat för varje projektkontrakt, eller så kan du skapa fakturor i bulk för flera projektkontrakt.

Följ det här steget om du vill skapa en faktura för ett specifikt projektkontrakt.

- På listsidan **projektkontrakt**, öppna ett projektkontrakt och välj sedan **skapa faktura**.

    ![Skapa projektfakturor för ett visst projektkontrakt](media/CreateProjectInvoicesOneByOne.png)

    En faktura skapas för alla transaktioner för det valda projektkontraktet som har statusvärdet **klart att fakturera**. Dessa transaktioner inkluderar tid, utgifter, milstolpar och produktbaserade kontraktrader.

Följ stegen nedan om du vill skapa fakturor i bulk.

1. På listsidan **projektkontrakt** väljer du ett eller flera projektkontrakt som du måste skapa en faktura för och väljer sedan **skapa projektfakturor**.

    ![Skapa projektfakturor i bulk](media/CreateProjectInvoicesBulk.png)

    Ett varningsmeddelande visas med information om att en fördröjning kan uppstå innan fakturorna skapas. Även processen visas.

2. Stäng meddelanderutan genom att välja **OK**.

    En faktura skapas för alla transaktioner på en kontraktrad som har statusvärdet **klart att fakturera**. Dessa transaktioner inkluderar tid, utgifter, milstolpar och produktbaserade kontraktrader.

3. Om du vill visa fakturorna som genereras går du till **försäljning** \> **fakturering** \> **fakturor**. En faktura visas för varje projektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Konfigurera automatisk skapande av projektfakturor i PSA

Följ stegen nedan om du vill konfigurera en automatisk fakturakörning i PSA.

1. Gå till **Project Service** \> **Inställningar** \> **Batchjobb**.
2. Skapa ett batch-jobb och ge det namnet **PSA skapa fakturor**. Namnet på batch-jobbet måste innehålla termen "skapa fakturor".
3. I fältet **Jobbtyp**, välj **Ingen**. Som standard är alternativen **Frekvens dagligen** och **Är aktiv** angivna som **Ja**.
4. Välj **Kör arbetsflöde**. I dialogrutan **Sök efter post** visas tre arbetsflöden:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Välj **ProcessRunCaller** och välj **Lägg till**.
6. Klicka på **OK** i nästa dialogrutan. Arbetsflödet **Vila** följs av **Process**.

    Du kan också välja **ProcessRunner** i steg 5. När du sedan väljer **OK**, följs arbetsflödet **Process** av arbetsflödet **Vila**.

Arbetsflödena **ProcessRunCaller** och **ProcessRunner** skapar fakturor. **ProcessRunCaller** anropar **ProcessRunner**. **ProcessRunner** är det arbetsflöde som verkligen skapade fakturorna. Det går igenom alla kontraktrader som fakturorna måste skapas för och fakturor för dessa rader skapas. För att fastställa vilka kontraktrader som fakturor ska skapas tittar jobbet på körningsdatum för faktura för kontraktraderna. Om kontraktrader som tillhör ett kontrakt har samma datum för fakturakörning kombineras transaktionerna till en faktura med två fakturarader. Om det inte finns några transaktioner för att skapa fakturor hoppar jobbet över skapandet av fakturan.

När **ProcessRunner** har körts klart anropas **ProcessRunCaller**, anger sluttiden och är stängd. **ProcessRunCaller** startar sedan en timer som körs i 24 timmar från den angivna sluttiden. **ProcessRunCaller** stängs i slutet av timern.

Batchprocessjobbet för att skapa fakturor är ett återkommande jobb. Om batchprocessen körs flera gånger skapas flera instanser av jobbet och det uppstår fel. Därför bör du endast starta batchprocessen en gång och du bör starta om den endast om den slutar att fungera.

> [!NOTE]
> Batch-fakturering i Project Service Automation körs endast för projekt kontrakt rader som konfigurerats av fakturascheman. En kontraktrad med en fast pris faktureringsmetod måste ha milstolpar konfigurerad. En projekts kontraktrad med en tids- och material faktureringsmetod måste ha en datumbaserad fakturauppställning. Information om hur du ställer in faktureringsfrekvenser inom ramen för ett projekt som bygger på en offertrad finns på raderna för ämne, [offerter och offertrader](basic-quote-lines.md#invoice-schedule). Detsamma gäller för en projektrelaterad kontraktrad.      
 
### <a name="edit-a-draft-psa-invoice"></a>Redigera ett utkast till en PSA-faktura

När du skapar ett utkast till en projektfaktura skickas alla ej fakturerade försäljningstransaktioner som skapades när utgiftsposterna godkändes. Du kan göra följande justeringar medan fakturan är i ett utkaststadium:

- Ta bort eller redigera information om fakturarader.
- Redigera och justera kvantitet och faktureringstyp.
- Lägg direkt till tid, utgifter och avgifter som transaktioner på fakturan. Du kan använda den här funktionen om fakturaraden är mappad till en kontraktrad som tillåter dessa transaktionsklasser.

Välj **bekräfta** om du vill bekräfta en faktura. Åtgärden Bekräfta är en enkelriktad åtgärd. När du väljer **bekräfta** blir fakturan skrivskyddad och verkliga värden för fakturerad försäljning skapas utifrån varje fakturaradinformation för varje fakturarad. Om fakturaradinformationen refererar till en ofakturerad faktisk försäljning återförs även den ofakturerade faktiska försäljningen. (All information på fakturaraden som skapades från en tidpunkt eller utgiftspost refererar till en ofakturerad faktisk försäljning.) Integreringssystemen för redovisning kan använda den här återföringen för att omvända pågående pågående projekt (WIP) i redovisningssyfte.

### <a name="correct-a-confirmed-psa-invoice"></a>Korrigera en bekräftad PSA-faktura

Bekräftade PSA-fakturor kan redigeras (korrigeras). När du korrigerar en bekräftad faktura skapas en ny korrigeringsfaktura för utkast. Eftersom det är en förutsättning att du vill återföra alla transaktioner och kvantiteter från den ursprungliga fakturan, inkluderar den korrigerande fakturan alla transaktioner från den ursprungliga fakturan och alla kvantiteter på den är 0 (noll).

Om en transaktion inte kräver korrigering kan du ta bort dem från utkastfakturan. Om du vill återföra eller returnera en delkvantitet kan du redigera fältet **antal** på raddetaljen. Om du öppnar fakturaradinformationen visas ursprungligt fakturaantal. Du kan sedan redigera aktuellt fakturerat antal så att det är mindre än eller lika med den ursprungliga fakturan.

När du bekräftar en rättningsfaktura återförs den ursprungliga fakturerade faktiska försäljningen och en ny fakturerad faktisk försäljning skapas. Om antalet minskas kommer differensen att skapa en ny fakturerad faktiskt försäljning. Om t.ex. den ursprungliga fakturerade försäljningen var åtta timmar och detaljerna för korrigeringsfakturaraderna har en mindre mängd på sex timmar, återförs den ursprungliga faktureringsförsäljningsraden och två nya faktiska värden skapas:

- En fakturerad faktisk försäljning som faktiskt innehåller sex timmar.
- En ofakturerad faktisk försäljning för de återstående två timmarna. Denna transaktion kan antingen faktureras senare eller vara markerad som icke debiterbar, beroende på förhandlingarna med kunden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]