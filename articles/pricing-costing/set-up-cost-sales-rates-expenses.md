---
title: Konfigurera kostnads- och försäljningstaxa för utgifter
description: I det här ämnet finns information om hur du konfigurerar kostnads- och försäljningstaxor för transaktions- och utgiftskategorier.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b518c9eda00bef4d342dd66677344af516012749
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180304"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Konfigurera kostnads- och försäljningstaxa för utgifter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan konfigurera kostnads- och försäljningspriser för transaktionskategorier i Dynamics 365 Project Operations. Eftersom kostnaden och försäljningspriset är utformade för utgifter måste även varje transaktionskategori som innehåller dessa vara inställd som en utgiftskategori. Detta innebär att precisionen garanteras i underordnad funktion. Kostnads- och försäljningspriser för transaktionskategorier kan endast visas i en valuta, som måste vara valutan i prislistans huvud.

Följ stegen nedan om du vill ange kostnadstaxa och försäljningstaxa för transaktionskategorier. 

1. Skapa en prislista utifrån prislistans huvud. 
2. I **kategoripriser** i underrutnätet väljer du **+ Nytt kategoripris**. 
3. På sidan **Snabbskapa** anger du transaktionskategori och enhet som du skapar det nya priset för.

I följande tabell visas fälten i fliken **Allmänt** och sidan **Snabbskapa** för en kategoriprisrad som du bör ha i åtanke när du skapar kategoripriser i en försäljnings- eller kostnadsprislista.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| Transaktionskategori | Fliken **Allmänt** och sidorna **Snabbskapa** | Välj den transaktionskategori som du vill skapa en försäljnings- eller självkostnad för. | Transaktionskategorin för inkommande uppskattade eller faktiska värden för utgifter matchas mot den här raden så att kostnads- eller försäljningstaxan för transaktionskategorin blir standard. |
| Enhetsschema | Fliken **Allmänt** och sidorna **Snabbskapa** | Enheten schemalägger standardvärden från transaktionskategorins enhetsschema. | Det här fältet har ingen inverkan nedströms. |
| Enhet | Fliken **Allmänt** och sidorna **Snabbskapa** | Välj den enhet som taxorna ska ställas in för. | Enheten för inkommande uppskattade eller den faktiska värden matchas mot enheten på denna rad så att taxan i utgiftsuppskattningen eller det faktiska värdet blir standard. |
| Prismodell | Fliken **Allmänt** och sidorna **Snabbskapa** | Möjliga värden för fältet **Prissättningsmetod** är **Pris per enhet**, **Till kostnad** och **Pålägg över kostnad**. | Under prisinställning väljer du **Pris per enhet** för att låsa fältet **Procentsats** på kategoriprisraden. Om **Till kostnad** har valts låses fälten **Pris** och **Procentsats** på försäljningsprislistan. Om du väljer **Pålägg över kostnad** låser du fältet **Pris** i försäljningsprislistan. På en rad för inkommande faktiskt värde leder prissättningsmetoderna **Till kostnad** eller **Pålägg över kostnad** till att motsvarande rad för ofakturerad försäljning tilldelas ett pris som är lika med priset i det faktiska kostnadsvärdet eller beräknas som ett pålägg över priset. |
| Pris | Fliken **Allmänt** och sidorna **Snabbskapa** | Konfigurera ett styckpris för kombinationen av transaktionskategori och enhet. Taxan för körsträcka är till exempel 10 USD per mile och 8 USD per kilometer. | Taxan för körsträcka är den taxa som använder styckpriset eller kostnaden på raden för inkommande uppskattade eller faktiska värden för en transaktionsklass för utgifter.|
| Procent | Fliken **Allmänt** och sidorna **Snabbskapa** | Konfigurera en procentsats över kostnaden för kombinationen av transaktionskategori och enhet. Till exempel ska flygtaxa ha ett pålägg på 10 procent över kostnaden för flygutgiften. | Denna procentsats över kostnaden gäller endast för en försäljningsprislista när prissättningsmetoden som valts är **Pålägg över kostnad**. |
| Valuta | Fliken **Allmänt** och sidorna **Snabbskapa** | Som standard hämtas värdet från valutan i huvudet i prislistan. För prissättningen av transaktionskategorierna kan valutan inte åsidosättas. | Valutan använder styckpriset på raden för inkommande faktiska värden för transaktionsklassen för kostnad och försäljning. |

## <a name="pricing-methods-for-expenses"></a>Prissättningsmetoder för utgifter

När du konfigurerar kategoripriser som endast är relevanta i samband med utgiftsprissättning kan du använda någon av följande tre prissättningsmetoder:

- **Pris per enhet**
- **Vid kostnad**
- **Pålägg över kostnad**

### <a name="price-per-unit"></a>Pris per enhet
När den här prissättningsmetoden väljs på en kategoriprisrad som är länkad till en försäljningsprislista är priset standardvärdet för kategori- och enhetskombinationen både i uppskattning och faktiska värden. Uppskattning hänvisar till projektuppskattningsrader för utgifter, offertradsinformationen och kontraktradsinformationen för utgifter.

### <a name="at-cost"></a>Vid kostnad
När den här prissättningsmetoden väljs på kategoriprisraden som är länkad till en försäljningsprislista är priset standardvärdet för kategori- och enhetskombinationen enbart för det faktiska utgiftsvärdet. Till exempel faktiska ofakturerade försäljningsvärden för utgiftstransaktionsklassen. Styckpriset anges som faktiskt ofakturerat försäljningsvärde från styckpriset i det faktiska kostnadsvärdet för den utgiften. Pris som standardiseras utifrån kostnad görs inte på projektuppskattningar av utgifter eller i offertrads- och kontraktradsinformation för utgifter.

### <a name="markup-over-cost"></a>Pålägg över kostnad
När den här prissättningsmetoden väljs på kategoriprisraden som är länkad till en försäljningsprislista är priset standardvärdet för kategori- och enhetskombinationen enbart för ett faktiskt utgiftsvärde. Till exempel faktiska ofakturerade försäljningsvärden för utgiftstransaktionsklassen. Det här styckpriset anges som faktiskt ofakturerat försäljningsvärde till ett beräknat värde från styckpriset på det faktiska kostnadsvärde som angetts för utgiften efter att den definierade påläggsprocenten har tillämpats. Pris som standardiseras utifrån kostnad görs inte på projektuppskattningar av utgifter eller i offertrads- och kontraktradsinformation för utgifter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]