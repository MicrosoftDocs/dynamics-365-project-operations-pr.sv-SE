---
title: Importera och underhåll kreditkortstransaktioner
description: I det här ämnet beskrivs hur du importerar och underhåller utgifter för kreditkortstransaktioner. Dessa transaktioner kan ställas in så att de importeras automatiskt till ett återkommande schema, eller så kan de importeras manuellt efter behov.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7bf75c13bb190c7b992aa516f1593d886dfa604d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960449"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importera och underhåll kreditkortstransaktioner

Utgift som är relaterade kreditkortstransaktioner kan ställas in så att de importeras automatiskt i ett återkommande schema. Transaktionerna kan också importeras manuellt när de krävs. Kreditkortstransaktionerna importeras via dataentiteten för kreditkortstransaktioner.

Mer information om dataentiteter finns i [Dataentiteter](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importera kreditkortstransaktioner

1. På sidan **Kreditkortstransaktioner** väljer du **importera transaktioner**. Om du öppnar datahantering för första gången måste du uppdatera listan med dataentiteter i systemet innan du kan fortsätta.
2. I fältet **Namn** ange en unik beskrivning av import jobbet.
3. I fältet **Källdataformat** väljer du formatet för den fil som innehåller de kreditkortstransaktioner som ska importeras.
4. Välj **överför** välj sedan den fil du vill importera.
5. När filen har överförts kontrollerar du mappningen av kreditkortstransaktionsfilen och kolumnerna i dataentiteten för kreditkortstransaktioner genom att välja länken **Visa karta** på panelen. Om det uppstår mappningsfel eller om du måste ändra mappningen gör du mappningsändringarna antingen från fliken **Mappningsvisualisering** eller **Mappningsinformation**.
6. Om du vill automatisera kreditkortstransaktionerna väljer du **Skapa återkommande datajobb**. Du kan ange en återkommande tid som anger hur ofta kreditkortstransaktioner ska importeras. När du är klar väljer du **OK**.
7. Välj importera om du vill importera den valda filen nu **Import**.
8. Om det uppstår fel under importen kan du visa körningsloggen eller mellanlagringsmappen för att se de fel du måste åtgärda för att kunna garantera en lyckad import.

> [!NOTE]
> Om du måste importera fler än ett fil format måste du skapa separata importjobb för varje formattyp.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tilldela om kreditkortstransaktionerna för avslutade medarbetare

När en anställds post har avslutats inaktiveras den anställdes konto Active Directory Domain Services (AD DS) är inaktiverat. Det kan dock finnas aktiva kreditkortstransaktioner som fortfarande måste vara utgifter och ersättas. På sidan **Kreditkortstransaktioner** kan du omtilldela medarbetaren för en kreditkortstransaktion där den associerade medarbetaren har avslutas.

Välj en eller flera kreditkortstransaktioner och välj sedan **tilldela om transaktioner**. Du kan sedan välja en annan medarbetare att tilldela kreditkortstransaktionerna till. När kreditkortstransaktionerna har omtilldelats kan de väljas för en utgiftsrapport och betalas i den normala processen för återbetalning av utgiftsrapporter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]