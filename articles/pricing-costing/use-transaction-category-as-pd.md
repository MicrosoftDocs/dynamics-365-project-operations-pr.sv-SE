---
title: Använd transaktionskategori som prissättningsdimension
description: I det här ämnet finns information om hur du använder fältet Transaktionskategori som prissättningsdimension.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a7fe9bfc87db992252f8ef3f0f688e7426cafebb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591150"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Använd transaktionskategori som prissättningsdimension


_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


Det här ämnet förklarar hur du använder fältet **Transaktionskategori** som prissättningsdimension. 

## <a name="prerequisites"></a>Förutsättningar
Innan du slutför procedurerna i detta ämne måste du ha en ny lösning för prissättningsdimension för din organisation. Om du inte redan har skapat en sådan, se [Skapa anpassade fält och entiteter som prissättningsdimensioner](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Lägg till fältet Transaktionskategori i formulär och vyer
Om du vill göra fältet **Transaktionskategori** synligt i lösningen för prissättningsdimension måste du lägga till fältet i alla formulär och vyer som en entitet.

I följande tabell visas alla färdiga formulär och vyer efter entitet. Du kommer också att behöva lägga till det nya fältet i alla eventuella ytterligare formulär eller vyer i dina anpassade entiteter.

|  Entitet        | Formulär     |Vyer        |
| ------------------------------|---------------------------------|----------------------------------|
|  Pris för roll| Information |- Aktiva resurskategoripriser<br> - Associerad med för resurskategoripris |
|  Pålägg för rollpris| Information|- Aktivt pålägg för rollpris<br>- Associerat med pålägg för rollpris |
|  Information om offertrad|- Projektinformation<br>- Snabbregistrera projekt| - Information om aktiv offertrad<br>- Information om kombinerad offertrad<br>- Associerat med information om offertrad |
|  Information om projektkontraktrad|- Projektinformation<br>- Snabbregistrera projekt|- Information om kombinerad kontraktrads<br>- Aktiv kontraktradsinformation<br>- Associerat med kontraktradsinformation |
|  Projektuppgift|- Information<br>- Nytt formulär| &nbsp; |
|  Projektgruppmedlem|- Information<br>- Nytt formulär|- Aktiva projektgruppmedlemmar<br>- Projektets gruppmedlemmar<br>- Associerat med projektgruppmedlemmar |
|  Tidspost|- Information<br>- Skapa tidspost|- Mina tidsposter efter datum<br>- Mina tidsposter för den här veckan<br>- Tidsposter för godkännande|
|  Journalrad|- Information<br>- Snabbregistrering|- Aktiva journalrader<br>- Associerat med journalrad|
|  Information om fakturarad|- Information<br>- Snabbregistrering|- Information om aktiv fakturarad<br>- Debiterbara fakturatransaktioner<br>- Kostnadsfria fakturatransaktioner<br>- Associerat med information om fakturarad <br>- Icke-debiterbar fakturatransaktion|
|  Faktisk|- Information<br>- Aktiva faktiska värden| Associerat med faktiska värden |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Ställ in fältet Transaktionskategori som prissättningsdimension

1. Gå till **Inställningar** > **Parametrar**. 
2. På sidan **Parametrar**, på fliken **Beloppsbaserade prissättningsdimensioner**, bekräftar du att rutnätet visar posterna i entiteten **Prissättningsdimensioner**.
3. Lägg till **Transaktionskategori** i den här listan och ange fälten **Gäller för kostnad** och **Gäller för försäljning** som **Ja**.
4. I fältet **Dimensionstyp** väljer du **Beloppsbaserad** och väljer sedan prioriteten för **Transaktionskategori** som gäller för kostnad och försäljning.


[!INCLUDE[footer-include](../includes/footer-banner.md)]