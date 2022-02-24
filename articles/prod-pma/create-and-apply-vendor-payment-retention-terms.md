---
title: Skapa och tillämpa villkor för innehållen leverantörsbetalning
description: I det här ämnet finns information om hur du konfigurerar och upprätthåller villkor för innehållen leverantörsbetalning.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270970"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Skapa och tillämpa villkor för innehållen leverantörsbetalning

[!include [banner](../includes/banner.md)] 

Det är användbart att konfigurera villkor för innehållen leverantörsbetalning för ett projekt när organisationen vill hålla inne del av betalningen som ska göras till en leverantör. T.ex. när du vill spärra betalning till en leverantör tills de produkter som levererats uppfyller dina förväntningar. Villkor för innehållen leverantörsbetalning kan anges när du förhandlar ett leverantörskontrakt.

## <a name="create-vendor-payment-retention-terms"></a>Skapa villkor för innehållen leverantörsbetalning

Du kan ange procentandelen av leverantörsbetalningen som ska hållas inne och procentandelen av de belopp som har hållits inne tidigare och som ska släppas. Belopp hålls automatiskt inne på leverantörsfakturor tills kontraktet når det angivna slutsteget. När du har konfigurerat villkoren för kvarhållande kan du tillämpa dem på vilket projekt som helst för den leverantören.

Följ stegen nedan om du vill konfigurera och upprätthålla villkor för innehållen leverantörsbetalning. 

1. Gå till **Projekthantering och redovisning** > **Kvarhållning** > **Villkor för innehållen leverantörsbetalning**.
2. Välj **Ny** om du vill lägga till ett nytt villkor för kvarhållande för leverantören. Värdet **Regel-ID** för det nya villkoret anges automatiskt. 
3. Ange en kort beskrivning i fältet **Beskrivning** och på snabbfliken **Villkor** väljer du **Lägg till rad** för att ange villkorsvärden för följande:

   - **Procentandel av levererade enheter**: Ange en procentandel som slutförts av villkoret. Belopp hålls automatiskt inne på leverantörsfakturor tills projektslutförandet är lika med den specificerade procentandelen. Om du till exempel anger 50,00 kvarhålls beloppen tills projektet har slutförts till 50 procent.
   - **Procent att hålla inne**: Ange en procentandel av leverantörsfakturans belopp som ska hållas inne. Om du till exempel anger 10,00 kvarhålls 10 procent av beloppet på en leverantörsfaktura tills projektet når slutförandeprocenten som angetts i fältet **Procentandel av levererande enheter**.
   - **Procentandel som ska släppas**: Välj **Lägg till rad** om du vill ange en procentandel av tidigare kvarhållna belopp som ska frisläppas för den valda slutförandenivån av projektet.

> [!NOTE]
> Om du har fler än en milstolpe för olika nivåer av projektslutförande anger du en separat rad för villkor för kvarhållande för varje kvarhållningsregel. Varje rad kan ange en annan kvarhållandeprocentandel och en annan procentandel för varje angiven nivå av projektets slutförande.

När du har skapat villkor för kvarhållande för en leverantör kan du tillämpa villkoren på ett projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Tillämpa villkor för leverantörskvarhållande på ett projekt

1. Gå till **Projekthantering och redovisning** > **Projekt** > **Alla projekt** och öppna ett projekt från projektets listsida.
2. Under snabbfliken **Leverantörsavtal** väljer du **Lägg till rad**.
3. I fältet **Kontokod** väljer du något av följande alternativ: 

   - **Tabell**: Villkoren för leverantörskvarhållande gäller för en enskild leverantör.
   - **Grupp**: Villkoren för leverantörskvarhållande gäller för alla leverantörer i en leverantörsgrupp.
   - **Alla**: Villkoren för leverantörskvarhållande gäller för alla leverantörer.

4. I fältet **Leverantör/leverantörsgrupp** väljer du den leverantör eller leverantörsgrupp som villkoren för leverantörskvarhållande gäller för. Om du valde **Alla** i föregående steg är detta fält inte tillgängligt.
5. I fältet **Villkor för leverantörskvarhållning** väljer du de kvarhållningsvillkor som du skapade i föregående procedur.
6. Om projektet även har ställts in för betala vid betalning (PWP) för leverantören anger du tröskelvärdet i procent för projektet i fältet **Tröskelvärdesprocent för PWP**.

Villkoren för leverantörskvarhållande visas även på inköpsorder som du skapar för leverantören.


[!INCLUDE[footer-include](../includes/footer-banner.md)]