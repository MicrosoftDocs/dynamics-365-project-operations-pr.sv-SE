---
title: Projektmallar
description: I det här ämnet finns information om hur du använder projektmallar för att snabbkonfigurera projekt.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998298"
---
# <a name="project-templates"></a>Projektmallar 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En projektmall är en fördefinierad ramverk som hjälper dig att snabbt och enkelt starta ett projekt. Du kan använda en fördefinierad mall för att skapa ett nytt projekt med en enkel klickning. Du måste liksom för projekt definiera förutsättningarna för projektmallar. Du måste definiera en projektkalender för varje projektmall och roller och prislistor måste vara fördefinierade i organisationen så att komponenterna i mallen har användbara data.

En projektmall består av tre komponenter: ett schema, projektuppskattningar och projektteammedlemmar.

## <a name="schedule"></a>Schemalägg

Ett schema i en projektmall har samma uppsättning element som ett schema i ett projekt. Du kan skapa en uppgiftshierarki, koppla roller till uppgifter, definiera attribut i scheman och ange beroenden. Ett schema i en projektmallen stöder även uppgiftslägen för varje uppgift. Därför stöder den schemaläggningsmotorn. Du måste associera en projektkalender med projektet. När du skapar ett arbetsschema är det ingen skillnad mellan en projektmall och ett projekt.

## <a name="project-estimates"></a>Projektberäkningar

Projektuppskattningar i projektmallen fungerar på samma sätt som projektuppskattningar i ett projekt. Kostnaden och försäljningspriset hämtas emellertid från standardkostnads- och försäljningsprislistorna som definieras i parametrarna.

## <a name="creating-a-project-from-a-template"></a>Skapa ett projekt från en mall
 
Det finns flera sätt att skapa ett projekt från en projektmall:

- När du skapar ett projekt från en offert kan du välja en projektmall i dialogrutan **Snabbregistrering: projekt**.

> ![Snabbregistrering: dialogrutan Projekt](media/project-11.png)

- När du skapar ett projekt genom att välja **Nytt projekt**, visas sidan **Projekt** innan posten sparas. I fältet **Välj en mall** väljer du en av de fördefinierade projektmallarna i organisationen.
- Använd **Skapa projekt från en mall** på sidan **Mallentitet**.

## <a name="copying-components-of-template-to-project"></a>Kopiera komponenter av en mall till ett projekt

När du kopierar komponenterna i en projektmall till ett projekt kan det hända att en del åsidosättningar inträffar, beroende på inställningarna i projektet.

### <a name="copying-the-schedule"></a>Kopiera schemat

När du kopierar schemat från en projektmall, om projektet har en annan projektkalender än mallen, används arbetstimmarna från projektets kalender i schemat över uppgiftsschemat. På så sätt justeras schemat till att matcha den säkerhetskopierade projektkalendern. På samma sätt tar den första uppgiften i schemat projektets startdatum och schemat för resten av hierarkin uppdateras baserat på varaktighet och beroenden som anges i mallen. 

### <a name="copying-project-estimates"></a>Kopiera projektberäkningar 

När du kopierar över beräkningsrader för projekt uppdateras prislistorna. För självkostnadslistan bygger uppdateringarna på projektets ägande enhet. För försäljningsprislistan bygger de på kunden. För projekt som är förknippade med en försäljningsentitet bestäms enhetskostnaden och försäljningspriserna baserat på dessa prislistor.

### <a name="copying-a-project-team"></a>Kopiera ett projektteam

När ett projektgrupp kopieras från en projektmall till ett projekt, kopieras de generiska resurserna tillsammans med de färdigheter och färdigheter som definieras i mallen. Allmänna resurstilldelningar hanteras också i projektmallen. Namngivna resurser stöds inte i projektmallar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]