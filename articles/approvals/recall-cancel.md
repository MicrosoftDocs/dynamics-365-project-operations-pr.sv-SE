---
title: Återkalla tidigare godkända poster
description: I denna artikel förklaras hur en projektteammedlem kan begära återkallande av tidigare skickade och godkända poster för tid, utgifter och materialanvändning, samt hur en projektledare kan godkänna eller avvisa förfrågningar om godkännande.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930386"
---
# <a name="recall-previously-approved-entries"></a>Återkalla tidigare godkända poster

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

En projektteammedlem som skickar en post om tid, utgift eller material kan återkalla denna post efter att den har godkänts. Återkallandeprocessen har två huvudsteg:

1. En avsändare begär återkallande.
2. En godkännare godkänner återkallandebegäran.

## <a name="request-a-recall"></a>Begär en återkallelse

Följ stegen nedan om du vill begära en återkallelse för godkända poster om tid, utgifter eller materialanvändning.

1. Följ ett av dessa steg beroende på den posttyp du vill återkalla:

    - För tidsposter går du till **Projekt** \> **Mitt arbete** \> **Tidspost** och väljer alla tidsposter för en specifik kombination av projekt och uppgift. I rutnätet kan du också välja enskilda celler för tid på ett visst datum för ett visst projekt.
    - För utgiftsposter går du till **Projekt** \> **Mitt arbete** \> **Utgifter** och väljer raden för den utgiftspost du vill återkalla.
    - För poster för materialanvändning går du till **Projekt** \> **Mitt arbete** \> **Logg för materialanvändning** och väljer raden för den materialanvändning du vill återkalla.

2. Välj **återkalla**. En dialogruta för bekräftelse visas. Om de valda posterna för tid, utgift och materialanvändning redan har godkänts uppmanas du att ange ett skäl för återkallandet.
3. Ange ett skäl till återkallningen och klicka sedan på **OK** för att bekräfta åtgärden. Systemet skickar personen som godkände posterna en förfrågan om att godkänna återkallandet.

> [!IMPORTANT]
> Du kan inte skapa en begäran om återkallande för en tidigare godkänd tids-, utgifts- eller materialanvändningspost som redan har fakturerats kunden. Om du försöker göra detta kommer du att få ett meddelande om att posten för tid, utgift eller materialanvändning inte kan återkallas eftersom den redan har fakturerats. I så fall kan du endast begära ett återkallande av posten om en korrigeringsfaktura används för att utfärda en fullständig kreditering eller återbetalning till kunden för den ursprungliga fakturan.

## <a name="approve-or-reject-a-recall-request"></a>Godkänna eller avvisa en återkallningsbegäran

Följ stegen nedan om du vill godkänna eller avvisa en återkallningsbegäran.

1. Gå till **Projekt** \> **Mitt arbete** \> **Godkännanden**.
2. På listsidan **godkännanden** ändrar du vyn till **återkallningsbegäran för godkännande**. En lista med skickade återkallningsbegäran visas.
3. Markera en eller flera poster och välj sedan antingen **Godkänn** eller **Avvisa**.
4. Om du valde **Godkänn** visas ett varningsmeddelande som förklarar hur godkännandet har påverkats. Bekräfta åtgärden genom att välja **OK**. Återkallningsbegäran är godkänd.

    –eller–

    Om du valde **avvisa** kommer återkallningsbegäran att avvisas.

> [!IMPORTANT]
> När ett återkallande godkänns kommer - precis som när det begärs - systemet att kontrollera om det finns någon faktureringsaktivitet för tids-, utgifts- eller materialanvändningsposterna. Om en post redan har fakturerats eller om den finns i en utkastfaktura får godkännaren ett felmeddelande om att tiden eller utgiften inte kan godkännas för återkallande eftersom den redan har fakturerats. I så fall kan godkännaren begära ett återkallande endast om en korrigeringsfaktura används för att utfärda en fullständig kreditering eller återbetalning till kunden för den ursprungliga fakturan.

## <a name="impact-of-a-recall-request"></a>Hur en återkallningsbegäran påverkas

När ett godkännande återkallas finns det både driftseffekter och ekonomiska effekter.

### <a name="operational-impact"></a>Driftseffekter

Om en återkallningsbegäran har godkänts markeras godkännandeposten som **avvisad**. Status för posten ändras till antingen **Returnerad** eller **Avvisad** beroende på om posten är en tidspost, en utgiftspost eller en materialanvändningspost.

Projektteammedlemmen kan visa poster, redigera och skicka in poster på nytt, eller ta bort poster helt och hållet.

Om en återkallningsbegäran förblir **godkänd** och posten inte kan redigeras av projektteammedlemmen eller godkännaren för projektet.

### <a name="financial-impact"></a>Finansiella effekter

Om en återkallningsbegäran godkänns kommer motsvarande verkliga värden för kostnader och försäljning på följande sätt:

- Fältet **Justeringsstatus** uppdateras till **Justerad**.
- Fältet **Faktureringsstatus** uppdateras till **Annullerad**.

Sedan skapas återföringsposter i tabellen faktiska värden. Om du vill skapa återföringsposter kopieras systemet över fältvärdena från de ursprungliga värdena. De enda värden som inte kopieras över är antalet värden. De här värdena återförs i stället. Återförda faktiska värden skapas både för **kostnad** och för **fakturerade försäljningsvärden**. Fältet **justeringsstatus** på de återförda verkliga värdena ställs till att värdet **inte justerat** och fält **faktureringsstatus** är **annullerad**. På grund av dessa ändringar tar de registrerade utgifterna och den totala förväntande omsättningen kommer inte längre att räknas för de belopp som dessa faktiska värden representerar.

Om en återkallningsbegäran avslås påverkas inte projektets ekonomiska påverkan.

## <a name="changes-to-time-entry-records"></a>Ändringar i tidsposter

Följande illustration visar de ändringar som inträffar för godkända tidsposter och motsvarande godkännandeposter när de återkallas.

![Tillståndsövergångar för post.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Ändringar i poster för utgift och materialanvändning

Följande illustration visar de ändringar som inträffar för godkända utgifts- och materialanvändningsposter, samt motsvarande godkännandeposter när de återkallas.

![Utgiftspostens tillståndsövergångar.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
