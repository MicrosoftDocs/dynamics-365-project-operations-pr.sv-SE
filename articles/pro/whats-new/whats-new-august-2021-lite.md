---
title: Vad är nytt i augusti 2021 – Project Operations lite-distribution
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i augusti 2021-versionen av Project Operations lite-distributionen.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323528"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Vad är nytt i augusti 2021 – Project Operations lite-distribution

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

  - Project Operations i Dataverse-miljöversion 4.13.0.152

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- **Godkännandeuppsättningar**: Med godkännande anges gruppförfrågningar om tid, utgifter eller materialanvändningsgodkännande tillsammans i mindre underuppsättningar med åtgärder. Med hjälp av denna gruppering kan godkännanden bearbetas per projekt i en specifik ordning, och det går att försöka och sekvensera på nytt. Genom att gruppera förfrågningarna ökar tillförlitligheten och spårbarheten för bearbetning av godkännanden för stora godkännandevolymer. Mer information finns i [Godkännandeuppsättningar](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2295625 | Milstolpens namn måste kopieras från fakturaschemat till detaljinformation för fakturaraden. |
| Fakturering och prissättning | 2316323 | Rabatten ska inte vara redigerbar på en proformafaktura i Project Operations för resursbaserade scenarier. |
|   Affärsmöjlighetshantering | 2338619 | Affärsreglerna **Affärsmöjlighet** och **Offert** får endast anropas på sidor. |
| Resurshantering | 2316523 | Användning av **Skicka förfrågan** från ett resurskrav med tillhörande roll ska inte generera något fel. |
| Resurshantering | 2326885 | Om du skapar ett resurskrav via ett projekt ska inget fel visas. |
| Tid och utgift | 2335584 | Inaktuella uppgiftsflöden i tidsposten. |
| Tid och utgift | 2336884 | Tidspostknappen **Kopiera vecka** måste fungera för mer än bara den aktuella användaren. |
