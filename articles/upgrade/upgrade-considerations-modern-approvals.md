---
title: Att tänka på vid uppgradering till moderna godkännanden
description: Artikeln omfattar de punkter administratörer bör tänka på när de aktiverar funktionen för modernt godkännande.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931766"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Att tänka på vid uppgradering till moderna godkännanden 

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Som en del av lanseringsvåg 1-versionen för april 2022 aktiveras funktionen för moderna godkännanden som standard. Den här funktionen förbättrar tillförlitligheten för godkännandelogiken och garanterar att du kan avgöra orsaken om godkännandelogiken misslyckas.

Som en del av den här ändringen uppdateras statusändringar för projektgodkännanden. Statusen går nu direkt från **Skickad** till **Godkänd**. **Väntande** har inte längre någon status för godkännanden. Om du vill fastställa om ett godkännande väntar på att godkännas kontrollerar du att detta godkännande ingår i en godkännandeuppsättning och granskar sedan tillståndet för den bifogade godkännandeuppsättningen.

## <a name="before-you-upgrade"></a>Innan du uppgraderar

Innan du uppgraderar till Moderna godkännanden bör du kontrollera att du inte har några väntande godkännanden. För moderna godkännanden används inte statusen **Väntar**. Därför bearbetas inte godkännanden som fortfarande markerade som **Väntar** efter uppgraderingen.

## <a name="after-you-upgrade"></a>Efter uppgradering

När du har uppgraderat till Moderna godkännanden måste en administratör verifiera att molnflödet som bearbetar godkännanden har aktiverats.

1. Logga in på [flow.microsoft.com](https://flow.microsoft.com)
2. Växla miljön till den miljö som du har uppgraderat längst upp till höger på sidan.
3. Välj **Lösningar** om du vill lista de lösningar som har installerats i miljön.
4. I lösningslistan väljer du **Project Operations** eller **Project Service**.
5. Ändra filtret från **Alla** till **Molnflöden**.
6. Bekräfta att alternativet **Project Service – Projektgodkännandeuppsättningar med återkommande schema** har angetts som **På**. Om detta inte är fallet väljer du flödet och sedan **Aktivera**.
7. Kontrollera att bearbetningen sker var femte minut genom att granska listan **Systemjobb** i avsnittet **Inställningar**.

## <a name="short-term-rollback"></a>Återställning på kort sikt

Om du inte kan implementera ändringarna, eller om du stöter på ett svårt problem med den här funktionen, kan du tillfälligt återställa till det ursprungliga godkännandeflödet genom att utföra följande steg:
1. Logga in i din miljö och verifiera att det inte finns några väntande godkännanden.
2. Gå till **Inställningar** > **Projektparametrar**.
3. Välj **Funktionskontroll** och välj Sedan **Moderna godkännanden** du vill inaktivera funktionen.

## <a name="removing-the-feature-flag"></a>Ta bort funktionsflaggan

I lanseringsvåg 2 för oktober 2022 kommer möjligheten att inaktivera den här funktionen att tas bort.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
