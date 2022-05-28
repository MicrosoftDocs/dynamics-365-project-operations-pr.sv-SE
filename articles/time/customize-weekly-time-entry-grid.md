---
title: Utöka tidsposter
description: I det här ämnet finns information om hur utvecklare kan utöka tidspostkontrollen.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583008"
---
# <a name="extending-time-entries"></a>Utöka tidsposter

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations innehåller en anpassad kontroll för längre tidsinmatning. Denna kontroll omfattar följande funktioner:

- Ange tid vågrätt över en vecka
- Summor per dag, rad eller vecka
- Kopiera rader eller veckor
- Tidspost med HH:mm eller HH.hh (konverteras automatiskt till HH.hh)
- Importera från tilldelningar, bokningar och avtalade tider

Det går att utöka tidsposter i två områden:
- [Lägga till anpassade tidsposter för egen användning](#add)
- [Anpassa kontroll för tidsposter för en vecka](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Lägga till anpassade tidsposter för egen användning

Tidsposter är en huvudsaklig entitet som används i flera scenarier. Under utgivningscykel 1 i april 2020 introducerades lösningen TESA. TESA tillhandahåller en **inställningsentitet** och en ny säkerhetsroll **Användare av tidsposter**. Även de nya fälten **msdyn_start** och **msdyn_end**, som har en direkt relation till **msdyn_duration**, ingår. Den nya entiteten, säkerhetsrollen och de nya fälten ger en mer enhetlig inställning till tid över flera produkter.


### <a name="time-source-entity"></a>Källentitet för tid
| Fält | Beskrivning | 
|-------|------------|
| Namn  | Namnet på posten Tidskälla som används som urvalsvärde vid skapande av tidsposter. |
| Standardtidskälla [Tidskälla: isdefault] | Som standard kan endast en tidskälla vara markerad som standard. Detta gör att poster som standard tilldelas en tidskälla om ingen har angetts. |
|Typ av tidskälla [Tidskälla: sourcetype] | Källtypen är ett alternativ (Typ av tidspostkälla) som möjliggör associationen av tidskällan till en app. Microsoft förbehåller värden som är större än 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsposter och källentiteten för tid
Varje tidspost associeras till en tidskällpost. Denna post avgör vilka program som ska bearbeta tidsposten och hur.

Tidsposter är alltid ett sammanhängande tidsblock med start, slut och varaktighet sammankopplade.

I logiken uppdateras tidsposten automatiskt i följande situationer:

- Om två av de tre följande fälten är tillgängliga beräknas det tredje automatiskt: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Fälten **msdyn_start** och **msdyn_end** är tidszonsmedvetna.
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

1. Lägg till det anpassade fältet i dialogrutan **Snabbregistrering**.
2. Konfigurera rutnätet så att det anpassade fältet visas.
3. Lägg till det anpassade fältet på sidan **Radredigering** eller **Tidspostredigering**.

Se till att det nya fältet har de valideringar som krävs på sidan **Radredigering** eller **Tidspostredigering**. Som en del av den här uppgiften låser du fältet utifrån tidspoststatusen.

När du lägger till ett anpassat fält i rutnätet **Tidspost** och sedan skapar tidsposter direkt i rutnätet, anges det anpassade fältet för dessa poster automatiskt så att det matchar raden. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lägg till det anpassade fältet i dialogrutan Snabbregistrering
Lägg till det anpassade fältet i idalogrutan **Snabbregistrering: Skapa tidspost**. Användarna kan sedan ange ett värde när de lägger till en tidspost genom att välja **Ny**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurera rutnätet så att det anpassade fältet visas.
Du lägger till ett anpassat fält i rutnätet **Veckovis tidspost** på ett av två sätt:

- Anpassa vyn **Mina veckovisa tidsposter** och lägg till ett anpassat fält i den. Du kan ange placering och storlek för det anpassade fältet i rutnätet genom att redigera egenskaperna i vyn.
- Skapa en ny anpassad vy för anpassad tidspost och ange den som standardvy. Den här vyn ska innehålla fälten **Beskrivning** och **Externa kommentarer**, förutom de kolumner som du vill inkludera i rutnätet. Du kan ange placering, storlek och standardorienteringsorder för rutnätet genom att redigera egenskaperna i vyn. Konfigurera sedan den anpassade kontrollen för vyn så att den är en kontroll för **rutnät för tidspost**. Lägg till kontrollen i vyn och välj den för **Webb**, **Telefon** och **Surfplatta**. Konfigurera sedan parametrarna för rutnätet för **Veckotidspost**. Ange fältet **Startdatum** som **msdyn\_date**, ange fältet **Tid** som **msdyn\_duration**, och ange fältet **Status** som **msdyn\_entrystatus**. Fältet **Skrivskyddad statuslista** är inställt på **192350002 (godkänt)**, **192350003 (skickat)** eller **192350004 (återkallelse begärd)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Lägg till det anpassade fältet på lämplig redigeringssida
Sidorna som används för att redigera en tidspost eller en rad med tidsposter finns under **Formulär**. Knappen **Redigera post** i rutnätet öppnar sidan **Redigera post**, och knappen **Redigera rad** öppnar sidan **Radredigering**. Du kan redigera sidorna så att de innehåller anpassade fält.

Båda alternativen tar bort färdig filtrering på entiteterna **projekt** och **projektuppgift** så att alla uppslagsvyer för entiteter visas. Endast relevanta uppslagsvyer visas.

Du måste fastställa lämplig sida för det anpassade fältet. Om du har lagt till fältet i rutnätet bör det med största sannolikhet visas på sidan **Radredigering** som används för fält som tillämpas på hela raden med tidsposter. Om det anpassade fältet har ett unikt värde på raden varje dag (om det till exempel är ett anpassat fält för sluttiden) bör det hamna på sidan **Tidspostredigering**.

Om du vill lägga till det anpassade fältet på en sida drar du ett element av typen **Fält** till rätt plats på sidan och anger sedan egenskaperna.

### <a name="add-new-option-set-values"></a>Lägg till nya värden för alternativuppsättning
Följ stegen nedan om du vill lägga till alternativuppsättningsvärden i ett färdigt fält.

1. Öppna redigeringssidan för fältet innan du under **Typ** väljer **Redigera** bredvid alternativuppsättningen.
2. Lägg till ett nytt alternativ som har en egen etikett och färg. Om du vill lägga till en ny tidspoststatus heter det färdiga fältet **Poststatus**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Ange en ny tidspoststatus som skrivskyddad
Om du vill ange en ny tidspoststatus som skrivskyddad lägger du till det nya värdet till egenskapen **Skrivskyddad statuslista**. Se till att lägga till numret, inte etiketten. Den redigerbara delen av rutnätet för tidsposter låses nu för rader med den nya statusen. Om du vill ställa in egenskapen **Skrivskyddad statuslista** på olika sätt för olika **Tidspost**-vyer, lägg då till rutnätet **Tidspost** i avsnittet **Anpassade kontroller** för en vy, och konfigurera sedan parametrarna efter behov.

Lägg sedan till affärsregler för att låsa alla fält på sidorna **Radredigering** och **Redigera tidspost**. Du kan komma åt affärsreglerna för dessa sidorn genom att öppna formulärsredigeraren för respektive sida och sedan välja **Affärsregler**. Du kan lägga till den nya statusen i villkoret i befintliga affärsregler eller lägga till en ny affärsregel för den nya statusen.

### <a name="add-custom-validation-rules"></a>Lägga till anpassade verifieringsregler
Du kan lägga till två typer av valideringsregler för rutnätsupplevelsen **Veckovis tidspost**:

- Affärsregler på klientsidan som fungerar på sidor
- Valideringar av plugin-program på serversidan som gäller alla uppdateringar av tidsposter

#### <a name="client-side-business-rules"></a>Affärsregler på klientsidan
Använd affärsregler för att låsa och låsa upp fält, ange standardvärden i fält och definiera valideringar som endast kräver information från den aktuella tidsposten. Du kan komma åt affärsreglerna för en sida genom att öppna formulärsredigeraren och sedan välja **Affärsregler**. Du kan sedan redigera de befintliga affärsreglerna eller lägga till en ny affärsregel.

#### <a name="server-side-plug-in-validations"></a>Validering av plugin-program på serversidan
Du bör använda plugin-valideringar för alla valideringar som kräver mer kontext än vad som är tillgängligt i en enskild tidspost. Du bör också använda dem för alla valideringar som du vill köra på infogade uppdateringar i rutnätet. Slutför valideringar genom att skapa ett eget plugin-program för entiteten **tidspost**.

### <a name="limits"></a>Gränser
För tillfället har rutnätet **Tidspost** en storleksbegränsning på 500 rader. Om det finns fler än 500 rader visas inte radöverskottet. Det går inte att öka storleksgränsen.

### <a name="copying-time-entries"></a>Kopiera tidsposter
Använd vyn **Kopiera tidspostkolumner** för att definiera listan över fält som ska kopieras under en tidspost. **Datum** och **Varaktighet** är obligatoriska fält och bör inte tas bort från vyn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
