---
title: Konfigurera kreditkortsintegration
description: Den ämne förklarar hur du arbetar med utgiftsrelaterade kreditkortstransaktioner.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826278"
---
# <a name="set-up-credit-card-integration"></a>Konfigurera kreditkortsintegration

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Utgift som är relaterade kreditkortstransaktioner kan ställas in så att de importeras automatiskt i ett återkommande schema. Transaktionerna kan också importeras manuellt när de krävs. Kreditkortstransaktionerna importeras via dataentiteten för kreditkortstransaktioner.

## <a name="import-credit-card-transactions"></a>Importera kreditkortstransaktioner

Importera kreditkortstransaktioner genom att följa stegen nedan:

1. På sidan **Kreditkortstransaktioner** väljer du **importera transaktioner**. Om du öppnar datahantering för första gången måste systemet uppdatera listan med dataentiteter innan du kan fortsätta.
2. I fältet **Namn** ange en unik beskrivning för importjobbet.
3. I fältet **Källdataformat** väljer du formatet för den fil som innehåller de kreditkortstransaktioner som ska importeras.
4. Välj **överför** välj sedan den fil du vill importera.
5. När filen har överförts kontrollerar du mappningen av kreditkortstransaktionsfilen och kolumnerna i dataentiteten för kreditkortstransaktioner genom att välja länken **Visa karta** på panelen. Om det uppstår mappningsfel eller om du måste ändra mappningen gör du mappningsändringarna antingen från fliken **Mappningsvisualisering** eller **Mappningsinformation**.
6. Om du vill automatisera kreditkortstransaktionerna väljer du **Skapa återkommande datajobb**. Du kan ange en återkommande tid som anger hur ofta kreditkortstransaktioner ska importeras. När du är klar väljer du **OK**.
7. Välj importera om du vill importera den valda filen nu **Import**.
8. Om det uppstår fel under importen kan du visa körningsloggen eller testdata och se vilka fel du måste åtgärda för att importen ska lyckas.

> [!NOTE]
> Om du måste importera fler än ett filformat måste du skapa separata importjobb för varje formattyp.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tilldela om kreditkortstransaktionerna för avslutade medarbetare

När en anställds post har avslutats inaktiveras den anställdes Active Directory Domain Services (AD DS)-konto. Det kan dock finnas aktiva kreditkortstransaktioner som fortfarande måste vara utgifter och ersättas. På sidan **Kreditkortstransaktioner** kan du tilldela om den anställde för alla kreditkortstransaktioner där den associerade medarbetaren har avslutats.

Välj en eller flera kreditkortstransaktioner och välj sedan **tilldela om transaktioner**. Du kan sedan välja en annan medarbetare att tilldela kreditkortstransaktionerna till. När kreditkortstransaktionerna har omtilldelats kan de väljas för en utgiftsrapport och betalas i den normala processen för återbetalning av utgiftsrapporter.

## <a name="delete-credit-card-transactions"></a>Ta bort kreditkortstransaktioner 

Ibland, efter att kreditkortstransaktioner har importerats, kan vissa transaktioner behöva raderas. Detta kan beror på att transaktionerna är dubbletter eller på att datan inte är korrekt. Administratörer kan använda funktionen **"Ta bort kreditkortstransaktioner"** för att välja och ta bort kreditkortstransaktioner som **inte är bifogad** till en utgiftsrapport. 

1. Gå till **Periodiska uppgifter** > **Ta bort kreditkortstransaktioner**.
2. Välj **Filter** och tillhandahåll information om vilka poster som ska ingå.
3. Välj **OK** för att ta bort posterna. 

## <a name="storing-credit-card-numbers"></a>Lagra kreditkortsnummer

Det finns tre alternativ för att lagra kreditkortsnummer. Kreditkortsnummer lagras på sidan **Parametrar för utgiftshantering**.

- **Förhindra kortnummerinmatning** – kreditkortsnummer lagras inte.
- **"Hasha" kortnummer (lagra de sista fyra siffrorna)** – De sista fyra siffrorna i kreditkortsnummer lagras i krypterat format.
- **Lagra kortnummer** – kreditkortsnummer lagras i ett okrypterat format. Detta alternativ överensstämmer inte med datasäkerhetsstandarden (DSS) för betalkortsbranschen (PCI). För att organisationen ska uppfylla PCI DSS-regelverken bör därför organisationsadministratörerna välja att antingen inte lagra kreditkortsnummer eller att lagra hash-kortnummer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
