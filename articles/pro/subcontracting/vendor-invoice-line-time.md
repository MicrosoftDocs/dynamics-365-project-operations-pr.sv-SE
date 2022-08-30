---
title: Leverantörsfakturarader för tid
description: I denna artikel beskrivs hur du registrerar leverantörersfakturarader för tidskostnader som underleverantörer anger.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262035"
---
# <a name="vendor-invoice-lines-for-time"></a>Leverantörsfakturarader för tid

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En leverantörsfaktura i Microsoft Dynamics 365 Project Operations kan ha leverantörsfakturarader för tid. Projektansvariga kan använda leverantörers fakturarader för tid för att registrera kostnaderna för underleverantörers tid i projekt.

Leverantörens fakturarader för tid kan ha (eller inte) referenser till en underleverantörsrad för tid. Om en leverantörsfakturarad för tid refererar till en underleverantör kan projektansvariga matcha och kontrollera den tid som leverantörens fakturarad fakturerar mot tid som registreras av underleverantörer och som har godkänts av projektansvariga i projektet.

Följande tabell innehåller information om fälten för tid på leverantörsfakturarader.

| Fält | Description | Funktionellt påverkan |
| --- | --- | --- |
| Name | Namnet på leverantörsfakturaraden (i identifieringssyfte). | Detta namn visas som den första kolumnen i alla uppslag som baseras på leverantörsfakturarader. |
| Description | En kort beskrivning av de tjänster som faktureras av leverantören på leverantörsfakturaraden. | None |
| Underleverantörskontrakt | Den underleverantör som tjänsterna ursprungligen beställdes på. | När en underleverantör väljs för leverantörsfakturan ärver alla rader på leverantörsfakturan det valet. En leverantörsfaktura kan inte ha leverantörsfakturarader som refererar till olika underleverantörer. |
| Kontraktrad för underleverantör | Den underleverantörsrad som tjänsterna ursprungligen beställdes på. Den lista över underkontaktrader som kan markeras är begränsad till raderna på det markerade underkontraktet. | När en underleverantörsrad väljs på en leverantörsfakturarad för tid anges standardvärden för fälten **Projekt**, **Roll** och **Bokningsbar resurs** från motsvarande fält på underleverantörsraden. Om den valda underleverantörsraden har värden i fälten **Projekt**, **Roll** och **Bokningsbar** kan inte värdena för motsvarande fält på leverantörsfakturaraden skilja sig åt från dessa värden. |
| Transaktionsdatum | Det datum då den faktiska kostnaden för leverantörsfakturaraden registreras i projektet. | None |
| Transaktionsklass | Standardvärdet är **Tid**. | Värdet **Tid** anger att leverantörens fakturarad används för att registrera fakturabeloppet för underleverantörstid. |
| Project | Namnet på det projekt där de tjänster som faktureras användes. | detta fält är obligatoriskt och får inte lämnas tomt. |
| Aktivitet | Namnet på den projektuppgift där de tjänster som faktureras användes. Detta fält är endast tillgängligt om ett projekt har markerats. Val av projektuppgift är valfritt. | Om detta fält lämnas tomt kan projektledaren matcha leverantörsfakturaraden med den tid som registreras av underleverantörsresurser för alla uppgifter i projektet. Om leverantörens fakturarad inte refererar till en underleverantörsrad och det här fältet lämnas tomt, länkas inte den faktiska kostnaden som skapas av leverantörens fakturarad till några ofakturerade försäljningsvärden. Om uppgiftsbaserad fakturering har konfigurerats kanske kostnaderna i detta fall inte kan faktureras till slutkunden. |
| Roll | Rollen för de underleverantörsresurser vars tid faktureras. | Detta fält anger den roll som utförs av de underleverantörsresurser vars tid faktureras på leverantörsfakturan. |
| Bokningsbar resurs | Namnet på den underleverantör vars tid faktureras. Valet av bokningsbar resurs är valfritt. | Om detta fält lämnas tomt kan projektledaren matcha leverantörsfakturaraden med den tid som registreras av valfri resurs som tillhör leverantören på leverantörsfakturaraden. |
| Kvantitet | Ange antalet timmar som faktureras av leverantören på leverantörsfakturaraden. |None |
| Enhetsgrupp | Standardvärdet är **Tidsenhetsgrupp** och kan inte ändras. | None |
| Enhet | Standardvärdet är basenhet i timmar från tidsenhetsgruppen. Du kan ändra detta värde om du vill köpa valfri tidsenhetsgrupp, till exempel dag eller vecka. | Kombinationen av värdena **Roll** och **Enhet** kommer att användas som standard- eller beräknat värde för fältet **Enhetspris** på leverantörsfakturaraden. |
| Enhetspris | Standardenhetspriset använder kombinationen av värdena för **Roll** och **Enhet** från den projektprislista som är tillämpbar på leverantörsfakturaradens transaktionsdatum. | Om priset för den tillämpbara projektprislistan ställs in i en enhet som skiljer sig åt från enheten på leverantörens fakturarad, använder systemet enhetskonverteringen för att beräkna priset per enhet. |
| Delsumma | Detta skrivskyddade fält beräknas som *Kvantitet* &times; *Enhetspris* om värdena anges i såväl fältet **Kvantitet** som fältet **Enhetspris**. Om ett eller båda dessa fält är tomma kan du ange ett värde i det här fältet. | None |
| Moms | Ange momsbeloppet. | None |
| Totalbelopp | Totalt belopp för leverantörens fakturarad, inklusive moms. Detta fält beräknas som *Delsumma* + *Moms*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
