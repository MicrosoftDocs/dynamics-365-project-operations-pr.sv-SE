---
title: Översikt över prissättningsdimensioner
description: I det här ämnet finns information om prissättningsdimensioner i Dynamics 365 Project Operations.
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128485"
---
# <a name="pricing-dimensions-overview"></a>Översikt över prissättningsdimensioner

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dimensionerna som används i personal för att ställa in priser och kostnader faller i två kategorier:

- Personer
- Planerat arbete

Därför finns det två typer av dimensionsvärden för prissättning tillgängliga:

- **Alternativuppsättningar**: dimensioner som är fasta uppräkningar för en uppsättning värden.
- **Entitetsbaserade värden**: dimensioner som kan vara en varierad uppsättning värden.

## <a name="pricing-dimensions"></a>Prissättningsdimensioner

Dynamics 365 Project Operations levereras med en standarduppsättning med prissättningsdimensioner. Du kan visa dessa prissättningsdimensioner genom att gå till **Project Operations** > **parametrar**. I parameterposten, på fliken **Beloppsbaserad prissättningsdimension** ska du kontrollera att rollen **msdyn_resourcecategory** och resursorganisationsenheten **msdyn_organizationalunit** har fälten **Gäller för försäljning** och **Gäller för kostnad** inställd på **Ja**. Med dessa fält aktiverade kan du ange pris och kostnad för varje kombination av roll och organisationsenheter.

Om du behöver pris eller kostnad för dina resurser med hjälp av ytterligare attribut kan du skapa anpassade fält, entiteter och dimensioner.

## <a name="pricing-human-resource-time"></a>Prissättning av mänsklig resurs
Hur en organisation prissätter mänsklig resurs är ofta ett viktigt strategiskt övervägande som påverkar organisationens lönsamhet direkt. Arbeta med ekonomiteamen och övningsrubriker när organisationen är klar att identifiera hur fakturering och kostnader för personaltid ska konfigureras.

Andra faktorer för prissättningen är om återanvända fält eller entiteter som inte för närvarande är prissättningsdimensioner men som används som prissättningsdimensioner för organisationen. Fält som **transaktionskategori** (**msdyn_transactioncategory**) och **bokningsbar resurs** (**bookableresource**) är exempel på sökande dimensioner. 

Fundera över om prissättningsdimensionen ska vara en tabell eller en alternativuppsättning. Om du förväntar dig ändringar av värden i en dimension som blir större än 10 eller 12 och du behöver ytterligare attribut för dessa värden kan du skapa en entitet i stället för en alternativuppsättning. Om du underhåller en alternativuppsättning, t.ex. lägga till eller ta bort värden, krävs en administratör eller utvecklare för att kunna lägga till nya rader i en tabell kan utföras av de flesta användare.

I följande exempel visas faktureringskostnader som är inställda utifrån den roll och den resursorganisationsenhet som resursen tillhör. Kostnadstariffer är vanligtvis baserade på den anställdes löneområde och den organisationsenhet de tillhör. I det här exemplet ser faktureringskursen och kostnadstabellerna ut på följande sätt:

**Exempel på faktureringskostnader**

| Roll        | Organisationsenhet    |Enhet      |Pris      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Utvecklare   | Contoso US  |Hour | 200|USD     |
| Utvecklare   | Contoso India |Hour|   112|USD     |


**Exempelkostnadstariffer**

| Löneband     | Organisationsenhet    |Enhet      |Pris      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mitt företag_Band1 | Contoso US  |Hour | 145|USD     |
| Mitt företag_Band2 | Contoso India |Hour|   67|USD     |
