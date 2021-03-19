---
title: Granska föreslagna resurser
description: I det här ämnet finns information om hur du föreslår projektresurser.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279295"
---
# <a name="review-proposed-resources"></a>Granska föreslagna resurser

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Resursansvariga kan föreslå en resurs till projektledaren genom att använda en resursbegäran.

1. Från rutnätet för begäran eller själva begäran, välj **Hitta resurser**.
2. På sidan **schemaassistent** markerar du resursen och väljer rutan **Skapa resursbokning** i fältet **bokningsstatus** och väljer **boka**.

Följande statusuppdateringar inträffar:

- På sidan **schemaläggningsassistent** uppdateras statusindikatorerna för att indikera att bokningen är föreslagen, inte en fast bokade.
- I resursbegäran ändras status till **måste granskas**.
- På fliken **team** i projektet ändras värdet för den allmänna teammedlemmens **Status för begäran** till **måste granskas**.

Projektledaren kan antingen acceptera eller avvisa förslaget.

När resursansvariga behandlar resursbegäranden kan de använda någon av följande metoder:

- Föreslå flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att uppfylla de timmar som krävs. Föreslagna timmar delas sedan mellan flera resurser som kan uppfylla de begärda timmarna. I det här scenariot kan timmarna inte överlappas.
- Föreslå färre resurser än vad som krävs. I det här scenariot är den föreslagna resurskapaciteten mindre än de timmar som begärdes av den begärande. När den som beställt accepterar de föreslagna resurserna skapas därför ett ouppfyllt resursbehov som fångar upp det återstående behovet.
- Boka flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att slutföra arbetet.
- Boka färre resurser än vad som krävs. I det här scenariot är bokade timmar färre än de timmar som krävs. Systemet hjälper dig att föreslå resurser i stället för bokningar, så att den som gör en förfrågan kan verifiera och hålla ordning på återstående efterfrågan.

## <a name="resource-availability"></a>Resurstillgänglighet

Det är viktigt att resursansvariga kan visa tillgängligheten till resurser och uppdatera bokningar. I vissa fall finns ingen formell efterfrågan (resursbegäran), men en resursansvarig måste svara på en oplanerad efterfrågan som sker via kanaler som e-post, telefonsamtal eller snabbmeddelanden. Resursansvariga kan uppdatera resurser och bokningar med hjälp av schemaläggningstavlan.

Resursens arbetstider används som grund för att beräkna resursens tillgänglighet. Resursbokningarna förbrukar kapaciteterna för resurserna.

I schemaläggningstavlan används färger och fyllning för att visa bokningar, tillgänglighet och förbokningar samt även status för bokningar. En inställning i schemaläggningstavlan gör att du kan visa en förklaring.

Om en högerriktad pil visas bredvid en enskild bokningsbar resurs på schemaläggningstavlan kan resursen expanderas så att den innehåller information om det arbete som resursen är bokad på.

Eftersom Dynamics 365 Project Operations använder Universal Resource Scheduling-motorn, om du även har Dynamics 365 Field Service installerat kan du visa information om resursbokningar för projekt, arbetsorder och andra entiteter som du har utvidgat schemaläggning till.

Om du vill visa mer information om en enskild resurs högerklickar du på den så att resurskortet öppnas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]