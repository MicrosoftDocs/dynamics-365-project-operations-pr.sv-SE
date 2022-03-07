---
title: Nyheter eller ändringar i Project Service Automation version 3.x våg 1 2020
description: I det här ämnet finns information om vad som är nytt och ändrat i Project Service Automation version 3 våg 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a88b777c54ce54935d5483f616f3a24724ee192d40fbfd5d514f990e958dd5ea
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002128"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Nyheter eller ändringar i Project Service Automation version 3 våg 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

I ämnet framhävs viktiga uppgraderingsaspekter när de flyttar till den senaste versionen av Project Service Automation (PSA) version 3.x våg 1 2020.

## <a name="time-entry"></a>Tidspost
Tidsingångsupplevelsen har utökats för att ge möjlighet att förlänga tidregistreringen i fler kundscenarier. I det här ingår möjligheten att lägga till transaktionstyper, som nu specifikt styr funktioner som baseras på fältschemanamn **Inställningar för tidspost** som visas som **tidskälla**. En ny lösning som kallas tid, kostnad, status och godkännanden (TESA) har lagts till för att stödja den här funktionen.

### <a name="upgrade-consideration"></a>Att tänka på när du uppgraderar
För att du ska kunna använda den här funktionen har rollerna inom PSA-uppdateringen uppdaterats med nya privilegier. De här privilegierna ger läsbehörighet till den nya entiteten **tidsinmatningsinställningar**.

Användare som kräver möjlighet att logga tid bör ges användarrollen **tidspostanvändare** utöver befintliga roller. Den här rollen omfattar de nya funktionerna och ser till att tidsposten fortsätter att fungera.

Om du har några anpassade programmoduler som innehåller alla formulär för entiteten tidspost måste du ta bort **Snabbregistreringsformulär för TESA tidspost** från modulen.

### <a name="currently-extended-time-entry-changes"></a>För närvarande ändras utökad tidspost
Den här rolländringen är det enda grundläggande kravet som krävs för att fortsätta utnyttjandet av tidposten för att minimera påverkan för aktuella tidsposter. Om du har skapat anpassade vyer eller olika tidstransaktionsupplevelser måste du ange korrekt fält för **tidspostinställning** i korrekt PSA-värde.


[!INCLUDE[footer-include](../includes/footer-banner.md)]