---
title: Inställningar för affärsmöjlighet - lite
description: I det här ämne finns information om projektbaserade avtal och projektbaserade affärsmöjlighetsrader.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f40154fed5790083e3a4d3264cc9f8cc23ae18bc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596854"
---
# <a name="header-details-for-project-opportunities"></a>Rubrikinformation för projektaffärsmöjligheter

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I affärsmöjlighetens rubrik anges övergripande information om en projektbaserad affär som gäller alla rader på en projektbaserad affärsmöjlighet.

Projektbaserade affärsmöjligheter i Dynamics 365 Project Operations har utformats med tillägg av affärsmöjligheter i Dynamics 365 Sales. De här tilläggen tillhandahåller ytterligare funktioner som är specifika för och krävs för projektbaserade affärsmöjligheter. De här tilläggen kan innehålla nya fält och åtgärder för menyfliksområdet som är tillgängliga i projektbaserade affärsmöjligheter. Vissa fält, funktioner och standardlogik som är tillgängliga i Sales är inte tillgängliga i Project Operations.

Följande tabell innehåller de fält i en projektbaserad affärsmöjlighet som antingen är unika för Project Operations eller som har viktiga ändringar i beteendet jämfört med affärsmöjligheter i Sales.

| **Fält** | **Plats** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Type | Fliken Allmänt (dold) | Den här alternativuppsättningen har följande alternativ:</br>- Arbetsbaserad (endast tillgängligt med Project Operations)</br>- Artikelbaserad (endast tillgänglig när Project Operations och Sales är installerat)</br>- Serviceunderhåll-baserad (tillgängligt när Field Service är installerat) | När du använder Project Operations anges värdet i det här fältet automatiskt som **Arbetsbaserad** som klassificerar affärsmöjligheten som projektbaserad. En affärsmöjlighet bör vara projektbaserad för att aktivera alla projektspecifika tillägg och funktioner i den efterföljande försäljningsprocessen för affären. |
| Kontaktperson | Fliken Allmänt | Referens till kundens primära kontakt för denna affär. | |
| Konto | Fliken Allmänt | Referens till kundens företag eller kontopost. | |
| Kontohanteraren | Fliken Allmänt | Namnet på kontohanteraren för den projektbaserade affärsmöjligheten. | Kontoansvarig är ansvarig för att hantera relationen med kunden genom att fullborda arbetet på det här projektet. På grundval av den bokningsbara resursposten som är kopplad till kontohanteraren hämtas den avtalande enheten. |
| Kontrakteringsenhet | Fliken Allmänt | Den organisationsenhet som är ansvarig för leveransen av projektet eller projekten som är associerade med denna affär. | Den avtalande enheten är den avdelning i företaget som ska utföra projekten efter det att affären har stängts. Varje avtalande enhet har en valuta och valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under projektet. |

För alla andra fält och avsnitt under fliken **Sammanfattning** för affärsmöjligheten, se [Skapa eller redigera affärsmöjligheter (försäljning och försäljningsnav)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
