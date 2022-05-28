---
title: Arbeta med privata utgifter i en utgiftsrapport
description: Detta ämne innehåller information om hur du arbetar med personliga utgifter som anställda har när de reser i affärssyfte.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: d35bf6960bb60e2ad4184e1b5f188695a3525be0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586550"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Arbeta med privata utgifter i en utgiftsrapport

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

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
