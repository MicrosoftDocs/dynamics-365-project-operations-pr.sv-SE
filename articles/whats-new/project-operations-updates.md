---
title: Uppdateringar av Project Operations
description: I det här ämnet finns information om släppta versioner av Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0dfcd47e0c8ac2d9edd45049ffefb6e364c8aa4b
ms.sourcegitcommit: f366fe0ba062e4e500921854563d57ee3bfd1ce5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/09/2022
ms.locfileid: "8732953"
---
# <a name="project-operations-updates"></a>Uppdateringar av Project Operations

_**Gäller till:** Project Operations för resurs-/icke-lagerbaserade scenarier, Lite-distribution – avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_



## <a name="project-operations-components"></a>Project Operations komponenter

Dynamics 365 Project Operations består av två komponenter:

- Project Operations i Dataverse-miljön täcker funktioner från affärsmöjlighet till proforma-fakturering. Dataverse används i Lite-distribution och resurs-/icke-lagerbaserade scenarier i Project Operations.
- Projekthantering och redovisning i Dynamics 365 Finance-miljön omfattar funktioner för utgiftshantering, projektredovisning och intäktsidentifiering. Appmiljön för ekonomi och drift används i Project Operations för resurs-/icke-lagerbaserade scenarier och Project Operations för lagerbaserade/produktionsbaserade scenarier.

## <a name="project-operations-release-notes"></a>Viktig information om Project Operations
- Den senaste viktig informationen om Project Operations för [Resursbaserade/icke-lagerbaserade](whats-new-may-2022-resource-based.md) scenarier.
- Den senaste viktig informationen om Project Operations för [Lite-distribution](../pro/whats-new/whats-new-may-2022-lite.md) scenarier.
- Den senaste viktig informationen om Project Operations för [lagerbaserade/produktionsbaserade](../prod-pma/whats-new/whats-new-oct-2021-stocked.md) scenarier.

## <a name="project-operations-latest-version"></a>Project Operations senaste version

| Project Operations i Dataverse-miljö | Projekthantering och redovisning i appar för ekonomi och drift | 
| --- | --- |
| 4.42.0.70 | 10.0.26 |

För resurs-/icke-lagerbaserade scenarier för Project Operations rekommenderar vi att du använder Orchestration för dubbelriktad skrivning version 2.3.1.15 eller senare.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Utgivningsplan för Project Operations i Dataverse-miljö

Uppdateringar för Project Operations i Dataverse-miljö är tillgängliga varje månad. 

| Station | Region | Aktuellt versionsnummer | Automatiska uppdateringar för Lite-distribution | Automatiska uppdateringar för distribution av resurser/icke-lager | Nästa versionsnummer | Nästa version är vanligtvis tillgänglig |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| Station 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Första utgivning         |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
| Station 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Sydamerika         |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
|   &nbsp;  | Kanada                |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
|   &nbsp;  | Indien                 |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
|   &nbsp;  | Frankrike                |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
|   &nbsp;  | Sydafrika          |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
|   &nbsp;  | Schweiz           |  4.42.0.70      | Slutförd           | Slutförd            | TBD                 | 27 maj 2022        |
| Station 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japan                 |  4.42.0.70      | 13 maj 2022       | 13 maj 2022        | TBD                 | 03 juni 2022       |
|   &nbsp;  | Asien och stillahavsområdet          |  4.42.0.70      | 13 maj 2022       | 13 maj 2022        | TBD                 | 03 juni 2022       |
|   &nbsp;  | Storbritannien         |  4.42.0.70      | 13 maj 2022       | 13 maj 2022        | TBD                 | 03 juni 2022       |
|   &nbsp;  | Oceanien               |  4.42.0.70      | 13 maj 2022       | 13 maj 2022        | TBD                 | 03 juni 2022       |
|   &nbsp;  | Förenade Arabemiraten  |  4.42.0.70      | 13 maj 2022       | 13 maj 2022        | TBD                 | 03 juni 2022       |
| Station 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.41.0.45      | Slutförd           | Slutförd            | 4.42.0.70           | 13 maj 2022        |
| Station 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Nordamerika         |  4.41.0.45      | Slutförd           | Slutförd            | 4.42.0.70           | 20 maj 2022        |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Versionsschema för projekthantering och redovisning i appmiljön för ekonomi och drift

Uppdateringar för projektledning och redovisning publiceras åtta gånger per år.

|Version som stöds| Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.26     |      4 mars 2022          |        15 april 2022             |                          29 april 2022                              | 15 juli 2022      |
|     10.0.25     |      31 januari 2022       |        18 mars 2022             |                          1 april 2022                               | 10 juni 2022      |


Målinriktade utgivningsdatum kan ändras. Mer information finns i [Tjänstuppdatering tillgänglig](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|Målversion | Tillgänglighet i förhandsversion (PEAP) | Allmänt tillgänglig (automatisk uppdatering) | Startdatum för schema för automatisk uppdatering (via LCS-uppdateringsinställningar) |   Slut på tjänsten   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.27     |      22 april 2022         |        17 juni 2022              |                          1 juli 2022                                | 16 september 2022 |
|     10.0.28     |      27 maj 2022           |        15 juli 2022              |                          29 juli 2022                               | 21 oktober 2022   |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
