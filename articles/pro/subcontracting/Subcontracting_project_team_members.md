---
title: Underkontraktering av projektteammedlemmar
description: I det här ämnet beskrivs hur man underkontrakterar projektteammedlemmar i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902943"
---
# <a name="subcontracting-project-team-members"></a>Underkontraktering av projektteammedlemmar

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I Microsoft Dynamics 365 Project Operations kan du välja att underkontraktera icke anställda eller anställda projektteammedlemmar.

- Projektteammedlemmar som inte är anställda har tilldelats en allmän resurs.
- Anställda teammedlemmar har tilldelats en namngiven resurs.

När du länkar en projektteammedlem till en underleverantörsrad, beräknas alla tilldelningar till uppgifter som teammedlemmen har gjort baserat på inköpsprislistan som är bifogad till underleverantörskontraktet.  Under fliken **Uppskattningar** på sidan **Projektdetaljer** väljer du knappen **Uppdatera priser** för att se uppdaterad prissättning och/eller kostnadsföring till följd av beslutet att underkontraktera. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Underkontraktering av en obemannad projektteammedlem
Sidan **Teammedlemsdetaljer** har fält för underleverantör och underleverantörsrad som gör det möjligt för projektledare att uttrycka hur de vill använda den kapacitet som krävs från en underleverantör. Följ stegen nedan om du vill anlita en projektteammedlem som allmän resurs:

1.  Välj en underleverantör på sidan **Teammedlemsdetaljer**.

2.  Du kan endast välja underleverantörer med statusen **Utkast** eller **Bekräftad**. **Stängda** eller **Avbrutna** underleverantörskontrakt kan inte väljas. 

3.  Fältet **Underleverantörsrad** visas när du har valt en underleverantör.

4.  I fältet **Underkontraktsrad** kan du endast välja underleverantörsrader som gäller tid. Du kan inte välja underleverantörsrader för utgifter eller material.

5.  Rollen för projektteammedlemsposten måste matcha rollen på underleverantörsraden. Detta säkerställer att den tid för rollen som beräknas för projektet är samma roll som köpts på underleverantörsraden. 

När en generisk teammedlem associeras till en underleverantör och underleverantörsrad uppdateras fältet **Arbetartyp** på raden för generiska teammedlemmar till **Kontraktarbetare** och **Underleverantörs giltighet** till **Giltig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Underkontraktering av en bemannad projektteammedlem
Precis som generiska eller icke anställda teammedlemmar kan den kapacitet av anställda teammedlemmar som krävs för ett projekt också länkas till en underleverantör. Följ stegen nedan om du vill anlita en namngiven projektteammedlem:

1.  Kontrollera att den namngivna resursen har angetts som en kontraktarbetare av en bokningsbar resurs. Kontrollera också att fältet **Leverantör** på den bokningsbara resursen matchar leverantören på det underleverantörskontrakt som du väljer. 

2.  Du kan endast välja underleverantörer med statusen **Utkast** eller **Bekräftad**. **Stängda** eller **Avbrutna** underleverantörskontrakt kan inte väljas. 

3.  Fältet **Underleverantörsrad** visas när du har valt en underleverantör.

4.  I fältet **Underkontraktsrad** kan du endast välja underleverantörsrader som gäller tid. Du kan inte välja underleverantörsrader för utgifter eller material.

5.  Rollen för projektteammedlemsposten måste matcha rollen på underleverantörsraden. Detta säkerställer att den tid för rollen som beräknas för projektet är samma roll som köpts på underleverantörsraden. 

Namngivna projektteammedlemmar som är konfigurerade som kontraktarbetare av typen **Bokningsbar resurs** visas med underleverantörsstatusen **Ej giltig** om de inte är länkade till en underleverantör. När en namngiven projektteammedlem associeras till en underleverantör och underleverantörsrad uppdateras fältet **Arbetartyp** på raden för teammedlemmar till **Kontraktarbetare** och **Underleverantörs giltighet** till **Giltig**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
