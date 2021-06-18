---
title: Utvecklingsanteckningar för godkännanden
description: I det här ämnet finns ytterligare utvecklarinformation om att arbeta med godkännanden.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996813"
---
# <a name="developer-notes-for-approvals"></a>Utvecklingsanteckningar för godkännanden

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen. Korrigera post övergångar garanterar följande: 

  - Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.
  - Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]