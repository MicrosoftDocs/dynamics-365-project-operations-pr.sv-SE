---
title: Konfigurera koncernintern fakturering
description: Detta ämne innehåller information och exempel om konfigurering av koncernintern fakturering av projekt.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595566"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurera koncernintern fakturering

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Slutför följande steg för att konfigurera koncernintern fakturering för projekt i Dynamics 365 Project Operations. Koncerninterna transaktioner är tids- och utgiftstransaktioner från ett projektkontrakt som tillhör ett företag eller en organisationsenhet, medan resurserna i projektkontraktet ingår i ett annat företag eller en annan organisationsenhet.

## <a name="example-configure-intercompany-invoicing"></a>Exempel: Konfigurera koncernintern fakturering

I följande exempel är Contoso Robotics USA (USPM) den låntagande juridiska personen och Contoso Robotics UK (GBPM) den långivande juridiska personen. 

1. **Konfigurera koncernintern redovisning mellan juridiska personer**. Varje par låntagande och utlånande juridiska personer måste konfigureras på sidan [Koncernintern redovisning](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup) i huvudboken.
    
    1. I Dynamics 365 Finance går du till **Huvudbok** > **Bokföringskonfiguration** > **Koncernintern redovisning**. Skapa en post med följande information:

        - **Ursprungsföretag** = **GBPM**
        - **Målföretag** = **USPM**

2. **Konfigurera handelsförhållandet mellan juridiska personer**. Kundposten som representerar den låntagande juridiska personen måste skapas i den långivande juridiska personen. Leverantörsposten som representerar den långivande juridiska personen måste skapas i den låntagande juridiska personen.

     1. I Finance väljer du den juridiska personen **GBPM**.
     2. Gå till **Kundreskontra** > **Kund** > **Alla kunder**. Skapa en ny post för den juridiska personen, **USPM**.
     3. Expandera **Namn**, filtrera posterna efter **Typ** och välj sedan **Juridiska personer**. 
     4. Sök efter och välj kundposten för **Contoso Robotics USA (USPM)**.
     5. Välj **Använd matchning**. 
     6. Markera kundgruppen och spara sedan posten.
     7. Välj den juridiska enheten **USPM**.
     8. Gå till **Leverantörsreskontra** > **Leverantörer** > **Alla leverantörer**. Skapa en ny post för den juridiska personen **GBPM**.
     9. Expandera **Namn**, filtrera posterna efter **Typ** och välj sedan **Juridiska personer**. 
     10. Sök efter och välj kundposten för **Contoso Robotics UK (GBPM)**.
     11. Välj **Använd matchning**, välj leverantörsgrupp och spara sedan posten.
     12. I leverantörsposten väljer du **Allmänt** > **Konfigurera** > **Koncernintern**.
     13. På fliken **Handelsrelation** anger du **Aktiv** som **Ja**.
     14. Välj leverantörsföretaget **GBPM**, under **Min kontopost** väljer du den kundpost som du skapade tidigare i proceduren.

3. **Konfigurera koncerninterna inställningar i Projektlednings- och redovisningsparametrar**. 

    1. Välj den juridiska personen **USPM** och gå till **Projektledning och redovisning** > **Konfiguration** > **Projektlednings- och redovisningsparametrar**.
    2. På fliken **Koncerninternt** väljer du den anskaffningskategori som ska matcha de leverantörsfakturor som genereras automatiskt.
    3. Under **Standardkategori** väljer du **Koncerninterna resurser**.
    4. Välj den juridiska personen **GBPM** och gå till **Projektledning och redovisning** > **Konfiguration** > **Projekthanterings- och redovisningsparametrar**.
    5. Under fliken **Koncerninternt** väljer du en standardprojektkategori för respektive transaktionstyp. Projektkategorier används för momskonfiguration när den fakturerade kategorin i koncerninterna transaktioner endast finns i den långivande juridiska personen. Du kan välja att periodisera intäkter för koncerninterna transaktioner. Periodisering sker när transaktionerna bokförs via integreringsjournalen för Project Operations i utlånande juridisk person. Journalen återställs när den koncerninterna fakturan bokförs.
    6. I gruppen **Vid utlåning av resurser** väljer du **...** > **Nytt**. 
    7. I rutnätet väljer du följande information:

          - **Låntagande juridisk person** = **GBPM**
          - **Periodisera intäkter** = **Ja**
          - **Standardkategori för tidrapport** = **Standard – Timme**
          - **Standardkategori för utgift** = **Standard – utgift**

