---
title: Projektscheman
description: I det här ämnet finns information om hur du skapar ett schema.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b7b221c2b0c47ed02c59fb724cf65bc41697d82
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600626"
---
# <a name="project-schedules"></a>Projektscheman 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ett projektschema kommunicerar vad som behöver slutföras, vilka resurser som ska utföra arbetet och tidsramen inom vilken arbetet behöver slutföras. Det återspeglar det arbete som är associerat med att leverera projektet i tid. I Dynamics 365 Project Service Automation skapar du ett projektschema genom att bryta ned arbetet med hanterbara uppgifter, beräkna hur lång tid som krävs för att utföra varje uppgift, ange uppgiftssamband, ange varaktighet för uppgifter och beräkna de generiska resurser som ska utföra uppgifterna. Projektschemat skapas på fliken **schema** på projektsidan.
 
## <a name="tasks"></a>Uppgifter

Det första steget när du skapar ett projekt är att bryta ned arbetet till hanterbara delar. Schemat i PSA stöder följande funktioner:

- Rotnoden för projektet.
- Sammanfattning- eller behållaruppgifter.
- Lövnodsuppgifter.

### <a name="project-root-node"></a>Rotnoden för projektet.

Projektets rotnod är den översta sammanfattningsuppgiften för projektet. Alla andra projektuppgifter som skapas under den. Namnet på rotnoden anges alltid till projektnamnet. Insats, datum och varaktighet för rotnoden beskrivs baserat på värden i hierarkin under den. Du kan inte redigera egenskaperna för rotnoden. Du kan inte heller ta bort rotnoden.

### <a name="summary-or-container-tasks"></a>Sammanfattning- eller behållaruppgifter. 

Sammanfattningsuppgifter har underuppgifter eller behållaruppgifter under dem. De har ingen egen arbetsinsats eller egen kostnad. I stället är deras arbetsinsats och kostnad en sammanslagning av arbetsinsatsen och kostnaden för behållaruppgifter. Sammanfattningsuppgifternas startdatum är startdatum för behållaruppgifter och slutdatum är slutdatum för behållaruppgifter. Namnet på en sammanfattningsuppgifter kan redigeras, men det går inte att redigera egenskaper för schemaläggning (arbete, datum och varaktighet). Om du tar bort en sammanfattningsuppgift tas även alla dess behållaruppgifter bort.

### <a name="leaf-node-tasks"></a>Lövnodsuppgifter.

Lövnodsuppgift representerar det mest detaljerade arbetet i projektet. De har en uppskattad insats, resurser, planerade start- och slutdatum och en tid.
 
## <a name="creating-a-task-hierarchy"></a>Skapa en ny uppgiftshierarki

Du kan skapa en uppgiftshierarki med följande alternativ:

- Knappen **Lägg till uppgift**
- Knappen **Dra in uppgift**
- Knappen **Dra ut uppgift**
- Knapparna **Flytta upp** och **Flytta ned**
- Hjälpmedel och tangentbordsgenvägar

### <a name="add-task"></a>Lägg till uppgift

Med knappen **Lägg till uppgift** kan du skapa en ny uppgift i hierarkin. Om du inte väljer en plats infogas den uppgiften i slutet. 

Ett schema-ID tilldelas varje uppgift. Schema-ID representerar uppgiftens djup och position i hierarkin. Med hjälp av dispositionsnumrering. För uppgifter på den första nivån under projektrotnoden används ett numreringsschema på 1, 2, 3 och så vidare. För uppgifter under den första nivån används ett numreringsschema på 1.1, 1.2, 1.3 och så vidare.

### <a name="indent-task"></a>Dra in uppgift

När en uppgift är indragen blir den underordnad den uppgift som är direkt ovanför. Uppgiftens schema-ID beräknas sedan om, så att den är baserad på det nya överordnade objektets schema-ID och att det följer dispositionsnumrering. Den överordnade uppgiften är nu en sammanfattningsuppgift eller en behållaruppgift. Därför blir det en sammanslagning av underordnade uppgifter.

### <a name="outdent-task"></a>Dra ut uppgift. 

När en uppgift dras ut blir den inte längre underordnad den överordnade uppgiften. Schema-ID:t beräknas sedan om så att det visar uppgiftens uppdaterade djup och position i hierarkin. Arbetsinsatsen, kostnaden och datumen för den föregående överordnade uppgiften beräknas om, så att de inte inkluderar uppgiften.

### <a name="move-up-and-move-down"></a>Flytta upp och flytta ned. 

Knapparna **Flytta upp** och **Flytta ned** ändrar du en uppgifts position inom dess överordnade hierarki. Ändringar av den här typen påverkar inte uppgiftens arbete, kostnad, datum eller varaktighet. Endast uppgiftens schema-ID påverkas. Schema-ID:t beräknas sedan om så att det visar uppgiftens nya position överordnad lista i underordnade uppgifter.

### <a name="accessibility-and-keyboard-shortcuts"></a>Hjälpmedel och tangentbordsgenvägar

