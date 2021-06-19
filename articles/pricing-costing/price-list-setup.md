---
title: Konfigurera prislistor
description: I det här ämnet finns information om hur du konfigurerar prislistor för kostnad och försäljning.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 118c2bd6b59b509e5628ac00fc1607809458853b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005048"
---
# <a name="set-up-price-lists"></a>Konfigurera prislistor

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Prislistor i Dynamics 365 Project Operations representerar en katalog med priser. Priserna avser kostnad, försäljning och fakturering. Beroende på om prislistan avser kostnad eller försäljning och fakturering kan prislistans sammanhang vara **Försäljning** eller **Kostnad**.

Följande tillägg är specifika för Project Operations och tillämpas på prislistor från Dynamics 365 Sales.

- **Sammanhang**: Det här fältet värdena som stöds för **Kostnad** och **Försäljning**. Värdet **Inköp** stöds inte. Ställ in sammanhanget till **Kostnad** om du vill göra en kostnadsprislista eller ställ in sammanhanget till **Försäljning** för att göra en försäljningsprislista. Kostnadsprislistor löser priset för kostnadstypen för poster med uppskattade och faktiska värden. Försäljningsprislistor löser priset på poster med uppskattade och faktiska värden av ej fakturerade och fakturerade försäljningstyper.
- **Tidsenhet**: Det här är standardenheten för tid för vilken priset har konfigurerats i den aktuella tabellen **Rollpris** för prislistan.
- **Entitet i prislista**: Det här dolda fältet är av Project Operations för att differentiera prislistor som är offert- eller kontraktspecifika och som är standard och globalt tillämpliga.

## <a name="price-list-header"></a>Rubrik på prislista

Följande tabell innehåller fält under fliken **Allmänt** i en prislista som är unika för Projekt Operations eller som skiljer sig betydligt från prislistor i Sales.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| Namn | Fliken **Allmänt** och formulären **Snabbskapa** | Prislistans identitet. | Prislistan visas med det här värdet på alla listsidor och listrutealternativ.|
| Sammanhang | Fliken **Allmänt** och formulären **Snabbskapa** | Fältet kan anges till **Kostnad** eller **Försäljning**. | En prislista som är inställd på **Kostnad** används för att slå upp priset för kostnadsuppskattningar och faktiska kostnadsvärden. En prislista som är inställd på **Försäljning** används för att slå upp priset för försäljningsuppskattningar och faktiska försäljningsvärden. Endast prislistor som har sammanhanget inställt på **Försäljning** kan kopplas till projektprislistor för kunder, projektofferter och projektkontrakt. |
| Startdatum | Fliken **Allmänt** och formulären **Snabbskapa** | Startdatum för perioden som prislistan gäller. | Med fältet **Slutdatum** används det här fältet för att avgöra vilken prislista som gäller för en viss rad för uppskattning eller faktiska värden. |
| Slutdatum | Fliken **Allmänt** och formulären **Snabbskapa** | Slutdatum för perioden som prislistan gäller. | Med fältet **Startdatum** används det här fältet för att avgöra vilken prislista som gäller för en viss rad för uppskattning eller faktiska värden. |
| Valuta | Fliken **Allmänt** och formulären **Snabbskapa** | Fältet används för att standardisera valutan för varje rad för roll, kategori eller prislistepost som rör prislistan. | I prislistor som är inställda på **Försäljning** går det inte att skapa roller, kategorier eller prislisteposter i någon annan valuta än denna valuta. I prislistor som är inställda på **Kostnad** kan du skapa en rollprisrad i valfri valuta. Den valuta som definieras här används som standard. Användarinställningarna som tillhör rollpriser kan åsidosätta det här värdet så att arbetskraftskostnad aktiveras i valfri valuta. Kategorikostnad och prislisteposters kostnad kan endast konfigureras i den valuta som definieras här. |
| Tidsenhet | Fliken **Allmänt** och formulären **Snabbskapa** | Fältet används för att standardisera tidsenheten för varje rollrad som rör prislistan. | Det här fältvärdet används endast på relaterade rollprisinställningar. I prislistor som är inställda på **Kostnad** och **Försäljning** kan du skapa en rollprisrad i valfri tidsenhet. Den tidsenhet som definieras här används som standard. Användarinställningarna som tillhör rollpriser kan åsidosätta det här värdet så att arbetskraftskostnad och fakturakostnad aktiveras i valfri tidsenhet. |
| Beskrivning | Fliken **Allmänt** och formulären **Snabbskapa** | Det här textfältet gör att du kan tillhandahålla en flerradig beskrivning av prislistan. | Det här fältet visas i **associerade** vyer för prislistan i olika entiteter som har relaterade prislistor. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]