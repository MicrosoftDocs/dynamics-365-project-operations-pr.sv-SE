---
title: Godkännandeuppsättningar i Project Service Automation
description: Det här ämnet innehåller information om godkännandeuppsättning, förfrågningar och underuppsättningen för dessa åtgärder.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583376"
---
# <a name="approval-sets-in-project-service-automation"></a>Godkännandeuppsättningar i Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Godkännandeuppsättningar samlar godkännandeförfrågningar i mindre underuppsättningar. Med hjälp av den här grupperingen kan godkännanden bearbetas i projektordning och det går att försöka och sekvensera igen. Genom att gruppera ökar tillförlitligheten och spårningen för godkännandebearbetning för stora godkännanden.

Godkännandeuppsättningar anger det övergripande bearbetningstillståndet för de relaterade posterna. När en godkännandepost bearbetas med hjälp av en godkännandeuppsättning flyttas posten från **Skickad** till **Godkänd** och avlänkas från godkännandeuppsättningen. Om en post misslyckas när den skickas för godkännande har posten fortfarande statusen **Skickad** och godkännandeuppsättningen markeras som misslyckad. I godkännandeuppsättningen loggas felmeddelandet om felet.

## <a name="processing-approvals-and-approval-sets"></a>Bearbetning av godkännanden och godkännandeuppsättningar
Godkännanden som köas för bearbetning visas i vyn **Bearbetningsgodkännanden**. Systemet försöker bearbeta alla poster flera gånger asynkront, inklusive att försöka utföra ett godkännande igen om det inte gick att utföra tidigare försök.

I fältet **Livstid för godkännandeuppsättning** registreras antalet försök kvar att bearbeta uppsättningen innan den markeras som misslyckad.

## <a name="failed-approvals-and-approval-sets"></a>Misslyckade godkännanden och godkännandeuppsättningar
I vyn **Misslyckade godkännanden** listas alla godkännanden som kräver användaråtgärd. Öppna de associerade godkännandeuppsättningsloggarna för att identifiera orsaken till felet.
Om du väljer **Försök igen** läggs detta till i godkännandeuppsättningens livstid, förs godkännandeuppsättningen tillbaka till statusen **Bearbetar** och försöker att bearbeta de återstående posterna.

## <a name="configure-approval-sets"></a>Konfigurera godkännandeuppsättningar

###  <a name="enable-the-approval-sets-feature"></a>Aktivera funktionen Godkännandeuppsättningar
Innan du aktiverar funktionen Godkännandeuppsättningar bör du kontrollera att inga godkännanden för närvarande bearbetas.

- Gå till sidan **Projektparametrar** och välj **Funktionskontroll** > **Aktivera moderna godkännanden**.

### <a name="turn-off-the-approval-sets-feature"></a>Inaktivera funktionen Godkännandeuppsättningar
Innan du inaktiverar funktionen Godkännandeuppsättningar bör du kontrollera att inga godkännanden för närvarande bearbetas.

- Gå till sidan **Projektparametrar** och välj **Funktionskontroll** > **Inaktivera moderna godkännanden**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurera det asynkrona tröskelvärdet 
När godkännandeuppsättningar skapas flyttas bearbetning till bakgrunden när det valda antalet poster för godkännande överskrider det angivna tröskelvärdet. Använd fältet **Asynkront tröskelvärde** för att konfigurera när godkännandeprocessen ska köras synkront eller asynkront.
Giltiga värden är:

  - Noll: Alla förfrågningar ska bearbetas asynkront. 
  - Nummer som är större än noll: Godkännanden bearbetas asynkront endast när det skickade antalet godkännanden överskrider detta värde.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
