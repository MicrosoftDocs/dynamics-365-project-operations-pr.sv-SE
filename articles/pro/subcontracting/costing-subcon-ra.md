---
title: Kostnadsuppskattning av underleverantörers resurstilldelningar
description: Den här artikeln innehåller information om hur Microsoft Dynamics 365 Project Operations beräknar kostnadsuppskattningar av underleverantörers resurstilldelningar.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522678"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Kostnadsuppskattning av underleverantörers resurstilldelningar

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Uppgiftstilldelningar för kontrakterade projektteammedlemmar kostnadsförs med hjälp av prislistan **Inköp** som är bifogad till kontraktet i den relaterade teammedlemsposten. Detta skiljer sig från hur anställdas resurstilldelningar kostnadsförs då uppgiftstilldelningar för medarbetarens resurser kostnadsförs med hjälp av prislistan **Kostnad** som är bifogad till den kontrakterande enheten för projektet. 

För generiska projektteammedlemmar som är underleverantörer kostnadsförs uppgifterna med hjälp av en rollbaserad prislista i inköpsprislistan som är bifogad till kontraktet. Inköpspriser kan också anges specifikt för varje resurs. Dessa resursspecifika priser får prioritet när tilldelningar av kostnadsuppgifter för namngivna projektteammedlemmar är kontraktarbetare. 

Prioriteten av att använda rollspecifikt inköpspris jämfört med resursspecifikt styrs av prissättningsdimensionens prioritet i **Parametrar > Beloppsbaserade prissättningsdimensioner**.

Den här funktionen med dynamiskt härledda priser baserat på inköpspriser för underleverantörer liknar metoden för beräkningen av utgifter och faktureringskostnader för heltidsanställda. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Skapa uppgiftstilldelningar för att få kostnadsuppskattningar för underleverantörer

Uppgiftstilldelningar för underleverantörer kan skapas på två sätt: 
- Med hjälp av fliken **Uppgifter**.
- Med hjälp av fliken **Team**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Skapa resurstilldelningar med hjälp av fliken Uppgifter
Med hjälp av listan **Resurser** under fliken **Uppgifter** för en specifik uppgift kan du skapa en uppgiftstilldelning för en namngiven resurs eller en generisk resurs. Om du väljer en namngiven resurs från listrutan **Tilldelad resurs** i uppgiften och den här resursen är en kontraktarbetare, tilldelas den namngivna resursen till uppgiften och en motsvarande post för en projektteammedlem skapas med arbetartypen inställd på **Kontraktarbetare** och **Giltighet** inställd på **Ogiltig**. I nästa steg måste du öppna posten för projektteammedlemmen och välja en underleverantör och underleverantörsrad. Då uppdateras uppgiftstilldelningen till att ha en referens till underleverantören och underleverantörsraden och statusen för teammedlemmen uppdateras till **Giltig**.

Om du väljer att skapa en generisk teammedlem från listrutan **Tilldelad resurs** i uppgiften, gör dialogrutan **Skapande av generisk teammedlem** att du kan välja en underleverantör och underleverantörsrad. När den generiska resursen tilldelas uppgiften och den motsvarande posten för projektteammedlem skapas ser du att posten för projektteammedlem skapas med arbetartypen inställd på **Kontraktarbetare** och **Giltighet** inställd på **Giltig**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Skapa projektteammedlemmar med hjälp av fliken Team
Med hjälp av fliken Team i projektet kan du skapa en generisk medlem eller en namngiven teammedlem. När du skapar teammedlemmen kan du välja underleverantör och underleverantörsrad. När teammedlemmen har skapats måste du tilldela teammedlemmen en uppgift med hjälp av listrutan **Tilldelade resurser** i uppgiften. 

## <a name="updating-estimates"></a>Uppdatera uppskattningar
När du har tilldelat projektteammedlemmar uppgifter ska du navigera till fliken **Uppskattningar** i projektet och välja **Uppdatera priser** för att säkerställa att kostnaderna för underleverantörstilldelningar är uppdaterade, baserat på inköpsprislistan som bifogas underleverantörskontraktet. Uppskattningar genereras inte för ej tilldelade uppgifter i Microsoft Dynamics 365 Project Operations. Därför måste du skapa uppgiftstilldelningar för att prissätta olika uppgifter i projektet. 

> [OBS!] Projektteammedlemmar som har **Arbetstyp** inställd på **Kontraktarbetare** men som inte har en underleverantörsreferens flaggas som **Ogiltiga** i rutnätet **Projektteammedlemmar**. Om det finns projektteammedlemmar med den här statusen öppnar du posten för projektteammedlemmen och uppdaterar fälten för underleverantör och underleverantörsrad manuellt så att kostnadsberäkningen återspeglar underleverantörers kostnad på fliken **Uppskattningar**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
