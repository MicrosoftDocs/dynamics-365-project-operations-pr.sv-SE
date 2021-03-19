---
title: Koncernintern fakturering
description: Den här artikeln innehåller information och exempel på koncernintern fakturering för projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76eba87e7cc78dcc14510a8fb53677d626bf204f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270790"
---
# <a name="intercompany-invoicing"></a>Koncernintern fakturering

[!include [banner](../includes/banner.md)]

Den här artikeln innehåller information och exempel på koncernintern fakturering för projekt.

Organisationen kan ha flera avdelningar, dotterbolag och andra juridiska enheter som överför produkter och tjänster till varandra för projekt. Den juridiska personen som tillhandahåller tjänsten eller produkten kallas *långivande juridisk person* och den juridiska personen som tar emot tjänsten eller produkten kallas för *låntagande juridisk person*. 

Följande illustration visar ett typiskt scenario där två juridiska enheter, SI FR (den låntagande juridiska personen) och SI USA (den långivande juridiska personen) delar resurser för att leverera ett projekt för kund A. I det här scenariot kontrakteras SI FR för att leverera arbetet till kund A. 

[![Exempel koncernintern fakturering](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Målet är att göra kostnadskontrollen, intäktsredovisning, moms och överföringspris för koncerninterna projekttransaktioner mer flexibla och kraftfullt. Dessutom tillhandahålls följande funktioner:

-   Skapa kundfakturor för ett projekt i en låntagande juridisk person med hjälp av koncerninterna tidrapporter, utgifter och leverantörsfakturor i en långivande juridisk person.
-   Stöd momsberäkningar och indirekta kostnader.
-   Senarelägg intäktserkännandet i en långivande juridisk person och när en låntagande juridisk person bör känna igen kostnaden.
-   Periodisera resurser i arbete (PIA) i den långivande juridiska personen.
-   Ange överföringspriser som kan baseras på olika prismodeller. Här följer några exempel:
    -   **Kvantitet** – det belopp som du anger i fältet **Prissättning** är den faktiska kostnaden per kvantitet eller enhet.
    -   **Avgiftsbelopp** – priset/kostnaden per transaktion plus det avgiftsbelopp som du anger i fältet **prissättning**.
    -   **Avgiftsprocent** – överföringspriset är priset/kostnaden per transaktion multiplicerad med den avgiftsprocent som du anger i fältet **prissättning**.
    -   **Procent av försäljningspriset** – procentandelen av försäljningspriset som har överförts till den långivande juridiska personen.
    -   **Belopp under försäljningspris** – det belopp som den låntagande juridiska personen innehåller tillbaka från försäljningspriserna före överföring till den långivande juridiska personen.
    -   **Täckningsgrad** – det nummer du anger i fältet **prissättning** är täckningsgraden, uttryckt som en procentsats av försäljningspriset.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exempel 1: Ställ in parametrar för koncernintern fakturering
I det här exemplet är USSI en långivande juridisk person och dess resurser rapporterar tid till den låntagande juridiska personen FRSI som äger kontraktet med slutkunden. Timmar och utgifter som USSI personalrapport kan inkluderas i projektfakturan som FRSI genererar. Det finns dessutom en tredje källa med transaktioner som kan utgå från långivande juridiska personen (USSI i det här exemplet) när den tillhandahåller tjänster för delade leverantörer till dotterbolag (t.ex. FRSI) och sedan passerar kostnaderna för projekt inom dessa dotterbolag. Alla matchande fakturadokument och momsberäkningar slutförs efter Finance. 

I det här exemplet måste FRSI vara en kund i den USSI juridiska personen och USSI måste vara en leverantör i den FRSI juridiska personen. Du kan sedan konfigurera en koncernintern relation mellan de två juridiska enheterna. Nedan beskrivs en procedur för att ställa in parametrarna så att de juridiska enheterna kan delta i koncern intern fakturering.

1. Konfigurera FRSI som kund i den USSI juridiska personen och ställ in USSI som en leverantör i den FRSI juridiska personen. Det finns tre startpunkter för de steg som krävs för den här uppgiften.

   | Steg |                                                       Startpunkt                                                        |                                                                                                                                                                                               Beskrivning                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | I USSI, klicka på <strong>Fordringar</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alla kunder</strong>. |                                                                                                                                                                  Skapa en ny kundpost för FRSI och välj kundgruppen.                                                                                                                                                                  |
   |  F   |    I FRSI, klicka på <strong>Kundreskontra</strong> &gt; <strong>Leverantörer</strong> &gt; <strong>Alla leverantörer</strong>.     |                                                                                                                                                                    Skapa en ny leverantörspost för USSI och välj leverantörsgruppen.                                                                                                                                                                    |
   |  C   |                                  Öppna den leverantörspost som du precis skapade i FRSI.                                  | I åtgärdsfönstret på fliken <strong>Allmänt</strong> i gruppen <strong>Konfigurera</strong> klicka på <strong>Koncerninternt</strong>. På sidan <strong>Koncerninternt</strong> på fliken <strong>Handelsförhållande</strong> ange skjutreglaget <strong>Aktivera</strong> till <strong>Ja</strong>. I fältet <strong>Kundföretag</strong> väljer du kundposten du skapade i steg A. |


2. Klicka på **Parametrar för projekthantering och redovisning** &gt; **Konfiguration** &gt; **Projektledning och redovisningsparametrar** och klicka på fliken **Koncernintern**. Hur du anger parametrarna beror på om du är den låntagande juridiska personen eller den långivande juridiska personen.
   -   Om du är en låntagande juridisk person väljer du den anskaffningskategori som ska användas för att matcha leverantörsfakturorna som skapas automatiskt.
   -   Om du är långivande juridisk person väljer du en standardprojektkategori för varje låntagande enhet för varje transaktionstyp. Projektkategorier används för momskonfiguration när den fakturerade kategorin i koncerninterna transaktioner endast finns i den långivande juridiska personen. Du kan välja att periodisera intäkter för koncerninterna transaktioner. Den här periodiseringen sker när transaktionerna bokförs och sedan återförs när den koncerninterna fakturan bokförs.

3. Klicka på **projekthantering och bokföring** &gt; **inställningar** &gt; **priser** &gt; **överföringspris**.
4. Välj en valuta, en transaktionstyp och en prismodell för överföring. Valutan som används på fakturan är den valuta som är konfigurerad i kundposten för den låntagande juridiska personen i den långivande juridiska personen. Valutan används för att matcha poster i tabellen överföringspris.
5. Klicka på **Redovisning** &gt; **Bokföringsinställning** &gt; **Koncernintern redovisning** och ställ in en relation för USSI och FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exempel 2: Skapa och bokföra en koncernintern tidrapport
USSI, den långivande juridiska personen för utlåningen, måste skapa och bokföra tidrapporten för ett projekt från FRSI, den låntagande juridiska personen. Det finns två startpunkter för de steg som krävs för den här uppgiften.

| Steg | Startpunkt                                                                       | Beskrivning                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projekthantering och redovisning** &gt; **tidrapporter** &gt; **alla tidrapporter** | Skapa en ny tidrapport. På tidrapportraden för fältet **juridisk person** välj **FRSI**. I fältet **Projekt-ID**, välj projektet i FRSI. Ange timmarna för varje veckodag. |
| F    | Sidan **Tidrapport**                                                                | När arbetsflödet har körts bokför du tidrapporten och noterar verifikationsnumret.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exempel 3: Skapa och bokföra en koncernintern leverantörsfaktura
USSI, den långivande juridiska personen för utlåningen, måste skapa och bokföra koncernintern leverantörsfaktura för ett projekt från FRSI, den låntagande juridiska personen. Den här leverantörsfakturan visar de utlagda arbeten och kostnader som har utförts av leverantörer som har betalats av USSI. Det finns två startpunkter för de steg som krävs för den här uppgiften.

| Steg | Startpunkt                                                                                      | Beskrivning                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Leverantörsreskontra** &gt; **Fakturor** &gt; **Öppna leverantörsfakturor** &gt; **Ny leverantörsfaktura** | Skapa en ny leverantörsfaktura och ange de tjänster som har införskaffats på uppdrag av FRSI-projekt.                                                                                                                                                                                  |
| F    | Sidan **Leverantörsfaktura**                                                                      | Ange rader som representerar tjänster som har flyttats på uppdrag av FRSI. På snabbfliken **Raddetaljer** på fliken **Projekt** för fakturaraden **Projektföretag** anger du **FRSI**. Ange projektet och motsvarande information. Bokför sedan leverantörsfakturan. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exempel 4: Skapa och bokföra en koncernintern faktura
USSI, den långivande juridiska personen måste skapa och bokföra den koncerninterna fakturan. Det finns två startpunkter för de steg som krävs för den här uppgiften.

| Steg | Startpunkt                                                                                             | Beskrivning                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projekthantering och redovisning** &gt; **projektfakturor** &gt; **koncernintern kundfaktura**  | Klicka på **Ny** för att öppna sidan **Skapa koncernintern faktura**.                                                                                  |
| F    | **Projekthantering och redovisning** &gt; **projektfakturor** &gt; **koncernintern kundfakturor** | På sidan **Skapa koncernintern faktura** anger du den juridiska personen, anger den transaktion som ska tas med och klickar sedan på **Sök**. |
| C    | **Projekthantering och redovisning** &gt; **projektfakturor** &gt; **koncernintern kundfakturor** | Välj de transaktioner som ska faktureras eller klicka på **Markera alla** om du vill fakturera alla transaktioner i listan och klicka sedan på **OK**.                  |
| D    | Sidan **Koncernintern faktura**                                                                       | Det koncerninterna kundfaktura förslaget visas.                                                                                             |
| E    | Sidan **Koncernintern faktura**                                                                       | Klicka på **Publicera**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exempel 5: bokför leverantörsfakturan och fakturera kunden
När den långivande juridiska personen USSI bokför den koncerninterna kundfakturan, skapas en matchande pågående leverantörsfaktura i den låntagande juridiska personen FRSI. När leverantörsfakturan har bokförts fakturerar FRSI även projektkunden för de timmar som USSI anger. Det finns tre startpunkter för de steg som krävs för den här uppgiften.

| Steg | Startpunkt                                                                                        | Beskrivning                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Leverantörsreskontra** &gt; **Fakturor** &gt; **Väntande leverantörsfakturor**                            | Granska fakturan och kontrollera att tidrapportvärdena ingår och bokför sedan leverantörsfakturan.                  |
| F    | **Projekthantering och redovisning** &gt; **Projektfakturor** &gt; **Projektfakturaförslag** | Skapa en ny projektfaktura för projektet och kontrollera att de timtransaktioner som har bokförts visas.            |
| C    | Sidan **Projektfaktura**                                                                       | Välj projektfakturan och klicka sedan på **Visa detaljer** för att granska kostnaden och försäljningsbeloppet. Bokför sedan fakturan. |


Mer information finns i [Konfigurera en koncernintern projektfaktura](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]