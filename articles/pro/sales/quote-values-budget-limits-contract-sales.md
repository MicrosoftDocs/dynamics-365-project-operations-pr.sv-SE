---
title: Översiktsinformation för en projektoffert - lite
description: I det här ämnet finns information om den information och de inställningar som gäller för projektofferter. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 967e2170aac72de629ebb930e485b8cd6560b6ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272455"
---
# <a name="summary-information-on-a-project-quote---lite"></a>Översiktsinformation för en projektoffert - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Den här artikeln innehåller information om hur du använder en projektoffert. Detta inkluderar de inställningar som påverkar alla offertrader och information om den offert som summeras från alla radartiklarna för att köra KPI:er för projektofferten.

I följande tabell visas fälten sammanfattningsinformation i en projektoffert som är unika för Dynamics 365 Project Operations eller har några viktiga funktionsförändringar från offerter i Dynamics 365 Sales.

| **Fält** | **Plats** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Type | Fliken Sammanfattning (dold) | Detta fälthash med alternativuppsättningen har följande alternativ:</br>- Arbetsbaserad (endast tillgängligt när Project Operations är installerat)</br>- Artikelbaserad (endast tillgänglig när Project Operations och Sales är installerat)</br>- Serviceunderhåll-baserad (tillgängligt när Dynamics 365 Field Service är installerat) | När du använder Project Operations-programmet anges värdet i det här fältet automatiskt som **Arbetsbaserad**. Detta klassificerar offerten som en projektbaserad offert. En offert ska vara projektbaserad för att alla projektspecifika tillägg och funktioner ska kunna aktiveras. |
| Potentiell kund | Fliken sammanfattning  | Referens till kundens företag eller kontopost. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Valutan i projektofferten används som standard utifrån kundens valuta. Detta kan dock inte ändras innan offerten sparas. |
| Kontohanteraren | Fliken sammanfattning  | Namnet på kontoansvarig för denna affär. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Kontoansvarig är ansvarig för att hantera relationen med kunden genom att fullborda arbetet på det här projektet. På grundval av den bokningsbara resursposten som är kopplad till kontoansvarig hämtas den avtalande enheten till projektofferten. |
| Kontrakteringsenhet | Fliken sammanfattning  | Den organisationsenhet som är ansvarig för leveransen av projektet eller projekten som är associerade offerten. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Den avtalande enheten är den avdelning i företaget som ska utföra projekten efter det att affären har stängts. Varje avtalande enhet har en valuta och valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under utförandet av projektet. |
| Produktprislista | Fliken sammanfattning  | Det här är prislistan som används som standard för priserna på de produktbaserade offertraderna. I listan med alternativ för det här fältet visas en lista med prislistor där prislistans valuta stämmer överens med valutan i offerten. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. Fältet i affärsmöjligheten visas som standard från kontoposten men kan ändras. | När en offert har vunnits kopieras värdet till projektkontraktraden som skapas. |
| Valuta | Fliken sammanfattning  | Detta anger valutan som används för att rapportera värdet av denna affär. Det är också den valuta i vilken kunden faktureras om affären genomförs. När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. Fältet i affärsmöjligheten visas som standard från kontoposten men kan ändras av användaren. | När en offert har sparats går det inte längre att redigera det här fältet. Detta används för att standardisera produkt- och projektprislistorna i offerten. Valutan i offerten används för att matcha valutan i prislistan. |
| Undre gräns | Fliken sammanfattning  | Detta anger det förhandlade taket på det slutgiltiga värde som kunden accepterar för denna affär. | Taket utvärderas under utförande och är tillämplig för alla radartiklar och projekt som är kopplade till denna affär. |
| Begärt leveransdatum | Fliken sammanfattning  | När en offert skapas från en affärsmöjlighet kopieras fältet från motsvarande fält på affärsmöjlighetsraden. | Detta datum används som slutdatum för generering av fakturascheman. |

Nedan finns flikarna och KPI:erna som är tillgängliga i en projektoffert som är unik för Project Operations eller som har viktiga förändringar i beteendet hos Sales-offerter:

| **Fält** | **Plats** | **Beskrivning** |
| --- | --- | --- |
| Lönsamhetsanalys | Flik i offerten | Fliken visar följande mått:</br>- Total debiterbar kostnad</br></br>- Total icke debiterbar kostnad</br>- Totalintäkt</br>- Totalintäkt (bas)</br>- Bruttomarginal</br>- Justerad bruttomarginal|
| Jämförelse med kundförväntningar | Flik i offerten | Fliken visar följande mått:</br>- Beräknat färdigställande</br>- Begärt färdigställande</br>- Kundbudget</br>- Offertvärde |
| Offertanalys | Flik i offerten | Den här fliken sammanfattar följande KPI:er för en projektoffert</br>- Jämförelse med kundförväntningar på budget och schema</br>- Bruttomarginal</br>- Justerad bruttomarginal |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]