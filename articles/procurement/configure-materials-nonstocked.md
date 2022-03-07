---
title: Konfigurera icke-lagerbaserade material och väntande leverantörsfakturor
description: I ämnet beskrivs hur du aktiverar icke-lagerbaserade material och väntande leverantörsfakturor.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003253"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurera icke-lagerbaserade material och väntande leverantörsfakturor

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

## <a name="minimum-version-requirement"></a>Lägsta version som krävs

För användning av icke-lagerbaserade material och väntande leverantörsfakturor för Dynamics 365 Project Operations icke-lagerbaserade/resursbaserade scenarier krävs följande versioner:

Dynamics 365 Dataverse-lösningar:

- Project Operations – 4.9.0.221 eller högre
- Lösning med dubbelriktad skrivning av programorkestrering – 2.2.2.23 eller senare

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) eller senare. Kontrollera att ekonomimiljön är aktuell och att alla kvalitetsuppdateringar tillämpas för att uppfylla minimiversionskraven.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Kör dubbelriktad skrivningsmappningar för icke-lagerbaserade material och integration med leverantörsfaktura

Det här avsnittet innehåller information om specifika mappningar som krävs för icke-lagerbaserade material och leverantörsfakturor. Kontrollera att de nödvändiga mappningar som finns i avsnittet [Etablera en ny miljö](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) körs i din miljö.

1. Gå till Lifecycle Services (LCS), navigera till ditt LCS-projekt och gå till sidan **Miljöinformation**.
2. I avsnittet **Common Data Service miljöinformation** väljer du **Länka till CDS for Apps**. När du har valt länken dirigeras du om till listan över entiteter i mappningarna.
3. Kontrollera att följande mappningar körs. Om de inte körs startar du dem och ser till att alla relaterade tabellmappningar inkluderas.

    - CDS har gett ut olika produkter (produkter)
    - Leverantörer v2 (msdyn_vendors)
    - Tabellen Project Operations för att föra fram material (msdyn_estimatelines)
    - Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices)
    - Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn_projectvendorinvoicelines)
    - Faktiska värden för Project Operations-integration (msdyn_actuals). Kontrollera att du kör mappningsversion 1.0.0.14 eller senare. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du kan aktivera en ny version av mappningen genom att välja **Tabellmappningsversion** och sedan spara den valda versionen.

Om du använder standarddemodata kan du också behöva stoppa och starta om följande entitetsmappningar med inledande synkning:
  - Betalningsdagar CDS V2 (msdyn_paymentdays)
  - Betalningsplan (msdyn_paymentschedules)
  - Betalningsvillkor (msdyn_paymentterms)
  - Leverantörsgrupper (msdyn_vendorgroups)
  - Enheter (uom)

> [!NOTE]
> Den första synkningen för leverantörsgrupper och enheter kan misslyckas för en del poster i den befintliga demodatauppsättningen. Du kan ignorera felen eftersom de inte hindrar dig från att använda demodata med Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurera krav i Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivera arbetsflöde för att skapa konton baserat på leverantörsentitet

