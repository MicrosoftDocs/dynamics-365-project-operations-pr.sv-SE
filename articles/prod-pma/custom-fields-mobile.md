---
title: Implementera anpassade fält för Microsoft Dynamics 365 Project Timesheet mobilappen på iOS och Android
description: I det här ämne finns vanliga mönster för att använda tillägg för att implementera anpassade fält.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271015"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="496b1-103">Implementera anpassade fält för Microsoft Dynamics 365 Project Timesheet mobilappen på iOS och Android</span><span class="sxs-lookup"><span data-stu-id="496b1-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="496b1-104">I det här ämne finns vanliga mönster för att använda tillägg för att implementera anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="496b1-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="496b1-105">Följande ämnen berörs:</span><span class="sxs-lookup"><span data-stu-id="496b1-105">The following topics are covered:</span></span>

- <span data-ttu-id="496b1-106">De olika datatyper som det anpassade fältramverket stöder</span><span class="sxs-lookup"><span data-stu-id="496b1-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="496b1-107">Visa skrivskyddade eller redigerbara fält i tidrapportposter och återställ värdena som användaren har angett tillbaka till databasen</span><span class="sxs-lookup"><span data-stu-id="496b1-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="496b1-108">Visa skrivskyddade fält i ett tidrapporthuvud</span><span class="sxs-lookup"><span data-stu-id="496b1-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="496b1-109">Integrera andra anpassade affärslogik för att ange standardvärden i fält och göra ytterligare verifiering</span><span class="sxs-lookup"><span data-stu-id="496b1-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="496b1-110">Målgrupp</span><span class="sxs-lookup"><span data-stu-id="496b1-110">Audience</span></span>

