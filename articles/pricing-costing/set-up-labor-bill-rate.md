---
title: Konfigurera fakturataxa för arbete
description: I det här ämnet finns information om hur du konfigurerar fakturataxa för arbete i Project Operations.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ffb947533a42ace3615e7755c12a5ab69491f747
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585538"
---
# <a name="set-up-labor-bill-rates"></a>Konfigurera fakturataxa för arbete

**Gäller:** Project Operations för resursbaserade/icke-lagerbaserade scenarier

Varje prislista har en uppsättning rollpriser, eller arbetstaxor, som gäller för det samband och datum som anges på prislistans huvud. Fakturataxa för tid i Dynamics 365 Project Operations kan endast anges i en valuta, vilket är valutan i sidhuvudet Prislista.

1. För att ställa in fakturataxa för arbete för en försäljningsprislista, gå till **Sales** > **Kunder** > **Prislistor** och välj **Ny** för att skapa en ny prislista. 
2. Under fliken **Rollpriser**, in underrutnätet, väljer du **Nytt rollpris**. 
3. I fönstret **Snabbskapa** anger du kombinationen av roll och organisationsenhet som du vill konfigurera fakturataxan för.

   I följande tabell visas fälten i fliken **Allmänt** och rutan **Snabbskapa** för en rollprisrad som du måste ha i åtanke när du skapar rollpriser i en försäljningsprislista:

    | Fält | Plats | Beskrivning | Inverkan nedströms |
    | --- | --- | --- | --- |
    | Roll | Fliken **Allmänt** och rutan **Snabbskapa** | Välj den roll du ställer in fakturataxan för. | Rollen för inkommande uppskattade eller faktiska värden matchas mot den här raden så att fakturataxan för rollen blir standard. |
    | Resursföretag | Fliken **Allmänt** och rutan **Snabbskapa** | Välj det företag eller den juridiska person som rollen kommer från. Exempel: En utvecklare från Fabrikam Indien eller en utvecklare från Fabrikam USA. | Resursföretaget för inkommande uppskattade eller faktiska värden matchas mot den här raden så att fakturataxan för rollen blir standard. |
    | Resursenhet | Fliken **Allmänt** och rutan **Snabbskapa** | Välj organisationsenhet eller avdelning av det företag som rollen kommer från. Det kan till exempel vara en utvecklare från Robotics-avdelningen av Fabrikam Indien eller en utvecklare från programvaruavdelningen av Fabrikam USA. | Resursenheten för inkommande uppskattade eller faktiska värden matchas mot den här raden så att fakturataxan för rollen blir standard. |
    | Pris | Fliken **Allmänt** och rutan **Snabbskapa** | Ange fakturataxa för kombinationen av roll, resursföretag och resursenhet. En utvecklare från Fabrikam India har till exempel en fakturataxa på 100 USD eller en utvecklare från Fabrikam USA har en fakturataxa på 150 USD. | Priset är standardfakturataxan för styckpriset på raden för inkommande uppskattade eller faktiska värden för transaktionsklassen Tid. |
    | Valuta | Fliken **Allmänt** och rutan **Snabbskapa**| Som standard hämtas valutavärdet från valutan i huvudet i försäljningsprislistan. I en försäljningsprislista kan inte valutan åsidosättas. | Valutan är standardvalutan för styckpriset på raden för inkommande faktiska försäljningsvärden för transaktionsklassen Tid. |
    | Enhetsschema | Fliken **Allmänt** och rutan **Snabbskapa** | Enhetsschemat använder Tid och kan inte ändras för entiteten Rollpris eftersom det uttrycker taxor i tidsenheter. | Det här fältet har ingen inverkan nedströms. |
    | Enhet | Fliken **Allmänt** och rutan **Snabbskapa** | Enhetsvärdet hämtas från fältet **Tidsenhet** i huvudet i försäljningsprislistan. Men värdet kan åsidosättas. Exempel: En utvecklare från Fabrikam India har en fakturataxa på 1 000 USD per **indisk dag**. En utvecklare från Fabrikam USA har en fakturataxa på 1 500 USD per **amerikansk dag**. | När styckpriset standardiseras från en rad för inkommande uppskattade eller faktiska värden använder systemet systemet för enheter och konvertering i basenheter för att beräkna ett styckpris. Till exempel är en uppskattning på 10 **indiska dagar** av arbete för en utvecklare från Indien och enheten indisk dag definieras som 10 timmar. Vid prissättning av uppskattningsrad beräknar programmet styckpriset i uppskattningen som 1 000 USD/10 timmar = 100 USD per timme. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Överföra prissättning eller konfigurera fakturataxor för resurser från andra organisationsenheter eller avdelningar 

På projektbaserade företag används ofta anställda från olika juridiska personer och olika avdelningar inom den juridiska personen för att arbeta med projekt. Projekt kan utföras av en viss juridisk person och avdelning, men de medarbetare eller konsulter som arbetar på projektet kan komma från samma juridiska person och avdelning eller från en annan. Projektet kan också bestå av en kombination av personer från olika juridiska personer och avdelningar. I Project Operations är den juridiska personen som äger leveransen av projektet det **ägande företaget** och den avdelning som äger leveransen är den **kontrakterande enheten**. Alla andra juridiska personer som tillhandahåller resurser är **resursföretag** och avdelningar som tillhandahåller resurser är **resursenheter**. På grund av olikheterna i arbetskostnaderna för olika geografier och arbetsmarknader i världen konfigureras fakturataxor på olika sätt för olika geografier.

Exempel: En utvecklare från Robotics-avdelningen av Fabrikam India som arbetar på USA-projekt faktureras med taxan 100 USD per timme. En utvecklare från Robotics-avdelningen av Fabrikam US som arbetar på USA-projekt faktureras med taxan 150 USD per timme. 

### <a name="example-set-up-a-bill-rate"></a>Exempel: Konfigurera en fakturataxa 

1. Skapa en försäljningsprislista med namnet *Fakturataxa för Fabrikam US* och ange giltighetsdatum.
2. I försäljningsprislistan anger du följande information om taxa:

    | Roll | Resursföretag | Resursenhet | Fakturataxa |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India – Robotics | 100 |
    | Developer | Fabrikam Philippines | Fabrikam Philippines – Robotics | 90 USD |
    | Developer | Fabrikam US | Fabrikam US – Robotics | 150 USD |

3. Bifoga försäljningsprislistan, **Fakturataxa för Fabrikam US** till projektprislistan för projektkontraktet eller till ett visst konto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