Lösningen dubbelriktad skrivningsorkestrering ger [Masterintegration av leverantörer](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Som en förutsättning för den här funktionen måste leverantörsdata skapas i entiteten **Konton**. Aktivera en mall för arbetsflödesprocess för att skapa leverantörer i tabellen **Konton** enligt beskrivningen i [Växla mellan leverantörsdesigner](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Ange produkter som ska skapas som aktiva

Icke-lagerbaserade material måste konfigureras som **Släppta produkter** i Ekonomi. Lösningen dubbelriktad skrivningsorkestrering ger en helt ny [Integration av släppta produkter i Dataverse produktkatalog](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Som standard synkroniseras produkter från Ekonomi till Dataverse som utkast. För att synkronisera produkten med ett aktivt tillstånd så att den kan användas direkt i materialförbrukningsdokument eller väntande leverantörsfakturor går du till **System** > **Administration** > **Systemadministration** > **Systeminställningar** och på fliken **Försäljningar** ställer du in **Skapa produkter i aktivt tillstånd** som **Ja**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurera krav i Ekonomi

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Aktivera funktionsnyckeln för väntande leverantörsfakturor

Slutför följande steg för att aktivera funktioner för att lägga till projektinformation på rader i väntande leverantörsfakturor.

1. Gå till arbetsytan **Funktionshantering** i Ekonomi.
2. I funktionslistan söker du reda på funktionen **Aktivera väntande leverantörsfakturor i Project Operations för resursbaserade/icke-lagerbaserade scenarier** och väljer **Aktivera**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definiera kategorigrupper och projektkategorier för objekt

Konfigurera minst en kategorigrupp för transaktionstypen **Artikel** och minst en projektkategori med den här gruppen. Mer information finns i [Konfigurera projektkategorier](../project-accounting/configure-project-categories.md#category-groups).

Granska projektkostnads- och intäktsprofilerna och konfigurera inställning för huvudboksregistrering av artikeltransaktioner. Mer information finns i [Konfigurera redovisning av fakturerbara projekt](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Ställ in en oregistrerad produkt

I Project Operations kan du registrera materialberäkningar och förbrukning för katalogprodukter som har konfigurerats i den släppta produktkatalogen och för oregistrerade produkter. För användning av oregistrerade produkter krävs en enskild produkt som har konfigurerats i Ekonomi för detta ändamål. Konfigurera en oregistrerad produkt genom att följa stegen nedan. Upprepa dessa steg för samtliga juridiska entiteter som använder Project Operations för resurs/icke-lagerbaserade scenarier.

1. I Ekonomi går du till **Produktinformationshantering** > **Produkter** > **Släppta produkter** och väljer **Ny**.
2. I fältet **Produkttyp** väljer du **Artikel** och i fältet **Produktundertyp** väljer du **Produkt**.
3. Ange produktnumret (WRITEIN) och produktnamnet (Oregistrerad produkt).
4. Välj artikelmodellgrupp. Kontrollera att artikelmodellgruppen du väljer har fältet **Lagerpolicy produkt i lager** inställt på **False**.
5. Välj värden i fälten **Artikelgrupp**, **Lagerdimensionsgrupp** och **Spårningsdimensionsgrupp**. Använd **Lagringsplatsen** för **Webbplats** och i fältet **Spårningsmått**, välj **Inga**.
6. Välj värden i fältet **Lagerenhet**, **Inköpsenhet** och **Försäljningsenhet** och spara sedan ändringarna.
7. Ange standardorderinställningar på fliken **Plan** och ange standardplats och distributionslager på fliken **Lager**.
8. Gå till **Projektledning och redovisning** > **Inställning** > **Projekthanterings- och redovisningsparametrar** och öppna **Project Operations i Dynamics 365 Dataverse**. 
9. Välj den produkt du skapat på fliken **Material** i fältet **Oregistrerad produkt**.
10. I miljön Dataverse öppnar du entiteten **Produkter** på webbplatsöversikten och söker reda på posten för den oregistrerade produkten. 
11. Öppna postinformationen och ange produkttillstånd som **Tillbakadragen**. Produkttillståndet förhindrar att någon använder posten av misstag direkt i materialberäkningar och förbrukningsdokument.

### <a name="set-up-a-procurement-integration-account"></a>Ställ in ett inköpsintegrationskonto

Inköpsintegrationskontot används som rensningskonto när en väntande leverantörsfaktura registreras med rader kopplade till ett projekt.

När systemet registrerar en väntande leverantörsfaktura används det här kontot för projektkostnadsbeloppet. Leverantörsfakturainformationen bearbetas i Dataverse och ett motsvarande projektvärde skapas. Informationen från projektvärdet läggs till i Project Operations integrationsjournal. När du registrerar integrationsjournalen rensas beloppet från inköpsintegrationskontot och registreras på projektkostnaden.

1. För att ställa in inköpsintegrationskontot ska du gå till **Projektledning och redovisning** > **Inställning** > **Projekthanterings- och redovisningsparametrar** och öppna **Project Operations i Dynamics 365 Dataverse**. 
2. Välj fliken **Material** och välj ett värde i fältet **Inköpsintegrationskonto**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Ange standard för projektkategori för en artikel

1. I Ekonomi ska du gå till **Projektledning och redovisning** > **Inställning** > **Projekthanterings- och redovisningsparametrar** och öppna **Project Operations i Dynamics 365 Dataverse**. 
2. På fliken **Standardprojektkategori** väljer du ett värde i fältet **Artikel**. Den här projektkategorin används för materialtransaktioner om projektkategorin inte ställts in i posten projektvärde.
