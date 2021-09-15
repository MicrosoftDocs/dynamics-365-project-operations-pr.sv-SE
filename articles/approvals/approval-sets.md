---
title: Godkännandeuppsättningar
description: Detta ämne hur du arbetar med godkännandeuppsättningar, förfrågningar och underuppsättningar för dessa åtgärder.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323258"
---
# <a name="approval-sets"></a>Godkännandeuppsättningar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Godkännandeuppsättningar samlar godkännandeförfrågningar i mindre underuppsättningar. Med hjälp av denna gruppering kan godkännanden bearbetas per projekt i en särskild ordning, och det går att försöka och sekvensera på nytt. Genom att gruppera godkännandeförfrågningarna ökar tillförlitligheten och spårbarheten för bearbetning av godkännanden för stora godkännandevolymer.

Godkännandeuppsättningar anger det övergripande bearbetningstillståndet för de relaterade posterna. När en godkännandepost bearbetas med hjälp av en godkännandeuppsättning flyttas posten från **Skickad** till **Godkänd,** och posten länkas inte längre till godkännandeuppsättningen. Om en post misslyckas när den skickas för godkännande har posten fortfarande statusen **Skickad** och godkännandeuppsättningen markeras som misslyckad. I godkännandeuppsättningen loggas felmeddelandet om felet.

## <a name="processing-approvals-and-approval-sets"></a>Bearbetning av godkännanden och godkännandeuppsättningar
Godkännanden som köas för bearbetning visas i vyn **Bearbetningsgodkännanden**. Systemet bearbetar alla poster flera gånger asynkront, inklusive ett nytt försök till godkännande om tidigare försök misslyckats.

I fältet **Livstid för godkännandeuppsättning** registreras antalet försök kvar att bearbeta uppsättningen innan den markeras som misslyckad.

## <a name="failed-approvals-and-approval-sets"></a>Misslyckade godkännanden och godkännandeuppsättningar
I vyn **Misslyckade godkännanden** listas alla godkännanden som kräver användaråtgärd. Öppna de associerade godkännandeuppsättningsloggarna för att identifiera orsaken till felet.
Om du väljer **Försök igen** läggs detta till i godkännandeuppsättningens livstid, förs godkännandeuppsättningen tillbaka till statusen **Bearbetar** och försöker att bearbeta de återstående posterna.

## <a name="configure-approval-sets"></a>Konfigurera godkännandeuppsättningar

### <a name="enable-the-approval-sets-feature"></a>Aktivera funktionen Godkännandeuppsättningar
Innan du aktiverar funktionen Godkännandeuppsättningar bör du kontrollera att inga godkännanden för närvarande bearbetas.

- Gå till sidan **Projektparametrar** och välj **Funktionskontroll** > **Aktivera moderna godkännanden**.

### <a name="turn-off-the-approval-sets-feature"></a>Inaktivera funktionen Godkännandeuppsättningar
Innan du inaktiverar funktionen Godkännandeuppsättningar bör du kontrollera att inga godkännanden för närvarande bearbetas.

- Gå till sidan **Projektparametrar** och välj **Funktionskontroll** > **Inaktivera moderna godkännanden**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurera det asynkrona tröskelvärdet 
När godkännandeuppsättningar skapas flyttas bearbetning till bakgrunden när det valda antalet poster för godkännande överskrider det angivna tröskelvärdet. Använd fältet **Asynkront tröskelvärde** för att konfigurera när godkännandeprocessen ska köras synkront eller asynkront. Välj ett av följande värden:

  - Noll: Alla förfrågningar ska bearbetas asynkront. 
  - Nummer som är större än noll: Godkännanden bearbetas asynkront endast när det skickade antalet godkännanden överskrider detta värde.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
