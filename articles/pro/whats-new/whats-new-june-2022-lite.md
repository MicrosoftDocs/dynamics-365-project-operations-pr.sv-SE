---
title: Vad är nytt i juni 2022 – Project Operations lite-distribution
description: Denna artikel innehåller information om de kvalitetsuppdateringar som är tillgängliga i distributionsversionen av Microsoft Dynamics 365 Project Operations lite för juni 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959503"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Vad är nytt i juni 2022 – Project Operations lite-distribution

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.43.0.77

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Legotillverkning | 2708885 | Åtgärdade felmeddelandet som visas när en användare skapar en bokningsbar resursbokningsrubrikpost där ingen bokningsbar resurs fylls i. |
| Projektplanering och spårning | 2629441 | Korrigerade arbetsflödesutlösningslogiken för att hjälpa till att förhindra en loop för loopar när projektuppgifter uppdateras. |
| Tid och utgift | 2641209 | För tidsinmatning som importeras från tilldelningar/bokningar måste det finnas en bokningsbar resursreferens. |
| Projektplanering och spårning | 2651148 | Projektdokumentrubriken måste vara försedd med ett meddelande.|
| Projektplanering och spårning | 2653145 | Lade till valideringar för att säkerställa att en projektpost inte kan skapas med icke-giltiga tecken i namnet. |
| Tid och utgift | 2654710 | Korrigerade filtreringen på sidan **Godkännanden**. |
| Fakturering och prissättning | 2667805 | Lade till valideringar för att förhindra att faktiska fakturerade försäljningar skapas om det inte finns några fakturerade försäljningsfakturering. |
| Fakturering och prissättning | 2668378 | Ytterligare valideringar har lagts till för att förhindra att anpassade priser läggs till såvida inte ett logiskt namn och ett fältnamn fylls i. |
| Tid och utgift | 2700428 | Förbättrad godkännandelogik för att se till att andra godkännandeuppsättningar för projektet kan bearbetas även om en av godkännandeuppsättningarna har fastnat i systemjobb. |
