---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 20, V3
description: Den här artikeln innehåller funktioner och korrigeringar som är tillgängliga i Project Service Automation uppdateringsutgåva 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913090"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation uppdateringsversion 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, V3, uppdateringsversion 20. Den här versionen har ett versionsnummer på V 3.10.31.37 och är allmänt tillgänglig via en självuppdatering i juni 2020.

## <a name="update-release-20"></a>Uppdatering version 20

### <a name="bug-fixes"></a>Felkorrigeringar

**Projektledning**

Följande problem har åtgärdats:

- Om du importerar projektmedlemmar med en allokeringsmetod som kräver timmar uppstår ett oklart felmeddelande när de angivna timmarna är noll.
- Användare får ett felmeddelande när det maximala tillåtna antalet tecken har angetts i fältet **Beskrivning** för en projektaktivitet.
- Sidan **Hämta tillägg för Microsoft Dynamics 365 Project Service Automation** omdirigeras till den engelska hämtningssidan när användarens språkinställningar är inställda på japanska.
- När ett serverfel inträffar blir synkroniseringsetiketten på fliken **schema** i formuläret **projekt** ibland kvar.
- Redundanta aktivitetsuppdateringar skickas till servern när en uppgift ändras.

**Sales**

Följande problem har åtgärdats:

- På formuläret **Kontrakt** dubbelklickar du på **Skapa faktura** för att skapa två fakturor för en post i en verklig post.
- I Internet Explorer 11 kan användare inte skapa utgiftsposter.
- Återföring av kostnad och återföring av faktiska fakturerade försäljningsvärden är inte kopplade.
- Knappen **Uppdatera faktiska värden** på formuläret **Projekt** uppdaterar inte **Uppgifternas faktiska tider**.
- Plugin-programmet **PreValidateProjectTeamMemberCreate** kan skapa dubbletter av allmänna bokningsbara resurser när attributet **msdyn_isgenericresourceprojectscoped** anges till **False**.
- **Beräkna om** rensar debiterbara kostnader för produktbaserad offertradinformation och kontraktradinformation.
- I vissa scenarier visar plugin-programmet **PostEstimateLineUpdate** ett undantagsfel med null-referens.
- Varaktighet av tidsfas på **Diagram över lönsamhetsanalys** stämmer inte överens med kostnaderna i offertradsinformationen om fast pris.
- Värdena för enhet och enhetsgrupp är inte korrekt standard för utgiftskategorier i formulären **kontraktradsinformation** och **offertradsinformation**.
- **Självkostnad för organisationsenhet** anger tillåtna överlappningar i giltighetsdatum.
- Användare har inte behörighet att ändra **OrgUnit** när ordertypen inte fungerar eftersom den leder till ett fel av typen null-referens.
- När du försöker navigera från formuläret **Information om offertrad** tillbaka till **Offert** uppdateras formuläret och fliken **Sammanfattning**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
