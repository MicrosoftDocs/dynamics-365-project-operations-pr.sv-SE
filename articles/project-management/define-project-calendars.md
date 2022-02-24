---
title: Definiera projektkalendrar
description: Ämnet innehåller information om hur du använder en kalendermall på ett projekt för att följa upp projektschemat.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981322"
---
# <a name="define-project-calendars"></a>Definiera projektkalendrar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

För att skapa och hantera ett projekt måste du använda en kalendermall för projektet. Kalendermallen definierar följande projektattribut:

- Arbetstider, inklusive start- och sluttid
- Arbetsdagar
- Kalenderundantag, som lediga dagar

Kalendermallen som används för ett projekt är en kopia av kalendermallen som har definierats i organisationens inställningar.

> [!NOTE]
> Om du ändrar kalendermallen överförs inte ändringarna till projektets arbetstider. För att ändra projektets arbetstider måste en ny mall användas.

Det finns två viktiga krav om du vill skapa en kalendermall för organisationen:

- Ange mallens önskade arbetstider med hjälp av en ny eller befintlig bokningsbar resurs.
- Skapa en ny kalendermall och associera mallen med den bokningsbara resursen.

**Definiera arbetstider i mallen**

1. Gå till **Resurser** \> **Resurser**.
2. Skapa en ny resurs att referera till i kalendermallen eller välj en befintlig resurs.
3. Välj resursens flik **Arbetstider** och följ instruktionerna i [Ange arbetstider för en resurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) för att konfigurera kalenderreglerna.

**Skapa en ny kalendermall**

1. Gå till **Inställningar** \> **Kalendermall**.
2. Välj **Ny** och ange namn, beskrivning och mallresurs.

> [!NOTE]
> När en resurs refereras till i en kalendermall associeras en kopia av resursens kalender med kalendermallen. Om du ändrar arbetstider i den kopierade mallen överförs inte ändringarna till kalendermallen.

Du kan nu associera arbetsmallen med en projektkalendermall.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

