---
title: Skapa projektmall
description: Skapa en projektmall i Project Service
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 127b6e43a15f19a42791e78b55865ab11ca50c7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599016"
---
# <a name="create-a-project-template-project-service"></a>Skapa en projektmall (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Med projektmallar sparar du tid om ditt företag regelbundet bjuder på liknande typer av projekt. Du får en standarduppsättning roller och uppskattade timmar för en typ av projekt. Kontoansvariga och projektledare kan skapa projekt baserade på en projektmall eller så kan de kan kopiera mallen och göra sin egen.  
  
## <a name="components-of-project-template"></a>Komponenter i en projektmall
 En projektmall består av tre komponenter:  
  
- **Uppdelad arbetsstruktur**: En uppdelad arbetsstruktur i en projektmall har samma uppsättning element som i projektet. Du kan skapa en uppgiftshierarki, koppla roller till en aktivitet, definiera attribut i scheman, ange beroenden och visa alla data i Gantt. Den uppdelade arbetsstrukturen projektmallar har också stöd för uppgiftslägen för varje uppgift. Det är ingen skillnad mellan en projektmall och ett projekt när ett arbetsschema skapas.  
  
- **Projektberäkningar**: Projektberäkningar i mallar fungerar på samma sätt som de gör i projekt, förutom att prislistorna som ska användas som standard för utgifts- och försäljningspriser alltid utgör standardkostnad och -försäljningsprislistor angivna i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-parametrarna. Övriga funktioner är desamma som i ett projekt.  
  
- **Projektteambildning**: När ett projektteam bildas för en projektmall går det inte att boka en namngiven resurs i en mall. Du kan använda **Generera projektteam** i den uppdelade arbetsstrukturen för att generera en uppsättning allmänna resurser. Du kan även ange de kunskaper som krävs och kompetenser för allmänna resurser. Du kan inte ersätta en allmän resurs med en bokningsbar resurs i projektmallar.  
  
## <a name="create-a-project-from-a-template"></a>Skapa ett projekt från en mall  
 Du kan skapa ett projekt från en mall på följande sätt:  
  
-   Du kan välja en projektmall i projektet för att snabbt skapa formulär när du skapar ett projekt i offerten.  
  
-   När du skapar ett projekt genom att klicka på **Nytt projekt** visas i formuläret innan du sparar posten. Härifrån kan du klicka på fältet **Välj en mall** om du vill välja från listan över fördefinierade projektmallar i organisationen.  
  
-   Klicka på **Skapa projekt från en mall** på sidan **Projektmall** om du vill skapa ett projekt från mallen.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiera komponenter av en mall till ett projekt  
 När du kopierar komponenter i en mall till ett projekt finns det några saker du bör känna till.  
  
 **Kopiera en uppdelad arbetsstruktur**: När du kopierar den uppdelade arbetsstrukturen från en projektmall, om projektet har en annan projektkalender än mallen, används arbetstimmarna från projektets kalender i schemat över aktiviteter. Detta ändrar schemat till den säkerhetskopierade projektkalendern. På samma sätt tar den första uppgiften i den uppdelade arbetsstrukturen projektets startdatum, så att resten av hierarkischemat för uppgiften uppdateras baserat på varaktighet och beroenden som anges i mallen för uppdelad arbetsstruktur.  
  
 **Kopiera projektberäkningar**: När du kopierar över projektets beräkningsrader uppdateras prislistorna baserat på projektets ägande enhet för självkostnadslistan och kunden för försäljningslistan. Enhetskostnaden och försäljningspriserna fastställs utifrån dessa prislistor på projekt som är kopplade till en försäljningsenhet.  
  
 **Kopiera ett projektteam**: När du kopierar ett projektteam från mallen till ett projekt kopieras de allmänna resurserna över tillsammans med de angivna färdigheterna och kompetenserna i mallen. Allmänna resurstilldelningar hanteras också i projektmallen.  
  
### <a name="see-also"></a>Se även  
 [Guiden för projektledare](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
