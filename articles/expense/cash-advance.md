---
title: Förskott
description: I denna artikel finns information om förskott.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: bc270944faa7c16d2e97a988495a2a16380ba879
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931536"
---
# <a name="cash-advance"></a>Förskott

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Ett förskott gör det möjligt för anställda att låna pengar från sitt företag innan de får utgifter. När ett begärt förskott godkänns och betalas kan medarbetaren använda sig av pengarna för de affärsutgifter de är på väg att ådra sig. 

## <a name="create-and-submit-a-cash-advance-request"></a>Skapa och skicka in en förskottsbegäran
Så här skapar du ett nytt förskott och skickar en begäran om förskott: 

1. Under **Mina utgifter** väljer du **Förskott** > **Nytt**. 
2. På sidan **Ny förskottsbegäran** anger du syftet med utgiften och väljer den plats där kostnad ska påföras.
3. Ange det begärda beloppet och valutan och välj sedan **Spara**. 
4. När du är redo att skicka in förskottsbegäran går du till sidan **Förskottsbegäran** och väljer **Arbetsflöde** > **Skicka in**.

## <a name="modify-a-cash-advance-request"></a>Ändra en förskottsbegäran

Du kan ändra en förskottsbegäran om den inte har skickats för godkännande.

1. Under **Mina utgifter: förskott** letar du upp det förskott du vill redigera.
2. Välj **Redigera** och gör nödvändiga ändringar i förskottsförfrågan. 
3. Välj **Spara och stäng**.


## <a name="view-cash-advance-requests"></a>Visa begäran om förskott
Du kan granska listan över alla förskott i utkast, skickade, i granskning eller betalda under **Mina utgifter: förskott**. 

## <a name="approve-cash-advance-requests"></a>Godkänn begäran om förskott

Chefer eller användare som konfigurerats som godkännare i arbetsflödet kan godkänna de förskott som skickas till dem för granskning. 

1. Om du vill godkänna ett förskott går du till **Behandla förskott** och väljer **Förskott som jag granskar**.
2. Välj förskott som du vill granska och välj **Godkänn**.  

## <a name="pay-cash-advances"></a>Betala förskott 
Följande procedur slutförs vanligen av en revisor eller en användare med redovisningsbehörigheter.

1. Om du vill skicka godkända förskott väljer du **Godkända förskott** och väljer sedan **Betala och överför**.  
2. Ange journalinformationen för förskott och klicka sedan på **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Skicka en utgiftsrapport mot ett betalat förskott 

När du skapar och skickar en utgiftsrapport för det förskott som du redan har fått, justeras utgifterna automatiskt mot det förskottet. Om förskottet är större än utgiftsbeloppet måste du returnera saldot till företaget med hjälp av utgiftskategorin **Returnera kontanter**. Om förskottet som betalas av företaget är mindre än det belopp du har lagt ut för, måste företaget ersätta dig för detta. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Välj förskott som ska användas för dina utgifter
Innan du skickar en utgiftsrapport kan du välja ett förskott som justeras mot utgiftstransaktionerna i rapporten. Om du vill använda den här funktionen måste följande två funktioner aktiveras från arbetsytan för **funktionshantering**:

  - Ny typ av utgiftsrapporter
  - Möjlighet att mappa kostnader till utgiftsrader
 
 När de här funktionerna har aktiverats:
 
  - Du kan lägga till ett eller flera förskott för varje utgiftsrad.
  - Det tillgängliga saldot för ett förskott visas i realtid när en utgiftsrapport sparas. På så sätt kan du bearbeta utgiftstransaktioner och returnera en kassatransaktion samtidigt.
  - Du kan välja flera förskott för en kostnadstransaktion.
  - Information om förskottsavstämning kan fås med hjälp av en fråga. 
 
Om du inte använder dessa funktioner kommer funktionen att förbli densamma, med befintliga kassar automatiskt reducerade efter det att en utlägg skickas in.

### <a name="example"></a>Exempel 
Du planerar att resa från Seattle till New York City för en konferens. Du skapar en förskottsförfrågan för 3 000 USD utifrån den beräknade kostnaden för konferensbiljetten, flyg, hotell, måltider och taxiresor. Du kommer inte att få betalt om inte din chef godkänner denna förfrågan. Efter att chefen har godkänt betalningen betalas det begärda förskottet på 30 000 kr till ditt bankkonto. Du ska sedan delta i konferensen. När resan är klar upptäcker du att endast de totala utgifterna var 27 900 kr. Välj **Kontant** i fältet **Betalsätt** och skicka in dina utgifter uppgående till 2 790 USD. Det inskickade utgiftsbeloppet justeras automatiskt mot förskottet för de 30 000 kronorna som lånades ut till dig. Du får nu ett saldo på 210 USD (3 000 - 2 790) som du kan återföra tiull företaget med hjälp av utgiftskategorin **Returnera medel**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
