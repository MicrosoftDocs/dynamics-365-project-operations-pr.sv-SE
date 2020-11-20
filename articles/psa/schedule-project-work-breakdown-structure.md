---
title: Schemalägg ett projekt med en uppdelad arbetsstruktur
description: Schemalägga ett projekt med uppdelad arbetsstruktur i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127900"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Schemalägg ett projekt med en uppdelad arbetsstruktur (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ett projektschema kommunicerar vad som behöver göras, vilka resurser som ska utföra arbetet och tidsramen inom vilken arbetet behöver slutföras. Projektschemat återspeglar det arbete som är associerat med att leverera projektet i tid. Ett av de första stegen i projektets inledande fas är att skapa ett projektschema. Om du vill upprätta ett projektschema måste du skapa en mall för uppdelad arbetsstruktur.  
  
 Skapa en projektstruktur med en uppdelad arbetsstruktur, som hjälper dig att:  
  
- Dela upp arbetet i hanterbara uppgifter  
  
- Uppskatta den tid som krävs för att slutföra en uppgift  
  
- Ange uppgiftssamband och uppgifters varaktighet  
  
- Fastställa roller som krävs för att slutföra varje uppgift  
  
  Projektschemat i den uppdelade arbetsstrukturen har ett välbekant utseende, komplett med ett interaktivt Gantt-schema.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Skapa en uppdelad arbetsstruktur för ett projekt  
 Skapa en uppdelad arbetsstruktur för att representera ordningen för uppgifter i ett projekt. Uppdelad arbetsstruktur innehåller uppgifter, krav för varje uppgift och information om intäkter och utgifter. I en uppdelad arbetsstruktur kan du lägga till:  
  
-   Sekvens av uppgifter i en hierarki  
  
-   Andra uppgifter, om det finns någon som måste slutföras innan du kan starta en uppgift  
  
-   Startdatum, slutdatum och varaktighet för en uppgift  
  
-   Antal timmar som krävs för en uppgift  
  
-   Alla nödvändiga färdigheter och utbildning för arbetare  
  
-   De arbetstagare som har tilldelats till en uppgift  
  
-   Beräknad intäkt och utgifter  
  
## <a name="task-types"></a>Uppgiftstyper  
Du ska använda följande typer av uppgifter när du skapar en mall för uppdelad arbetsstruktur:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Rotnoden för projektet**. | Översta sammanfattningsuppgiften för projektet. Alla andra projektuppgifter som skapas under den. Namnet på rotuppgiften är projektnamnet. Insats, datum och varaktighet för rotnoden baseras på värden i hierarkin under den. Du kan inte redigera egenskaper för rotnod eller ta bort rotnoden. | 
| **Sammanfattning- eller behållaruppgifter**. | En sammanfattningsuppgift är en uppgift som har underordnade uppgifter under den. En sammanfattningsuppgift har inte någon egen arbetsinsats eller utgift. Dess arbetsinsats och utgift är en sammanslagning av dess underuppgifter. Du kan ändra namnet på en sammanfattningsuppgift, men du kan inte ändra insats, datum eller tid, eftersom de beräknas automatiskt. Om du tar bort en sammanfattningsuppgift tas uppgiften och alla dess underordnade uppgifter bort.|  
| **Lövnodsuppgifter**. | En lövnodsuppgift representerar det mest detaljerade arbetet i projektet. Den har en uppskattad insats, ett planerat antal resurser, planerade start- och slutdatum och en tid.|

  
## <a name="task-hierarchy"></a>Uppgiftshierarki  
 När du skapar en uppgiftshierarki har du följande alternativ:  
  
- **Lägg till uppgift**.   Du kan lägga till en uppgift på en plats som du väljer i uppgiftshierarkin. Om du inte väljer en plats visas den nya uppgiften i slutet.  
  
- **Dra in uppgift**.   Dra in en uppgift så att den blir underordnad uppgiften direkt ovanför.  
  
- **Dra ut uppgift**.   Dra ut en uppgift så att den inte längre är en underuppgift till dess ursprungliga överordnade uppgift.  
  
- **Flytta upp och flytta ned**.   Flytta uppgifter upp och ned i hierarkin för den överordnade uppgiften. Om du flyttar en uppgift uppåt eller nedåt påverkar inte dess insats, utgift, datum eller tid.  
  
## <a name="task-attributes"></a>Uppgiftsattribut  
 En uppgifts namn beskriver det arbete som måste utföras. Olika uppgiftsattribut används för att beskriva schemat och bemanningsbehov för uppgiften.  
  
### <a name="schedule-attributes"></a>Schemalägg attribut

 - Tilldela värden till **Insatstimmar**, **Antal resurser**, **Startdatum**, **Slutdatum** och **Tid** för att fastställa schemat för uppgiften. 
 - **Insats** är en uppskattning av antalet timmar som det tar för att slutföra uppgiften.
 - **Antalet resurser** är en uppskattning som projektledaren placerar i uppgiften för att få bästa möjliga schema. 
 - **Tid** (i dagar) anger antalet dagar det tar att slutföra uppgiften.  
  
