---
title: Inleverera artiklar på inköpsorder från artikelbehov
description: I den här ämne beskrivs hur du tar emot artiklar på en inköpsorder från ett artikelbehov.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085707"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Inleverera artiklar på inköpsorder från artikelbehov

[!include [banner](../../includes/banner.md)]

I den här ämne beskrivs hur du tar emot artiklar på en inköpsorder från ett artikelbehov.

Om du använder ett artikelbehov i stället för en artikeltransaktion kan du planera för leverans precis innan artikeln faktiskt används, skapa en inköpsorder, ta med artikeln i ramverket för handelsavtal och ta med artikelbehovet i produktionsplaneringen. 

I den här uppgiften används USSI-datauppsättningen.

1. I navigerings fönstret går du till **moduler > projektledning och redovisning > projekt > alla projekt**.
2. Klicka på länken i önskad rad i listan.
3. Välj plan i åtgärdsrutan **åtgärd**.
4. Välj **artikelkrav**.
5. Välj **Nytt**.
6. Ange eller välj ett värde i den nya raden i fältet **artikelnummer**.
7. I fältet **Kvantitet** anger du ett nummer.
8. Välj **Spara**.
9. Välj plan i åtgärdsrutan **Hantera**.
10. Välj **Funktioner**.
11. Välj **Skapa en ny inköpsorder**.
12. Markera kryssrutan **Inkludera alla**.
13. I fältet **Leverantörskonto** field, enter or select a value.
14. Välj **OK**.
15. I navigeringsfönstret går du till **moduler > leverantörsreskontra > inköpsorder > alla inköpsorder**.
16. Klicka på länken i önskad rad i listan.
17. Välj plan i åtgärdsrutan **Köpa**.
18. Välj **Bekräfta**.
19. Välj plan i åtgärdsrutan **Ta emot**.
20. Välj **Produktinleverans**.
21. I fältet **Produktinleverans** skriver du ett värde.
22. Välj **OK**.
