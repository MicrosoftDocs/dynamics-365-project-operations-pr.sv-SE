---
title: Bearbetning av utgiftskvitto
description: I den här ämne finns information om optisk teckeninläsning (OCR) av kvitton. Den här funktionen är avsedd att förbättra användarupplevelsen när du skapar utgiftsrapporter i Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993528"
---
# <a name="expense-receipt-processing"></a>Bearbetning av utgiftskvitto

Utgiftsposten har förbättrats med introduktionen av optisk teckeninläsning (OCR) för inleveranser. Den här funktionen är avsedd att förbättra användarupplevelsen när du skapar utgiftsrapporter.

## <a name="key-features"></a>Viktiga funktioner

- Namn och datum för återförsäljaren och det totala beloppet extraheras från kvitton.
- Den här funktionen försöker att matcha ej bifogade kvitton på ej bifogade utgiftstransaktioner.
- Användare kan skapa manuellt registrerade utgiftstransaktioner från kvitton.

## <a name="usage-examples"></a>Användningsexempel

Om du vill automatiskt bifoga kvitton som inkluderar kreditkortstransaktioner när en utgiftsrapport skapas gör du följande:

  1. Öppna arbetsytan för **utgiftshantering**.
  2. På fliken **Kvitton** kontrollerar du att det finns ej bifogade kvitton. Du kan även överföra kvitton på fliken **Kvitton**.
  3. På fliken **Utgifter** kontrollerar du att det finns ej bifogade utgifter. Vanligtvis importerar utgiftsadministratören dessa utgifter från kreditkortsutfärdaren.
  4. Välj **ny utgiftsrapport**. Observera att du även kan ta med utgifter och inleveranser när du skapar en utgiftsrapport. Om du lägger till både utgifter och inleveranser utlöses automatisk matchning av inleveranser mot utgifterna.

Följ stegen nedan om du vill skapa en utgift eller matcha en utgift från ett kvitto:

  1. På en utgiftsrapport, på fliken **Kvitton** bifogar du ett kvitto genom att välja **Lägg till kvitton**.
  2. Under kvittots uppladdade bild ser du alternativen **Skapa** och **Matcha**.

      - Välj **Skapa** om du vill skapa en manuellt registrerad utgiftstransaktion och fyll i värdena som ska extraheras från kvittot.
      - Om du väljer **Matcha** görs ett försök att matcha en befintlig utgift mot kvittot.

## <a name="installation"></a>Installation

Den här funktionen fungerar tillsammans med funktionen **Ny typ av utgiftsrapporter** som hjälper dig att förenkla utgiftsupplevelsen. Den här funktionen är endast tillgänglig för nivå 2+-miljöer, som är Sandbox och produktion.

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

Mer information om funktionen Ny typ av utgiftsrapporter finns i [Ny typ av utgiftsrapporter](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

**Används mina data för modellerna i Microsoft?**

Nej, Microsoft har byggt en allmän maskininlärningsmodell för mottagande bearbetningstjänst. Den här modellen bygger inte på de kvitton som du har överfört.

**Var är den här funktionen tillgänglig och bearbetad?**

USA stöds för närvarande.

**Var hamnar mina kvitton?**

Finans ska kontakta Cognitive Services för att extrahera fältdata. Cognitive Services behåller en kopia av ditt kvitto i upp till 24 timmar under bearbetningen. När bearbetningen har slutförts tas kvittot bort av Cognitive Services. Kvitton lagras fortfarande i Finance.

Mer information finns i [Aktivera kvittoförståelse med formigenkänningens nya förmåga](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]