---
title: Prestanda för projektfakturaförslag
description: Detta ämne ger information om prestandaförbättringar av projektfakturaförslag.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005728"
---
# <a name="project-invoice-proposal-performance"></a>Prestanda för projektfakturaförslag

[!include [banner](../includes/banner.md)]

När du skapar ett nytt fakturaförslag kan du stöta på prestandaproblem när antalet projekt och delprojekt ökar. För att förbättra prestanda är en funktion tillgänglig som minskar den tid som krävs för att skapa ett nytt fakturaförslag för bokförda projekttransaktioner.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Aktivera förbättring av prestanda för projektfakturaförslag
Så här aktiverar du funktionen för förbättring av prestanda för projektfakturaförslag:

1.  Gå till **Funktionshantering** > **Alla**. Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.
2.  Välj **Aktivera nu**.
3.  Uppdatera webbläsaren och skapa sedan ett nytt fakturaförslag.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Inaktivera förbättring av prestanda för projektfakturaförslag
Slutför följande steg för att stänga av prestandaförbättringen av projektfakturaförslaget.

1.  Gå till **Funktionshantering** > **Alla**. Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.
2.  Välj **Inaktivera**.
3.  Uppdatera webbläsaren.

> [!NOTE]
> Fakturaförslagsresultat kan inte tillämpas när faktureringsregler har aktiverats.
> 
> Under batchprocessen för att skapa fakturaförslag delar antalet underaktiviteter uppgifterna till ett högsta antal baserat på antalet kontrakt med fakturabara transaktioner, oavsett vad du har angett. Om du till exempel anger **3** för antalet underaktiviteter för att skapa fakturaförslag i batch och det bara finns två kontrakt med faktureringsbara transaktioner skapas endast två underaktiviteter.
