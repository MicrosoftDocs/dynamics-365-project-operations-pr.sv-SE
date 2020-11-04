---
title: Lägg till anpassade fält som krävs i prisinställningar och transaktionella entiteter
description: I det här ämnet finns information om hur du lägger till obligatoriska anpassade fältreferenser till entiteter och formulär och vyer.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e589465eb98723b3b49c5d96e263eb3abf15eb2c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085580"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Lägg till anpassade fält som krävs i prisinställningar och transaktionella entiteter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Det här ämnet förutsätter att du har slutfört procedurerna i ämnet [Skapa anpassade fält och entiteter att användas som prissättningsdimensioner](create-custom-fields-entities-pricing-dimensions.md). Om du inte har slutfört de här procedurerna går du tillbaka och slutför dem och går sedan tillbaka till ämne. 

I det här ämnet visar procedurerna hur du lägger till de anpassade fältreferenser som krävs för entiteter och användargränssnittselementen, t.ex. formulär och vyer.

## <a name="add-custom-pricing-dimension-fields"></a>Lägg till anpassade prisdimensionsfält 
När anpassade fält och entiteter har skapats är nästa steg att göra prisinställning och transaktionella entiteter medvetna om anpassade entiteter eller alternativuppsättningar genom att skapa referensfält. Beroende på om listan över prissättningsdimensioner innehåller alternativuppsättningsdimensioner eller entitetsdimensioner eller båda, följer du endast stegen i **Alternativuppsättningsbaserade anpassade prissättningsdimensioner** eller **Entitetbaserade prissättningsdimensioner** eller båda.

### <a name="option-set-based-custom-pricing-dimensions"></a>Alternativuppsättningsbaserade anpassade prissättningsdimensioner
När en dimension för anpassad prissättning är alternativbaserad lägger du till den som ett fält för att viktiga entiteter. I följande procedur används **Resursens arbetsplats** och **Arbetstid för resurs** används som alternativuppsättningsbaserade prissättningsdimensioner. Dessa måste först läggas till som fält till prissättningsentiteter **Rollpris** och **Pålägg för rollpris**.

1. I Project Operations, väljer **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter > Rollpris**.
3. Utöka entiteten **Rollpris** och välj **Fält**.
4. Klicka på **Ny** om du vill skapa ett nytt fält med namnet **Resursens arbetsplats** och välj **Alternativuppsättning** och fälttyp. 
5. Välj **Använd en befintlig alternativuppsättning** , välj alternativuppsättningen **Resursens arbetsplats** och klicka på **Spara**.
6. Upprepa steg 1-5 om du vill lägga till det här fältet i entiteten **Pålägg för rollpris**. 
7. Upprepa steg 1-5 för alternativuppsättning **Arbetstid för resurs**.

> [!IMPORTANT]
> När du lägger till ett fält till fler än en entitet använder du samma fältnamn i alla entiteter. 

I försäljnings- och beräkningsfaserna för ett projekt används beräkningar av den arbetsinsats som krävs för att slutföra arbetet **Lokal** och **På plats** i **Vanliga timmar** och **Övertid** används för att beräknat värdet på offert/projekt. Fälten **Resursens arbetsplats** och **Arbetstid för resurs** läggs till i uppskattnings entiteterna **Information om offertrad** , **Information om kontraktrad** , **projektteammedlem** och **Beräkningsrad**.

1. I Project Operations, väljer **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter > Information om offertrad**.
3. Expandera entiteten för **Information om offertrad** och välj **fält**.
4. Klicka på **Ny** om du vill skapa ett nytt fält med namnet **Resursens arbetsplats** och väljer fälttypen **Alternativuppsättning**. 
5. Välj **Använd en befintlig alternativuppsättning** och **Resursens arbetsplats** och klicka på **Spara**.
6. Upprepa steg 1-5 för att lägga till det här fältet i entiteterna **Information om projektkontraktrad** , **Projektteammedlem** och **Beräkningsrad**.
7. Upprepa steg 1-6 för alternativuppsättning **Arbetstid för resurs**. 

