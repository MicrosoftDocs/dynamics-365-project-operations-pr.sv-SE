---
title: Nyheter i Project Service Automation uppdatering version 13, v3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756215"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3, uppdatering version 13
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
     - Fast: extra knappar för **ny affärsmöjlighet**, **offert**, **orderrad** och **lägg till produkt** visas i kommandon för affärsmöjligheter, offerter, orderprodukter och de projektbaserade raderna i underrutnätet.


