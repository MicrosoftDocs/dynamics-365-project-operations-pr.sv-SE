---
title: Förskott
description: I det här ämnet finns information om förskott.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908642"
---
# <a name="cash-advance"></a>Förskott

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Ett förskott gör det möjligt för anställda att låna pengar från sitt företag innan de får utgifter. När ett begärt förskott godkänns och betalas kan medarbetaren använda sig av pengarna för de affärsutgifter de är på väg att ådra sig. 

## <a name="create-and-submit-a-cash-advance-request"></a>Skapa och skicka in en förskottsbegäran

1. Under **Mina utgifter** väljer du **Förskott** > **Ny** för att skapa en ny förskottsbetalning. 
2. På sidan **Ny förskottsbegäran** anger du syftet med utgiften och väljer den plats där kostnad ska påföras.
3. Ange det begärda beloppet och valutan och välj sedan **Spara**. 
4. När du är redo att skicka in förskottsbegäran går du till sidan **Förskottsbegäran** och väljer **Arbetsflöde** > **Skicka in**.

## <a name="modify-a-cash-advance-request"></a>Ändra en förskottsbegäran

Du kan ändra en förskottsbegäran om den inte har skickats för godkännande.

1. Under **Mina utgifter: förskott** söker du efter och markerar de förskott du vill redigera.
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

När du skapar och skickar en utgiftsrapport för den förskottsbetalning som du redan har tagit emot justeras utgifterna automatiskt mot förskottet. Om förskottet är större än utgiftsbeloppet måste du returnera saldot till företaget med hjälp av utgiftskategorin **Returnera kontanter**. Om förskottet som betalats av företaget är mindre än det belopp som du har betalat måste företaget betala mellanskillnaden. 

### <a name="example"></a>Exempel
Du planerar att resa för en konferens från Stockholm till Göteborg. Du skapar en förskottsbegäran för 30 000 kr då du har uppskattat att detta är den ungefärliga kostnaden för konferensbiljetten, flygningar, hotell, måltider och taxiresor. Du kommer inte att få betalt om din chef inte har godkänt förfrågan. Efter att chefen har godkänt betalningen betalas det begärda förskottet på 30 000 kr till ditt bankkonto. Du ska sedan delta i konferensen. När resan är klar upptäcker du att endast de totala utgifterna var 27 900 kr. Välj **Kontanter** i fältet **Betalningsmetod** och skicka in utgiften på 27 900 kr. Det inskickade utgiftsbeloppet justeras automatiskt mot förskottet för de 30 000 kronorna som lånades ut till dig. Du är nu skyldig en mellanskillnad på 2 100 kr (30 000 - 27 900) till företaget, som du kan betala till företaget med hjälp av utgiftskategorin **Returnera kontanter**. 
