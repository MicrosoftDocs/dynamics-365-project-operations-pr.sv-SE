---
title: Ställ in arbetsflöden för utgiftshantering
description: Du kan konfigurera en arbetsflödesprocess för att granska och godkänna rese- och utgiftsdokument.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085694"
---
# <a name="set-up-expense-management-workflows"></a>Ställ in arbetsflöden för utgiftshantering

[!include [banner](../includes/banner.md)]

Du kan konfigurera en arbetsflödesprocess som används för att granska och godkänna rese- och utgiftsdokument. Dokument för vilka arbetsflöden kan definieras innefattar utgiftsrapporter, reserekvisitioner och förfrågningar om förskott.

Ett arbetsflöde representerar en affärsprocess. Den definierar hur ett dokument flödar i systemet och anger vem som måste utföra en uppgift eller godkänna ett dokument. Det finns flera fördelar med att använda arbetsflödessystemet i organisationen:

-   **Konsekventa processer** – du kan definiera godkännandeprocessen för specifika dokument, t.ex. inköpsrekvisitioner och utgiftsrapporter. Genom att använda arbetsflödessystemet ser du till att dokumenten bearbetas och godkänns på ett konsekvent och effektivt sätt.

-   Processens synlighet – Du kan spåra status, historik och prestandamått för en specifik arbetsflödesinstans. På det här sättet kan du fastställa om ändringar ska göras i arbetsflödet för att öka effektiviteten.

-   Centraliserad arbetslista – Användare kan visa en centraliserad arbetslista för att visa uppgifter och godkännanden som har tilldelats dem. 

**Typer av arbetsflöden som du kan skapa**

I följande tabell visas de typer av arbetsflöden som du kan skapa i **Utgift**.


|              <strong>Typ</strong>              |                   <strong>Använd den här typen för att</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Utgiftsrapport</strong>         |            Skapa godkännande arbetsflöden för utgiftsrapporter.             |
|  <strong>Automatisk bokföring av utgiftsrapporter</strong>   |        Skapa arbetsflöden för automatisk bokföring av utgiftsrapporter.        |
|       <strong>Utgiftsradobjekt</strong>        |     Skapa godkännande arbetsflöden för radobjekt på utgiftsrapporter.      |
| <strong>Automatisk bokföring av utgiftsradartiklar</strong> | Skapa arbetsflöden för automatisk bokföring för radobjekt på utgiftsrapporter. |
|       <strong>Reserekvisition</strong>       |          Skapa godkännande arbetsflöden för reserekvisitioner.           |
|      <strong>Begäran om förskott</strong>      |         Skapa godkännande arbetsflöden för begäran om förskott.          |
|        <strong>Momsåtervinning</strong>        | Skapa godkännande arbetsflöden för att momsåtervinning.  |
