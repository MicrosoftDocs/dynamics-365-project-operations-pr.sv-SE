---
title: Uppdateringar av Project Operations
description: I det här ämnet finns information om släppta versioner av Dynamics 365 Project Operations.
author: sigitac
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5e37bc90a74e6bc9f1bf3d3820a34c3f4c3496d
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942861"
---
# <a name="project-operations-updates"></a>Uppdateringar av Project Operations

_**Gäller till:** Project Operations för resursscenarier/icke lagerbaserade scenarier, Lite-distribution – avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations komponenter

Dynamics 365 Project Operations består av två komponenter:

- Project Operations i Dataverse-miljön täcker funktioner från affärsmöjlighet till proforma-fakturering. Dataverse används i Lite-distribution och resursscenarier/icke-lagerbaserade scenarier i Project Operations.
- Projektledning och redovisning i Dynamics 365 Finance-miljön behandlar hanteringsfunktioner för utgifter, projektredovisning och intäktsredovisning. Finance and Operations-appmiljön används i Project Operations för resursscenarier/icke lagerbaserade scenarier och Project Operations för lagerbaserade/produktionsbaserade scenarier.

## <a name="project-operations-release-notes"></a>Viktig information om Project Operations
- Den senaste viktig informationen om Project Operations för [Resursbaserade/icke-lagerbaserade](whats-new-dec-2021-resource-based.md) scenarier.
- Den senaste viktig informationen om Project Operations för [Lite-distribution](../pro/whats-new/whats-new-dec-2021-lite.md) scenarier.
- Den senaste viktig informationen om Project Operations för [lagerbaserade/produktionsbaserade](../prod-pma/whats-new/whats-new-oct-2021-stocked.md) scenarier.

## <a name="project-operations-latest-version"></a>Project Operations senaste version

| Project Operations i Dataverse-miljö | Projektledning och redovisning i Finance and Operations-appmiljöer | 
| --- | --- |
| 4.27.0.242 | 10.0.23 |

För Project Operations Resource/icke-lagerbaserade scenarier rekommenderar vi att du använder Orchestration för dubbelriktad skrivning version 2.3.1.15 eller senare.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Utgivningsplan för Project Operations i Dataverse-miljö

Uppdateringar för Project Operations i Dataverse-miljö är tillgängliga varje månad. 

| Station | Region | Aktuellt versionsnummer | Automatiska uppdateringar för Lite-distribution | Automatiska uppdateringar för distribution av resurser/icke-lager | Nästa versionsnummer | Nästa version är vanligtvis tillgänglig |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| Station 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Första utgivning         |  4.27.0.242     | Slutfört*          | Slutfört*           | TBD                 | 14 januari 2022    |
| Station 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Sydamerika         |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 14 januari 2022    |
|   &nbsp;  | Kanada                |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 14 januari 2022    |
|   &nbsp;  | Indien                 |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 14 januari 2022    |
|   &nbsp;  | Frankrike                |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 14 januari 2022    |
|   &nbsp;  | Sydafrika          |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 14 januari 2022    |
| Station 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japan                 |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 21 januari 2022    |
|   &nbsp;  | Asien och stillahavsområdet          |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 21 januari 2022    |
|   &nbsp;  | Storbritannien         |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 21 januari 2022    |
|   &nbsp;  | Oceanien               |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 21 januari 2022    |
|   &nbsp;  | Förenade Arabemiraten  |  4.27.0.242     | Slutförd           | 07 januari 2022    | TBD                 | 21 januari 2022    |
| Station 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.26.0.155     | Slutförd           | 07 januari 2022    | 4.27.0.242          | 10 januari 2022    |
| Station 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Nordamerika         |  4.26.0.155     | 07 januari 2022   | 14 januari 2022    | 4.27.0.242          | 17 januari 2022    |

>[!Note]
> - Slutförd* – Automatiska uppdateringar slutfördes med version 4.27.0.195.


## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Utgivningsplan för projektledning och redovisning i Finance and Operations-appmiljön

Uppdateringar för projektledning och redovisning publiceras åtta gånger per år.

|Version som stöds| Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.23     |      15 oktober 2021       |        10 december 2021          |                          31 december 2021                           | 18 mars 2022     |
|     10.0.22     |      3 september 2021      |        22 oktober 2021           |                          5 november 2021                            | 14 januari 2022   |


Målinriktade utgivningsdatum kan ändras. Mer information finns i [Tjänstuppdatering tillgänglig](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|Målversion | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.24     |      3 december 2021       |        14 januari 2022           |                          4 februari 2022                            | 15 april 2022     |
|     10.0.25     |      31 januari 2022       |        18 mars 2022             |                          1 april 2022                               | 10 juni 2022      |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
