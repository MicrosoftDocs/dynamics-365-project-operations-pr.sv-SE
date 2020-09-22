---
title: Återkalla godkända tids- eller utgiftsposter
description: I det här ämnet finns information om hur du återkallar en tidigare godkänd tids- eller utgiftstransaktion.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756298"
---
# <a name="recall-approved-time-or-expense-entries"></a>Återkalla godkända tids- eller utgiftsposter

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En projektteammedlem eller en annan person som skickar en tids- eller utgiftspost kan återkalla den tids- eller utgiftsposten efter att den har godkänts. Processen för att återkalla en godkänd tids- eller utgiftspost består av två steg:

1. En avsändare begär återkallande.
2. En godkännare godkänner återkallningen.

## <a name="request-a-recall"></a>Begär en återkallelse

Följ stegen nedan om du vill begära en återkallelse för en godkänd tids- eller utgiftstransaktion.

1. För tidsposter går du till **projekt** \> **mitt arbete** \> **tidsposter**.

    –eller–

    För utgiftsposter går du till **projekt** \> **mitt arbete** \> **utgifter**.

2. För tidsposter, välj alla tidposter för en specifik kombination av ett projekt och en uppgift. I rutnätet kan du också välja enskilda celler för tid på ett visst datum för ett visst projekt.

    –eller–

    För utgiftsposter markerar du raden för den utgiftspost du vill återkalla.

3. Välj **återkalla**. En dialogruta för bekräftelse visas. Om de valda tids- och utgiftsposterna redan har godkänts uppmanas du att ange ett skäl till att återkalla det.
4. Ange ett skäl till återkallningen och klicka sedan på **OK** för att bekräfta åtgärden. Systemet skickar personen som godkände posterna en förfrågan om att godkänna återkallandet.

> [!NOTE]
> Även om godkända tids- och utgiftsposter kan återkallas, om en godkänd tid eller utgift redan har fakturerats till kunden, kan en återkallningsbegäran inte skapas. En användare som försöker skapa en återkallningsbegäran får ett meddelande om att tiden eller kostnaden inte kan återkallas eftersom den redan har fakturerats.

## <a name="approve-or-reject-a-recall-request"></a>Godkänna eller avvisa en återkallningsbegäran

Följ stegen nedan om du vill godkänna eller avvisa en återkallningsbegäran.

1. Gå till **Projekt** \> **Mitt arbete** \> **Godkännanden**.
2. På listsidan **godkännanden** ändrar du vyn till **återkallningsbegäran för godkännande**. En lista med skickade återkallningsbegäran visas.
3. Markera en eller flera poster och välj sedan antingen **Godkänn** eller **Avvisa**.
4. Om du valde **Godkänn** visas ett varningsmeddelande som förklarar hur godkännandet har påverkats. Bekräfta åtgärden genom att välja **OK**. Återkallningsbegäran är godkänd.

    –eller–

    Om du valde **avvisa** kommer återkallningsbegäran att avvisas.

> [!NOTE]
> När ett återkallande begärs, när ett återkallande godkänns kontrollerar systemet om det finns någon faktureringsaktivitet för tids- eller utgiftsposterna. Om en post redan har fakturerats eller om den är på en utkastfaktura får godkännaren ett fel meddelande om att tiden eller kostnaden inte kan godkännas för återkallande eftersom den redan har fakturerats.

## <a name="impact-of-a-recall-request"></a>Hur en återkallningsbegäran påverkas

När ett godkännande återkallas finns det både driftseffekter och ekonomiska effekter.

### <a name="operational-impact"></a>Driftseffekter

Om en återkallningsbegäran har godkänts markeras godkännandeposten som **avvisad**. Status för transaktionen ändras till antingen **returnerad** eller **avvisad** beroende på om det är en tids- eller utgiftspost.

Projektteammedlemmen kan visa poster, redigera och skicka om poster eller endast ta bort poster.

Om en återkallningsbegäran förblir **godkänd** och posten inte kan redigeras av projektteammedlemmen eller godkännaren för projektet.

### <a name="financial-impact"></a>Finansiella effekter

Om en återkallningsbegäran godkänns kommer motsvarande verkliga värden för kostnader och försäljning på följande sätt:

- Fältet **Justeringsstatus** uppdateras till **Justerad**.
- Fältet **Faktureringsstatus** uppdateras till **Annullerad**.

Sedan skapas återföringsposter i tabellen faktiska värden. Om du vill skapa återföringsposter kopieras systemet över fältvärdena från de ursprungliga värdena. De enda värden som inte kopieras över är antalet värden. De här värdena återförs i stället. Återförda faktiska värden skapas både för **kostnad** och för **fakturerade försäljningsvärden**. Fältet **justeringsstatus** på de återförda verkliga värdena ställs till att värdet **inte justerat** och fält **faktureringsstatus** är **annullerad**. På grund av dessa ändringar tar de registrerade utgifterna och den totala förväntande omsättningen kommer inte längre att räknas för de belopp som dessa faktiska värden representerar.

Om en återkallningsbegäran avslås påverkas inte projektets ekonomiska påverkan.

## <a name="changes-to-time-entry-records"></a>Ändringar i tidsposter

Följande illustration visar de ändringar som inträffar för godkända tidsposter när de återkallas.

![Tidpostens tillståndsövergångar](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Ändringar i utgiftsposter

Följande illustration visar de ändringar som inträffar för godkända utgiftsposter när de återkallas.

![Utgiftspostens tillståndsövergångar](media/ExpenseEntryStateTransitions.png)
