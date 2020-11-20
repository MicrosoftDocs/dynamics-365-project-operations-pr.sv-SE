---
title: Konfigurera prislista för försäljning
description: I det här ämne finns information om prislista för försäljning för projektprissättning.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176273"
---
# <a name="set-up-a-sales-price-list"></a>Konfigurera prislista för försäljning

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

För projektofferter och kontrakt har en projektprislista ett annat pris för åsidosättningsmönster än en produktprislista. På en produktkatalogbaserad offertrad kan du åsidosätta priset till roller och kategorier direkt på offertraden, eftersom varje offertrad pekar till exakt ett katalogobjekt. På en projektrelaterad offertrad kan du emellertid inte åsidosätta priset för roller och kategorier direkt på offertraden. Du kan använda projektprislistan för att arbeta med de två distinkta åsidosättningarna.

> [!NOTE]
> Vi rekommenderar att du har en separat prislista för dina projektresurser och dina katalogobjekt, eftersom det finns skillnader mellan de två när du åsidosätter priserna.

Följande entiteter kan ha en eller flera associerade försäljningsprislistor för projektprissättning:

- Kund (konto) 
- Affärsmöjlighet 
- Offert 
- Projektkontrakt

Associationen mellan dessa entiteter och en prislista visas i projektprislistorna. Du kan associera en eller flera prislistor med entiteterna kund, affärsmöjlighet, offert och projektkontraktförsäljning.

En standardprislista för projekt anges inte automatiskt i en kundpost. Du kan emellertid bifoga en projektprislista manuellt till kundposten. Däremot bör du endast bifoga en projektprislista manuellt när du har ett anpassat prissättningsavtal med kunden. 

När en projektpris lista är kopplad till en försäljningsenhet verifieras följande information:

- Prislistan har kontexten **försäljning**. 
- Prislistans valuta matchar kundvalutan. 

I ett projektkontrakt använder följande prioriteringsordning för att automatiskt ange relaterade projektprislistor:

1. Offert
2. Affärsmöjlighet
3. Kund 
4. Globala inställningar 

När en projektprislista anges som standard verifierar systemet att valutan överensstämmer med kundens valuta och att standardprislistorna som har angetts har kontexten **försäljning**.

Du kan associera flera projektprislistor med entiteterna kund, affärsmöjlighet, offert och projektkontrakt. Den här funktionen har stöd för tidsspecifika standardpriser för ett långvarigt projektkontrakt, där du kan behöva mer än en prislista för att ta hänsyn till prisuppdateringar som sker på grund av inflation. Om de prislistor som du associerar med en entitet för kund, affärsmöjlighet, offert eller projektkontrakt har överlappande giltighetsdatum kan standardpriset vara fel. Därför bör du kontrollera att projektprislistor som har överlappande giltighetsdatum inte är associerade med dessa entiteter.
