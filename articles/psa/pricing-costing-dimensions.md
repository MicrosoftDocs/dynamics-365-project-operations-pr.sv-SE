---
title: Startsida för prissättnings- och kostnadsdimensioner
description: I det här ämnet finns en översikt över prissättningsdimensioner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085581"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Startsida för prissättnings- och kostnadsdimensioner

De dimensioner som används för att ange lönesättning och kostnader i projektbaserade organisationer påverkas av följande attribut:

- Personer som utför arbete på ungefär samma sätt som deras erfarenheter, roll eller geografi
- Arbete som utförs på samma sätt som komplexitet eller tid på dygnet

Med tanke på att de olika attrubuten av arbete och de personer som krävs för att utföra arbetet finns det två typer av prisdimensionsvärden tillgängliga i Project Service Automation: 

- **Alternativuppsättningar** : - Attribut som är fasta uppräkningar för en uppsättning värden.
- **Entitetbaserade värden** - attribut som kan ha en varierad uppsättning värden som är begränsade men kan ändras med tiden.

## <a name="pricing-dimensions"></a>Prissättningsdimensioner

PSA levererar en standarduppsättning med prisdimensioner. Du kan visa dessa genom att gå till **Project Service** > **parametrar**. I parameterposten, på fliken **Beloppsbaserad prissättningsdimension** ska du kontrollera att rollen **msdyn_resourcecategory** och resursorganisationsenheten **msdyn_organizationalunit** har fälten **Gäller för försäljning** och **Gäller för kostnad** inställd på **Ja**. På så sätt kan du ange pris och kostnad för varje kombination av roll och organisationsenheter.

![Skärmbild av parametrar för Project Service med "gäller för försäljning" markerad](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Om du har använt de här fälten som roll- och organisationsenhet som prissättningsdimensioner före version 3 av PSA-versionen kommer det inte att finnas någon observerbar förändring. Du kan fortsätta att använda Project Service som vanligt. 

Om du behöver pris eller kostnad för dina resurser med hjälp av ytterligare attribut kan du skapa anpassade fält, entiteter och dimensioner. Mer information finns i följande avsnitt: Tänk dock på att du måste genomföra procedurerna i nedanstående ordning:

- [Skapa anpassade fält och entiteter](create-custom-fields-entities.md)
- [Lägg till anpassade fält i prisinställning och transaktionella entiteter](field-references.md)
- [Konfigurera anpassade fält som prissättningsdimensioner](set-up-pricing-dimensions.md)
- [Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Prissättning av mänsklig resurs
Hur en organisation prissätter mänsklig resurs är ofta ett viktigt strategiskt övervägande som påverkar organisationens lönsamhet direkt. Arbeta med ekonomiteamen och övningsrubriker när organisationen är klar att identifiera hur fakturering och kostnader för personaltid ska konfigureras.

Andra faktorer för prissättningen är om återanvända fält eller entiteter som inte för närvarande är prissättningsdimensioner men som används som prissättningsdimensioner för organisationen. Fält som **transaktionskategori** ( **msdyn_transactioncategory** ) och **bokningsbar resurs** ( **bookableresource** ) är exempel på sökande dimensioner. 

Fundera över om prissättningsdimensionen ska vara en tabell eller en alternativuppsättning. Om du förväntar dig ändringar av värden i en dimension som blir större än 10 eller 12 och du behöver ytterligare attribut för dessa värden kan du skapa en entitet i stället för en alternativuppsättning. Om du underhåller en alternativuppsättning, t.ex. lägga till eller ta bort värden, krävs en administratör eller utvecklare för att kunna lägga till nya rader i en tabell kan utföras av de flesta företagsanvändare.

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
