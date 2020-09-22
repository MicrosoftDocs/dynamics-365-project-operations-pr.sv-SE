---
title: Nyheter i Project Service Automation uppdatering version 12, v3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756216"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, uppdatering version 12
Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 12. Den här versionen har ett versionsnummer på V3.10.2.34 och är allmänt tillgänglig via en självuppdatering i oktober 2019.

## <a name="update-release-12"></a>Uppdatering version 12

### <a name="bug-fixes"></a>Felkorrigeringar

- Tid och utgift

    - Fast: meddelande om tidsinmatningsfel har uppdaterats med en mer relevant kontext.
    - Fast: rutnätet för tidsinmatning och schema visar den lodräta rullningslisten på rätt sätt vid behov.
    - Fast: Skickade kostnads- och tidsposter kan godkännas.
    - Fast: dialogrutan för bekräftelse av annullering av godkännande har korrigerats för att återspegla statusen för godkännandet när det ändrades från **godkänd** till **skickad**.
    - Fast: **pris**, **enhet** och **antal** är nu låsta i utgiftsposten efter att den har godkänts.

- Projektledning

    - Fast: **ny** åtgärd i huvudformuläret **teammedlem** har tagits bort.
    - Fast: resurstilldelningar har uppdaterats till att utgöra ett felaktigt avrundningsfel som leder till en ändring i uppgiftens slutdatum.
    - Fast: relevanta serverfel visas i aktivitetsrutnätet för användaren.
    - Fast: namnet på teammedlemmen återges nu i väljaren för aktivitetens personväljare i stället för befattningens namn.

- Resurshantering

    - Fast: information om resurskrav för projekt som skapats från en mall använder nu projektkalendern.
    - Fast: nu förvalda kunskaper och kompetenser från rollhuvuddata till resurskravet som skapats för rollen.

- Sales

    - Fast: dubbletter av objekt-ID hittas i huvudformuläret **Kontrakt**.
    - Fast: logiken har uppdaterats för att fliken **Offertanalys** ska visas så att flikens metadata visas.
    - Fast: bokföringsdatumet på den faktiska posten kommer nu från datumet då datum för tid/utgiftspost skapades, inte datumet för godkännandet.
