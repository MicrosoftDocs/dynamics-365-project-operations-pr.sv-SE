---
title: Hantera projektprislistor i projektkontrakt
description: I det här ämnet finns information om hur du hanterar projektprislistor i projektkontrakt.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133455"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Hantera projektprislistor i projektkontrakt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektkontrakt i Dynamics 365 Project Operations är utformade för att stödja flera prislistor för försäljningsdatum i ett kontrakt. I Project Operations finns det en ny associerad entitet som kallas **projektprislistor**. Entiteten har en 1:n-relation till ett projektkontrakt.

Projektprislistor används för att visa pris-, tids- och utgiftstransaktioner för ett projekt. När ett kontrakt har en eller flera projekt prislistor används de här prislistorna som priser för uppskattningar av tid och utgifter och faktiska värden för projekt som är associerade med kontraktet via kontraktraden.

Om det inte finns några projekt prislistor i ett projektkontrakt visas ett varnings meddelande om att det inte finns några projektprislistor och att uppskattningar, projektarbete och utgifter inte ska vara prissatta. Det kommer inte att finnas något pris för försäljningsvärden.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associera eller ta bort associationen för en projekt prislista till ett projektkontrakt

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Skapa eller associera en specifik prislista för uppskattning av projektbaserade resurser och utgifter

1. I projektkontraktet, välj fliken **Projektprislistor**.
2. Välj i delnätet **+ Lägg till ny projektprislista**.
3. I skjutreglaget **Snabbregistrering** välj en prislista. 

  I den nedrullningsbara listan visas alla prislistor som har kontexten inställd på **försäljning**, där valutan i prislistan överensstämmer med valutan i kontraktet.
  
4. Ange en beskrivning av kopplingen till prislistan för projekt, välj **Spara** och stäng sedan reglaget **Snabbregistrering**.

   En koppling till projektprislistan skapas.
   
5. Upprepa steg 1-4 om du vill associera fler än en projektprislista till projektkontraktet. Skapa endast flera projektprislistor om du har olika giltighetsdatum för de associerade projektprislistorna.

> [!NOTE]
> Project Operations stöder inte överlappande giltighetsdatum för projektprislistorna. Om det finns flera projektprislistor för en transaktion med ett visst datum blir priset på den transaktionen standard till noll.

### <a name="remove-a-project-price-list-association"></a>Ta bort en association för projektprislista

- Markera projektprislistan och välj sedan **ta bort kontraktprojekt prislista** i underrutnätet. 

  Prislistan tas bort från projekt prislistorna för kontraktet. Själva prislistan tas inte bort. Endast associationen till kontraktet kommer att tas bort.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Ange automatisk standard av projekt prislistor för ett kontrakt

Du kan ställa in en projekt prislista som standardlista i ett projektkontrakt. Med hjälp av den här installationen kan du se till att alla kontrakt i organisationen alltid startas med en standard prislista för den prisperioden.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Konfigurera organisationens standard för projekt prislistor

1. Gå till **Inställningar** > **Allmän** och välj sedan **Parametrar**.
2. I listsida **Aktiva parametrar**, välj och dubbelklicka på posten för att öppna den. Kontrollera att du inte klickar på ett fältvärde som är hyperlänk medan du dubbelklickar på. 
3. På sidan **aktiva parametrar** välj fliken **prislista**. I ett underrutnät visas en lista över standardprislistor. Det här är en lista över standardkostnads- och försäljningsprislistor. Att ha en prislista för **Försäljning** här för varje valuta som du säljer i ser till att försäljningsprislistan är standard på alla kontrakt som du skapar för kunder som handlar i den här valutan.

### <a name="set-up-a-customer-specific-project-price-list"></a>Ställ in en kundspecifik projektprislista

Du kan också skapa kundspecifika projektprislistor när du har förhandlat fram ett huvudprisavtal med kunderna.

1. Gå till **Försäljning** > **Kunder**.
2. Välj den kund som har en särskild prislista i listan med aktiva konton.
3. Markera kundposten och öppna den och välj sedan fliken **projektprislistor**. I ett underrutnät visas en lista över projektprislistor som är specifika för kunden. 
4. Skapa en ny association av prislista här om du vill ha en specifik projektprislista för den här kunden.

## <a name="custom-pricing-on-a-project-contract"></a>Anpassad prissättning på ett projektkontrakt

När du har skapat organisations- och kundspecifika standard prislistor skapas projektkontrakten automatiskt med de här kopplingarna av prislistorna i projekt. Projektkontraktslistor i ett projektkontrakt kopieras dock alltid med datum- och kontraktnamn som bifogas till dem. Konto- och projektledarna kan sedan göra ändringar i priser för kopiorna. Dessa ändrade priser gäller endast för detta projektkontrakt.
