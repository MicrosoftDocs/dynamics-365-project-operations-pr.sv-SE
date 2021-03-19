---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 13, version 3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: dbdcb811bfeacf17e841d679f097c591c16cd4c0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281050"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation uppdateringsversion 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 13. Den här versionen har versionsnumret för V3.10.3.18 och är tillgängligt enligt följande schema:

- **Allmän tillgänglighet (självuppdatering):** 2019 november
- **Automatisk uppdatering:** December 2019


## <a name="update-release-13"></a>Uppdatering version 13 

### <a name="bug-fixes"></a>Felkorrigeringar

- Tid och utgift

     - Fast: Sökfunktionen på sidan **utgiftsgodkännande** fungerar inte när du söker efter utgiftssyften.

- Resurshantering

     - Fast: nummer i avstämningen har uppdaterats till att vara högerjusterad.
     - Fast: namngivna resurser kan inte tilldelas till aktiviteter via fliken **schema**.

- Projektledning

     - Fast: Null referensundantag vid tilldelning av teammedlem när **TransactionType** saknas i inställningsinformation för **enhet** och **DefaultGroup**.

- Sales

     - Fast: dubbla transaktionstypposter returnerar ett fel när rollprisposter skapas.
     - Fast: extra knappar för **Ny affärsmöjlighet**, **Offert**, **Orderrad** och **Lägg till produkt** visas i kommandon för affärstillfällen, offerter, orderprodukter och i underrutnätet projektbaserade rader.




[!INCLUDE[footer-include](../includes/footer-banner.md)]