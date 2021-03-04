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
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085594"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementera anpassade fält för Microsoft Dynamics 365 Project Timesheet mobilappen på iOS och Android

[!include [banner](../includes/banner.md)]

I det här ämne finns vanliga mönster för att använda tillägg för att implementera anpassade fält. Följande ämnen berörs:

- De olika datatyper som det anpassade fältramverket stöder
- Visa skrivskyddade eller redigerbara fält i tidrapportposter och återställ värdena som användaren har angett tillbaka till databasen
- Visa skrivskyddade fält i ett tidrapporthuvud
- Integrera andra anpassade affärslogik för att ange standardvärden i fält och göra ytterligare verifiering

## <a name="audience"></a>Målgrupp

Den här ämne är avsedd för utvecklare som integrerar sina anpassade fält i Microsoft Dynamics 365 Project Timesheet mobilappen som är tillgänglig för Apple iOS och Google Android. Antagandet är att läsarna är bekant med funktionerna för utveckling av X++ utveckling och tidrapport för projekt.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datakontrakt – TSTimesheetCustomField X++ klass

**TSTimesheetCustomField** -klassen är X++ datakontraktsklassen som representerar information om ett anpassat fält för tidrapportfunktioner. Listorna över de anpassade fältvärdena skickas både i TSTimesheetDetails datakontrakt och TSTimesheetEntry för att visa anpassade fält i mobilappen.

- **TSTimesheetDetails** – kontrakt för tidrapporthuvud.
- **TSTimesheetEntry** – kontrakt för tidrapporttransaktion. Grupper med dessa objekt som har samma projektinformation och värdet **timesheetLineRecId** utgör en rad.

### <a name="fieldbasetype-types"></a>fieldBaseType (typer)

Egenskapen **FieldBaseType** i objektet **TsTimesheetCustom** avgör vilken typ av fält som visas i appen. Följande värden **typer** stöds.

| Värdet typer | Type              | Anteckning |
|-------------|-------------------|-------|
| 0           | Sträng (och Enum) | Fältet visas som ett textfält. |
| 1           | Integer           | Värdet visas som ett tal utan decimaler. |
| 2           | Real              | Värdet visas som ett tal som har decimaler.<p>Använd egenskapen **fieldExtenededType** för att visa det verkliga värdet som en valuta i appen. Du kan använda egenskapen **numberOfDecimals** för att ange antalet decimaler som ska visas.</p> |
| 3           | Datum              | Datumformat bestäms av användarens inställning för **datum, tid och nummerformat** som anges under **Inställning av språk- och land/region** i **Användaralternativ**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Om egenskapen **stringOptions** inte finns i objektet **TSTimesheetCustomField** kommer ett fritextfält att visas för användaren.

    Egenskapen **stringLength** kan användas för att ange den maximala stränglängd som användare kan ange.

