---
title: Kopiera prislistor
description: I det här ämnet finns information om hur du kopierar prislistor i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085579"
---
# <a name="copy-price-lists"></a>Kopiera prislistor

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan skapa kopior av prislistor i Dynamics 365 Project Operations. Du kan till exempel skapa prislistor för kommande år med hjälp av en prislista från aktuellt år.  Du kan också kopiera en prislista för fakturataxor och försäljningspriser från prislistorna för kostnader. 

Följ stegen nedan om du vill göra en kopia av prislistan.

1. Öppna den prislista som du vill göra en kopia av och välj **Kopiera**.
2. Ange all nödvändig information för att kopiera prislistan. I följande tabell visas överväganden som du bör tänka på när du matar in information.

| Fält | Relevans, syfte och vägledning | Inverkan nedströms |
| --- | --- | --- |
| Namn | Namnet på källprislistan med tillägget **-kopia**. | Prislistan innehåller det här värdet på alla listsidor och listrutealternativ. |
| Sammanhang | Ange det sammanhang du vill använda för målprislistan. | En prislista med sammanhanget inställt på **Kostnad** används för att slå upp priset för kostnadsuppskattningar och faktiska kostnadsvärden. En prislista med sammanhanget inställt på **Försäljning** används för att slå upp priset för försäljningsuppskattningar och faktiska försäljningsvärden. Endast prislistor som har sammanhanget inställt på **Försäljning** kan kopplas till en projektprislista för en kund, en offert eller ett kontrakt. |
| Startdatum | Startdatum för perioden som prislistan gäller. | Tillsammans med **Slutdatum** används det här fältet för att avgöra vilken prislista som gäller för en viss rad för uppskattning eller faktiska värden. |
| Slutdatum | Slutdatum för perioden som prislistan gäller. | Tillsammans med **Startdatum** används det här fältet för att avgöra vilken prislista som gäller för en viss rad för uppskattning eller faktiska värden. |
| Valuta | Valutan för källprislistan. Denna går att ändra. | När denna ändras konverteras alla prisrader för arbete, utgift och produktkatalogsartiklar till målprislistans valuta under kopieringen. |
| Tidsenhet | Valutan för källprislistan. Denna går att ändra. | När denna ändras konverteras alla prisrader för arbetsartiklar till målprislistans enhet under kopieringen. Konverteringen från enhetsinställningarna för källprislistans tidsenhet och målprislistans tidsenhet används. |
| Beskrivning | En beskrivning av källprislistan med tillägget **-kopia**. Det här är ett textfält som gör att du kan använda en flerradig beskrivning av prislistan. | Det här fältet visas i **associerade** vyer för prislistan i olika entiteter som har relaterade prislistor. |

3. Spara prislistan. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Uppdatera en prislista genom att lägga till ett pålägg på priserna

1. Under flikarna **Roll** , **Kategori** och **prislistepost** för prislistan kan du välja **Uppdatera priser** för att tillämpa ett pålägg på alla priser i underrutnätet. 
2. I dialogrutan som öppnas anger du ett pålägg. Du kan även ange en negativ påläggsprocent för att sänka priset med en viss procentsats. 
3. Välj **OK** i dialogrutan och kontrollera att priserna i underrutnätet återspeglar de ändringar du har gjort.