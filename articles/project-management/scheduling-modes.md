---
title: Schemaläggningslägen
description: I det här ämnet finns information om schemaläggningslägen.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588436"
---
# <a name="scheduling-modes"></a>Schemaläggningslägen

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


Dynamics 365 Project Operations gör att organisationer kan definiera hur de hanterar ändringar av nyckelvariabler i uppgifter inom den uppdelade arbetsstrukturen. Utifrån organisationens specifika behov kan projektansvariga ändra schemaläggningsläget när ett projekt skapas.

Det finns tre tillgängliga schemaläggningslägen i Project Operations:

  - Fast varaktighet (det här är standardläget)
  - Fast insats (*Arbete*)
  - Fasta enheter

Värdena som påverkas av definitionen i ett visst schemaläggningsläge bestäms av följande formel:

  Insats = Varaktighet x enheter

När du definierar ett projekts schemaläggningsläge ställer du in ett av dessa värden som sedan inte kan ändras. Om du har värdet som en konstant prioriteras det, vilket meddelar systemet att det inte ska ändras när de två andra värdena ändras. Följande tabell innehåller information om effekten av att välja ett visst läge.

| **I denna uppgift**             | **Om du reviderar enheter**   | **Om du reviderar varaktighet** | **Om du reviderar insats**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Uppgift med fasta enheter     | Varaktighet beräknas om. | Insats beräknas om.    | Varaktighet beräknas om. |
| Uppgift med fast insats    | Varaktighet beräknas om. | Enheter beräknas om.    | Varaktighet beräknas om. |
| Uppgift med fast varaktighet  | Insats beräknas om.   | Insats beräknas om.    | Enheter beräknas om.   |

Mer information om vad ett visst läge innebär finns i [Ändra uppgiftstyp för bättre schemaläggning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). I ämnet används termen **Arbete** i stället för **Insats**.

## <a name="change-the-organizations-scheduling-mode"></a>Ändra organisationens schemaläggningsläge

Definiera en organisations schemaläggningsläge genom att följa stegen nedan.

1. Gå till **Inställningar** \> **Allmänt** \> **Parametrar** och välj projektparametern. 
2. På sidan **Projektparametrar** väljer du standardschemaläggningsläget för organisationen och definierar om projektansvarig kan åsidosätta inställningen när ett nytt projekt skapas.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Ändra inställningen för schemaläggningsläge för ett projekt

Om en organisation tillåter att projektansvarig åsidosätter standardschemaläggningsläget kan projektansvarig göra ändringen när hen skapar ett nytt projekt. När projektet har sparats går det dock inte att ändra schemaläggningsläget.

## <a name="copied-projects"></a>Kopierade projekt

Eftersom ett projekt skapas när åtgärden kopiera projekt vidtas kan inte projektansvarig ställa in schemaläggningsläge. Målprojektet använder som standard alltid det läge som har definierats på organisationsnivå.

## <a name="copied-tasks"></a>Kopierade uppgifter

När en uppgift kopieras från ett projekt till ett annat, ärver uppgiften schemaläggningsläget för målprojektet.
