---
title: Kopiera ett projekt
description: I det här ämnet finns information om att kopiera projekt i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007213"
---
# <a name="copy-a-project"></a>Kopiera ett projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med Dynamics 365 Project Operations kan du snabbt skapa nya projekt genom att välja **Kopiera projekt** i formuläret **Projekt**. Om du vill kopiera ett projekt öppnar du projektet du vill kopiera och väljer **Kopiera projekt**. Åtgärden kopierar följande:

- Projektegenskaper 
- Uppdelad arbetsstruktur
- Projektets teammedlemmar
- Projektberäkningar
- Beräkning av projektutgifter
- Projektmaterialberäkningar

## <a name="project-properties"></a>Projektegenskaper

När projektet kopieras, kopieras värdena i följande fält:

- Namn
- Beskrivning
- Kund
- Kalendermall
- Valuta
- Kontrakteringsenhet
- Projektledare
- Status
- Övergripande projektstatus
- Kommentarer
- Beräkningar
- Beräknat startdatum: Det här är datumet då projektet skapades från kopian.
- Beräknat slutdatum: Datumet justeras utifrån startdatum för det nya projektet som gjordes från kopian.
- Insats (timmar)
- Beräknad arbetskostnad
- Beräknad utgiftskostnad
- Beräknad materialkostnad

> [!NOTE]
> Kopieringsprojektet är en långvarig körning. Projektposter, deras relevanta attribut och många relaterade entiteter kopieras också. Eftersom åtgärden tar lång tid är målprojektsidan låst efter att kopian har startat och kan redigeras tills kopieringen är slutförd.

## <a name="work-breakdown-structure"></a>Uppdelad arbetsstruktur

När projektet kopieras, kopieras hela den resursinlästa uppdelade arbetsstrukturen. Namngivna resurser ersätts av allmänna resurser. Om de namngivna resurserna inte har samma arbetstider som den allmänna resursen, kommer schemat att beräknas om och varaktigheten för aktiviteten kan ändras.

## <a name="project-team-members"></a>Projektets teammedlemmar

När ett projektteam kopieras från källprojektet kopieras de allmänna resurserna. Allmänna resurstilldelningar hanteras också som de hanterades i källprojektet. Namngivna resurser kommer att konverteras till allmänna teammedlemmar.

## <a name="estimates"></a>Beräkningar

När projektet kopieras kopieras rader för resurs-, utgifts- och materialberäkning från källprojektet. 

Mer information om hur du programmässigt kommer åt Kopiera projekt finns i [Utveckla projektmallar med Kopiera projekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
