---
title: Använd en bokningsbar resurs som prissättningsdimension
description: Denna artikel har information om hur du använder en bokningsbar resurs som prissättningsdimension.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914838"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Använd en bokningsbar resurs som prissättningsdimension

 _**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_ 

Denna artikel har information om hur du använder en bokningsbar resurs som prissättningsdimension. Om din prissättningsstrategi har ställts in så att varje bokningsbar resurs måste ha ett visst pris eller en viss kostnadssats använder du en bokningsbar resurs som prissättningsdimension.

## <a name="prerequisites"></a>Förutsättningar
Innan du slutför procedurerna i den här artikeln måste du ha en ny prissättningslösning för organisationen. Om du inte redan har skapat en sådan, se [Skapa anpassade fält och entiteter](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Lägg till fältet Bokningsbara resurser i formulär och vyer
Om du vill göra fältet **Bokningsbar resurs** synligt i lösningen för prissättningsdimension måste du lägga till fältet i alla formulär och vyer som en entitet.

I följande tabell visas alla färdiga formulär och vyer efter entitet. Du kommer också att behöva lägga till det nya fältet i alla eventuella ytterligare formulär eller vyer i dina anpassade entiteter.

|   Entitet        | Formulär   |Vyer        |
| ------------------------------|---------------------------------|----------------------------------|
|  Pris för roll| Information | - Aktiva resurskategoripriser<br> - Associerad med för resurskategoripris |
|  Pålägg för rollpris| Information| - Aktivt pålägg för rollpris<br>- Associerat med pålägg för rollpris |
|  Information om offertrad| - Projektinformation<br>- Snabbregistrera projekt| - Information om aktiv offertrad<br>- Information om kombinerad offertrad<br>- Associerat med information om offertrad |
|  Information om projektkontraktrad| - Projektinformation<br>- Snabbregistrera projekt| - Information om kombinerad kontraktrads<br>- Aktiv kontraktradsinformation<br>- Associerat med kontraktradsinformation |
|  Projektuppgift| - Information<br>- Nytt formulär| &nbsp; |
|  Projektgruppmedlem| - Information<br>- Nytt formulär| - Aktiva projektgruppmedlemmar<br>- Projektets gruppmedlemmar<br>- Associerade projektgruppmedlemmar |
|  Tidspost| - Information<br>- Skapa tidspost| - Mina tidsposter efter datum<br>- Mina tidsposter för den här veckan<br>- Tidsposter för godkännande|
|  Journalrad| - Information<br>- Snabbregistrering| - Aktiva journalrader<br>- Associerat med journalrad |
|  Information om fakturarad| - Information<br>- Snabbregistrering| - Information om aktiv fakturarad<br>- Debiterbara fakturatransaktioner<br>- Kostnadsfria fakturatransaktioner<br>- Associerat med information om fakturarad <br>- Icke-debiterbar fakturatransaktion|
|  Faktisk| - Information<br>- Aktiva faktiska värden| Associerat med faktiska värden |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Ställ in en bokningsbar resurs som prissättningsdimension
Följ dessa steg för att ställa in en bokningsbar resurs som prissättningsdimension:

1. Gå till **Inställningar** > **Parametrar**. 
2. På sidan **Parameter**, på fliken **Beloppsbaserade prissättningsdimensioner**, bekräftar du att rutnätet visar posterna i entiteten **Prissättningsdimensioner**. 
2. Lägg till **Bokningsbar resurs** i den här listan över prisdimensioner som **msdyn_bookableresource**. 
3. I **Gäller för kostnad** och **Gäller för försäljning** väljer du ett värde.
4. I fältet **Dimensionstyp** väljer du **Beloppsbaserad**. 
5. Välj kostnads- och försäljningsprioritet för den bokningsbara resursen. Vanligtvis har en bokningsbar resurs högsta prioritet när den ingår som en prissättningsdimension. Ange prioriteten som **1** (eller **0** beroende på hur du räknar prioriteten) för att säkerställa detta beteende.

## <a name="set-up-pricing-dimension-field-names"></a>Ange fältnamn för prissättningsdimension

När fältnamnet för en prissättningsdimension i tabellen **Rollpris** skiljer sig åt från fältnamnet i någon av de andra entiteterna där standardpriset används, måste posten för prissättningsdimension känna till de olika namnen.  

För en bokningsbar resurs har entiteten **Projektgruppmedlemmar** ett något annorlunda fältnamn jämfört med det som anges i entiteten **Rollpris**: 

 - Entiteten **Projektgruppmedlemmar** = **msdyn_bookableresourceid**
 - Entiteten **Rollpris** = **msdyn_bookableresource**

Posten för prissättningsdimension för **msydn_bookableresource** måste känna till denna skillnad.

1. Dubbelklicka på raden i rutnätet **Prissättningsdimensioner** för att öppna dimensionssidan för **msdyn_bookableresource**.
2. På fliken **Relaterat** på dimenssionssidan väljer du **Fältnamn för prissättningsdimension**.

  ![Fliken Fältnamn för prissättningsdimensioner.](media/PD-fieldname.png)

3. I den associerade vyn som öppnas väljer du **Lägg till nytt fältnamn för prissättningsdimension**.

  ![Lägg till nya fältnamn för prissättningsdimensioner.](media/Add-NewPD-fieldname.png)

  Då öppnas sidan **nya prissättningsdimensioner** för **msdyn_bookableresource**. 

4. På sidan **Fältnamn för ny prissättningsdimension** lägger du till **msdyn_projectteam** i **Logiskt entitetsnamn**.
5. Lägg till **msdyn_bookableresourceid** i **Fältnamn**.

 ![Formulär för fältnamn för prissättningsdimensioner.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]