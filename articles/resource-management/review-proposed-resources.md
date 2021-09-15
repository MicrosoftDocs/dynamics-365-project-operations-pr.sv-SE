---
title: Granska föreslagna resurser
description: I det här ämnet finns information om hur du föreslår projektresurser.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403817"
---
# <a name="review-proposed-resources"></a>Granska föreslagna resurser

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Resursansvariga kan föreslå en resurs till projektledaren genom att använda en resursbegäran.

Granska föreslagna resurser genom att följa dessa steg:

1. I rutnätet **Förfrågan** eller i själv förfrågan väljer du **Hitta resurser**.
2. På sidan **Schemaassistent** väljer du resursen och bekräftar sedan att samtliga föreslagna tider har inkluderats i föreslagen bokning.
3. I fönstret **Sakpa resursbokning** anger du fältet **Bokningsstatus** som **Föreslaget** och sedan **Boka**.

    > [!NOTE]
    > Att ange **Bokningsstatus** som **Föreslaget** definitivbokar inte resursen och ersätter inte den generiska resursen hos namngiven teammedlem.

    Följande statusuppdateringar inträffar:

    - På sidan **schemaläggningsassistent** uppdateras statusindikatorerna i syfte att indikera att bokningen är föreslagen, inte definitivbokad.
    - I resursbegäran ändras status till **måste granskas**.
    - På fliken **team** i projektet ändras värdet för den allmänna teammedlemmens **Status för begäran** till **måste granskas**.

Projektledaren kan godkänna eller avvisa förslaget.

När resursansvariga behandlar resursbegäranden kan de använda någon av följande metoder:

- Föreslå flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att uppfylla de timmar som krävs. Föreslagna timmar delas sedan mellan flera resurser som kan uppfylla de begärda timmarna. I det här scenariot kan timmarna inte överlappas.
- Föreslå färre resurser än vad som krävs. I det här scenariot är den föreslagna resurskapaciteten mindre än de timmar som begärdes av den begärande. När beställaren godkänner föreslagna resurser skapas ett ouppfyllt resursbehov i syfte att fånga upp det återstående behovet.
- Boka flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att slutföra arbetet.
- Boka färre resurser än vad som krävs. I det här scenariot är bokade timmar färre än de timmar som krävs. Systemet hjälper dig att föreslå resurser istället för bokningar, detta så att den som gör en förfrågan kan verifiera och hålla ordning på återstående förfrågan.

## <a name="resource-availability"></a>Resurstillgänglighet

Resursansvariga måste kunna visa tillgängligheten för resurser och uppdatera bokningar. I vissa fall finns ingen formell begäran (resursbegäran). En resursansvarig måste emellertid svara på en oplanerad begäran som kommer via andra kanaler, till exempel e-postmeddelanden, telefonsamtal eller snabbmeddelanden. Resursansvariga kan använda **schemaläggningstavlan** för att uppdatera resurser och bokningar.

Resursens arbetstider används som grund för att beräkna resursens tillgänglighet. Resursbokningarna förbrukar kapaciteterna för resurserna.

**Schemaläggningstavlan** använder färger och skuggning för att visa bokningar, tillgänglighet och överbokningar, samt även status för bokningar. En inställning på **schemaläggningstavlan** gör att du kan visa en förklaring.

Om en högerriktad pil visas bredvid en enskild bokningsbar resurs på **schemaläggningstavlan** kan resursen expanderas så att den innehåller information om det arbete som resursen är bokad på.

Eftersom Dynamics 365 Project Operations använder Universal Resource Scheduling-motorn, om du även har Dynamics 365 Field Service installerat kan du visa information om resursbokningar för projekt, arbetsorder och andra entiteter som du har utvidgat schemaläggning till.

Om du vill visa ytterligare information om en enskild resurs högerklickar du på den så att resurskortet öppnas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
