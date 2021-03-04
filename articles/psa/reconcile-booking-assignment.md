---
title: Stäm av bokningar och tilldelningar
description: I det här ämnet finns information om faktiska värden.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147945"
---
# <a name="reconcile-bookings-and-assignments"></a>Stäm av bokningar och tilldelningar

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En projektteammedlems projektbokningar och projektuppgiftstilldelningar är löst kopplade. En resurs kan därför ha uppgiftstilldelningar som inte motsvarar bokningar och bokningar som inte överensstämmer med uppgiftstilldelningar. Vanligtvis justeras projektbokningar och tilldelningar så att resurserna har rätt kapacitet för att utföra sina aktivitetstilldelningar. Verkligheten är dock att bokningar kan ske utifrån tillgänglighet och att tidsinställningar kan ändras när projektet fortsätter genom livscykeln. Därför är det en lös koppling som medger flexibilitet.

På grund av den lösa kopplingen av projektbokningar och aktivitetstilldelningar ingår fliken **avstämning** i entiteten projekt. På den här fliken får projektledarna avstämma teammedlemmarnas bokningar och deras tilldelningar för sina projektteam.

För varje namngiven teammedlem visar fliken **avstämning** bokningar och tilldelningar ned till den enskilda uppgiftstilldelningen. Den visar antalet timmar i celler som kan representera perioder från månader ned till dagar.

I fältet **Tidsskala** kan du välja **Månad**, **Vecka** eller **Dag**. **Vecka** är markerat som standard. Du kan emellertid ändra standardvärdet genom att klicka på knappen **inställningar**. När fliken **avstämning** öppnas visas aktuellt datum, men du kan använda kalenderkontrollen för att flytta framåt eller bakåt i tiden. När ett projekt har ett startdatum som är i framtiden visas datumet då det öppnas på fliken. Kalenderkontrollen har även alternativ som du kan använda för att gå till projektets start- och slutdatum.

Du kan använda utöka-kontrollerna på varje resurs för att visa information om resursens bokningar. Du kan även expandera varje resurs tilldelningar till nivån för den enskilda uppgiften.

Längst ned på fliken **avstämning** visas en övergripande nettosumma för projektet och fliken innehåller även en kolumn för summa. För varje resurs har fliken en skillnad mellan en teammedlems bokningar på projektet och sammanslagningen av teammedlemmens aktivitetstilldelningar. Vi rekommenderar att skillnaden är 0 (noll). Det bör alltså inte finnas någon skillnad mellan resursens bokningar och aktivitetstilldelningar. Alla skillnader är markerade med färg och fyllning för att anropa två villkor:

- **Underskott för bokning** – Underskott för bokning uppstår om en resurs har fler tilldelningar än bokningar. Eftersom denna kapacitet inte har reserverats kan en projektledare korrigera problemet genom att utöka resursens bokningar så att underskottet täcks.
- **Överflödiga bokningar** – Överflödiga bokningar inträffar när en resurs har bokats i projektet men inte tilldelats aktiviteter. Det här villkoret kan vara acceptabelt om till exempel resursen har bokats före en aktivitetstilldelning. I andra fall kan det emellertid hända att resursen inte är planerad att tilldelas. I så fall bör projektledaren överväga att annullera resursbokningarna så att kapaciteten kan användas för ett annat projekt.

> [!NOTE]
> Förklaringen för dessa villkor kan vara dold så att du lämnar mer utrymme för rutnätet. I det här fallet kan du göra förklaringen synlig genom att välja knappen **inställningar**.

I vissa fall när fältet **Tidsskala** anges till en nivå som är högre än **Dag** kan skillnader beräknas som 0 (noll). Till exempel på nivån **Månad** kan nettoskillnaden för en resurs vara 0 (noll) för att ange att bokningar är lika med tilldelningar. Om du tittar på nivån **Vecka** kan du se att det finns tilldelningar på 0 (noll) timmar och bokningar på 40 timmar under den första veckan i månaden och tilldelningar på 40 timmar och bokningar på 0 (noll) timmar i den andra veckan i månaden. Även om de totala bokningarna och tilldelningarna för månaden är lika stora skiljer de sig från varandra i veckan.

När du visar högre tidsnivåer visar fliken **avstämning** en cellindikator som meddelar att det finns olikheter på lägre tidsnivåer. I följande exempel visas en cellindikator i cellen för månaden oktober 2018 för resursen med namnet Nadja Jansson. Därför kan du se att även om resursens bokningar och tilldelningar är lika när de slås samman på nivån **månad** inte stämmer överens med de lägre nivåerna.

