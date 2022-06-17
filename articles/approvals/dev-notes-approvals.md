---
title: Utvecklingsanteckningar för godkännanden
description: Den här artikeln ger ytterligare utvecklarinformation om att arbeta med godkännanden.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924774"
---
# <a name="developer-notes-for-approvals"></a>Utvecklingsanteckningar för godkännanden

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen. Korrigera post övergångar garanterar följande: 

  - Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.
  - Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]