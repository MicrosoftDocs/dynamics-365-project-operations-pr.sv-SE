---
title: Hur anpassar jag affärsprocessflödet för projektstadier?
description: En översikt om hur jag anpassar affärsprocessflödet för projektstadier.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993168"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Hur anpassar jag affärsprocessflödet för projektstadier?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Det finns en känd begränsning i tidigare versioner av Project Service-programmet, nämligen att namnen på stadier i affärsprocessflödet för projektstadier måste matcha förväntade engelska namn exakt (**Quote**, **Plan**, **Close**). I annat fall fungerar affärslogiken, som är beroende av de engelska stadiernas namn, inte som förväntat. Därför visas inga välbekanta åtgärder som till exempel **Växla process** eller **Redigera process** som finns i projektformuläret, och du uppmuntras inte till att anpassa affärsprocessflödet. 

Den här begränsningen har åtgärdats i version 2.4.5.48 eller senare. Denna artikel innehåller rekommenderade lösningar om du vill anpassa det förvalda affärsprocessflödet för tidigare versioner.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Affärslogik kräver en exakt matchning med engelska stadienamn

Affärsprocessflödet för projektstadier innehåller affärslogik som ligger till grund för följande problem i programmet:
- När projektet är kopplat till en offert anger koden affärsprocessflödet som stadiet **Quote** (offert).
- När projektet är kopplat till ett kontrakt anger koden affärsprocessflödet till stadiet **Plan**.
- När affärsprocessflödet nått stadiet **Close** (stäng) kommer projektposten att inaktiveras. När projektet inaktiveras skrivskyddas projektformulär och uppdelad arbetsstruktur (WBS), namngivna resursbokningar frisläpps och alla kopplade prislistor inaktiveras.

Denna affärslogik vilar på de engelska namnen på projektstadierna. Detta beroende av de engelska stadienamnen är huvudorsaken till varför anpassning av projektstadiernas affärsprocessflöde inte uppmuntras, samt även varför du inte ser de vanliga åtgärderna för affärsprocessflöde som till exempel **Växla process** eller **Redigera process** i projektentiteten.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Vad händer om stadienamnen inte överensstämmer med de engelska namnen?

I Project Service-programversion 1.x på plattformen 8.2 gäller följande: När stadienamnen i affärsprocessflödet inte matchar de engelska stadienamnen exakt, kommer den affärslogik som anger rätt stadium för offerter eller kontrakt, eller som stänger projektet, att hoppas över. Inga felmeddelanden visas. Därför verkar det som att du kan anpassa affärsprocessflödet för projektstadier. Inga automatiska processer för offerter, kontrakt och projektstängning kommer emellertid att fungera.

I appen Project Service, version 2.4.4.30 eller tidigare på plattform 9.0 genomfördes en omfattande strukturell förändring i affärsprocessflödet som krävde en omskrivning av affärslogiken för affärsprocessflöde. Som ett resultat av detta får du ett felmeddelande om namnen i processtadiet inte matchar de förväntade engelska namnen. 

Om du vill anpassa affärsprocessflödet för projektstadier för projektentiteten kan du därför endast lägga till helt nya stadier i det förvalda affärsprocessflödet för projektentiteten, medan stadierna **Quote**, **Plan** och **Close** förblir som de är. Denna begränsning säkerställer att du inte får några felmeddelanden från den affärslogik som förväntar sig engelska stadienamn i affärsprocessflödet.

I en version 2.4.5.48 eller senare har den affärslogik som beskrivs i den här artikeln tagits bort från det förvalda affärsprocessflödet för projektentiteten. Om du uppgraderar till den versionen eller senare kan du anpassa eller ersätta det förvalda affärsprocessflödet med ett eget. 

## <a name="workarounds-for-earlier-versions"></a>Lösningar för tidigare versioner

Om uppgradering inte utgör ett alternativ kan du anpassa affärsprocessflödet för projektstadier för projektentiteten på ett av följande två sätt:

1. Lägg till fler stadier i standardkonfigurationen samtidigt som du behåller de engelska stadienamnen **Quote**, **Plan** och **Close**.


![Skärmbild på hur du lägger till stadier i standardkonfiguration](media/FAQ-Customize-BPF-1.png)
 
2. Skapa ett eget affärsprocessflöde och gör det till primärt affärsprocessflöde för projektentiteten projekt, vilket gör att du kan få alla stadienamn du vill. Om du emellertid vill använda samma standardprojektstadier (**Quote**, **Plan** och **Close**) måste du göra vissa anpassningar som baseras på dina anpassade stadienamn. Den mer komplexa logiken finns i nedstängningen av projektet, något som du fortfarande kan utlösa genom att helt enkelt inaktivera projektposten.

![BPF-anpassning](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Ytterligare överväganden programmet Project Service i version 2.4.4.30 eller tidigare på plattformen 9.0

I Project Service 2.4.4.30 eller tidigare på plattformen 9.0 kommer fältet **Stadienamn** på den projektentitet som används i listan **Projekt efter fas** samt projektlistvyer inte att uppdateras med ett anpassat affärsprocessflöde, detta eftersom det är kopplat till det förvalda affärsprocessflödet för projektstadier. Du kan åtgärda detta problem genom att vidta följande steg:

- Lägg till ett anpassat fält för att registrera det aktuella stadiet för affärsprocessflöde som uppdateras när användaren fortsätter genom det anpassade affärsprocessflödet.

- Ändra diagrammet **Projekt efter stadium** om du vill arbeta med ditt anpassade fält i stället för standardkonfigurationen.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Steg för att skapa ditt eget affärsprocessflöde för projektentiteten

För att skapa ditt eget affärsprocessflöde för projektentiteten, gör följande:

1. Gå till **Inställningar** > **Processcenter**. Kopiera inte affärsprocessflödet för projektstadier eftersom affärslogiken för Project Service då kopieras.

  ![Skapa process](media/FAQ-Customize-BPF-3.png)

2. Använd processdesignern för att skapa de stadienamn du vill. Om du vill ha samma funktioner som standardstadierna för **Quote**, **Plan** och **Stäng** måste du skapa detta utifrån stadienamnen på dina anpassade affärsprocessflöden.

   ![Skärmbild av den processdesigner som används för att anpassa BPF](media/FAQ-Customize-BPF-4.png) 

3. I processdesignern klickar du på **Processflöde för order** att göra det anpassade affärsprocessflödet till primärt affärsprocessflöde för projektentiteten genom att flytta den ovanför affärsprocessflödet för projektstadier och överst i listan.


   [Skärmbild på orderprocessflöde](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Följande åtgärder gäller programmet Project Service version 2.4.4.30 eller tidigare på 9.0-plattformen

4. Lägg till ett nytt anpassat fält till projektentiteten för att registrera anpassade stadier i ditt anpassade affärsprocessflöde. Du måste lägga till affärslogik (insticksprogram eller arbetsflöden) om du vill uppdatera fältet när stadiet i det anpassade affärsprocessflödet uppdateras.

   ![Skärmbild på anpassning av entitet för projekt](media/FAQ-Customize-BPF-6-720.png)

5. Ändra diagrammet **Projekt efter stadium** om du vill använda ditt nya anpassade fält för stadier.

   ![Skärmbild på användning av diagrammet Projekt efter stadium](media/FAQ-Customize-BPF-7-720.png)

6. Ändra alla vyer för projektentiteten för att ta med dina nya anpassade fält för stadier.

   ![Skärmbild på ändring av vyer i entiteten för projekt](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]