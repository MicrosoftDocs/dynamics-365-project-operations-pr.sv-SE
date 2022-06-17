---
title: Konfigurera automatiskt fakturaskapande
description: Den här artikeln innehåller information om hur du konfigurerar och konfigurerar automatisk generering av proforma-fakturor.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c5160b22bd0d8a738c31a5105d83bd15cf136fab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911756"
---
# <a name="set-up-automatic-invoice-creation"></a>Konfigurera automatiskt fakturaskapande 
 
_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resurs-/icke-lagerbaserade scenarier_

Du kan konfigurera automatiskt fakturaskapande i Dynamics 365 Project Operations. Systemet skapar ett utkast till en proforma-faktura utifrån faktureringsschemat för varje projektkontrakt och kontraktrad. Faktureringsscheman konfigureras på kontraktradsnivå. Varje rad i ett kontrakt kan ha en särskild faktureringsplan, eller så kan samma faktureringsschema tas med på alla rader i kontraktet.

När du skapar en faktura skapas alltid minst en faktura per projektkontrakt. I vissa fall kan flera fakturor skapas. Om kontraktet till exempel har flera kunder skapas samma antal fakturor som antalet kunder som har fakturerbara transaktioner att fakturera på det projektkontraktet.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Förstå hur transaktioner tas med på en faktura 

Ibland anges ett separat faktureringsschema för varje projektrelaterad kontraktrad. Implementeringstjänster för Adatum-kontrakt har t.ex. följande kontraktrader:

- Prototyparbete som är ett fast pris med två manuellt skapade milstolpar.
- Implementeringsarbete som omfattar tid och debiteras varannan vecka på måndagar.
- Utgifter som måste faktureras varje månad den första måndagen i varje månad.

Faktureringsscheman som har definierats på var och en av dessa två radartiklar ser ut som följande tabell:

| Kontraktrad | Körningsdatum för faktura | Transaktionens slutdatum | Milstolpens datum | Milstolpebelopp |
| --- | --- | --- | --- | --- |
| Prototyparbete | 5 oktober, måndag | - | 5 oktober, måndag | 5000 USD |
| - | Tisdagen den 3 november | - | Tisdagen den 3 november | 12,000 USD |
| Implementeringsarbete | 5 oktober, måndag | 4 oktober, söndag | - | - |
| - | 19 oktober, måndag | 18 oktober, söndag | - | - |
| - | Måndag 2 november | Söndag 1 november | - | - |
| - | Måndag 16 november | Söndag 15 november | - | - |
| Kostnader som uppstår | 5 oktober, måndag | 4 oktober, söndag | - | - |
| - | Måndag 2 november | Söndag 1 november | - | - |

I det här exemplet när automatisk fakturering körs för:

- **4 oktober eller något tidigare datum**: Ingen faktura genereras för det här kontraktet eftersom tabellen **Faktureringsschema** för var och en av dessa kontraktrader inte svarar till söndag den 4 oktober som ett datum för fakturakörning.
- **Måndagen den 5 oktober**: en faktura skapas för:

    - Prototyparbete som innehåller milstolpen om den är markerad som **Klar för fakturering**.
    - Implementeringsarbete som omfattar alla tidstransaktioner som skapats före transaktionens avskärningsdatum söndagen den 4 oktober och som är markerat som **Klar för fakturering**.
    - Utgift som omfattar alla utgifttransaktioner som skapats före transaktionens avskärningsdatum söndagen den 4 oktober och som är markerat som **Klar för fakturering**.
  
- **Den 6 oktober eller något datum för den 19 oktober**: Ingen faktura genereras för det här kontraktet eftersom tabellen **Faktureringsschema** för var och en av dessa kontraktrader inte svarar till den 6 oktober eller något datum före den 19 oktober som ett datum för fakturakörning.
- **Mådagen den 19 oktober**: En faktura genereras för implementeringsarbete som omfattar alla tidstransaktioner som skapats före transaktionens avskärningsdatum söndagen den 18 oktober och som är markerat som **Klar för fakturering**.
- **Måndagen den 2 november**: en faktura skapas för:

    - Implementeringsarbete som omfattar alla tidstransaktioner som skapats före transaktionens avskärningsdatum söndagen den 1 november och som är markerat som **Klar för fakturering**.
    - Utgift som omfattar alla utgifttransaktioner som skapats före transaktionens avskärningsdatum söndagen den 1 november och som är markerat som **Klar för fakturering**.

- **Tisdagen den 3 november** : En faktura skapas för prototyparbete som innehåller milstolpen för 12 000 USD om den är markerad som **Klar för fakturering**.

## <a name="configure-automatic-invoicing"></a>Konfigurera automatisk fakturering

Slutför stegen nedan om du vill konfigurera en automatisk fakturakörning.

1. I **Project Operations** går du till **Inställningar** > **Konfigurera återkommande faktura**.
2. Skapa ett batch-jobb och ge det namnet **Project Operations skapa fakturor**. Namnet på batch-jobbet måste innehålla orden "skapa fakturor".
3. I fältet **Jobbtyp**, välj **Ingen**. Som standard är fälten **Frekvens dagligen** och **Är aktiv** angivna som **Ja**.
4. Välj **Kör arbetsflöde**. I dialogrutan **Sök efter post** visas tre arbetsflöden:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Välj **ProcessRunCaller** och välj **Lägg till**.
6. Klicka på **OK** i nästa dialogrutan. Arbetsflödet **Vila** följs av **Process**. 

> [!NOTE]
> Du kan också välja **ProcessRunner** i steg 5. När du sedan väljer **OK**, följs arbetsflödet **Process** av arbetsflödet **Vila**.

Arbetsflödena **ProcessRunCaller** och **ProcessRunner** skapar fakturor. **ProcessRunCaller** anropar **ProcessRunner**. **ProcessRunner** är det arbetsflöde som verkligen skapade fakturorna. Arbetsflödet går igenom alla kontraktrader som fakturorna måste skapas för och fakturor för dessa rader skapas. För att fastställa vilka kontraktsrader som fakturor ska skapas tittar jobbet på körningsdatum för faktura för kontraktsraderna. Om kontraktrader som tillhör ett kontrakt har samma datum för fakturakörning kombineras transaktionerna till en faktura med två fakturarader. Om det inte finns några transaktioner att skapa fakturor för hoppar jobbet över skapandet av fakturan.

När **ProcessRunner** har körts klart anropas **ProcessRunCaller**, anger sluttiden och är stängd. **ProcessRunCaller** startar sedan en timer som körs i 24 timmar från den angivna sluttiden. **ProcessRunCaller** stängs i slutet av timern.

Batchprocessjobbet för att skapa fakturor är ett återkommande jobb. Om batchprocessen körs flera gånger skapas flera instanser av jobbet och det uppstår fel. Därför bör du endast starta batchprocessen en gång och du bör sedan starta om den endast om den slutar att fungera.

> [!NOTE]
> Batchfakturering i Project Operations körs endast för projektkontraktrader som konfigurerats av fakturascheman. En kontraktrad med en fast pris faktureringsmetod måste ha milstolpar konfigurerad. En projekts kontraktrad med en tids- och material faktureringsmetod måste ha en datumbaserad fakturauppställning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
