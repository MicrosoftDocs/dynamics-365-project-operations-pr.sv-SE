---
title: Nytt i december 2021 – Distribution av Project Operations Lite
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i distributionsversionen av Project Operations Lite för december 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942999"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Nytt i december 2021 – Distribution av Project Operations Lite

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

### <a name="subcontract-management"></a>Underleverantörshantering 

- [Underkontraktering av projektteammedlemmar](../subcontracting/subcontracting-project-team-members.md): En projektledare kan skapa namngivna eller generiska teammedlemmar med underleverantörer eller underleverantörsrader för att påverka bemanning och uppskattning.
- [Underleverantörsalternativ för projektteammedlemmar](../subcontracting/subcon-options.md): När projektledare gör bemanningsval för namngivna eller generiska projektteammedlemmar kan han eller hon granska befintliga underleverantörer eller skapa nya underleverantörer för en eller flera projektteammedlemmar. 
- [Kostnadsuppskattning för underleverantörstilldelning](../subcontracting/costing-subcon-ra.md): Projektkostnadsuppskattning tar i beaktande underleverantörstilldelningar och kostnadsför dem med hjälp av inköpsprislistan som är associerad med underleverantörer. 
- [Konfigurera schemaläggningstavlan så att den visar kontraktarbetare och underleverantörskapacitet](../subcontracting/configure-sb-subcon.md): Schemaläggningstavla i Project Operations kan nu konfigureras för att söka efter och föreslå kontraktarbetartyper av bokningsbara resurser och underleverantörskapacitet tillsammans med anställda. Den här konfigurationen kan användas när du söker efter resurser i samband med bemanning av ett visst projektkrav eller när du söker utanför ett projektkravs sammanhang.
- [Bemanna ett projekt med kontraktarbetare och underleverantörskapacitet](../subcontracting/staffing-cw.md): Kontraktarbetare kan nu bokas för projekt genom erfarenhet på schemaläggningstavlan.
- [Registrera tid, utgifter och materialanvändning i projekt för underleverantörskomponenter](../subcontracting/recording-subcon-actuals.md): Kontraktarbetare kan registrera tid och utgifter, och projektteammedlemmar kan även registrera användning av inköpta material med en underleverantör på ett projekt. Detta resulterar i att kostnaderna för projekt som använder köpt kapacitet eller material registreras korrekt.
- [Tillståndsövergångar på ett underleverantörskontrakt](../subcontracting/subcon-states.md): Underleverantörskontrakt kan bekräftas för att slutföra förhandlingen med leverantören, stängas för att indikera slutförande av leveransen eller avbrytas för att indikera avslutande av kontraktet med leverantören innan leveransen slutförs.

### <a name="task-planning"></a>Uppgiftsplanering
- Förbättrad felsökning för systemadministratörer. När en användare inte kan öppna ett projekt kan administratören granska icke-licensrelaterade fel som genererats från Project for the Web i [projektschemaläggningsloggar](../../project-management/schedule-api-logs.md).
- [Använd checklistorna för uppgifter i Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). I Microsoft Project for the Web kan du lägga till en checklista för en uppgift för att hålla ordning på specifika objekt.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Planering och spårning | 2392596 | Schema-API:er tillåter nu uppdateringar av fälten **Resterande insats**, **Slutförd insats** och **% slutförd**. |
| Planering och spårning | 2478497 | Schema-API:er för fälten **Aktivitetsnummer** och **Uppgifts-ID** kan vara tomma vid inmatning eftersom systemet fyller i dem med hjälp av automatisk numrering.|
| Tid och utgift | 2468135 | Antalet godkännanden minskas från fem till tre. |
| Tid och utgift | 2468188 | Åtgärdare problemet med loggtext som överskrider den maximala längden i attributet **anteckningstext** för entiteten **anteckning**. |
