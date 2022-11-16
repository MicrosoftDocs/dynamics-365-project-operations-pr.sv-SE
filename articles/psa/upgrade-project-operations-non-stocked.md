---
title: Uppgradera från Project Service Automation till Project Operations
description: I denna artikel finns en översikt över processen för att uppgradera från Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736689"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Uppgradera från Project Service Automation till Project Operations

Vi är glada över att kunna presentera den andra av tre faser för uppgradering från Microsoft Dynamics 365 Project Service Automation till Microsoft Dynamics 365 Project Operations. Denna artikel ger en översikt för kunder som tar del av denna intressanta resa. 

Uppgraderingsleveransprogrammet delas upp i tre faser.

| Uppgraderingsleverans | Fas 1 (januari 2022) | Fas 2 (november 2022) | Fas 3 (aprils utgivningscykel 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Inget beroende av uppdelad arbetsstruktur (WBS) för projekt | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS inom de gränser som för närvarande stöds för Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| WBS utanför de för närvarande stödda begränsningarna för Project Operations, inklusive stöd för Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funktioner för uppgraderingsprocessen 

Som en del av uppgraderingsprocessen har vi lagt till uppgraderingsloggar till webbplatsöversikten, så att administratörer enklare kan diagnostisera fel. Förutom det nya gränssnittet läggs nya valideringsregler till för att säkerställa dataintegriteten efter en uppgradering. Följande valideringar läggs till i uppgraderingsprocessen.

| Valideringar | Fas 1 (januari 2022) | Fas 2 (november 2022) | Fas 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS valideras mot vanliga dataintegritetsöverträdelser (till exempel resurstilldelningar som är associerade till samma överordnade uppgift men som har olika överordnade projekt). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideras mot de [kända gränserna för Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS valideras mot de kända gränserna för Project Desktop Client. | |  | :heavy_check_mark: |
| Bokningsbara resurser och projektkalendern utvärderas mot undantag av vanliga inkompatibla kalenderregler. | | :heavy_check_mark: | :heavy_check_mark: |

I fas 2 får de kunder som uppgraderar Project Operations sina befintliga projekt uppgraderade till en skrivskyddad upplevelse av projektplaneringen. I den här skrivskyddade upplevelsen visas hela WBS i spårningsrutnätet. Om projektledare vill redigera WBS kan de välja [**Konvertera**](/PSA-Upgrade-Project-Conversion.md) på projektets huvudsida. En bakgrundsprocess uppdaterar sedan projektet så att det stöder den nya projektschemaläggningsupplevelsen från Project for the Web. Den här fasen är lämplig för kunder som har projekt som passar inom de [kända begränsningarna för Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

I fas 3 läggs stöd för Project Desktop Client till, till nytta för kunder som vill fortsätta redigera sina projekt från det programmet. Om befintliga projekt däremot konverteras till den nya Project for the Web-upplevelsen inaktiveras åtkomsten till tillägget för varje konverterat projekt.

## <a name="prerequisites"></a>Förutsättningar

Du måste uppfylla följande villkor för att kunna uppgradera fas 1:

- Målmiljön får inte innehålla några poster i entiteten **msdyn_projecttask**.
- Giltiga Project Operations-licenser måste tilldelas till alla aktiva användare. 
- Kunden måste verifiera uppgraderingsprocessen i minst en icke-produktionsmiljö som har en representativ datauppsättning som är justerad mot produktionsmiljö.
- Målmiljön måste uppdateras till version 37 (V3.10.58.120) eller senare av Project Service Automation.

Du måste uppfylla följande villkor för att kunna uppgradera fas 2:

- Giltiga Project Operations-licenser måste tilldelas till alla aktiva användare. 
- Kunden måste verifiera uppgraderingsprocessen i minst en icke-produktionsmiljö som har en representativ datauppsättning som är justerad mot produktionsmiljö.
- Målmiljön måste uppdateras till version 37 (V3.10.58.120) eller senare av Project Service Automation.
- Miljöer som innehåller uppgifter (msdyn_projecttask) stöds endast om det totala antalet uppgifter per projekt är 500 eller färre.

Krav för fas 3 uppdateras när datumet för den allmänna tillgängligheten närmar sig.

## <a name="licensing"></a>Licensiering

Om du har aktiva licenser för Project Service Automation kan du installera och använda Project Operations, som omfattar alla funktioner inom Project Service Automation med mera. På så sätt kan du testa funktionerna i Project Operations medan du fortsätter att använda Project Service Automation i produktion. När dina licenser för Project Service Automation har upphört måste du övergå till Project Operations. När du planerar övergången måste du ta hänsyn till att licensen för Project Operations inte innehåller någon licens för Project Service Automation. Kunder som har scenarier där de har distribuerat Project Service Automation och behöver fortsätta att använda eller öka licenserna för PSA medan de planerar att flytta till Project Operations, kan begära tillfälliga PSA-licenser baserade på Project Operations köpta licenser. En licens för Project Service Automation utfärdas för en Project Operations-licens. Tillfälliga PSA-licenser kan begäras via den här länken: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testa och återanvända anpassningar

Börja med att importera alla anpassningar till en ren Project Operations (Lite)-miljö för att bekräfta att importen har lyckats och att affärsåtgärderna fungerar som förväntat.

Här är några saker du bör hålla utkik efter:

- Importen kan misslyckas på grund av saknade beroenden. Anpassningsreferensfälten eller andra komponenter som har tagits bort i Project Operations. I det här fallet tar du bort dessa beroenden från utvecklingsmiljön.
- Om dina ohanterade och hanterade lösningar innehåller komponenter som inte har anpassats tar du bort dessa komponenter från lösningen. När du anpassar entiteten **Projekt** lägger du endast till entitetshuvudet till lösningen. Lägg inte till alla fält. Om du tidigare har lagt till alla underkomponenter kan du behöva skapa en ny lösning manuellt och lägga till relevanta komponenter i den.
- Formulär och vyer kanske inte visas som förväntat. Under vissa omständigheter kan anpassningarna förhindra att nya uppdateringar i Project Operations genomförs om du har anpassat något av de färdiga formulären eller vyerna. Om du vill identifiera de här problemen rekommenderar vi att du gör en översiktsgranskning av en ren installation av Project Operations och en installation av Project Operations som omfattar dina anpassningar. Jämför de formulär som används mest i företaget för att bekräfta att din version av formuläret fortfarande är meningsfull och inte saknar någonting från den rena versionen av formuläret. Gör samma typ av granskning sida vid sida för alla vyer som du har anpassat.
- Affärslogiken kan misslyckas vid körning. Eftersom referenser till fält i plugin-program inte verifieras vid tidpunkten för importen kanske affärslogiken misslyckas på grund av referenser till fält som inte längre finns och du kan få ett felmeddelande som liknar följande exempel: "Projekt"-entiteten innehåller inte attributet med namn = "msdyn_plannedhours" och NameMapping = "Logisk". I det här fallet ändrar du anpassningarna så att de använder de nya fälten. Om du använder automatiskt skapade proxyklasser och starka typreferenser i plugin-logiken bör du överväga att återskapa de här proxyservrarna från en ren installation. På så sätt kan du enkelt identifiera alla platser där plugin-program är beroende av inaktuella fält.

När du har uppdaterat anpassningarna för att rent importera Project Operations går du vidare till nästa steg.

## <a name="end-to-end-testing-in-development-environments"></a>Heltäckande testning i utvecklingsmiljöer

### <a name="initiate-upgrade"></a>Påbörja uppgradering 

1. I Power Platform-administrationscentret letar du upp och väljer din miljö. I programfältet letar du sedan upp och väljer **Dynamics 365 Project Operations**.
2. Välj **Installera** för att starta uppgraderingen. I Power Platform-administrationscentret presenteras den här installationen som en ny installation. En tidigare version av Project Service Automation identifieras dock och den befintliga installationen uppgraderas.

    När uppgraderingen är klar ska miljön visa att Project Operations är installerat och att Project Service Automation inte har installerats.

    Beroende på mängden data i miljön kan uppgraderingen ta flera timmar. Kärnteamet som hanterar uppgraderingen ska planera och köra uppgraderingen under andra tider än arbetstiden. I vissa fall, om datavolymen är stor, bör uppgraderingen köras under veckoslutet. Beslutet om schemaläggning ska grundas på testresultaten i lägre miljöer.

3. Uppgradera anpassade lösningar efter behov. Nu ska du distribuera alla ändringar du gjort i anpassningarna i avsnittet [Testa och återanvända anpassningar](#testing-and-refactoring-customizations) i denna artikel.
4. Gå till **make.powerapps.com**, välj din miljö i listrutan längst upp till höger på portalen, välj **Lösningar** från den vänstra menyn, välj **Project Operations inaktuella komponenter** och **Avinstallera**.

    Den här lösningen är en tillfällig lösning som innehåller den befintliga datamodellen och de befintliga komponenterna under uppgraderingen. Genom att ta bort lösningen tar du bort alla fält och komponenter som inte längre används. På det här sättet förenklar du gränssnittet och gör integreringen och tillägget enklare.
    
### <a name="upgrade-to-project-operations-lite"></a>Uppgradera till Project Operations Lite

I följande steg beskrivs uppgraderingsprocessen och associerad felloggning:

1. **PSA-versionskontroll:** Om du vill installera Project Operations måste du ha V3.10.58.120 eller högre.
1. **Förvalidering:** När en administratör påbörjar en uppgradering körs en förvalideringsåtgärd för varje entitet som är central i lösningen Project Operations. Det här steget verifierar att alla entitetsreferenser är giltiga, och det säkerställer att data som är relaterade till WBS ligger inom de publicerade gränserna för Project for the Web.
1. **Metadatauppgradering:** När förvalideringen har lyckats initierar systemet ändringar i schemat och skapar en inaktuell komponentlösning. Du kan ta bort den här inaktuella lösningen när du har slutfört alla nödvändiga anpassningar. Det här steget är den längsta delen av uppgraderingsprocessen och kan ta upp till fyra timmar att slutföra.
1. **Datauppgradering:** När alla obligatoriska schemaändringar har slutförts i uppgraderingssteget för metadata migreras dina data till det nya schemat och eventuella obligatoriska standardändringar och omberäkningar utförs.
1. **Uppdatering av projektschemamotor:** När datauppgraderingen har lyckats visas fliken **Schema** på huvudsidan med namnet **Uppgifter**. När en användare väljer den här fliken efter uppgraderingen uppmanas de att navigera till spårningsrutnätet för att se en skrivskyddad version av WBS. För att redigera WBS måste de initiera schemat [konverteringsprocessen](/PSA-Upgrade-Project-Conversion.md). Alla projekt utan en redan existerande WBS kan använda den nya schemaläggningsupplevelsen direkt, utan konvertering.
 
### <a name="validate-common-scenarios"></a>Validera vanliga scenarier

När du validerar specifika anpassningar rekommenderar vi att du även granskar de affärsprocesser som stöds i alla program. Dessa affärsprocesser omfattar, men är inte begränsade till, skapandet av försäljningsentiteter som offerter och kontrakt, samt generering av projekt som omfattar WBS och godkännande av faktiska värden.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Stora förändringar mellan Project Service Automation och Project Operations

Det här avsnittet innehåller en sammanfattning av de viktigaste förändringarna mellan Project Service Automation och Project Operations.

### <a name="project-planning"></a>Projektplanering

Projektplaneringsfunktionerna i Project Operations bygger inte längre på en kombination av klientlogik och serverlogik. Istället använder Project Operations Project for the Web som schemaläggningsmotor. Den här förändringen av schemaläggningsfunktionerna möjliggör flera nya funktioner, t.ex. vyer för schemaläggningstavla och Gantt, resursbaserad planering, [punkter i uppgiftslistan](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) och lägen för projektschemaläggning. De nya schemaläggningsfunktionerna stöds också av en mängd nya [programmeringsgränssnitt (API:er)](../project-management/schedule-api-preview.md). Dessa API:er är avsedda att hjälpa till att säkerställa att inga programmatiska åtgärder för att skapa, uppdatera eller ta bort en entitet i WBS korrumperar de beräknade fälten i schemat.

### <a name="billing-and-pricing"></a>Fakturering och prissättning

Som en del av de fortlöpande investeringarna i Project Operations finns flera nya funktioner tillgängliga inom fakturering och prissättning. Här följer några exempel:

- [Registrera materialanvändning för projekt och projektuppgifter](../material/material-usage-log.md)
- [Underleverantörshantering](../pro/subcontracting/managing-subcontracts-overview.md)
- [Förskott och arvodesbaserade kontrakt](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontrakts undre status och valideringar](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Uppgiftsbaserad fakturering

### <a name="resource-management"></a>Resurshantering

Project Operations tillhandahåller valfritt stöd för Universal Resource Scheduling (URS) tavla och schemaläggningsassistenten. Den nya upplevelsen blir obligatorisk i april 2023-cykel.

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Vilka distributionstyper stöds för närvarande för uppgradering?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Distribution av Project Operations Lite                        | Stöds               |
| Projektledning och redovisning i Dynamics 365 Finance | Distribution av Project Operations Lite                        | Stöds för närvarande inte |
| Finansiera projektledning och redovisning              | Project Operations för resurs-/icke-lagerbaserade scenarier     | Stöds för närvarande inte |
| Project Service Automation 3.x                         | Project Operations för resurs-/icke-lagerbaserade scenarier     | Stöds för närvarande inte |
| Project for the Web (dedikerad miljö)            | Distribution av Project Operations Lite                        | Stöds för närvarande inte |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hur installerar jag Project Operations innan uppgraderingsverktyget är tillgängligt?

Det finns två sätt att installera Project Operations innan uppgraderingsverktyget är tillgängligt:

- Etablera en ny miljö.
- Distribuera Project Operations separat i en försäljningsorganisation där Project Service Automation inte finns.

Om Project Service Automation installeras i en organisation, men inte används, kan den avinstalleras. När du har tagit bort Project Service Automation helt kan Project Operations installeras i samma organisation.
