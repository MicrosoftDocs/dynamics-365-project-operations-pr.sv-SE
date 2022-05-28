---
title: Proforma projektfakturor
description: Den ämne information om projektbaserade proforma-fakturor i Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f2ce672a412f7ad73b072854590cd423a3499fc1
ms.sourcegitcommit: 650a84add65588defdd2ac2c4524806baab070e0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2022
ms.locfileid: "8628876"
---
# <a name="proforma-project-invoices"></a>Proforma projektfakturor

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Proforma-projektfakturering ger projektledarna en annan godkännandenivå innan de skapar fakturor för kunder. Den första godkännandenivån slutförs när tids- och utgifts- och materialposter som skickats från projektteammedlemmar har godkänns.

Dynamics 365 Project Operations Lite-distribution är inte utformat för att generera kundfakturor. I följande lista visas varför fakturor inte kan skapas:

- Den innehåller inte skatteinformation.
- Det går inte att konvertera andra valutor till faktureringsvalutan.
- Det går inte att formatera fakturor för utskrift korrekt.

I stället kan du använda ett finans- eller bokföringssystem för att skapa kundfakturor som använder informationen i genererade fakturaförslag.

## <a name="creating-project-invoices"></a>Skapa projektfakturor

Du kan skapa projektfakturor en i taget eller i bulk. Du kan skapa dem manuellt, eller så kan de konfigureras så att de genereras i automatiska körningar.

### <a name="manually-create-project-invoices"></a>Skapa projektfakturor manuellt 

På listsidan **projektkontrakt** kan du skapa projektfakturor separat för varje projektkontrakt, eller så kan du skapa fakturor i bulk för flera projektkontrakt.

   - För att skapa en faktura för ett specifikt projektkontrakt, på listsidan **Projektkontrakt**, öppna ett projektkontrakt och välj sedan **Skapa faktura**.

   En faktura skapas för alla transaktioner för det valda projektkontraktet som har statusvärdet **klart att fakturera**. Dessa transaktioner omfattar tid, utgifter, material, milstolpar, produktbaserade kontraktrader och andra ofakturerade försäljningsrader som kan ha bekräftats.

För att skapa fakturor i massåtgärd:

1. På listsidan **projektkontrakt** väljer du ett eller flera projektkontrakt för att skapa en faktura för och väljer sedan **skapa projektfakturor**.
2. Ett varningsmeddelande visas med information om att en fördröjning kan uppstå innan fakturorna skapas. Även processen visas. Stäng meddelanderutan genom att välja **OK**.

   En faktura skapas för alla transaktioner på en kontraktrad som har statusvärdet **klart att fakturera**. Dessa transaktioner omfattar tid, utgifter, material, milstolpar, produktbaserade kontraktrader och andra ofakturerade försäljningsrader som kan ha bekräftats.

3. Visa fakturorna som genereras genom att gå till **försäljning** \> **fakturering** \> **fakturor**. En faktura visas för varje projektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurera automatisk skapande av projektfakturor 

Följ stegen nedan om du vill konfigurera en automatisk fakturakörning.

1. Gå till **Inställningar** \> **Batchjobb**.
2. Skapa ett batch-jobb och ge det namnet **Project Operations skapa fakturor**. Namnet på batch-jobbet måste innehålla termen "skapa fakturor".
3. I fältet **Jobbtyp**, välj **Ingen**. Som standard är alternativen **Frekvens dagligen** och **Är aktiv** angivna som **Ja**.
4. Välj **Kör arbetsflöde**. I dialogrutan **Sök efter post** visas följande arbetsflöden:

    - ProcessRunCaller
    - Processkörare
    - Uppdatera rollanvändning

5. Välj **ProcessRunCaller** och välj **Lägg till**.
6. Klicka på **OK** i nästa dialogrutan. Arbetsflödet **Vila** följs av **Process**.

    Du kan också välja **ProcessRunner** i steg 5. När du sedan väljer **OK**, följs arbetsflödet **Process** av arbetsflödet **Vila**.

