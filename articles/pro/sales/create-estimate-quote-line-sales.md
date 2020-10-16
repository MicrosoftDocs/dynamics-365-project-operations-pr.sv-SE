---
title: Beräkna en projektbaserad offertrad
description: I det här ämnet finns information om hur du skapar en uppskattning på en projektbaserad offertrad.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966875"
---
# <a name="estimating-a-project-based-quote-line"></a>Beräkna en projektbaserad offertrad

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

En projektbaserad offertrad innehåller information som hjälper dig att beräkna kostnaden och potentiella intäkter för det arbete som är ägnat på att leverera offertraden.

Om du vill uppskatta en projektrelaterad offertrad väljer du fliken **Offertradsinformation** på den projektbaserade offertraden. Det finns två sätt att skapa en uppskattning på en projektbaserad offertrad:

- Skapa uppskattningen manuellt direkt på offertraden med hjälp av offertradsinformationen 
- Skapa ett projekt och en projektplan och koppla sedan projektet och uppgifterna till offertraden. Processen för att importera uppskattningarna i projektplanen till offertraden utifrån den information du har angett kommer att aktiveras.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Skapa uppskattningar direkt på en projektbaserad offertrad

Om du vill skapa en uppskattning på en projektrelaterad offertrad väljer du fliken **Offertradsinformation**. Radartikeln som du skapar på den här fliken sammanfattar det offererade värdet för den här offertraden. 

Om du vill skapa offertradsinformation väljer du **+ Ny offertradsinformation** i underrutnätet **Offertradsinformation**. Ett skjutreglage för snabbskapande öppnas. Följande fält i formuläret **Offertrad**:

| **Fält** | **Plats** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Beskrivning | Snabbregistrering | En beskrivning av den specifika uppskattningen. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Transaktionsklass | Snabbregistrering | I den här listrutan visas de transaktionsklasser som finns under fliken **Allmänt** i den projektbaserade offertraden.  | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Roll | Snabbregistrering | Den person som ska utföra det här arbetet eller som ådrar sig utgiften. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Kategori | Snabbregistrering | Kategori för arbetet eller utgiften. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Startdatum | Snabbregistrering | Startdatum för arbetet. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Slutdatum | Snabbregistrering | Arbetets slutdatum. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Resursenhet | Snabbregistrering | Resursenhet som kommer att ådra sig kostnaden och tillhandahålla de resurser som arbetar på den. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. Fältet används också för att hämta självkostnad. |
| Enhetsschema | Snabbregistrering | Enhetsgrupp för arbetet eller utgiften. Enheter tillhör ett enhetsschema eller en grupp enheter. Till exempel är miles och kilometer enheter som tillhör en grupp enheter som beskriver avståndet. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Enhet | Snabbregistrering | Enhet för arbetet eller utgiften. | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Antal | Snabbregistrering | Kvantitet för arbetet eller utgiften | Det här fältet används som standard för den relaterade offertradsinformationen för kostnader som skapas automatiskt. |
| Enhetspris | Snabbregistrering | Fakturataxa för den roll som utför arbetet eller försäljningspriset för utgiftskategorin. Det här fältet används för Tid utifrån kombinationen av roll och resursenhet på projektprislistan som gäller för startdatumet. För utgifter används det här fältet för prisinställningar för transaktionskategorin i projektprislistan som gäller för startdatumet. Om prissättningsmodellen för transaktionskategorin inte är pris per enhet, finns det inget standardvärde och fältet lämnas tomt. | Kostnadstaxa för den roll som utför arbetet eller styckpriset för utgiftskategorin. Det här fältet används för Tid utifrån kombinationen av roll och resursenhet på priset för den avtalande enheten av den offererade prislistan som gäller för startdatumet. För utgifter används det här fältet för prisinställningar för transaktionskategorin i prislistan för självkostnad för den avtalande enheten som gäller för startdatumet. Om prissättningsmodellen för transaktionskategorin inte är pris per enhet, finns det inget standardvärde och fältet lämnas tomt. |
| Beräknad skatt | Snabbregistrering | Du kan ange den uppskattade momsen manuellt för det här arbetet eller den här utgiften. | Det här fältet har ingen inverkan nedströms. |
| Belopp | Snabbregistrering | Du kan ange information manuellt i det här fältet om fälten **Antal** och **Pris** lämnas tomma. Om de här fälten inte är tomma blir fältet skrivskyddat och beräknas som (Antal \* Styckpris) + moms. | Det här fältet har ingen inverkan nedströms. |

## <a name="update-prices-on-quote-line-details"></a>Uppdatera priser i offertradsinformation

Om du har ändrat priser i den projektprislista som är bifogad till offerten, eller i en prislista för självkostnad för den avtalande enheten, kan du välja **Omberäkna** på sidan **Offert** för att uppdatera priserna i den enskilda offertradsinformationen så att den avspeglar ändringen. Om du väljer **Omberäkna** visas ett varningsmeddelande som anger att priserna i offertradsinformationen för alla offertrader i denna offert kommer att återställas. Välj **Ja** om du vill uppdatera priserna i offertradsinformationen för både försäljning och kostnad.

## <a name="access-quote-line-details-for-cost"></a>Visa offertradsinformation för kostnad

Under fliken **Offertradsinformation** väljer du en rad i rutnätet om du vill aktivera vissa åtgärder i verktygsfältet i underrutnätet. Den första åtgärden i underrutnätets verktygsfält när offertradsinformation har valts är **Öppna kostnadsinformation**. Välj **Öppna kostnadsinformation** om du vill se den relaterade kostnadstaxan och beloppet för den här offertraden.

> [!NOTE]
> Om du ändrar resursenhet, antal, datum, roll eller kategori i offertradsinformationen för kostnad, ändras motsvarande värden i offertradsinformationen för försäljning.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta i offertradsinformation för kostnad och försäljning

Valuta i offertradsinformation för försäljning hämtas från projektprislistan som gäller för startdatumet för offertradsinformationen.

Valuta i offertradsinformation för kostnad hämtas från prislistan för den avtalande enheten av offerten som gäller för startdatumet för offertradsinformationen för kostnad.

Vid beräkningen av lönsamhet konverteras beloppet i offertradsinformationen för kostnad och försäljning till miljöns basvaluta för att rapportera den uppskattade övergripande marginalen för offerten.

Detta kan resultera i avrundningsfel i valutan och att marginalerna ändras på grund av brist på aktuella valutakurser. Använd endast de här beräkningarna i projektofferter som uppskattningar och inte verklig lagstadgad eller annan rapportering som kräver högre precision för avrundning och medvetenhet om aktuella valutakurser.
