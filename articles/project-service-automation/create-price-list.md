---
title: Skapa en prislista
description: Skapa en prislista i Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756305"
---
# <a name="create-a-price-list-project-service"></a>Skapa en prislista (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Prislistor innehåller en mall som dina kontoansvariga kan använda för att skapa offerter och projekt, och för fastställande av utgifterna för ett projekt. De ger en radartikellista över roller och utgifter och det pris som du tar betalt för varje. Du kan skapa flera prislistor så att du kan ha separata prisstrukturer för olika regioner som du säljer produkterna i eller för olika försäljningskanaler. Det är en god idé att skapa minst en prislista för varje valuta som du vill fakturera dina kunder i.  
  
Om du vill skapa ekonomiska uppskattningar för arbetet som ska levereras, kontrollera att varje projekt har en bakomliggande utgifts- och prislista. Skapa en standardkostnad och försäljningsprislista som gäller alla projekt skapade inom din organisation.  
  
Prislistor är beroende av roller och utgiftskategorier, så innan du skapar en prislista kontrollerar du att du redan har konfigurerat rollerna och utgiftskategorierna som du vill använda när du skapar prislistan.  
  
1.  Gå till **Project Service > Prislistor**.  
  
2.  Klicka på **Nytt**.  
  
3.  I **Kontext** väljer du om prislistan gäller **Kostnad**, **Köp** eller **Försäljning**.  
  
4.  Ange ett namn på prislistan i **Namn**.  
  
5.  I **Valuta** väljer du den valuta som du ska använda för fakturering eller utgiftsredovisning.  
  
6.  I **Tidsenhet** anger du tidsperioden som priset gäller, till exempel dag eller timme.  
  
7.  Fyll i **Startdatum**, **Slutdatum** och **Beskrivning** efter behov.  
  
8.  Klicka på **Spara** för att skapa posten så att du kan fortsätta redigera den.  
  
9. Om du vill lägga till ett pris för rollen i prislistan, klickar du på **+** under **Rollpriser**.  
  
10. I fönstret **Priser för roll** fyller du i uppgifterna och klickar sedan på **Spara**. Fortsätt att lägga till priser för roll efter behov. Klicka på **Spara** i skärmens nedre högra hörn när du är klar.  
  
11. Om du vill lägga till ett pris för utgiftskategori prislistan klickar du på **+** under **kategoripriser**.  
  
12. I fönstret **Pris för transaktionskategori** fyller du i uppgifterna och klickar sedan på **Spara**. Fortsätt att lägga till priser för kategori efter behov. Klicka på **Spara** i skärmens nedre högra hörn när du är klar.  
  
13. Om du vill lägga till prislisteposter till prislistan klickar du på **+** under **Prislisteposter**.  
  
14. I fönstret **Prislisteposter** fyller du i uppgifterna och klickar sedan på **Spara**. Fortsätt att lägga till prislisteposter efter behov. Klicka på **Spara** i skärmens nedre högra hörn när du är klar.  
  
15. Om du vill lägga till områdesrelationer i prislistan klickar du på **+** under **Områdesrelationer**.  
  
16. I fönstret **Ny anslutning** fyller du i uppgifterna och klickar sedan på **Spara**. Fortsätt lägga till områdesrelationer om det behövs. Klicka på **Spara** i skärmens nedre högra hörn när du är klar.  
  
### <a name="see-also"></a>Se även  
 [Konfigurera Project Service Automation](../project-service/configure.md)
