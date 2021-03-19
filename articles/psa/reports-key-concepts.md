---
title: Nyckelbegrepp
description: Det här ämnet ger information om nyckelbegrepp för resurshantering i Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 704aadab3dd1b8b3e22ecdb15cf97cc7cbba1a23
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283345"
---
# <a name="key-concepts"></a>Nyckelbegrepp

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I följande tabell definieras viktiga begrepp som används i Dynamics 365 Project Service Automation-appen.

| Begrepp                    | Definition |
|----------------------------|------------|
| Projektteammedlem        | Som en del av projektteamet kan en projektteammedlem vara en namngiven resurs som innehåller bokningar, en namngiven resurs som inte har några bokningar eller en generisk resurs. Generiska resurser saknar bokningar, är inte lokala för projektet och har inte kapacitetsbegränsningar mellan projekten. |
| Projektgeneriska resurs   | En resursplatshållare som du kan använda för att skapa en projektplan för ett team och personal utan att behöva känna till den namngivna resursen. Projektkalendern används som den generiska resursens kalender. Generiska resurser kan läggas till i ett projektteam och tilldelas uppgifter. |
| Bokade timmar               | Resurstimmar är en fast bokad åtgärd mot ett projekt för att garantera att projektarbetet har slutförts. Bokade timmar förbrukas från resursens totala kapacitet. Bokningar gäller endast för namngivna resurser, inte för generiska resurser. |
| Tilldelade timmar             | Resurstimmarna tilldelas till aktiviteter i projektschemat. Tilldelningar kan vara antingen mot namngivna resurser eller generiska resurser. Tilldelningar kan vara oberoende av bokningar. |
| Timmar som krävs             | Kapaciteten som krävs, men som ännu inte har uppfyllts av en namngiven resurs. Obligatoriska timmar är endast relevanta för allmänna teammedlemmar som har genererat resurskrav. |
| Begäran                     | Aktuell och inkommande arbetsbelastning. I Project Service Automation visas efterfrågan som resurskrav eller resursbegäranden. |
| Resurskrav       | En entitet som används för att fånga upp obligatoriska timmar, start- och slutdatum, färdigheter, geografi och andra prissättningsdimensioner för de resurser som krävs. Resurskrav genereras antingen från projektteammedlemmar eller individuellt skapade. |
| Resursbegäran           | En entitet som används som ett "kuvert" för att bära resurskravet som måste uppfyllas av en resursansvarig. |
| Resursens standardroll      | Rollen som en resurs är grupperad under för resursutnyttjandeberäkning. Resursen antas ha den kompetens som krävs för rollen och för att uppfylla målutnyttjande för rollen. |
| Resursens organisationsenhet | Organisationsenhet som en resurs är tilldelad. |
| Profil                    | Uppgift, krav eller tilldelningens timmar när de delas upp i en daglig fördelning. En fem dagars 40-timmars uppgift kan till exempel läggas till åtta timmar per dag över fem dagar. |
| Vyn avstämningar        | En vy som visar bokningarna och tilldelningarna för varje projektmedlem i gruppen. I den här vyn kan projektledaren söka efter alla matchningar mellan bokningar och tilldelningar och åtgärda eventuella fel som uppstår om de inte stämmer. |
| Arbetstider                 | En entitet som används för att identifiera resursens kapacitet och arbetstider och lediga tider. Entiteten kallas även för resurskalendern. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]