---
title: Godkännandeuppsättningar
description: Den här artikeln innehåller information om hur du arbetar med godkännandeuppsättningar, förfrågningar och underuppsättningar för dessa åtgärder.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918104"
---
# <a name="approval-sets"></a>Godkännandeuppsättningar

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Godkännandeuppsättningar samlar godkännandeförfrågningar i mindre underuppsättningar. Med hjälp av denna gruppering kan godkännanden bearbetas per projekt i en särskild ordning, och det går att försöka och sekvensera på nytt. Genom att gruppera godkännandeförfrågningarna ökar tillförlitligheten och spårbarheten för bearbetning av godkännanden för stora godkännandevolymer.

Godkännandeuppsättningar anger det övergripande bearbetningstillståndet för de relaterade posterna. När en godkännandepost bearbetas med hjälp av en godkännandeuppsättning flyttas posten från **Skickad** till **Godkänd,** och posten länkas inte längre till godkännandeuppsättningen. Om en post misslyckas när den skickas för godkännande har posten fortfarande statusen **Skickad** och godkännandeuppsättningen markeras som misslyckad. I godkännandeuppsättningen loggas felmeddelandet om felet.

## <a name="processing-approvals-and-approval-sets"></a>Bearbetning av godkännanden och godkännandeuppsättningar
Godkännanden som köas för bearbetning visas i vyn **Bearbetningsgodkännanden**. Systemet bearbetar alla poster flera gånger asynkront, inklusive ett nytt försök till godkännande om tidigare försök misslyckats.

I fältet **Livstid för godkännandeuppsättning** registreras antalet försök kvar att bearbeta uppsättningen innan den markeras som misslyckad.

Godkännandeuppsättningar bearbetas genom den regelbundna aktiveringen baserat på ett **molnflöde** kallat **Project Service – Projektgodkännandeuppsättningar med återkommande schema**. Detta finns i **lösningen** kallad **Project Operations**. 

Kontrollera att flödet aktiveras genom att följa stegen nedan.

1. Logga in på [flow.microsoft.com](https://powerautomate.microsoft.com) som administratör.
2. Växla till den miljö som du använder för Dynamics 365 Project Operations längst upp till höger.
3. Välj **Lösningar** om du vill lista de lösningar som har installerats i miljön.
4. I lösningslistan väljer du **Project Operations**.
5. Ändra filtret från **Alla** till **Molnflöden**.
6. Kontrollera att flödet **Project Service – Projektgodkännandeuppsättningar med återkommande schema** har angetts som **På**. Om detta inte är fallet väljer du flödet och sedan **Aktivera**.
7. Kontrollera att bearbetningen sker var femte minut genom att gå till listan **Systemjobb** i området **Inställningar** i din Dataverse-miljö för Project Operations.

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
