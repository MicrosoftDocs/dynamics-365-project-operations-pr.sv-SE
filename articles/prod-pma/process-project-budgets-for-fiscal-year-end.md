---
title: Överför projektbudgetar vid räkenskapsårsslut
description: Den här artikeln innehåller information om hur du kan överföra resterande budgetbelopp till framtida år och skapa budgetregisterinformation.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085673"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Överför projektbudgetar vid räkenskapsårsslut

[!include [banner](../includes/banner.md)]

När du arbetar med ett projekt för flera år kanske du har resterande budget i slutet av räkenskapsåret. Du kan överföra de resterande budgetbeloppen till ett kommande år och skapa budgetregisterinformation för beloppen i de associerade redovisningskontona. Innan du överför de återstående beloppen bör du granska och analysera de resterande budgetbeloppen.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Granska och analysera resterande budgetbelopp

Följ stegen nedan om du vill granska budgetbeloppen för årets slut för projekt, men inte föra beloppen framåt.

1. Gå till **Projekthantering och redovisning** > **Periodisk** > **Budget** > **För budget framåt**. 
2. På sidan **Process för att föra projektbudget framåt**, under fliken **Alternativ för årsslut**, kontrollerar du att **För återstående budgetbelopp framåt** inte har aktiverats.
3. Under fliken **Parametrar**, i fältet **Projektbudgetår**, väljer du det räkenskapsår som du vill visa återstående budgetbelopp för. 
4. I fältet **Inledande räkenskapsår** väljer du det räkenskapsår som du vill visa återstående budgetbelopp för. 
5. I fältet **Från prognosmodell** väljer du **Återstående budget**. 
6. Om du vill ta med projekt som uppfyller de valda villkoren och inte har någon resterande budget väljer du **Visa noll kvar**.  
7. Under fliken **Välj budget** väljer du **Hämta alla budgetar** för att läsa in alla budgetar som matchar de valda villkoren och väljer sedan **Behandla**. 
8. Om du vill utforma en databasfråga som läser in en specifik uppsättning budgetar i rutan väljer du **Hämta valda budgetar**.

Om du vill ha mer information om en specifik rad i fönstret markerar du raden och väljer **Visa budgetinformation** eller **Visa konton**.

## <a name="carry-forward-remaining-budget-amounts"></a>För resterande budgetbelopp framåt 

När du bearbetar resterande budgetbelopp kan du skapa transaktioner i redovisningen för de belopp som du för framåt. Skapa redovisningstransaktioner genom att följa stegen i avsnittet [För budgetbelopp framåt och skapa redovisningstransaktioner](#carry-forward). 

> [!NOTE]
> Budgetbelopp som förs framåt överförs till den prognosmodell som är vald på sidan **Prognosmodeller** som prognosmodell för överföring framåt.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Föra budgetbelopp framåt och skapa redovisningstransaktioner

1.  Välj **Projekthantering och redovisning** > **Periodisk** > **Budget** > **För budget framåt**. 
2. På sidan **Process för att föra projektbudget framåt** väljer du **Årsslut** och aktiverar sedan **För återstående budgetbelopp framåt** och **Skapa budgetregisterposter i redovisningen**. 
3. Under fliken **Parametrar**, i fältgruppen **Projektparametrar**, väljer du följande:

   - **Projektbudgetår**: Välj början av räkenskapsåret för vilket du vill visa återstående budgetbelopp. 
   - **Vinst och förlust**: Skapa vinst- och förlusttransaktioner i redovisningen. 
   -  **PIA**: Skapa PIA-transaktioner (pågående arbete) i redovisningen.
   -  **Lön**: Skapa löneallokeringskonton i redovisningen. 

5. I fältgruppen **Redovisning** anger du följande information: 

   - I fältet **Inledande räkenskapsår** väljer du det räkenskapsår som du vill överföra återstående budgetbelopp till för projekten. Standardvärdet är ett år efter värdet i fältet **Projektbudgetår**.
   -  I fältet **Överföringsperiod** väljer du den period som du vill skapa budgetregisterinformationen för i redovisningen. Det är vanligtvis den första perioden i det inledande räkenskapsåret.

6. I fältgruppen **Kopiera från/till** anger du följande information:

   - I fältet **Från prognosmodell** väljer du den prognosmodell för projektbudget som är kopplad till de resterande budgetbelopp du vill överföra för projekten. 
   - I fältet **Till transaktionsregistrets budgetmodell** väljer du den budgetmodell för transaktionsregistret som är kopplad till de budgetbelopp du vill överföra till redovisningen. 
   -  Välj **Överför försäljningsvaluta** om du vill använda projektets försäljningsvaluta för de redovisningstransaktioner som skapas när du överför budgetbeloppen för projekten. Om alternativet inte är valt används redovisningsvalutan för transaktionerna. 
   -  Välj **Visa noll kvar** om du vill inkludera projekt som inte har några resterande budgetbelopp, men som uppfyller de övriga kriterier som du väljer bland de projekt som visas i den nedre rutan.

7. Under fliken **Välj budget** väljer du **Hämta alla budgetar** för att läsa in alla budgetar som matchar de villkor du har valt. Om du föredrar att utforma en databasfråga som läser in en specifik uppsättning projektbudgetar i rutan väljer du **Hämta valda budgetar**.
8. För varje projekt som du vill bearbeta markerar du alternativet i början av raden för projektet.

    > [!TIP]
    > Markera alla eller de flesta av projekten genom att markera kryssrutan längst upp till vänster. Avmarkera kryssrutan för det aktuella projektet om du vill utesluta bearbetning av ett projekt.

9. Om du vill överföra de resterande budgetbeloppen för de valda projekten till det valda räkenskapsåret och skapa budgetregisterinformation i redovisningen väljer du **Behandla**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Föra budgetbelopp framåt utan att skapa redovisningstransaktioner

1. Gå till **Projekthantering och redovisning** > **Periodisk** > **Budget** > **För budget framåt**.
2. På sidan **Process för att föra projektbudget framåt**, i fältet **Alternativ för årsslut**, väljer du **För återstående budgetbelopp framåt**.
3. I gruppen **Parametrar**, i fältet **Projektbudgetår**, väljer du det räkenskapsår som du vill visa återstående budgetbelopp för.
4. I gruppen **Kopiera från/till** anger du följande information:

   - I fältet **Från prognosmodell** väljer du den prognosmodell för projektbudget som är kopplad till de resterande budgetbelopp som du vill överföra för projekten. 
   - Välj **Visa noll kvar** om du vill inkludera projekt som inte har något återstående budgetbelopp, men som uppfyller övriga villkor du har valt.
   - I gruppen **Välj budget** väljer du **Hämta alla budgetar** för att läsa in alla budgetar som matchar de villkor du har valt. Om du vill utforma en databasfråga som läser in en specifik uppsättning projektbudgetar i rutan väljer du **Hämta valda budgetar**.

5. För varje projekt som du vill bearbeta markerar du alternativet i början av raden för projektet. 
6. Välj **Behandla** för att överföra de resterande budgetbeloppen för de valda projekten till det valda räkenskapsåret.

