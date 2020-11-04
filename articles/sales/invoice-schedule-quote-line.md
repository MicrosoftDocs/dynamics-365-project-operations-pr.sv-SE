---
title: Faktureringsscheman på projektbaserade offertrader
description: I det här ämnet finns information om hur du skapar faktureringsscheman och milstolpar för offertrader.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3ead79371c5ebf5801123e47dc0d24e35ae51e58
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085473"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Faktureringsscheman på projektbaserade offertrader

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

En projektbaserad offertrad ger möjlighet att uttrycka ett faktureringsschema. Detta är valfritt under offertfasen eftersom programmet inte stöder fakturering av ett projekt när det är knutet till en offertrad. Fakturering tillåts endast efter att offerten har vunnits. Den enda inverkan nedströms från skapandet av ett faktureringsschema under offertfasen är att faktureringsschemat kopieras till den projektbaserade kontraktraden. Om du inte skapar ett faktureringsschema under offertfasen kan du göra det på den projektbaserade kontraktraden.

Syftet med faktureringsscheman är att det ska vara möjligt att skapa utkast av fakturor automatiskt för en projektrelaterad kontraktrad. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Skapa ett faktureringsschema för tid och material för en projektbaserad offertrad

När faktureringsmetoden för en projektbaserad offertrad är Tid och material genererar systemet ett datumbaserat faktureringsschema. Följ stegen nedan om du vill generera ett datumbaserat faktureringsschema automatiskt.

1. Gå till **Inställningar** > **Faktureringsfrekvenser** och konfigurera en faktureringsfrekvens.
2. På sidan **Offerter** öppnar du projektofferten och under fliken **Sammanfattning** anger du ett önskat leveransdatum.
3. Öppna offertraden för tid och material som du behöver skapa ett datumbaserat faktureringsschema för. 
4. Under fliken **Faktureringsschema** väljer du värden i fälten **Faktureringsstart** och **Faktureringsfrekvens**. 
5. I underrutnätet väljer du **Generera faktureringsschema**.
6. Programmet genererar faktureringsschemat med fälten **Fakturans kördatum** , **Transaktionens sista datum** och **Körstatus** på följande sätt:

    - **Fakturans kördatum** är inställt på det datum som dikteras utifrån faktureringsfrekvensen.
    - **Transaktionens sista datum** har angetts till dagen före **fakturans kördatum**.
    - **Körstatus** är automatiskt inställd på **Ej körd**. När jobbet för automatiskt skapande av faktura körs för ett visst fakturadatum uppdateras detta fält till antingen **Körning klar** eller **Körning misslyckades**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Skapa ett faktureringsschema för fast pris för en projektbaserad offertrad

När den projektbaserade offertraden har faktureringsmetoden **Fast** skapas ett milstolpebaserat faktureringsschema. Utför följande steg för att automatiskt generera schemat för en fast uppsättning milstolpar som är jämnt fördelade över kalenderperioden.

1. Gå till **Inställningar** > **Faktureringsfrekvenser** och konfigurera en faktureringsfrekvens.
2. På sidan **Offerter** öppnar du projektofferten och under fliken **Sammanfattning** anger du ett önskat leveransdatum.
3. Öppna offertraden för fast pris som du behöver skapa ett milstolpeschema för. 
4. Under fliken **Faktureringsschema** väljer du värden i fälten **Faktureringsstart** och **Faktureringsfrekvens**. 
5. I underrutnätet väljer du **Generera periodiska milstolpar**.
6. Programmet genererar faktureringsschemat med ett namn, datum och belopp för milstolpen.

    - Milstolpens namn är inställt på det datum som dikteras utifrån faktureringsfrekvensen.
    - Milstolpens datum är inställt på det datum som dikteras utifrån faktureringsfrekvensen.
    - Milstolpens belopp beräknas genom att dela offertbeloppet på den projektbaserade offertraden med antalet milstolpar som styrs av frekvensen och faktureringsstarten och önskade leveransdatum.
    - Om offertraden också har ett uppskattat momsbelopp delas det här värdet lika mellan varje milstolpe när periodiska milstolpar genereras.

### <a name="manually-create-milestones"></a>Skapa milstolpar manuellt

Milstolpar med fast pris kan också skapas manuellt när de inte delas periodiskt. Skapa en milstolpe manuellt:

Öppna offertraden Fast pris där du behöver skapa en milstolpe. Under fliken **Faktureringsschema** i underrutnätet väljer du **+ Skapa ny milstolpe för offertrad** och ange den information som krävs utifrån följande tabell.

| **Fält** | **Plats** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Milstolpens namn | Snabbregistrering | Namnet på milstolpen. | Detta sprids till milstolpen i projektets kontraktrad och till fakturan |
| Projektuppgift | Snabbregistrering | Om milstolpen är knuten till en projektuppgift kan du använda den här referensen för att lägga till anpassad logik och ange milstolpens status utifrån uppgiftens status. | Programmet har inte någon inverkan nedströms för den här referensen till en uppgift. |
| Milstolpens datum | Snabbregistrering | Ange det datum då processen för automatiskt skapande av faktura ska söka efter statusen för den här milstolpen för att överväga fakturering. | Detta sprids till milstolpen i projektets kontraktrad och till fakturan. |
| Fakturastatus | Snabbregistrering | När en milstolpe skapas är statusen alltid inställd på **Inte klar för fakturering**. | Detta sprids till milstolpen i projektets kontraktrad och till fakturan. |
| Radbelopp | Snabbregistrering | Beloppet eller värdet för den milstolpe som ska faktureras kunden. | Detta sprids till milstolpen i projektets kontraktrad och till fakturan. |
| Moms | Snabbregistrering | Momsbelopp som ska tillämpas på milstolpen. | Detta sprids till milstolpen i projektets kontraktrad och till fakturan. |
