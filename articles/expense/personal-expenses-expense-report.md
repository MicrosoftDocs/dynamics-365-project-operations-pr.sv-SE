---
title: Arbeta med privata utgifter i en utgiftsrapport
description: Detta ämne innehåller information om hur du arbetar med personliga utgifter som anställda har när de reser i affärssyfte.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993173"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Arbeta med privata utgifter i en utgiftsrapport

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Under resor kan en anställd debitera sina personliga utgifter på företagets kreditkort. Om en process inte har definierats för hantering av personliga utgifter kan godkännandeprocessen för utgiftsrapporten komma att avbrytas när en anställd skickar in sin specificerade utgiftsrapport.

Du kan använda två metoder för att arbeta med en anställds personliga utgifter:

  - **Betalas av den anställde**: Din organisation betalar inte privata utgifter som visas på fakturan för företagskreditkortet. I stället betalar den anställde kreditkortsleverantören direkt för kostnaderna. 
  - **Betald av företag**: Organisationen betalar den fullständiga fakturan för företagets kreditkort och debiterar sedan den anställdes konto för de personliga kostnaderna.

Du kan välja vilken metod som ska användas av organisationen på sidan **Parametrar för utgiftshantering**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Aktivera funktionen dela utgift när fältet för personligt belopp har ett definierat värde

Funktionen **Aktivera funktionen dela utgift när fältet för personligt belopp har ett definierat värde** gäller endast utgiftsrapporter som har godkänts genom ett arbetsflöde på radnivå. Rapporter godkänns genom att gå till **Bearbeta utgiftsrapporter** > **Utgiftsrapporter som har tilldelats mig** > **Öppna utgiftsrapport**. 

Om du vill aktivera den här funktionen, går du till **Arbetsytor** > **Funktionshanterring**, väljer **Aktivera funktionen dela utgift när fältet personligt belopp har ett definierat värde** och väljer sedan **Aktivera nu**. 

När funktionen har aktiverats skapar utgiftsrader som använder funktionen två rader när rapporten skickas. Två rader skapas så att godkännaren kan godkänna varje rad separat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