![Inkompatibla bokningar och tilldelningar på månadsnivå](media/reconcile-assignments-01.JPG)

Dubbelklicka på en cell om du vill zooma in på nästa lägre nivå och visa skillnaden. Om du till exempel dubbelklickar på differensen 2018 för Nadja Jansson, öka detaljnivån du på nivån **vecko**. Du kan se att resursen har bokningar på 16 timmar, men inga tilldelningar under de två första veckorna i oktober och 16 timmars tilldelningar, men inga bokningar under den tredje veckan i oktober.

![Inkompatibla bokningar och tilldelningar på veckonivå](media/reconcile-assignments-02.JPG)

Du kan högerklicka på en cell om du vill zooma ut nästa högre nivå. Du kan också inaktivera cellindikatorn genom att välja knappen **inställningar**. 

Du kan också använda knapparna **föregående** och **nästa** ovanför rutnätet för att navigera genom alla skillnader i projektet. Om du vill använda de här knapparna måste du först välja en resurs. Välj **nästa** om du vill gå vidare till nästa skillnad mellan bokningar och tilldelningar för resursen. Välj **föregående** om du vill gå till föregående skillnad.

I situationer där du har aktivitetstilldelningar för en resurs men inga bokningar kan du välja bokningsbrist och sedan välja **utöka bokning**. Du kan sedan se den bokning som krävs för att den ska kunna användas för att adressera resursens underskott. Du kan även visa resursens bokningar i det aktuella projektet och i andra projekt. Välj **OK** om du vill skapa bokningen för resursen utan hänsyn till aktuell tillgänglighet. Projektledaren eller resursansvarig kan sedan använda schemaläggningstavlan för att hantera situationer där en resurs har blivit överbokad utanför sin kapacitet, eftersom dess bokningar har utökats.

## <a name="managing-with-time-zones"></a>Hantera med tidszoner
För att se till att resultatet blir korrekt och förutsägbart när du använder Utöka bokning måste du ha två viktiga förutsättningar som måste uppfyllas:  

- Användaren måste konfigurera tidszonen för sina enheter så att den motsvarar den tidszon som har angetts i datorns inställningar för personliga alternativ.
 
  ![Tidszonsinställningar i Windows 10](media/reconcile-assignments-03.png)

  ![Tidszonsinställningar i inställningar för personliga alternativ](media/reconcile-assignments-04.png)
 
- Bokningsbar resurs måste innehålla minst en minut som överlappar de profiler som används för att definiera det begärda filnamnstillägget. Följande exempel visar hur du granskar resurser med arbetstimmar som faller mellan 9:00 och 19:00. 

  ![Jämförelse av resursprofiler](media/reconcile-assignments-05.png)

Följande tabell visar:

- En projektkalendermall.
- Resurs A: den här resursen har samma kalender och finns i samma tidszon som i projektet. Starttiden för bokningarna blir 9:00.
- Resurser B: den här resursen finns i en annan tidszon än projektet och börjar därför på 7:00 i tidszon. Bokningarna kan emellertid börja klockan 9:00 eftersom det är den tidigaste starttiden för tilldelningens profil.
- Resurser C och D: resurserna finns också i olika tidszoner, de skiljer sig från varandra och projektet och deras bokningar startas inte tidigare än deras respektive tillgängliga starttider.

|Entitet  |Kalender  |
|-|-|
|Projektkalendermall   | ![projektkalender](media/reconcile-assignments-06.png) |
|Resurs A  | ![Resurs A kalendern](media/reconcile-assignments-06.png) |
|Resurs B  |  ![Resurs B kalendern](media/reconcile-assignments-07.png) |
|Resurs C  |  ![Resurs C kalendern](media/reconcile-assignments-08.png) |
|Resurs D  | ![Resurs D kalendern](media/reconcile-assignments-09.png)  |
 
När du navigerar till vyn avstämning visas resurstilldelningarna och tillhörande bokningsunderskott.
 ![Vyn avstämning före tillägg](media/reconcile-assignments-10.png)

När funktionerna för att utöka bokning har körts för varje resurs utökas bokningarna för varje resurs. Detta beror på att de olika resursernas arbetstimmar överlappar bristens konturer.
 ![Vyn avstämning efter bokningstillägget](media/reconcile-assignments-11.png) 

Men en närmare information om bokföringarna visar att det finns skillnader i bokföringens starttid. Bokningarna startar inte tidigare än starttiden för tilldelningens profil och inte tidigare än resursens tillgängliga starttid.
 ![Nya bokningar av de resurser som har schemaläggningstavlan](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]