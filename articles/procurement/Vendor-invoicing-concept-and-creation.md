---
title: Skapa leverantörsfakturor
description: I denna artikel beskrivs konceptet med leverantörsfakturor samt hur du skapar dem i Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475438"
---
# <a name="create-vendor-invoices"></a>Skapa leverantörsfakturor

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

För att kunna använda funktionen som beskrivs i den här artikeln måste du aktivera funktionen **Aktivera behandling av faktiska värden för underkontraktet med Project Operations för resursbaserade scenarier** i arbetsytan **Funktionshantering**.

Leverantörsfakturering i Microsoft Dynamics 365 Project Operations kan användas för att registrera kostnader från leveranser av tjänster och/eller material i ett projekt som slutförs av leverantörer.

När tjänster och/eller material läggs ut på entreprenad till en leverantör, representerar en underleverantör det kontraktsenliga avtalet med den leverantören. När leverantören levererar tjänsterna, eller när materialet tas emot och används i projektuppgifter, registreras kostnader för projektet. Leverantören skickar sedan regelbundet fakturor. Dessa fakturor verifieras och matchas med kostnader som registreras i projektet. När verifieringsprocessen är klar bekräftas leverantörsfakturan och frigörs för betalning.

## <a name="scenarios-for-use"></a>Användbara scenarier

Leverantörsfakturor i Project Operations kan användas för två olika scenarier:

- Kunderna använder de fullständiga underleverantörsupplevelserna.
- Kunderna använder inte alla underleverantörsupplevelser men vill ändå få en enhetlig bild av kostnaderna för projekt i Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunderna använder de fullständiga underleverantörsupplevelserna

Med hjälp av leverantörsfakturan kan du verifiera tidsposter, materialanvändning och utgiftsposter som refererar underleverantörskomponenter och matcha dem med leverantörsfakturarader. Den här processen kan användas för att kontrollera att leverantörsfakturaraderna är korrekta. När verifieringsprocessen har slutförts och leverantörsfakturan har verifierats, vänder systemet de faktiska värden som registrerats av godkända tids-, utgifts- och materialanvändningsloggar, och skapar sedan nya faktiska kostnader med hjälp av fakturaraderna för leverantör.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunderna använder inte alla underleverantörsupplevelser men vill ändå få en enhetlig bild av kostnaderna för projekt i Project Operations

Om du spårar underleverantörsprocessen i ett tredjepartssystem kan du registrera kostnader från det tredjepartssystemet till Project Operations genom att skapa leverantörsfakturor som inte refererar till underleverantörer. På så sätt kan dina projektansvariga få en enda, enhetlig bild av alla kostnader för ett visst projekt.

## <a name="create-vendor-invoices-in-project-operations"></a>Skapa leverantörsfakturor i Project Operations

Leverantörsfakturor skapas i Dynamics 365 Finance med hjälp av modulen **Leverantörsreskontra**. Det går inte att skapa leverantörsfakturor direkt i Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Ställ in leverantörsfakturaverifiering

Om leverantörsfakturan är avsedd för en underleverantör i Dataverse måste du aktivera parametern **Manuell verifieringen av PM krävs**. Inställningen av alternativet avgör om leverantörsfakturan ska bekräftas automatiskt eller i Dataverse eller om det krävs en manuell bekräftelse. I sidhuvudet för varje faktura för projektleverantörer finns ett alternativ med samma namn. Som standard är alternativet i sidhuvudet för alla projektleverantörsfakturor inställt på det värde du anger här. Du kan dock uppdatera värdet efter behov i sidhuvudet för enskilda leverantörsfakturor.

Om alternativet har angetts till **Ja** får leverantörsfakturan som skapas i Finance och synkroniseras till Dataverse statusen **Utkast**. Fakturan måste sedan valideras och verifieras av projektledaren och bekräftas innan den bearbetas och publiceras i det specifika projekt- och huvudbokskontot i Finance.

Om alternativet har angetts till **Nej** bekräftas leverantörsfakturan automatiskt. Inga ytterligare åtgärder krävs.

Så här ställer du in verifiering av leverantörsfakturor:

