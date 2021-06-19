---
title: Ekonomisk kalkyl för kostnader på projekt
description: I det här ämnet finns information om hur du definierar eller uppskattar projektbaserade utgifter.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 18d8568fae35fc251d9cf48d900b8a436e2e4500
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014183"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Ekonomisk kalkyl för kostnader på projekt
_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations tillåter projektledare att definiera projektbaserade utgifter för varje projekt eller uppgift. Varje utgiftsobjekt kan kopplas till en specifik projektuppgift. Utgifter kategoriseras i olika utgiftskategorier, som definieras på organisationsnivå. Prissättning och kostnad för varje utgiftskategori definieras i prislistan. 

Följ stegen nedan om du vill visa, lägga till eller ta bort en projektutgift.

1. Gå till **Projekt** och välj det projekt du vill arbeta med.
2. Välj fliken **Projektuppskattningar** och visa listan med projektutgifter.
3. Välj **Ny utgift** om du vill lägga till en utgift. Du kan också välja vilka utgifter som ska tas bort och sedan välja **Ta bort utgift**.

Följande tabell ger information om fälten på sidan **utläggsberäkningsrad** på ett projekt. 

| **Fält** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- |
| Uppgift | En lista över alla uppgifter i ett projekt. Detta omfattar uppgifter för sammanfattning och nod för noderna. | Om du väljer en uppgift för en utläggsberäkningsrad påverkas den beräknade utgiftskostnaden och den beräknade utgiftsförsäljningen för en uppgift. Om detta fält är tomt spåras och sammanfattas utgiftsberäkningen endast på projektnivå. |
| Kategori | En lista över transaktionskategorier som har länkat utgiftskategorier i programmet. | Om du väljer en kategori kan du beräkna priser och kostnader på utläggsberäkningsraden. |
| Startdatum | Det prognostiserade datumet då kostnaden kommer att ske. | Det här fältet har ingen inverkan nedströms. |
| Enhetsgrupp | Standardvärdet i det här fältet kommer från den enhetsgrupp som har angetts som standard för vald kategori. Du kan uppdatera fältet om du vill välja en annan enhetsgrupp. | Det här fältet har ingen inverkan nedströms. |
| Enhet | Värdet i det här fältet är standardenheten för den valda kategorin. Du kan uppdatera fältet om du vill välja en annan enhet. | Om du ändrar enheten får du ett annat standardpris och en annan standardkostnad för enheten. |
| Antal | Kvantiteten av den beräknade kostnaden för dig. | Det här fältet har ingen inverkan nedströms. |
| Enhetskostnad | Kostnaden för den valda kategori och enhetskombinationen enligt den aktuella kostnadsprislistan | Enhetskostnaden visas alltid i projektets kostnadsvaluta. |
| Enhetspris | Priset för den valda kategori och enhetskombinationen enligt den aktuella prislistan för försäljning. | Enhetspriset visas alltid i projektets försäljningsvaluta. |
| Total kostnad | Kostnadsbeloppet som beräknas som enhetskostnad för \* kvantitet.| Kostnadsbeloppet visas alltid i projektets kostnadsvaluta. |
| Total försäljning | Försäljningsbeloppet som beräknas som enhetspris för \* kvantitet. | Försäljningsbeloppet visas alltid i projektets försäljningsvaluta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
