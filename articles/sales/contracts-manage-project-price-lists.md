---
title: Hantera projektprislistor i projektkontrakt
description: Den här artikeln innehåller information om hur du hanterar projektprislistor i projektkontrakt.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 23b9e6f9bc3e4bc3fb03de62064644dd58da34c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926200"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Hantera projektprislistor i projektkontrakt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektkontrakt i Dynamics 365 Project Operations är utformade för att stödja flera prislistor för försäljningsdatum i ett kontrakt. I Project Operations finns det en ny associerad entitet som kallas **projektprislistor**. Entiteten har en 1:n-relation till ett projektkontrakt.

Projektprislistor används för pristransaktioner med tid, material och utgifter för ett projekt. När ett kontrakt offert har en eller flera projektprislistor används dessa prislistor för pristid, material, kostnader och faktiska värden för projekt som är associerade med kontraktet via kontraktraden.

När det inte finns några projektprislistor på ett projektavtal ser du ett varningsmeddelande om att det inte finns några projektprislistor och dina uppskattningar, faktiska projektarbete, material och inloggade kostnader kommer inte att prissättas. Det kommer inte att finnas något pris för försäljningsvärden.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associera eller ta bort associationen för en projekt prislista till ett projektkontrakt

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Skapa eller associera en specifik prislista för projektbaserat arbete, material och utgifter

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

En projektprislista kan anges som standardprislista för projekt. Med den här inställningen kan du se till att alla kontrakt i organisationen alltid börjar med en standardprislista för projekt för den prisperioden.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
