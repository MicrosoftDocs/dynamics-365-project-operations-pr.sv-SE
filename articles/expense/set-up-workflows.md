---
title: Ställ in arbetsflöden för utgiftshantering
description: Du kan konfigurera en arbetsflödesprocess som används för att granska och godkänna rese- och utgiftsdokument.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001043"
---
# <a name="set-up-workflows-for-expense-management"></a>Ställ in arbetsflöden för utgiftshantering

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan konfigurera en arbetsflödesprocess för att granska och godkänna rese- och utgiftsdokument. Du kan definiera arbetsflöden för utgiftsrapporter, reserekvisitioner och begäran om förskott.

Ett arbetsflöde representerar en affärsprocess och definierar hur ett dokument flödar i systemet. I arbetsflödet anges också vem som måste slutföra en uppgift eller godkänna ett dokument. Det finns flera fördelar med att använda arbetsflödessystemet i organisationen:

- **Konsekventa processer**: du kan definiera godkännande processen för specifika dokument, t.ex. inköpsrekvisitioner och utgiftsrapporter. Genom att använda arbetsflödessystemet ser du till att dokumenten bearbetas och godkänns på ett konsekvent och effektivt sätt.
- **Processens synlighet**: du kan spåra status, historik och prestandamått för en specifik arbetsflödesinstans. På det här sättet kan du fastställa om ändringar ska göras i arbetsflödet för att öka effektiviteten.
- **Centraliserad arbetslista**: användare kan visa en centraliserad arbetslista för att visa uppgifter och godkännanden som har tilldelats dem. 

## <a name="workflow-types"></a>Arbetsflödestyper

I följande tabell visas de typer av arbetsflöden som du kan skapa i **utgiftshantering**.


|              <strong>Typ</strong>              |                   <strong>Använd den här typen för att</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Utgiftsrapport för automatiskt godkännande</strong> |            Skapa godkännande arbetsflöden för utgiftsrapporter.             |
|  <strong>Automatisk bokföring av utgiftsrapporter</strong>   |        Skapa arbetsflöden för automatisk bokföring av utgiftsrapporter.        |
|       <strong>Utgiftsradobjekt</strong>        |     Skapa godkännande arbetsflöden för radobjekt på utgiftsrapporter.      |
| <strong>Automatisk bokföring av utgiftsradartiklar</strong> | Skapa arbetsflöden för automatisk bokföring för radobjekt på utgiftsrapporter. |
|       <strong>Reserekvisition</strong>       |          Skapa godkännande arbetsflöden för reserekvisitioner.           |
|      <strong>Begäran om förskott</strong>      |         Skapa godkännande arbetsflöden för begäran om förskott.          |
|        <strong>Momsåtervinning</strong>        | Skapa godkännande arbetsflöden för att momsåtervinning.  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]