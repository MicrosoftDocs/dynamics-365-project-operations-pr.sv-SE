---
title: Konfigurera projektresurser
description: I det här ämnet finns information om hur du konfigurerar eller begär projektresurser.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288761"
---
# <a name="set-up-project-resources"></a>Konfigurera projektresurser

[!include [banner](../includes/banner.md)]

Du måste ange en kalender och associera den med en medarbetare eller arbetare. Kalendern används för att schemalägga projektet och arbetstiden för de resurser som reserveras för projektet. Under kalenderinstallationen kan projektledarna göra resursutjämning som en del av resursoptimeringen. Begränsningar kan anges för resurser utifrån kalenderschemat. Du kan skapa en kalender på sidan **kalendrar**.

När du konfigurerar en arbetare som en projektresurs kan du välja bland arbetare som arbetar i det företag som du konfigurerar resurser för. Alternativt kan du välja arbetare från andra företag i organisationen. Dessa arbetare kallas för koncerninterna resurser.

I följande procedurer förklaras hur du konfigurerar en arbetare som en projektresurs i företaget och hur du skapar en koncernintern projektresurs.

## <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurera en arbetare som en projektresurs

1. På sidan **arbetare** i listan **arbetare** väljer du den arbetare som du vill lägga till som en projektresurs i listan arbetare och öppnar sedan arbetarens post.
2. I åtgärdsfönstret, välj **Projekt** &gt; **Inställning** &gt; **Projektinställningar**.
3. Välj en kalender och stäng sidan.

Du kan även ange standardprojekt för en resurs som en typ av förtilldelning. Förtilldelningar kan användas när resurs chefen eller projektledaren vet vilka projektresursen kommer att arbeta i förväg. Förtilldelningar kan också baseras på en förfrågan från en projekt sponsor eller kund. Om du vill förtilldela ett projekt fördelat på sidan **Tilldela projekt** på fliken **Projekt** i listan **Återstående projekt** välj lämpligt projekt.

## <a name="set-up-an-intercompany-resource"></a>Konfigurera en koncernintern resurs

När du konfigurerar en arbetare som en koncernintern resurs måste du fylla i inställningarna både i långivande bolaget och låntagande bolaget.

### <a name="in-the-lending-company"></a>I långivande bolaget

1. I Finance kontrollera att långivande bolaget är valt och slutför proceduren i det föregående avsnittet "Konfigurera en arbetare som projektresurs".
2. På sidan **Koncernintern redovisning** klicka på **Ny**.
3. I fältet **juridisk person-ID** välj långivande bolag. Fyll i de återstående fälten efter behov och välj sedan **Spara**.
4. På sidan **Överföringspris** klicka på **Ny**.
5. I fältet **låntagande juridisk person** välj rätt bolag.
6. Om du vill låna ut till det låntagande bolaget endast till den resurs du skapade i början av det här avsnittet markerar du i fältet **resurs** namnet på den resurs som du har skapat. För att göra alla resurser i det långivande bolaget tillgängligt för det låntagande bolaget, lämna fältet **Resurs** tom.
7. På sidan **Projektledning och redovisningsparametrar** på fliken **Koncerninternt** ange alternativet **Aktivera koncernintern resursschemaläggning och tidrapport** till **Ja**.

### <a name="in-the-borrowing-company"></a>I låntagande bolaget

- På sidan **Resurslista** i sökfiltret ange namnet på den resurs som du skapade för det långivande bolaget för att verifiera att namnet ingår i resurslistan för det långivande bolaget.

## <a name="request-project-resources"></a>Begär projektresurser
Med funktionerna för schemaläggning av projektresurser kan du bara distribuera personalresurser för åtaganden eller projekt. Aktivera den här funktionen genom att utföra följande uppgifter eller kontrollera att de har slutförts:

- Ställ in nummerserier.
- Ställ in arbetsflöden för projekthantering och redovisning.
- Aktivera arbetsflöden för resursförfrågan.

När föregående aktiviteter har slutförts kan du utföra följande uppgifter som du behöver:

- Skapa en resursförfrågan från en bemannad resurs med mjuka bokningar.
- Övervaka resursförfrågningar.
- Uppfyll resursförfrågningar.
- Begära en personalresurs från en WBS.
- Boka resurser i ett projekt utan att behöva begära en personalresurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]