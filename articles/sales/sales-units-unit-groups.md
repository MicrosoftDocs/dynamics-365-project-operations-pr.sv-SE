---
title: Enheter och enhetsgrupper
description: Det här avsnittet innehåller information om hur du skapar enheter och enhetsgrupper i Dynamics 365 Project Operations.
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277360"
---
# <a name="units-and-unit-groups"></a>Enheter och enhetsgrupper

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Enheterna är de kvantiteter eller de mått du säljer dina produkter eller tjänster i. Om du till exempel säljer trädgårdsredskap kan du sälja dem i enheter som paket, lådor och lastpallar En enhetsgrupp är en samling av dessa olika enheter.

Följ stegen i det här ämnet genom att kontrollera att du har tilldelats rollen systemadministratör eller Sales Professional-ansvarig eller har motsvarande behörighet.

## <a name="create-a-unit-group"></a>Skapa en enhetsgrupp

1. I webbplatsöversikten, markera **Enheter**.
2. Välj **Ny** och dialogrutan **Skapa enhetsgrupp** ange enhetsruta.
3. I fältet **Primär enhet** anger du den lägsta måttenheten som produkten kommer att säljas i. Du kan till exempel ange "stycke" eller "ounce".
4. Välj **OK**.

## <a name="add-units-to-a-unit-group"></a>Lägg till enheter till en enhetsgrupp.

1. Öppna en enhetsgrupp och på fliken **relaterad** väljer du **Enheter**. Du ser att den primära enheten redan lagts till.
2. Välj **Lägg till ny enhet** och på sidan **Snabbregistrering: enhet** i fältet **Namn** anger du namnet för enheten.
3. I fältet **kvantitet** ange den kvantitet som enheten ska innehålla. Om en låda till exempel innehåller 2 stycken skriver du "2". 
4. I fältet **Basenhet** väljer du en basenhet för att fastställa den lägsta mått enheten för enheten. Du kan till exempel välja "stycke".
5. Välj **Spara**:


[!INCLUDE[footer-include](../includes/footer-banner.md)]