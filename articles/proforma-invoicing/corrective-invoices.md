---
title: Det här avsnittet innehåller information om korrigerade fakturor.
description: I det här ämnet finns information om korrigerade fakturor.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898103"
---
# <a name="corrected-invoices"></a>Korrigerande fakturor

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Bekräftade fakturor kan redigeras. När du redigerar en bekräftad faktura skapas ett utkast av den korrigerade fakturan. Eftersom det är en förutsättning att du vill återföra alla transaktioner och kvantiteter från den ursprungliga fakturan, inkluderar den korrigerade fakturan alla transaktioner från den ursprungliga fakturan och alla kvantiteter på den är noll (0).

När transaktioner inte kräver korrigering kan du ta bort dem från utkastfakturan. Om du vill återföra eller returnera en delkvantitet kan du redigera fältet antal på raddetaljen. Om du öppnar fakturaradinformationen visas ursprungligt fakturaantal. Du kan sedan redigera aktuellt fakturerat antal så att det är mindre än eller lika med den ursprungliga fakturan.

När du bekräftar en rättningsfaktura återförs den ursprungliga fakturerade faktiska försäljningen och en ny fakturerad faktisk försäljning skapas. Om antalet minskas kommer differensen att skapa en ny fakturerad faktiskt försäljning. Om t.ex. den ursprungliga fakturerade försäljningen var åtta timmar och detaljerna för den korrigerade fakturaraden har en mindre mängd på sex timmar, återförs den ursprungliga faktureringsförsäljningsraden och två nya faktiska värden skapas:

- En fakturerad faktisk försäljning som faktiskt innehåller sex timmar.
- En ofakturerad faktisk försäljning för de återstående två timmarna. Denna transaktion kan antingen faktureras senare eller vara markerad som icke debiterbar, beroende på förhandlingarna med kunden.