Rutnätet **Schema** är fullt åtkomligt och kan användas med skärmläsare som Berättare, JAWS eller NVDA. Du kan flytta i rutnäts området med hjälp av piltangenterna (som i Microsoft Excel), men du kan använda tabbtangenten för att gå igenom de interaktiva gränssnittselementen, och du kan använda nedpil, retur eller blanksteg för att välja och aktivera listrutemenyerna. Kolumnrubrikerna är också interaktiva. Du kan dölja och visa kolumner, använda tabb-tangenten och piltangenterna för att förflytta dig mellan kolumnrubrikerna och använda åtgärdsknapparna i verktygsfältet. Du kan också använda följande kortkommandon:

- **Uppdatera**: ALT+SHIFT+F5
- **Lägg till**: ALT + SHIFT + infoga
- **Ta bort**: ALT+SHIFT+Ta bort
- **Flytta upp/ned**: ALT+SHIFT+upp- eller nedpil
- **Dra in/dra ut**: ALT_SHIFT + vänster- eller högerpil
- **Visa/Dölj hierarkier**: ALT + SKIFT + plus/minus tangenter

## <a name="task-attributes"></a>Uppgiftsattribut

En uppgifts namn beskriver det arbete som måste utföras. I PSA beskriver de attribut som associeras med en uppgift schemat för uppgiften och dess krav på personalen.

> ![Uppgiftsattribut.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Schemalägg attribut

Attributen **Insats**, **Startdatum**, **Slutdatum** och **Varaktighet** definierar schemat för uppgiften.

Ytterligare schemaattribut är:

- **Insatstimmar**: Ange en uppskattning av de timmar som krävs för att slutföra uppgiften. 
- **Varaktighet**: Ange antalet arbetsdagar som krävs för att slutföra uppgiften.
- **Schema-ID**: detta automatiskt genererade ID används för att beställa uppgifter i hierarkin. Beroenden mellan uppgifterna hanterar den faktiska ordning som uppgifterna arbetas i.
 
### <a name="staffing-attributes"></a>Bemanningsattribut

Du når attribut för personal via fältet **resurser** i schemat. Du kan antingen söka efter en befintlig resurs eller klicka på **skapa** och i fönstret **snabbregistrering**, lägg till en projektteammedlem som en ny resurs.

Fälten **roll**, **resursenhet** och **befattningsnamn** används för att beskriva personalkraven för uppgiften. Dessa personalattribut och uppgiftsschema används för att hitta tillgängliga resurser för att utföra den här uppgiften.

**Role** - ange vilken typ av resurs som krävs för att utföra uppgiften.

**Resursenhet** - ange den enhet som resurs för uppgiften ska tilldelas. Det här attributet påverkar kostnads- och försäljningsuppskattningen för aktiviteten om kostnaden och faktureringsräntan för resursen är inställda baserat på resursenheter.

**Befattningsnamn** – ange ett eget namn för den allmänna resurs som fungerar som platshållare för resursen och som slutligen ska utföra arbetet.

Fältet **resurser** innehåller befattningsnamnet för den generiska resursen eller resursen när en hittas.

Fältet **kategori** innehåller värden som visar en bredare typ av arbete som uppgiften kan grupperas till. Det här fältet påverkar inte schemaläggning eller bemanning. Den används endast för rapportering.

### <a name="task-dependencies"></a>Beroenden mellan uppgifter 

Du kan använda schemat i PSA för att skapa föregående relationer mellan uppgifter. Fältet **Föregångare** under **aktiviteter** använder ett eller flera värden för att ange vilka uppgifter en uppgift är beroende av. När du tilldelar ett värde för en föregångare kan uppgiften starta först när alla föregående uppgifter har slutförts. På grund av beroendet återställs uppgiftens planerade startdatum till det datum då de föregående uppgifterna slutförs.

Uppgiftsläget påverkar inte uppdateringar som görs av start- och slutdatum för föregående och underordnade uppgifter.

## <a name="task-mode"></a>Uppgiftsläge 

Uppgiftsläget styr schemaläggningen av uppgifter på en lövnod. PSA stöder två uppgiftslägen för varje uppgift: automatiskt schemaläggning och manuell schemaläggning.

### <a name="auto-scheduling"></a>Automatisk schemaläggning 
 
När du anger uppgiftsläget till **Automatiskt schemalagt** använder schemaläggningsmotorn schemaläggningsreglerna på följande uppgiftsattribut för att fastställa schemat för en uppgift:

#### <a name="scheduling-rules"></a>Schemaläggningsregler.

Startdatumet för en lövnodsuppgift som saknar föregångare blir som standard projektets planeringsstartdatum. En lövnodsuppgifts tid beräknas alltid som antalet arbetsdagar mellan dess start- och slutdatum. När en uppgift schemaläggs automatiskt, följer schemaläggningsmotorn reglerna nedan:

- Start- och slutdatumen för en uppgift måste alltid vara arbetsdagar enligt projektets schemaläggningskalender 
- För alla uppgifter som har föregående uppgifter ställs startdatumet automatiskt in på föregångarnas senaste slutdatum.
- Insats beräknas med hjälp av följande formel: antal personer × varaktighet × timmar i en standardarbetsdag i projektkalendern.

### <a name="manual-scheduling"></a>Manuell schemaläggning

Om reglerna för automatisk schemaläggning inte uppfyller dina krav kan du ange uppgiftsläget för uppgiften till **manuellt schemalagt**. Denna inställning stoppar schemaläggningsmotorn från att beräkna värdena för andra schemaläggningsattribut. Oavsett uppgiftsläget påverkas alltid den beroende uppgiftens startdatum om du anger föregående uppgifter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
