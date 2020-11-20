---
title: Kopiera ett projekt
description: I det här ämnet finns information om kopiering av projekt i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131815"
---
# <a name="copy-a-project"></a>Kopiera ett projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med Dynamics 365 Project Operations kan du snabbt skapa nya projekt genom att välja **Kopiera projekt** i formuläret **Projekt**. Om du vill kopiera ett projekt öppnar du projektet du vill kopiera och väljer **Kopiera projekt**. Åtgärden kommer att kopiera:

- Projektegenskaper
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
