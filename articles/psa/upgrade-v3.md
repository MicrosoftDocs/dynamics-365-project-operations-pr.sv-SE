---
title: Att tänka på när du uppgraderar - Microsoft Dynamics 365 Project Service Automation version 2.x eller 1.x till version 3
description: I det här ämnet finns information om hur du uppgraderar från Project Service Automation version 2.x eller 1.x till version 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c51726f71cfd0d4be98982d6a02268d64a70b91
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121735"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Att tänka på när du uppgraderar - PSA-version 2.x eller 1.x till version 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation och Field Service
Både Dynamics 365 Project Service Automation och Dynamics 365 Field Service använder URS-lösningen (Universal Resourcing Scheduling) för resursschemaläggning. Om du har både Project Service Automation och Field Service i din instans bör du planera för att uppgradera båda lösningarna till den senaste versionen (version 3.x för Project Service Automation, version 8.x för Field Service). Uppgradering av Project Service Automation eller Field Service kommer att installera den senaste versionen av URS, vilket innebär att inkonsekvent beteende är möjlig om både Project Service Automation och Field Service-lösningar i samma instans inte uppgraderas till den senaste versionen.

## <a name="resource-assignments"></a>Resurstilldelningar
I Project Service Automation version 2 och version 1, sparades uppgiftstilldelningar som underordnade uppgifter (kallas även raduppgifter) i **uppgiftsentiteten** och relaterade indirekt till entiteten **Resurstilldelning**. Raduppgiften visas i popup-fönstret för tilldelning i strukturen för Work Breakdown Structure (WBS).

![Raduppgifter i WBS i Project Service Automation version 2 och version 1](media/upgrade-line-task-01.png)

I version 3 av Project Service Automation har det underliggande schemat för tilldelning av bokningsbara resurser till aktiviteter ändrats. Raduppgiften är inaktuell och det finns en direkt 1:1-relation mellan uppgiften i **uppgiftsentiteten** och teammedlemmen i entiteten **resurstilldelning**. Uppgifter som tilldelas en projektmedlem lagras nu direkt i entiteten resurstilldelning.  

Ändringarna påverkar uppgraderingen av befintliga projekt med resurstilldelningar för namngivna bokningsbara resurser och generiska resurser i ett projektteam. I det här ämnet finns information om hur du kommer att behöva ta hänsyn till dina projekt när du uppgraderar till version 3. 

### <a name="tasks-assigned-to-named-resources"></a>Uppgifter tilldelade namngivna resurser
Med hjälp av den underliggande uppgiftsentiteten får uppgifter i version 2 och version 1 tillåtna teammedlemmar att framställa en roll som inte är definierad som standardroll. Till exempel kan Karla Larsson, som tilldelas som standardrollen som programhanterare, tilldelas en aktivitet med rollen utvecklare. I version 3 är rollen för en namngiven teammedlem alltid standard så därför använder uppgifter som är tilldelade Karla Larsson hennes standardroll i programhanteraren.

Om du har tilldelat en resurs till en uppgift utanför sin standardroll i version 2 och version 1, tilldelas den namngivna resursen standardrollen för alla aktivitetstilldelningar när du uppgraderar, oavsett rolltilldelning i version 2. Detta innebär skillnader i beräknade uppskattningar från version 2 eller version 1 till version 3 eftersom uppskattningar beräknas utifrån resursens roll och inte tilldelningen av radens tilldelning av uppgifter. Exempel: i version 2 har två uppgifter tilldelats Greta Andreasson. Rollen för raduppgift för uppgift 1 är utvecklare och för uppgift 2, programhanterare. Greta Andreasson har standardrollen programhanterare.

![Flera roller som har tilldelats en resurs](media/upgrade-multiple-roles-02.png)

Eftersom rollerna för utvecklare och programhanterare skiljer sig åt är kostnads- och försäljningsberäkningarna följande:

![Kostnadsuppskattningar för resursroller](media/upggrade-cost-estimates-03.png)

![Försäljningsuppskattningar för resursroller](media/upgrade-sales-estimates-04.png)

När du uppgraderar till version 3 ersätts raduppgifter med resurstilldelningar för uppgiften för den bokningsbara resursteammedlemmen. Tilldelningen kommer att använda standardrollen för den bokningsbara resursen. I följande bild är Greta Andreasson som har rollen programhanterare resursen.

![Resurstilldelningar](media/resource-assignment-v2-05.png)

Eftersom uppskattningarna bygger på standardrollen för resursen kan det hända att uppskattningar av försäljning och kostnad ändras. Observera att rollen **utvecklare** i följande bild inte längre visas eftersom rollen nu tas från den bokningsbara resursens standardroll.

![Kostnadsuppskattningar för standardroller](media/resource-assignment-cost-estimate-06.png)
![Försäljningsuppskattningar för standardroller](media/resource-assignment-sales-estimate-07.png)

