---
title: Inleverera artiklar på inköpsorder från artikelbehov
description: I den här artikeln beskrivs proceduren för att ta emot artiklar i en inköpsorder från ett artikelbehov.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbe15fac325ad00bdd2f2fc6ddf3ae15df45271
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929558"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Inleverera artiklar på inköpsorder från artikelbehov

[!include [banner](../../includes/banner.md)]

I den här artikeln beskrivs proceduren för att ta emot artiklar i en inköpsorder från ett artikelbehov.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]