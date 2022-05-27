---
title: Inställningar för projektoffert
description: I det här ämnet finns information om den information och de inställningar som gäller för projektofferter.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c5870c75d5337b951a453000369baf9f6e81a1da
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575188"
---
# <a name="header-details-for-project-based-quotes"></a>Rubrikinformation för projektbaserade offerter

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_


Den här artikeln innehåller information om hur du använder en projektoffert. Detta inkluderar de inställningar som påverkar alla offertrader och information om den offert som summeras från alla radartiklarna för att köra KPI:er för projektofferten.

I följande tabell visas fälten sammanfattningsinformation i en projektoffert som är unika för Dynamics 365 Project Operations eller har några viktiga funktionsförändringar från offerter i Dynamics 365 Sales.

| **Fält** | **Plats** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Type | Fliken Sammanfattning (dold) | Detta fälthash med alternativuppsättningen har följande alternativ:</br>- Arbetsbaserad (endast tillgängligt när Project Operations är installerat)</br>- Artikelbaserad (endast tillgänglig när Project Operations och Sales är installerat)</br>- Serviceunderhåll-baserad (tillgängligt när Dynamics 365 Field Service är installerat) | När du använder Project Operations-programmet anges värdet i det här fältet automatiskt som **Arbetsbaserad**. Detta klassificerar offerten som en projektbaserad offert. En offert ska vara projektbaserad för att alla projektspecifika tillägg och funktioner ska kunna aktiveras. |
| Ägande företag | Sammanfattning | Den juridiska person som ska redovisa de kostnader och intäkter som påförs från det här projektet eller projekt som är associerade med offerten. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Det ägande företaget är lika med begreppet juridisk person i modulen **Projektledning och redovisning** i Project Operations. Alla kostnader och intäkter som härrör från detta projekt redovisas i det ägande företagets huvudbok. |
| Potentiell kund | Fliken Sammanfattning | Referens till kundens företag eller kontopost. En giltig kund att referera till i projektofferten måste vara konfigureras som en kund i det ägande företaget i offerten. Det ägande företaget visar listan över juridiska personer och dessa konfigureras i modulen **Projektledning och redovisning** i Project Operations. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Valutan i projektofferten används som standard utifrån kundens valuta. Detta kan dock inte ändras innan offerten sparas. |
| Kontohanteraren | Fliken Sammanfattning | Namnet på kontoansvarig för denna affär. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Kontoansvarig är ansvarig för att hantera relationen med kunden genom att fullborda arbetet på det här projektet. På grundval av den bokningsbara resursposten som är kopplad till kontoansvarig hämtas den avtalande enheten till projektofferten.|
| Kontrakteringsenhet | Fliken Sammanfattning | Den organisationsenhet som är ansvarig för leveransen av projektet eller projekten som är associerade offerten. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Den avtalande enheten är den avdelning i företaget som ska utföra projekten efter det att affären har stängts. Varje avtalande enhet har en valuta och valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under utförandet av projektet. |
| Produktprislista | Fliken Sammanfattning | Det här är prislistan som används som standard för priserna på de produktbaserade offertraderna. I listan med alternativ för det här fältet visas en lista med prislistor där prislistans valuta stämmer överens med valutan i offerten. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. Fältet i affärsmöjligheten visas som standard från kontoposten men kan ändras. | När en offert har vunnits kopieras värdet till projektkontraktraden som skapas. |
| Valuta | Fliken Sammanfattning | Detta anger valutan som används för att rapportera värdet av denna affär. Det är också den valuta i vilken kunden faktureras om affären genomförs. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. Fältet i affärsmöjligheten visas som standard från kontoposten men kan ändras av användaren.  | När en offert har sparats går det inte längre att redigera det här fältet. Detta används för att standardisera produkt- och projektprislistorna i offerten. Valutan i offerten används för att matcha valutan i prislistan. |
| Undre gräns | Fliken Sammanfattning | Detta anger det förhandlade taket på det slutgiltiga värde som kunden accepterar för denna affär. | Taket utvärderas under utförande och är tillämplig för alla radartiklar och projekt som är kopplade till denna affär. |
| Begärt leveransdatum | Fliken Sammanfattning | När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Detta datum används som slutdatum för generering av fakturascheman. |

Nedan finns flikarna och KPI:erna som är tillgängliga i en projektoffert som är unik för Project Operations eller som har viktiga förändringar i beteendet hos Sales-offerter:

| **Fält** | **Plats** | **Beskrivning** |
| --- | --- | --- |
| Lönsamhetsanalys | Flik i offerten | Fliken visar följande mått:</br>- Total debiterbar kostnad</br></br>- Total icke debiterbar kostnad</br>- Totalintäkt</br>- Totalintäkt (bas)</br>- Bruttomarginal</br>- Justerad bruttomarginal|
| Jämförelse med kundförväntningar | Flik i offerten | Fliken visar följande mått:</br>- Beräknat färdigställande</br>- Begärt färdigställande</br>- Kundbudget</br>- Offertvärde |
| Offertanalys | Flik i offerten | Den här fliken sammanfattar följande KPI:er för en projektoffert</br>- Jämförelse med kundförväntningar på budget och schema</br>- Bruttomarginal</br>- Justerad bruttomarginal |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
