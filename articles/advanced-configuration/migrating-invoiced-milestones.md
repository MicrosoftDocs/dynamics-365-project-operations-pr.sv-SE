---
title: Migrera helfakturerade faktureringsmilstolpar vid övergång
description: I denna artikel finns information om hur du migrerar faktureringsmilstolpar med fast pris som har fakturerats till kunden för öppna projektkontrakt före publiceringsdatum.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028724"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrera helfakturerade faktureringsmilstolpar vid övergång

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

## <a name="scenario"></a>Scenario

Contoso använder Microsoft Dynamics 365 Project Operations för publicering av resurs-/icke-lagerbaserade scenarier. Implementeringsteamet måste migrera öppna projektkontrakt från det gamla systemet som en del av övergångsaktiviteterna. Några av projektkontrakten innehåller kontraktrader som använder faktureringsmetod med fastpris och som redan delvis har fakturerats till slutkunden. Implementeringsteamet måste migrera dessa faktureringsmilstolpar som **Bokförda kundfakturor**, detta eftersom de måste ingå i det totala kontraktvärdet för intäktsidentifiering. Kundsaldon i kundreskontra och redovisning får emellertid inte påverkas.

## <a name="solution"></a>Lösning

### <a name="prerequisites"></a>Förutsättningar

- Dynamics 365 Finance 10.0.24 eller senare måste installeras.
- Miljön där migreringsstegen ska slutföras måste vara i underhållsläge. Inga andra aktiviteter ska utföras när milstolpen migreras.
- Migreringsstegen måste följas exakt så som det beskrivs här och kan endast användas för övergångsaktiviteten. Microsoft stöder ingen annan användning av den här funktionen.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Skapa en övergångsversion av kontraktradsmilstolparna för integrering av Project Operations med dubbelskrivning 

1. Se till att målmappningen för entiteten **Project Operations-integrering för milstolpar för kontraktrad** är uppdaterad. 

    1. I Finance går du till **Datahantering** \> **Dataentiteter** och väljer entiteten **Project Operations-integrering för milstolpar för kontraktrad**. 
    2. Välj **Ändra målmappningar**. 
    3. På sidan **Mappa mellanlagring till mål** väljer du **Generera mappning** och bekräftar sedan att du vill generera mappningen.

2. Stoppa och uppdatra mappningen **Project Operations integration contract line** (**msdyn\_contractlinescheduleofvalues**) med dubbelskrivning. 

    1. Gå till **Datahantering** \> **Dubbelskrivning**, markera mappningen och öppna informationen. 
    2. Välj **Stoppa** och vänta tills kartan stoppas av systemet. 
    3. Välj **Uppdatera tabeller**.

3. Lägg till en mappning för transaktionsstatusen.

    1. Välj **Lägg till mappning**.
    2. I kolumnen **Appar för ekonomi och drift** markerar du fältet **TRANSSTATUS \[TRANSSTATUS\]**.
    3. I kolumnen **Microsoft Dataverse** väljer du **msdyn\_invoicestatus \[Fakturastatus\]**.
    4. I kolumnen **Mappningstyp** väljer du högeprilen (**\>**).
    5. I dialogrutan som visas, i fältet **Synkroniseringsriktning**, väljer du **Dataverse till appar för ekonomi och drift**.
    6. Välj **Lägg till transformering**.
    7. I fältet **Transformeringstyp** väljer du **ValueMap**.
    8. Markera **Lägg till värdemappning**.
    9. I vänster fält anger du **4**. I höger fält anger du **192350001**. 
    10. Välj **Spara** och stäng sedan dialogrutan.

4. Välj **Spara som** om du vill spara versionen av mappningen med dubbel skrivning. 
5. I rutan **Lägg till tabell**, i fältet **Utgivare**, väljer du **Standardutgivare**.
6. I fältet **Version** anger du versionen.
7. I fältet **Beskrivning** skriver du en anteckning om denna övergångsversion för mappningen. 
8. Välj **Spara**.
9. Starta mappningen.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrera fakturerade milstolpar till Dataverse-miljön

1. I Project Operations Dataverse-miljön skapar du milstolpar med fakturastatusen **Redo att fakturera**. Vid denna tidpunkt ska du inte migrera milstolpar som inte har fakturerats.

    > [!NOTE]
    > Innan du migrerar faktureringsmilstolparna bör du kontrollera att de ekonomiska måtten som är relaterade till projektkontraktraden är inställda som förväntat. Ekonomiska mått kan inte redigeras efter migreringen.

2. När alla milstolpar har migrerats stoppar du följande mappningar med dubbel skrivning:

    - Kontraktsradmilstolpar för Project Operations-integrering (msdyn\_contractlinescheduleofvalues)
    - Project Operations-integration av faktiska värden (msdyn\_actuals)
    - Projektfakturaförslag version 2 (fakturor)

    Följ stegen nedan för att stoppa mappningarna:

    1. I Finance går du till **Datahantering** \> **Dubbelskrivning**, markerar en mappning och öppnar sedan informationen.
    2. Välj **Stoppa** och vänta tills systemet stoppar mappningen.

3. Skapa och bekräfta pro forma-fakturor i Dataverse-miljön för Project Operations. 

    1. I webbplatsöversikten går du till projektkontrakten, väljer kontrakten och sedan **Skapa fakturor**.
    2. När fakturorna har skapats öppnar du dem från menyn **Fakturor** i webbplatsöversikten och väljer **Bekräfta**.

    I detta steg skapas de obligatoriska posterna i Dataverse-miljön. Detta påverkar emellertid inte ekonomi och kundreskontra, detta eftersom tidigare listade mappningar med dubbelskrivning stoppades.

4. När alla proforma-fakturor har bekräftats återför du alla mappningar med dubbelskrivning till deras ursprungliga tillstånd.

    1. Uppdatera versionen av mappningen **Kontraktsradmilstolpar för Project Operations-integrering** (**msdyn\_contractlinescheduleofvalues**) med dubbelskrivning tillbaka till ursprungsversionen. 
    2. Markera mappningen med dubbelskrivning i mappningslistan, välj **Tabellmappningsversion** och välj sedan den ursprungliga versionen av tabellmappningen.
    3. Välj **Spara**.
    4. Starta om följande mappningar med dubbelskrivning:

        - Kontraktsradmilstolpar för Project Operations-integrering (msdyn\_contractlinescheduleofvalues)
        - Project Operations-integration av faktiska värden (msdyn\_actuals)
        - Projektfakturaförslag version 2 (fakturor)

Nu migreras milstolparna, och systemet är redo för nästa steg i den övergångsaktiviteten.
