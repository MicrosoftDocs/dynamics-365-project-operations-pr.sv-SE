---
title: Skapa prognosmodeller för projektbudgetar
description: I det här ämnet beskrivs hur du skapar en prognosmodell för resterande budgetar.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271060"
---
# <a name="create-forecast-models-for-project-budgets"></a>Skapa prognosmodeller för projektbudgetar 

[!include [banner](../includes/banner.md)]

I det här ämnet beskrivs hur du skapar en prognosmodell för resterande budgetar. I ett projekt som är underställt budgetkontroll används två typer av budget: ursprunglig och resterande. När du skapar en projektbudget måste du ange de prognosmodeller för ursprunglig och resterande budget som skapades på sidan **Prognosmodeller**. Projektbudgetar som bygger på de angivna modellerna skapas när du fastställer projektbudgeten.

> [!NOTE]
> En prognosmodell som används för budgetkontroll kan inte ha en delmodell eller användas som en delmodell.

1. Välj **Projekthantering och redovisning** > **Konfiguration** > **Prognoser**  > **Prognosmodeller**.
2. Välj **Ny** om du vill skapa en ny prognosmodell och ange sedan ID-nummer och namn för den nya modellen. 
3. Ange alternativet **Stoppad** till **Ja** om du vill förhindra att prognosraderna för prognosmodellen ändras. 
4. Om prognosraderna som modellen är kopplad till ska generera kassaflödesprognoser i redovisningen anger du **Inkludera i kassaflödesprognoser** till **Ja**. 
5. Om du vill använda projektdatumet som fakturadatum anger du **Prognosfakturadatum** till **Ja**. 
6. I fältet **Budgettyp** väljer du en av följande modelltyper:

   - **Ursprunglig budget**: Använd de ursprungliga budgetbeloppen som har fastställts när den inledande budgeten skapas och godkänns.
   - **Resterande budget**: Använd resterande budgetbelopp under projektets livslängd. Saldon i denna prognosmodell minskas genom faktiska transaktioner och ökas eller minskas genom budgetrevideringar.
   - **Överför**: Använd de överförda budgetbeloppen för projektet. Överföring är en frivillig process som kan köras för att överföra oanvända budgetbelopp från ett räkenskapsår till ett annat.

7. Ange följande alternativ efter behov:

   - Aktivera **Prognosfakturadatum** om du vill använda projektdatumet som fakturadatum.
   - Aktivera **Prognos med PIA** för prognos baserad på pågående arbete (PIA) och välj sedan typ av PIA. 
   - Du kan behålla den förvalda **budgettypen** som **Ingen** eller ange en ny typ. Budgettypen kan inte ändras när du har ändrat en post.     
    > [!NOTE]
    > Om du ändrar den förvalda budgettypen blir inga andra alternativ tillgängliga för uppdatering och du kan inte återanvända prognosmodellen. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]