---
title: Ekonomisk kalkyl för material på projekt
description: Detta ämne information om hur du definierar eller skapar projektbaserat material.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788901"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Ekonomisk kalkyl för material på projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations tillåter projektledare att definiera projektbaserade materialkostnader för varje projekt eller uppgift. Varje materialberäkning kan kopplas till en specifik projektuppgift. Utgifter kategoriseras i olika utgiftskategorier, som definieras på organisationsnivå. Prissättning och kostnad för varje utgiftskategori definieras i prislistan. 

Utför följande steg för att visa, lägga till eller ta bort en beräkning av projektmaterialet.

1. Gå till **Projekt** och markera det projekt du vill uppdatera.
2. På fliken **Materialberäkningar**, visa listan med uppskattningar av projektmaterial.
3. Välj **Ny materialuppskattning** för att skapa en ny materialuppskattning. Du kan också välja en materialberäkning som ska tas bort och sedan välja **Ta bort materialberäkning**.

Följande tabell ger information om fälten på sidan **materialberäkningsrader** på ett projekt. 

| **Fält** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- |
| Uppgift | En lista över alla uppgifter i ett projekt. Detta omfattar uppgifter för sammanfattning och nod för noderna. | När du väljer en uppgift för en materialberäkningsrad påverkas den beräknade materialkostnaden och den beräknade materialförsäljningen för en uppgift. Om detta fält är tomt spåras och sammanfattas materialuppskattningen endast på projektnivå. |
| Välj produkt |  Du kan ange om uppskattningsraden är för en befintlig (katalog) eller inskriven produkt. | Det här fältet avgör om du väljer en produkt i katalogen eller en produktskrivning. |
| Produkt | ID för produkten från produktkatalogen. När du väljer ett produkt-ID uppdateras värdet fältet **Välj produkt** automatiskt till **Befintlig produkt**. ID används för att hämta kostnader och försäljningspriser från prislistan. | Det här fältet har ingen inverkan nedströms. |
| Beskrivning av oregistrerad produkt | Ett textfält som oregistrerad ska ange produktnamnet. Detta fält bör användas när **Oregistrerad** väljs i **Välj produkt**.| Det här fältet har ingen inverkan nedströms. |
| Startdatum | Det prognostiserade datum då materialet förväntas användas. | Det här fältet har ingen inverkan nedströms. |
| Enhetsgrupp | Standardvärdet i det här fältet kommer från standardenhetsgruppen på katalogprodukten Du kan uppdatera fältet om du vill välja en annan enhetsgrupp. | Det här fältet har ingen inverkan nedströms. |
| Enhet | Värdet i det här fältet kommer från standardenheten för den valda produkten. Du kan uppdatera fältet om du vill välja en annan enhet. | Om du ändrar enheten får du ett annat standardpris och en annan standardkostnad för enheten. |
| Antal | Beräknad kvantitet av produkten som ska användas i projektet. | Det här fältet har ingen inverkan nedströms. |
| Enhetskostnad | Enhetskostnaden för den valda produkten och enhetskombinationen enligt den aktuella kostnadsprislistan. | Enhetskostnaden visas alltid i projektets kostnadsvaluta. Om det inte finns någon enhetskostnad inställd för kombinationsprodukten och enhetsinställning i prislistan blir enhetskostnaden 0,00 som standard. |
| Enhetspris | Priset för den valda produkten och enhetskombinationen enligt den aktuella prislistan för försäljning. | Enhetspriset visas alltid i projektets försäljningsvaluta. Om det inte finns någon enhetskostnad inställd för kombinationsprodukten och enhetsinställning i prislistan blir enhetspriset 0,00 som standard.|
| Total kostnad | Kostnadsbeloppet som beräknas som enhetskostnad för \* kvantitet.| Kostnadsbeloppet visas alltid i projektets kostnadsvaluta. |
| Total försäljning | Försäljningsbeloppet som beräknas som enhetspris för \* kvantitet. | Försäljningsbeloppet visas alltid i projektets försäljningsvaluta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