När uppgraderingen är klar kan du redigera en teammedlems roll som någon annan än den tilldelade standarden. Om du ändrar en roll för en teammedlem ändras den emellertid i alla tilldelade uppgifter, eftersom teammedlemmar inte längre får tilldelas flera roller i version 3.

![Uppdatera en resursroll](media/resource-role-assignment-08.png)

Detta gäller även för raduppgifter som tilldelats till namngivna resurser när du ändrar resursens organisationsenhet från standardenheten till en annan organisationsenhet. När uppgraderingen av version 3 har slutförts använder tilldelningen resursens standardorganisationsenhet i stället för den som har angetts för raduppgiften.

### <a name="tasks-assigned-to-generic-resources"></a>Uppgifter tilldelade generiska resurser
I version 2 och version 1 kan du ange roll och organisationsenhet för en uppgift och sedan använda funktionen **generera team** för att generera generiska resurser utifrån de angivna attributen för uppgiften. I version 3 skapar du allmänna teammedlemmar med roll och organisationsenhet och tilldelar teammedlemmarna till aktiviteter.

I version 2 och version 1 kan projekt med allmänna resurser vara i två steg, eller en blandning av båda på uppgiftsnivån. Detta händer till exempel om du har följande scenarier:

- Uppgifter med roller och organisationsenhetsuppsättningar men ingen resurstilldelning har genererats.
- Uppgifter med de resurstilldelningar som tilldelats av en teammedlem, genom att skapa en generisk resurs med hjälp av funktionen **generera team**.

Innan du börjar uppgraderingen rekommenderar vi att du återskapar teamet för varje projekt som har tilldelats generiska resurser eller ännu inte har skapat en teamprocess.

För uppgifter som är tilldelade till generiska teammedlemmar och som genererats med **generera team** lämnar uppgraderingen den generiska resursen i teamet och lämnar tilldelningen till den generiska teammedlemmen. Vi rekommenderar att du skapar resurskravet för den generiska teammedlemmen efter uppgraderingen, men innan du bokför eller skickar en resursbegäran. Eventuella tilldelningar av organisationsenhet bevaras i de generiska teammedlemmar som skiljer sig från projektets avtalade organisationsenhet.

I projektets Z-projekt är till exempel den upphandlande organisationsenhet Contoso US. I projektplanen har testuppgifterna i implementeringsfasen tilldelats rollen teknisk konsult och den tilldelade organisationsenheten är Contoso India.

![Implementeringsfas för organisationstilldelning](media/org-unit-assignment-09.png)

Efter implementeringsfasen tilldelas integrationstestaktiviteten till rollen teknisk konsult, men organisationen anges till Contoso US.  

![Integrering av testaktivitet för organisationstilldelning](media/org-unit-generate-team-10.png)

När du skapar ett team för projektet skapas två generiska teammedlemmar på grund av de olika organisationsenheterna i uppgifterna. Teknisk konsult 1 tilldelas de Contoso India-uppgifterna och teknisk konsult 2 tilldelas Contoso US-uppgifterna.  

![Genererade generiska teammedlemmar](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> I Project Service Automation version 2 och version 1 innehåller teammedlemmen inte organisationsenheten som underhålls på raduppgiften.

![Version 2 och version 1 raduppgifter i Project Service Automation](media/line-tasks-12.png)

Du kan se organisationsenheten i vyn uppskattningar. 

![Organisationsenhetens uppskattningar](media/org-unit-estimates-view-13.png)
 
När uppgraderingen är klar läggs organisationsenheten för den raduppgift som motsvarar den generiska teammedlemmen till i den generiska teammedlemmen och raduppgiften tas bort. Innan du uppgraderar rekommenderar vi att du genererar eller återskapar teamet i varje projekt som innehåller generiska resurser.

För uppgifter som tilldelas en roll med en organisationsenhet som skiljer sig från organisationsenhet i det avtalade projektet och ett team inte har genererats, skapar uppgraderingen en generisk teammedlem för rollen, men kommer att använda den upphandlande enheten för projektmedlemmens organisationsenheter. Om du refererar tillbaka till exemplet med Project Z innebär det att den upphandlande organisationsenheten Contoso US och projektplanen har tilldelats rollen teknisk konsult med den organisationsenhet som tilldelats Contoso India. Integrering av testaktivitet som slutförs efter att implementeringsfasen har tilldelats rollen teknisk konsult. Organisationsenheten är Contoso US och ett team har inte skapats. Uppgradering skapar en generisk teammedlem, en teknisk konsult som har tilldelade timmar av alla tre aktiviteter och en organisationsenhet för Contoso US som är projektets upphandlande organisationsenhet.   
 
Om du ändrar standardvärdet för de olika organisationsenheterna för resurser på icke-genererade teammedlemmar rekommenderar vi att du genererar eller återskapar teamet i varje projekt som innehåller generiska resurser innan du uppgraderar, så att tilldelningen av organisationsenhet inte bortfaller.