- Om egenskapen **stringOptions** tillhandahålls objekt **TSTimesheetCustomField** är dessa listelement de enda värden som användarna kan välja med hjälp av alternativknappar (radioknappar).

    I det här fallet kan strängfältet användas som ett uppräkningsvärde för användarpostens syfte. För att spara värdet i databasen som enum, mappa strängvärdet manuellt tillbaka till enumvärdet innan du sparar i databasen med hjälp av kommandokedjan (se "Använd kommandokedjan i klassen TSTimesheetEntryService för att spara en tidrapportspost från appen tillbaka till databasen ”senare i detta ämne för ett exempel).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Du kan använda den här egenskapen om du vill formatera verkliga värden som valuta. Den här metoden gäller endast om värdet **fieldBaseType** är **real**.

- **TSCustomFieldExtendedType:None** – ingen formatering tillämpas.
- **TSCustomFieldExtendedType::Currency** – Formatera värdet som valuta.

    När valuta formatet är aktivt kan fältet **stringValue** användas för att skicka valutakoden som ska visas i appen. Värdet är ett skrivskyddat värde.

    Fältet **realValue** innehåller det belopp som ska sparas i databasen.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Du kan använda den här egenskapen för att ange var ett anpassat fält ska visas i appen.

- **TSCustomFieldSection::rubrik** – Fältet kommer att visas i avsnittet **Visa fler detaljer** i appen. De här fälten är alltid skrivskyddade.
- **TSCustomFieldSection::Rad** – fältet kommer att visas efter alla färdiga radfält i tidrapportposter. Dessa fält kan antingen vara redigerbara eller skrivskyddade.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Den här egenskapen identifierar fältet när värden som appen tillhandahåller sparas i databasen.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Den här egenskapen identifierar fältet när värden som appen tillhandahåller sparas i databasen.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Ange den här egenskapen till **Ja** för att ange att fältet i avsnittet tidrapportpost ska vara redigerbart av användarna. Ange egenskapen till **Nej** om fältet ska vara skrivskyddat.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Ange den här egenskapen till **Ja** för att ange att fältet i avsnittet tidrapportpost ska vara obligatoriskt.

### <a name="label-str"></a>etikett (str)

Den här egenskapen anger etiketten som visas bredvid fält i appen.

### <a name="stringoptions-list-of-strings"></a>stringOptions (lista över strängar)

Den här egenskapen gäller endast om **fieldBaseType** har värdet **Sträng**. Om **stringOptions** har angetts anges strängvärden som är tillgängliga för markering via alternativknappar (radioknappar) enligt strängarna i listan. Om det inte finns några strängar tillåts fritextpost i strängfältet (se avsnittet "använd en kedja i klassen TSTimesheetEntryService för att spara en tidrapportpost från appen tillbaka till databasen" längre ned i det här ämnet för ett exempel).

### <a name="stringlength-int"></a>stringLength (int)

Den här egenskapen anger den maximala tillåtna längden för ett strängfält. Det är bara tillämpligt när **fieldBaseType** anges till **Sträng**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Den här egenskapen anger antalet decimaler som visas för ett realfält. Det är bara tillämpligt när **fieldBaseType** anges till **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Den här egenskapen styr i vilken ordning de anpassade fälten visas i appen när fler än ett anpassat fält anges. Fält som har lägre nummer visas först.

### <a name="booleanvalue-boolean"></a>booleanValue (boolesk)

För fält av typen **Boolesk** den här egenskapen skickar fältets booleska värde mellan servern och appen.

### <a name="guidvalue-guid"></a>guidValue (guid)

För fält av typen **GUID** den här egenskapen skickar fältets värde globalt unik identifierare (GUID) mellan servern och appen.

### <a name="int64value-int64"></a>int64Value (int64)

För fält av typen **Int64** den här egenskapen skickar fältets Int64 värde mellan servern och appen.

### <a name="intvalue-int"></a>intValue (int)

För fält av typen **Int** den här egenskapen skickar fältets int värde mellan servern och appen.

### <a name="realvalue-real"></a>realValue (real)

För fält av typen **Real** den här egenskapen skickar fältets realvärde mellan servern och appen.

### <a name="stringvalue-str"></a>stringValue (str)

För fält av typen **Sträng** den här egenskapen skickar fältets strängvärde mellan servern och appen. Det används även för fält av typen **Real** som är formaterade som valuta. För dessa fält används egenskapen för att skicka valutakoden till appen.

### <a name="datevalue-date"></a>dateValue (datum)

För fält av typen **Datum** den här egenskapen skickar fältets datumvärde mellan servern och appen.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Visa och spara ett anpassat fält i avsnittet tidrapportpost

Nedan visas en skärmdump från mobilappen för en tidrapportpost skapande. Den visar de medföljande fälten och ett anpassat fält i avsnittet "tidspost", "teststräng", med ett uppräkningsvärde för ett "andra alternativ" har redan angetts.

![Teststrängens anpassade fält i appen](media/timesheet-entry.jpg)



Nedan visas en skärmdump från mobilappen för användaren välja ett av de uppräkningsalternativ som är tillgängliga för det anpassade fältet "teststräng".  De två alternativen är "första alternativ" och "andra alternativet" visas som alternativknappar. Det andra alternativet är markerat.

![Alternativknappar (radioknappar) för det anpassade fältet för teststräng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Utöka tabellen TSTimesheetLine så att den har ett anpassat fält

I vanliga situationer är det troligt att data för ett anpassat fält i avsnittet tidrapportspost kommer att sparas i TSTimesheetLine-tabellen. Andra tabeller kan dock användas om data kan hämtas baserat på en TSTimesheetTrans-post som tillhandahålls eller om den inte har ett specifikt postkontext (till exempel om fältet är skrivskyddat i projektparametrarna) .

Observera att anpassade fält inte behöver ha några säkerhetsposter i databasen. De kan skapas dynamiskt utifrån X++ logik. Detta tillvägagångssätt kan vara användbart i skrivskyddade scenarier (se avsnittet "Använd kommandokedja i TSTimesheetDetails-klassen, buildCustomFieldListForHeader-metoden för att fylla i tidsrapportdetaljer" för ett exempel på dynamiskt genererade anpassade fältvärden.)

Nedan visas en skärmbild från Visual Studio av appens objektträdet. Den visar en utvidgning av TSTimesheetLine-tabellen med TestLineString-fältet tillagt som ett anpassat fält.

![Radsträng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Använd kommandokedja på buildCustomFieldList-metoden i TSTimesheetSettings-klassen för att visa ett fält i tidrapportpost

Den här koden styr bildskärmsinställningarna för fältet i appen. Till exempel styr den typen av fält, etiketten, om fältet är obligatoriskt och vilket avsnitt fältet visas i.

I följande exempel visas ett sträng fält i tidposter. Det här fältet har två alternativ **Första alternativet** och **Andra alternativet** , som är tillgängliga via alternativknappar (radioknappar). Fältet i appen är associerat med fältet **TestLineString** som läggs till i tabellen TSTimesheetLine.

Observera att användningen av metoden **TSTimesheetCustomField::newFromMetatdata()** för att förenkla initieringen av de anpassade fältegenskaperna: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** och **numberOfDecimals**. Du kan även ange dessa parametrar manuellt, som du vill.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Använd kommandot på buildCustomFieldListForEntry-metoden i TSTimesheetEntry-klassen för att ange värden i tidrapportpost

Metoden **buildCustomFieldListForEntry** används för att ange värden för de sparade tidrapportraderna i mobilappen. En TSTimesheetTrans-post tas som en parameter. Fält från den posten kan användas för att fylla i det anpassade fältvärdet i appen.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Använd kommandot kedja i klassen TSTimesheetEntryService för att spara en tidrapportpost från appen tillbaka till databasen

Om du vill att ett anpassat fält ska sparas i databasen i normal användning måste du utöka flera metoder:

- Metoden **timesheetLineNeedsUpdating** används för att avgöra om radposten har ändrats av användaren i appen och måste sparas i databasen. Om prestanda inte är ett problem kan den här metoden förenklas så att den alltid returnerar **sant**.
- Metoderna **populateTimesheetLineFromEntryDuringCreate** och **populateTimesheetLineFromEntryDuringUpdate** kan utökas så att de anger värden i databas posten TSTimesheetLine från posten för TSTimesheetEntry data som tillhandahålls. I exemplet nedan ser du att mappningen mellan databasfält och transaktionsfält görs manuellt via X++ kod.
- Metoden **populateTimesheetWeekFromEntry** kan även utökas om det anpassade fält som mappas till objektet **TSTimesheetEntry** måste skriva tillbaka till TSTimesheetLineweek-databastabellen.

> [!NOTE]
> I följande exempel sparas värdet **firstOption** eller **secondOption** som användaren väljer i databasen som ett värde för rådatasträngar. Om databasfältet är ett fält av typen **Enum** kan dessa värden mappas manuellt till ett enum-värde och sedan sparas i ett enum-fält i databastabellen.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Visa ett anpassat fält i avsnittet tidrapporthuvud

Nedan visas en skärmdump från mobilappen för en användare som visar en tidrapport. Knappen "Mer information" har markerats i det övre högra hörnet för att visa alternativet "Visa mer information".  

![Visa kommandot för mer information](media/show-more.png)

Nedan följer en skärmdump från mobilappen som visar avsnittet "Mer" i en tidrapport. Ett anpassat fält som heter "Utnyttjandegraden för denna tidrapport (beräknat anpassat fält)" har lagts till i rubriken för tidrapport. Ett skrivskyddat värde på "0,667" har angetts för det anpassade fältet.

![Avsnittet Mer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Utöka tabellen TSTimesheetTable så att den har ett anpassat fält

I vanliga situationer är det troligt att data för ett anpassat fält i avsnittet rubrik kommer att dras från tabellen TSTimesheetHeader. Andra tabeller kan dock användas om data kan hämtas baserat på en TSTimesheetTable-post som tillhandahålls eller om den inte har ett specifikt postkontext (till exempel om fältet är skrivskyddat i projektparametrarna) .

Observera att anpassade fält inte behöver ha några säkerhetsposter i databasen. De kan skapas dynamiskt utifrån X++ logik. I exemplet nedan visas den här metoden.

Fält i rubrikavsnittet är alltid skrivskyddade i appen.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Använd kommandokedja på buildCustomFieldList-metoden i TSTimesheetSettings-klassen för att visa ett fält i avsnittet rubrik

Den här koden styr bildskärmsinställningarna för fältet i appen. Till exempel styr den typen av fält, etiketten, om fältet är obligatoriskt och vilket avsnitt fältet visas i.

I följande exempel visas ett beräknat värde i avsnittet rubrik i appen.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Använd kommandot på buildCustomFieldListForHeader-metoden i TSTimesheetDetails-klassen för att fylla i tidrapportens detaljer

Metoden **buildCustomFieldListForHeader** används för att fylla i tidsrapportens rubrikinformation i mobilappen. En TSTimesheetTable-post tas som en parameter. Fält från den posten kan användas för att fylla i det anpassade fältvärdet i appen. Följande exempel läser inga värden från databasen. I stället använder den X++ logik för att skapa ett beräknat värde som sedan visas i appen.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Andra konfigurations- och utökningsmöjligheter

### <a name="adding-additional-validation-for-the-app"></a>Lägga till ytterligare verifiering för appen

Befintlig logik för tidrapportfunktioner på databasnivå fungerar fortfarande som förväntat. Om du vill avbryta genomförandet av spara eller skicka åtgärden och visa ett visst felmeddelande kan du lägga till **utlösa fel ("meddelande till användare")** till koden via en kedja med kommandotillägg. Här är tre exempel på användbara utökningsmetoder:

- Om **validateWrite** i TSTimesheetLine-tabellen returnerar **falsk** under en spara-åtgärd för en tidrapportrad visas ett felmeddelande i mobilappen.
- Om **validateSubmit** i TSTimesheetTable-tabellen returnerar **falsk** under inlämning av tidrapport i appen visas ett felmeddelande för användaren.
- Logik som fyller i fält (till exempel **radegenskap** ) under metoden **infoga** på TSTimesheetLine-tabellen, körs fortfarande.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Dölja och markera färdiga fält som är skrivskyddade via konfiguration

Från projektparametrar kan du göra fält som inte är skrivskyddade eller dolda i mobilappen. Ange alternativen i avsnittet **Mobila tidrapporter** på fliken **Tidrapporter** för sidan **Projektledning och redovisningsparametrar**.

![Projektparametrar](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Ändra vilka aktiviteter som är tillgängliga för markering via tillägg

Aktiviteterna som är tillgängliga för urval för ett projekt fylls i via metoderna **getActivitiesForProject()** och **getActivityQuery()** i klassen **TsTimesheetProjectService**. Du kan använda kommandokedja för att ändra det här beteendet så att det överensstämmer med affärsscenariot för de aktiviteter som är tillgängliga för markering för ett visst projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Ange en standardkategori för projekt i tidrapportposter

Inmatning av en standardprojektkategori i tidrapportposter sker på tre nivåer. Du kan använda kommandokedja för att utöka beteendet på någon av eller alla de här nivåerna för att uppnå det önskade beteendet. Följande hierarki används:

1. I appen görs ett försök att lägga till standardkategori från projektresursen. Den här standardkategorin anges i metoderna **getCurrentUserResource** och **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.
2. Om standardkategorin inte visas på projektresursnivån försöker appen att hämta den från projektaktiviteten. Den här standardkategorin anges i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.
3. Om standardkategorin inte visas på projektetaktivitetsnivå, standardkategorin som den hämtade från projektparametrarna. Den här standardkategorin anges i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]