---
title: Hantera projektfakturaförslag
description: Detta ämne innehåller information om hur du bearbetar kundriktade fakturor med Project Operations för resurs- eller icke-lagerbaserade scenarier.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6b8eacf2b43219a9adad897637b78a9c94351554
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950736"
---
# <a name="manage-project-invoice-proposals"></a>Hantera projektfakturaförslag

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Projektfakturaförslag kan bearbetas av faktureringsavdelningen när följande två villkor uppfylls:

  - Projektledaren bekräftar proforma-fakturan i Microsoft Dataverse.
  - Alla icke-fakturerade försäljningstransaktioner med tid och material som ingår i proforma-fakturan bokförs med hjälp av Dynamics 365 **Project Operations Integration**-journalen.

Slutför ett projektfakturaförslag i enligt följande steg i Dynamics 365 Finance:

1. Läs faktureringsinformationen för tids- och materialtransaktioner och publicera **integrationsjournal för Project Operations**.
2. Granska faktureringsinformation för faktureringsmilstolpar med fast pris.
3. Granska och formatera ett projektfakturaförslag.
4. Bokför och skriv ut projektfakturor.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Hantera faktureringsinformation i integrationsjournal för Project Operations

Projektets faktiska resultat som skapas Dataverse granskas och publiceras i Finance av projektrevisorn. Mer information om arbete med integreringsjournalen finns i [Integreringsjournal i Project Operations](../project-accounting/project-operations-integration-journal.md).

Faktiska kostnader och icke-fakturerade faktiska kostnader läggs till som separata rader i integreringsjournalen:

  - Enhetskostnadspris och kostnadsbelopp i det faktiska standardkostnadsbeloppet från projektets faktiska kostnadstransaktion i Dataverse.
  - Enhetsförsäljningspriset och försäljningsbeloppet i standardvärdet för den icke-fakturerade försäljningstransaktionen från den faktiska icke-fakturerade försäljningstransaktionen i Dataverse.

### <a name="billing-sales-tax"></a>Faktureringsmoms

Momsberäkningen för fakturering fastställs av fältkombinationen **Fakturerings momsgrupp** och **Momsgrupp för faktureringsobjekt** på en ofakturerad försäljningspost på journalraden **Project Operations-integrering**. Standardvärdena för dessa fält baseras på inställningarna på fliken **Ekonomi** på sidan **Projekthanterings- och redovisningsparametrar**.

- **Metoden för momsgrupp** avgör standardlogiken för faktureringsmomsgrupp:
  
  - **Projekt:** Kommer alltid att återställa momsgruppen för fakturering från projektet. Du kan granska eller ändra momsgruppen för standardfakturering för ett projekt genom att välja **Visa standardredovisning** på sidan **Alla projekt**.
  - **Projektkontrakt**: Kommer alltid att återställa momsgruppen för fakturering från kontraktet. Du kan granska eller ändra momsgruppen för standardfakturering för ett kontrakt **Visa standardredovisning** på sidan **Projektkontrakt**.
  - **Kund**: Kommer alltid att återställa momsgruppen för fakturering från kunden.
  - **Sök:** Söker i alla ovanstående entiteter och väljer det första tillgängliga värdet. Sökningen startar med entiteten **Projekt**, därefter entiteten **Projektkontrakt**, och slutligen entiteten **Kund**.

- **Metod för artikelmomsgrupp** avgör standardlogiken för momsgrupp för faktureringsartikel.
  
  - För transaktionstyperna tid, utgift och avgift används alltid momsgruppen för faktureringsobjekt från entiteten för **projektkategori**.
  - För materialtransaktionstyper återställs standardvärden för faktureringsobjektets momsgrupp utifrån inställningen **Metod för artikelmomsgrupp** i **Projekthantering och redovisningsparametrar**. Artikelnumret återställer momsgruppen för artikelförsäljning från entiteten **Frisläppt produkt**. Kategorin återställer momsgruppen för artikelförsäljning från entiteten **Produktkategori**.

### <a name="financial-dimensions"></a>Ekonomiska dimensioner

De ekonomiska måtten för icke-fakturerade försäljningsposter i journalen **Project Operations-integrering** återställs från entiteten **Projekt**. Ekonomiska mått kan granskas och justeras genom att välja **Distribuera belopp**. Om du behöver ändra de ekonomiska måtten för den ofakturerade försäljningsposten efter integreringsfakturan har bokförts - men innan Proforma-fakturan har bekräftats - går du till **Alla projekt** > **Administrera** > **Bokförda transaktioner**, väljer transaktionen och sedan **Bearbeta** > **Justera redovisning**.

