---
title: Detaljerad sidhuvudinformation för underavtal
description: Detta ämne förklarar de funktioner som tillhandahålls i underavtalshuvudet i Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fade0ff876486ad60ffd9ad618be7864c1b28185
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598188"
---
# <a name="header-details-for-subcontracts"></a>Detaljerad sidhuvudinformation för underavtal

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Detta ämne förklarar de funktioner som tillhandahålls i underavtalshuvudet i Dynamics 365 Project Operations.

I takt med att projektledare planerar och genomför projekt kan de anlita underleverantörer och köpa produkter och tjänster från leverantörer. När en projektledare behöver köpa produkter eller tjänster kan han eller hon skapa ett underavtal i Project Operations.

Skapa ett underavtal genom att följa stegen nedan.

1. I navigeringsfönstret väljer du **Underavtal**, innan du på sidan **Underavtal** väljer **Ny**.
2. Ange information som krävs och klicka sedan på **Spara**.

    Följande tabell innehåller information om fälten på sidan **Underavtalshuvud**.

    | Fält | Beskrivning |Funktionellt påverkan |
    |---|------|---| 
    | Namn | Namnet på underavtalet. | I alla listrutan underleverantör visas namnet på undernamnet i den första kolumnen så att du kan identifiera underleverantörsnamnet. | 
    | Beskrivning | En kort beskrivning av tjänster produkter som köps i underavtalet. | Nej |
    | Leverantör | Namnet på det företag som produkterna och tjänsterna köps från. Denna kontopost har relationstypen **Säljare** eller **Leverantör**. | Standardvärden anges automatiskt för följande fält baserat på den leverantör som valts:<br/> **• Valuta** </br> **• Prislistor** </br> **• Betalningsvillkor**</br> **• Betalningsadress**</br> **• Fakturera till adress**</br> **• Fakturera till namn** </br>**• Leverantörens kontoansvariga**|
    | Underkontraktsdatum | Det datum då underkonsekvensen skapas. | Underleverantörsdatum används för att välja rätt inköpsprislista antingen från de prislistor som är kopplade till den relaterade leverantören eller från projektparametrarna. |
    | Statusorsak | Status för underavtalet. | Status avgör var underleverantör finns i affärsprocessen och om den kan redigeras. <br/>Exempel på värden:<br>• **Utkast**: Undermappen kan redigeras. Du kan endast redigera underleverantörer med status **Utkast**.<br/>• **Bekräftad**: Kontraktet med leverantören är slutfört och underleverantören är godkänd för leverans. <br/>• **Stängd**: Leveranserna i underkontraktet är slutförda.<br/>• **Annullerad**: Underentreprenaden avbröts och ingen leverans är planerad.  | 
    | Valuta | Valuta som produkter och tjänster köps i. Standardvärdet anges automatiskt från leverantörskontot, men det kan ändras. | Delkontraktets valuta för att välja inköpsprislista antingen från de prislistor som är kopplade till den relaterade leverantören eller från projektparametrarna. Prislistor i en annan valuta kan inte associeras med undervalutan. Kostnaden för tid, utgifter och material som leverantörers resurser levererar från denna underleverantör registreras i den här valutan i projektet. När underleverantörsposten har sparats går det inte att ändra valutan på underleverantörsposten.|
    | Kontrakteringsenhet | Den avdelning i företaget som ingår ett köpekontrakt eller ett underavtal med leverantören. | Nej |
    | Betalningsvillkor | Betalningsvillkor för leverantörsfakturor som utfärdas för denna underleverantör. Standardvärdet anges automatiskt från leverantörskontot. | Betalningsvillkor från underleverantören kopieras till alla leverantörsfakturor som är relaterade till denna underleverantör. Betalningsvillkor kan uppdateras om underleverantör har statusen **Utkast**. | 
    | Betalningsadress | Adressen till den leverantör som betalningar måste skickas till. Standardvärdet anges automatiskt från leverantörskontot. | Betalningsadressen från underleverantören kopieras som betalningsadress till alla leverantörsfakturor som skapas för den här underleverantören. Betalningsadressen kan uppdateras om underleverantör har statusen **Utkast**.|
    | Fakturera till namn | Namnet på den person eller avdelning i det leverantörsföretag som ska skicka fakturan. Standardvärdet anges automatiskt från leverantörskontot. | **Fakturera till namn** från underleverantören kopieras till alla leverantörsfakturor som är relaterade till denna underleverantör. Detta fält kan uppdateras om underleverantör har statusen **Utkast**.|
    | Faktureringsadress | Adressen som används på fakturor från leverantören. Standardvärdet anges automatiskt från leverantörskontot. | Den här adressen är "faktura från"-adressen på leverantörsfakturor som skapas för den här underleverantören. |
    | Delsumma | Om en underleverantör inte har några rader anger du ordern som delsumma före moms. Om underavtalet har rader är det här fältet skrivskyddat. Det belopp som visas är delsumma från alla raderna i underleverantörsbeloppet. | Nej |
    | Total moms | Om en underleverantör inte har några rader, ange totala skatter på detta underentreprenad. Om underavtalet har rader är det här fältet skrivskyddat. Det belopp som visas är summan av skatten från alla raderna i underleverantörsbeloppet. | Nej |
    | Totalbelopp | Detta beräknade fält visar totalbeloppet för underavtalet efter det att moms har inkluderats. | Nej |
    | Bekräftelsedatum | Datum då underentreprenaden bekräftades. | Nej |
    | Begärd av | Som standard anges det här fältet till namnet på användaren som skapar undernamnet. Men den som skapade underkontraktet kan ändra värdet för att ange den person som underkontraktet den skapar för. | Nej |
    | Leverantörens kontoansvariga | Namnet på den primära kontakten för leverantörskontot. Standardvärdet anges automatiskt från leverantörskontot. Du kan välja en annan kontakt som leverantörskontohanterare för underleverantören. | Du kan konfigurera e-postaviseringar så att kontakten meddelas när ändringar görs i underkontakten till följd av prisförseningar. |
