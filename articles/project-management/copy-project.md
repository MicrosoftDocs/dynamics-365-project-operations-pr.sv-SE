---
title: Kopiera ett projekt
description: I det här ämnet finns information om att kopiera projekt i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574452"
---
# <a name="copy-a-project"></a>Kopiera ett projekt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med Dynamics 365 Project Operations kan du snabbt skapa nya projekt genom att välja **Kopiera projekt** i formuläret **Projekt**. Om du vill kopiera ett projekt öppnar du projektet du vill kopiera och väljer **Kopiera projekt**. Åtgärden kopierar följande:

- Projektegenskaper 
- Uppdelad arbetsstruktur
- Projektets teammedlemmar
- Projektberäkningar
- Beräkning av projektutgifter
- Projektmaterialberäkningar
- Projektchecklistor
- Projektbuckets

## <a name="project-properties"></a>Projektegenskaper

När projektet kopieras, kopieras värdena i följande fält:

| Fält | Ej lagerförda material för Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Kunder | :heavy_check_mark: | :heavy_check_mark: | |
| Kalendermall | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Kontrakteringsenhet | :heavy_check_mark: | :heavy_check_mark: | |
| Ägande företag | :heavy_check_mark: | | |
| Projektledare | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Övergripande projektstatus | :heavy_check_mark: | :heavy_check_mark: | |
| Kommentarer | :heavy_check_mark: | :heavy_check_mark: | |
| Beräkningar | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Beräknat startdatum</p><p><strong>Obs!</strong> I det här fältet anges det datum då projektet skapas från kopian. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Beräknat slutdatum</p><p><strong>Obs!</strong> Datumet i fältet justeras utifrån startdatum för det nya projektet som gjordes från kopian.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Insats (timmar) | :heavy_check_mark: | :heavy_check_mark: | |
| Beräknad arbetskostnad | :heavy_check_mark: | :heavy_check_mark: | |
| Beräknad utgiftskostnad | :heavy_check_mark: | :heavy_check_mark: | |
| Beräknad materialkostnad | | :heavy_check_mark: | |

> [!NOTE]
> Kopieringsprojektet är en långvarig körning. Projektposter, deras relevanta attribut och många relaterade entiteter kopieras också. Eftersom åtgärden tar lång tid är målprojektsidan låst efter att kopian har startat och kan redigeras tills kopieringen är slutförd.

## <a name="work-breakdown-structure"></a>Uppdelad arbetsstruktur

När projektet kopieras, kopieras hela den resursinlästa uppdelade arbetsstrukturen. Namngivna resurser ersätts av allmänna resurser. Om de namngivna resurserna inte har samma arbetstider som den allmänna resursen beräknas schemat om och varaktigheten för uppgiften kan komma att ändras.

## <a name="project-team-members"></a>Projektets teammedlemmar

När ett projektteam kopieras från källprojektet kopieras de allmänna resurserna. Allmänna resurstilldelningar hanteras också som de hanterades i källprojektet. Namngivna resurser kommer att konverteras till allmänna teammedlemmar.

> [!NOTE]
> Teammedlemmar och tilldelningar kopieras inte i Project for the Web.

## <a name="estimates"></a>Beräkningar

När projektet kopieras kopieras rader för resurs-, utgifts- och materialberäkning från källprojektet. 

Mer information om hur du programmässigt kommer åt Kopiera projekt finns i [Utveckla projektmallar med Kopiera projekt](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Offerter och kontrakt

Offerter och kontrakt är inte kopplade till målprojektet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
