---
title: Navigera i användargränssnittet
description: I det här ämne finns information om projektledning i Dynamics 365 i projektåtgärder.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127540"
---
# <a name="navigating-the-user-interface"></a>Navigera i användargränssnittet

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

## <a name="overview"></a>Översikt

Projektets huvudformulär är indelat på flera flikar. Varje flik motsvarar en annan detaljnivå i projektet.

- **Sammanfattning**: visar en beskrivning av projektet och aggregerar både planerat och faktiskt projektresultat.

    ![Fliken Sammanfattning och fält](media/navigation7.png)

- **Uppgifter**: innehåller information om uppdelad arbetsstruktur som representeras av en rutnätsvy, en trädvy och ett Gantt-schema.

    ![Fliken Uppgift och fält](media/navigation8.png)

- **Team**: ger information om projektdeltagarna. Den tilldelade insatsen för varje teammedlem sammanfattas i den här vyn.

    ![Fliken Team och fält](media/navigation9.png)

- **Resurstilldelningar**: tillhandahåller en tidsfasad vy över arbetsinsatsen för varje resurs i ett projekt.

    ![Fliken Resurstilldelningar och fält](media/navigation10.png)

- **Resursavstämning**: visar en tidsfasad vy över skillnaderna mellan tilldelningarna för varje namngiven resurs och deras bokningar.

    ![Fliken Resursavstämning och fält](media/navigation11.png)

- **Uppskattningar**: visar en tidsfasad vy över kostnads- och försäljningsuppskattningarna för ett projekt.

    ![Fliken Uppskattningar och fält](media/navigation12.png)

- **Spårning**: en vy som visar förloppet för uppgifter i uppdelad arbetsstruktur för insats, kostnader och försäljning.

    ![Fliken Spårning och fält](media/navigation13.png)

- **Försäljning**: ger djupa länkar till offerter och kontrakt som är associerade med projektet.

- **Utgiftsuppskattningar**: tillhandahåller ett rutnät som definierar projektutgifter baserat på organisationens utgiftskategorier.

    ![Fliken Utgiftsuppskattningar och fält](media/navigation14.png)

## <a name="grid-controls"></a>Rutnätskontroller

Här följer en kortfattad översikt över de typiska kontroller som finns på flikarna för projektplanering.

### <a name="refresh"></a>Uppdatera

**Uppdatera**: hämtar senaste data från servern om några ändringar gjordes efter att rutnätet lästes in.

![Knappen Uppdatera](media/navigation7.png)

### <a name="group-by"></a>Gruppera efter

**Gruppera efter**: uppdaterar en grupp av rader i rutnätet så att den motsvarar antingen resurser, roller eller kategorier utifrån användarens behov.

![Gruppera efter knapp](media/navigation6.png)

### <a name="previousnext"></a>Föregående/nästa

**Föregående**/**nästa**: uppdatera de synliga tidsperioderna för tidsfasade rutnät.

![Knapparna Föregående och Nästa](media/navigation2.png)

### <a name="timescale"></a>Tidsskala

**Tidsskala**: ändra sammansättningen av tidsfasdata mellan dagar, veckor, månader och år.

![Knappen Tidsskala](media/navigation3.png)

### <a name="expand"></a>Utöka

**Visa**: återger det synliga rutnätet på fullskärm så att fler roller kan visas.

![knappen Visa detaljer](media/navigation4.png)

### <a name="time-phase-by"></a>Tidsfas efter

**Tidsfas efter**: uppdatera grupperingen av raderna i rutnätet så att det visar kostnadsuppskattningar för försäljningsuppskattningar. Den här kontrollen gäller även för uppskattningsskript och spårningsrutnät.

![Tidsfas efter knapp](media/navigation0.png)

### <a name="add-column"></a>Lägg till kolumn

**Lägg till kolumn**: gör att användaren kan definiera de synliga kolumnerna i rutnätet. Endast kolumner som är färdiga kan läggas till i rutnäten i formuläret **Projektplanering**.

![Lägg till kolumnknapp](media/navigation5.png)
