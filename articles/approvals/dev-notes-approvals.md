---
title: Utvecklingsanteckningar för godkännanden
description: I det här ämnet finns ytterligare utvecklarinformation om att arbeta med godkännanden.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290291"
---
# <a name="developer-notes-for-approvals"></a>Utvecklingsanteckningar för godkännanden

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen. Korrigera post övergångar garanterar följande: 

  - Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.
  - Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]