### <a name="exchange-rates"></a>Växelkurser

Icke-fakturerad transaktionsvaluta i Dataverse används som transaktionsvalita i Finance och konverteras till företagets redovisningsvaluta med hjälp av växelkurser som anges i Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Hantera ekonomiska attribut för faktureringsmilstolpar 

Projektkontraktrader med faktureringsmetoden med fast pris faktureras via [Milstolpar med fast pris](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Projektrevisorn kan granska faktureringsmilstolparna i Finance genom att gå till **Projekthantering och redovisning** > **Alla projekt** > **Hantera** > **Kontotransaktioner**.

### <a name="billing-sales-tax"></a>Faktureringsmoms

Värdena **Momsgrupp** och **Momsgrupp för artikelförsäljning** återställs till inställningsvärdena när en ny faktureringsmilstolpe skapas i Dataverse. Systemet återställer standardvärdena för dessa fält baserat på inställningarna i fliken **Ekonomi** på sidan **Projekthanterings- och redovisningsparametrar**.

- **Metoden för momsgrupp** avgör standardlogiken för **Momsgrupp för fakturering**:

    - **Projekt** Kommer alltid att återställa momsgruppen för fakturering från projektet. Du kan granska eller ändra momsgruppen för standardförsäljning för ett projekt genom att välja **Visa standardredovisning** på sidan **Alla projekt**.
    - **Projektkontrakt** kommer alltid att återställa momsgruppen för fakturering från kontraktet. Du kan granska eller ändra momsgruppen för standardförsäljning för ett kontrakt genom att välja **Visa standardredovisning** på sidan **Projektkontrakt**.
    - **Kund** kommer alltid att återställa till momsgruppen för fakturering från kunden.
    - **Sök** söker igenom alla entiteter i listan och väljer det första tillgängliga värdet. Sökningen startar med entiteten **Projekt**, därefter entiteten **Projektkontrakt**, och sedan entiteten **Kund**.

- **Artikelmomsgruppens fastprismilstolpe** används som standardvärde i fältet **Artikelmomsgrupp** för faktureringsmilstolpen. Redovisaren kan granska och modifiera värdet på sidan **Kontotransaktioner**. Systemet använder värdet från kontotransaktionen när en projektfakturaförslagsrad skapas.
 

### <a name="financial-dimensions"></a>Ekonomiska dimensioner

Standardekonomiska mått för faktureringsmilstolpen med fast pris anges på kontraktraderna för projekt. Gå till **Projektkontrakt** > **Visa standardredovisning** innan du under fliken **Kontraktrader**, **priskontraktrad** och anger sedan de finansiella dimensionsvärden som du vill använda som standard.

Projektrevisorn kan redigera informationen om moms och ekonomiska mått på fakturamilstolparna tills förslaget om projektfakturan har skapats.


## <a name="create-project-invoice-proposals"></a>Skapa projektfakturaförslag

Projektfakturaförslag kan granskas i modulen **Projekthantering och redovisning** genom att gå till **Projektfakturor** > **Projektfakturaförslag**.

Projektfakturaförslagets huvud skapas i Finance när Proforma-fakturan bekräftas i Dataverse. För enklare avstämning anger systemet projektfakturaförslagsnumret i Finance som samma nummer som Proforma-fakturans ID i Dataverse. Eftersom Proforma-fakturor inte nödvändigtvis behöver bekräftas i samma ordning som de skapas, måste projektfakturaförslagsnumret i Finance tillåta ändringar av lägre och högre värden. Konfigurera nummersekvenser enligt följande steg:

1. Gå till **Organisationsadministration** > **Nummersekvenser** > **Nummersekvenser** i Finance.
2. I filtret **Område** väljer du **Projekt**.
3. I filtret **Referens** väljer du **Fakturaförslag**.
4. Använd fältet **Företag** om du vill filtrera varje juridisk person med Dataverse-integrering för Project Operations aktiverad.
5. Öppna **Nummersekvensinformation** och ange på fliken **Allmänt**:

    - **Tillåt användarändringar: Till ett lägre tal** = **Ja**
    - **Tillåt användarändringar: Till ett högre tal** = **Ja**

Förslagsrader för projektfaktura läggs till av systemet med hjälp av den periodiska processen **Importera från mellanlagringstabell** (**Projekthantering och redovisning** > **Periodisk** > **Project Operations-integrering** > **Importera från mellanlagringstabell**). Denna process kan köras antingen manuellt eller genom att använda ett periodiskt schema. Systemet lägger inte till rader i fakturaförslagsdokumentet förrän alla rader är klara att faktureras. Tids- och materialtransaktioner är endast klara att faktureras när de har publicerats med **Project Operations Integration**-journalen.

## <a name="format-and-print-invoice-proposals"></a>Formatera och skriva ut projektfakturaförslag

Projektrevisorn kan anpassa en utskrift av projektfakturan med hjälp av sidan **Formatera fakturaförslag** och funktioner för utskriftshantering.

### <a name="format-invoice-proposals"></a>Formatera fakturaförslag

På sidan **Formatera fakturaförslag** kan anpassade grupperingstransaktioner visas i kundprojektfakturan.

1. På sidan **Projektfakturaförslag** väljer du **Skriv ut** > **Projektfakturaförslag**.
2. Välj **Ny** om du vill skapa en ny gruppering för utskriften av projektfakturan.
3. I fältet **Detaljer/sammanfattning** väljer du alternativ för denna gruppering:

    - Välj **Detaljer** om du vill skriva ut transaktionsinformationen för kundfakturan.
    - Välj **Sammanfattning** om du vill skriva ut transaktionssammanfattningen för kundfakturan.

> [!NOTE]
> Valet i fältet **Detaljer/sammanfattning** på sidan **Formatera fakturaförslag** åsidosätter det alternativ som valts i fältet **Fakturaformat** på sidan **Fakturaförslag** för utskrift av en detaljerad eller sammanfattad faktura.

- Markera de transaktionsrader som ska ingå i det här avsnittet på fliken **Tillgängliga transaktioner** och välj **Inkludera transaktioner** för att flytta dem till fliken **Valda transaktioner**.
- Välj **Flytta upp** och **Flytta ned** för att ändra ordningen på avsnitten.
- Välj **Förhandsgranska** om du vill förhandsgranska formaterad faktura.

### <a name="print-management"></a>Utskriftshantering

För utskriftshantering används olika rapportfiler för att skriva ut, ange mål och anpassa sidfotstext för fakturan. Utskriftshantering kan konfigureras på modulnivå, men inställningarna kan åsidosättas för en viss kund, ett visst kontrakt eller ett visst fakturaförslag. Om du vill få åtkomst till denna funktion går du till sidan **Projektfakturaförslag** och väljer **Skriv ut** > **Utskriftshantering**.

Utskriftshanteringskonfigurationen visas som en trädvy där varje nodnivå visar tillgängliga dokument att justera. Du kan tilldela anpassade utskrifter på dokumentnivån för modul, kund, kontrakt eller fakturaförslag. Om du vill ändra utskriften för det ursprungliga dokumentet expanderar du den önskade noden och väljer **Ursprunglig artikel**. I fältet **Rapportformat** väljer du det rapportformat som ska användas för utskrift. Du kan använda anpassade rapportformat med hjälp av [Ramverk för dokumenthantering för företag](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Bokför fakturaförslag

När fakturan har granskats och redigerats och fakturaförslagsraderna är tillfredsställande, kontrollerar du totalsummorna och momsen. I gruppen **Detaljer** väljer du **Totalsummor** och sedan **Bokför** för att bokföra fakturan.

Om du vill visa fakturan innan du bokför rensar du kryssrutan **Bokföra**. **Pro forma** skrivs ut på fakturan i syfte att märka den som en exempelfaktura. Markera kryssrutan **Skriv ut faktura** om du vill skriva ut fakturan.

Förutom sidan **Fakturaförslag** kan fakturaförslag även bokföras genom att köra det periodiska jobbet **Bokför fakturaförslag**. Om du vill hitta det här jobbet går du till **Projekthantering och redovisning** > **Periodisk** > **Projektfakturor** > **Bokför fakturaförslag**.

På den här sidan visas alla fakturaförslag som är klara att bokföras. Du kan schemalägga bokföringen av fakturaförslag genom att välja **Batch**. Ange **batchbearbetningsparametern** som **Ja** och ange upprepningen för batchbearbetning genom att välja **Återkommande**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
