---
title: Skapa en uppdelad arbetsstruktur
description: Detta ämne förklarar hur du skapar en uppdelad arbetsstruktur (WBS) inklusive enkel kontroll i det nya schemaläggningsgränssnittet.
author: ruhercul
ms.date: 01/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ac3facacd95e5e677635cb037d0d3458da612410
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005723"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Skapa en uppdelad arbetsstruktur (WBS)

Ett projektschema kommunicerar vad som behöver slutföras, vilka resurser som ska utföra arbetet samt den tidsram inom vilken arbetet behöver slutföras. Schemat återspeglar det arbete som är associerat med att leverera projektet i tid. I Dynamics 365 Project Operations skapar du ett projektschema genom att:

  - Dela upp arbetet i hanterbara uppgifter.
  - Beräkna den tid som krävs för att utföra varje uppgift.
  - Ange uppgiftsberoenden.
  - Ange varaktighet för uppgift.
  - Beräkna de generiska resurser som ska utföra uppgifterna. 

Projektschemat skapas på fliken **Schema** på sidan **Projekt**.

## <a name="tasks"></a>Aktiviteter

Det första steget när du skapar ett projekt är att bryta ned arbetet till hanterbara delar. Schemat i Project Operations stöder följande funktioner:

- Sammanfattning- eller behållaruppgifter.
- Lövnodsuppgifter.

### <a name="summary-tasks"></a>Sammanfattande uppgifter

Sammanfattningsuppgifter kan lagra andra sammanfattningsuppgifter eller lövnodsuppgifter. De har ingen egen arbetsinsats eller egen kostnad. I stället är deras arbetsinsats och kostnad en sammanslagning av arbetsinsatsen och kostnaden för behållaruppgifter. Sammanfattningsuppgifternas startdatum är startdatum för behållaruppgifter och slutdatum är slutdatum för behållaruppgifter. Namnet på en sammanfattningsuppgift kan redigeras, men det går inte att redigera egenskaper för schemaläggning (inklusive arbete, datum och varaktighet). Om du tar bort en sammanfattningsuppgift tas även alla dess behållaruppgifter bort.

### <a name="leaf-node-tasks"></a>Lövnodsuppgifter.

Lövnodsuppgift representerar det mest detaljerade arbetet i projektet. De har en uppskattad insats, resurser, planerade start- och slutdatum och en tid.

## <a name="create-a-task-hierarchy"></a>Skapa en uppgiftshierarki

### <a name="add-a-task"></a>Lägga till en uppgift

Följ stegen nedan för att lägga till en eller flera uppgifter.

1. Gå till **Projekt** och öppna den projektpost som du vill skapa ett schema för. 
2. Välj fliken **Uppgifter**. 
3. Välj **Lägg till ny uppgift**, ange ett namn för uppgiften och tryck sedan på Retur.
2. Ange ett annat uppgiftsnamn och tryck på Retur igen tills en fullständig lista med uppgifter visas.

### <a name="manage-hierarchy-of-a-task"></a>Hantera hierarkin för en uppgift

När en uppgift är indragen blir den underordnad den uppgift som är direkt ovanför. Uppgiftens schema-ID beräknas sedan om, så att den är baserad på det nya överordnade objektets schema-ID och att det följer dispositionsnumrering. Den överordnade uppgiften är nu en sammanfattningsuppgift. Därför blir det en sammanslagning av underordnade uppgifter. När en uppgift blir upphöjd är den inte längre underordnad den överordnade uppgiften. Schema-ID:t beräknas sedan om så att det visar uppgiftens uppdaterade djup och position i hierarkin. Arbetsinsatsen, kostnaden och datumen för den föregående överordnade uppgiften beräknas om, så att de inte inkluderar uppgiften.

Följ stegen nedan för att lägga till indrag eller höja upp en uppgift.

1. På sidan **Projekt**, på fliken **Uppgifter** samt under **Sammanfattningsuppgifter** väljer du de tre vertikala punkterna bredvid uppgiftens namn och sedan **Skapa underuppgift**. 
2. Markera uppgiften att dra in eller upphöja. Om du vill markera mer än en uppgift markerar du en uppgift, trycker samt håller nere Ctrl och väljer sedan ytterligare uppgifter.
2. Välj **Indrag** eller **Höj upp underuppgift** om du vill förflytta uppgifter in under eller ut underifrån sammanfattande uppgifter.

### <a name="move-tasks-up-and-down"></a>Flytta uppgifter upp och ned

