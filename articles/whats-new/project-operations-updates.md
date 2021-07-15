---
title: Uppdateringar av Project Operations
description: I det här ämnet finns information om släppta versioner av Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 951ce2f277c0c2c447ee5b2e7add4febbc8486d9
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433585"
---
# <a name="project-operations-updates"></a>Uppdateringar av Project Operations

_**Gäller till:** Project Operations för resursscenarier/icke lagerbaserade scenarier, Lite-distribution - avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations komponenter

Dynamics 365 Project Operations består av två komponenter:

- Project Operations i Dataverse-miljön täcker funktioner från affärsmöjlighet till proforma-fakturering. Dataverse används i Lite-distribution och resursscenarier/icke-lagerbaserade scenarier i Project Operations.
- Projektledning och redovisning i Dynamics 365 Finance-miljön behandlar hanteringsfunktioner för utgifter, projektredovisning och intäktsredovisning. Finance and Operations-appmiljön används i Project Operations för resursscenarier/icke lagerbaserade scenarier och Project Operations för lagerbaserade/produktionsbaserade scenarier.

## <a name="project-operations-release-notes"></a>Viktig information om Project Operations
- Den senaste viktig informationen om Project Operations för [Resursbaserade/icke-lagerbaserade](whats-new-july-2021-resource-based.md) scenarier.
- Den senaste viktig informationen om Project Operations för [Lite-distribution](../pro/whats-new/whats-new-july-2021-lite.md) scenarier.
- Den senaste viktig informationen om Project Operations för [lagerbaserade/produktionsbaserade](../prod-pma/whats-new/whats-new-jul-2021-stocked.md) scenarier.

## <a name="project-operations-latest-version"></a>Project Operations senaste version

| Project Operations i Dataverse-miljö | Projektledning och redovisning i Finance and Operations-appmiljöer | 
| --- | --- |
| 4.12.0.148 | 10.0.20 |

För Project Operations Resource/icke lagerbaserade scenarier rekommenderar vi att du använder orkestrering för dubbelriktad skrivning och 2.2.2.83 eller senare.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Utgivningsplan för Project Operations i Dataverse-miljö

Uppdateringar för Project Operations i Dataverse-miljö är tillgängliga varje månad. 

| Station | Region | Aktuellt versionsnummer | Automatiska uppdateringar för Lite-distribution | Automatiska uppdateringar för distribution av resurser/icke-lager | Nästa versionsnummer | Nästa version är vanligtvis tillgänglig |
|-----------|-----------------------|-----------------|--------------|---------------------|---------------------|---------------------|
| Station 1 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Första utgivning         |  4.12.0.148     | Slutför     | 09-juli-21          | TBD                 | 06-augusti-21        |
| Station 2 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Sydamerika         |  4.12.0.148     | 09-juli-21   | 16-juli-21          | TBD                 | 06-augusti-21        |
|    &nbsp; | Kanada                |  4.12.0.148     | 09-juli-21   | 16-juli-21          | TBD                 | 06-augusti-21        |
|   &nbsp;  | Indien                 |  4.12.0.148     | 09-juli-21   | 16-juli-21          | TBD                 | 06-augusti-21        |
|   &nbsp;  | Frankrike                |  4.12.0.148     | 09-juli-21   | 16-juli-21          | TBD                 | 06-augusti-21        |
|   &nbsp;  | Förenade Arabemiraten  |  4.12.0.148     | 09-juli-21   | 16-juli-21          | TBD                 | 06-augusti-21        |
|   &nbsp;  | Sydafrika          |  4.12.0.148     | 09-juli-21   | 16-juli-21          | TBD                 | 06-augusti-21        |
| Station 3 |      &nbsp;           |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japan                 |  4.11.0.164     | Slutför     | Slutför            | 4.12.0.148          | 09-juli-21          |
|   &nbsp;  | Asien och stillahavsområdet          |  4.11.0.164     | Slutför     | Slutför            | 4.12.0.148          | 09-juli-21          |
|   &nbsp;  | Storbritannien         |  4.11.0.164     | Slutför     | Slutför            | 4.12.0.148          | 09-juli-21          |
|   &nbsp;  | Oceanien               |  4.11.0.164     | Slutför     | Slutför            | 4.12.0.148          | 09-juli-21          |
| Station 4 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.11.0.164     | Slutför     | Slutför            | 4.12.0.148          | 16-juli-21          |
| Station 5 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Nordamerika         |  4.11.0.164     | Slutför     | 09-juli-21          | 4.12.0.148          | 23-juli-21          |



## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Utgivningsplan för projektledning och redovisning i Finance and Operations-appmiljön

Uppdateringar för projektledning och redovisning publiceras åtta gånger per år.

|          Version som stöds          | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.19          |        23 april 2021       |            18 juni 2021           |                             2 juli 2021                             | 17 september 2021 |
|          10.0.18          |        5 mars 2021        |           16 april 2021          |                            30 april 2021                            |    16 juli 2021   |


Målinriktade utgivningsdatum kan ändras. Mer information finns i [Tjänstuppdatering tillgänglig](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|          Målversion          | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.20          |         28 maj 2021        |           16 juli 2021           |                             30 juli 2021                             |  22 oktober 2021  |
|          10.0.21          |         02 augusti 2021     |           17 september 2021      |                             1 oktober 2021                           |  10 december 2021  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
