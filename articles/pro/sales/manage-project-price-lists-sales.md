---
title: Hantera projektprislistor i projektofferter
description: I det här ämnet finns information om hur du arbetar med projektprislistor i offerter. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966872"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Hantera projektprislistor i projektofferter (försäljning)

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Projektofferter har utformats för att stödja flera datumeffektiva försäljningsprislistor. Med Dynamics 365 Project Operations läggs en ny associerad entitet med namnet **Projektprislistor** till. Entiteten har förhållandet 1-till-många till en projektoffert.

Projektprislistor används för att visa pris-, tids- och utgiftstransaktioner för ett projekt. När en offert har en eller flera projektprislistor används de här prislistorna som uppskattningar och faktiska värden av pris, tid och utgifter för projekt som associeras med offerten via offertraden.

Om det inte finns några projektprislistor på en projektoffert visas ett varningsmeddelande. Meddelandet anger att eftersom det inte finns några projektprislistor blir inte uppskattade och faktiska värden för arbete och utgifter i projektet prissatta. De kommer i stället att ha noll (0) pris för försäljningsvärden.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Associera eller ta bort kopplingen mellan en projektprislista och en projektoffert

Följ stegen nedan om du vill skapa eller välja en specifik prislista som uppskattar projektbaserat arbete och projektbaserade utgifter.

1. I offerten väljer du fliken **Projektpris** och i underrutnätet väljer du **+ Lägg till ny projektprislista**.
2. Välj en prislista på sidan Snabbskapande. I den nedrullningsbara listan visas alla prislistor som har kontexten inställd på **Försäljning** och valutan överensstämmer med valutan i offerten.
4. Ange en beskrivning av kopplingen till projektprislistan och välj **Spara och stäng**.

En koppling till projektprislistan skapas.

Du kan upprepa den här processen om du behöver associera fler än en projektprislista till projektofferten. Skapa endast flera projektprislistor om du har olika giltighetsdatum för de associerade projektprislistorna.

> [!NOTE]
> Project Operations har inte stöd för överlappande datumeffektivitet i projektprislistorna. Om det finns flera projektprislistor för en transaktion med angivet datum, blir priset för den transaktionen standardvärdet noll (0).
Om du vill ta bort en association för projektprislistan väljer du projektprislistan och väljer sedan **Ta bort offertens projektprislista**. Prislistan tas bort från offertens projektprislistor, men själva prislistan tas inte bort. Endast associationen till offerten tas bort.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Ange standardprislistor för projekt i en offert

Projektprislistor kan anges som standard i en projektoffert. Den här inställningen innebär att alla offerter i organisationen alltid startas med en standardprislista för den prisperioden.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Ange organisationens standardprislistor för projekt

1. Gå till **Inställningar** > **Allmänt** > **Parametrar**.
2. På sidan **Aktiva parametrar** letar du upp posten och dubbelklickar för att öppna den. 
3. På sidan **Parametrar** väljer du fliken **Prislista**. Du kan se listan över standardprislistor. Det här är en lista med standardkostnads- och försäljningsprislistor. Om en försäljningsprislista är kopplad till alla valutor som du säljer i ser du till att den här försäljningsprislistan standardiseras i alla offerter som du skapar för kunder som är med i den här valutan.

### <a name="set-up-customer-specific-project-price-lists"></a>Konfigurera kundspecifika projektprislistor

Kundspecifika projektprislistor kan också konfigureras när du har förhandlat fram ett huvudprisavtal med dina kunder.

Följ stegen nedan om du vill skapa en kundspecifik projektprislista.

1. I området **Försäljning** väljer du **Kunder**.
2. Välj och öppna kundposten som du har en särskild prislista för i listan över aktiva konton.
3. Under fliken **Projektprislistor** kan du skapa en ny prislistkoppling för att få den projektprislista som är specifik för kunden.

## <a name="create-custom-pricing-on-a-project-quote"></a>Skapa anpassad prissättning för en projektoffert

När du har skapat organisations- och kundspecifika standardprislistor skapas dina projektofferter automatiskt med de här associationerna till projektprislistor. I vissa fall kan du emellertid behöva skapa en anpassad prissättning för en specifik projektoffert. 

1. I **Projektoffert**, under fliken **Projektprislistat**, verifierar du i underrutnätet att ingen specifik prislistpost har valts.
2. Välj **Skapa anpassad prissättning**. Då skapas en kopia av alla standardprislistor som är associerade med offerten och dessa kopior associeras till offerten. De befintliga kopplingarna till standardprislistor tas bort. Säljaren kan sedan göra ändringar i priser för kopiorna. De ändrade priserna gäller endast för den här projektofferten.
