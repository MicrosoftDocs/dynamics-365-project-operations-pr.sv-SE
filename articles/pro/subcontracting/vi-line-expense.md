---
title: Leverantörsfakturarader för utgiftskategorier
description: I detta ämne beskrivs hur du registrerar leverantörsfakturarader för utgiftskategorier.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579558"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Leverantörsfakturarader för utgiftskategorier

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En leverantörsfaktura i Microsoft Dynamics 365 Project Operations kan ha leverantörsfakturarader för utgiftskategorier. Projektansvariga kan använda leverantörsfakturarader för utgiftskategorier i syfte att registrera kostnader för tjänster som köps in som utgiftskategorier.

Leverantörsfakturarader för utgiftskategorier kan ha (eller inte) referenser till en underleverantörsrad för utgiftskategorier. Om en leverantörsfakturarad för utgiftskategorier refererar till en underleverantör kan projektansvariga matcha och verifiera de utgifter som leverantörsfakturaraden fakturerar mot mot utgifter som registreras mot dessa utgiftskategorier och godkänns av projektansvariga.

Följande tabell innehåller information om fälten på leverantörsfakturarader för utgiftskategorierna.

| Fält | Description | Funktionellt påverkan |
| --- | --- | --- |
| Name | Namnet på leverantörsfakturaraden (i identifieringssyfte). | Detta namn visas som den första kolumnen i alla uppslag som baseras på leverantörsfakturarader. |
| Description | En kort beskrivning av de tjänster som faktureras av leverantören på leverantörsfakturaraden. | None |
| Underleverantörskontrakt | Den underleverantör som tjänsterna ursprungligen beställdes på. | När en underleverantör väljs för leverantörsfakturan ärver alla rader på leverantörsfakturan det valet. En leverantörsfaktura kan inte ha leverantörsfakturarader som refererar till olika underleverantörer. |
| Kontraktrad för underleverantör | Den underleverantörsrad som tjänsterna ursprungligen beställdes på. Den lista över underkontaktrader som kan markeras är begränsad till raderna på det markerade underkontraktet. | När en underleverantörsrad väljs på en leverantörsfakturarad för utgiftskategorier kommer standardvärden för fälten **Projekt**, **Uppgift** och **Transaktionskategori** från motsvarande fält på underleverantörsraden. Om den valda underleverantörsraden har värden i fälten **Projekt**, **Projektuppgift** och **Transaktionskategori** kan inte värdena för motsvarande fält på leverantörsfakturaraden skilja sig åt från dessa värden. |
| Transaktionsdatum | Det datum då den faktiska kostnaden för leverantörsfakturaraden registreras i projektet. |None |
| Transaktionsklass | Välj **Utgift** om du vill registrera en leverantörsfaktura för en utgiftskategori. | Värdet **Utgift** anger att leverantörens fakturarad används för att registrera fakturabeloppet för tjänster som köpts in som utgiftskategorier. |
| Project | Namnet på det projekt där de tjänster som faktureras användes. | detta fält är obligatoriskt och får inte lämnas tomt. |
| Aktivitet | Namnet på den projektuppgift där de tjänster som faktureras användes. Detta fält är endast tillgängligt om ett projekt har markerats. Val av projektuppgift är valfritt. | Om detta fält lämnas tomt kan projektledaren matcha leverantörsfakturaraden med utgifter som registrerats i någon av projektets uppgifter. Om leverantörens fakturarad inte refererar till en underleverantörsrad och det här fältet lämnas tomt, länkas inte den faktiska kostnaden som skapas av leverantörens fakturarad till några ofakturerade försäljningsvärden. Om uppgiftsbaserad fakturering har konfigurerats kanske kostnaderna i detta fall inte kan faktureras till slutkunden. |
| Transaktionskategori | Den transaktionskategori som faktureras. En motsvarande utgiftskategori måste skapas för den valda transaktionskategorin. | Kombinationen av värdena **Transaktionskategori** och **Enhet** kommer att användas som standard- eller beräknat värde för fältet **Enhetspris** på leverantörsfakturaraden. |
| Kvantitet | Ange kvantiteten som leverantören fakturerar på fakturaraden. |None|
| Enhetsgrupp | Ett standardvärde anges utifrån enhetsgruppen för den valda transaktionskategorin. | None |
| Enhet | Standardvärdet är basenhet för den valda enhetsgruppen. Du kan ändra det här värdet för att köpa i valfri enhet av vald enhetsgrupp. | Kombinationen av värdena **Transaktionskategori** och **Enhet** kommer att användas som standard- eller beräknat värde för fältet **Enhetspris** på leverantörsfakturaraden. |
| Enhetspris | Standardenhetspriset använder kombinationen av värdena för **Transaktionskategori** och **Enhet** från den projektprislista som är tillämpbar på leverantörsfakturaradens transaktionsdatum. | Om priset för den tillämpbara projektprislistan ställs in i en enhet som skiljer sig åt från enheten på leverantörens fakturarad, använder systemet enhetskonverteringen för att beräkna priset per enhet. |
| Delsumma | Detta skrivskyddade fält beräknas som *Kvantitet* &times; *Enhetspris* om värdena anges i såväl fältet **Kvantitet** som fältet **Enhetspris**. Om ett eller båda dessa fält är tomma kan du ange ett värde i det här fältet.| None |
| Moms | Ange momsbeloppet. | None |
| Totalbelopp | Totalt belopp för leverantörens fakturarad, inklusive moms. Detta fält beräknas som *Delsumma* + *Moms*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
