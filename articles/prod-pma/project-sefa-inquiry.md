---
title: Tidsplan för utgifter för en förfrågan om federala beviljanden
description: I det här ämnet finns information om tidsplanen för utgifter för förfrågan om federala beviljanden.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: b88c97f3dcb1020ccf17788256990485580f6964
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684480"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Tidsplan för utgifter för en förfrågan om federala beviljanden

[!include [banner](../includes/banner.md)]

Enligt Office of Management and Budget Circular A-133, organ som erhåller federala fonder underkastade granskningskrav, vilka även kallas enstaka revisioner. Granskningsprocessen används för att rapportera om de federala stödens intäkter och utgifter på återkommande basis. En del av rapporten för en enskild granskning inkluderar tidsplanen för utgifter för federala beviljanden (SEFA).

Tidsplanen för utgifter för en förfrågan om federala beviljanden innehåller titel och nummer i Catalog of Federal Domestic Assistance (CFDA), anslagsnummer, året för anslaget, namnet på det federala organ som tillhandahåller anslaget samt namnet på den direkta entiteten. Förfrågan gäller en särskild period. Den perioden är vanligtvis samma som bokslutsperioden, som är ett räkenskapsår.

Förfrågan innehåller anslag med projektionsdatum i det valda datumintervallet. Kolumnen **Tilldelande organ** för förfrågan visar anslagets kund eller, när det gäller ett direkt anslag, det tilldelande organet. För ett direkt anslag visar kolumnen **Direkt organ** anslagets kund. Om anslaget inte är ett direkt anslag är kolumnen **Direkt organ** tom.

## <a name="set-up-the-cfda-clusters"></a>Konfigurera CFDA-kluster

Du måste konfigurera de CFDA-kluster som kan kopplas till CFDA-nummer i tidsplanen för utgifter för en förfrågan om federala beviljanden.

1. Gå till **Projektledning och redovisning \> Konfiguration \> Anslag \> Katalog med kluster av federalt inhemskt stöd**.
2. Välj **Nytt** för att skapa ett CFDA-kluster.
3. Ange klusternamnet.
4. Välj **Spara** för att spara dina ändringar.

## <a name="set-up-cfda-numbers"></a>Ställ in CFDA-nummer

Du måste konfigurera de CFDA-nummer som kan läggas till i anslag och inkluderas i tidsplanen för utgifter för en förfrågan om federala beviljanden.

1. Gå till **Projektledning och redovisning \> Konfiguration \> Anslag \> Katalog med nummer för federalt inhemskt stöd**.
2. Välj **Nytt** för att skapa ett CFDA-nummer.
3. I kolumnen **Nummer** anger du CFDA-numret.
4. Tryck på tangenten **TAB**.
5. I kolumnen **Beskrivning** anger du CFDA-titeln.
6. Tryck på tangenten **TAB**.
7. Valfritt: I fältet **Programkluster** lägger du till lämpligt CFDA-kluster.
8. Välj **Spara** för att spara dina ändringar.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Ställ in anslag som ska rapporteras för tidsplanen för utgifter för en förfrågan om federala beviljanden

1. Gå till **Projektledning och redovisning \> Anslag \> Anslag** och välj ett befintligt anslag.
2. Under snabbfliken **Konfiguration**, i fältet **Katalog med federalt inhemskt stöd**, tilldelar du CFDA-numret. CFDA-numret för anslaget avgör CFDA-klustret för rapportering.
3. Under snabbfliken **Kontaktinformation** anger du information om tilldelaren genom att följa dessa steg:

    1. I fältet **Anslagets kund** anger du den kund som är ansvarig för anslaget. För ett befintligt anslag kan den här informationen redan finnas.
    2. Ange om anslagskunden är finansiären. Om anslagskunden är finansiären lämnar du kryssrutan **Direkt** omarkerad. Om en annan kund är finansiär och anslagskunden ansvarar för utgifterna och spårning av pengarna, markerar du kryssrutan **Direkt**.

4. Om du markerade kryssrutan **Direkt** i föregående steg anger du, i fältet **Tilldelande organ**, den kund som tillhandahöll anslaget. Det tilldelande organet och anslagskunden kan inte vara samma kund.

Här är ett exempel på ett direkt anslag:

Den federala regeringen finansierade ett infrastrukturprojekt för en delstat. Den federala regeringen gav delstaten pengar att spendera. I det här fallet är den federala regeringen det tilldelande organet och delstaten är anslagskunden.

> [!NOTE] 
> När du först aktiverar funktionen anges de första CFDA-numren med hjälp av de befintliga numren på anslagen.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Exkludera anslag från SEFA-rapportering utifrån anslagstypen

1. Gå till **Projektledning och redovisning \> Konfiguration \> Anslag \> Anslagstyper**.
2. Under snabbfliken **Standardinformation** markerar du kryssrutan **Exkludera från tidsplan för utgifter för federala beviljanden**.
3. Välj **Spara** för att spara dina ändringar.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Kör Tidsplan för utgifter för en förfrågan om federala beviljanden

1. Gå till **Projektledning och redovisning \> Förfrågningar och rapporter \> Anslagsförfrågan \> Tidsplan för utgifter för federala beviljanden**.
2. I avsnittet **Parametrar** följer du dessa steg:

    1. I fältet **Datumintervall** väljer du koden för datumintervallet. Du kan också definiera datumintervallet i fälten **Från datum** och **Till datum**.
    2. Valfritt: Om du endast vill ta med fakturerade transaktioner som intäkt i förfrågan ställer du in alternativet **Inkludera endast fakturerade intäkter** på **Ja**.

## <a name="columns"></a>Kolumner

I tidsplanen för utgifter för en förfrågan om federala beviljanden finns följande kolumner:

- Katalog med namn på kluster av federalt inhemskt stöd
- Tilldelande organ
- Direkt organ
- Namn på anslag
- Anslags-ID
- ID för anslagsansökan
- Katalog med federalt inhemskt stöd
- Kvitton
- Utgifter


[!INCLUDE[footer-include](../includes/footer-banner.md)]