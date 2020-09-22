---
title: Använd transaktionskategori som prissättningsdimension
description: I det här ämnet finns information om hur du använder en transaktionskategori som prissättningsdimension.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756286"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Använd transaktionskategori som prissättningsdimension
Det här ämnet visar hur du använder en transaktionskategori som prissättningsdimension. Innan du börjar måste du, om du inte redan har skapat en dimensionslösning för prissättning, skapa en ny. Om du redan har en dimensionslösning för prissättning kan du göra ändringarna i den lösningen. Om du inte har skapat en ny dimensionslösning för prissättning för organisationen ska du slutföra procedurerna i ämnet [skapa anpassade fält och entiteter](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Lägg till transaktionskategori i formulär och vyer
Om du vill att transaktionskategori ska visas i användargränssnittet i dimensionslösningen för prissättning måste du gå igenom alla formulären och vyerna för de huvudsakliga enheterna och lägga till dessa fält i formulären och vyerna för dessa entiteter.
Följande tabell är en fullständig lista över de formulär och vyer som inte ingår i rutan efter entitet som behöver uppdateras med de nya fälten. Om det finns ytterligare vyer eller formulär i anpassningarna i dessa entiteter kan du lägga till de nya fälten i dem.

|  Entitet        | Formulär     |Vyer        |
| ------------------------------|---------------------------------|----------------------------------|
|  Pris för roll|• Information |• Aktiva resurskategoripriser<br> • Associerad vy för resurskategoripris|
|  Pålägg för rollpris|• Information|• Aktivt pålägg för rollpris<br>• Associerad vy för pålägg för rollpris|
|  Information om offertrad|• Projektinformation<br>• Snabbregistrera projekt|• Aktiv information om offertrad<br>• Kombinerad information om offertrad<br>• Associerad vy för information om offertrad|
|  Information om projektkontraktrad|• Projektinformation<br>• Snabbregistrera projekt|• Kombinerad kontraktradsinformation<br>• Aktiv kontraktradsinformation<br>• Associerad vy för kontraktradsinformation|
|  Projektteammedlem|• Information<br>• Nytt formulär|• Aktiva projektteammedlemmar<br>• Projektteammedlemmar<br>• Associerad vy för projektteammedlemmar|
|  Tidspost|• Information<br>• Skapa tidspost|• Mina tidsposter efter datum<br>• Mina tidsposter för den här veckan<br>• Tidsposter för godkännande.|
|  Journalrad|• Information<br>• Snabbregistrering|• Aktiva journalrader<br>• Associerad vy för journalrad|
|  Information om fakturarad|• Information<br>• Snabbregistrering|• Information om aktiv fakturarad<br>• Debiterbara fakturatransaktioner<br>• Kostnadsfria fakturatransaktioner<br>• Associerad vy för information om fakturarad<br>• Icke debiterbar fakturatransaktion|
|  Faktiskt|• Information<br>• Aktiva faktiska värden|• Associerad vy för faktiska värden|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Ställ in transaktionskategori som prissättningsdimension

1. I webbgränssnittet, gå till **Project Service** > **inställningar** > **parametrar**. 
2. På sidan **parametrar** på fliken **Beloppsbaserade prissättningsdimensioner** kan du notera att i rutnätet på fliken visas posterna i entiteten **prissättningsdimensioner**.
3. Lägg till **transaktionskategori** i den här listan och ange värdet **Gäller för kostnad** och **Gäller för försäljning** till **Ja**.
4. I fältet **Dimensionstyp** väljer du **Beloppsbaserad** och väljer sedan prioriteten för **transaktionskategori** som gäller för kostnad och försäljning.
