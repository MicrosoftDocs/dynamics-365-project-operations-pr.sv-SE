---
title: Konfigurera kreditkortsintegration
description: I det här ämnet beskrivs hur du importerar och underhåller utgifter för kreditkortstransaktioner.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276190"
---
# <a name="set-up-credit-card-integration"></a>Konfigurera kreditkortsintegration

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Utgift som är relaterade kreditkortstransaktioner kan ställas in så att de importeras automatiskt i ett återkommande schema. Transaktionerna kan också importeras manuellt när de krävs. Kreditkortstransaktionerna importeras via dataentiteten för kreditkortstransaktioner.

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