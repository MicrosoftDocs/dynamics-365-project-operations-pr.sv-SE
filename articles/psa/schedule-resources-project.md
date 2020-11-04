---
title: Schemalägg resurser för ett projekt.
description: Schemalägga resurser för ett projekt i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085746"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Schemalägg resurser för ett projekt (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan kontrollera resurstillgänglighet för att få en övergripande bild av hur bokade resurser är, eller du kan filtrera vyn efter färdigheter, team, plats och andra alternativ.  
  
Schematavlan visar en lista över resurser och deras tillgänglighet. Välj ett visningsläge för att visa tillgänglighet efter **Timmar** , **Dag** , **Vecka** eller **Månad**.  
  
Det är viktigt att ställa in schematavlan innan du använder den. Mer information finns i [Konfigurera schemaläggningstavlan (Field Service eller Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Om du använder en äldre version och vill se resurstillgängligheten, se då [Visa resurstillgänglighet](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Om du vill använda funktionen för schemaläggningstavla, geocoding och platstjänster, måste du aktivera kartor.  
> 
> 1. I huvudmenyn väljer du **Schemaläggning av resurs** > **Administration**.  
> 2. Klicka på **Schemaläggningsparametrar**.  
> 3. Öppna post och bläddra ned till avsnittet **Resource Scheduling Optimization**.  
> 4. I fältet **Anslut till kartor** väljer du **Ja**.  
> 5. Godkänn villkoren och spara posten.  
> 6. I huvudmenyn väljer du **Project Service** > **Schemaläggningstavla**. Härifrån finns det flera sätt att schemalägga ett bokningskrav. Välj den metod som fungerar för dig.
  
## <a name="find-available-resources"></a>Hitta tillgängliga resurser

1.  I listan **Bokningskrav** högerklickar du på en oplanerad bokning och välj något av följande:  
  
- Välj **Sök tillgänglighet - Aktuella resurser** för att hitta tillgängliga resurser i listan över resurser på schemaläggningstavlan.  
- Välj **Sök tillgänglighet - Aktuella resurser** för att hitta tillgängliga resurser bland resurserna i systemet  
   > [!NOTE]
   >  När du gör detta visar filtren alternativ för det valda bokningskravet.  
  
2. När du ser en tillgänglig lucka högerklickar du på tidsluckan på schemaläggningstavlan och väljer **Boka här**. Eller också kan du dra och släpp bokningskravet till den tillgängliga tidsluckan.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Boka en resurs med hjälp av den dagliga vyn och se vem som är underbokad
  
1.  På schematavlan väljer du **Visa läge** och sedan **Dagar**.  
  
    Här visas en rutnätsvy över hur många timmar en resurs är bokad per dag och vilka dagar de är gratis.  
  
2.  Klicka på namnet på den resurs som du vill boka, och markera sedan **Boka**.  
  
3.  I dialogrutan **Resursbokning (skapa)** väljer du det projekt som du vill boka resursen för, tillsammans med bokningsmetod och start- och sluttider.  
  
4.  När du är klar väljer du **Boka**.  
  
## <a name="view-to-the-schedule-board"></a>Visa i schemaläggningstavlan
  
1.  Välj en ej schemalagd bokningskrav från listan längst ned.  
  
2.  Dra bokningskravet till en tillgänglig resurs/tidslucka på schemaläggningstavlan.  
  
3.  När du är klar väljer du **Boka**.  
  
### <a name="additional-resources"></a>Ytterligare resurser  
 [Guide för resurshanteraren](../psa/resource-manager-guide.md)
