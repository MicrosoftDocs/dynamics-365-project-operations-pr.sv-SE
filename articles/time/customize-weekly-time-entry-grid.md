---
title: Utöka tidsposter
description: I det här ämnet finns information om hur utvecklare kan utöka tidspostkontrollen.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 190ad9e1f9ced690aee953ed992bf7aa2844c3b3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085439"
---
# <a name="extending-time-entries"></a>Utöka tidsposter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I Dynamics 365 Project Operations ingår en anpassad kontroll för utökad tidspost. Denna kontroll omfattar följande funktioner:

- Ange tid vågrätt över en vecka
- Summor per dag, rad eller vecka
- Kopiera rader eller veckor
- Tidspost med HH:mm eller HH.hh (konverteras automatiskt till HH.hh)
- Importera från tilldelningar, bokningar och avtalade tider

Det går att utöka tidsposter i två områden:
- [Lägga till anpassade tidsposter för egen användning](#add)
- [Anpassa kontroll för tidsposter för en vecka](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Lägga till anpassade tidsposter för egen användning

Tidsposter är en huvudsaklig entitet som används i flera scenarier. Under utgivningscykel 1 i april 2020 introducerades lösningen TESA. TESA tillhandahåller en **inställningsentitet** och en ny säkerhetsroll **Användare av tidsposter**. Även de nya fälten **msdyn_start** och **msdyn_end** , som har en direkt relation till **msdyn_duration** , ingår. Den nya entiteten, säkerhetsrollen och de nya fälten ger en mer enhetlig inställning till tid över flera produkter.


### <a name="time-source-entity"></a>Källentitet för tid
| Fält | Beskrivning | 
|-------|------------|
| Namn  | Namnet på posten Tidskälla som används som urvalsvärde vid skapande av tidsposter. |
| Standardtidskälla [Tidskälla: isdefault] | Som standard kan endast en tidskälla vara markerad som standard. Detta gör att poster som standard tilldelas en tidskälla om ingen har angetts. |
|Typ av tidskälla [Tidskälla: sourcetype] | Källtypen är ett alternativ (Typ av tidspostkälla) som möjliggör associationen av tidskällan till en app. Microsoft förbehåller värden som är större än 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsposter och källentiteten för tid
Varje tidspost associeras till en tidskällpost. Den här posten avgör hur och vilka program som sak behandla tidsposten.

Tidsposter är alltid ett sammanhängande tidsblock med start, slut och varaktighet sammankopplade.

I logiken uppdateras tidsposten automatiskt i följande situationer:

- Om två av de tre följande fälten är tillgängliga beräknas det tredje automatiskt: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Fälten **msdyn_start** och **msdyn_end** är medvetna om tidszonen.
- Tidsposter som skapas med endast **msdyn_date** och **msdyn_duration** angivna startar vid midnatt. Fälten **msdyn_start** och **msdyn_end** uppdateras därefter.

#### <a name="time-entry-types"></a>Typer av tidsposter

Tidsposter har en associerad typ som definierar beteendet för överföringsflödet för det associerade programmet.

|Etikett | Värde|
|-----|-----|
|På rast   |192,355,000|
|Resor | 192,355,001|
|Övertid   | 192,354,320|
|Arbete   | 192,350,000|
|Frånvaro    | 192,350,001|
|Ledighet   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Anpassa kontroll för tidsposter för en vecka
Utvecklare kan lägga till ytterligare fält och uppslag i andra entiteter och implementera anpassade affärsregler för att stödja affärsscenarier.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Lägga till anpassade fält med uppslag för andra entiteter
Du lägger till ett anpassat fält i rutnätet med en tidspost i veckan i tre steg.

1. Lägg till det anpassade fältet i dialogrutan snabbregistrering.
2. Konfigurera rutnätet så att det anpassade fältet visas.
3. Lägg till det anpassade fältet i flödet för att redigera uppgift eller i cellen för att redigera uppgiftsflöde.

Kontrollera att de nya fälten har de valideringar som krävs i rad- eller cellflödet för redigera uppgift. Som en del av det här steget låser du fältet utifrån tidspoststatus.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lägg till det anpassade fältet i dialogrutan snabbregistrering.
Lägg till det anpassade fältet i dialogrutan **Skapa tidspost för snabbregistrering**. När tidsposter sedan läggs till kan ett värde anges genom att välja **Ny**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurera rutnätet så att det anpassade fältet visas.
Du lägger till ett anpassat fält i rutnätet med en tidspost i veckan på ett av två sätt:

  - Anpassa en vy och lägg till ett anpassat fält
  - Skapa en ny anpassad standardtidspost 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Anpassa en vy och lägg till ett anpassat fält

Anpassa vyn **Mina veckovisa tidsposter** och lägg till ett anpassat fält i den. Du kan välja placering och storlek för det anpassade fältet i rutnätet genom att redigera egenskaperna i vyn.

#### <a name="create-a-new-default-custom-time-entry"></a>Skapa en ny anpassad standardtidspost

Den här vyn ska innehålla fälten **Beskrivning** och **Externa kommentarer** förutom de kolumner som du vill ha i rutnätet. 

1. Välj placering, storlek och standardorientering för rutnätet genom att redigera egenskaperna i vyn. 
2. Konfigurera den anpassade kontrollen för vyn så att den är en kontroll för **Rutnät för tidspost**. 
3. Lägg till den här kontrollen i vyn och välj den för webben, telefon och surfplatta. 
4. Konfigurera parametrarna för rutnät för veckotidspost. 
5. Ange fältet **Startdatum** till **msdyn_date** , ange värdet för **varaktighet** till **msdyn_duration** och ange fältet **Status** till **msdyn_entrystatus**. 
6. I standardvyn är fältet **Skrivskyddad statuslista** inställd på **192350002,192350003,192350004**. Fältet **Uppgiftsflöde för radredigering** är inställt på **msdyn_timeentryrowedit**. Fältet **Uppgiftsflöde för cellredigering** är inställt på **msdyn_timeentryedit**. 
7. Du kan anpassa de här fälten om du vill lägga till eller ta bort skrivskyddad status eller om du vill använda olika uppgiftsbaserade miljöer (TBX) för redigering av rader eller celler. De här fälten är nu bundna till ett statiskt värde.


> [!NOTE] 
> Båda alternativen tar bort färdig filtrering på entiteterna **Projekt** och **Projektuppgift** så att alla uppslagsvyer för entiteter visas. Endast relevanta uppslagsvyer visas.

Fastställ lämpligt uppgiftsflöde för det anpassade fältet. Om du har lagt till fältet i rutnätet bör du i så fall gå till uppgiftsflödet för radredigering som används för fält som gäller för hela raden med tidsposter. Om det anpassade fältet har ett unikt värde varje dag, t.ex. ett anpassat fält för **Sluttid** ska det gå vidare i cellen för redigera uppgiftsflöde.

Om du vill lägga till det anpassade fältet i ett uppgiftsflöde drar du elementet **Fält** till rätt plats på sidan och anger sedan fältegenskaperna. Ange egenskapen **Källa** till **Tidspost** och ange egenskapen för **datafältet** till det anpassade fältet. Egenskapen **Fält** anger visningsnamn på sidan TBX. Välj **Tillämpa** om du vill spara ändringarna i fältet och välj sedan **Uppdatera** för att spara ändringarna på sidan.

Om du vill använda en ny anpassad TBX-sida i stället skapar du en ny process. Ange kategorin som **affärsprocessflöde** , ange posten till **tidspost** och ange affärsprocesstypen till **Kör process som uppgiftsflöde**. Under **egenskaper** ska egenskapen **sidnamn** anges som visningsnamn för sidan. Lägg till alla relevanta fält på sidan TBX. Spara och aktivera processen. Uppdatera egenskapen anpassad kontroll för det aktuella uppgiftsflödet till värdet för processens **namn**.

### <a name="add-new-option-set-values"></a>Lägg till nya värden för alternativuppsättning
Om du vill lägga till värden för alternativuppsättning i ett färdigt fält öppnar du redigeringssidan för fältet och under **Typ** väljer du sedan **Redigera** bredvid alternativuppsättningen. Lägg till ett nytt alternativ som har en egen etikett och färg. Om du vill lägga till en ny tidspoststatus heter det färdiga fältet **Poststatus** , inte **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Ange en ny tidspoststatus som skrivskyddad
Om du vill ange en ny tidspoststatus som skrivskyddad lägger du till det nya värdet till egenskapen **Skrivskyddad statuslista**. Den redigerbara delen av rutnätet för tidsposter låses för rader med den nya statusen.
Lägg sedan till affärsregler för att låsa alla fält på TBX-sidorna **Redigera tidspostrad** och **Redigera tidspost**. Du kan komma åt affärsreglerna för de här sidorna genom att öppna affärsprocessflödesredigeraren för sidan och sedan välja **affärsregler**. Du kan lägga till den nya statusen i villkoret i befintliga affärsregler eller lägga till en ny affärsregel för den nya statusen.

### <a name="add-custom-validation-rules"></a>Lägga till anpassade verifieringsregler
Det finns två typer av valideringsregler som du kan lägga till för veckotidspostens rutnätsfunktioner:

- Affärsregler på klientsidan som fungerar i dialogrutorna för snabbskapande och på TBX-sidorna.
- Valideringar av plugin-program på serversidan som gäller alla uppdateringar av tidsposter.

#### <a name="business-rules"></a>Affärsregler
Använd affärsregler för att låsa och låsa upp fält, ange standardvärden i fält och definiera valideringar som endast kräver information från den aktuella tidsposten. Du kan komma åt affärsreglerna för en TBX-sida genom att öppna affärsprocessflödesredigeraren för sidan och sedan välja **affärsregler**. Du kan sedan redigera de befintliga affärsreglerna eller lägga till en ny affärsregel. För ännu mer anpassade valideringar kan du använda en affärsregel för att köra JavaScript.

#### <a name="plug-in-validations"></a>Valideringar av plugin-program
Använd plugin-valideringar för alla valideringar som kräver mer kontext än vad som är tillgängligt i en enskild tidspost eller för alla verifieringar som du vill ska köras på infogade uppdateringar i rutnätet. Slutför valideringen genom att skapa ett eget plugin-program för entiteten **tidspost**.

### <a name="copying-time-entries"></a>Kopiera tidsposter
Använd vyn **Kopiera tidspostkolumner** för att definiera listan över fält som ska kopieras under en tidspost. **Datum** och **Varaktighet** är obligatoriska fält och bör inte tas bort från vyn.
