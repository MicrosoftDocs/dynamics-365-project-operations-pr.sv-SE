---
title: Konfigurera fakturataxa för arbete
description: I det här ämnet finns information om hur du konfigurerar fakturataxa för arbete i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6294895857442f3a24a9d73ee07d2b90926a4fb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085602"
---
# <a name="setting-up-bill-rates-for-labor-rate-billing"></a>Konfigurera fakturataxa för fakturering av arbete 

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Varje prislista har en uppsättning rollpriser, eller arbetstaxor, som gäller för det samband och datum som anges på prislistans huvud. Fakturataxa för tid i Dynamics 365 Project Operations kan endast konfigureras i en valuta, vilket är valutan i prislistans huvud.

1. Om du vill konfigurera fakturataxor för arbete i en försäljningsprislista, skapar du en prislista baserad på prislistans huvud. 
2. Under fliken **Rollpriser** , in underrutnätet, väljer du **+ Nytt rollpris**. 
3. I fönstret **Snabbskapa** anger du kombinationen av roll och organisationsenhet som du vill konfigurera fakturataxan för.

  I följande tabell visas fälten i fliken **Allmänt** och rutan **Snabbskapa** för en rollprisrad som du måste ha i åtanke när du skapar rollpriser i en försäljningsprislista:

  | Fält | Plats | Relevans, syfte och vägledning | Inverkan nedströms |
  | --- | --- | --- | --- |
  | Roll | Fliken **Allmänt** och rutan **Snabbskapa** | Välj den roll du ställer in fakturataxan för. | Rollen för inkommande uppskattade eller faktiska värden matchas mot den här raden så att fakturataxan för rollen blir standard. |
  | Resursenhet | Fliken **Allmänt** och rutan **Snabbskapa** | Välj organisationsenhet eller avdelning av det företag som rollen kommer från. Det kan till exempel vara en utvecklare från Robotics-avdelningen av Fabrikam Indien eller en utvecklare från programvaruavdelningen av Fabrikam USA. | Resursenheten för inkommande uppskattade eller faktiska värden matchas mot den här raden så att fakturataxan för rollen blir standard. |
  | Pris | Fliken **Allmänt** och rutan **Snabbskapa** | Ange fakturataxa för kombinationen av roll, resursföretag och resursenhet. En utvecklare från Fabrikam India har till exempel en fakturataxa på 100 USD eller en utvecklare från Fabrikam USA har en fakturataxa på 150 USD. | Priset är standardfakturataxan för styckpriset på raden för inkommande uppskattade eller faktiska värden för transaktionsklassen Tid. |
  | Valuta | Fliken **Allmänt** och rutan **Snabbskapa**| Som standard hämtas valutavärdet från valutan i huvudet i försäljningsprislistan. I en försäljningsprislista kan inte valutan åsidosättas. | Valutan är standardvalutan för styckpriset på raden för inkommande faktiska försäljningsvärden för transaktionsklassen Tid. |
  | Enhetsschema | Fliken **Allmänt** och rutan **Snabbskapa** | Enhetsschemat använder Tid och kan inte ändras för entiteten Rollpris eftersom det uttrycker taxor i tidsenheter. | Det här fältet har ingen inverkan nedströms. |
  | Enhet | Fliken **Allmänt** och rutan **Snabbskapa** | Enhetsvärdet hämtas från fältet **Tidsenhet** i huvudet i försäljningsprislistan. Men värdet kan åsidosättas. Exempel: En utvecklare från Fabrikam India har en fakturataxa på 1 000 USD per **indisk dag**. En utvecklare från Fabrikam USA har en fakturataxa på 1 500 USD per **amerikansk dag**. | När styckpriset standardiseras från en rad för inkommande uppskattade eller faktiska värden använder systemet systemet för enheter och konvertering i basenheter för att beräkna ett styckpris. Till exempel är en uppskattning på 10 **indiska dagar** av arbete för en utvecklare från Indien och enheten indisk dag definieras som 10 timmar. Vid prissättning av uppskattningsrad beräknar programmet styckpriset i uppskattningen som 1 000 USD/10 timmar = 100 USD per timme. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Överföra prissättning eller konfigurera fakturataxor för resurser från andra organisationsenheter eller avdelningar 

Projektbaserade företag använder anställda från olika avdelningar av företaget för att arbeta på projekt. Projekt kan utföras från en avdelning även om de anställda eller konsulter kommer från samma eller olika avdelningar av företaget. Projektet kan också bestå av en kombination av personer från olika avdelningar. I Project Operations kallas företaget som äger leveransen av projektet den **kontrakterande enheten**. Alla andra avdelningar som tillhandahåller resurser kallas för **resursenheter**. På grund av olikheterna i arbetskostnaderna för olika geografier och arbetsmarknader i världen konfigureras fakturataxor på olika sätt för olika geografier.

Exempel: En utvecklare från Fabrikam India som arbetar på ett USA-projekt faktureras med taxan 100 USD per timme. En utvecklare från Fabrikam US som arbetar på USA-projekt faktureras med taxan 150 USD per timme.

### <a name="example-set-up-a-bill-rate"></a>Exempel: Konfigurera en fakturataxa

1. Skapa en försäljningsprislista med namnet *Fakturataxa för Fabrikam US* och ange giltighetsdatum.
2. I försäljningsprislistan anger du följande information om taxa:

    | Roll | Organisationsenhet | Fakturataxa |
    | --- | --- | --- |
    | Developer | Fabrikam India | 100 |
    | Developer | Fabrikam Philippines | 90 USD |
    | Developer | Fabrikam US | 150 USD |

3. Bifoga försäljningsprislistan, **Fakturataxa för Fabrikam US** till projektprislistan för projektkontraktet eller till ett visst konto.
