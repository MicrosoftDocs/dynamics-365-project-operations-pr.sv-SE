---
title: Nyheter i februari 2022 – Distribution av Project Operations lite
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i distributionsversionen av Project Operations Lite för februari 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574590"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Nyheter i februari 2022 – Distribution av Project Operations lite

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.28.0.120

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

I den här versionen kan du lägga till upp till 300 teammedlemmar i ett enda projekt. Tidigare var gränsen för antalet teammedlemmar 150. Mer information finns i [Projektgränser](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2497369 | Materialkorrigeringen måste följa datumvärdet i parametrarna för **Korrigering**. |
| Fakturering och prissättning | 2498697 | Förbättrade säkerhetskonfigurationen för **Tidspoståterkallelse**. |
| Fakturering och prissättning | 2517455 | Åtgärden **Uppdaterad fakturaradstransaktion** får inte utlösas flera gånger samtidigt för samma faktura. |
| Fakturering och prissättning | 2517465 | Åtgärden **Inaktivera fakturaradsinformation** blockeras eftersom den inte stöds. |
| Fakturering och prissättning | 2556660 | Åtgärdade kontrollerna för datumverkställning som görs i prislistan som är bifogad till en projektparameterpost. |
|   Affärsmöjlighetshantering | 2369202 | Rättade affärslogiken som bekräftar att prislistor med överlappande verkställandedatum kan kopplas till samma projektkontrakt. |
|   Affärsmöjlighetshantering | 2385965 | Rättade beteendet på fliken **Kunder** på sidan **Projektkontrakt** när du väljer **Spara och stänga**. |
