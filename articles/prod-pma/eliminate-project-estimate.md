---
title: Eliminera en projektuppskattning
description: I det här ämnet finns information om hur du eliminerar en projektuppskattning efter att den har slutförts.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085593"
---
# <a name="eliminate-a-project-estimate"></a>Eliminera en projektuppskattning

[!include [banner](../includes/banner.md)]

Projektuppskattningar ger den ekonomiska vyn för arbete som har uppskattats och schemalagts för ett projekt. Om du vill arbeta med uppskattningar för ett projekt måste du koppla projektet till ett uppskattningsprojekt. Ett uppskattningsprojekt bygger alltid på ett befintligt projekt, men flera projekt kan emellertid referera till ett enda uppskattningsprojekt. Det går endast att koppla projekt med fast pris och investering till uppskattningsprojekt och projekten måste tillhöra samma projektgrupp som uppskattningsprojektet.

Om du vill eliminera ett uppskattningsprojekt måste det vara klart. I följande steg förklaras hur du eliminerar en uppskattning.

1. Gå till **Projektledning och redovisning** > **Alla projekt** och öppna projektet. 
2. Under fliken **Hantera** väljer du **Uppskattningar** och på sidan **Uppskatta** väljer du **Eliminera**.
3. På sidan **Eliminera uppskattning** under fliken **Allmänt** anger du följande alternativ:

   - **Periodkod** : Välj periodkoden för att välja lämpliga uppskattningsprojekt. 
   - **Uppskattningsdatum** : Välj lämpligt uppskattningsdatum för eliminering.
   - **Eliminera med PIA-varningar** : Aktivera det här alternativet om du vill att aviseringar ska visas när en uppskattning som är kopplad till ett pågående arbete (PIA) ska elimineras. Om det här alternativet inte är aktiverat kan eliminering inte fortsätta om det finns icke uppskattade transaktioner. 
   > [!NOTE]
   > Det här alternativet är endast tillgängligt när eliminering tillämpas på ett uppskattningsprojekt. Det är inte tillgängligt om du använder periodiska bokningar. Den här inställningen fungerar med inställningarna under fliken **Uppskattning** på sidan **Projektparametrar** i fältgruppen **Tillåt eliminering när transaktioner som inte uppskattas finns**.
   - **Ange att stadiet har slutförts** : Aktivera det här alternativet om du vill att uppskattningsprojektets stadium ska vara anges som **Slutfört** efter att elimineringen har körts.
   - **Skriv ut uppskattningslista** : Välj vilken information som ska inkluderas när uppskattningslistan skrivs ut.
   - **Visa informationslogg** : Aktivera det här alternativet om du vill visa informationsloggen.
   - **Bokföringsdatum** : Välj datumet då uppskattningen bokförs i transaktionsregistret.

4.  Välj **OK**.
5. När elimineringsprocessen har slutförts visas det eliminerade uppskattningsprojektet med ett negativt värde. 

Om du inte har för avsikt att eliminera en uppskattning kan du markera den eliminerade uppskattningen och välja **Återför eliminering**.   