---
title: Vad är nytt i juni 2022 – Project Operations lite-distribution
description: Denna artikel innehåller information om de kvalitetsuppdateringar som är tillgängliga i distributionsversionen av Microsoft Dynamics 365 Project Operations lite för juni 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031215"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Vad är nytt i juni 2022 – Project Operations lite-distribution

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.43.0.77 eller 4.43.0.119

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
