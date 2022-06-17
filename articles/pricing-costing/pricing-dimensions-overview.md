---
title: Prissättningsdimensioner – Översikt
description: I den här artikeln finns information om prissättningsdimensioner i Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 294dcff8e9717aaa3a0459daf87cb7d608c96106
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918058"
---
# <a name="pricing-dimensions-overview"></a>Prissättningsdimensioner – Översikt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dimensionerna som används i personal för att ställa in priser och kostnader faller i två kategorier:

- Personer
- Planerat arbete

Därför finns det två typer av dimensionsvärden för prissättning tillgängliga:

- **Alternativuppsättningar**: dimensioner som är fasta uppräkningar för en uppsättning värden.
- **Entitetsbaserade värden**: dimensioner som kan vara en varierad uppsättning värden.

## <a name="pricing-dimensions"></a>Prissättningsdimensioner

Med Dynamics 365 Project Operations följer standarduppsättning med prissättningsdimensioner. Du kan visa dessa prissättningsdimensioner genom att gå till **Project Operations** > **parametrar**. I parameterposten, på fliken **Beloppsbaserad prissättningsdimension** ska du kontrollera att rollen **msdyn_resourcecategory** och resursorganisationsenheten **msdyn_organizationalunit** har fälten **Gäller för försäljning** och **Gäller för kostnad** inställd på **Ja**. Med dessa fält aktiverade kan du ange pris och kostnad för varje kombination av roll och organisationsenheter.

![Skärmbild av parametrar för Project Service med "gäller för försäljning" markerad.](media/PS-OOB-parameters.png)

Om du behöver pris eller kostnad för dina resurser med hjälp av ytterligare attribut kan du skapa anpassade fält, entiteter och dimensioner. Mer information finns i följande artiklar. 
  
  > [!NOTE]
  > Procedurerna måste slutföras i den ordning de listas.

1. [Skapa en lösning för anpassade prissättningsdimensioner](../sales/create-solution-custompd.md)
2. [Skapa anpassade fält och entiteter](create-custom-fields-entities-pricing-dimensions.md)
3. [Lägga till anpassade fält i prisinställningar och transaktionella entiteter](add-custom-fields-price-setup-transactional-entities.md)
4. [Konfigurera anpassade fält som prissättningsdimensioner](set-up-custom-fields-pricing-dimensions.md)
5. [Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Prissättning av mänsklig resurs
Hur en organisation prissätter mänsklig resurs är ofta ett viktigt strategiskt övervägande som påverkar organisationens lönsamhet direkt. Arbeta med ekonomiteamen och övningsrubriker när organisationen är klar att identifiera hur fakturering och kostnader för personaltid ska konfigureras.

Andra faktorer för prissättningen är om återanvända fält eller entiteter som inte för närvarande är prissättningsdimensioner men som används som prissättningsdimensioner för organisationen. Fält som **transaktionskategori** (**msdyn_transactioncategory**) och **bokningsbar resurs** (**bookableresource**) är exempel på sökande dimensioner. 

Fundera över om prissättningsdimensionen ska vara en tabell eller en alternativuppsättning. Om du förväntar dig ändringar av värden i en dimension som blir större än 10 eller 12 och du behöver ytterligare attribut för dessa värden kan du skapa en entitet i stället för en alternativuppsättning. Om du underhåller en alternativuppsättning, t.ex. lägga till eller ta bort värden, krävs en administratör eller utvecklare för att kunna lägga till nya rader i en tabell kan utföras av de flesta användare.

I följande exempel visas faktureringskostnader som är inställda utifrån den roll och den resursorganisationsenhet som resursen tillhör. Kostnadstariffer är vanligtvis baserade på den anställdes löneområde och den organisationsenhet de tillhör. I det här exemplet ser faktureringskursen och kostnadstabellerna ut på följande sätt:

**Exempel på faktureringskostnader**

| Roll        | Organisationsenhet    |Enhet      |Pris      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Utvecklare   | Contoso US  |Timme | 200|USD     |
| Utvecklare   | Contoso India |Timme|   112|USD     |


**Exempelkostnadstariffer**

| Löneband     | Organisationsenhet    |Enhet      |Pris      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mitt företag_Band1 | Contoso US  |Timme | 145|USD     |
| Mitt företag_Band2 | Contoso India |Timme|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]