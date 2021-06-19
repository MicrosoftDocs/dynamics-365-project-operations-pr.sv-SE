---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 14, version 3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 14 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006893"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation uppdateringsversion 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 14. Den här versionen har versionsnumret för V-3.10.4.21 och är tillgängligt enligt följande schema:

- **Allmän tillgänglighet (självuppdatering):** 2020 januari
- **Automatisk uppdatering:** 2020 februari

## <a name="update-release-14"></a>Uppdatering version 14

### <a name="enhancements"></a>Förbättringar

- Sales

     - Anpassade fältvärden från **Information om offertrad** kopieras till **Projektkontraktradens detaljer** när en offert uppdateras till **stängd som vunnen**.
     - Bekräftade projekt kan **stängas som förlorade**.

- Resurshantering

     - När du utökar bokningarna visas en dialogruta där du bekräftar bokningsresultat och skapar en länk för att underhålla bokningar.


### <a name="bug-fixes"></a>Felkorrigeringar

- Tid och utgift

     - Fast: bättre användarupplevelse när användaren inte har valt några poster som ska rättas till.

- Resurshantering

     - Fast: boka en resurs flera gånger flödar från namnet på den bokningsbara resursen.

- Sales

     - Fast: det totala försäljningspriset beräknas inte förrän användaren även försummar en självkostnad för utgiftsuppskattningar i ett projekt.
     - Fixat: Stängning av en offert som **vunnen** misslyckas om det associerade projektavtalet inte har statusen **Utkast**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]