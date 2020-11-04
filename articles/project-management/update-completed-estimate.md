---
title: Uppdatera beräkning vid färdigställande
description: I det här ämnet finns information om hur du uppdaterar projektionen av arbetsinsatsen i ett projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085723"
---
# <a name="update-estimate-at-completion"></a>Uppdatera beräkning vid färdigställande

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Det är vanligt att projektledaren ändrar de ursprungliga uppskattningarna för en aktivitet. Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status. Vi rekommenderar dock inte att projektledare ändrar baslinjenumren, eftersom projektbaslinjen representerar den etablerade sanningen för projektets schema och kostnadsberäkning, och alla projektintressenter har gått med på det.

Det finns två sätt som en projektledare kan använda för att förnya arbetet för uppgifter:

- Åsidosätt standardtid som krävs för att slutföra (ETC) en ny uppskattning av den faktiska resterande insatsen för aktiviteten. 
- Åsidosätt standardförlopp i procent med en ny uppskattning av det faktiska förloppen för aktiviteten.

Var och en av dessa är en omberäkning av aktivitetens ETC, uppskattning för att slutföra (EAC) och förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, ETC och förloppsprocent för sammanfattningsaktiviteterna beräknas om, och produktionen skapas som en ny projektion av insatsavvikelsen.
