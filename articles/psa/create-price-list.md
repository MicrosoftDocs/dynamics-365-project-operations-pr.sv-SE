---
title: Skapa en prislista
description: Skapa en prislista i Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 18f6e7a7a96f374acc85ee1027c5252cbf7ab5f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149475"
---
# <a name="create-a-price-list-project-service"></a>Skapa en prislista (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

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
 [Konfigurera Project Service Automation](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]