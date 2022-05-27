---
title: Konfigurera kostnadstaxa för arbete – Lite
description: I det här ämnet finns information om hur du konfigurerar kostnadstaxa för arbete i Project Operations.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 01e3b41ca5c8fcc9146186873e0f44daad020c6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575694"
---
# <a name="set-up-labor-cost-rates---lite"></a>Konfigurera kostnadstaxa för arbete – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Varje prislista har en uppsättning arbetstaxor (rollpriser) som överensstämmer med innehåll och giltighetsdatum i prislistan.

1. Skapa en prislista och fliken **Rollpris** i underrutnätet, välj **Ny roll**.
2. På sidan **Snabbskapa** väljer du roll och organisationsenhet.
3. Ange eventuell annan information som krävs.

Följande tabell innehåller några av de fält som är viktiga när det gäller skapande av arbetstaxa i en kostnadsprislista.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| Roll | Fliken **Allmänt** och sidorna **Snabbskapa** | Välj den roll som kostnadstaxan gäller för. | Rollen för inkommande uppskattade eller faktiska värden matchas mot den här raden så att kostnaden för rollen blir standard. |
| Resursenhet | Fliken **Allmänt** och sidorna **Snabbskapa** | Välj organisationsenhet eller avdelning av det företag där rollen ska användas. Det kan till exempel vara en utvecklare från Robotics-avdelningen av Fabrikam Indien eller en utvecklare från programvaruavdelningen av Fabrikam USA. | Resursenheten för inkommande uppskattade eller faktiska värden matchas mot den här raden så att kostnaden för rollen blir standard. |
| Pris | Fliken **Allmänt** och sidorna **Snabbskapa** | Ange kostnadstaxa för kombinationen av roll, resursföretag och resursenhet. Exempel: En utvecklare från Fabrikam Indien kostar 1 000 INR eller en utvecklare från Fabrikam USA kostar 150 USD. | Priset är den kostnadstaxa som använder styckpriset på raden för inkommande uppskattade eller faktiska värden för transaktionsklassen **Tid**. |
| Valuta | Fliken **Allmänt** och sidorna **Snabbskapa** | Som standard hämtas valutavärdet från valutan i huvudet i kostnadsprislistan, men kan åsidosättas. Exempel: En utvecklare från Fabrikam Indien kostar 1 000 INR. En utvecklare från Fabrikam USA kostar 150 USD. | Valutan använder styckpriset på kostnadsraden för inkommande faktiska värden för transaktionsklassen **Tid**. Vid en projektuppskattning konverteras valutavärdet till projektvalutan och visas i tidsfasad vy över uppskattningen. |
| Enhetsschema | Fliken **Allmänt** och sidorna **Snabbskapa** | Enhetsschemat använder Tid och kan inte ändras för entiteten Rollpris eftersom det uttrycker taxor i tidsenheter. | Detta har ingen inverkan nedströms. |
| Enhet | Fliken **Allmänt** och sidorna **Snabbskapa** | Som standard hämtas värdet från fältet **Tidsenhet** i huvudet i kostnadsprislistan. Värdet kan åsidosättas. Exempel: En utvecklare från Fabrikam Indien kostar 1 000 INR per **indisk day**. En utvecklare från Fabrikam USA kostar 150 USD per **amerikansk dag**. | Systemet använder systemet för enheter och konvertering i basenheter för att beräkna ett styckpris för att beräkna standardpriset per enhet på en rad för inkommande uppskattade eller faktiska värden. Till exempel är en uppskattning på 10 **indiska dagar** av arbete för en utvecklare från Indien och enheten **indisk dag** definieras som 10 timmar. Vid kostnadsredovisning av den uppskattningsraden beräknar programmet styckkostnaden i uppskattningen enligt följande: 1 000 INR/10 hours = 100 INR per timme, vilket konverteras till USD och visas som styckkostnad på sidan **Projektuppskattningar**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Överföra priser och kostnader för resurser utanför din avdelning eller juridiska person

I projektbaserade företag är det vanligt att använda anställda från olika juridiska personer eller avdelningar i projekt. Ett projekt kan utföras av en juridisk person, men de medarbetare eller konsulter som arbetar på projektet kan komma från samma juridiska person eller från en annan, eller så kan det finnas en kombination av båda. I Dynamics 365 Project Operations är den juridiska entitet som äger leverans av projektet är **Ägande företag** och den avdelning som äger leverans **uppslagsenhet**. Andra juridiska personer som tillhandahåller resurser är **resursföretag** och avdelningar som tillhandahåller resurser är **resursenheter**. I de flesta länder krävs ett företag för att säkerställa att den juridiska personen eller avdelningen för resurser debiterar det ägande företaget och den kontrakterande enheten för användningen av resurser.

Företaget Fabrikam måste exempelvis se till att Fabrikam India-Robotics har förhandlat en kostnadsprislista med Fabrikam US-Robotics eller Fabrikam UK-Robotics.

En utvecklare från Fabrikam India-Robotics tar 100 USD vid utlånande till Fabrikam US-Robotics och 150 USD vid utlånande till Fabrikam UK-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Ställ in kostnader för externa resurser

1. Skapa en kostnadsprislista med namnet, *Fabrikam US-Robotics kostnadstaxor* och ange ett giltigt datumintervall.
2. I kostnadsprislistan anger du taxor med hjälp av informationen i följande tabell. 

| Roll | Resursföretag | Resursenhet | Kostnadstaxa |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | 100 |
| Developer | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
| Developer | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Bifoga den här kostnadsprislistan till organisationsenheten Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Ställ in överföringspriser för en resurs i den aktuella valutan 

I Project Operations kan du konfigurera resursprissättningen i alla valutor. Som standard används valutan i prislistans huvud, men kan ändras.

Med exemplet för inställning av överföringspris kan informationen ändras till:

Företaget Fabrikam måste se till att Fabrikam India-Robotics har förhandlat en kostnadstaxa med Fabrikam US-Robotics eller Fabrikam UK-Robotics.

En utvecklare från Fabrikam India-Robotics kostar 5000 INR vid utlånande till Fabrikam US-Robotics och 5500 INR vid utlånande till Fabrikam UK-Robotics.

I kostnadsprislistan för Fabrikam US-Robotics kan kostnadstaxan uttryckas som:

| Roll | Resursföretag | Kostnad |
| --- | --- | --- |
| Developer | Fabrikam India | 5 000 INR |
| Developer | Fabrikam US | 115 USD |

I kostnadsprislistan för Fabrikam UK-Robotics kan kostnadstaxan uttryckas enligt nedan:

| Roll | Resursföretag | Kostnad |
| --- | --- | --- |
| Developer | Fabrikam India | 5 500 INR |
| Developer | Fabrikam UK | 115 GBP |

Kostnadsprislistan kan ge arbetstaxor i flera olika valutor. När du genererar en kostnadsuppskattning i projektet konverterar Project Operations de här kostnadstaxorna till projektvalutan och visar dessa för användaren. När en tidspost godkänns och en faktisk kostnad skapas prissätts den faktiska kostnaden i valutan på den motsvarande rollprisraden i kostnadsprislistan. Faktiska kostnader för tid i ett enskilt projekt kan registreras i flera olika valutor. När de faktiska arbetskostnaderna på projektnivå slås samman eller summeras kommer dock Project Operations att konvertera alla arbetskostnadsbelopp till projektvalutan, som användaren kan visa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]