<span data-ttu-id="496b1-111">Den här ämne är avsedd för utvecklare som integrerar sina anpassade fält i Microsoft Dynamics 365 Project Timesheet mobilappen som är tillgänglig för Apple iOS och Google Android.</span><span class="sxs-lookup"><span data-stu-id="496b1-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="496b1-112">Antagandet är att läsarna är bekant med funktionerna för utveckling av X++ utveckling och tidrapport för projekt.</span><span class="sxs-lookup"><span data-stu-id="496b1-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="496b1-113">Datakontrakt – TSTimesheetCustomField X++ klass</span><span class="sxs-lookup"><span data-stu-id="496b1-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="496b1-114">**TSTimesheetCustomField**-klassen är X++ datakontraktsklassen som representerar information om ett anpassat fält för tidrapportfunktioner.</span><span class="sxs-lookup"><span data-stu-id="496b1-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="496b1-115">Listorna över de anpassade fältvärdena skickas både i TSTimesheetDetails datakontrakt och TSTimesheetEntry för att visa anpassade fält i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="496b1-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="496b1-116">**TSTimesheetDetails** – kontrakt för tidrapporthuvud.</span><span class="sxs-lookup"><span data-stu-id="496b1-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="496b1-117">**TSTimesheetEntry** – kontrakt för tidrapporttransaktion.</span><span class="sxs-lookup"><span data-stu-id="496b1-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="496b1-118">Grupper med dessa objekt som har samma projektinformation och värdet **timesheetLineRecId** utgör en rad.</span><span class="sxs-lookup"><span data-stu-id="496b1-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="496b1-119">fieldBaseType (typer)</span><span class="sxs-lookup"><span data-stu-id="496b1-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="496b1-120">Egenskapen **FieldBaseType** i objektet **TsTimesheetCustom** avgör vilken typ av fält som visas i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="496b1-121">Följande värden **typer** stöds.</span><span class="sxs-lookup"><span data-stu-id="496b1-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="496b1-122">Värdet typer</span><span class="sxs-lookup"><span data-stu-id="496b1-122">Types value</span></span> | <span data-ttu-id="496b1-123">Type</span><span class="sxs-lookup"><span data-stu-id="496b1-123">Type</span></span>              | <span data-ttu-id="496b1-124">Anteckning</span><span class="sxs-lookup"><span data-stu-id="496b1-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="496b1-125">0</span><span class="sxs-lookup"><span data-stu-id="496b1-125">0</span></span>           | <span data-ttu-id="496b1-126">Sträng (och Enum)</span><span class="sxs-lookup"><span data-stu-id="496b1-126">String (and Enum)</span></span> | <span data-ttu-id="496b1-127">Fältet visas som ett textfält.</span><span class="sxs-lookup"><span data-stu-id="496b1-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="496b1-128">1</span><span class="sxs-lookup"><span data-stu-id="496b1-128">1</span></span>           | <span data-ttu-id="496b1-129">Integer</span><span class="sxs-lookup"><span data-stu-id="496b1-129">Integer</span></span>           | <span data-ttu-id="496b1-130">Värdet visas som ett tal utan decimaler.</span><span class="sxs-lookup"><span data-stu-id="496b1-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="496b1-131">2</span><span class="sxs-lookup"><span data-stu-id="496b1-131">2</span></span>           | <span data-ttu-id="496b1-132">Real</span><span class="sxs-lookup"><span data-stu-id="496b1-132">Real</span></span>              | <span data-ttu-id="496b1-133">Värdet visas som ett tal som har decimaler.</span><span class="sxs-lookup"><span data-stu-id="496b1-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="496b1-134">Använd egenskapen **fieldExtenededType** för att visa det verkliga värdet som en valuta i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="496b1-135">Du kan använda egenskapen **numberOfDecimals** för att ange antalet decimaler som ska visas.</span><span class="sxs-lookup"><span data-stu-id="496b1-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="496b1-136">3</span><span class="sxs-lookup"><span data-stu-id="496b1-136">3</span></span>           | <span data-ttu-id="496b1-137">Datum</span><span class="sxs-lookup"><span data-stu-id="496b1-137">Date</span></span>              | <span data-ttu-id="496b1-138">Datumformat bestäms av användarens inställning för **datum, tid och nummerformat** som anges under **Inställning av språk- och land/region** i **Användaralternativ**.</span><span class="sxs-lookup"><span data-stu-id="496b1-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="496b1-139">4</span><span class="sxs-lookup"><span data-stu-id="496b1-139">4</span></span>           | <span data-ttu-id="496b1-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="496b1-140">Boolean</span></span>           | |
| <span data-ttu-id="496b1-141">15</span><span class="sxs-lookup"><span data-stu-id="496b1-141">15</span></span>          | <span data-ttu-id="496b1-142">GUID</span><span class="sxs-lookup"><span data-stu-id="496b1-142">GUID</span></span>              | |
| <span data-ttu-id="496b1-143">16</span><span class="sxs-lookup"><span data-stu-id="496b1-143">16</span></span>          | <span data-ttu-id="496b1-144">Int64</span><span class="sxs-lookup"><span data-stu-id="496b1-144">Int64</span></span>             | |