4. **Ange koncerninterna kostnads- och intäktskonton i inställningarna för redovisningsbokföring**. Kontot för koncerninterna intäkter krediteras när fakturan Koncerninterna kunder bokförs i den utlånande juridiska personen. Kontot för koncerninterna intäkter debiteras när matchande, väntande leverantörsfaktura bokförs i den låntagande juridiska personen. Dessa konton ställs in i motsvarande juridiska personer. 
      
     1. I Finance väljer du den låntagande juridiska personen **USPM**. 
     2. Gå till **Projektledning och redovisning** > **Konfiguration** > **Bokföring** > **Inställningar för redovisningsbokföring**. 
     3. I fliken **Kostnadskonton**, under **Typ av huvudkonto** väljer du **Koncernintern kostnad**. Skapa en ny post med följande information:
      
        - **Utlånande juridisk person** = **GBPM**
        - **Huvudkonto** = Välj huvudkonto för koncernintern kostnad
        
     4. Välj den utlånande juridiska enheten **GBPM**. 
     5. Gå till **Projektledning och redovisning** > **Konfiguration** > **Bokföring** > **Inställningar för redovisningsbokföring**. 
     6. I fliken **Intäktskonton**, under **Typ av huvudkonto** väljer du **Koncernintern intäkt**. Skapa en ny post med följande information:

        - **Låntagande juridisk person** = **USPM**
        - **Huvudkonto** = Välj huvudkonto för koncernintern intäkt 

5. **Ställ in överföringsprissättning för arbete**. Koncernintern överföringsprissättning konfigureras i Project Operations för Dataverse. Konfigurera [arbetskostnadssatser](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) och [fakturataxor](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) för koncernintern fakturering. Överföringsprissättning stöds inte för koncerninterna utgiftstransaktioner. Försäljningspriset per enhet mellan organisationer kommer alltid att anges som samma värde som resursenhetens kostnadspris.

      Utvecklarresurskostnaden i Contoso Robotics UK är 88 GBP per timme. Contoso Robotics Storbritannien kommer att fakturera Contoso Robotics USA 120 USD för varje timme denna resurs arbetat med amerikanska projekt. Contoso Robotics USA kommer att fakturera kunden Adventure Works 200 USD för det arbete som utförs av Contoso Robotics brittiska utvecklarresurs.

      1. I Project Operations på Dataverse går du till **Försäljning** > **Prislistor**. Skapa en ny kostnadsprislista som heter **Kostnadstaxa för Contoso Robotics Storbritannien.** 
      2. Skapa en post med följande information i kostnadsprislistan:
         - **Roll** = **Utvecklare**
         - **Kostnad** = **88 GBP**
      3. Gå till **Inställningar** > **Organisationsenheter** och bifoga denna kostnadsprislista till organisationsenheten **Contoso Robotics Storbritannien**.
      4. Gå till **Försäljning** > **Prislistor**. Skapa en ny kostnadsprislista som heter **Kostnadstaxor för Contoso Robotics USA**. 
      5. Skapa en post med följande information i kostnadsprislistan:
          - **Roll** = **Utvecklare**
          - **Resursföretag** = **Contoso Robotics Storbritannien**
          - **Kostnad** = **120 USD**
      6. Gå till **Inställningar** > **Organisationsenheter** och bifoga kostnadsprislistan **Kostnadstaxa för Contoso Robotics USA** till organisationsenheten **Contoso Robotics USA**.
      7. Gå till **Försäljning** > **Prislistor**. Skapa en försäljningsprislista kallad **Fakturataxor för Adventure Works**. 
      8. Skapa en post med följande information i försäljningsprislistan:
          - **Roll** = **Utvecklare**
          - **Resursföretag** = **Contoso Robotics Storbritannien**
          - **Fakturataxa** = **200 USD**
      9. Gå till **Försäljning** > **Projektkontrakt** och bifoga **Fakturataxor för Adventure Works** till Adventure Works projektprislista för projektkontrakt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]