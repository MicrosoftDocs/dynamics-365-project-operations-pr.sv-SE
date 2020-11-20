---
title: Skapa tidsposter
description: I det här ämnet finns information om hur du skapar tidsposter.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085631"
---
# <a name="create-time-entries"></a>Skapa tidsposter

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I tidigare versioner av Dynamics 365 Project Service Automation angavs tidsposter veckovis. I version 3 av Project Service Automation anges tidsposter som dagliga uppgifter. När du har skapat några tidsposter kan du dock skapa eller kopiera dem.

## <a name="create-a-time-entry"></a>Skapa en tidspost

Följ dessa steg för att skapa en tidspost.

1. På sidan **Tidspost** klicka på **Ny**.
2. I dialogrutan **Snabbregistrering: tidspost** ange varaktigheten av tidsposten i minuter, timmar eller dagar. Varaktigheten måste anges i följande format: *x* minuter, *x* timmar eller *x* dagar. Timmar och dagar kan även anges som decimalvärden, till exempel *x.x* timmar eller *x.x* dagar.
3. Välj vilken typ av tidsposten och projektet som du vill registrera tidsposten för.
4. I fältet **projektuppgift** letar du upp uppgiften för den här tidsposten.

    > [!NOTE]
    > Om du skapar en tid för en uppgift som inte är tilldelad en användare kan du välja fältet **projektuppgift** , välj knappen **Sök** , välj **Ändra vy** och välj sedan **Alla aktiva projektuppgifter** för att ange alla uppgifter.

5. Ange en beskrivning, om det behövs en beskrivning, och välj sedan **Spara och stäng**.

När du har skapat och sparat tidsposten kan du redigera den i rutnätet för tidsposten. Rutnätet för tidsposten stöder två format:

- Du kan ange tidsposter i formatet **hh:mm**. Formatet konverteras sedan till timmar och bråktal.
- Du kan ange timmar och bråktal direkt.

Observera att bråkdelen av en timme inte är några minuter. Därför motsvarar 1,5 timmar 1 timme och 30 minuter. Samma regel gäller för bråkdelar av en dag. En dag är 24 timmar och 0,5 dagar motsvarar 12 timmar.

## <a name="bulk-create-time-entries"></a>Masskapa tidsposter

När du har skapat några tidsposter kan du kopiera dem för att skapa ytterligare många tidsposter samtidigt.

1. På sidan **Tidspost** klicka på **Kopiera vecka**.
2. I fältgruppen **från period** i fälten **Startdatum** och **Slutdatum** definierar du datumintervallet för att kopiera tidsposter från.
3. I fältgruppen **Till period** i fältet **Startdatum** , ange datumet att skapa tidsposter för.
4. Välj **kopiera** om du vill skapa en kopia av de tidsposter som motsvarar den veckodag som anges i fältgruppen **till period**. Exempelvis kopieras tidsposten för måndagen i den senaste veckan till måndagen i veckan som anges i fältgruppen **till period**.

## <a name="import-data-for-time-entries"></a>Importera data för tidsposter

Du kan importera data från projektbokningar och tilldelningar. När du importerar data kan du ange datumintervallet för de bokningar som ska importeras och sedan uttryckligen välja de bokningar som ska skapas som **utkast** tidsposter.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Gruppera efter, sortera, söka och filtrera funktioner

Du kan gruppera och filtrera tidsposter efter de dimensioner som anges i kolumnerna. I fältet **gruppera efter** väljer du den dimension som ska användas för att filtrera tidsposter. Du kan också sortera tidsposter i stigande eller fallande ordning med hjälp av pilen sortera i kolumnrubrikerna. Du kan även visa eller dölja poster genom att välja knappen **Filter** i kolumnrubrikerna och i rutan **Sök** ange den text som ska användas för att söka efter tidsposter efter projektnamn, projektuppgift, tidspost eller resurs.