- <span data-ttu-id="496b1-145">Om egenskapen **stringOptions** inte finns i objektet **TSTimesheetCustomField** kommer ett fritextfält att visas för användaren.</span><span class="sxs-lookup"><span data-stu-id="496b1-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="496b1-146">Egenskapen **stringLength** kan användas för att ange den maximala stränglängd som användare kan ange.</span><span class="sxs-lookup"><span data-stu-id="496b1-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="496b1-147">Om egenskapen **stringOptions** tillhandahålls objekt **TSTimesheetCustomField** är dessa listelement de enda värden som användarna kan välja med hjälp av alternativknappar (radioknappar).</span><span class="sxs-lookup"><span data-stu-id="496b1-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="496b1-148">I det här fallet kan strängfältet användas som ett uppräkningsvärde för användarpostens syfte.</span><span class="sxs-lookup"><span data-stu-id="496b1-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="496b1-149">För att spara värdet i databasen som enum, mappa strängvärdet manuellt tillbaka till enumvärdet innan du sparar i databasen med hjälp av kommandokedjan (se "Använd kommandokedjan i klassen TSTimesheetEntryService för att spara en tidrapportspost från appen tillbaka till databasen ”senare i detta ämne för ett exempel).</span><span class="sxs-lookup"><span data-stu-id="496b1-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="496b1-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="496b1-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="496b1-151">Du kan använda den här egenskapen om du vill formatera verkliga värden som valuta.</span><span class="sxs-lookup"><span data-stu-id="496b1-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="496b1-152">Den här metoden gäller endast om värdet **fieldBaseType** är **real**.</span><span class="sxs-lookup"><span data-stu-id="496b1-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="496b1-153">**TSCustomFieldExtendedType:None** – ingen formatering tillämpas.</span><span class="sxs-lookup"><span data-stu-id="496b1-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="496b1-154">**TSCustomFieldExtendedType::Currency** – Formatera värdet som valuta.</span><span class="sxs-lookup"><span data-stu-id="496b1-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="496b1-155">När valuta formatet är aktivt kan fältet **stringValue** användas för att skicka valutakoden som ska visas i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="496b1-156">Värdet är ett skrivskyddat värde.</span><span class="sxs-lookup"><span data-stu-id="496b1-156">The value is a read-only value.</span></span>

    <span data-ttu-id="496b1-157">Fältet **realValue** innehåller det belopp som ska sparas i databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="496b1-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="496b1-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="496b1-159">Du kan använda den här egenskapen för att ange var ett anpassat fält ska visas i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="496b1-160">**TSCustomFieldSection::rubrik** – Fältet kommer att visas i avsnittet **Visa fler detaljer** i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="496b1-161">De här fälten är alltid skrivskyddade.</span><span class="sxs-lookup"><span data-stu-id="496b1-161">These fields are always read-only.</span></span>
- <span data-ttu-id="496b1-162">**TSCustomFieldSection::Rad** – fältet kommer att visas efter alla färdiga radfält i tidrapportposter.</span><span class="sxs-lookup"><span data-stu-id="496b1-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="496b1-163">Dessa fält kan antingen vara redigerbara eller skrivskyddade.</span><span class="sxs-lookup"><span data-stu-id="496b1-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="496b1-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="496b1-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="496b1-165">Den här egenskapen identifierar fältet när värden som appen tillhandahåller sparas i databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="496b1-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="496b1-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="496b1-167">Den här egenskapen identifierar fältet när värden som appen tillhandahåller sparas i databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="496b1-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="496b1-168">isEditable (NoYes)</span></span>

<span data-ttu-id="496b1-169">Ange den här egenskapen till **Ja** för att ange att fältet i avsnittet tidrapportpost ska vara redigerbart av användarna.</span><span class="sxs-lookup"><span data-stu-id="496b1-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="496b1-170">Ange egenskapen till **Nej** om fältet ska vara skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="496b1-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="496b1-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="496b1-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="496b1-172">Ange den här egenskapen till **Ja** för att ange att fältet i avsnittet tidrapportpost ska vara obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="496b1-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="496b1-173">etikett (str)</span><span class="sxs-lookup"><span data-stu-id="496b1-173">label (str)</span></span>

<span data-ttu-id="496b1-174">Den här egenskapen anger etiketten som visas bredvid fält i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="496b1-175">stringOptions (lista över strängar)</span><span class="sxs-lookup"><span data-stu-id="496b1-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="496b1-176">Den här egenskapen gäller endast om **fieldBaseType** har värdet **Sträng**.</span><span class="sxs-lookup"><span data-stu-id="496b1-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="496b1-177">Om **stringOptions** har angetts anges strängvärden som är tillgängliga för markering via alternativknappar (radioknappar) enligt strängarna i listan.</span><span class="sxs-lookup"><span data-stu-id="496b1-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="496b1-178">Om det inte finns några strängar tillåts fritextpost i strängfältet (se avsnittet "använd en kedja i klassen TSTimesheetEntryService för att spara en tidrapportpost från appen tillbaka till databasen" längre ned i det här ämnet för ett exempel).</span><span class="sxs-lookup"><span data-stu-id="496b1-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="496b1-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="496b1-179">stringLength (int)</span></span>

<span data-ttu-id="496b1-180">Den här egenskapen anger den maximala tillåtna längden för ett strängfält.</span><span class="sxs-lookup"><span data-stu-id="496b1-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="496b1-181">Det är bara tillämpligt när **fieldBaseType** anges till **Sträng**.</span><span class="sxs-lookup"><span data-stu-id="496b1-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="496b1-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="496b1-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="496b1-183">Den här egenskapen anger antalet decimaler som visas för ett realfält.</span><span class="sxs-lookup"><span data-stu-id="496b1-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="496b1-184">Det är bara tillämpligt när **fieldBaseType** anges till **Real**.</span><span class="sxs-lookup"><span data-stu-id="496b1-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="496b1-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="496b1-185">orderSequence (int)</span></span>

<span data-ttu-id="496b1-186">Den här egenskapen styr i vilken ordning de anpassade fälten visas i appen när fler än ett anpassat fält anges.</span><span class="sxs-lookup"><span data-stu-id="496b1-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="496b1-187">Fält som har lägre nummer visas först.</span><span class="sxs-lookup"><span data-stu-id="496b1-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="496b1-188">booleanValue (boolesk)</span><span class="sxs-lookup"><span data-stu-id="496b1-188">booleanValue (boolean)</span></span>

<span data-ttu-id="496b1-189">För fält av typen **Boolesk** den här egenskapen skickar fältets booleska värde mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="496b1-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="496b1-190">guidValue (guid)</span></span>

<span data-ttu-id="496b1-191">För fält av typen **GUID** den här egenskapen skickar fältets värde globalt unik identifierare (GUID) mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="496b1-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="496b1-192">int64Value (int64)</span></span>

<span data-ttu-id="496b1-193">För fält av typen **Int64** den här egenskapen skickar fältets Int64 värde mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="496b1-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="496b1-194">intValue (int)</span></span>

<span data-ttu-id="496b1-195">För fält av typen **Int** den här egenskapen skickar fältets int värde mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="496b1-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="496b1-196">realValue (real)</span></span>

<span data-ttu-id="496b1-197">För fält av typen **Real** den här egenskapen skickar fältets realvärde mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="496b1-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="496b1-198">stringValue (str)</span></span>

<span data-ttu-id="496b1-199">För fält av typen **Sträng** den här egenskapen skickar fältets strängvärde mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="496b1-200">Det används även för fält av typen **Real** som är formaterade som valuta.</span><span class="sxs-lookup"><span data-stu-id="496b1-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="496b1-201">För dessa fält används egenskapen för att skicka valutakoden till appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="496b1-202">dateValue (datum)</span><span class="sxs-lookup"><span data-stu-id="496b1-202">dateValue (date)</span></span>

<span data-ttu-id="496b1-203">För fält av typen **Datum** den här egenskapen skickar fältets datumvärde mellan servern och appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="496b1-204">Visa och spara ett anpassat fält i avsnittet tidrapportpost</span><span class="sxs-lookup"><span data-stu-id="496b1-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="496b1-205">Nedan visas en skärmdump från mobilappen för en tidrapportpost skapande.</span><span class="sxs-lookup"><span data-stu-id="496b1-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="496b1-206">Den visar de medföljande fälten och ett anpassat fält i avsnittet "tidspost", "teststräng", med ett uppräkningsvärde för ett "andra alternativ" har redan angetts.</span><span class="sxs-lookup"><span data-stu-id="496b1-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Teststrängens anpassade fält i appen](media/timesheet-entry.jpg)



<span data-ttu-id="496b1-208">Nedan visas en skärmdump från mobilappen för användaren välja ett av de uppräkningsalternativ som är tillgängliga för det anpassade fältet "teststräng".</span><span class="sxs-lookup"><span data-stu-id="496b1-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="496b1-209">De två alternativen är "första alternativ" och "andra alternativet" visas som alternativknappar.</span><span class="sxs-lookup"><span data-stu-id="496b1-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="496b1-210">Det andra alternativet är markerat.</span><span class="sxs-lookup"><span data-stu-id="496b1-210">The second option is currently selected.</span></span>

![Alternativknappar (radioknappar) för det anpassade fältet för teststräng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="496b1-212">Utöka tabellen TSTimesheetLine så att den har ett anpassat fält</span><span class="sxs-lookup"><span data-stu-id="496b1-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="496b1-213">I vanliga situationer är det troligt att data för ett anpassat fält i avsnittet tidrapportspost kommer att sparas i TSTimesheetLine-tabellen.</span><span class="sxs-lookup"><span data-stu-id="496b1-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="496b1-214">Andra tabeller kan dock användas om data kan hämtas baserat på en TSTimesheetTrans-post som tillhandahålls eller om den inte har ett specifikt postkontext (till exempel om fältet är skrivskyddat i projektparametrarna) .</span><span class="sxs-lookup"><span data-stu-id="496b1-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="496b1-215">Observera att anpassade fält inte behöver ha några säkerhetsposter i databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="496b1-216">De kan skapas dynamiskt utifrån X++ logik.</span><span class="sxs-lookup"><span data-stu-id="496b1-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="496b1-217">Detta tillvägagångssätt kan vara användbart i skrivskyddade scenarier (se avsnittet "Använd kommandokedja i TSTimesheetDetails-klassen, buildCustomFieldListForHeader-metoden för att fylla i tidsrapportdetaljer" för ett exempel på dynamiskt genererade anpassade fältvärden.)</span><span class="sxs-lookup"><span data-stu-id="496b1-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="496b1-218">Nedan visas en skärmbild från Visual Studio av appens objektträdet.</span><span class="sxs-lookup"><span data-stu-id="496b1-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="496b1-219">Den visar en utvidgning av TSTimesheetLine-tabellen med TestLineString-fältet tillagt som ett anpassat fält.</span><span class="sxs-lookup"><span data-stu-id="496b1-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Radsträng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="496b1-221">Använd kommandokedja på buildCustomFieldList-metoden i TSTimesheetSettings-klassen för att visa ett fält i tidrapportpost</span><span class="sxs-lookup"><span data-stu-id="496b1-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="496b1-222">Den här koden styr bildskärmsinställningarna för fältet i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="496b1-223">Till exempel styr den typen av fält, etiketten, om fältet är obligatoriskt och vilket avsnitt fältet visas i.</span><span class="sxs-lookup"><span data-stu-id="496b1-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="496b1-224">I följande exempel visas ett sträng fält i tidposter.</span><span class="sxs-lookup"><span data-stu-id="496b1-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="496b1-225">Det här fältet har två alternativ **Första alternativet** och **Andra alternativet**, som är tillgängliga via alternativknappar (radioknappar).</span><span class="sxs-lookup"><span data-stu-id="496b1-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="496b1-226">Fältet i appen är associerat med fältet **TestLineString** som läggs till i tabellen TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="496b1-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="496b1-227">Observera att användningen av metoden **TSTimesheetCustomField::newFromMetatdata()** för att förenkla initieringen av de anpassade fältegenskaperna: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** och **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="496b1-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="496b1-228">Du kan även ange dessa parametrar manuellt, som du vill.</span><span class="sxs-lookup"><span data-stu-id="496b1-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="496b1-229">Använd kommandot på buildCustomFieldListForEntry-metoden i TSTimesheetEntry-klassen för att ange värden i tidrapportpost</span><span class="sxs-lookup"><span data-stu-id="496b1-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="496b1-230">Metoden **buildCustomFieldListForEntry** används för att ange värden för de sparade tidrapportraderna i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="496b1-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="496b1-231">En TSTimesheetTrans-post tas som en parameter.</span><span class="sxs-lookup"><span data-stu-id="496b1-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="496b1-232">Fält från den posten kan användas för att fylla i det anpassade fältvärdet i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="496b1-233">Använd kommandot kedja i klassen TSTimesheetEntryService för att spara en tidrapportpost från appen tillbaka till databasen</span><span class="sxs-lookup"><span data-stu-id="496b1-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="496b1-234">Om du vill att ett anpassat fält ska sparas i databasen i normal användning måste du utöka flera metoder:</span><span class="sxs-lookup"><span data-stu-id="496b1-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="496b1-235">Metoden **timesheetLineNeedsUpdating** används för att avgöra om radposten har ändrats av användaren i appen och måste sparas i databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="496b1-236">Om prestanda inte är ett problem kan den här metoden förenklas så att den alltid returnerar **sant**.</span><span class="sxs-lookup"><span data-stu-id="496b1-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="496b1-237">Metoderna **populateTimesheetLineFromEntryDuringCreate** och **populateTimesheetLineFromEntryDuringUpdate** kan utökas så att de anger värden i databas posten TSTimesheetLine från posten för TSTimesheetEntry data som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="496b1-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="496b1-238">I exemplet nedan ser du att mappningen mellan databasfält och transaktionsfält görs manuellt via X++ kod.</span><span class="sxs-lookup"><span data-stu-id="496b1-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="496b1-239">Metoden **populateTimesheetWeekFromEntry** kan även utökas om det anpassade fält som mappas till objektet **TSTimesheetEntry** måste skriva tillbaka till TSTimesheetLineweek-databastabellen.</span><span class="sxs-lookup"><span data-stu-id="496b1-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="496b1-240">I följande exempel sparas värdet **firstOption** eller **secondOption** som användaren väljer i databasen som ett värde för rådatasträngar.</span><span class="sxs-lookup"><span data-stu-id="496b1-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="496b1-241">Om databasfältet är ett fält av typen **Enum** kan dessa värden mappas manuellt till ett enum-värde och sedan sparas i ett enum-fält i databastabellen.</span><span class="sxs-lookup"><span data-stu-id="496b1-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="496b1-242">Visa ett anpassat fält i avsnittet tidrapporthuvud</span><span class="sxs-lookup"><span data-stu-id="496b1-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="496b1-243">Nedan visas en skärmdump från mobilappen för en användare som visar en tidrapport.</span><span class="sxs-lookup"><span data-stu-id="496b1-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="496b1-244">Knappen "Mer information" har markerats i det övre högra hörnet för att visa alternativet "Visa mer information".</span><span class="sxs-lookup"><span data-stu-id="496b1-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Visa kommandot för mer information](media/show-more.png)

<span data-ttu-id="496b1-246">Nedan följer en skärmdump från mobilappen som visar avsnittet "Mer" i en tidrapport.</span><span class="sxs-lookup"><span data-stu-id="496b1-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="496b1-247">Ett anpassat fält som heter "Utnyttjandegraden för denna tidrapport (beräknat anpassat fält)" har lagts till i rubriken för tidrapport.</span><span class="sxs-lookup"><span data-stu-id="496b1-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="496b1-248">Ett skrivskyddat värde på "0,667" har angetts för det anpassade fältet.</span><span class="sxs-lookup"><span data-stu-id="496b1-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Avsnittet Mer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="496b1-250">Utöka tabellen TSTimesheetTable så att den har ett anpassat fält</span><span class="sxs-lookup"><span data-stu-id="496b1-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="496b1-251">I vanliga situationer är det troligt att data för ett anpassat fält i avsnittet rubrik kommer att dras från tabellen TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="496b1-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="496b1-252">Andra tabeller kan dock användas om data kan hämtas baserat på en TSTimesheetTable-post som tillhandahålls eller om den inte har ett specifikt postkontext (till exempel om fältet är skrivskyddat i projektparametrarna) .</span><span class="sxs-lookup"><span data-stu-id="496b1-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="496b1-253">Observera att anpassade fält inte behöver ha några säkerhetsposter i databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="496b1-254">De kan skapas dynamiskt utifrån X++ logik.</span><span class="sxs-lookup"><span data-stu-id="496b1-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="496b1-255">I exemplet nedan visas den här metoden.</span><span class="sxs-lookup"><span data-stu-id="496b1-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="496b1-256">Fält i rubrikavsnittet är alltid skrivskyddade i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="496b1-257">Använd kommandokedja på buildCustomFieldList-metoden i TSTimesheetSettings-klassen för att visa ett fält i avsnittet rubrik</span><span class="sxs-lookup"><span data-stu-id="496b1-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="496b1-258">Den här koden styr bildskärmsinställningarna för fältet i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="496b1-259">Till exempel styr den typen av fält, etiketten, om fältet är obligatoriskt och vilket avsnitt fältet visas i.</span><span class="sxs-lookup"><span data-stu-id="496b1-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="496b1-260">I följande exempel visas ett beräknat värde i avsnittet rubrik i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="496b1-261">Använd kommandot på buildCustomFieldListForHeader-metoden i TSTimesheetDetails-klassen för att fylla i tidrapportens detaljer</span><span class="sxs-lookup"><span data-stu-id="496b1-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="496b1-262">Metoden **buildCustomFieldListForHeader** används för att fylla i tidsrapportens rubrikinformation i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="496b1-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="496b1-263">En TSTimesheetTable-post tas som en parameter.</span><span class="sxs-lookup"><span data-stu-id="496b1-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="496b1-264">Fält från den posten kan användas för att fylla i det anpassade fältvärdet i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="496b1-265">Följande exempel läser inga värden från databasen.</span><span class="sxs-lookup"><span data-stu-id="496b1-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="496b1-266">I stället använder den X++ logik för att skapa ett beräknat värde som sedan visas i appen.</span><span class="sxs-lookup"><span data-stu-id="496b1-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="496b1-267">Andra konfigurations- och utökningsmöjligheter</span><span class="sxs-lookup"><span data-stu-id="496b1-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="496b1-268">Lägga till ytterligare verifiering för appen</span><span class="sxs-lookup"><span data-stu-id="496b1-268">Adding additional validation for the app</span></span>

<span data-ttu-id="496b1-269">Befintlig logik för tidrapportfunktioner på databasnivå fungerar fortfarande som förväntat.</span><span class="sxs-lookup"><span data-stu-id="496b1-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="496b1-270">Om du vill avbryta genomförandet av spara eller skicka åtgärden och visa ett visst felmeddelande kan du lägga till **utlösa fel ("meddelande till användare")** till koden via en kedja med kommandotillägg.</span><span class="sxs-lookup"><span data-stu-id="496b1-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="496b1-271">Här är tre exempel på användbara utökningsmetoder:</span><span class="sxs-lookup"><span data-stu-id="496b1-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="496b1-272">Om **validateWrite** i TSTimesheetLine-tabellen returnerar **falsk** under en spara-åtgärd för en tidrapportrad visas ett felmeddelande i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="496b1-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="496b1-273">Om **validateSubmit** i TSTimesheetTable-tabellen returnerar **falsk** under inlämning av tidrapport i appen visas ett felmeddelande för användaren.</span><span class="sxs-lookup"><span data-stu-id="496b1-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="496b1-274">Logik som fyller i fält (till exempel **radegenskap**) under metoden **infoga** på TSTimesheetLine-tabellen, körs fortfarande.</span><span class="sxs-lookup"><span data-stu-id="496b1-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="496b1-275">Dölja och markera färdiga fält som är skrivskyddade via konfiguration</span><span class="sxs-lookup"><span data-stu-id="496b1-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="496b1-276">Från projektparametrar kan du göra fält som inte är skrivskyddade eller dolda i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="496b1-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="496b1-277">Ange alternativen i avsnittet **Mobila tidrapporter** på fliken **Tidrapporter** för sidan **Projektledning och redovisningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="496b1-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektparametrar](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="496b1-279">Ändra vilka aktiviteter som är tillgängliga för markering via tillägg</span><span class="sxs-lookup"><span data-stu-id="496b1-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="496b1-280">Aktiviteterna som är tillgängliga för urval för ett projekt fylls i via metoderna **getActivitiesForProject()** och **getActivityQuery()** i klassen **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="496b1-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="496b1-281">Du kan använda kommandokedja för att ändra det här beteendet så att det överensstämmer med affärsscenariot för de aktiviteter som är tillgängliga för markering för ett visst projekt.</span><span class="sxs-lookup"><span data-stu-id="496b1-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="496b1-282">Ange en standardkategori för projekt i tidrapportposter</span><span class="sxs-lookup"><span data-stu-id="496b1-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="496b1-283">Inmatning av en standardprojektkategori i tidrapportposter sker på tre nivåer.</span><span class="sxs-lookup"><span data-stu-id="496b1-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="496b1-284">Du kan använda kommandokedja för att utöka beteendet på någon av eller alla de här nivåerna för att uppnå det önskade beteendet.</span><span class="sxs-lookup"><span data-stu-id="496b1-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="496b1-285">Följande hierarki används:</span><span class="sxs-lookup"><span data-stu-id="496b1-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="496b1-286">I appen görs ett försök att lägga till standardkategori från projektresursen.</span><span class="sxs-lookup"><span data-stu-id="496b1-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="496b1-287">Den här standardkategorin anges i metoderna **getCurrentUserResource** och **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="496b1-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="496b1-288">Om standardkategorin inte visas på projektresursnivån försöker appen att hämta den från projektaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="496b1-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="496b1-289">Den här standardkategorin anges i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="496b1-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="496b1-290">Om standardkategorin inte visas på projektetaktivitetsnivå, standardkategorin som den hämtade från projektparametrarna.</span><span class="sxs-lookup"><span data-stu-id="496b1-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="496b1-291">Den här standardkategorin anges i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="496b1-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]