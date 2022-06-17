---
title: Lägg till nya anpassade entitetsformulär (Project Service Automation 2.x)
description: I den här artikeln finns information om hur du lägger till anpassade entitetsformulär för affärsmöjligheter, offerter, order i Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922750"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Lägg till nya anpassade entitetsformulär (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Typfält 

Dynamics 365 Project Service Automation är beroende av fältet **Typ** (**msdyn\_ordertyp**) som används i entiteterna affärsmöjlighet, offert, order och faktura för att särskilja **arbetsbaserade** versioner av dessa entiteter från **objektbaserade** och **tjänstbaserade** versioner. Arbetsbaserade versioner av dessa entiteter hanteras av PSA. Många affärs logiker på klientsidan och serversidan av lösningen beror på fältet **typ**. Därför är det viktigt att fältet initieras med ett korrekt värde när entiteterna skapas. Ett felaktigt värde kan orsaka felaktiga beteenden och en del affärslogik kanske inte fungerar korrekt.

## <a name="automatic-form-switching"></a>Automatisk formulärväxling

För att undvika potentiella dataskador och oväntade problem som orsakas av felaktig initiering och redigering av försäljningsentitetsposterna inkluderar PSA nu logik för automatisk formulärväxling i färdiga formulär. Den här logiken använder rätt formulär för att arbeta med den arbetsbaserade versionen eller någon annan typ av entitet för affärsmöjlighet, offert, order eller faktura. När en användare öppnar den arbetsbaserade versionen av en entitet för affärsmöjlighet, offert, order eller faktura växlas formuläret till **projektinformation**.

Den automatiska formulär växlingslogiken förlitar sig på mappningen mellan **formId** och fältet **msdyn\_ordertyp**. Alla färdiga formulär har lagts till i mappningen. Anpassade formulär måste dock läggas till manuellt för att ange vilken version av entiteten de ska hantera. Det här baseras på fältet **msdyn\_ordertyp**. Om formulärväxlingen saknas i mappningen växlar logik till det färdiga formuläret utifrån värdet som sparas i fältet **msdyn\_ordertyp** i entiteten.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Lägga till egna formulär och aktivera formulärväxlingslogik

I följande exempel visas hur du lägger till ett anpassat formulär **min projektinformation** så att det fungerar med arbetsbaserade affärsmöjligheter. Samma process används för att lägga till egna formulär så att de fungerar med offerter, order och fakturor.

Följ stegen nedan om du vill skapa en anpassad version av formuläret **projektinformation**.

1. I entiteten Affärsmöjlighet, öppna formuläret **Projektinformation** och spara en kopia under namnet **Min projektinformation**.
2. Öppna det nya formuläret och kontrollera att skripten för formulärinitiering från formuläret **projektinformation** finns. 

    > [!IMPORTANT]
    > Ta inte bort skripten. Annars kan vissa data ha initierats felaktigt.

3. Kontrollera att fältet **Typ** (**msdyn\_ordertyp**) finns i formuläret. 

    > [!IMPORTANT]
    > Ta inte bort det här fältet. Annars misslyckas initieringsskripten.

4. Leta upp värdet **formId** för det nya formuläret. Du kan slutföra detta steg på två olika sätt:

    - Exportera **Min projektinformation** som en del av en ohanterad lösning och leta upp värdet för **formId** i filen customization.xml för den exporterade lösningen.
    - Öppna formuläret **Min projektinformation** i formulärredigerare och leta upp globalt unik identifierare (GUID) bredvid parametern **fromId** i URL som visas i följande bild.

    ![Värdet formId för det nya formuläret i URL:en.](media/how-to-add-custom-forms-in-v2.0.png)

5. Skapa en mappning **msdyn\_ordertyp** för värdet **formId** genom att redigera webbresursen msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Ta bort koden från resursen och ersätt den med följande kod.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Spara och publicera anpassningarna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
