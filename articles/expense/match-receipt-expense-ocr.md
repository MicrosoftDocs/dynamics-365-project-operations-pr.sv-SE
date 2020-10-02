---
title: Matcha kvitto mot utgift med OCR
description: I den här ämne finns information om optisk teckeninläsning (OCR) av kvitton.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897023"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Matcha kvitto mot utgift med OCR

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Utgiftsposten har förbättrats med introduktionen av optisk teckeninläsning (OCR) för inleveranser. Den här funktionen är avsedd att förbättra användarupplevelsen när du skapar utgiftsrapporter.

## <a name="key-features"></a>Viktiga funktioner

- I systemet extraheras namn och datum för handlaren och det totala beloppet från kvitton.
- Systemet försöker att inte använda ej bifogade kvitton på icke-anslutna utgiftstransaktioner.
- Du kan skapa manuellt registrerade utgiftstransaktioner från kvitton.

## <a name="attach-receipts-to-an-expense-report"></a>Bifoga kvitton till en utgiftsrapport

Om du vill automatiskt bifoga kvitton som inkluderar kreditkortstransaktioner när en utgiftsrapport skapas utför du följande steg.

  1. Öppna arbetsytan för **utgiftshantering**.
  2. På fliken **Kvitton** kontrollerar du att det finns ej bifogade kvitton. Du kan även överföra kvitton på fliken **Kvitton**.
  3. På fliken **Utgifter** kontrollerar du att det finns ej bifogade utgifter. Vanligtvis importerar utgiftsadministratören dessa utgifter från kreditkortsutfärdaren.
  4. Välj **ny utgiftsrapport**. Observera att du även kan ta med utgifter och inleveranser när du skapar en utgiftsrapport. Om du lägger till både utgifter och inleveranser utlöses automatisk matchning av inleveranser mot utgifterna.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Skapa eller matcha kvitton till en utgiftsrapport
Följ stegen nedan om du vill skapa en utgift eller matcha en kostnad från ett kvitto.

  1. På en utgiftsrapport, på fliken **Kvitton** bifogar du ett kvitto genom att välja **Lägg till kvitton**.
  2. Under kvittots uppladdade bild ser du alternativen **Skapa** och **Matcha**.

      - Välj **Skapa** om du vill skapa en manuellt registrerad utgiftstransaktion och fyll i värdena som ska extraheras från kvittot.
      - Om du väljer **Matcha** görs ett försök att matcha en befintlig utgift mot kvittot.

## <a name="installation"></a>Installation

Om du vill använda de här avancerade utgiftsfunktionerna installerar du tillägget utgiftshanteringstjänst för Microsoft Dynamics 365 Finance och aktiverar funktionerna i din instans. Du kan komma åt tillägget från projektet i Microsoft Dynamics Lifecycle Services (LCS).

1. Logga in på LCS och öppna den önskade miljön.
2. Gå till **Alla detaljer**.
3. Välj **Bibehåll** eller bläddra ned till snabbfliken **Miljötillägg**.
4. Välj **Installera ett nytt tillägg**.
5. Välj **utgiftshanteringstjänst**.
6. Följ anvisningarna i installationsguiden och godkänn villkoren.
7. Välj **Installera**.

Arbetsytan **Funktionshantering** aktiverar du följande funktioner:

- Ny typ av utgiftsrapporter
- Matcha automatiskt och skapa utgift från kvitto

När du aktiverar de här funktionerna utförs följande åtgärder:

- Den befintliga arbetsytan **utgiftshantering** ersätts med den nya arbetsytan.
- Ett nytt menyobjekt för synlighet för utgiftsfält läggs till.
- Du kan fortfarande öppna sidan tidigare sidan **Utgiftsrapporter** genom att gå till **Utgiftshantering > Mina utgifter > Utgiftsrapporter**.
- Arbetsflöden och eventuella godkännanden går fortfarande till sidan befintliga utgiftsrapporter.
- Kvitton bearbetas med hjälp av Microsoft Azure Cognitive Services och metadata extraheras och läggs till.
- Ett alternativ läggs till som gör att du kan skapa en utgiftsrapport som innehåller ej bifogade kvitton.
- Ett alternativ som läggs till i utgiftsrapporter innebär att du kan skapa en utgiftsrad från en inleverans eller att matcha en befintlig inleverans till en befintlig utgiftsrad.

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

**Används mina data för modellerna i Microsoft?**

Nej, Microsoft har byggt en allmän maskininlärningsmodell för mottagande bearbetningstjänst. Den här modellen bygger inte på de kvitton som du har överfört.

**Var är den här funktionen tillgänglig och bearbetad?**

USA stöds för närvarande.

**Var hamnar mina kvitton?**

Finans ska kontakta Cognitive Services för att extrahera fältdata. Cognitive Services behåller en kopia av ditt kvitto i upp till 24 timmar under bearbetningen. När bearbetningen har slutförts tas kvittot bort av Cognitive Services. Kvitton lagras fortfarande i Finance.

Mer information finns i [Aktivera kvittoförståelse med formigenkänningens nya förmåga](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
