---
title: Utvecklingsanteckningar för godkännanden
description: I det här ämnet finns ytterligare utvecklarinformation om att arbeta med godkännanden.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579742"
---
# <a name="developer-notes-for-approvals"></a>Utvecklingsanteckningar för godkännanden

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen. Korrigera post övergångar garanterar följande: 

  - Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.
  - Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]