Uppgifter kan flyttas till vilken nivå som helst i den uppdelade arbetsstrukturen på ett av två sätt:

- Markera ytterligare en uppgift och dra dem till önskad plats.
- Markera en eller flera uppgifter, högerklicka på och välj **Klipp ut**, välj målcell i schemat, och högerklicka och välj sedan **Klistra in**.

## <a name="task-attributes"></a>Uppgiftsattribut

En uppgifts namn beskriver det arbete som måste utföras. I Project Operations beskriver de attribut som associeras med en uppgift schemat för uppgiften och dess personalkrav.

## <a name="schedule-attributes"></a>Schemalägg attribut

Attributen **Insats**, **Startdatum**, **Slutdatum** och **Varaktighet** definierar schemat för uppgiften.

I följande tabell visas ytterligare schemaattribut.

| **Slutgiltigt visningsnamn** | **Slutgiltig beskrivning** |
| --- | --- |
| Arbetet slutfört (timmar) | Slutfört arbete för uppgiften i timmar. |
| Tid | Visar varaktigheten i dagar för uppgiften. |
| Total arbetsinsats | Total mängd arbete för uppgiften i timmar. |
| Slutför | Datum och tid för slutförande. |
| % slutfört | Uppgiftens slutförandegrad i procent. |
| Projektgrupp | Uppgiftstavlan kan grupperas efter bucket så att varje bucket har en egen kolumn. |
| Resterande insats (timmar) | Återstående arbete för uppgiften i timmar. |
| Början | Startdatum och starttid. |
| Namn | Uppgiftens namn. |
| ID | ID:t för uppgiften i den uppdelade arbetsstrukturen. |

Som en administratör kan du definiera anpassade fält för uppgiftsentiteten. Fälten kan dock inte visas i schemarutnätet. För att se dina anpassade fält, lägg till dem i informationssidan **Projektuppgift**.

## <a name="staffing-attributes"></a>Bemanningsattribut

Du når attribut för personal via fältet **resurser** i schemat. Du kan antingen söka efter en befintlig resurs eller välja **Skapa**. I fönstret **Snabbregistrering** lägger du sedan till en projektteammedlem som en ny resurs.

Fälten **roll**, **resursenhet** och **befattningsnamn** används för att beskriva personalkraven för uppgiften. Dessa personalattribut används tillsammans med uppgiftsschemat för att hitta tillgängliga resurser för att utföra den här uppgiften.

   - **Roll**: Ange vilken typ av resurs som krävs för att utföra uppgiften.
   - **Resursenhet**: Ange den enhet som uppgiftens resurser ska tilldelas från. Det här attributet påverkar kostnads- och försäljningsuppskattningen för aktiviteten om kostnaden och faktureringsräntan för resursen är inställda baserat på resursenheter.
   - **Befattningsnamn**: Ange ett eget namn för den allmänna resurs som fungerar som platshållare för den resurs som slutligen ska utföra arbetet.

Fältet **resurser** innehåller befattningsnamnet för den generiska resursen eller resursen när en hittas.

Fältet **kategori** innehåller värden som visar en bredare typ av arbete som uppgiften kan grupperas till. Det här fältet påverkar inte schemaläggning eller bemanning. Fältet används i stället endast för rapportering.

## <a name="task-dependencies"></a>Beroenden mellan uppgifter

Du kan använda schemat i Project Operations för att skapa föregående relationer mellan uppgifter. Fältet **Föregångare** använder ett eller flera värden för att ange vilka uppgifter en uppgift är beroende av. När du tilldelar en uppgift ett värde för en föregångare kan uppgiften starta först när alla föregångarens uppgifter har slutförts. På grund av beroendet återställs uppgiftens planerade startdatum till det datum då de föregående uppgifterna slutförs.

Uppgiftsläget påverkar inte uppdateringar som görs av start- och slutdatum för föregående och underordnade uppgifter.

## <a name="accessibility-and-keyboard-shortcuts"></a>Hjälpmedel och tangentbordsgenvägar

Rutnätet **Schema** är fullt åtkomligt och kan användas med skärmläsare som Berättare, JAWS eller NVDA. Du kan förflytta dig i rutnätsområdet med hjälp av piltangenterna (som i Microsoft Excel), men du kan använda tabbtangenten för att gå igenom de interaktiva användargränssnittselementen, och du kan använda nedåtpil, Retur eller blanksteg för att välja och öppna listrutemenyerna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]