1. I Finance går du till **Projektledning och redovisning** \> **Konfiguration** \> **Parametrar för projektledning och redovisning**.
1. På fliken **Ekonomi** anger du alternativet **Manuell verifiering av PM krävs** till **Ja** om företagets policy kräver verifiering av fakturor för underleverantörer. Om det inte krävs någon verifiering av projektledaren i Dataverse låter du alternativuppsättning stå på **Nej**. Som standard används inställningen på sidan **Väntande leverantörsfaktura**.

> [!NOTE]
> Leverantörsfakturor som skapas för underleverantörskontrakt i Dataverse kan endast bearbetas korrekt om alternativet **Manuell verifiering av PM krävs** har ställts in på **Ja**. Faktiska värden för tid, material och utgifter som underleverantörer skapar kan matchas manuellt med leverantörersfakturarader av projektledaren endast om alternativet har ställts in på **Ja**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Ställ in ett inköpsintegrationskonto för leverantörsfakturor

När en leverantörsfaktura har lagts upp i Finance för Project Operations-integrerad miljö (icke-lager) publiceras ekonomi till integrationskontot Inköp. I systemet genereras faktiska värden i Dataverse för den upplagda fakturan. Dessa faktiska värden publiceras i Finance med hjälp av projektintegreringsjournalen. Om du publicerar projektintegreringsjournalen publiceras den faktiska kostnaden och integrationskontot Inköp återställs.

Följ dessa steg för att konfigurera integrationskontot Inköp för leverantörsfakturor.

1. I Finance går du till **Projektledning och redovisning** \> **Konfiguration** \> **Parametrar för projektledning och redovisning**.
1. På fliken **Project Operations på Dynamics 365 Customer Engagement** väljer du **Material** \> **Integrationskontot Inköp**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Skapa och publicera underleverantörsfakturor

När en ansvarig för leverantörsreskontra får en faktura från underleverantören skapas en ny faktura i Finance.

1. I Finance går du till **Leverantörsreskontra** \> **Fakturor** \> **Väntande leverantörsfakturor**.
1. I **åtgärdsfönstret** väljer du **Nytt** för att skapa en leverantörsfaktura.
1. I fakturasidhuvudet går du till fältet **Fakturakonto** och väljer **Underleverantör**.
1. Välj fakturadatum.
1. På fliken **Rubrik** ställer du in alternativet **Manuell verifiering av PM krävs** på **Ja**. Standardinställningen för det här alternativet kommer från sidan **Parametrar för projekthantering och redovisning**. Den kan dock ändras på leverantörsfakturanivå.
1. Under snabbfliken **Fakturarad** väljer du **Lägg till rad** för att skapa en leverantörsfakturarad.
1. Välj den inköpskategori som har skapats för underleverantörskontraktrad och ange enhetspris, måttenhet och kvantitet.
1. I avsnittet med leverantörsfakturarader under fliken **Projekt** väljer du det projekt som underleverantören delar underleverantörsfakturan mot.
1. Välj projektkategori. Det kan vara någon av typerna **Objekt**, **Utgifter**, **Material** eller **Timmar**.
1. Välj rollen endast om den valda projektkategorin är av typen **Timme**.
1. Välj **Bokför** för att bokföra leverantörsfakturan.

Du kan också skapa en leverantörsfaktura genom att gå till **Leverantörsreskontra** \> **Fakturor** \> **Öppna leverantörsfakturor** och välja **Nytt**.

När leverantörsfakturan har lagts upp blir den tillgänglig i Dataverse för verifiering och bearbetning av projektledare.

## <a name="vendor-invoice-processing-in-dataverse"></a>Bearbetning av leverantörsfaktura i Dataverse

I leverantörsfakturan som skapas i Dataverse kommer vissa fältvärden från leverantörsfakturan som är registrerad i Finance. Andra värden är standardvärden som kommer från underleverantörskontraktet.

Följande fält och relaterade poster kopieras från underleverantörskontraktet till sidhuvudet på leverantörsfakturan:

- Valuta
- Kontrakteringsenhet
- Betalningsvillkor

På leverantörsfakturaraderna använder Project Operations följande fältvärden för att ange standardreferensen för underleverantör och underleverantörsrad:

- Transaktionsklass
- Roll
- Transaktionskategori
- Produktfält
- Project
- Aktivitet

> [!NOTE]
> Underleverantörsrader med fast pris stöds inte i Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