För leverans och fakturering måste färdigt arbete prissättas korrekt för att välja om det har utförts **Lokalt** eller **På plats** och om det har slutförts på **vanliga timmar** eller **övertid** på projektets faktiska värden. Fälten **Resursens arbetsplats** och **Resursens arbetstider** bör läggas till entiteterna **Tidspost** , **Faktisk** , **Information om fakturarad** och **Journalrad**.

1. Välj **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter > Tidspost**.
3. Expandera entiteten för **Information om offertrad** och välj **fält**.
4. Klicka på **Ny** om du vill skapa ett nytt fält med namnet **Resursens arbetsplats** och välj **Alternativuppsättning** och fälttyp. 
5. Välj **Använd en befintlig alternativuppsättning** , välj alternativuppsättningen **Resursens arbetsplats** och klicka på **Spara**.
6. Upprepa steg 1-5 om du vill lägga till entiteterna **Faktisk** , **Information om fakturarad** och **Journalrad**.
7. Upprepa steg 1-6 för alternativuppsättning **Arbetstid för resurs**. 

Detta slutför de schemaändringar som krävs för alternativuppsättningsbaserade anpassade dimensioner.

## <a name="entity-based-custom-pricing-dimensions"></a>Entitetbaserade prissättningsdimensioner

När den anpassade prissättningsdimensionen är en entitet lägger du till 1:N-relationer mellan dimensionsentiteten och huvudsakliga entiteterna. Om du använder standardrubrikexemplet ovan är det rimligt att förvänta dig att varje anställd tilldelas en standardrubrik. Som ett resultat behöver du en 1 till N-relation från standardrubrik till bokningsbar resurs, eller en N till 1-relation om den har skapats från bokningsbar resurs till standardrubrik.

1. I Project Operations, väljer **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter > Standardrubrik**.
3. Expandera entiteten **Standardrubrik** och välj **1 till N-relationer**.
4. Klicka på **Ny** om du vill skapa en ny 1 till N-relation som kallas **standardrubrik till bokningsbar resurs**. Ange information som krävs och klicka sedan på **Spara**.

Standardrubriken måste också läggas till i prissättningsentiteter, **Rollpris** och **Pålägg för rollpris**. Detta slutförs också med hjälp av 1 till N-relationer mellan entiteterna **Standardrubrik** och **Rollpris** och **Standardrubrik** och **Pålägg för rollpris**.

1. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter > Standardrubrik**.
2. Expandera entiteten **Standardrubrik** och välj **1 till N-relationer**.
3. Klicka på **Ny** om du vill skapa en ny 1 till N-relation som kallas **standardrubrik till rollpris**. Ange information som krävs och klicka sedan på **Spara**.
4. Upprepa steg 1-4 för att skapa 1 till N-relationer mellan entiteterna **Standardrubrik** och **Pålägg för rollpris**.

I faserna försäljning och beräkning för projektet beräknas arbetsinsatsen för varje standardrubrik för priset för offerten/projektet. Detta innebär att 1 till N-relationer från Standardrubrik till var och en av dessa beräkningsentiteter behövs: 

- **Information om offertrad**
- **Information om projektkontraktrad**
- **Projektteammedlem**
- **Beräkningsrad**

5. Upprepa steg 1 - 5 för att skapa 1 till N-relationer från **Standardrubrik** till **Information om offertrad** , **Information om projektkontraktrad** , **Projektteammedlem** , och **Beräkningsrad**.

  I leverans- och faktureringsfaserna måste arbetet som slutförts av varje standardrubrik vara korrekt prissatt på projektets faktiska värden. Detta innebär att det måste vara 1 till N-relationer från entiteterna **Standardrubrik** till **Tidspost** , **Faktisk** , **Information om fakturarad** och **Journalrad**.

