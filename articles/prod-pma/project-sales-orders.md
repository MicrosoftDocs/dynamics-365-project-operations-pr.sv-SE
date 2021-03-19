---
title: Projektförsäljningsorder för tids- och materialprojekt
description: I det här ämnet beskrivs hur du skapar projektbaserade försäljningsorder för tids- och materialprojekt.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289076"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektförsäljningsorder för tids- och materialprojekt

[!include[banner](../includes/banner.md)]

I den här ämnet beskrivs hur du skapar en försäljningsorder för ett projekt. Det går endast att skapa försäljningsorder för projekt av typen **tid och material**.

Om ett tids- och materialprojekt har flera finansieringskällor i projektkontraktet måste du aktivera parametern **Tillåt försäljningsorder för projekt med flera finansieringskällor** på sidan **Projektledning och redovisningsparametrar**. 

> [!NOTE]
> - Stöd för projektförsäljningsorder med flera finansieringskällor kan startas med hjälp av programversionen 10.0.2 och senare.
> - Parametern för att aktivera stöd för projektförsäljningsorder med flera finansieringskällor tas bort i april 2020 utgivningsvåg, efter vilken funktionen alltid är aktiverad.

Du kan skapa projektbaserade försäljningsorder på två sätt:

- Gå till själva projektet. I åtgärdsrutan väljer du **hantera > artikeluppgifter > försäljningsorder**. Projektinformationen används som standard för försäljningsordern från projektet. Om projektkontraktet har fler än en finansieringskälla måste du välja finansieringskällan för att ange kunden för försäljningsordern. Om det bara finns en finansieringskälla för projektet kommer kunden att ställas in automatiskt.
- Gå till listsidan **Alla försäljningsorder** och skapa en ny försäljningsorder. Du måste välja projektet för försäljningsordern. När du har valt projektet kommer kunden att ställas in från finansieringskällan, eller så måste du välja finansieringskälla om projektkontraktet har flera finansieringskällor.



[!INCLUDE[footer-include](../includes/footer-banner.md)]