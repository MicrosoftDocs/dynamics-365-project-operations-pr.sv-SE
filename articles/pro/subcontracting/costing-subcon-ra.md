---
title: Kostnadsuppskattning av underleverantörers resurstilldelningar
description: Det här ämnet innehåller information om hur Microsoft Dynamics 365 Project Operations beräknar kostnadsuppskattningar av underleverantörers resurstilldelningar.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903537"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Kostnadsuppskattning av underleverantörers resurstilldelningar

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

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