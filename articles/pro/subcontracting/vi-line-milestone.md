---
title: Leverantörsfakturarader för milstolpar
description: Denna artikel förklarar hur du skapar leverantörsfakturarader för milstolpar för en underleverantör.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261051"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Leverantörsfakturarader för milstolpar

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En leverantörsfaktura i Microsoft Dynamics 365 Project Operations kan har leverantörsfakturarader för milstolpar som definieras på en underleverantörsrad. Projektansvariga kan använda leverantörsfakturarader för milstolpar, detta för att registrera kostnader för tjänster som köps in som milstolpebaserade kostnader för tjänster eller produkter som förs in i projektet.

Leverantörsfakturarader för milstolpar måste alltid referera till en underleverantörsrad med faktureringsmetoden Fast pris. Om en leverantörsfakturarad för milstolpar refererar till en underleverantörsrad kan projektansvariga matcha och verifiera den underliggande kostnad för tid, utgifter och material som refererar till denna underleverantörsrad genemot den milstolpe som faktureras av leverantören.

Följande tabell innehåller information om fälten för milstolpar på leverantörsfakturarader.

| Fält | Description | Funktionellt påverkan |
| --- | --- | --- |
| Name | Namnet på leverantörsfakturaraden (i identifieringssyfte). | Detta namn visas som den första kolumnen i alla uppslag som baseras på leverantörsfakturarader. |
| Description | En kort beskrivning av de tjänster som faktureras av leverantören på leverantörsfakturaraden. | None |
| Underleverantörskontrakt | Den underleverantör som tjänsterna ursprungligen beställdes på. | När en underleverantör väljs för leverantörsfakturan ärver alla rader på leverantörsfakturan det valet. En leverantörsfaktura kan inte ha leverantörsfakturarader som refererar till olika underleverantörer. |
| Kontraktrad för underleverantör | Den underleverantörsrad som tjänsterna ursprungligen beställdes på. Den lista över underkontaktrader som kan markeras är begränsad till raderna på det markerade underkontraktet. | När en underleverantörsrad väljs på en leverantörsfakturarad för milstolpar är fälten **Roll** och **Transaktionskategori** samt produktrelaterade fält irrelevanta och inte tillgängliga. Fälten **Kvantitet**, **Enhet** och **Enhetsgrupp** är inte heller relevanta för milstolpebaserade leverantörsfakturarader. |
| Transaktionsdatum | Det datum då den faktiska kostnaden för leverantörsfakturaraden registreras i projektet. | None |
| Transaktionsklass | Välj **Milstolpe** om du vill registrera en leverantörsfaktura för en slutförd milstolpe som definierats på en underleverantörsrad. | None |
| Milstolpe | Markera den milstolpe som definierats på den relaterade underleverantörsraden som markerats som **Redo att fakturera**. | Milstolpar på kontraktsrader för underleverantör och har statusen **Redo att fakturera** kan väljas på en leverantörsfakturarad. |
| Project | Namnet på det projekt där de tjänster som faktureras användes. | detta fält är obligatoriskt och får inte lämnas tomt. |
| Aktivitet | Namnet på den projektuppgift där de tjänster som faktureras användes. Detta fält är endast tillgängligt om ett projekt har markerats. Val av projektuppgift är valfritt. | Om det här fältet lämnas tomt kan projektledaren matcha leverantörsfakturaraden med klassen för transaktioner på den relaterade underleverantörsraden som registreras för alla uppgifter i projektet. Om leverantörens fakturarad inte refererar till en underleverantörsrad och det här fältet lämnas tomt, länkas inte den faktiska kostnaden som skapas av leverantörens fakturarad till några ofakturerade försäljningsvärden. Om uppgiftsbaserad fakturering har konfigurerats kanske kostnaderna i detta fall inte kan faktureras till slutkunden. |
| Milstolpebelopp | Enge värdet för den milstolpe som definierats på den underleverantörsrad som är redo att faktureras. | None |
| Moms | Ange momsbeloppet. | None |
| Totalbelopp | Totalt belopp för leverantörens fakturarad, inklusive moms. Detta fält beräknas som *Belopp för milstolpe* + *Moms*. | None |

> [!NOTE]
> När en leverantörsfakturarad som refererar till en milstolpe för underleverantörsrad skapas, uppdateras statusen för underleverantörsmilstolparna till **leverantörsfaktura skapad**. När den leverantörsfakturan sedan bekräftas uppdateras statusen för milstolpen för underleverantörsrad till **Leverantörsfaktura bekräftad**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
