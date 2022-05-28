---
title: Leverantörsfakturarader för produkter
description: I detta ämne beskrivs hur du registrerar leverantörsfakturarader för produkter och använder de olika fälten för att registrera produktinköp från leverantörer.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599200"
---
# <a name="vendor-invoice-lines-for-products"></a>Leverantörsfakturarader för produkter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En leverantörsfaktura i Microsoft Dynamics 365 Project Operations kan ha leverantörsfakturarader för produkter (kallas även "material"). Projektansvariga kan använda leverantörers fakturarader för produkter för att registrera kostnaderna för produkter som köpts i projekt.

Leverantörens fakturarader för produkter kan ha (eller inte) referenser till en underleverantörsrad för material. Om en leverantörsfakturarad för produkter refererar till en underleverantör kan projektansvariga matcha och kontrollera de produkter som leverantörens fakturarad fakturerar mot användningen av inköpta produkter som registreras av och godkänns av projektansvariga.

Följande tabell innehåller information om fälten för produkter på leverantörsfakturarader.

| Fält | Description | Funktionellt påverkan |
| --- | --- | --- |
| Name | Namnet på leverantörsfakturaraden (i identifieringssyfte). | Detta namn visas som den första kolumnen i alla uppslag som baseras på leverantörsfakturarader. |
| Description | En kort beskrivning av de produkter som faktureras av leverantören på leverantörsfakturaraden. | None |
| Underleverantörskontrakt | Det underleverantörskontrakt som produkterna ursprungligen beställdes på. | När en underleverantör väljs för leverantörsfakturan ärver alla rader på leverantörsfakturan det valet. En leverantörsfaktura kan inte ha leverantörsfakturarader som refererar till olika underleverantörer. |
| Kontraktrad för underleverantör | Den underleverantörsrad som produkterna ursprungligen beställdes på. Den lista över underkontaktrader som kan markeras är begränsad till raderna på det markerade underkontraktet. | När en underleverantörsrad väljs på en leverantörsfakturarad för produkter anges standardvärden för fälten **Projekt**, **Uppgift** och **Produkt** från motsvarande fält på underleverantörsraden. Om den valda underleverantörsraden har värden i fälten **Projekt**, **Uppgift** och **Produkt** kan inte värdena för motsvarande fält på leverantörsfakturaraden skilja sig åt från dessa värden. |
| Transaktionsdatum | Det datum då den faktiska kostnaden för leverantörsfakturaraden registreras i projektet. | None|
| Transaktionsklass | När produkter faktureras ska detta fält ha angetts som **Material**. | Värdet **Material** anger att leverantörens fakturarad används för att registrera fakturabeloppet för material som köpts in. |
| Project | Namnet på det projekt där produkterna som faktureras användes. | detta fält är obligatoriskt och får inte lämnas tomt. |
| Aktivitet | Namnet på den projektuppgift där produkterna som faktureras användes. Detta fält är endast tillgängligt om ett projekt har markerats. Val av projektuppgift är valfritt. | Om detta fält lämnas tomt kan projektledaren matcha leverantörsfakturaraden med den inköpta produkt som används i någon av projektets uppgifter. Om leverantörens fakturarad inte refererar till en underleverantörsrad och det här fältet lämnas tomt, länkas inte den faktiska kostnaden som skapas av leverantörens fakturarad till några ofakturerade försäljningsvärden. Om uppgiftsbaserad fakturering har konfigurerats kanske kostnaderna i detta fall inte kan faktureras till slutkunden. |
| Välj produkt | Ange om produkten som faktureras är en befintlig produkt i katalogen eller en oregistrerad produkt. | Standardvärdet anges från underleverantörsraden när en underleverantörsrad väljs. |
| Produkt | Välj produkten i katalogen. Om produkten är en oregistrerad produkt anger du namnet på produkten. | Detta fält används för att ange standardinköpspriser för befintliga produkter. |
| Kvantitet | Ange kvantiteten material som leverantören fakturerar på fakturaraden. | None |
| Enhetsgrupp | Markera enhetsgruppen för den enhet som kvantiteten som faktureras uttrycks i. | None |
| Enhet | Standardvärdet är basenhet för den valda enhetsgruppen. Du kan ändra det här värdet för att betala i valfri enhet av vald enhetsgrupp. | Kombinationen av värdena **Produkt** och **Enhet** kommer att användas som standard- eller beräknat värde för fältet **Enhetspris** på leverantörsfakturaraden. |
| Enhetspris | Standardenhetspriset använder kombinationen av värdena för **Produkt** och **Enhet** från den projektprislista som är tillämpbar på leverantörsfakturaradens transaktionsdatum. | None |
| Delsumma | Detta skrivskyddade fält beräknas som *Kvantitet* &times; *Enhetspris* om värdena anges i såväl fältet **Kvantitet** som fältet **Enhetspris**. Om ett eller båda dessa fält är tomma kan du ange ett värde i det här fältet. | None |
| Moms | Ange momsbeloppet. | None |
| Totalbelopp | Totalt belopp för leverantörens fakturarad, inklusive moms. Detta fält beräknas som *Delsumma* + *Moms*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