Arbetsflödena **ProcessRunCaller** och **ProcessRunner** skapar fakturor. **ProcessRunCaller** anropar **ProcessRunner**. **ProcessRunner** är det arbetsflöde som skapade fakturorna. Detta arbetsflöde går igenom alla kontraktrader som fakturorna måste skapas för och skapar dessa fakturor. För att fastställa vilka kontraktrader som fakturor ska skapas tittar arbetsflöde på körningsdatum för faktura för kontraktraderna. Om kontraktrader som tillhör ett kontrakt har samma datum för fakturakörning kombineras transaktionerna till en faktura med två fakturarader. Om det inte finns några transaktioner för att skapa fakturor, inga fakturor skapas.

När **ProcessRunner** har körts klart anropas **ProcessRunCaller**, anger sluttiden och är stängd. **ProcessRunCaller** startar sedan en timer som körs i 24 timmar från den angivna sluttiden. **ProcessRunCaller** stängs i slutet av timern.

Batchprocessjobbet för att skapa fakturor är ett återkommande jobb. Om batchprocessen körs flera gånger skapas flera instanser av jobbet och det kan uppstå fel. Lås problemet genom att starta batchprocessen en gång och endast starta om den endast om den slutar att fungera.

> [!NOTE]
> Batchfakturering körs endast för projektkontraktrader som konfigurerats av fakturascheman. En kontraktrad med en fast pris faktureringsmetod måste ha milstolpar konfigurerad. En projekts kontraktrad med en tids- och material faktureringsmetod måste ha en datumbaserad fakturauppställning. Detsamma gäller för en projektrelaterad kontraktrad.      
 
### <a name="edit-a-draft-invoice"></a>Redigera ett utkast till en faktura

När du skapar ett utkast till en projektfaktura skickas alla ej fakturerade försäljningstransaktioner som skapades när utgiftsposterna godkändes. Du kan göra följande justeringar medan fakturan är i ett utkaststadium:

- Ta bort eller redigera information om fakturarader.
- Redigera och justera kvantitet och faktureringstyp.
- Lägg direkt till tid, utgifter, material och avgifter som transaktioner på fakturan. Du kan använda den här funktionen om fakturaraden är mappad till en kontraktrad som tillåter dessa transaktionsklasser.

Välj **bekräfta** om du vill bekräfta en faktura. Denna åtgärden är en enkelriktad åtgärd. När du väljer **bekräfta** blir fakturan skrivskyddad och verkliga värden för fakturerad försäljning skapas utifrån varje fakturaradinformation för varje fakturarad. Om fakturaradinformationen refererar till en ofakturerad faktisk försäljning återförs även den ofakturerade faktiska försäljningen. Alla fakturaraddetaljer som skapats utifrån en tids-, utgifts- eller materialanvändningspost refererar till den faktiska försäljningen som inte har fakturerats. I system för redovisning av huvudboksintegrering kan detta användas för att vända projektarbete (WIP) för redovisningssyften.

### <a name="correct-a-confirmed-invoice"></a>Korrigera en bekräftad faktura

Bekräftade fakturor kan redigeras. När du korrigerar en bekräftad faktura skapas en ny korrigeringsfaktura för utkast. Eftersom det är en förutsättning att du vill återföra alla transaktioner och kvantiteter från den ursprungliga fakturan, inkluderar den korrigerande fakturan alla transaktioner från den ursprungliga fakturan och alla kvantiteter på den är noll.

Om en transaktion inte kräver korrigering kan du ta bort dem från utkastfakturan. Om du vill återföra eller returnera en delkvantitet kan du redigera fältet **antal** på raddetaljen. Om du öppnar fakturaradinformationen visas ursprungligt fakturaantal. Du kan sedan redigera aktuellt fakturerat antal så att det är mindre än eller lika med den ursprungliga fakturan.

När du bekräftar en rättningsfaktura återförs den ursprungliga fakturerade faktiska försäljningen och en ny fakturerad faktisk försäljning skapas. Om antalet minskas kommer differensen att skapa en ny fakturerad faktiskt försäljning. Om t.ex. den ursprungliga fakturerade försäljningen var åtta timmar och detaljerna för den korrigerade fakturaraden har en mindre mängd på sex timmar, återförs den ursprungliga faktureringsförsäljningsraden och två nya faktiska värden skapas:

- En fakturerad faktisk försäljning som faktiskt innehåller sex timmar.
- En ofakturerad faktisk försäljning för de återstående två timmarna. Denna transaktion kan faktureras senare eller vara markerad som icke debiterbar, beroende på förhandlingarna med kunden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
