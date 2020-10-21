---
title: Förstå projektstatus
description: I det här ämnet finns information om den status som projekt i Dynamics 365 Project Operations har tilldelats.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965698"
---
# <a name="understand-project-status"></a>Förstå projektstatus

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


I avsnittet **Status** på sidan **Projektentitet** ges en sammanfattning av ett projekts hälsa baserat på kostnad och arbetsinsats.


## <a name="status-summary-fields"></a>Fält för statussammanfattning

- Fältet **Övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status. Detta fält använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker. 
- I fältet **Kommentarer** kan projektledaren ange kommentarer om statusen. 
- Fältet **Status uppdaterades senast** går inte att redigera. Värdet i det här fältet är en tidstämpel som anger när statusen senast uppdaterades.
- Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsrutnätet. När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva uppdateras dessa fält till **Före**. När schema och kostnadsavvikelse för rotnoden är negativa anges dessa fält till **Efter**.