6. Upprepa steg 1 - 6 för att skapa 1 till N-relationer från entiteterna **Standardrubrik** till **Tidspost** , **Faktisk** , **Information om fakturarad** och **Journalrad**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Ange standardvärdet för dimensionsvärde med hjälp av mappningsfunktionerna i plattformen
När det gäller tid kan det vara bra att se till att systemet är standardrubriken på tidspost från den bokningsbara resursen som registrerar tidsposten. Gör på följande sätt om du vill lägga till fältmappningar i 1 till N-relationen från **Bokningsbara resurser** till **Tidspost**.

1. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter > Standardrubrik**.
2. Expandera entiteten **Standardrubrik** och välj **1 till N-relationer**.
3. Dubbelklicka på **Bokningsbar resurs till tidspost**. På sidan **relation** klickar du på **Använd fältmappningar**. 
4. Klicka på **Ny** om du vill skapa en ny fältmappning mellan fältet **Standardrubrik** på entiteten **Bokningsbar resurs** till referensfältet **Standardrubrik** på entiteten **Tidspost**. 

Detta slutför de schemaändringar som krävs för entitetbaserade anpassade dimensioner.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Lägga till anpassade fält i formulär, vyer och affärsregler.

När du har gjort alla nödvändiga schemaändringar är nästa steg att göra fälten synliga i användargränssnittet genom att lägga till fälten i formulär och vyer.

1. Öppna formuläret eller vyn. I det högra navigeringsfönstret markerar du fältet och drar det till formulärarbetsytan. 
2. Om du redigerar en vy använder du det högra navigeringsfönstret, klickar på **Lägg till fält** och i dialogrutan **fältlistor** väljer du fälten du behöver och klickar på **OK**.

Följande tabell ger en fullständig lista över de formulär och vyer som inte ingår i rutan efter entitet som behöver uppdateras med de nya fälten. Om det finns ytterligare vyer eller formulär i anpassningarna i dessa entiteter kan du lägga till de nya fälten i dem.

| Entity        | Formulär som behöver det nya fältet   |Vyer som behöver det nya fältet      |
| ------------------------------|---------------------------------|----------------------------------|
|  Pris för roll|• Information |• Aktiva resurskategoripriser<br> • Associerad vy för resurskategoripris|
|  Pålägg för rollpris|• Information|• Aktivt pålägg för rollpris<br>• Associerad vy för pålägg för rollpris|
|  Information om offertrad|• Projektinformation<br>• Snabbregistrera projekt|• Aktiv information om offertrad<br>• Kombinerad information om offertrad<br>• Associerad vy för information om offertrad|
|  Information om projektkontraktrad|• Projektinformation<br>• Snabbregistrera projekt|• Kombinerad kontraktradsinformation<br>• Aktiv kontraktradsinformation<br>• Associerad vy för kontraktradsinformation|
|  Projektteammedlem|• Information<br>• Nytt formulär|• Aktiva projektteammedlemmar<br>• Projektteammedlemmar<br>• Associerad vy för projektteammedlemmar|
|  Tidspost|• Information<br>• Skapa tidspost|• Mina tidsposter efter datum<br>• Mina tidsposter för den här veckan<br>• Tidsposter för godkännande.|
|  Journalrad|• Information<br>• Snabbregistrering|• Aktiva journalrader<br>• Associerad vy för journalrad|
|  Information om fakturarad|• Information<br>• Snabbregistrering|• Information om aktiv fakturarad<br>• Debiterbara fakturatransaktioner<br>• Kostnadsfria fakturatransaktioner<br>• Associerad vy för information om fakturarad<br>• Icke debiterbar fakturatransaktion|
|  Faktiskt|• Information<br>• Aktiva faktiska värden|• Associerad vy för faktiska värden|

Anpassade fält kan också behöva läggas till i affärsregler beroende på vad du har definierat. Ett färdigt exempel är för affärsregeln **Redigering baserat på status för tidspost**. Den här regeln definierar vilka fält som måste låsas när tidsposten är i en icke redigerbar status, t.ex **godkänd**. Lägg till fält i den här affärsregeln så att fälten blir låsta för redigering när tidsposten är i en annan status än **utkast** eller **returnerad**.
