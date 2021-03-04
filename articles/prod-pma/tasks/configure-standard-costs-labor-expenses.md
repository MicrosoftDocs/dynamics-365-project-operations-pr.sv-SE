---
title: Konfigurera standardkostnader för arbete och utgifter
description: I det här ämnet beskrivs hur du skapar standardkostnader för arbete och utgifter för ett projekt.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085597"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurera standardkostnader för arbete och utgifter

[!include [banner](../../includes/banner.md)]

I det här ämnet beskrivs hur du skapar standardkostnader för arbete och utgifter för ett projekt. I den här uppgiften används USSI-datauppsättningen.

1. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > självkostnad (timme)**.
2. Välj **Nytt**.
3. I fältet **Effektivt datum** anger du ett datum.
4. Ange ett nummer i fältet **självkostnad**. Du kan ange en standard självkostnad för projektkategorin, eller så kan du ange att en självkostnad ska vara efter arbetsnummer, projektnummer, kategori, datum eller någon kombination av dessa. Den självkostnad som används är den självkostnad som har den högsta detaljnivån.  
5. Välj **Spara**.
6. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > försäljningskostnad (timme)**.
7. Välj **Nytt**.
8. I fältet **Effektivt datum** anger du ett datum.
9. I fältet **Giltig för** , välj ett alternativ.
10. I fältet **Prissättning** anger du ett nummer. Du kan ange ett standard försäljningspris för timtransaktioner eller för en projektkategori. Du kan också ange försäljningspriser efter arbetsnummer, projektnummer, kategori, transaktionsdatum eller någon kombination av dessa. Det faktiska försäljningspriset, som används när en arbetare registrerar en transaktion i timjournalen, är försäljningspriset på den högsta detaljnivån. Om t.ex. både ett allmänt försäljningspris och ett arbetar försäljningspris är inställda används det arbetsspecifika försäljningspriset.  
11. Välj **Spara**.
12. Stäng sidan.
13. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > självkostnad (utgift)**.
14. Välj **Nytt**.
15. I fältet **Effektivt datum** anger du ett datum.
16. Ange ett nummer i fältet **självkostnad**. Du kan fylla i flera fält, men det är det minsta som krävs för att spara posten.  
17. Välj **Spara**.
18. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > försäljningspris (utgift)**.
19. Välj **Nytt**.
20. I fältet **Effektivt datum** anger du ett datum.
21. I fältet **Giltig för** , välj ett alternativ.
22. I fältet **Prissättning** anger du ett nummer. Det faktiska försäljningspriset, som används när en arbetare registrerar transaktioner i en utgiftsjournal, är försäljningspriset på den högsta detaljnivån. Om t.ex. både ett allmänt och ett arbetar försäljningspris är inställda används det arbetsspecifika försäljningspriset.  
23. Välj **Spara**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]