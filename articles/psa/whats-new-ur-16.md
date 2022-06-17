---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 16, version 3
description: Den här artikeln innehåller funktioner och korrigeringar som är tillgängliga i Project Service Automation uppdateringsutgåva 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926522"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation uppdateringsversion 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.  Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i [Installera och uppdatera en prioriterad lösning](/dynamics365/project-service/upgrade-psa-home-page).
I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för PSA, V3, uppdateringsversion 16. Den här versionen har versionsnummer V3.10.6.34 och är allmänt tillgänglig via en självuppdatering i januari 2020.


## <a name="update-release-16"></a>Uppdatering version 16

### <a name="bug-fixes"></a>Felkorrigeringar

-   Tid och utgift

    -   Åtgärdat: Användare som försöker skicka raderade tid- och utgiftsposter för godkännanden får nu relevanta felmeddelanden.

-   Projektledning

    -   Åtgärdat: De resursenheter som har definierats för teammedlemmar i mallar beaktas när mallarna tillämpas på ett nytt projekt.

    -   Åtgärdat: Förbättrad hantering av omtilldelning av postägarskap.

    -   Åtgärdat: Projekt som håller på att kopieras får inte kopieras förrän alla kopieringsåtgärder har slutförts.

-   Resurshantering

    -   Åtgärdat: Utökade bokningar hanterar nu korta varaktigheter korrekt och skapar inte längre noll timmar för utökade bokningar.

    -   Åtgärdat: Vyn Avstämningen visas nu när projektets tidszon är + 5:30 GMT och användarens tidszon är annorlunda.

-   Sales

    -   Åtgärdat: När ett projekt som har mappats till en kontraktrad tas bort och ett nytt projekt mappas, utvärderades inte de faktiska posterna i det nya projektet på nytt, detta grund val av de fakturerings- och prisregler som definierats på kontraktraden. Detta har åtgärdats i den här versionen. Priser och faktiska poster för det nymappade projektet kommer att återföras och återskapas på rätt sätt utifrån pris och faktureringsregler för kontraktraden. Som en följd utvärderas ochså de faktiska posterna för det icke-mappade projektet på nytt.

    -   Åtgärdat: Ytterligare validering har lagts till i fältet **Belopp** för en uppskattningsrad, detta för att se till att noll-värden inte sparas.

    -   Åtgärdat: När faktiska värden har uppdaterats i ett projekt har en uppdateringsknapp lagts till i projektets huvudformulär så att användarna kan synkronisera de faktiska värdena på nytt.

    -   åtgärdat: När användare uppgraderar från 2.X till 3. X tillåts projekt med ett NULL-värde för projektets namn.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
