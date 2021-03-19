---
title: Kopiera ett projekt
description: I det här ämnet finns information om att kopiera projekt i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479541"
---
# <a name="copy-a-project"></a>Kopiera ett projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med Dynamics 365 Project Operations kan du snabbt skapa nya projekt genom att välja **Kopiera projekt** i formuläret **Projekt**. Om du vill kopiera ett projekt öppnar du projektet du vill kopiera och väljer **Kopiera projekt**. Åtgärden kommer att kopiera:

- Projektegenskaper (Det uppskattade startdatumet kopieras från källprojektet)
- Uppdelad arbetsstruktur
- Projektets teammedlemmar
- Projektberäkningar
- Beräkning av projektutgifter

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
- Beräknat startdatum
- Slutdatum
- Insats (timmar)
- Beräknad arbetskostnad
- Beräknad utgiftskostnad

## <a name="work-breakdown-structure"></a>Uppdelad arbetsstruktur

När projektet kopieras, kopieras hela den resursinlästa uppdelade arbetsstrukturen. Namngivna resurser ersätts av allmänna resurser. Om de namngivna resurserna inte har samma arbetstider som den allmänna resursen, kommer schemat att beräknas om och varaktigheten för aktiviteten kan ändras.

## <a name="project-team-members"></a>Projektets teammedlemmar

När ett projektteam kopieras från källprojektet kopieras de allmänna resurserna. Allmänna resurstilldelningar hanteras också som de hanterades i källprojektet. Namngivna resurser kommer att konverteras till allmänna teammedlemmar.

## <a name="estimates"></a>Beräkningar

När projektet kopieras, kopieras både resurs- och utgiftsraderna för uppskattningar från källprojektet. 

Mer information om hur du programmässigt kommer åt Kopiera projekt finns i [Utveckla projektmallar med Kopiera projekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
