---
title: Skapa koncerninterna kund- och leverantörsfakturor
description: Detta ämne innehåller information om hur du skapar koncerninterna kund- och leverantörsfakturor.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287485"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Skapa koncerninterna kund- och leverantörsfakturor

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En projektrevisor i en utlånande juridisk person skapar en koncernintern kundfaktura för de projektkostnader som överförs till den låntagande enheten. När den koncerninterna kundfakturan har godkänts och bokförts skickar den utlånande juridiska personen den koncerninterna fakturan till den låntagande juridiska personen.

Projektrevisorn för den utlånande juridiska personen kan ställa in en batchprocess för att generera koncerninterna fakturor på återkommande basis. Projektrevisorn anger kriterierna, till exempel specifika projekt, för att skapa koncerninterna fakturor i batch.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Skapa en koncernintern kundfaktura manuellt för projekttransaktioner 

Använd denna procedur för att skapa en koncernintern kundfaktura manuellt för projekttransaktioner. Sök efter timmar som bokförts av anställda på projekt i de låntagande juridiska personerna och för utgifter som uppstått på grund av din juridiska person på uppdrag av låntagande juridiska personer. Du kan söka efter den juridiska personens namn, projektkontraktsnummer, projektnummer, datumintervall eller valfri kombination av dessa alternativ. I sökresultatet väljer du de transaktioner som ska läggas till i en koncernintern faktura.

1. I Dynamics 365 Finance går du till **Projektledning och redovisning** > **Projektfakturor** > **Koncerninterna kundfakturor**. På listsidan **Koncerninterna kundfakturor** anger du **Ny** i åtgärdsfönstret.
2. På sidan **Skapa koncernintern faktura** väljer du en låntagande juridisk person i fältet **Juridisk person**.
3. Valfritt: Ange ett visst projektkontrakt och projektnummer.
4. Begränsa sökningen genom att välja ett datumintervall. Ange specifika datum i fälten **Startdatum** och **Slutdatum**. Endast koncerninterna transaktioner som bokförs inom detta datumintervall visas i sökresultaten.
5. Ange **Avancerad journalsradsparameter för projekt** som **Ja** och välj sedan **Sök**.
6. Välj de transaktioner som ska ingå i det koncerninterna fakturaförslaget i sökresultatet och välj sedan **OK**.
7. På sidan **Koncernintern kundfaktura** visas de koncerninterna projekttransaktioner som du har valt bland sökresultaten. Gör så här om du vill ändra transaktionerna innan du skickar fakturan till den låntagande juridiska personen:
  
    1. Öppna sidan **Skapa fakturaförslag**. Välj ytterligare koncerninterna transaktioner för den aktuella fakturan och välj sedan **Lägg till rad**.
    2. Om du vill ta bort en rad markerar du den och klickar sedan på **Ta bort**.
    3. Visa kommentarer, orsaker, ekonomiska dimensioner och annan information om en vald rad på snabbfliken **Fakturarader**.
    
8. Välj **Bokför** i åtgärdsfönstret om du vill bokföra den koncerninterna kundfakturan.

> [!NOTE]
> Om organisationen kräver att koncerninterna fakturor granskas innan de bokförs kanske en systemadministratör skapar ett arbetsflöde för koncerninterna fakturor. Om ett arbetsflöde inte har ställts in för koncerninterna fakturor kan du bokföra den koncerninterna fakturan.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Skapa ett batchjobb för koncerninterna fakturor

Du kan skapa flera koncerninterna fakturor samtidigt för alla låntagande juridiska personer. Med hjälp av sökfunktioner kan du till exempel söka efter alla transaktioner som bokförs av låntagande medarbetare och som är relaterade till projekt som hanteras av andra juridiska personer. Du kan sedan skapa en koncernintern faktura för de transaktioner som tillhandahålls i sökresultatet för varje enskild låntagande juridisk person.

1. Gå till **Projektledning och redovisning** > **Periodisk** > **Projektfakturor** > **Skapa koncerninterna kundfakturor**.
2. På sidan **Skapa koncerninterna kundfakturor** väljer du den juridiska person du vill fakturera i fältet **Företag**. Om du inte väljer ett företag visas alla transaktioner som uppfyller sökkriterierna för alla låntagande juridiska personer.
3. Under **Skapa en faktura per** väljer du om du vill skapa en faktura för koncerninterna transaktioner baserat på ett projekt eller baserat på en låntagande juridisk person.
4. Valfritt: Om du vill välja ett visst projekt och ett visst projektkontrakt som koncerninterna fakturor ska skapas för klickar du på **Välj**. På sidan **Fråga**, i fältet **Kriterier**, väljer du projektkontrakt, projektnummer eller båda, och klickar sedan på **OK**.
5. På fliken **Batch** skapar du en batchprocess för att skapa koncerninterna fakturor på återkommande basis. Mer information finns i [Skicka in ett batchbearbetningsjobb från ett formulär](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Välj **Bokför** i åtgärdsfönstret om du vill bokföra de koncerninterna kundfakturorna.

> [!NOTE]
> Om organisationen kräver att koncerninterna fakturor granskas innan de bokförs kanske en systemadministratör skapar ett arbetsflöde för koncerninterna fakturor. Om ett arbetsflöde inte har skapats för koncerninterna fakturor kan du bokföra de koncerninterna fakturorna.

## <a name="post-the-intercompany-vendor-invoice"></a>Bokför den koncerninterna leverantörsfakturan

En projektrevisor i den låntagande juridiska personen kan granska koncerninterna, väntande leverantörsfakturor när motsvarande koncerninterna kundfaktura bokförs. I Finance går du till **Leverantörsreskontra** > **Fakturor** > **Väntande leverantörsfaktura**. Det väntande fakturanumret kommer att matcha det koncerninterna kundfakturanumret. Kontrollera att fakturan är korrekt och bokför sedan fakturan. Bokföring av koncernintern leverantörsfaktura skapar en projektredovisning och en redovisningstransaktion som återspeglar transaktionskostnaderna i den låntagande juridiska personen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]