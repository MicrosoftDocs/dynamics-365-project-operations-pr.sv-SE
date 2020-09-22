---
title: Skapa en projektbokning från schemaläggningstavlan
description: I det här ämnet finns information om hur du skapar en projektbokning från schemaläggningstavlan.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756275"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Skapa en projektbokning från schemaläggningstavlan

Du kan boka en resurs för ett projekt direkt från fliken **Team** på projektet eller genom att skapa ett resurskrav från en tilldelning av en allmän teammedlem och sedan uppfylla det genererade kravet med en projektteammedlem.

Du kan också boka en resurs till ett projekt direkt från schemaläggningstavlan. Det finns tre sätt att göra det:

- **Boka från ett genererat resurskrav:** du kan skapa ett resurskrav efter att du har skapat en generisk resurs och tilldelning av uppgifter i ett projekt.

- **Boka från det primära kravet:** de primära kraven visas på schemaläggningstavlan på fliken **projekt**. 

- **Boka från ett nytt resurskrav:** du kan skapa ett resurskrav från grunden och associera det med ett projekt. Resurskravet visas i fliken **Öppna krav** på schemaläggningstavlan.

## <a name="book-from-a-generated-resource-requirement"></a>Boka från ett genererat resurskrav

Du kan skapa en generisk resurs och tilldela den en eller flera aktiviteter i ett projekt. Du kan sedan generera ett resurskrav från den generiske teammedlemmen. 

1.  På schemaläggningstavlan visas denna resurs i fliken **Öppna krav** fliken. Du kan behöva använda kolumnfilter i rutnätet om du har många öppna krav. 

    ![Öppna en kravflik på schemaläggningstavlan](media/FAQ-Project-Booking-Schedule-Board-1.png "Skärmbild på tabell för bokningar och tilldelningar")

2. Välj krav. Fliken **Sök tillgänglighet** visas högst upp på den valda raden.
 
3. När du sedan väljer fliken öppnas schemaläggningstavlans läge för schemaläggningshjälp, och tillgängliga resurser som uppfyller kraven för resursen filtreras. Därifrån kan du boka en resurs.

4. Du kan också dra och släppa den markerade raden från botten av schemaläggningstavlan till en resurscell i rutnätet ovan. När du släpper öppnas panelen **Skapa resursbokning** till höger.

    Om du väljer **Boka** bokas resursen till projektteamet.

![Skapa resursbokningspanel](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Boka från primärt krav

Om du skapar ett projekt i Project Service skapas automatiskt ett resurskrav kallat "primärt krav". Detta är ett tomt krav som används för att snabbt boka en resurs via schemaläggningstavlan utan att generera ett krav eller skapa ett helt nytt. Eftersom kravet är tomt måste du ange datum samt tilldelning och arbetstimmar (om tillämpligt). 

1. För att boka en resurs med det primära kravet markerar du fliken **Projekt** på schemaläggningstavlan. Du kan komma att behöva använda kolumnfiltret på kolumnen **Projekt** om du har många projekt.

   ![Kolumnfilter på schemaläggningstavlan](media/FAQ-Project-Booking-Schedule-Board-2.png "Skärmbild på tabell för bokningar och tilldelningar")

2. Välj det krav som bara har projektnamnet som namn och som har en varaktighet på noll (0).

3. Markera fliken **Sök tillgänglighet** som visas högst upp på raden. Detta placerar schemaläggningstavlan i läget för schemaläggningshjälpen och visar tillgängliga resurser som kan bokas för projektet.

4. Eftersom ett **primärt krav** är ett tomt krav med zero (0) i varaktighet måste du ange en varaktighet på panelen **Skapa Resursbokning** när du väljer och bokar en resurs.

5. Du kan också välja **primärt krav för projektet** längst ned i schemaläggningstavlan och dra och släppa det på en resurs för att schemalägga det.
 
    Eftersom ett **primärt krav** är ett tomt krav med zero (0) i varaktighet måste du ange en varaktighet på panelen **Skapa Resursbokning** när du väljer och bokar en resurs.
 
    När du bokar en resurs via **primärt krav** på schemaläggningstavlan lägger du till den i projektteamet utan några tilldelningar.
 
## <a name="book-from-a-new-resource-requirement"></a>Boka från ett nytt resurskrav
Följ stegen nedan om du vill boka från ett nytt resurskrav. 

1. Gå till **Resurskrav** och markera **Nytt** för att skapa ett nytt resurskrav.

2. Välj ett **projekt** på fliken projekt som du vill associera kravet med projektet.
 
    PÅ schemaläggningstavlan visas detta nya krav som **Öppet krav** som du kan uppfylla.

3. Boka resursen för att lägga till den i projektteamet.

4. Nu när resursen har bokats måste du tilldela uppgifter manuellt.

