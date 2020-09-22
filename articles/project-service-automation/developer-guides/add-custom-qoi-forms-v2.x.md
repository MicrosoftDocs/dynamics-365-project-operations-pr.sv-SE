---
title: Lägg till nya anpassade entitetsformulär (Project Service Automation 2.x)
description: I det här ämnet finns information om hur du lägger till anpassade entitetsformulär för affärsmöjligheter, offerter, order i Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756127"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="06c6d-103">Lägg till nya anpassade entitetsformulär (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="06c6d-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="06c6d-104">Typfält</span><span class="sxs-lookup"><span data-stu-id="06c6d-104">Type field</span></span> 

<span data-ttu-id="06c6d-105">Dynamics 365 Project Service Automation är beroende av fältet **Typ** (**msdyn\_ordertyp**) som används i entiteterna affärsmöjlighet, offert, order och faktura för att särskilja **arbetsbaserade** versioner av dessa entiteter från **objektbaserade** och **tjänstbaserade** versioner.</span><span class="sxs-lookup"><span data-stu-id="06c6d-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="06c6d-106">Arbetsbaserade versioner av dessa entiteter hanteras av PSA.</span><span class="sxs-lookup"><span data-stu-id="06c6d-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="06c6d-107">Många affärs logiker på klientsidan och serversidan av lösningen beror på fältet **typ**.</span><span class="sxs-lookup"><span data-stu-id="06c6d-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="06c6d-108">Därför är det viktigt att fältet initieras med ett korrekt värde när entiteterna skapas.</span><span class="sxs-lookup"><span data-stu-id="06c6d-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="06c6d-109">Ett felaktigt värde kan orsaka felaktiga beteenden och en del affärslogik kanske inte fungerar korrekt.</span><span class="sxs-lookup"><span data-stu-id="06c6d-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="06c6d-110">Automatisk formulärväxling</span><span class="sxs-lookup"><span data-stu-id="06c6d-110">Automatic form switching</span></span>

<span data-ttu-id="06c6d-111">För att undvika potentiella dataskador och oväntade problem som orsakas av felaktig initiering och redigering av försäljningsentitetsposterna inkluderar PSA nu logik för automatisk formulärväxling i färdiga formulär.</span><span class="sxs-lookup"><span data-stu-id="06c6d-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="06c6d-112">Den här logiken använder rätt formulär för att arbeta med den arbetsbaserade versionen eller någon annan typ av entitet för affärsmöjlighet, offert, order eller faktura.</span><span class="sxs-lookup"><span data-stu-id="06c6d-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="06c6d-113">När en användare öppnar den arbetsbaserade versionen av en entitet för affärsmöjlighet, offert, order eller faktura växlas formuläret till **projektinformation**.</span><span class="sxs-lookup"><span data-stu-id="06c6d-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="06c6d-114">Den automatiska formulär växlingslogiken förlitar sig på mappningen mellan **formId** och fältet **msdyn\_ordertyp**.</span><span class="sxs-lookup"><span data-stu-id="06c6d-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="06c6d-115">Alla färdiga formulär har lagts till i mappningen.</span><span class="sxs-lookup"><span data-stu-id="06c6d-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="06c6d-116">Anpassade formulär måste dock läggas till manuellt för att ange vilken version av entiteten de ska hantera.</span><span class="sxs-lookup"><span data-stu-id="06c6d-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="06c6d-117">Det här baseras på fältet **msdyn\_ordertyp**.</span><span class="sxs-lookup"><span data-stu-id="06c6d-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="06c6d-118">Om formulärväxlingen saknas i mappningen växlar logik till det färdiga formuläret utifrån värdet som sparas i fältet **msdyn\_ordertyp** i entiteten.</span><span class="sxs-lookup"><span data-stu-id="06c6d-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="06c6d-119">Lägga till egna formulär och aktivera formulärväxlingslogik</span><span class="sxs-lookup"><span data-stu-id="06c6d-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="06c6d-120">I följande exempel visas hur du lägger till ett anpassat formulär **min projektinformation**så att det fungerar med arbetsbaserade affärsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="06c6d-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="06c6d-121">Samma process används för att lägga till egna formulär så att de fungerar med offerter, order och fakturor.</span><span class="sxs-lookup"><span data-stu-id="06c6d-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="06c6d-122">Följ stegen nedan om du vill skapa en anpassad version av formuläret **projektinformation**.</span><span class="sxs-lookup"><span data-stu-id="06c6d-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="06c6d-123">I entiteten Affärsmöjlighet, öppna formuläret **Projektinformation** och spara en kopia under namnet **Min projektinformation**.</span><span class="sxs-lookup"><span data-stu-id="06c6d-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="06c6d-124">Öppna det nya formuläret och kontrollera att skripten för formulärinitiering från formuläret **projektinformation** finns.</span><span class="sxs-lookup"><span data-stu-id="06c6d-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="06c6d-125">Ta inte bort skripten.</span><span class="sxs-lookup"><span data-stu-id="06c6d-125">Don't remove the scripts.</span></span> <span data-ttu-id="06c6d-126">Annars kan vissa data ha initierats felaktigt.</span><span class="sxs-lookup"><span data-stu-id="06c6d-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="06c6d-127">Kontrollera att fältet **Typ** (**msdyn\_ordertyp**) finns i formuläret.</span><span class="sxs-lookup"><span data-stu-id="06c6d-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="06c6d-128">Ta inte bort det här fältet.</span><span class="sxs-lookup"><span data-stu-id="06c6d-128">Don't remove this field.</span></span> <span data-ttu-id="06c6d-129">Annars misslyckas initieringsskripten.</span><span class="sxs-lookup"><span data-stu-id="06c6d-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="06c6d-130">Leta upp värdet **formId** för det nya formuläret.</span><span class="sxs-lookup"><span data-stu-id="06c6d-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="06c6d-131">Du kan slutföra detta steg på två olika sätt:</span><span class="sxs-lookup"><span data-stu-id="06c6d-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="06c6d-132">Exportera **Min projektinformation** som en del av en ohanterad lösning och leta upp värdet för **formId** i filen customization.xml för den exporterade lösningen.</span><span class="sxs-lookup"><span data-stu-id="06c6d-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="06c6d-133">Öppna formuläret **Min projektinformation** i formulärredigerare och leta upp globalt unik identifierare (GUID) bredvid parametern **fromId** i URL som visas i följande bild.</span><span class="sxs-lookup"><span data-stu-id="06c6d-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Värdet formId för det nya formuläret i URL:en.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="06c6d-135">Skapa en mappning **msdyn\_ordertyp** för värdet **formId** genom att redigera webbresursen msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="06c6d-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="06c6d-136">Ta bort koden från resursen och ersätt den med följande kod.</span><span class="sxs-lookup"><span data-stu-id="06c6d-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="06c6d-137">Spara och publicera anpassningarna.</span><span class="sxs-lookup"><span data-stu-id="06c6d-137">Save and then publish the customizations.</span></span>
