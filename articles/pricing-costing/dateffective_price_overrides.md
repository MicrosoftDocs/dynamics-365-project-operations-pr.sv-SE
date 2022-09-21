---
title: Datumspecifika prisändringar
description: I den här artikeln finns information om hur du konfigurerar åsidosättningar av specifika priser i prislistan.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445980"
---
# <a name="date-effective-price-overrides"></a>Datumspecifika prisändringar 

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

*Datumspecifika prisändringar* är ett sätt att åsidosätta eller ändra specifika priser i prislistan. Du har till exempel en standardprislista som gäller från 1 januari 2022 till 31 december 2022. Prislistan innehåller priser för många roller. Priset för rollen **Nätverkstekniker** är 100 amerikanska dollar (USD) i timmen. När en nätverkstekniker loggar tid mellan 1 januari 2022 och 31 december 2022 prissätts tiden till 100 USD. Den 1 oktober 2022 måste du justera priset för *enbart* rollen **Nätverkstekniker**, från 100 USD per timme till 110 USD per timme. Med funktionen **Datumspecifika prisändringar** kan du konfigurera denna ändring som en ersättning av raden för det specifika rollpriset. Därför behöver du inte kopiera hela prislistan och ändra priset för bara den raden.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datumspecifika prisändringar för arbetsprissättning

Processen med att konfigurera prisändringar på specifika datum för arbetstid i ett projekt består av två grundläggande steg.

1. Aktivera funktionen **Datumspecifika prisändringar**.
1. Konfigurera en datumspecifik prisändring.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Aktivera funktionen Datumspecifika prisändringar

> [!NOTE]
> När funktionen **Datumspecifika prisändringar** har aktiverats kan den inte inaktiveras.

Följ stegen nedan om du vill aktivera funktionen **Datumspecifika prisändringar**.

1. Gå till **Inställningar** \> **Parametrar**.
1. Öppna posten **Parametrar**.
1. I åtgärdsfönstret under fliken **Funktionskontroll** väljer du **Aktivera datumspecifika prisändringar**.
1. Klicka på **OK** i bekräftelsedialogrutan.
1. Uppdatera webbläsaren efter en stund. Funktioner för datumspecifika prisändringar ska nu vara tillgängliga. Du vet att funktionerna har aktiverats om **Aktivera datumspecifika prisändringar** inte längre syns i åtgärdsfönstret.

### <a name="set-up-a-date-effective-price-override"></a>Konfigurera en datumspecifik prisändring

Datumspecifika prisändringar kan konfigureras för prislistorna **Kostnad**, **Försäljning** och **Inköp**.

> [!NOTE]
>Beteendet för **Datumspecifika prisändringar** har för närvarande följande begränsningar:
>
> - Endast rollpriser och rollprispålägg har stöd för funktionen **Datumspecifika prisändringar** i Project Operations.
> - När du kopierar en prislista med hjälp av åtgärden **Kopiera** på sidan **Information om prislista** och när du skapar en projektprislista från en standardprislista eller en anpassad prislista under projektskapandet, kopierar **inte** datumspecifika prisändringar från källprislistan.

Följ stegen nedan om du vill konfigurera en datumspecifik prisändring för ett rollpris eller ett rollprispålägg.

1. Öppna sidan för den prislista som du vill konfigurera den datumspecifika prisändringen för.
1. Välj fliken **Rollpriser**. På den här fliken visas alla **rollprisposter** i prislistan.
1. Välj den **rollprispost** som du vill konfigurera en ny datumspecifik prisändring för och dubbelklicka sedan på **Rollpris** för att öppna sidan **Information om rollpris**.
1. Välj fliken **Datumspecifika ändringar**. I rutnätet på den här fliken visas alla datumspecifika prisändringar för den valda **rollprisposten**.
1. I verktygsfältet ovanför rutnätet väljer du **Ny rollprisändring**. Reglaget **Ny rollprisändring** öppnas.
1. Ange startdatum, enhet och det nya priset efter prisändringen. Välj sedan **Spara** och stäng formuläret.

> [!NOTE]
> - En datumspecifik prisändring för ett rollrpis eller ett rollprispålägg gäller samma kombination av prisdimensionsvärden som finns på den överordnade raden **Rollpris** eller **Rollprispålägg**.
> - Datumet som väljs i fältet **Gäller från** ska vara inom de giltiga datumen för den överordnade prislistan. Prisändringen träder i kraft det datum som väljs i fältet **Gäller från** och gäller till slutdatumet för den överordnade prislistan. Om du konfigurerar en annan datumspecifik prisändring för samma rollpris träder den första ändringen i kraft det datum som väljs i fältet **Gäller från** och gäller tills den andra ändringen börjar.

## <a name="examples"></a>Exempel

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exempel 1: Bestämma giltighetsdatum för ett rollpris som har rollprisändringar

Följande exempel visar hur giltighetsdatum bestäms för ett visst rollpris som rollprisändringar har konfigurerats för.

**Prislista A: 1 januari till och med 30 juni**

*Rollpris*

| Rollpris | Enhet | Pris | Effekt på prissättning för inkommande transaktioner |
|---|---|---|---|
| Nätverkstekniker | timme | 100 | Priset används för alla transaktioner där transaktionsdatumet är mellan 1 januari och 14 mars. |

*Rollprisändring*

| Gäller från | Enhet | Pris | Effekt på prissättning för inkommande transaktioner |
|---|---|---|---|
| Mars 15 | timme | 110 | Priset används för alla transaktioner där transaktionsdatumet är mellan 15 mars och 30 mars. |
| April 1 | timme | 120 | Priset används för alla transaktioner där transaktionsdatumet är mellan 1 april och 30 juni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exempel 2: Bestämma giltighetsdatum för ett rollprispålägg som har rollprispåläggsändringar

Följande exempel visar hur giltighetsdatum bestäms för ett visst rollprispålägg som rollprispåläggsändringar har konfigurerats för.

**Prislista A: 1 januari till och med 30 juni**

*Rollpris*

| Rollpris | Arbetstider | Enhet | Pris | Effekt på prissättning för inkommande transaktioner |
|---|---|---|---|---|
| Nätverkstekniker | Vanlig | timme | 100 | Priset används för alla transaktioner där transaktionsdatumet är mellan 1 januari och 14 mars. |

*Rollprispålägg*

| Organisationsenhet | Arbetstider | Pålägg % |
|---|---|---|
| Contoso US | Övertid | 10 % |

*Ändring av rollprispålägg*

| Gäller från | Pris | Effekt på prissättning för inkommande transaktioner |
|---|---|---|
| Mars 15 | 20 % | Påläggsprocenten används för alla transaktioner där transaktionsdatumet är mellan 15 mars och 30 mars. |
| April 1 | 25 % | Pålägget används för alla transaktioner där transaktionsdatumet är mellan 1 april och 30 juni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
