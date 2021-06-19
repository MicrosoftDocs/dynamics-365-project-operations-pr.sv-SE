---
title: Uppdateringar av Project Operations
description: I det här ämnet finns information om släppta versioner av Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d19148c868aa5be77db59e70fcf1fb8b7de6868c
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213467"
---
# <a name="project-operations-updates"></a>Uppdateringar av Project Operations

_**Gäller till:** Project Operations för resursscenarier/icke lagerbaserade scenarier, Lite-distribution - avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations komponenter

Dynamics 365 Project Operations består av två komponenter:

- Project Operations i Dataverse-miljön täcker funktioner från affärsmöjlighet till proforma-fakturering. Dataverse används i Lite-distribution och resursscenarier/icke-lagerbaserade scenarier i Project Operations.
- Projektledning och redovisning i Dynamics 365 Finance-miljön behandlar hanteringsfunktioner för utgifter, projektredovisning och intäktsredovisning. Finance and Operations-appmiljön används i Project Operations för resursscenarier/icke lagerbaserade scenarier och Project Operations för lagerbaserade/produktionsbaserade scenarier.

## <a name="project-operations-release-notes"></a>Viktig information om Project Operations
- Den senaste viktig informationen om Project Operations för [Resursbaserade/icke-lagerbaserade](whats-new-may-2021-resource-based.md) scenarier.
- Den senaste viktig informationen om Project Operations för [Lite-distribution](../pro/whats-new/whats-new-may-2021-lite.md) scenarier.
- Den senaste viktig informationen om Project Operations för [lagerbaserade/produktionsbaserade](../prod-pma/whats-new/whats-new-apr-2021-stocked.md) scenarier.

## <a name="project-operations-latest-version"></a>Project Operations senaste version

| Project Operations i Dataverse-miljö | Projektledning och redovisning i Finance and Operations-appmiljöer | 
| --- | --- |
| 4.10.0.186 | 10.0.18 |

För Project Operations Resource/icke lagerbaserade scenarier rekommenderar vi att du använder orkestrering för dubbelriktad skrivning och 2.2.2.60 eller senare.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Utgivningsplan för Project Operations i Dataverse-miljö

Uppdateringar för Project Operations i Dataverse-miljö är tillgängliga varje månad. 

| Station | Region | Aktuellt versionsnummer | Automatiska uppdateringar för Lite-distribution | Automatiska uppdateringar för distribution av resurser/icke-lager | Nästa versionsnummer | Nästa version är vanligtvis tillgänglig |
|-----------|-----------------------|-----------------|--------------|---------------------|---------------------|---------------------|
| Station 1 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Första utgivning         |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
| Station 2 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Sydamerika         |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
|    &nbsp; | Kanada                |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
|   &nbsp;  | Indien                 |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
|   &nbsp;  | Frankrike                |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
|   &nbsp;  | Förenade Arabemiraten  |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
|   &nbsp;  | Sydafrika          |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 28-Maj-21           |
| Station 3 |      &nbsp;           |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japan                 |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 04 juni 21          |
|   &nbsp;  | Asien och stillahavsområdet          |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 04 juni 21          |
|   &nbsp;  | Storbritannien         |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 04 juni 21          |
|   &nbsp;  | Oceanien               |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 04 juni 21          |
| Station 4 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.10.0.186     | Slutför     | Slutför            | TBD                 | 11 juni 21          |
| Station 5 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Nordamerika         |  4.10.0.186     | Slutför     | 11 juni 21          | TBD                 | 18 juni 21          |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Utgivningsplan för projektledning och redovisning i Finance and Operations-appmiljön

Uppdateringar för projektledning och redovisning publiceras åtta gånger per år.

|          Version som stöds          | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.18          |        5 mars 2021        |           16 april 2021          |                            30 april 2021                            |    16 juli 2021   |
|          10.0.17          |       1 februari 2021      |           19 mars 2021          |                             2 april 2021                            |    11 juni 2021   |

Målinriktade utgivningsdatum kan ändras. Mer information finns i [Tjänstuppdatering tillgänglig](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|          Målversion          | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.19          |        23 april 2021       |            18 juni 2021           |                             2 juli 2021                             | 17 september 2021 |
|          10.0.20          |         28 maj 2021        |           16 juli 2021           |                             30 juli 2021                             |  22 oktober 2021  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