### <a name="staffing-attributes"></a>Bemanningsattribut

 - **Roll**, **Organisationsenhet för resurs**, **Antal resurser** och **Resurser** beskriver bemanningsbehovet för uppgiften. 
 - **Roll** beskriver typen av resurs som behövs för att utföra uppgiften. 
 - **Organisationsenhet för resursen** anger den organisationsenhet från vilken resurser ska bemannas för uppgiften. Detta påverkar också utgift- och försäljningsuppskattningen för uppgiften, eftersom det redovisas vid bestämning av enhetsförsäljningspriset för resursen. 
 - **Resurser** innehåller en allmän eller namngiven resurs när någon hittas.  
  
## <a name="task-dependencies"></a>Beroenden mellan uppgifter  
 Du kan skapa relationer till föregångare mellan en eller flera uppgifter i den uppdelad arbetsstrukturen. Du kan ange ett eller flera värden för föregångarfältet för uppgifter om du vill ange vilka uppgifter den är beroende av. När du tilldelar en uppgift ett föregångarvärde kan uppgiften starta först när alla föregående uppgifter har slutförts. Om du anger detta beroende för en uppgift leder det till omberäkning av det planerade startdatumet för uppgiften till det senaste slutet för alla dess föregående uppgifter. Föregångarrelaterad påverkan på ett schema är inte begränsad av uppgiftsläget som definieras för uppgiften.  
  
## <a name="task-mode"></a>Uppgiftsläge  
 Uppgiftsläget är en av de viktiga faktorer som fastställer schemaläggningen av lövnodsuppgifter. Det finns två uppgiftslägen för varje uppgift: automatiskt schemaläggningsläge och manuellt schemaläggningsläge.  
  
-   **Automatisk schemaläggning**.   När du anger uppgiftsläget till Automatiskt schemalagt använder schemaläggningsmotorn schemaläggningsreglerna på följande uppgiftsattribut för att fastställa schemat för en uppgift:  
  
    -   Föregångare  
  
    -   Insats  
  
    -   Antal resurser  
  
    -   Start- och slutdatum  
  
-   **Schemaläggningsregler**.   Startdatumet för en lövnodsuppgift som saknar föregångare blir som standard projektets planeringsstartdatum. En lövnodsuppgifts tid beräknas alltid som antalet arbetsdagar mellan dess start- och slutdatum. När en uppgift schemaläggs automatiskt, följer schemaläggningsmotorn reglerna nedan:  
  
    -   Start- och slutdatumen för en uppgift måste alltid vara arbetsdagar enligt projektets schemaläggningskalender  
  
    -   Startdatum för en uppgift med föregångare har som standard det senaste slutdatumet för föregående uppgifter  
  
    -   Insats = antal personer * tid * timmar i en standardarbetsdag i projektkalendern  
  
-   **Manuell schemaläggning**.   I vissa fall kanske du vill avvika från dessa regler. I dessa fall kan du ange uppgiftsläget för manuell tidsplanering för uppgiften. Detta stoppar schemaläggningsmotorn från att beräkna värdena för andra schemaläggningsattribut. Att ange föregående uppgifter påverkar alltid den beroende uppgiftens startdatum.  
  
## <a name="create-a-work-breakdown-structure"></a>Skapa en uppdelad arbetsstruktur  
  
1.  Gå till **Project Service > Projekt**.  
  
2.  Klicka på projektet du vill arbeta med.  
  
3.  Välj nedpilen bredvid projektnamnet i fältet överst på skärmen och klicka på Uppdelad arbetsstruktur.  
  
4.  Om du vill lägga till en uppgift klickar du på **Lägg till uppgift**. Fyll i fälten för uppgiften och klicka sedan på **Spara**.  
  
5.  Fortsätt lägga till uppgifter tills din uppdelade arbetsstruktur är klar. När du skapar en uppdelad arbetsstruktur, kan du göra följande för att organisera dina uppgifter:  
  
    -   Markera en uppgift och klicka på **Dra in** för att flytta den under en annan uppgift, eller klicka på Minska indrag för att flytta ut den en nivå.  
  
    -   Markera en uppgift och klicka på **Flytta upp** eller **Flytta ned** för att flytta den uppåt eller nedåt i listan.  
  
    -   Klicka på **Dölj Gantt-schema** för att dölja Gantt-schemat och klicka på **Visa Gantt-schema** för att visa det igen.  
  
    -   Välj en annan tidsperiod för Gantt-schemat i **Tidsskala**.  
  
6.  In du vill lägga till de roller som du har angett i den uppdelade arbetsstrukturen till projektets gruppmedlemmar klickar du på **Generera projektteam**.  
  
7.  Klicka på **Spara** i skärmens nedre högra hörn när du är klar med ändringarna.  
  
### <a name="see-also"></a>Se även  
 [Guide för projektansvarig](../psa/project-manager-guide.md)
