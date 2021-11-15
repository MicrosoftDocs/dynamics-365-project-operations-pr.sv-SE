---
title: Uppdateringar av Project Operations
description: I det här ämnet finns information om släppta versioner av Dynamics 365 Project Operations.
author: sigitac
ms.date: 10/04/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 493218d53075f3044adce47bed8ecdc031cca8e7
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783445"
---
# <a name="project-operations-updates"></a>Uppdateringar av Project Operations

_**Gäller till:** Project Operations för resursscenarier/icke lagerbaserade scenarier, Lite-distribution – avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations komponenter

Dynamics 365 Project Operations består av två komponenter:

- Project Operations i Dataverse-miljön täcker funktioner från affärsmöjlighet till proforma-fakturering. Dataverse används i Lite-distribution och resursscenarier/icke-lagerbaserade scenarier i Project Operations.
- Projektledning och redovisning i Dynamics 365 Finance-miljön behandlar hanteringsfunktioner för utgifter, projektredovisning och intäktsredovisning. Finance and Operations-appmiljön används i Project Operations för resursscenarier/icke lagerbaserade scenarier och Project Operations för lagerbaserade/produktionsbaserade scenarier.

## <a name="project-operations-release-notes"></a>Viktig information om Project Operations
- Den senaste viktig informationen om Project Operations för [Resursbaserade/icke-lagerbaserade](whats-new-oct-2021-resource-based.md) scenarier.
- Den senaste viktig informationen om Project Operations för [Lite-distribution](../pro/whats-new/whats-new-oct-2021-lite.md) scenarier.
- Den senaste viktig informationen om Project Operations för [lagerbaserade/produktionsbaserade](../prod-pma/whats-new/whats-new-jul-2021-stocked.md) scenarier.

## <a name="project-operations-latest-version"></a>Project Operations senaste version

| Project Operations i Dataverse-miljö | Projektledning och redovisning i Finance and Operations-appmiljöer | 
| --- | --- |
| 4.26.0.145 | 10.0.21 |

För Project Operations Resource/icke lagerbaserade scenarier rekommenderar vi att du använder orkestrering för dubbelriktad skrivning och 2.2.2.83 eller senare.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Utgivningsplan för Project Operations i Dataverse-miljö

Uppdateringar för Project Operations i Dataverse-miljö är tillgängliga varje månad. 

| Station | Region | Aktuellt versionsnummer | Automatiska uppdateringar för Lite-distribution | Automatiska uppdateringar för distribution av resurser/icke-lager | Nästa versionsnummer | Nästa version är vanligtvis tillgänglig |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| Station 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Första utgivning         |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 03 december 2021   |
| Station 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Sydamerika         |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 03 december 2021   |
|   &nbsp;  | Kanada                |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 03 december 2021   |
|   &nbsp;  | Indien                 |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 03 december 2021   |
|   &nbsp;  | Frankrike                |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 03 december 2021   |
|   &nbsp;  | Sydafrika          |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 03 december 2021   |
| Station 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japan                 |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 10 december 2021   |
|   &nbsp;  | Asien och stillahavsområdet          |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 10 december 2021   |
|   &nbsp;  | Storbritannien         |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 10 december 2021   |
|   &nbsp;  | Oceanien               |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 10 december 2021   |
|   &nbsp;  | Förenade Arabemiraten  |  4.26.0.145     | 12 november 2021  | 19 november 2021   | TBD                 | 10 december 2021   |
| Station 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.25.0.91      | Slutför           | Slutför            | 4.26.0.145          | 12 november 2021   |
| Station 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Nordamerika         |  4.25.0.91      | Slutför           | Slutför            | 4.26.0.145          | 19 november 2021   |


## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Utgivningsplan för projektledning och redovisning i Finance and Operations-appmiljön

Uppdateringar för projektledning och redovisning publiceras åtta gånger per år.

|Version som stöds| Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.22     |      3 september 2021      |        22 oktober 2021           |                          5 november 2021                            | 14 januari 2022   |
|    10.0.21      |         02 augusti 2021     |           17 september 2021      |                             1 oktober 2021                          |  10 december 2021 |


Målinriktade utgivningsdatum kan ändras. Mer information finns i [Tjänstuppdatering tillgänglig](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|Målversion | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.23     |      15 oktober 2021       |        10 december 2021          |                          31 december 2021                           | 18 mars 2022     |
|     10.0.24     |      3 december 2021       |        14 januari 2022           |                          4 februari 2022                            | 15 april 2022     |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
