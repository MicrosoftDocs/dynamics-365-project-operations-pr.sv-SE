---
title: Uppgraderingshänsyn för uppdelad arbetsstruktur
description: I det här ämnet finns information om hur du uppgraderar uppdelad arbetsstruktur från Project Service Automation 2.x till 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 0b75fd372732f42a3557aaa5eccec1f24a644941
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121825"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Uppgraderingshänsyn för uppdelad arbetsstruktur
I det här ämnet finns information om hur du uppgraderar uppdelad arbetsstruktur från Project Service Automation 2.x till 3.x. I det här ämnet anges hälsotillståndet för ett projekt i Project Service Automation (PSA) som krävs för en lyckad uppgradering. Det finns också information om de vanligaste spärrningsförhållanden som gör att uppgraderingen misslyckas. Mer information om hur du definierar projektuppgifter och deras funktioner i ett projektschema finns i [projektscheman](project-creating.md).

## <a name="key-entities"></a>Nyckelentiteter
Följande entiteter krävs för att du ska kunna utföra en korrekt uppdelad arbetsstruktur som redan har laddats med resurser:

- [Projekt](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektuppgift](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Resurstilldelningar](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Beroende för projektuppgift](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Bokningsbara resurser](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Om du vill definiera en resursinläst uppdelad arbetsstruktur som ska användas måste du utföra följande steg:

1. Skapa ett nytt projekt. Mer information om hur du skapar ett nytt projekt finns i [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Skapa en eller flera uppgifter. Mer information om hur du skapar en ny uppgift finns i [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definiera uppgiftberoenden Mer information finns i [Beroende för projektuppgift](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Tilldela projektets teammedlemmar till projektet. Mer information finns i [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Tilldela projektets teammedlemmar till uppgifter. Mer information finns i [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Projektteamrelationer

För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:
- Alla projektmedlemmar i teamet måste associeras med en bokningsbar resurs.
- Alla projektmedlemmar i teamet måste associeras med samma projekt. 

## <a name="project-task-relationships"></a>Projektuppgiftsrelationer
För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:

- Alla relaterade uppgifter måste associeras med samma projekt.
- Varje raduppgift måste ha en överordnad uppgift.
- Varje uppgift måste ha ett överordnat projekt.

### <a name="valid-conditions"></a>Giltiga villkor

- Alla uppgiftsvaraktigheter måste vara större än eller lika med (>=) en timme och mindre än 1 800 000 minuter (1 250 dagar).*
- Alla uppgifter måste ha ett startdatum som inte är tidigare än 2000-01-01.*
- Alla uppgifter måste vara ett startdatum som inte är längre än 17 år från och med idag.*
- Alla uppgifter måste ha ett startdatum som är tidigare eller lika med deras slutdatum.
- Alla transaktionstyper för klassificeringar (utgift, material, skatt och tid) måste ha värden för **standardenhet** och **enhetsgrupp**.
- Datumformat med bokstäver bör undvikas.

### <a name="potential-mitigation-steps"></a>Potentiella åtgärdssteg
- Använd avancerad sökning för att identifiera projektaktiviteter som inte innehåller projekt-ID.
- Använd avancerad sökning för att identifiera projektaktiviteter där den schemalagda varaktigheten är större än > 1 800 000.
- Innan du gör några dataändringar bör du undersöka alla anpassningar som har associerats med den entitet som kan ha lett till ett dåligt tillstånd. De här anpassningarna ska åtgärdas innan du fortsätter med några databaserade uppdateringar.
- Om du har identifierat vilka uppgifter som har överbliven åtgärd kan du överväga att ta bort de här uppgifterna om de inte behövs eller om de ska associeras med rätt överordnat projekt.
- Om det är möjligt kan du lägga till flera uppgifter som representerar den totala varaktigheten för aktiviteter där varaktigheten är mer än 1 250 dagar.

> [!NOTE]
> Objekt som anges med en asterisk (\*) har gränser som beror på att CRM (Customer Relationship Management) bara stöder av 7 320 upprepade utvidgningar. Du måste stanna kvar under den här gränsen.

## <a name="resource-assignment-relationships"></a>Resurstilldelningsrelationer
För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:

- Alla resurstilldelningar i en uppdelad arbetsstruktur måste relateras till samma projekt.
- Alla resurstilldelningar i en uppdelad arbetsstruktur måste kopplas till projektteammedlemmar i samma projekt.

### <a name="potential-mitigation-steps"></a>Potentiella åtgärdssteg
- Identifiera alla uppgifter som faller utanför villkoren som beskrivs ovan.  
- Alla resurstilldelningar som inte längre är giltiga ska tas bort.

## <a name="project-task-dependency-relationships"></a>Projektuppgiftsberoende relationer
För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:

- Alla beroende av projektuppgifter måste vara relaterade till samma projekt.
- En uppgift får inte ha samma beroendereferens mer än en gång.
